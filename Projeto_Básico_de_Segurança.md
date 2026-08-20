# Projeto Básico de Segurança Física

## 1. Objetivo

Este projeto tem como objetivo proteger os funcionários, equipamentos, instalações e informações de uma empresa de desenvolvimento de software.

A empresa possui 50 funcionários, 40 notebooks, 10 computadores desktop, equipamentos de rede, uma sala de servidores, sistema interno e banco de dados de clientes. Parte dos funcionários trabalha presencialmente e parte remotamente.

O plano busca reduzir riscos como furto, perda de equipamentos, entrada de pessoas não autorizadas, incêndios, quedas de energia e vazamento de informações.



## 2. Identificação dos ativos

Ativos são todos os recursos importantes que a empresa precisa proteger.

| Ativo | Quantidade/descrição | Importância |
|---|---:|---|
| Funcionários | 50 pessoas | Alta |
| Notebooks corporativos | 40 unidades | Alta |
| Computadores desktop | 10 unidades | Média |
| Sala de servidores | Ambiente restrito | Muito alta |
| Servidores | Hospedam sistemas e dados | Muito alta |
| Sistema interno | Uso dos funcionários | Alta |
| Banco de dados de clientes | Dados pessoais e comerciais | Muito alta |
| Equipamentos de rede | Roteadores, switches, cabos e firewall | Alta |
| Backups | Cópias dos dados da empresa | Muito alta |
| Dispositivos removíveis | Pendrives e HDs externos autorizados | Média/alta |
| Documentos físicos | Contratos, relatórios e informações internas | Média/alta |



## 3. Principais ameaças

As principais situações que podem causar danos à empresa são:

- Furto ou perda de notebooks, computadores, pendrives e equipamentos de rede.
- Entrada de visitantes ou pessoas não autorizadas em áreas restritas.
- Incêndio na sala de servidores ou em outros setores.
- Queda de energia que desligue servidores e sistemas.
- Danos causados por água, infiltração, alagamento ou vazamento.
- Uso de pendrives desconhecidos ou pessoais, podendo levar vírus ou arquivos indevidos para os computadores.
- Funcionário remoto deixando o notebook exposto em locais públicos ou dentro de veículos.
- Acesso indevido ao banco de dados de clientes.
- Falta de backup ou backup que não funciona quando necessário.
- Danos físicos a cabos, roteadores, switches ou servidores.



## 4. Avaliação dos riscos

| Risco | Probabilidade | Impacto | Nível de risco | Medida principal |
|---|---|---|---|---|
| Furto de notebook | Média | Alta | Alto | Identificação, armário, termo de responsabilidade e bloqueio remoto |
| Entrada não autorizada | Média | Alta | Alto | Crachá, recepção, câmeras e controle de acesso |
| Incêndio na sala de servidores | Baixa | Muito alta | Alto | Detector de fumaça, extintor, alarme e plano de emergência |
| Queda de energia | Média | Alta | Alto | Nobreak, estabilização e gerador, se possível |
| Falha ou perda do banco de dados | Média | Muito alta | Alto | Backup diário, cópia externa e testes de restauração |
| Pendrive infectado ou perdido | Média | Alta | Alto | Uso somente de dispositivos autorizados e criptografados |
| Visitante em área restrita | Média | Média | Médio | Cadastro, crachá temporário e acompanhamento |
| Danos por água ou infiltração | Baixa | Alta | Médio | Sala elevada, sensores e inspeções periódicas |
| Danos a equipamentos de rede | Baixa | Alta | Médio | Rack fechado, organização e acesso limitado |

A empresa deve priorizar os riscos classificados como **altos**, pois podem interromper o funcionamento do negócio ou causar vazamento de dados de clientes.



## 5. Segurança do perímetro

O perímetro é a área externa e a entrada da empresa. Para protegê-lo, serão adotadas as seguintes medidas:

- Instalação de câmeras na entrada, corredores, estacionamento e áreas externas.
- Iluminação adequada nas entradas e áreas de circulação.
- Portas e portões resistentes, mantidos fechados fora do horário de atendimento.
- Sistema de alarme para horários em que a empresa estiver fechada.
- Recepção para identificar funcionários, visitantes, fornecedores e prestadores de serviço.
- Controle da entrada e saída de materiais, principalmente notebooks, servidores, monitores e equipamentos de rede.
- Manutenção das gravações das câmeras por um período definido pela empresa, por exemplo, 30 dias.
- Inspeção periódica de portas, fechaduras, janelas, câmeras e alarmes.



