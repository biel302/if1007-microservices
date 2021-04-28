![](https://img.shields.io/badge/Status-Under%20Development-green)

# if1007-microservices

- Link para o site --> https://strateegia-trello.herokuapp.com/
- Link para o Trello --> https://trello.com/b/WbD1gchY/planejamento
- Projeto da disciplina de [Microservices](https://github.com/IF1007/if1007) do Centro de informática da UFPE

## Sumário

- [Projeto](#Projeto)
- [Equipe](#Equipe)
- [Strateegia](#Strateegia)
- [Trello](#Trello)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Tomadas de Decisão](#tomadas-de-decisão)
- [Limitações](#Limitações)
- [Arquitetura](#Arquitetura)
- [Projetos Futuros](#Projetos-Futuros)
- [Iterações](#Iterações)

## Projeto

A ideia do projeto é criar um middleware de conexão entre os kits do Strateegia e os boards do trello, aplicando o conhecimento de microsserviços adquirido na disciplina.
Mapeamento: 
Kit do strateegia → Board do Trello
Questão do strateegia→ Cards do Trello na lista ‘To do’

## Equipe

|             Nome              |         Função          |
| :---------------------------: | :---------------------: |
|   Gabriel Estevam Longuinhos  | Engenheiro de software  |
| Joao Gabriel Silva de Andrade | Engenheiro de software  |
## Strateegia

Plataforma da TDS Company com foco nos processos existentes de um projeto. Com um design inovador, o framework abrange as três  principais áreas de um projeto: Pessoas, Negócios e Tecnologia. Para saber mais, acesse: https://strateegia.digital/ 

## Trello

Ferramenta de gerenciamento de projetos e atividades. Nele, é possível quadros personalizados no contexto do seu projeto

## Tecnologias Utilizadas

- **NodeJS**: Escolhemos o Node por ser simples de utilizar e de começar a desenvolver, além de ser um ambiente o qual temos um pouco de confortabilidade. Com isso, faz com que o desenvolvimento do projeto acabe se tornando mais rápido. 

- **mongoDB**: Utilizamos o mongoDB pelo mesmo motivo que o NodeJS, por causa da familiaridade com o banco. Além de ser fácil de aplicar, o mongoDB possui uma escalabilidade muito boa, documentação fácil de acessar ao que é preciso e banco compartilhável (diferente do SQLite) e fácil gerenciamento dos dados. 

- **ReactJS**: O React é open source e possui uma biblioteca de Javascript, além de sermos também familiarizados com JS. O React consegue ser rápido, escalável e simples naquilo que foi desenvolvido. ReactJS também é possível criar componentes reutilizáveis, recarregar apenas um elemento ou dado de página sem ter que fazer refresh, dá para utilizar o Single Page Application com várias rotas , entre outros fatores que torna uma aplicação rápida e simples.


## Tomadas de Decisão

- **Conversão**: Inicialmente, pensamos em transformar cada projeto do strateegia em um board no trello e os kits como listas. Porém, percebemos que os kits eram longos para ser apenas listas, isso fez que nós mudássemos de ideia e fazer o método de conversão da forma atual: Um projeto do Strateegia ser uma organização do trello, dentro dessa organização teria os kits do strateegia convertidos em boards, e dentro dos boards, há a  lista ‘To Do’ preenchida com as questões em forma de card.
 - **Arquitetura**: A motivação de decompor um  sistema em microsserviços é facilitar o desenvolvimento e implantação de tecnologias. Como nosso sistema tem poucas funcionalidades, não vimos necessidade de decompor o mesmo em vários microsserviços, até porque, há desvantagens nessa abordagem. Por isso, nosso sistema possui apenas um microsserviço.
- **Banco de dados**: Ao acessar pela primeira vez o aplicativo, o sistema pede a key e token do Trello para o usuário. Essa informação fica guardada no banco de dados, facilitando a usabilidade do usuário que não precisará ter essa informação a todo momento. Além disso, como a  organização do Trello tem um limite de 10 boards, decidimos guardar a informação dos kits convertidos em nosso banco de dados, assim, se caso chegar no limite de 10 boards convertidos, o usuário será informado via notificação e poderá excluir algum dos boards convertidos. Dessa forma, ele não terá o trabalho de entrar no Trello e excluir por lá. 

## Limitações

- O usuário precisa ter uma conta no strateegia
- O usuário precisa fornecer o token do trello
- Kits de pontos de conversação não são convertidas
- Respostas de questões não são convertidas
- Só é possível importar 10 kits para o Trello
- Não é possível atualizar um kit convertido

## Arquitetura
![alt text](https://i.ibb.co/zxGcjrT/Arq.jpg)

## Projetos Futuros

Mapeamentos alguns pontos de melhorias para trabalhos futuros:
- Criação de mais um tipo de conversão: É possível criar diferentes tipos de conversão, fornecendo poder para o usuário decidir qual tipo de conversão faz sentido dado o seu contexto.
- Converter as respostas das questões do Strateegia: Para uma conversão mais completa, é interessante trazer as respostas para cada questão do kit como comentário no trello.
- Rastreamento de kits já convertidos para atualização: Dessa forma, não haveria duplicação de um board e o usuário já teria conhecimento de que kits já foram convertidos, podendo atualizar os mesmos.
- Estudar uma forma de extrair o token do trello pelo email e senha.

## Iterações:

- Iteração 1
   - Período: 07 de abril de 2021 - 14 de abril de 2021
   - Planejado
     - Gabriel Longuinhos: Pesquisar sobre a API do Trello e analisar testes de frontend
     - João Gabriel: Pesquisar sobre a API do Strateegia
     - Ambos: Analisar a arquitetura do software e iniciar a fase de desenvolvimeto
   - Atividades feitas
     - Gabriel Longuinhos: Pesquisar sobre a API do Trello
     - João Gabriel: Pesquisar sobre a API do Strateegia
     - Ambos: Iniciar a fase de desenvolvimento
   - Atividades não feitas e motivo
     - Analisar a arquitetura do software: Estamos analisando melhor as API's para pensar depois pensar na arquitetura
     - Analisar testes de frontend: Precisa ficar de acordo com o retorno da API do Strateegia
  - Lições aprendidas
     - Requisições que precisamos fazer para a API do Trello
     - Requisições que precisamos fazer para a API do Strateegia
     - Regra de negócio
  - Próxima iteração:
     - Determinar a estrutura do banco de dados
     - Continuar o desenvolvimento
     - Analisar os testes

- Iteração 2
   - Período: 14 de abril de 2021 - 21 de abril de 2021
   - Planejado
     - Gabriel Longuinhos: Continuar o desenvolvimento com foco no trello
     - João Gabriel: Continuar o desenvolvimento com foco no strateegia
     - Ambos: Definir a arquitetura do software e do banco de dados
   - Atividades feitas
      - Todas as atividades foram feitas
   - Lições aprendidas
     - Aprendemos na prática a estrutura de um microsserviço
  - Próxima iteração:
     - Reunião com Vinicius Garcia para coletar possíveis melhorias
     - Implementar as melhorias definidas
     - Fazer deploy na aplicação
     - Realizar mais testes exploratórios


- Iteração 3
   - Período: 21 de abril de 2021 - 28 de abril de 2021
   - Planejado
     - Gabriel Longuinhos: Alterar forma de converter os kits e criar botão de deletar boards convertidos
     - João Gabriel: Implementar notificação de sucesso e erro ao converter um kit e fazer deploy na aplicação
     - Ambos: Testar a aplicação
   - Atividades feitas
      - Todas as atividades foram feitas
   - Lições aprendidas
     - Aprendemos na prática a estrutura de um microsserviço

