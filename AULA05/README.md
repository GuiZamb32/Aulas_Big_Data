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