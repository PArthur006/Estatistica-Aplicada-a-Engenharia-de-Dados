# Case de Análise de Vendas em uma Loja de Roupa

## Estudo de Caso: Otimização de Estoque e Varejo com Ciência e Engenharia de Dados

O caso aborda a resolução do desequilíbrio de estoque (ruptura de produtos de alto giro versus capital retido em peças encalhadas) por meio de análise estatística descritiva, automação de dados em Python e modelagem analítica.

---

### Diagnóstico Estatístico Aplicado ao Varejo

* **Média vs. Mediana (Tendência Central):**
  * **Problema:** A média aritmética (25 un/dia) foi distorcida para baixo pelo baixo movimento dos dias úteis.
  * **Solução:** A mediana (30 un/dia) revelou que em 50% dos dias o volume real de vendas superava a média, prevenindo subdimensionamento de compras.
* **Moda (Frequência Absoluta):**
  * **Aplicação:** Identificou a "Camiseta Básica Preta" como o item de maior volume de vendas, orientando prioridade de reposição contínua.
* **Desvio Padrão (Dispersão):**
  * **Aplicação:** Evidenciou alta volatilidade semanal, comprovando concentração de demanda crítica às sextas-feiras e sábados.
* **Decisão de Negócio:** Abandono da reposição homogênea. Adoção de compra orientada a picos de demanda para itens líderes de venda e queima estratégica de itens lentos nos dias de menor fluxo.

---

### Atuação Técnica em Engenharia de Dados

A infraestrutura substitui planilhas manuais por pipelines analíticos escaláveis e automatizados:

* **Pipeline de Ingestão e Modelagem (ETL/ELT):**
  * Extração automatizada de logs e transações do ERP da loja.
  * Tratamento de nulos, inconsistências e validação de tipos na camada *Silver*.
  * Carga em modelagem dimensional na camada *Gold*: criação de tabelas fato (ex.: `F_VendaDetalhe`) e dimensões (`D_Produto`, `D_Calendario`) para consultas OLAP.
* **Automação Analítica (Python / Pandas):**
  * Desenvolvimento de scripts para cálculo contínuo de métricas estatísticas:
    * Média: `.mean()`
    * Mediana: `.median()`
    * Moda: `.mode()`
    * Desvio Padrão: `.std()`
  * Geração e disparo automático de alertas e métricas para a gestão de compras.

---

### Matriz de Impacto Analítico no Varejo

| Etapa Analítica | Conceito Aplicado | Ação Prática no Varejo | Impacto Operacional e Financeiro |
| :--- | :--- | :--- | :--- |
| **Diagnóstico de Volume** | Média vs. Mediana | Isolar o impacto de dias atípicos (fracos ou picos). | Evita subdimensionamento ou compra excessiva baseada em métricas distorcidas. |
| **Giro de Produto** | Moda | Mapear o SKU com maior frequência de saída. | Elimina ruptura de estoque do item campeão de vendas. |
| **Gestão de Risco** | Desvio Padrão | Mensurar a oscilação da demanda ao longo da semana. | Otimiza a escala de estoque para fins de semana e reduz capital parado na semana. |

---

### Conexão com o Mercado Corporativo Real

* **Pirelli:** Implementação de visibilidade analítica em tempo real para rastrear estoque e pedidos, eliminando gargalos logísticos.
* **Magazine Luiza:** Mineração de séries históricas de navegação e vendas para previsão de demanda regionalizada e controle centralizado de compras.
* **Target:** Modelos preditivos alimentados por padrões sutis de compra para antecipar a demanda de categorias de produtos antes da manifestação direta do cliente.
* **Amazon:** Monitoramento contínuo de elasticidade e níveis de estoque em tempo real para precificação dinâmica e aceleração do giro de inventário.