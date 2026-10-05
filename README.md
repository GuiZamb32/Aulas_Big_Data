# Aulas Big Data

Repositório destinado ao estudo prático de **Big Data, bancos de dados distribuídos, processamento de dados, ETL, computação em nuvem e arquiteturas de dados**.

O projeto reúne os materiais, códigos, exercícios e laboratórios desenvolvidos ao longo das aulas, organizados progressivamente desde conceitos de bancos NoSQL até a construção de pipelines de dados utilizando **Apache Spark, PySpark, AWS S3, Azure Blob Storage, arquitetura Medalhão e Spark ML**.

A proposta do repositório é manter uma documentação prática e organizada do processo de aprendizagem, permitindo acompanhar a evolução dos conceitos e das implementações realizadas.

---

## Objetivos

Este repositório tem como principais objetivos:

* Estudar conceitos fundamentais de Big Data.
* Compreender diferentes modelos de armazenamento de dados.
* Trabalhar com bancos de dados relacionais e NoSQL.
* Explorar conceitos de consistência, disponibilidade e replicação.
* Compreender o modelo PACELC.
* Desenvolver pipelines de ETL.
* Utilizar Apache Spark e PySpark para processamento distribuído.
* Trabalhar com armazenamento de objetos em ambientes de nuvem.
* Implementar processos de ingestão, transformação, validação e agregação.
* Aplicar a arquitetura Medalhão em pipelines de dados.
* Explorar Machine Learning distribuído utilizando Spark ML.
* Trabalhar com aprendizado supervisionado e não supervisionado.
* Desenvolver uma base prática para projetos de Engenharia de Dados e Ciência de Dados.

---

## Conteúdo do Repositório

O conteúdo está organizado por aulas, seguindo uma evolução dos conceitos básicos para arquiteturas de processamento, armazenamento e análise de dados mais completas.

#### AULA01 — Bancos de Dados e Sistemas Distribuídos

#### AULA02 — Modelos de Dados NoSQL

#### AULA03 — PySpark Básico

#### AULA04 — PySpark e Armazenamento em Nuvem

#### AULA05 — Arquitetura Medalhão

#### AULA06 — Spark ML e Machine Learning

---

## Tecnologias e Ferramentas

As principais tecnologias utilizadas no repositório incluem:

| Tecnologia         | Utilização                                |
| ------------------ | ----------------------------------------- |
| Python             | Desenvolvimento dos scripts e pipelines   |
| PySpark            | Processamento e transformação de dados    |
| Apache Spark       | Motor de processamento distribuído        |
| Spark MLlib        | Machine Learning distribuído              |
| PostgreSQL         | Banco de dados relacional                 |
| Redis              | Armazenamento em memória                  |
| Cassandra          | Banco NoSQL distribuído                   |
| DynamoDB           | Banco NoSQL orientado a chave-valor       |
| ScyllaDB           | Banco NoSQL distribuído                   |
| AWS S3             | Armazenamento de objetos                  |
| Azure Blob Storage | Armazenamento de objetos                  |
| Docker             | Execução de ambientes e serviços isolados |
| Docker Compose     | Orquestração dos ambientes locais         |
| Git                | Controle de versão                        |
| GitHub             | Hospedagem e documentação do projeto      |

---

## Conceitos Trabalhados

Ao longo das aulas são explorados conceitos importantes para Big Data e Engenharia de Dados, como:

* Big Data.
* Sistemas distribuídos.
* Bancos relacionais.
* Bancos NoSQL.
* Key-Value.
* Document databases.
* Column-oriented databases.
* Replicação.
* Consistência.
* Disponibilidade.
* Tolerância a falhas.
* Latência.
* PACELC.
* ETL.
* DataFrames.
* Apache Spark.
* PySpark.
* Processamento distribuído.
* Data Lake.
* Object Storage.
* AWS S3.
* Azure Blob Storage.
* Data Quality.
* Validação de dados.
* Deduplicação.
* Data Lineage.
* Arquitetura Medalhão.
* Bronze.
* Silver.
* Gold.
* Pipelines de dados.
* Machine Learning.
* Spark MLlib.
* Aprendizado supervisionado.
* Aprendizado não supervisionado.
* Classificação.
* Regressão.
* Clusterização.
* Redução de dimensionalidade.
* Avaliação de modelos.
* Validação cruzada.
* Ajuste de hiperparâmetros.
* Sistemas de recomendação.
* Processamento de texto.

---

## Organização

Cada laboratório possui sua própria documentação, scripts, exercícios e instruções de configuração quando necessário.

As atividades mais avançadas utilizam a estrutura de processamento em camadas **Bronze, Silver e Gold**, permitindo separar ingestão, preparação e aplicação dos modelos ou transformações.

