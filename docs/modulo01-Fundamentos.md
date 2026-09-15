# Ciência de Dados: Fundamentos

> **Módulo 01:** Fundamentos da Ciência de Dados

## 1. A Ciência de Dados

### O que é e Pilares Principais

Ciência de Dados combina programação, matemática/estatística e conhecimento do negócio para encontrar padrões em dados e apoiar decisões automáticas ou estratégicas.

* **Interdisciplinaridade:** Código sozinho não resolve; você precisa entender a matemática por trás do modelo e a regra de negócio da empresa.
* **Big Data:** Lidar com grande volume, variedade e velocidade (logs, eventos em tempo real, bancos relacionais e NoSQL).
* **Técnicas Analíticas:** Uso de Machine Learning para prever cenários e gráficos para comunicar os achados.
* **Automação e Escala:** Criação de rotinas que rodam sozinhas em produção, sem intervenção humana a cada execução.
* **Foco Prático:** Resolver problemas reais da empresa (ex.: prever cancelamentos, fraudes ou gargalos de vendas).

### Estatística e Probabilidade

A matemática é o que garante que o modelo aprendeu um padrão real, e não apenas uma coincidência nos dados.

#### Estatística Descritiva vs. Inferencial
| Tipo | O que faz | Exemplo Prático | Por que o mercado usa |
| :--- | :--- | :--- | :--- |
| **Descritiva** | Resume e descreve a base atual. | Média, mediana, desvio padrão, gráficos de distribuição. | Entender a qualidade dos dados e achar anomalias logo no início. |
| **Inferencial** | Tira conclusões sobre uma população usando apenas uma amostra. | Testes de hipótese, intervalos de confiança. | Economia de processamento: testar hipóteses em amostras representativas sem precisar varrer tabelas gigantescas na nuvem. |

#### Probabilidade
* **Conceito:** Mede a chance de um evento acontecer em cenários de incerteza.
* **No mercado:** Tomada de decisão baseada em risco. Em aprovação de crédito, por exemplo, o banco nunca tem 100% de certeza se o cliente vai pagar; ele calcula a probabilidade de calote para definir o limite ou a taxa de juros.

---

### Aspectos Essenciais na Prática

#### 3.1 Machine Learning (Aprendizado de Máquina)
O algoritmo encontra as regras sozinho a partir do histórico, substituindo blocos manuais de `if/else` que ficariam inviáveis de manter.

* **Supervisionado:** Usa dados com resposta conhecida (rótulo).
  * *Classificação:* Resposta em categorias (ex.: "fraude" ou "não fraude").
  * *Regressão:* Resposta em número contínuo (ex.: prever o valor de uma venda).
* **Não Supervisionado:** Dados sem resposta prévia. O algoritmo agrupa por semelhança.
  * *Exemplo:* Agrupamento (clustering) de clientes com perfis parecidos de compra.
* **Deep Learning:** Redes neurais complexas (usando PyTorch ou TensorFlow) voltadas para dados não estruturados, como imagens e texto livre.

#### 3.2 Engenharia e Preparação de Dados
* **Realidade do trabalho:** 70% a 80% do tempo de um projeto é gasto limpando a base (tratar nulos, remover duplicatas, normalizar valores e corrigir formatos).
* **Regra básica:** Se a entrada for dado corrompido ou mal tratado, a previsão do modelo será inútil (*garbage in, garbage out*).
* **Ferramentas comuns:** Python (Pandas, Matplotlib, Seaborn) e ferramentas de BI (Tableau, Power BI) para análise visual.

#### 3.3 Validação do Modelo e Big Data
* **Overfitting (Sobreajuste):** Quando o modelo "decora" os dados de treino e falha feio ao receber dados novos da produção.
  * *Como evitar:* Separar os dados em treino e teste, ou usar validação cruzada (dividir a base em vários pedaços para testar).
* **Métricas de avaliação:**
  * Para números contínuos: Erro Médio Quadrático (MSE).
  * Para categorias: Não confiar só na acurácia geral. Olhar precisão, taxa de acerto da classe minoritária e matriz de confusão (medir falsos positivos vs. falsos negativos).
* **Ferramentas de Big Data:** Quando a máquina local não aguenta o volume, usa-se processamento distribuído (Spark, Hadoop) e mensageria em tempo real (Kafka).

#### 3.4 Ética e Governança
* **Governança:** Regras para manter os dados seguros, organizados, documentados e com acessos restritos.
* **Privacidade (LGPD):** Anonimização de dados pessoais e respeito ao consentimento do usuário para evitar multas e problemas jurídicos.
* **Viés algorítmico:** Garantir que o modelo não tome decisões preconceituosas ou discriminatórias (ex.: rejeição automática de candidatos ou de crédito por critérios indevidos).

