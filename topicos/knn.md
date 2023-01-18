# K Nearest Neighbors (KNN)

O **KNN** é um **algoritmo de aprendizado supervisionado**, que pode ser utilizado para cases de **classificação** ou 
**regressão**, no qual temos um **parâmetro** chamado 'K', número de instâncias (vizinhos) que o algoritmo usa 
para fazer sua previsão, normalmente esse valor é um número ímpar (em classificação, k ímpar 
garante que não haverá empate entre classes).

O KNN é um exemplo de **algoritmo não parâmetrico**, ou seja, que não assume considerações antecipadamente sobre os dados, tal como a LinearRegression faz de que os dados podem ser modelados por uma função linear (considerações fortes podem resultar em resultados ruins, porque a relação entre um X e y pode não ser linear).

<p align="center">
  <img src="https://vitalflux.com/wp-content/uploads/2022/08/k-nearest-neighbors-algorithm.png" width=550>
</p>

No exemplo acima, a nova instância (representada pelo ?) e para k = 3, a nova instância será classificada pela classe representada pelo símbolo $\triangle$ (triângulo). Se k = 1, então o objeto é simplesmente atribuído à classe daquele único vizinho mais próximo.

## Para o que pode ser usado

1. Em problemas de classificação do k vizinho mais próximo, a saída é uma associação de classe. Um objeto é classificado por maioria de votos de seus vizinhos, sendo o objeto atribuído à classe mais comum entre seus k vizinhos mais próximos (k é um inteiro positivo, geralmente pequeno).\newline
    
    Se k = 1, então o objeto é simplesmente atribuído à classe daquele único vizinho mais próximo.\newline
    
    Para k = 3, a nova instância será classificada pela classe representada pelo símbolo $\triangle$ (triângulo).

2. Na regressão dos K vizinhos mais próximos, a saída é o valor da propriedade do objeto. Este valor é a média dos valores de seus k vizinhos mais próximos. A equação abaixo representa o problema:
    
\end{itemize}

## Etapas do algoritmo

- Calcular distância: o algoritmo K-NN calcula a distância entre um novo ponto de dados e todos os pontos de dados de treinamento. Isso é feito usando a métrica de distância selecionada (seja Euclidiana, Manhattan, Markowski, Hamming).
- Encontrar vizinhos mais próximos: Depois que as distâncias são calculadas, K vizinhos mais próximos são determinados com base em um valor definido de K.
- Prever o rótulo da classe de destino: depois de descobrir os K vizinhos mais próximos, podemos prever o rótulo da classe de destino para um novo ponto de dados obtendo a maioria dos votos deseus K vizinhos (no caso de classificação) ou obtendo a média de seus K vizinhos (no caso de regressão).

\subsection{Importância do parâmetro k}

<p align="center">
  <img src="https://vitalflux.com/wp-content/uploads/2020/09/Screenshot-2020-09-22-at-2.34.57-PM.png" width=550>
</p>

Na imagem acima:

- Se K = 3, a classe do ponto de dados (verde) é designada como o triângulo laranja (2 votos a 1 a favor do triângulo 
- Se K = 5, a classe do ponto de dados é atribuída como quadrado azul (3 votos a 2 votos a favor do quadrado azul).
\end{itemize}

<span style="color:red">*Baixos valores de k (como k=1 ou k-2), podem ser ruidos e muito sujeitos aos efeitos de outliers.</span>.

Uma boa sugestão para escolher k é usar:

$k = log(N)$

Sendo N o número de instâncias do conjunto de dados.

## Materiais
- Introduction to Statistical Learning - Cap 

### Videos

- [StatQuest](https://www.youtube.com/watch?v=HVXime0nQeI)
  - Apresenta KNN usando um case de tumores em diferentes tipos celulares.
  - Demonstra a importância do parâmetro k, para a resposta final do algoritmo.
 - [Algoritmo KNN e Avaliações de Modelos Preditivos - UNIVESP TV](https://www.youtube.com/watch?v=4Dpf76AB9Js)
    - Definição do algoritmo
    - Funcionamento do algoritmo
    - Exemplo usando o Iris Dataset
      - Treinando
      - Testando
      - Avaliando com o score do scikit-learn (acurácia).
