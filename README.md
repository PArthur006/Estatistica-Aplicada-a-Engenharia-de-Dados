# 📊 Fundamentos da Ciência de Dados & Engenharia Reversa de Cases

Repositório dedicado ao armazenamento, consolidação teórica e aplicação prática dos conceitos abordados no curso **Fundamentos da Ciência de Dados**. 

O objetivo deste espaço é duplo:
1. **Base de Conhecimento:** Centralizar anotações técnicas e resumos estruturados dos módulos teóricos.
2. **Laboratório Prático (Engenharia Reversa):** Documentar os estudos de caso (cases) do curso e transformá-los em pipelines funcionais de Engenharia de Dados, com foco em Data Quality, modelagem, ingestão e arquitetura de dados.

---

## 📁 Estrutura do Repositório

```text
.
├── docs/                      # Anotações teóricas e resumos dos módulos
│   ├── modulo-1-fundamentos.md
│   ├── modulo-2-estatistica.md
│   └── modulo-3-inferencia-outliers.md
├── cases/                     # Implementações práticas e resumos dos cases
│   ├── case-1-analise-vendas/
│   │   ├── README.md          # Resumo do case e arquitetura da solução
│   │   ├── src/               # Scripts de mock, pipeline e data quality
│   │   └── data/              # Dados sintéticos gerados
│   ├── case-2-satisfacao-restaurante/
│   │   ├── README.md
│   │   └── src/
│   └── case-3-precificacao-imoveis/
│       ├── README.md
│       └── src/
├── requirements.txt           # Dependências do projeto (Pandas, PySpark, Faker, etc.)
└── README.md                  # Documentação principal