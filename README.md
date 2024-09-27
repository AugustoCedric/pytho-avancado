# pytho-avancado

Repositório do projeto de extração de dados de filmes do IMDB usando Python.

## Índice

- [Descrição do Projeto](#descrição-do-projeto)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Uso](#uso)
- [Estrutura do Código](#estrutura-do-código)
- [Funções Principais](#funções-principais)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Descrição do Projeto

Este projeto realiza a extração de dados de filmes da seção "Filmes Mais Populares" do IMDB. Os dados extraídos incluem título, data de lançamento, classificação e sinopse dos filmes, que são salvos em um arquivo CSV.

## Pré-requisitos

Antes de executar o projeto, você precisa ter o Python 3.x instalado, além das seguintes bibliotecas:

- requests
- beautifulsoup4

Para instalar as dependências, você pode usar o seguinte comando:


pip install requests beautifulsoup4


## Informações do Autor
- **Nome**: Augusto Cedric
- **Curso**: Fullstack Python
- **Instituição**: EBAC


## Instalação
- Clone o repositório:

- git clone https://github.com/usuario/pytho-avancado.git
- Navegue até o diretório do projeto:


- cd pytho-avancado
- Instale as dependências (caso ainda não tenha feito):

- pip install -r requirements.txt

# Uso
- Para executar o script e iniciar a extração de dados, basta rodar o arquivo principal:


- python main.py
- Os dados extraídos serão salvos no arquivo movies.csv na mesma pasta do projeto.

## Estrutura do Código
- main.py: Arquivo principal que contém a lógica de extração de dados.
- movies.csv: Arquivo onde os dados extraídos dos filmes são armazenados.
- Funções Principais

- extract_movie_details(movie_link)
- Extrai os detalhes de um filme a partir do link fornecido. Os dados extraídos incluem:

- Título
- Data de lançamento
- Classificação

## Sinopse
## extract_movies(soup)
- Extrai os links dos filmes da página de "Filmes Mais Populares" e inicia a extração de detalhes usando múltiplas threads para otimizar o tempo de execução.

## main()
- Função principal que orquestra o fluxo do programa:

- Realiza a requisição para obter a página de "Filmes Mais Populares".
- Chama a função extract_movies para extrair os detalhes dos filmes.

# Threading e Processamento
- Este projeto utiliza threading para otimizar a extração de dados. A classe ThreadPoolExecutor do módulo concurrent.futures é utilizada para criar um pool de threads que permite executar várias solicitações de extração simultaneamente. Isso melhora o desempenho e reduz o tempo total de execução, especialmente ao lidar com um grande número de URLs.


- Vantagens do Uso de Threads
- Desempenho Melhorado: O uso de threads permite que múltiplas solicitações sejam feitas ao mesmo tempo, aproveitando a latência das operações de rede.
- Eficiência de Tempo: Em vez de processar cada filme sequencialmente, as threads ajudam a reduzir o tempo total de execução ao lidar com várias tarefas simultaneamente.
``` 
