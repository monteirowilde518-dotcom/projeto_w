# Respostas da Atividade — Banco de Dados NoSQL

# Questão 1 — Modelos NoSQL

| Item | Situação | Modelo indicado |
|---|---|---|
| a) | Cadastro e acesso dos usuários | Chave-Valor |
| b) | Grande quantidade de dados | Colunas ou Distribuído |
| c) | Perfil dos estudantes | Documentos |
| d) | Relação entre estudantes e cursos | Grafos |

# Questão 2 — Justificativas

 a) Chave-Valor

O modelo chave-valor é indicado para cadastrar e encontrar usuários rapidamente. Cada usuário possui uma chave própria, que pode ser o seu código. A partir dessa chave, podemos encontrar o nome, o e-mail e outras informações.

 b) Colunas ou Distribuído

Esse modelo é indicado quando o sistema possui muitos dados. As informações podem ser divididas entre vários servidores, ajudando o banco de dados a trabalhar melhor e com mais rapidez.

 c) Documentos

O modelo de documentos é bom para guardar o perfil dos estudantes. Ele permite colocar várias informações em um único documento, como nome, idade, curso, matrícula e semestre.

Outra vantagem é que os documentos podem ter informações diferentes. Assim, não é obrigatório que todos os estudantes tenham exatamente os mesmos dados.

 d) Grafos

O modelo de grafos é usado quando precisamos mostrar relações entre pessoas, cursos e disciplinas. Ele pode mostrar, por exemplo, quais estudantes estão matriculados em uma disciplina e qual professor ministra essa disciplina.

# Questão 3 — Modelo Chave-Valor

Os dados de Elfaba Thropp podem ser representados assim:

```text
"Código": 1025
"Nome": "Elfaba Thropp"
"E-mail": "elfaba@exemplo.com"
```

Também podemos usar o código como a chave principal:

```text
1025: {
  "Nome": "Elfaba Thropp",
  "E-mail": "elfaba@exemplo.com"
}
```

Nesse caso, o número `1025` identifica a estudante e os outros dados ficam ligados a esse código.

# Questão 4 — Modelo de Documentos

O perfil de Elfaba Thropp pode ser representado em formato JSON:

```json
{
  "nome": "Elfaba Thropp",
  "idade": 22,
  "curso": "Banco de Dados",
  "matricula": "2026001",
  "semestre": "3º semestre",
  "turno": "Noturno"
}
```

O modelo de documentos é flexível porque podemos acrescentar outras informações depois, como telefone, endereço ou notas.

# Questão 5 — Modelo de Grafos

Nesse exemplo, temos:

- Fiyero, que é um estudante.
- Morrible, que é uma professora.
- Banco de Dados, que é uma disciplina.

A representação pode ser feita assim:

```text
[Fiyero: Estudante]
        |
        | está matriculado em
        ▼
[Banco de Dados: Disciplina]
        ▲
        | é ministrada por
        |
[Morrible: Professora]
```

Também podemos escrever os relacionamentos da seguinte forma:

```text
Fiyero está matriculado em Banco de Dados.

Morrible ministra Banco de Dados.
```

Nesse grafo, Fiyero, Morrible e Banco de Dados são os nós. As frases que ligam esses elementos são os relacionamentos.

# Questão 6 — Escalabilidade

a) O que é escalabilidade?

Escalabilidade é a capacidade de um sistema crescer sem ficar muito lento ou parar de funcionar. Por exemplo, se o número de estudantes e usuários aumentar, o sistema deverá continuar funcionando corretamente.

 b) Diferença entre escalabilidade vertical e horizontal

A escalabilidade vertical acontece quando aumentamos a capacidade de um único servidor. Podemos colocar mais memória, um processador melhor ou mais espaço de armazenamento.

A escalabilidade horizontal acontece quando adicionamos mais servidores ao sistema. Dessa forma, os dados e as tarefas são divididos entre várias máquinas.

 c) Por que a escalabilidade é importante nos bancos NoSQL?

A escalabilidade é importante porque os bancos NoSQL são usados para armazenar muitos dados e atender a vários usuários ao mesmo tempo.

Com a possibilidade de usar vários servidores, o sistema consegue crescer sem depender somente de uma única máquina.

# Questão 7 — Replicação e Particionamento

 a) O que é replicação?

Replicação é quando fazemos cópias dos mesmos dados em mais de um servidor. Isso é importante porque, se um servidor apresentar algum problema, os dados ainda estarão disponíveis em outro servidor.

A replicação também pode ajudar a melhorar o acesso às informações.

 b) O que é particionamento?

Particionamento é quando dividimos os dados em partes menores e colocamos cada parte em um servidor diferente.

Assim, um único servidor não precisa guardar tudo sozinho. Isso facilita o trabalho do sistema e permite armazenar uma quantidade maior de dados.

# Questão 8 — Comparação dos modelos NoSQL

Não existe apenas um modelo NoSQL ideal para todos os casos. Cada modelo é melhor para uma situação diferente.

O modelo chave-valor é simples e rápido. Ele é usado quando precisamos encontrar uma informação por meio de uma chave, como o código de um usuário.

O modelo orientado a colunas é bom para trabalhar com uma grande quantidade de dados e vários servidores.

O modelo de documentos é indicado para guardar informações que podem mudar ou ter formatos diferentes, como o perfil dos estudantes.

O modelo de grafos é melhor quando existem muitos relacionamentos entre os dados, como estudantes, professores, cursos e disciplinas.

Por isso, antes de escolher um modelo NoSQL, é preciso analisar o tipo de informação, a quantidade de dados e a maneira como eles serão consultados. Cada modelo possui uma função diferente e pode ser escolhido de acordo com a necessidade do sistema.