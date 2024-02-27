# Projeto 1: 2º Semestre de 2021 

<img src="https://github.com/fluffyfatec/SPanel/blob/main/Sprint_2/assets/logospanel3.png" width="60%" height="55%">

### Reposiório do Projeto

[SPANEL - Fluffy Fatec](https://github.com/fluffyfatec/SPanel)

### Parceiro Acadêmico

Interno

### Visão do Projeto

Com intuito de melhorar e facilitar o acesso aos números da COVID-19 disponibilizados pelo Estado de São Paulo, a Fluffy está, a pedido de um cliente, desenvolvendo o SPanel, um painel virtual que reúne os principais dados da pandemia em uma interface única e de fácil utilização.

Como solução, a equipe desenvolveu um software web para a empresa, que possibilita a visualização dos dados de forma prática e intuitiva através de um dashboard. Nele está contido informações como a quantidade de pessoas imunizadas, novos casos, casos acumulados, número de óbitos, entre outras informações. Também é possível fazer o filtro por período, cidades, regiões, e visualizar esses mesmo através de gráficos que facilitam a consulta.

O sistema possui uma automação da extração dos dados diretamente da base de dados do Governo de São Paulo, onde eram disponibilizados os dados referente a pandemia. Como também possui um bot desenvolvido no site Telegram.org que é responsável por disponibilizar informações do sistema de forma mais prática e dinâmica para o usuário. 

### Tecnologias Adotadas na Solução

#### Python

A linguagem Python foi utilizada para o desenvolvimento do projeto ao todo. Com ela, foi feita a automação da extração dos dados disponibilizados no [site do Governo de São Paulo](https://www.saopaulo.sp.gov.br/planosp/simi/dados-abertos/), o tratamento desses dados para a utilização no sistema (que foram gerenciados em arquivos CSVs), e a interface do sistema web para a visualização dos dados pelo usuário.

Para saber mais, acesse: [Python](https://www.python.org)

#### Telegram Bots

A ferramenta Telegram Bots foi utilizada para o desenvolvimento de um bot na própria plataforma do Telegram que ficou responsável por fornecer uma forma prática de visualição dos dados já tratados pelo sistema.

Para saber mais, acesse: [Telegram Bots](https://core.telegram.org/bots)

### Contribuições Pessoais

Fui responsável pelo desenvolvimento do aplicativo web programado em Python usando o framework Dash, buscando oferecer uma interface interativa para análise de dados relacionados à pandemia de COVID-19 no Estado de São Paulo.

pré-processamento de dados a partir de arquivos CSV sobre COVID-19 e população usando Pandas.
Criação de Gráficos e Layout do Aplicativo:

criar diversos tipos de gráficos, como barras, pizza, linhas e dispersão, representando estatísticas relacionadas a casos de COVID-19, óbitos, vacinação, etc.
Desenvolve o layout da interface usando Dash Bootstrap Components para criar um design responsivo com elementos visuais como cabeçalho, filtros de data, seleção de municípios, entre outros.
Funcionalidades Interativas:

Oferece recursos de filtragem, classificação e seleção de colunas em uma tabela interativa com dados detalhados sobre a COVID-19 em diferentes localidades.


Fornece gráficos dinâmicos e estatísticas atualizadas com base nas seleções feitas pelo usuário.

Define o estilo visual da aplicação, incluindo cores, layouts e posicionamento dos elementos na página.
Utiliza marcações de texto (Markdown) para destacar títulos e subtítulos em diferentes seções da interface.

Em resumo, o aplicativo Dash oferece uma plataforma interativa para visualização e análise dos dados relacionados à pandemia de COVID-19 em São Paulo, permitindo aos usuários explorar estatísticas, gráficos e informações detalhadas, além de interagir com a interface para obter uma visão abrangente da situação epidemiológica.


```python
# Pré Processamentos de Dados
df_tratado = pd.read_csv("docs/df_tratado.csv")
df_vacinastratado = pd.read_csv("docs/df_vacinastratado.csv")
df_estadotratado = pd.read_csv("docs/df_estadotratado.csv")
df_vacinas = pd.read_csv("docs/vacinas.csv", sep=';')
df_vacinas = df_vacinas.rename(
    columns={'Município': 'nome_munic'})
list_municipios = sorted(df_tratado['nome_munic'].unique()) #formatação de municipios
date_column = df_tratado["datahora"]
max = date_column.max()
row = df_tratado.loc[df_tratado["datahora"] == max]
df_vacinastratadonotpop = df_vacinastratado.drop(columns=['pop'])
df_totais = pd.merge(row,df_vacinastratadonotpop, how='inner', on='nome_munic')
df_totais = df_totais.drop(
    columns=['Unnamed: 0_x', 'Unnamed: 0_y'])
df_tratado_rename = df_totais.rename(
                columns={'nome_munic': 'Localização', 'casos': 'Casos Acumulados', 'datahora': 'Data da Atualização',
                         'obitos': "Óbitos Acumulados","pop": "População","doseunica":"Dose Unica","primeiradose":"Primeira Dose",
                         "segundadose":"Segunda Dose","terceiradose":"Terceira Dose"})
df_tratado_rename = df_tratado_rename.reindex(
                columns=['Localização', 'Casos Acumulados', 'Óbitos Acumulados','Dose Unica','Primeira Dose','Segunda Dose','Terceira Dose','População', 'Data da Atualização'])

casosacumulados = df_tratado_rename["Casos Acumulados"].sum()
obitossacumulados = df_tratado_rename["Óbitos Acumulados"].sum()
doseunica = df_tratado_rename["Dose Unica"].sum()
primeiradose = df_tratado_rename["Primeira Dose"].sum()
segundadose = df_tratado_rename["Segunda Dose"].sum()
terceiradose = df_tratado_rename["Terceira Dose"].sum()
populacao = df_tratado_rename["População"].sum()
data = df_tratado_rename['Data da Atualização'].max()
df_tratado_rename = df_tratado_rename.append(dict(zip(df_tratado_rename.columns, ['ESTADO DE SÃO PAULO', casosacumulados,obitossacumulados,doseunica,primeiradose,segundadose,terceiradose,populacao,data])),ignore_index=True)
list_tabela=['ESTADO DE SÃO PAULO','SÃO PAULO', 'GUARULHOS', 'CAMPINAS', 'SÃO BERNARDO DO CAMPO', 'SÃO JOSÉ DOS CAMPOS', 'SANTO ANDRÉ']
list_municipios2 = sorted(df_tratado_rename['Localização'].unique())
```


### Aprendizados Efetivos (Soft e Hard Skills)


