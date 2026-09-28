# Ciência de Dados: Fundamentos

> **Módulo 02:** Probabilidade, Dados e Análises

## 1. Probabilidade: Conceitos Fundamentais, Regra da Adição e da Multiplicação

A teoria da probabilidade fornece o aparato matemático para quantificar incertezas, modelar fenômenos aleatórios e sustentar decisões estatísticas em Engenharia e Ciência de Dados (testes A/B, risco de crédito, detecção de anomalias e algoritmos como Naive Bayes).

---

### Fundamentos e Definição Técnica

* **Espaço Amostral ($S$):** Conjunto exaustivo de todos os resultados possíveis de um experimento aleatório.
* **Evento ($A$):** Qualquer subconjunto do espaço amostral ($A \subseteq S$).
* **Fórmula Clássica (Espaços Equiprováveis):**
  $$P(A) = \frac{n(A)}{n(S)} = \frac{\text{Número de casos favoráveis}}{\text{Número total de casos possíveis}}$$
* **Aplicações em Dados:** Avaliação de significância em testes A/B, matrizes de confusão, cálculo de propensão de churn e risco de inadimplência.

---

### Regra da Adição (União de Eventos: $A \cup B$ ou "A OU B")

Determina a probabilidade de que ao menos um dos eventos ocorra em uma tentativa.

#### Eventos Mutuamente Exclusivos (Disjuntos)
* **Condição:** Os eventos não podem ocorrer simultaneamente ($A \cap B = \emptyset \implies P(A \cap B) = 0$).
* **Fórmula:**
  $$P(A \cup B) = P(A) + P(B)$$
* **Exemplo (Dado de 6 faces):** Probabilidade de sair 1 OU 6:
  $$P(1 \cup 6) = \frac{1}{6} + \frac{1}{6} = \frac{2}{6} = \frac{1}{3} \approx 33,33\%$$

#### Eventos Não Mutuamente Exclusivos (Com Interseção)
* **Condição:** Os eventos possuem elementos em comum ($A \cap B \neq \emptyset$). A interseção deve ser subtraída para eliminar a contagem dupla.
* **Fórmula:**
  $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
* **Exemplo (Dado de 6 faces):** Probabilidade de número par ($\{2, 4, 6\}$) OU maior que 4 ($\{5, 6\}$):
  $$P(\text{par}) = \frac{3}{6}, \quad P(>4) = \frac{2}{6}, \quad P(\text{par} \cap >4) = P(\{6\}) = \frac{1}{6}$$
  $$P(\text{par} \cup >4) = \frac{3}{6} + \frac{2}{6} - \frac{1}{6} = \frac{4}{6} = \frac{2}{3} \approx 66,67\%$$

---

### Regra da Multiplicação (Interseção de Eventos: $A \cap B$ ou "A E B")

Determina a probabilidade de ocorrência conjunta, simultânea ou sucessiva de múltiplos eventos.

#### Eventos Independentes
* **Condição:** A ocorrência de $A$ não altera a probabilidade de ocorrência de $B$ ($P(B|A) = P(B)$).
* **Fórmula:**
  $$P(A \cap B) = P(A) \times P(B)$$
* **Exemplo (2 dados de 6 faces):** Obter face 6 em ambos os lançamentos:
  $$P(6_1 \cap 6_2) = \frac{1}{6} \times \frac{1}{6} = \frac{1}{36} \approx 2,78\%$$

#### Eventos Dependentes (Probabilidade Condicional)
* **Condição:** A ocorrência prévia de $A$ altera o espaço amostral ou a probabilidade de $B$.
* **Fórmula:**
  $$P(A \cap B) = P(A) \times P(B | A)$$
  * *Onde $P(B|A)$ representa a probabilidade condicional de $B$ ocorrer dado que $A$ já se concretizou.*

---

### Quadro Comparativo de Operações Probabilísticas

| Operação | Conectivo Lógico | Cenário | Expressão Matemática |
| :--- | :---: | :--- | :--- |
| **União** | **OU** | Mutuamente Exclusivos | $P(A \cup B) = P(A) + P(B)$ |
| **União** | **OU** | Não Mutuamente Exclusivos | $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ |
| **Interseção** | **E** | Independentes | $P(A \cap B) = P(A) \times P(B)$ |
| **Interseção** | **E** | Dependentes | $P(A \cap B) = P(A) \times P(B \| A)$ |
