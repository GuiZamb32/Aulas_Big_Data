# Aulas Big Data

Repositório destinado ao estudo prático de **Big Data, bancos de dados distribuídos, processamento de dados, ETL, computação em nuvem e arquiteturas de dados**.

O projeto reúne os materiais, códigos, exercícios e laboratórios desenvolvidos ao longo das aulas, organizados progressivamente desde conceitos de bancos NoSQL até a construção de pipelines de dados utilizando **Apache Spark, PySpark, AWS S3, Azure Blob Storage e arquitetura Medalhão**.

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
* Desenvolver uma base prática para projetos de Engenharia de Dados e Ciência de Dados.

---

## Conteúdo do Repositório

O conteúdo está organizado por aulas, seguindo uma evolução dos conceitos básicos para arquiteturas de processamento e armazenamento de dados mais completas.

### AULA01 — Bancos de Dados e Sistemas Distribuídos

A primeira etapa aborda conceitos relacionados a bancos de dados distribuídos, replicação, consistência e disponibilidade.

Entre os laboratórios estão:

* **RDS / PostgreSQL**

  * Replicação síncrona e assíncrona.
  * Multi-AZ.
  * Read Replica.
  * Análise prática dos efeitos da latência.
  * Relação entre consistência e disponibilidade.
  * Conceitos relacionados ao PACELC.

* **Redis / ElastiCache**

  * Armazenamento em memória.
  * Replicação.
  * Disponibilidade.
  * Comportamento diante de falhas.

* **DynamoDB / ScyllaDB**

  * Bancos NoSQL distribuídos.
  * Modelo de chave-valor.
  * Distribuição e replicação.
  * Consistência e disponibilidade.

* **Cassandra**

  * Cluster distribuído.
  * Fator de replicação.
  * Níveis de consistência.
  * `ONE`, `QUORUM` e `ALL`.
  * Comportamento do sistema conforme a quantidade de nós disponíveis.

Esses laboratórios permitem observar na prática como diferentes arquiteturas lidam com replicação, falhas, latência e consistência.

---

### AULA02 — Modelos de Dados NoSQL

A segunda etapa aborda diferentes modelos de bancos de dados NoSQL e suas respectivas formas de organização dos dados.

Os conteúdos estão divididos em:

* **Key-Value**

  * Estrutura baseada em chave e valor.
  * Características e casos de uso.

* **Document**

  * Armazenamento orientado a documentos.
  * Estrutura flexível.
  * Organização de dados em documentos.

* **Column**

  * Bancos orientados a colunas.
  * Estruturas distribuídas.
  * Organização e acesso aos dados.

A aula permite comparar diferentes modelos NoSQL e compreender como a estrutura dos dados influencia a forma de armazenamento e consulta.

---

### AULA03 — PySpark Básico

A terceira etapa introduz o **Apache Spark** utilizando **PySpark**.

Os exemplos trabalham conceitos fundamentais de processamento de dados, incluindo:

* Primeiro contato com Spark.
* `SparkSession`.
* DataFrames.
* Schema.
* Operações com colunas.
* Transformações.
* Ações.
* Funções do Spark SQL.
* Processamento de arquivos.
* ETL local.
* Manipulação e transformação de dados.
* Exercícios práticos.
* Processamento de dados relacionados ao ENEM.

Entre os arquivos principais estão exemplos de:

```text
00_primeiro_contato.py
01_dataframe.py
02_funcionalidades.py
03_etl_local.py
05_etl_enem_sc.py
pratica.py
pratica_enem.py
```

Essa etapa estabelece a base necessária para os laboratórios posteriores envolvendo armazenamento em nuvem e pipelines distribuídos.

---

### AULA04 — PySpark e Armazenamento em Nuvem

A quarta etapa amplia o uso do PySpark para trabalhar com armazenamento de objetos.

São abordadas duas plataformas:

#### AWS S3

O laboratório trabalha com:

* Conexão com armazenamento de objetos.
* Upload e download de arquivos.
* Processamento de dados com PySpark.
* ETL.
* Dados relacionados ao consumo de energia em Santa Catarina.
* Integração entre processamento e armazenamento.

