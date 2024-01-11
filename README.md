# Explicação descritiva dos dados da [planilha de precificação](https://docs.google.com/spreadsheets/d/1_GYgavkEbLLr7kyt4ZlJYMXsbDk1Jt-96cjR4khYs9M/edit#gid=852988936) 💕

## Requisitos Funcionais

O que são?


> Requisitos funcionais são todas as necessidades, características ou funcionalidades esperadas em um processo que podem ser atendidos pelo software.

Ou seja é **o que o sistema deve fazer**, por exemplo: "manter o usuário" é um requisito funcional (onde manter,
é sinônimo de [_CRUD_](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)).

### Tipos Funcionais
- **Arquivos de Interface Externa**: Basicamente qualquer consumo de [API](https://en.wikipedia.org/wiki/API) que não seja nosso: APIs de pagamento, de dados ([filmes](https://www.omdbapi.com/), [digimons](https://digimon-api.com/), paçocas, etc). PS: tercerização de um serviço contratado por nós **não** se enquadra neste requisito :)
 
- **Entrada Externa**:
"Funcionalidades de inclusão, alteração e exclusões de dados"
leia-se _CRUD_. A orientção é considerar cada função separadamente, ou seja, imagine um requisito de _CRUD_ de paçoquinha: cada operação de Criar, Ler, Atualizar e ~~Comer~~ Deletar deve ser contada separadamente.
  
- **Saída Externa**: "Funcionalidades que apresentam informações para o usuário com utilização de cálculos ou algoritmos. São as consultas ou relatórios com totalização de dados, relatórios estatísticos, gráficos, entre outros.". Imagine que um dos requisitos funcionais é entregar um relatório de todas as paçocas consumidas por DPJ nas reuniões, com os dados abaixo junto de um dashboard:
  
  
    1. Membro
    2. Média de Paçocas
    3. Valor Total Consumido
    4. [PCC](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient) com felicidade</tr>
   

  Concorda que para termos média, valor total e PCC devemos realizar cálculos? Bem, ai está um requisito de saída externa. Outro exemplo, uma plataforma de estudos precisa entregar cards de disciplina com distribuição baseada por determinadas condições, como: familiaridade com o tópico, tempo de estudo, etc. Não possuímos um "conta" clara, mas com o regulamento em baixo do braço ("apresentam informações para o usuário com utilização de cálculos ou **algoritmos**") podemos considerá-lo como requisito de saída externa.
  
- **Consulta Externa**: "Funcionalidades que apresentam informações para o usuário sem a utilização de cálculos ou algoritmos. São os processos elementares do tipo “lê - imprime - apresenta dados”, incluindo consultas, relatórios entre outros.". Voltando ao exemplo das paçocas ~~sim, eu gosto bastante :)~~. De tanto que DPJ as consumiu foi desenvolvido uma série de casos de diabetes, e pior, o vício foi passado para os membros da família; e o Diretor de DVP solicita um relatório com todos os casos (de membro e familiares) com dados de cada um e a conta do hospital. Perceba que para processarmos esse relatório não há a necessidade de realizar contas ou lógica complexa, somente a boa e velha consulta SQL simples (com muitos [_JOINs_](https://en.wikipedia.org/wiki/Join_(SQL))). Temos ai um requisito de consulta externa :)

- **Arquivo Lógico Interno**: "Banco de Dados Lógico da Aplicação (tabelas e arquivos mantidos pela aplicação).". Talvez o mais simples deles. Se temos um back-end que guarda informções da aplicação por um banco de dados, temos um arquivo lógico interno. Lembre-se de conta-lo pra cada banco que for utilizado pela aplicação! (Geralmente é apenas um mesmo).
> PS: O texto fala de arquivos da aplicação, mas se tu ver o gerente sugerindo guardar **qualquer** dado em um arquivo, pode ir falar com o diretor de DPJ, é pcd na hora :)

### Complexidade
O nome é alto explicativo, quase todos os requisitos vão entrar em simples. Mas o que seriam os médios e complexos? Sempre que ficar com dúvida, se pergunte:

1. Já realizamos e documentamos(!) isto antes?
2. Os membros terão que estudar soluções muito diferentes do escopo que estão acostumados?

Se você respondeu:

- [x] 1.
- [ ] 2.
 
Então provavelmente é de dificuldade média. Agora, se as respostas foram:

- [ ] 1.
- [X] 2.

Temos uma dificuldade complexa ai.

> PS: Essas perguntas são apenas para te direcionar, **não siga regras automáticamente sem pensar sobre elas**, conversar com um membro de DPJ, com o cliente, pesquisar sobre o tópico são a chave para realizar uma boa precificação. Quanto mais você fizer e quanto mais analisar o que acertou e errou melhor tu vai ficar nisso :) 
