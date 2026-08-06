# Estrutura de um Projeto NoSQL para um Supermercado

## 1. Banco Chave-Valor

O banco Chave-Valor guarda uma informação usando uma chave e um valor. Ele é bom para informações simples e que precisam ser acessadas rapidamente.

### Exemplos de uso:

- Guardar o login do usuário.
- Guardar o token de acesso.
- Salvar produtos que são acessados com mais frequência.
- Guardar alertas de estoque baixo.
- Salvar algumas configurações do sistema.

### Exemplo:

```text
produto:001 → Arroz 5kg
usuario:123 → Administrador
alerta:001 → Produto com estoque baixo
```

Esse tipo de banco pode ser usado porque ele é simples e rápido para encontrar as informações.

## 2. Banco de Dados em Colunas

O banco em Colunas organiza os dados em colunas e pode ser usado quando existem muitas informações para analisar.

### Exemplos de uso:

- Histórico de vendas.
- Movimentações do estoque.
- Relatórios por data.
- Produtos mais vendidos.
- Valores gastos por cada centro de custo.

### Exemplos de informações:

```text
Data
Produto
Quantidade vendida
Valor da venda
Loja
Centro de custo
```

Esse modelo pode ajudar na criação de relatórios, pois facilita a comparação das vendas e dos gastos do supermercado.

## 3. Banco de Documentos

O banco de Documentos armazena as informações em documentos. Esse tipo é parecido com arquivos em formato JSON e pode guardar várias informações juntas.

Ele pode ser usado para:

- Cadastro de produtos.
- Cadastro de fornecedores.
- Cadastro de funcionários.
- Pedidos de compra.
- Notas fiscais.
- Informações dos clientes.
- Dados do estoque.

### Exemplo de um produto:

```json
{
  "id": "P001",
  "nome": "Leite Integral",
  "categoria": "Laticínios",
  "validade": "2026-09-10",
  "quantidade": 120,
  "preco": 5.49,
  "fornecedor": "Distribuidora ABC"
}
```

Esse banco é interessante porque permite colocar várias informações sobre o produto dentro do mesmo documento. Também é possível adicionar novas informações depois, sem precisar alterar toda a estrutura.

## 4. Banco de Grafos

O banco de Grafos serve para mostrar as relações entre as informações. Ele trabalha com conexões entre pessoas, produtos, lojas e fornecedores.

### Exemplos de relações:

- Um fornecedor fornece um produto.
- Um produto pertence a uma categoria.
- Um cliente compra determinado produto.
- Um funcionário trabalha em uma loja.
- Uma loja possui um centro de custo.
- Um produto pode combinar com outro produto.

### Exemplo:

```text
Fornecedor ABC → fornece → Arroz 5kg
Arroz 5kg → pertence à categoria → Alimentos
Cliente 001 → comprou → Arroz 5kg
Loja Centro → possui → Centro de Custo 01
```

Esse modelo pode ajudar o supermercado a entender melhor as relações entre os dados e também a identificar os produtos mais comprados ou os fornecedores mais utilizados.

## Uso dos modelos no supermercado

Cada modelo pode ser usado para uma parte diferente do sistema:

- **Chave-Valor:** para informações simples e rápidas, como sessões, alertas e configurações.
- **Colunas:** para grandes quantidades de dados, relatórios e análises.
- **Documentos:** para cadastros de produtos, fornecedores, clientes e pedidos.
- **Grafos:** para mostrar relações entre produtos, clientes, fornecedores e centros de custo.
