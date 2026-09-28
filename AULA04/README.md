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