## 6. Controle de acesso

O acesso físico deve ser liberado de acordo com a função de cada pessoa.

| Local | Quem pode acessar | Forma de controle |
|---|---|---|
| Recepção e áreas comuns | Funcionários e visitantes autorizados | Crachá e registro na recepção |
| Área de trabalho | Funcionários | Crachá ou chave controlada |
| Sala de servidores | Equipe de TI e responsáveis autorizados | Cartão, biometria ou chave controlada |
| Sala de equipamentos de rede | Equipe de TI autorizada | Porta trancada e registro de acesso |
| Arquivo físico | Administração e pessoas autorizadas | Armário ou sala trancada |
| Área de backups | Equipe de TI autorizada | Armário fechado ou cofre |

Medidas gerais:

- Todos os funcionários devem usar crachá de identificação.
- As permissões de acesso devem seguir o princípio do menor privilégio: cada pessoa entra apenas onde precisa para executar seu trabalho.
- Chaves, cartões e senhas de acesso físico não podem ser emprestados.
- Quando um funcionário sair da empresa, seu crachá, chave e permissões devem ser cancelados imediatamente.
- A lista de pessoas autorizadas a entrar na sala de servidores deve ser revisada periodicamente.
- Entradas e saídas da sala de servidores devem ser registradas. O controle e o registro de acessos são práticas alinhadas às recomendações de proteção física do NIST.


## 7. Proteção da sala de servidores

A sala de servidores é um ambiente crítico, pois concentra sistemas, banco de dados e equipamentos de rede.

A empresa deve adotar as seguintes medidas:

- Manter a porta sempre trancada.
- Permitir acesso somente à equipe de TI e pessoas previamente autorizadas.
- Usar biometria, cartão de acesso ou chave com registro de retirada.
- Instalar câmeras na entrada da sala.
- Não permitir visitantes desacompanhados.
- Proibir alimentos, bebidas e objetos desnecessários no local.
- Utilizar rack fechado para servidores, switches, roteadores e firewall.
- Organizar e identificar cabos de energia e rede.
- Instalar detector de fumaça, extintor apropriado para equipamentos elétricos e alarme de incêndio.
- Manter ar-condicionado ou climatização adequada para evitar superaquecimento.
- Usar nobreak para evitar desligamento imediato em quedas de energia.
- Avaliar a instalação de gerador, caso a empresa dependa dos sistemas continuamente.
- Evitar que a sala fique próxima de banheiros, tubulações, janelas expostas ou locais com risco de infiltração.
- Fazer manutenção periódica dos equipamentos, da energia, do ar-condicionado e do sistema de prevenção de incêndio.



## 8. Segurança dos notebooks

Como há 40 notebooks e funcionários trabalham remotamente, esse ativo precisa de regras específicas.

- Todo notebook deve possuir número de patrimônio, etiqueta de identificação e registro do funcionário responsável.
- O funcionário deve assinar um termo de responsabilidade ao receber o notebook.
- O notebook não deve ser deixado sozinho em locais públicos, carros, salas abertas ou mesas sem supervisão.
- No escritório, notebooks sem uso devem ser guardados em armários trancados ou em local protegido.
- Em trabalho remoto, o equipamento deve ficar em local seguro, fora do alcance de terceiros não autorizados.
- O funcionário deve utilizar bloqueio de tela automático e senha de acesso.
- Em viagens ou deslocamentos, o notebook deve ser transportado em mochila apropriada.
- A empresa deve manter ferramenta de localização, bloqueio remoto e, quando possível, apagamento remoto de dados.
- Em caso de afastamento ou desligamento, o notebook deve ser devolvido ao setor de TI para conferência.

A CISA recomenda manter dispositivos bloqueados em áreas seguras quando não estão sob controle direto e evitar inserir mídias removíveis desconhecidas. 



## 9. Política para dispositivos removíveis

Dispositivos removíveis incluem pendrives, HDs externos, cartões de memória e outros meios usados para transportar arquivos.

A política da empresa será:

