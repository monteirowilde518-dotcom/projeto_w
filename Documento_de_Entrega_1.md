Claro. Abaixo está a versão com linguagem mais simples, direta e objetiva, retirando todo o conteúdo relacionado a fotos.

# Documento de entrega

## [CABEÇALHO]

**Projeto:** Sistema de Gestão de Perdas – Supermercado  
**Documento:** Especificação de Requisitos Não Funcionais (RNF)  
**Equipe Responsável:** Grupo [3]  
**Líder de Área:** [Ed]  
**Data de Emissão:** [19/08/2026]  

***

# 1. INTRODUÇÃO E OBJETIVO

Este documento define os requisitos necessários para que o Sistema de Gestão de Perdas funcione com segurança, rapidez e estabilidade.

O sistema deverá processar as bipagens, integrar-se ao PDV, RMS e Totvs, manter o estoque atualizado, proteger os dados e permitir a recuperação das informações em caso de falhas.

***

# 2. DETALHAMENTO DOS REQUISITOS

| Requisito (RNF) | Descrição do Funcionamento | Métrica/Indicador de Sucesso |
|---|---|---|
| **Desempenho da Bipagem** | O sistema deverá processar cada bipagem e atualizar o estoque sem atrasos que prejudiquem a operação. | Cada bipagem deverá ser processada em até 2 segundos em condições normais de conexão. |
| **Capacidade de Armazenamento** | O servidor deverá armazenar os dados do sistema, os registros de perdas, os históricos de movimentação e os logs de auditoria. | O armazenamento deverá suportar o volume de dados previsto para a operação e permitir expansão futura. |
| **Escalabilidade – RN-07** | O sistema deverá permitir o cadastro de novas lojas e depósitos por configuração, sem necessidade de alterar o código ou realizar um novo desenvolvimento. | Uma nova loja ou depósito deverá ser incluído sem alteração do código-fonte. |
| **Separação por Loja e Depósito** | Os dados deverão ser separados logicamente por loja e depósito. Um usuário somente poderá acessar as unidades autorizadas para o seu perfil. | Nenhum usuário deverá consultar ou alterar dados de uma unidade não autorizada. |
| **Resiliência e Conexão** | Quando a conexão com o servidor for interrompida, os dados deverão ser salvos temporariamente no dispositivo. Quando a conexão voltar, o sistema deverá sincronizar os dados automaticamente. | A sincronização deverá ocorrer em até 2 segundos após o retorno da conexão. |
| **Controle de Acesso** | O sistema deverá verificar quem é o usuário, qual é o seu perfil e quais ações ele pode realizar. O acesso deverá ser negado quando não houver permissão definida. | 100% das operações protegidas deverão passar por autenticação e autorização. |
| **Política de Autenticação** | Cada usuário deverá possuir uma conta individual. O sistema deverá controlar senhas, tentativas inválidas, recuperação de acesso e encerramento de sessão. | Todos os usuários deverão possuir contas individuais. As tentativas inválidas deverão ser registradas. |
| **Integração com PDV, RMS e Totvs** | A comunicação com os sistemas externos deverá ocorrer por APIs protegidas. Cada sistema deverá utilizar uma identificação própria e permissões específicas. | 100% das APIs deverão validar a origem e a autorização da operação. |
| **Auditoria e Rastreabilidade** | O sistema deverá registrar acessos, falhas de login, alterações, perdas, bipagens, transferências, sincronizações e operações administrativas. | Todo evento importante deverá registrar responsável, data, hora, ação e resultado. |
| **Recuperação de Desastres** | O sistema deverá realizar backups automáticos para evitar a perda dos dados. O procedimento de restauração deverá ser testado regularmente. | Backup diário às 03:00h e restauração do sistema em até 4 horas após uma falha crítica. |
| **Proteção dos Backups** | Os arquivos de backup deverão ser acessíveis somente por pessoas autorizadas. As operações de backup e restauração deverão ser registradas. | 100% das restaurações deverão possuir registro do responsável, data, hora e resultado. |

