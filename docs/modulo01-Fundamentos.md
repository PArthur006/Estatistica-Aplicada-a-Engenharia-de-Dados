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

---

## 2. A Evolução da Ciência de Dados

A área evoluiu de formulações matemáticas isoladas para o núcleo de decisões estratégicas corporativas e enfrentamento de problemas globais (mudanças climáticas, saúde pública e segurança).


### Linha do Tempo da Evolução

| Período | Marco Principal | Tecnologias / Conceitos | Aplicação no Mercado |
| :--- | :--- | :--- | :--- |
| **Séc. XVII ao Início Séc. XX** | **Origens Históricas** | Teoria das Probabilidades, Teorema de Bayes, Mínimos Quadrados (Gauss/Legendre). | Base matemática para modelos de crédito e regressões lineares sem virar "caixa-preta". |
| **Anos 1950 a 1970** | **Revolução Tecnológica** | Computadores modernos, Teoria da Informação (Shannon), SGBDR e SQL (Edgar F. Codd), ACID. | Espinha dorsal de sistemas transacionais (ERPs, CRMs), garantindo consistência bancária e sem perdas de registros. |
| **Anos 1980 a 2000** | **Era do Big Data** | Migração do analógico para o digital, queda de custo de storage, primeiros Data Warehouses, Data Mining. | Armazenamento de histórico longo de vendas em Data Warehouses para cruzar dados via Business Intelligence (BI). |
| **Século XXI** | **Consolidação da Área** | "Três Vs" (Volume, Velocidade, Variedade), NoSQL (MongoDB), Hadoop/MapReduce, Apache Spark, Python e R. | Adoção de **Data Lakes**: armazenamento de dados brutos heterogêneos para processar sob demanda via clusters distribuídos. |
| **Dias Atuais** | **IA Profunda e Desafios** | Deep Learning, Aprendizado Federado, IA Explicável (XAI), LGPD/GDPR. | Modelos preditivos integrados a regras rígidas de compliance, auditoria e explicabilidade de decisões. |


### Desafios Críticos Atuais

#### Privacidade e Regulação
* **Cenário:** Leis como LGPD e GDPR exigem governança estrita sobre dados de ponta a ponta.
* **Impacto:** O vazamento ou uso indevido de dados gera sanções financeiras pesadas e perda de credibilidade corporativa.

#### Vieses Algorítmicos e Discriminação
* **Cenário:** Modelos treinados com dados históricos enviesados reproduzem e automatizam preconceitos passados.
* **Impacto:** Decisões automáticas injustas (ex.: recusa de vagas de emprego ou crédito bancário) abrem passivos jurídicos e éticos graves.

#### Transparência e IA Explicável (XAI)
* **Cenário:** Modelos de Deep Learning e ensembles complexos funcionam como "caixas-pretas".
* **Solução:** Aplicação de bibliotecas como **SHAP** e **LIME** para detalhar as variáveis exatas que levaram àquela previsão.
* **No mercado:** Sem explicabilidade, diretorias e órgãos reguladores não aprovam a entrada do modelo em produção.

#### Aprendizado Federado (Federated Learning)
* **Cenário:** Necessidade de treinar modelos sem centralizar dados confidenciais dos usuários em um único servidor.
* **Solução:** O modelo é enviado para treinar localmente nos aparelhos (celulares, sensores IoT) e apenas os pesos matemáticos ajustados retornam para consolidar o modelo global.

---

## 3. Exemplos de Aplicação da Ciência de Dados

Aplicações práticas da disciplina divididas por setor econômico, tipo de dado consumido e soluções adotadas em produção.


### Tabela Comparativa de Casos de Uso

| Setor | Tipos de Dados Utilizados | Solução / Algoritmo Aplicado | Objetivo Prático no Mercado |
| :--- | :--- | :--- | :--- |
| **Saúde e Medicina** | Prontuários eletrônicos (EHR), exames de imagem, logs hospitalares. | Deep Learning (visão computacional), classificação e séries temporais. | Diagnóstico precoce de patologias, previsão de surtos e alertas automáticos de risco do paciente. |
| **Serviços Financeiros** | Fluxo de transações em tempo real, geolocalização e cadastros. | Árvores de Decisão, KNN, regressões logísticas. | Prevenção a fraudes em milissegundos e cálculo de risco de crédito (*credit scoring*). |
| **Marketing e Varejo** | Histórico de compras, clickstream, buscas e redes sociais. | Sistemas de recomendação (filtragem colaborativa), clusterização, regressão. | Personalização de catálogo, precificação dinâmica em tempo real e redução de churn. |
| **Indústria e Manufatura** | Séries temporais de telemetria IoT (vibração, temperatura, pressão). | Modelos preditivos de regressão e visão computacional na esteira. | Manutenção preditiva (evitar parada de linha) e controle automático de qualidade de peças. |
| **Agricultura** | Imagens de satélite, dados de sensores de solo e previsão climática. | Modelagem preditiva geoespacial e regressão multivariável. | Otimização de janelas de plantio/colheita, irrigação de precisão e estimativa de safra. |
| **Setor Público e Governança** | Dados abertos, censo, GPS de transporte e registros fiscais. | Otimização de fluxos, detecção de anomalias financeiras e visualização espacial (ex.: DataViva). | Gestão de tráfego urbano, combate à evasão fiscal e direcionamento de verbas públicas. |
| **Educação** | Logs de navegação em AVA (tempo de tela, cliques, notas). | Modelagem preditiva e sistemas de recomendação instrucional. | Prevenção de evasão escolar/universitária e trilhas de estudo personalizadas. |
| **Esportes e Entretenimento** | Telemetria de atletas e métricas de consumo de streaming. | Análise de regressão para scouting de atletas e algoritmos de recomendação de mídia. | Contratação de talentos subvalorizados e decisões sobre investimentos em novas produções. |
| **Sustentabilidade** | Séries meteorológicas, telemetria naval (AIS) e imagens de satélite. | Processamento em larga escala (Google Earth Engine) e modelos de dispersão. | Monitoramento de emissões de CO2, mapeamento de desmatamento e auditoria de metas ESG. |