---

## Metodologia

Os conteúdos são desenvolvidos com foco em experimentação prática.

Em vez de apenas apresentar conceitos teóricos, os laboratórios procuram demonstrar o comportamento dos sistemas através de:

* Execução de ambientes locais.
* Containers Docker.
* Simulação de falhas.
* Medição de desempenho.
* Processamento de dados reais e sintéticos.
* Exercícios práticos.
* Pipelines de ETL.
* Pipelines de ELT.
* Aplicação de modelos de Machine Learning.
* Comparação entre diferentes arquiteturas.
* Avaliação de resultados e métricas.
* Validação dos resultados obtidos.

Essa abordagem permite relacionar os conceitos teóricos com situações próximas das encontradas em ambientes reais de dados.

---

## Evolução do Aprendizado

A organização das aulas segue uma progressão:

```text
Bancos de Dados
      │
      ▼
Sistemas Distribuídos
      │
      ▼
NoSQL
      │
      ▼
Processamento com PySpark
      │
      ▼
ETL
      │
      ▼
Armazenamento em Nuvem
      │
      ▼
Pipelines de Dados
      │
      ▼
Arquitetura Medalhão
      │
      ▼
Spark ML
      │
      ▼
Machine Learning
      │
      ▼
Engenharia de Dados
      │
      ▼
Ciência de Dados
```

Dessa forma, os conteúdos das primeiras aulas servem como base para os laboratórios mais avançados.

---

## Como utilizar este repositório

Cada aula possui uma documentação própria.

Para estudar um conteúdo específico, entre na pasta correspondente e consulte o `README.md` daquele laboratório.

Exemplo:

```bash
cd AULA03/PYSPARK-BASICO
```

ou:

```bash
cd AULA05/PYSPARK-MEDALHAO
```

ou:

```bash
cd AULA06/PYSPARK-SPARK-ML
```

Os arquivos `SETUP.md`, quando disponíveis, apresentam as configurações necessárias para execução do ambiente.

Os arquivos `EXERCICIOS*.md` apresentam os exercícios associados a cada laboratório.

---

## Requisitos

Dependendo do laboratório, podem ser necessários:

* Python 3.11
* Java
* Apache Spark
* PySpark
* Docker
* Docker Compose
* Git
* Windows, Linux ou WSL
* Configurações específicas de ambiente descritas nos respectivos `SETUP.md`

Os requisitos podem variar entre as aulas. Por isso, recomenda-se consultar a documentação específica de cada laboratório antes da execução.

---

## Estrutura dos Laboratórios

Os laboratórios foram organizados para que cada pasta possa ser estudada de maneira relativamente independente.

| Aula   | Tema principal               | Principais tecnologias                           |
| ------ | ---------------------------- | ------------------------------------------------ |
| AULA01 | Bancos distribuídos e PACELC | PostgreSQL, Redis, Cassandra, DynamoDB, ScyllaDB |
| AULA02 | Modelos NoSQL                | Key-Value, Document, Column                      |
| AULA03 | Processamento de dados       | Python, PySpark, Apache Spark                    |
| AULA04 | ETL e armazenamento em nuvem | PySpark, AWS S3, Azure Blob                      |
| AULA05 | Arquitetura Medalhão         | PySpark, Bronze, Silver, Gold                    |
| AULA06 | Machine Learning             | Spark MLlib, PySpark, Spark ML                   |

---


A estrutura da aula está dividida em diferentes laboratórios:

| Laboratório                           | Conteúdo                                      |
| ------------------------------------- | --------------------------------------------- |
| `PYSPARK-SPARK-ML`                    | Spark ML integrado ao ELT Medalhão            |
| `PYSPARK-SPARK-ML-PARTE2`             | Fraude, classificação de texto e recomendação |
| `PYSPARK-SPARK-ML-PARTE3`             | Manutenção preditiva e validação cruzada      |
| `PYSPARK-SPARK-ML-SUPERVISIONADO`     | Classificação e regressão supervisionadas     |
| `PYSPARK-SPARK-ML-NAO-SUPERVISIONADO` | K-Means e PCA                                 |

A documentação detalhada de cada laboratório está disponível dentro de suas respectivas pastas.

---

## Status

Este repositório representa um material de estudo em evolução.

Novas aulas, exercícios, experimentos e implementações podem ser adicionados conforme o avanço dos estudos em Big Data, Ciência de Dados e Engenharia de Dados.

---

## Autor

**Guilherme Zamboni**

Desenvolvedor Full Stack e estudante de Ciência de Dados e Inteligência Artificial.

GitHub: [GuiZamb32](https://github.com/GuiZamb32)

---

## Licença

Este projeto está disponível sob a licença definida no arquivo [LICENSE](LICENSE).
