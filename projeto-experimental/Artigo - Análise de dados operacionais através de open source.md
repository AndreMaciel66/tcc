Perguntas a serem respondidas no artigo.
- Qual o objeto de estudo?
- O que se pode saber sobre ele?
- De onde surgiram estas questões?
- Qual a relevância delas para entender o objeto?

keywords:
open source, analise de dados, visualização de dados, data visualization, data analytics, python, pandas, rest api, react js, react native, javascript for datavisualization, d3, operational report, relatorios operacionais

sources:

- science direct - https://www.sciencedirect.com
- scielo - https://scielo.org


# TCC - Desenvolvendo análise de dados operacionais através de open source

## Repensando a arquitetura de ambiente local para desenvolvimento de Análise de Dados Operacionais

Objetivo deste artigo é propor alternativas de linguagens, frameworks e de configuração ambiente para desenvolvimento de análise de dados operacionais com objetivo de automatizar a forma descrever as hipóteses e comentar as análises propostas seguidas pelo código, utilizando linguagens e frameworks Open Source.

---

## Sessões

### Abstract

Contendo o resumo em inglês do seu tema, bem como o seu tipo de pesquisa e uma prévia dos resultados.

Objective of this article is to study alternatives of languages, frameworks and environment configuration for the development of operational data analysis in order to automate a way defined as hypotheses and comment as proposed analyzes followed by the code, using Open Source languages and frameworks.


### Introdução

Aqui você deve contextualizar o leitor sobre o seu tema, embasando-o teoricamente sobre o conteúdo trabalhado, bem como sobre o método utilizado na pesquisa.


Estudo e trabalho encima deste tema/assunto desde ~2010, e sempre estive a procura de encontrar um método que fosse de fácil abstração e implementação de análise de dados, com isso, neste período eu testei e estudei diversas soluções, algumas open source como Python, R e Javascript, e outras tecnologias pertencentes a grandes empresas como, o Power BI (Microsoft), Tableau, Qliksense. Diante deste cenário, em paralelo aos conteúdos aprendidos no curso de Análise e desenvolvimento de sistemas eu estou finalmente chegando a um template, baseado interamente em tecnologias Open Source.

Neste artigo vamos construir um ambiente utilizando o Python no backend e vamos construir uma aplicação em react para o front end. 

Eu acredito que um desenvolvedor full-stack é capaz de criar uma aplicação completa para apresentar suas análises de dados e entregar uma aplicação com uma boa experiência de usuário, sendo capaz de criar uma engenharia e arquitetura de uma aplicação que poderá ser renderizada em qualquer dispositivo.

### Materias e Métodos

O método utilizado neste projeto experimental é baseado no livro Megaflask Tutorial de Miguel Grinberg, que propõe a criação de um REST API utilizando a linguagem Python, implementando o framework FLASK. O ambiente criado para este projeto tem como objetivo a criação de um produto de dados.

Produto de dados consiste em uma aplicação de software para consumo de informações de uma fonte de dados. O software faz operações matemáticas e renderiza componentes visuais para análises estatísticas de dados, como gráficos, cartões, tabelas e KPI's. Proporcionando assim uma experiência visual de dados agradável e intuitiva ao consumidor, além de promover insights para tomada de decisões.

Para análise dos dados, a biblioteca utilizada para renderizar os gráficos é a [Vega/Vega-Lite](https://vega.github.io/vega-lite/) que é implementada através da biblioteca de Python [Altair-Viz](https://altair-viz.github.io). O vega-lite é uma alternativa para renderizar componentes [D3](https://d3js.org/) sem a necessidade de curva de aprendizado que uma biblioteca java necessitaria.

Com esta ferramenta é possível que toda a lógica de consumo, preparação, modelagem e visualização dos dados seja feita no backend.

Para análise de dados, vamos utilizar uma biblioteca chamada Vega para renderizar nossos gráficos, a implementeção do [Vega/Vega-Lite](https://vega.github.io/vega-lite/) será realizada pelo [Altair-Viz](https://altair-viz.github.io), a escolha dessa biblioteca eu trago como uma alternativa para renderizar gráficos no topo do d3, sem precisar sofrer a curva de aprendizado que esta biblioteca em javascript demanda, tópico para outro artigo, a ideia é trazer toda a lógica de consumo, preparação e construção da visualização dos dados seja feita no backend.

Além disso vamos desenvolver o processo de análise exploratória dos dados utilizando Jupyter Lab/Notebook, para testar e validar nossas hipóteses, até a geração de uma história que queremos contar com o dado até chegar em um insight, note que, precisamos ter em mente que nada disso tem valor se nosso estudo e argumentação não chegar a uma conclusão de um insight, para tomada de decisão, o famoso __call to action__, precisamos sempre ter isso em mente para agregar valor à operação analisada.


### Resultados e discussão

Deve ser apresentado um resumo de quantas publicações foram encontradas, bem como uma análise de forma geral das publicações. Além disso, deve ser feita uma análise dos artigos mais relevantes sobre o tema, visando enriquecer a discussão. Ao final, o estudante deve concluir sobre o conteúdo disponível sobre o seu tema de pesquisa.


#### Configuração de seu ambiente Python

Crie o diretório do seu backend com o nome de codash-api.

```sh
mkdir codash-api
cd codash-api
```

Verificar se o python está instalado em sua máquina:

```python
python3 -v
```

No diretorio root de seu projeto instalar o virtual env:

```python
python3 -m venv venv
```

Ativando seu novo interpretador do Python.

```python
source venv/bin/activate
```

##### Instalando as dependencias

Iremos utilizar as seguintes bibliotecas para desenvolvimento de nossa aplicação:

- flask
- pandas
- flask-restx
- requests
- altair-viz vega-datasets
- jupyterlab

#### Configurando sua aplicação front end

Neste passo vamos criar um novo folder para a API da aplicação, de preferência separado do backend. Necessário instalar o node.

Para verificar qual versão do node temos instalado é só digitar o comando abaixo:

```sh
node --version
```

Estou utilizando a versão 14.9.0.

Agora precisamos criar uma nova aplicação em react com o nome de codash.

```javascript
npx create-react-app codash
```


### Referências Bibliográficas

- The megaflask tutorial - Miguel Grinberg
  - [Book](https://www.amazon.com.br/New-Improved-Flask-Mega-Tutorial-English-ebook/dp/B079KPG4HT)
  - [Articles](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)
- [Python Data Science handbook - By O'reilly] (https://tanthiamhuat.files.wordpress.com/2018/04/pythondatasciencehandbook.pdf)
- Techlead

Todas as publicações citadas devem ser referenciadas nesta seção. Caso existam trechos que caracterizam a citação e não forem citados, os mesmos serão considerados como plágio.