<h1> TCC </h1>
<div style="text-align: justify;"> Este repositório foi criado para fazer o manuseio dos dados da CAT(Comunicação de Acidentes de Trabalho) e elaborar o meu TCC que teve como tema: Análise dos acidentes de trabalho na área da saúde no período de julho/2018 a julho/2022 utilizando técnicas de mineração de dados.</div>

<br />
<h1> Sumário </h1>

- [Principais tecnologias utilizadas](#principais-tecnologias-utilizadas)
- [Funcionalidades principais](#funcionalidades-principais)
- [Explicação das funcionalidades](#explicação-das-funcionalidades)
  - [Seleção do conjunto de dados](#seleção-do-conjunto-de-dados)
  - [Análise exploratória dos dados](#análise-exploratória-dos-dados)
  - [Mineração de dados](#mineração-de-dados)
    - [Preparação dos dados para mineração](#preparação-dos-dados-para-mineração)
    - [Geração de nova base de dados](#geração-de-nova-base-de-dados)
    - [Técnicas de mineração](#técnicas-de-mineração)
- [Dica para usar o código](#dica-para-usar-o-código)

<br/>

# Principais tecnologias utilizadas
- Python
- Jupyter

<br/>

# Funcionalidades principais
 - Seleção do conjuto de dados 

- Análise exploratória dos dados 

- Mineração de dados 
  - Preparação dos dados para mineração 
  - Geração de nova base de dados
  - Técnicas de mineração

<br/>

# Explicação das funcionalidades 
## Seleção do conjunto de dados
<div style="text-align: justify;"> A partir dos dados da CAT(Comunicação de Acidentes de Trabalho) os quais forma baixados no <a href="https://dados.gov.br/dados/conjuntos-dados/inss-comunicacao-de-acidente-de-trabalho-cat1">site do governo</a>, formatou-se os dados para estes pudessem ser agrupados em um único arquivo. </div>

<br/>

## Análise exploratória dos dados 
<div style="text-align: justify;"> Com todos os dados em um único arquivo, filtrou-se os dados para pegar apenas os dados dos profissionais da saúde, que era o foco deste estudo, em seguida elaborou-se gráficos com intuito de entender o perfil dos profissionais da saúde e dos acidentes que estes profissionais sofreram. </div>

<br/>

## Mineração de dados
### Preparação dos dados para mineração 
<div style="text-align: justify;">Para que os dados pudessem ser utilizados nas técnicas de mineração de dados, eliminou-se alguns atributos e alterou seus valores para valores numéricos. </div>

<br/>

### Geração de nova base de dados
<div style="text-align: justify;">Para equilibrar a base dados que seria aplicada nas técnicas de mineração de dados, sorteou-se 101 linhas que possuíam o atributo óbito igual a 0 (não houve óbito) e juntou essas linhas com outras 101 linhas com atributo óbito igual a 1 (houve óbito) gerando assim uma nova base de dados.</div>

<br/>

### Técnicas de mineração
<div style="text-align: justify;">Aplicou-se as técnicas da pasta 'src/dataMining' tiradas do do site <a href="https://scikit-learn.org/stable/">scikit-learn</a> na nova base de dados. Em seguida, selecionou as técnicas que apresentaram melhor resultado, sendo uma técnica _não ensemble_ e outra  _ensemble_ para aplicar o algoritmo SHAP com intuito de entender o impacto dos atributos no óbito do trabalhador.</div>

<br />

# Dica para usar o código 
- Baixe este repositório 
  
Caso tenha o [git](https://git-scm.com/downloads) instalado, digite o comando abaixo no seu terminal. 
Se não, faça o download do repositório e descompacte o arquivo.

`````
git clone https://github.com/NataliaRamalho/TCC.git
`````

- Crie uma pasta na raiz do projeto com o nome database e insira os arquivos com os dados da CAT dentro
  
- Rode o arquivo 'CreateFile.ipynb', para criar um novo arquivo contendo todos os dados da CAT agrupados.  
  
<br/>
⏰ Projeto desenvolvido em abri/2023