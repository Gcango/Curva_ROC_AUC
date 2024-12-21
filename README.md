# Curva_ROC_AUC
 A Curva ROC mede a capacidade de um modelo de distinguir entre duas classes ao variar o limiar de decisão


Análise de Modelos de Classificação Usando a Curva ROC

Contexto do Problema

Este exercício se baseia em um problema de classificação binária com o objetivo de prever se um cliente irá ou não solicitar um empréstimo (churn). Para avaliar e comparar o desempenho de diferentes algoritmos de classificação, utilizamos a Curva ROC (Receiver Operating Characteristic) e suas respectivas áreas sob a curva (AUC).

Os algoritmos avaliados foram:

Árvore de Decisão

K-Nearest Neighbors (KNN)

Random Forest

Suporte a Vetores de Máquina (SVM)

O que é a Curva ROC?

A Curva ROC mede a capacidade de um modelo de distinguir entre duas classes ao variar o limiar de decisão. Ela é construída plotando:

Taxa de Verdadeiros Positivos (TPR) no eixo Y.

Taxa de Falsos Positivos (FPR) no eixo X.

A área sob a curva (AUC) fornece uma métrica quantitativa para comparar os modelos. Quanto mais próxima a curva estiver do canto superior esquerdo (TPR alto e FPR baixo), melhor o desempenho do modelo.

Desempenho dos Modelos

Abaixo estão as conclusões sobre cada modelo com base no gráfico da Curva ROC:

1. Árvore de Decisão (linha azul tracejada)

Desempenho:

A curva da Árvore de Decisão é a mais próxima do canto superior esquerdo do gráfico.

Isso indica uma alta taxa de verdadeiros positivos (TPR) e uma baixa taxa de falsos positivos (FPR).

Conclusão:

Este modelo apresenta o melhor desempenho geral neste problema.

É altamente recomendado, especialmente se o objetivo for minimizar erros do tipo falso positivo.

2. KNN (linha amarela tracejada)

Desempenho:

A curva do KNN é uma das menos acentuadas, aproximando-se da diagonal do gráfico, que representa o desempenho de um modelo aleatório.

Isso indica tanto TPR mais baixos quanto FPR mais altos.

Interpretação:

O KNN demonstra dificuldades em capturar padrões nos dados. Isso pode ser devido ao número inadequado de vizinhos ou à falta de complexidade do modelo.

Conclusão:

Este modelo não é adequado para este problema, a menos que sejam feitos ajustes significativos nos hiperparâmetros.

3. Random Forest (linha vermelha tracejada)

Desempenho:

A curva do Random Forest é intermediária, ficando entre a Árvore de Decisão e o KNN.

Indica um desempenho melhor que o KNN, mas inferior à Árvore de Decisão.

Conclusão:

Este modelo pode estar sofrendo com overfitting ou parametrização subótima (ex.: número de árvores ou profundidade).

Ajustar os hiperparâmetros pode torná-lo uma alternativa competitiva.

4. SVM (linha laranja tracejada)

Desempenho:

A curva da SVM está muito próxima da linha aleatória (diagonal), indicando um desempenho fraco.

Interpretação:

O modelo não consegue separar bem as classes. Isso pode ser devido a:

Dados não linearmente separáveis.

Escolha inadequada do kernel ou hiperparâmetros.

Conclusão:

A SVM não é recomendada neste cenário sem ajustes, como testar kernels não lineares (ex.: RBF, polinomial) ou realizar um ajuste fino.

Comparação Geral

Com base no gráfico da Curva ROC:

Modelo

Desempenho

Árvore de Decisão

Melhor desempenho geral

Random Forest

Competitivo, mas subótimo

KNN

Desempenho fraco

SVM

Desempenho próximo a aleatório

A Árvore de Decisão é o modelo mais confiável e indicado para este problema.

O Random Forest pode ser uma alternativa, mas requer ajustes.

Os modelos KNN e SVM apresentaram desempenho insuficiente, sugerindo que não são adequados neste contexto.

Próximos Passos

Cálculo da AUC:

Para quantificar melhor o desempenho, calcule a área sob a curva (AUC) para cada modelo.

Ajuste de Hiperparâmetros:

Melhorar o desempenho dos modelos Random Forest, KNN e SVM ajustando seus hiperparâmetros (ex.: número de árvores, número de vizinhos, ou tipo de kernel).

Validação Cruzada:

Use validação cruzada para garantir que os resultados são consistentes em diferentes subconjuntos de dados.

Explorar Métricas Complementares:

Avaliar métricas como Precision, Recall e F1-Score para entender outros aspectos do desempenho.

Conclusão Final:
A Curva ROC é uma ferramenta poderosa para comparar modelos de classificação. Neste exercício, ficou evidente que a Árvore de Decisão supera os outros modelos, sendo a melhor opção para resolver o problema de previsão de churn. Entretanto, o uso de Random Forest, com ajustes adequados, também pode ser uma solução robusta.

