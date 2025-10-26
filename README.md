# CP5 - Modelo de Classificação com IA: Posições de Jogadores da NBA

[cite_start]Este projeto foi desenvolvido como parte da avaliação CP5 (Checkpoint) [cite: 1][cite_start], com o objetivo de construir um pipeline completo de ciência de dados para um problema de classificação supervisionada[cite: 3, 4].

## 1. Objetivo do Projeto

[cite_start]O objetivo deste projeto é desenvolver e avaliar um modelo de Machine Learning capaz de prever a **posição principal** de um jogador da NBA ('C', 'PF', 'PG', 'SF', 'SG') com base em suas estatísticas de desempenho em jogo da temporada regular[cite: 23, 24].

## 2. Dataset Utilizado

* [cite_start]**Fonte:** Kaggle [cite: 18]
* **Dataset:** 2021-2022 NBA Player Stats
* **Link:** `https://www.kaggle.com/datasets/vivovinco/nba-player-stats`
* **Descrição:** O dataset contém 812 registros (jogadores) e 30 colunas (estatísticas e informações) da temporada regular 2021-2022. Para este projeto, foram utilizadas 26 colunas de estatísticas como *features*.

## 3. Pipeline do Projeto

[cite_start]O projeto seguiu o pipeline obrigatório definido na atividade[cite: 20]:

1.  [cite_start]**Definição do Problema:** Definido como um problema de classificação multiclasse (5 classes).
2.  [cite_start]**Descrição do Dataset:** Dados carregados, explorados e validados (812 linhas, 30 colunas)[cite: 27].
3.  **Pré-processamento:**
    * Filtragem para manter apenas as 5 posições principais (removendo posições híbridas).
    * [cite_start]Encoding da variável-alvo (`Pos`) com `LabelEncoder`.
    * [cite_start]Padronização das *features* (estatísticas) com `StandardScaler`.
4.  **Modelagem:**
    * [cite_start]Os dados foram divididos em 70% treino e 30% teste.
    * [cite_start]Foram treinados 3 modelos: Regressão Logística [cite: 37][cite_start], Árvore de Decisão  [cite_start]e Random Forest.
5.  [cite_start]**Avaliação:** Os modelos foram avaliados usando Acurácia [cite: 47][cite_start], Relatório de Classificação (Precisão [cite: 48][cite_start], Recall [cite: 49][cite_start], F1-Score [cite: 50][cite_start]) e Matriz de Confusão.
6.  **Interpretação:** Foi realizada uma análise comparativa dos resultados.
7.  **Conclusão:** Foram documentados os aprendizados e possíveis melhorias futuras.

## 4. Resultados e Modelo Escolhido

### Comparativo dos Modelos

| Modelo | Acurácia | F1-Score (Weighted Avg) |
| :--- | :--- | :--- |
| **Random Forest** | **0.5649** | **0.56** |
| Regressão Logística | 0.5607 | 0.55 |
| Árvore de Decisão | 0.4184 | 0.41 |

### Modelo Final

[cite_start]O **Random Forest** foi escolhido como o modelo final[cite: 55]. Ele apresentou a maior acurácia (56,5%) e, por ser um modelo *ensemble*, é mais robusto e menos suscetível a overfitting do que a Árvore de Decisão simples.

## 5. Como Executar o Projeto

1.  Clone este repositório:
    ```bash
    git clone [URL-DO-SEU-REPOSITÓRIO]
    ```
2.  Abra o arquivo `Seu_Notebook.ipynb` no Google Colab.
3.  Quando solicitado na Célula 5, faça o upload do arquivo `2021-2022 NBA Player Stats - Regular.csv` (incluído neste repositório).
4.  Execute todas as células na ordem.