Estrutura principal:

```text
AULA04/
└── PYSPARK-AWS-S3/
    ├── 00_conectar_s3.py
    ├── 01_etl_energia_sc.py
    ├── comum.py
    ├── verificar_ambiente.py
    ├── SETUP.md
    └── EXERCICIOS_AWS.md
```

#### Azure Blob Storage

O laboratório também trabalha com armazenamento de objetos utilizando uma estrutura compatível com Azure Blob Storage.

São abordados:

* Conexão com Blob Storage.
* Upload e download de arquivos.
* Listagem de blobs.
* Processamento de dados com PySpark.
* ETL.
* Dados de temperatura de cidades de Santa Catarina.
* Validação e enriquecimento dos dados.

Estrutura principal:

```text
AULA04/
└── PYSPARK-AZURE-BLOB/
    ├── 00_conectar_blob.py
    ├── 01_etl_temperaturas_sc.py
    ├── comum.py
    ├── verificar_ambiente.py
    ├── SETUP.md
    └── EXERCICIOS_AZURE.md
```

---

### AULA05 — Arquitetura Medalhão

A quinta etapa apresenta a **Arquitetura Medalhão**, organizando o pipeline de dados em diferentes níveis de processamento:

```text
Fonte
  │
  ▼
Bronze
  │
  ▼
Silver
  │
  ▼
Gold
```

#### Bronze

Representa os dados em seu estado original, mantendo as informações recebidas da fonte e adicionando informações de proveniência.

Objetivos:

* Preservar os dados originais.
* Permitir auditoria.
* Possibilitar reprocessamento.
* Evitar perda de informações durante a ingestão.

#### Silver

Representa os dados tratados e validados.

São realizadas operações como:

* Normalização.
* Deduplicação.
* Validação.
* Identificação de registros inválidos.
* Separação entre dados aprovados e rejeitados.
* Registro dos motivos de rejeição.

#### Gold

Representa os dados preparados para consumo e análise.

São realizadas operações como:

* Classificação.
* Enriquecimento.
* Agregações.
* Resumos por região.
* Organização dos dados para utilização analítica.

Um dos laboratórios utiliza dados de qualidade do ar, trabalhando com informações como:

* PM2.5.
* PM10.
* CO.
* Município.
* Região.
* Classificação da qualidade do ar.

A principal diferença em relação aos laboratórios anteriores é que cada camada funciona como um **job independente**, permitindo que uma etapa seja reprocessada sem necessariamente executar novamente todo o pipeline.

---

## Tecnologias e Ferramentas

As principais tecnologias utilizadas no repositório incluem:

| Tecnologia         | Utilização                                |
| ------------------ | ----------------------------------------- |
| Python             | Desenvolvimento dos scripts e pipelines   |
| PySpark            | Processamento e transformação de dados    |
| Apache Spark       | Motor de processamento distribuído        |
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

---

## Organização

A estrutura geral do projeto segue a organização abaixo:

```text
Aulas_Big_Data/
│
├── AULA01/
│   ├── RDS/
│   ├── cassandra/
│   ├── dynamodb-scylladb/
│   └── elastic-cache-redis/
│
├── AULA02/
│   ├── Collumn/
│   ├── Document/
│   └── KeyValue/
│
├── AULA03/
│   └── PYSPARK-BASICO/
│
├── AULA04/
│   ├── PYSPARK-AWS-S3/
│   └── PYSPARK-AZURE-BLOB/
│
├── AULA05/
│   ├── PYSPARK-MEDALHAO/
│   ├── PYSPARK-MEDALHAO-AWS-S3/
│   └── PYSPARK-MEDALHAO-AZURE-BLOB/
│
├── .gitignore
├── LICENSE
└── README.md
```

Cada laboratório possui sua própria documentação, scripts, exercícios e instruções de configuração quando necessário.

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
* Comparação entre diferentes arquiteturas.
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
Engenharia de Dados
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
