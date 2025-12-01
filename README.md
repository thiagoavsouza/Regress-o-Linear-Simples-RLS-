# Regressão Linear Simples — Idade x Valor do Seguro

## Descrição do Projeto

Este projeto aplica **Regressão Linear Simples** para investigar a relação entre
a variável **Idade (age)** e o **Valor do Seguro (charges)** utilizando o Insurance
Charges Dataset.

O objetivo é identificar se a idade possui influência estatisticamente
significativa sobre o custo do seguro e avaliar o poder explicativo desse modelo.

---

## Etapas do Projeto

### 1. Importação e Análise Inicial dos Dados
- Carregamento do dataset de custos de seguro.
- Inspeção das variáveis:
  - age
  - sex
  - bmi
  - children
  - smoker
  - region
  - charges

---

### 2. Análise Exploratória (EDA)
- Visualização da dispersão entre idade e valor do seguro.
- Cálculo de correlação entre age e charges.
- Identificação de padrões e outliers.

---

### 3. Estimação do Modelo de Regressão Linear Simples
Modelo estimado:

```
charges = β0 + β1 * age
```

Principais resultados:
- β1 ≈ 257.72 → aumento médio no seguro por ano de idade.
- Intercepto ≈ 3165.88.
- R² ≈ 0.089 → idade explica ~8.9% da variação no valor do seguro.
- p-value extremamente baixo (4.89e-29) → relação estatisticamente significativa.

---

### 4. Avaliação do Modelo
- Teste F para significância global do modelo.
- Interpretação do R².
- Análise de resíduos.
- Considerações sobre limitações da regressão simples.

---

## Funções Auxiliares Desenvolvidas

### Verificação automática de significância
```python
def checar_significancia_modelo(modelo, alpha=0.05):
    p_valor = modelo.f_pvalue
    if p_valor < alpha:
        return f"O modelo é estatisticamente significativo (p-value = {p_valor:.4e})."
    else:
        return f"O modelo NÃO é estatisticamente significativo (p-value = {p_valor:.4e})."
```

---

## Principais Bibliotecas Utilizadas
pandas  
numpy  
statsmodels  
matplotlib  
seaborn  

---

## Contato
**E-mail:** thiago.a.v.souza@gmail.com  
**LinkedIn:** https://www.linkedin.com/in/thiagoavsouza/
