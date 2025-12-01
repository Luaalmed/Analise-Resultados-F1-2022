# 🏎️ F1 2022 Data Analysis - Métodos Numéricos

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Concluído-success)
![Subject](https://img.shields.io/badge/Disciplina-Métodos%20Numéricos-orange)

## 📄 Sobre o Projeto

Este projeto foi desenvolvido como parte da disciplina de **Métodos Numéricos**, com o objetivo de aplicar conceitos estatísticos e matemáticos em um cenário do mundo real. Utilizamos o dataset da temporada de **Fórmula 1 de 2022** para investigar quais variáveis (Pole Positions, Voltas Mais Rápidas, Pódios, etc.) influenciam diretamente nos resultados finais (Vitórias e Posição no Campeonato).

Através de **Regressão Linear Simples** e **Múltipla (OLS)**, buscamos responder perguntas como: *"Largada na Pole garante vitória?"* ou *"Abandonos (DNFs) destroem o campeonato de um piloto?"*.

## 📊 Principais Análises e Insights

O estudo baseou-se no cálculo do **Coeficiente de Pearson (r)** e **Determinação (R²)** para validar as hipóteses.

### 1. Correlações Fortes
* **Pontos vs. Pódios:** Correlação quase perfeita (**r = 0.975**). Mostra que 95,1% da variação de pódios é explicada pelos pontos. Consistência é tudo.
* **Pódios vs. Posição Final:** Correlação negativa forte (**r = -0.779**), indicando que quanto mais pódios, menor (melhor) é a posição final no ranking (1º, 2º, etc.).
* **Pole Positions vs. Vitórias:** Correlação positiva forte (**r = 0.717**). Largar na frente explica cerca de 51,5% das vitórias, destacando a importância da classificação.

### 2. A Surpresa: Abandonos (DNFs)
* **DNFs vs. Posição Final:** Ao contrário do senso comum, **não houve correlação linear** significativa (**r = 0.046**). O número de abandonos, isoladamente, não determinou a posição final dos pilotos nesta temporada.

### 3. Modelagem Preditiva (Regressão Múltipla)
Utilizamos o método dos Mínimos Quadrados Ordinários (OLS) para criar um modelo preditivo de vitórias.
* **Modelo Final:** `Wins ~ Pole Positions + Podiums`
* **Resultado:** O modelo explicou aproximadamente **60.2% (R²)** da variância das vitórias, sendo estatisticamente mais robusto após a remoção de variáveis com alta colinearidade ou baixo impacto (p-value alto).

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas:**
    * `Pandas` (Manipulação de dados)
    * `Matplotlib / Seaborn` (Visualização gráfica)
    * `Statsmodels` (Modelagem estatística e OLS)
    * `NumPy` (Cálculos numéricos)

## 🚀 Como Executar

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repo.git](https://github.com/seu-usuario/nome-do-repo.git)