### Padrões Técnicos Observados no Mercado

#### 1. Ingestão em Tempo Real vs. Processamento em Lote (Batch)
* **Tempo Real (Streaming):** Obrigatório em detecção de fraude e telemetria de sensores industriais, onde a inferência atrasada invalida o resultado.
* **Lote (Batch):** Utilizado em cálculos de risco de crédito diário, relatórios de sustentabilidade e re-treinamento periódico de recomendações.

#### 2. Trade-off entre Complexidade e Latência
* Modelos de *deep learning* entregam precisão alta para exames de imagem e visão computacional na manufatura, mas demandam hardware dedicado (GPUs).
* Cenários de altíssima frequência (ex.: aprovação de transações de cartão) priorizam modelos mais leves (árvores de decisão, regressões calibradas) que respondem abaixo de 50 milissegundos.

---

## 4. Modelagem Dimensional e Arquitetura Medallion em Lakehouses

Organização em camadas que garante a transição incremental de dados brutos e não confiáveis até bases de consumo de alto desempenho analítico.


### Camadas Medallion

| Camada | Estado do Dado | Operações Principais | Tecnologias / Formatos | Consumidores Típicos |
| :--- | :--- | :--- | :--- | :--- |
| **Bronze** *(Raw)* | Bruto, íntegro, sem tratamento (cópia fiel da origem). | Ingestão contínua ou batch; preservação do histórico de logs, APIs, CDC e Kafka. | Cloud Object Storage (S3, GCS, ADLS) com formatos transacionais ACID (**Delta Lake**, Parquet). | Engenheiros de Dados e pipelines de saneamento. |
| **Silver** *(Enriched)* | Limpo, padronizado, tipado e deduplicado. | Cast de tipos, remoção de duplicatas, tratamento de nulos, mascaramento LGPD/GDPR. | Delta Lake / Parquet, tabelas semiestruturadas ou desnormalizadas. | Cientistas de Dados (EDA/Features) e analistas técnicos. |
| **Gold** *(Curated)* | Agregado, modelado para o negócio e de alta performance. | Modelagem Dimensional (Fatos e Dimensões), agregações pré-calculadas e regras de negócio. | Delta Lake, Data Warehouses analíticos e views otimizadas. | Ferramentas de BI (Power BI, Tableau), executivos e modelos de IA em produção. |


### Modelagem Dimensional na Camada Gold

Técnica de estruturação focada exclusivamente em otimizar consultas analíticas complexas sem sobrecarregar bancos transacionais (OLTP).

#### Star Schema vs. Snowflake Schema
* **Star Schema (Padrão de Mercado):**
  * Dimensões desnormalizadas conectam-se diretamente à tabela Fato central.
  * *Vantagem corporativa:* **Menor número de JOINs**, resultando em menor latência de consulta e custos reduzidos de computação em relatórios analíticos.
* **Snowflake Schema:**
  * Dimensões normalizadas e divididas em sub-dimensões hierárquicas (ex.: `Fato` $\to$ `Cliente` $\to$ `Cidade` $\to$ `Estado`).
  * *Trade-off:* Economiza armazenamento (irrelevante no custo de nuvem atual), mas penaliza consultas devido aos múltiplos JOINs necessários.

#### Boas Práticas Técnicas

* **Uso de Surrogate Keys (Chaves Artificiais):**
  * *Regra:* Nunca usar a chave natural de negócio (ex.: CPF, UUID de API, ID do ERP) como chave primária de relacionamento na Fato.
  * *Implementação:* Gerar chaves numéricas sequenciais/hash no próprio pipeline de carga.
  * *Motivo de Mercado:* Isola o Data Lakehouse de mutações, migrações ou redefinições no sistema transacional de origem e acelera a indexação matemática em bancos colunares.

* **Metadados de Rastreabilidade (Data Lineage):**
  * Toda tabela final de Fato e Dimensão deve conter colunas técnicas de auditoria:
    * `LinData`: Timestamp do momento em que a linha foi inserida/processada pelo pipeline.
    * `LinOrig`: Identificador do sistema de origem de onde aquele registro foi extraído.
  * *Motivo de Mercado:* Facilita o rastreamento em incidentes de dados, auditorias externas e reprocessamento pontual de partições corrompidas.