- É proibido usar pendrives pessoais em computadores corporativos sem autorização da equipe de TI.
- A empresa deve fornecer pendrives ou HDs externos autorizados quando houver necessidade de transferência de arquivos.
- Todo dispositivo corporativo deve ser identificado e registrado.
- Antes de ser usado, o dispositivo deve passar por verificação de segurança.
- Dados de clientes, códigos internos, senhas e backups não devem ser copiados para pendrives comuns.
- Quando for necessário transportar informação sensível, o dispositivo deve ser criptografado e protegido por senha.
- Pendrives e HDs externos devem ser guardados em armário trancado quando não estiverem em uso.
- Dispositivos danificados ou que não serão mais usados devem passar por apagamento seguro ou destruição física.
- É proibido conectar mídias desconhecidas encontradas fora da empresa.



## 10. Estratégia de backup

A empresa deve manter cópias de segurança para garantir a recuperação do sistema interno e do banco de dados de clientes.

| Item | Regra definida |
|---|---|
| Banco de dados de clientes | Backup diário automático |
| Sistema interno | Backup diário ou após atualizações importantes |
| Arquivos de projetos | Backup diário em servidor ou nuvem corporativa |
| Cópia externa | Manter uma cópia fora da sala de servidores, preferencialmente em nuvem ou outro local seguro |
| Proteção do backup | Criptografia, controle de acesso e armazenamento protegido |
| Teste de recuperação | Realizar testes mensais de restauração |
| Responsável | Equipe de TI |
| Retenção | Manter cópias diárias, semanais e mensais conforme necessidade da empresa |

A empresa deve seguir a ideia de manter mais de uma cópia dos dados e não deixar todas no mesmo local físico. O NIST recomenda realizar backups em frequência compatível com a necessidade de recuperação e armazenar cópias separadamente do sistema operacional, além de proteger a confidencialidade, integridade e disponibilidade dessas cópias.



## 11. Procedimentos para visitantes

Todo visitante, fornecedor ou técnico externo deve seguir estas regras:

1. Apresentar documento de identificação na recepção.
2. Informar nome, empresa, pessoa que será visitada, motivo da visita, horário de entrada e horário de saída.
3. Receber crachá temporário de visitante.
4. Permanecer acompanhado por um funcionário durante toda a visita.
5. Não acessar sozinho a sala de servidores, sala de rede, arquivos ou qualquer área restrita.
6. Não utilizar computadores, equipamentos de rede ou dispositivos removíveis sem autorização.
7. Não fotografar equipamentos, telas, documentos ou ambientes internos sem autorização.
8. Devolver o crachá temporário ao sair.



## 12. Procedimentos em caso de perda ou furto

Caso um notebook, desktop, pendrive, HD externo, documento ou equipamento de rede seja perdido ou furtado, deve-se seguir este procedimento:

1. O funcionário deve avisar imediatamente o gestor, a equipe de TI e o responsável pela segurança.
2. O caso deve ser registrado com data, horário, local, equipamento envolvido e descrição do ocorrido.
3. A equipe de TI deve identificar quais dados estavam no equipamento.
4. Se for notebook ou celular corporativo, a TI deve bloquear o acesso, revogar sessões ativas, alterar senhas necessárias e tentar localizar ou apagar os dados remotamente.
5. Se houver suspeita de dados de clientes expostos, a empresa deve avaliar o impacto e tomar as medidas internas necessárias.
6. Quando houver furto, deve ser feito boletim de ocorrência.
7. O equipamento deve ser marcado como indisponível no inventário.
8. Se houver perda de dados, a empresa deve restaurar as informações a partir do backup.
9. Depois do incidente, a empresa deve revisar a causa e melhorar os controles para evitar que aconteça novamente.



## 13. Relação com a tríade CID

A tríade CID é formada por **Confidencialidade, Integridade e Disponibilidade**. Todas as medidas do projeto devem ajudar a proteger pelo menos um desses três pontos.

| Pilar | Significado | Medidas do projeto relacionadas |
|---|---|---|
| Confidencialidade | Somente pessoas autorizadas podem ver ou acessar informações | Crachás, biometria, sala de servidores trancada, acompanhamento de visitantes, armários, criptografia de pendrives e bloqueio de notebooks |
| Integridade | Os dados devem permanecer corretos e não podem ser alterados, apagados ou danificados indevidamente | Controle de acesso, registro de entradas, backups, proteção dos servidores, antivírus em dispositivos autorizados e organização dos equipamentos |
| Disponibilidade | Sistemas, dados e equipamentos devem estar disponíveis quando a empresa precisar | Nobreak, gerador, climatização, prevenção contra incêndio, manutenção, backups e plano de recuperação |