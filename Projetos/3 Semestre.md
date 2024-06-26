# Projeto 3: 2º Semestre de 2022 

<img src="https://github.com/fluffyfatec/Iacit/blob/Sprint-2/GIT/cabecario (3).jpg" width="60%" height="55%">


## Reposiório do Projeto

[IACIT - Fluffy Fatec](https://github.com/fluffyfatec/Iacit)


## Parceiro Acadêmico

IACIT Soluções Tecnológicas


## Visão do Projeto

O desafio foi estipulado como desenvolver um sistema que permita realizar a importação dos dados meteorológicos, bem como armazená-los em uma base de dados, para posteriormente gerar os relatórios desejados por nossos clientes.

Como solução, a equipe desenvolveu um software web para a empresa, que possibilita a automatização desde o download, o processamento dos dados e a persistência dos dados no banco de dados de forma simplificada. Também é possível realizar a filtragem desses dados por temperatura, umidade, estações, vento, pressão atmosférica, radiação global e precipitação, além da diversa visualizações desses dados. E por último, foram desenvolvidos diferentes níveis de usuários juntamente com o painel administrativo possibilitando a exportação dos relatórios a partir dos dados.

Representação da solução do projeto:

<img src="./Midia/iacit_aplicacao.gif" width="60%" height="55%">


## Tecnologias Adotadas na Solução

### Java - Spring Boot

A linguagem Java foi utilizada em praticamente todo o back-end da aplicação. Junto com o framework Spring Boot, foram desenvolvidas, com a linguagem, diversas funcionalidades da aplicação, como a configuração da lógica para a utilização dos dados armazenados no banco de dados, o desenvolvimento de toda a API do sistema para que os dados possam ser consumidos pelo front-end, as funções de CRUD (Create, Read, Update, Delete) do usuário, e a segurança da aplicação via token.  

Para saber mais, acesse: [Java](https://www.java.com)

### Python

A linguagem Python foi utilizada para a automatização do tratamento de dados da aplicação. Com ela, foi feito desde o download dos arquivos CSVs, originados do [Portal INMET](https://portal.inmet.gov.br), efetuando a descompactação dos arquivos, tratamento de todos os dados meteorológicos, e a inserção desses dados no banco de dados. Tudo de forma automatizada pela rotina de tarefas desenvolvidas na linguagem.

Para saber mais, acesse: [Python](https://www.python.org)

### JavaScript

A linguagem JavaScript foi utilizada em grande parte do front-end da aplicação. Com ela foi efetuada a utilização dos dados enviados do back-end para o front-end, desenvolvendo gráficos, tabelas e outras formas de visualização de dados para o usuário. Além de ser utilizada para deixar as telas da aplicação de forma dinâmica, fazendo com que elas sejam responsivas com as ações tomadas pelo usuário e os dados atuais do banco de dados.

Para saber mais, acesse: [JavaScript](https://www.javascript.com)

### PostgreSQL

O SGDB (Sistema Gerenciador de Banco de Dados) PostgreSQL foi utilizado para o armazenamento dos dados automatizados pelo Python. Com ele, foram feitas as criações de tabelas, views e triggers do banco de dados da aplicação, e era feito o gerenciamento dos dados.

Para saber mais, acesse: [PostgreSQL](https://www.postgresql.org)


## Contribuições Pessoais

Fui responsável pelo desenvolvimento do front-end do projeto de sistema para importação de dados meteorológicos. Minha principal função consistiu em criar uma interface intuitiva e funcional para os usuários, utilizando os dados fornecidos pelo back-end por meio de APIs.

Trabalhando em colaboração com a equipe de front-end, participei ativamente do estudo e desenvolvimento das telas da aplicação. Durante esse processo, concentrei-me na geração de gráficos dinâmicos que exibiam as informações meteorológicas de forma clara e compreensível. Além disso, desenvolvi funcionalidades para exibição de tabelas contendo dados detalhados e implementei filtros dinâmicos para que os usuários pudessem personalizar sua visualização de acordo com suas necessidades.

Para realizar essas tarefas, utilizei linguagens e tecnologias como HTML, CSS e JavaScript. A marcação HTML e a estilização em CSS foram essenciais para a criação de layouts atraentes e responsivos. A parte lógica da aplicação foi desenvolvida principalmente em JavaScript, aproveitando técnicas como AJAX para melhorar a interatividade e a eficiência da aplicação.

Ao focar na geração de gráficos, exibição de tabelas e implementação de filtros dinâmicos, ajudei a criar uma aplicação que permite aos usuários explorar e entender os dados meteorológicos de forma intuitiva e personalizada.


## Aprendizados Efetivos

<h3 align="center"> Hard Skills </h3>

<table align="center">
    <tr>
      <th width="300px">Tecnologia/Metodologia</th>
      <th width="300px">Classificação</th>
    </tr>
    <tr>
      <td>Java</td>
      <td>Sei fazer com Ajuda</td>
    </tr>
    <tr>
      <td>Spring Boot</td>
      <td>Sei fazer com Ajuda</td>
    </tr>
    <tr>
      <td>Python</td>
      <td>Sei fazer com Autonomia</td>
    </tr>
    <tr>
      <td>HTML</td>
      <td>Sei fazer com Ajuda</td>
    </tr>
    <tr>
      <td>CSS</td>
      <td>Sei fazer com Ajuda</td>
    </tr>
    <tr>
      <td>JavaScript</td>
      <td>Entendi</td>
    </tr>
    <tr>
      <td>PostgreSQL</td>
      <td>Sei fazer com Ajuda</td>
    </tr>
    <tr>
      <td>GIT</td>
      <td>Sei fazer com Autonomia</td>
    </tr>
</table>

<h3 align="center"> Soft Skills </h3>

<table align="center">
    <tr>
      <th width="300px">Habilidade</th>
      <th width="300px">Descrição</th>
    </tr>
    <tr>
      <td>Organização</td>
      <td>Precisei me organizar e planejar para poder ser eficaz no desenvolvimento do projeto</td>
    </tr>
    <tr>
      <td>Comunicação</td>
      <td>Precisei me comunicar com a equipe sobre situações e status de tarefas</td>
    </tr>
    <tr>
      <td>Resolução de Problemas</td>
      <td>Precisei entender e buscar formas de resolver problemas encontrados durante o projeto</td>
    </tr>
    <tr>
      <td>Trabalho em Equipe</td>
      <td>Precisei entender e adaptar a forma de trabalho para colaborar com a equipe no desenvolimento do projeto</td>
    </tr>
    <tr>
      <td>Proatividade</td>
      <td>Precisei tomar atitudes para conseguir concluir o desenvolvimento do projeto</td>
    </tr>
</table>

---

## Outros Projetos:

[1º Semestre - SPANEL - Sistema de Automação e Visualização de Dados da COVID-19 ](https://github.com/tiagocamillo/Portfolio-Banco-de-Dados/blob/develop/Projetos/1%20Semestre.md)

[2º Semestre - Dom Rock - Sistema de Gerenciamento de Clientes](https://github.com/tiagocamillo/Portfolio-Banco-de-Dados/blob/develop/Projetos/2%20Semestre.md)

[4º Semestre - Embraer - Controle de Configuração de Aeronaves](https://github.com/tiagocamillo/Portfolio-Banco-de-Dados/blob/develop/Projetos/4%20Semestre.md)

[5º Semestre - Oracle - Análise e Gestão de Restaurante](https://github.com/tiagocamillo/Portfolio-Banco-de-Dados/blob/develop/Projetos/5%20Semestre.md)

[6º Semestre - Imagem - Sistema de Análise de Sentimento por Geolocalização](https://github.com/tiagocamillo/Portfolio-Banco-de-Dados/blob/develop/Projetos/6%20Semestre.md)