O controle de acesso deverá seguir duas regras básicas: negar o acesso por padrão e liberar somente as permissões necessárias para cada função. Esse procedimento é conhecido como princípio do menor privilégio. [owasp](https://owasp.org/Top10/2025/pt-BR/A01_2025-Broken_Access_Control/)

***

# 3. MAPEAMENTO DE REGRAS DE NEGÓCIO

## RN-01 – Estoque Inteligente

Os requisitos de desempenho, sincronização e controle de acesso ajudam a manter o estoque atualizado e confiável.

A bipagem deverá ser processada rapidamente. Se a conexão falhar, o registro deverá ser salvo temporariamente e enviado ao servidor após o retorno do sinal.

O sistema também deverá evitar que a mesma bipagem seja processada duas vezes, pois isso poderia alterar o saldo incorretamente ou deixar o estoque negativo.

## RN-07 – Multiestoque

O sistema deverá manter saldos separados por loja e depósito.

Cada usuário deverá acessar somente as unidades autorizadas para o seu perfil. Por exemplo, um supervisor da Loja A poderá consultar e alterar informações da Loja A, mas não deverá acessar os dados da Loja B sem autorização.

As transferências entre lojas e depósitos deverão registrar:

- Unidade de origem;
- Unidade de destino;
- Produto movimentado;
- Quantidade;
- Usuário ou sistema responsável;
- Data e hora;
- Resultado da operação.

## Relação com a segurança técnica

A segurança técnica ajudará a cumprir as regras do projeto por meio de:

- Autenticação dos usuários;
- Autorização por perfil;
- Separação dos dados por unidade;
- Controle das integrações;
- Registro das operações;
- Proteção contra duplicidade;
- Backup e recuperação dos dados.

Caso existam outras regras oficiais no projeto, elas deverão ser acrescentadas nesta seção utilizando os códigos e nomes definidos pelo grupo.

***

# 4. INTEGRAÇÃO E SEGURANÇA

## Sistemas externos

O sistema deverá integrar-se ao PDV, RMS e Totvs por meio de APIs protegidas.

Cada sistema externo deverá possuir:

- Identificação própria;
- Credenciais exclusivas;
- Permissões específicas;
- Limite de operações;
- Registro das requisições;
- Controle contra duplicidade;
- Tratamento de falhas.

As integrações deverão realizar somente as ações necessárias.

| Sistema | Permissões previstas |
|---|---|
| **PDV** | Enviar vendas e consultar disponibilidade de produtos |
| **RMS/Totvs** | Enviar ou receber movimentações autorizadas |
| **Serviço de Relatórios** | Consultar dados para gerar relatórios |
| **Serviço de Sincronização** | Enviar registros pendentes e atualizar o status das operações |

Uma integração responsável apenas por enviar vendas não deverá ter permissão para excluir perdas, alterar usuários ou modificar configurações administrativas.

As APIs deverão verificar a autorização em cada operação protegida, e não somente no momento do login. [owasp](https://owasp.org/API-Security/editions/2019/pt-pt/dist/owasp-api-security-top-10.pdf)

## Autenticação

O sistema deverá utilizar contas individuais para os usuários.

A política de autenticação deverá definir:

- Regras para criação de senhas;
- Proibição do compartilhamento de contas;
- Registro de tentativas inválidas;
- Bloqueio temporário após várias tentativas incorretas;
- Recuperação segura de senha;
- Expiração de sessões inativas;
- Encerramento da sessão após o logout;
- Proteção das contas administrativas;
- Bloqueio de usuários que não precisam mais acessar o sistema.

As senhas não deverão ser armazenadas em texto puro.

## Perfis de acesso

| Perfil | Permissões principais |
|---|---|
| **Estoquista** | Consultar produtos e registrar operações permitidas |
| **Supervisor** | Consultar estoque e registrar perdas da unidade autorizada |
| **Gerente** | Consultar relatórios e acompanhar perdas das unidades sob sua responsabilidade |
| **TI/Segurança** | Administrar recursos técnicos e consultar registros de auditoria |
| **Administrador** | Gerenciar usuários, perfis e configurações críticas |

O sistema deverá verificar:

1. Quem é o usuário;
2. Qual é o seu perfil;
3. Qual loja ou depósito ele pode acessar;
4. Qual ação ele está tentando realizar.

## Controle de acesso

O sistema deverá seguir estas regras:

- Negar acessos que não tenham autorização definida;
- Conceder somente as permissões necessárias;
- Verificar as permissões no servidor e nas APIs;
- Separar funções operacionais e administrativas;
- Impedir alterações fora da unidade autorizada;
- Registrar mudanças de perfil e permissão;
- Revisar os acessos periodicamente.

A ANPD apresenta o controle de acesso como a combinação de autenticação, autorização e auditoria: autenticação identifica o usuário, autorização define o que ele pode fazer e auditoria registra o que foi feito. [gov](https://www.gov.br/mds/pt-br/acesso-a-informacao/lgpd/principios-da-lgpd)

## Privacidade e proteção de dados

O sistema deverá proteger os dados pessoais contra acesso indevido, perda, alteração, destruição ou divulgação não autorizada.

O acesso aos dados deverá ser limitado ao necessário para realizar cada atividade. Usuários não deverão consultar informações que não estejam relacionadas às suas funções ou unidades de trabalho.

Essa proteção está de acordo com o artigo 46 da LGPD, que exige medidas técnicas e administrativas para proteger dados pessoais. [planalto.gov](https://www.planalto.gov.br/ccivil_03/%5C_ato2015-2018/2018/Lei/L13709compilado.htm)

## Auditoria e logs

O sistema deverá registrar:

- Login realizado com sucesso;
- Tentativas de login inválidas;
- Acessos negados;
- Inclusões, alterações e exclusões;
- Bipagens processadas;
- Registros de perdas;
- Transferências entre unidades;
- Sincronizações;
- Falhas de integração;
- Alterações de usuários e permissões;
- Backups;
- Restaurações.

Os logs não deverão armazenar senhas, tokens completos ou outras informações sensíveis desnecessárias.

Cada registro deverá conter, sempre que possível:

- Usuário ou sistema responsável;
- Data;
- Hora;
- Ação executada;
- Recurso utilizado;
- Resultado da operação.

***

# 5. VALIDAÇÃO DO LÍDER DE ÁREA

**Revisão técnica realizada por:** [Nome do Líder]

**Parecer:**  

( ) Aprovado  
( ) Necessita Ajustes  

**Notas do Líder:**  

[Comentários sobre a qualidade da entrega, a clareza dos requisitos, a adequação das métricas e o atendimento às regras de negócio.]

**Assinatura do Líder:** ______________________________________

**Data da validação:** ____/____/________

***