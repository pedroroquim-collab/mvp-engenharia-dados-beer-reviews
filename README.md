# MVP — Engenharia de Dados de Avaliações de Cervejas

MVP de Engenharia de Dados desenvolvido na pós-graduação em Ciência de Dados e Analytics da PUC-Rio. O projeto implementa um pipeline de ingestão, tratamento, controle de qualidade e modelagem dimensional de avaliações de cervejas, utilizando Databricks, Apache Spark, Delta Lake e Unity Catalog.

## Notebook

O notebook completo está disponível neste repositório, incluindo o código, as validações, o catálogo de dados, as consultas analíticas e a documentação do projeto.

**Plataforma de desenvolvimento:** Databricks Free Edition.

## Dataset

- **Fonte:** BeerAdvocate — avaliações de cervejas.
- **Formato:** CSV.
- **Volume utilizado:** 1.048.575 registros e 14 colunas.
- **Armazenamento:** volume gerenciado no Unity Catalog.

O arquivo CSV original não está incluído neste repositório. Para reproduzir o projeto, é necessário disponibilizar o conjunto de dados no ambiente Databricks e ajustar o caminho de leitura, caso necessário.

## Arquitetura

O pipeline foi desenvolvido seguindo a arquitetura Medallion:

- **Bronze:** ingestão e preservação dos dados originais.
- **Silver:** tratamento de registros incompletos, notas inválidas e campos temporais.
- **Gold:** construção de um modelo dimensional com três dimensões (cervejas, cervejarias e tempo) e uma tabela fato de avaliações.

As tabelas foram persistidas em formato Delta e organizadas no Unity Catalog.

## Resumo dos resultados

- **Bronze:** 1.048.575 registros ingeridos.
- **Silver:** 1.047.921 avaliações preservadas após a aplicação das regras de qualidade.
- **Dimensão de cervejas:** 42.551 cervejas identificadas.
- **Dimensão de cervejarias:** 3.817 cervejarias identificadas.
- **Dimensão de tempo:** 4.010 datas distintas.
- **Tabela fato:** 1.047.921 avaliações.

As consultas SQL sobre a camada Gold abordam cinco perspectivas: popularidade dos estilos, volume de avaliações por cervejaria, evolução temporal, diversidade de produtos e consistência das avaliações.

## Tecnologias

Python · PySpark · SQL · Databricks · Delta Lake · Unity Catalog

## Observações

As análises são descritivas e se limitam ao conjunto de dados utilizado no MVP. O notebook documenta as decisões de qualidade e as limitações dos dados.


## Notebook

📓 **[Acessar o MVP completo de Engenharia de Dados](https://github.com/pedroroquim-collab/mvp-engenharia-dados-beer-reviews/blob/main/MVP%20ENGENHARIA%20DE%20DADOS%20-%20BEER%20REVIEWS.ipynb)**

O notebook contém o pipeline completo, as validações de qualidade, o catálogo de dados, as consultas analíticas e a documentação do projeto.

**Plataforma de desenvolvimento:** Databricks Free Edition.
  
