# K Nearest Neighbors (KNN)

O **KNN** é um **algoritmo de aprendizado supervisionado**, que pode ser utilizado para cases de **classificação** ou 
**regressão**, no qual temos um **parâmetro** chamado 'K', número de instâncias que o algoritmo usa 
para fazer sua previsão, normalmente esse valor é um número ímpar (em classificação, k ímpar 
garante que não haverá empate entre classes).

<p align="center">
  <img src="https://vitalflux.com/wp-content/uploads/2022/08/k-nearest-neighbors-algorithm.png" width=550>
</p>

## Etapas do algoritmo

- Calcular distância: o algoritmo K-NN calcula a distância entre um novo ponto de dados e todos os pontos de dados de treinamento. Isso é feito usando a métrica de distância selecionada.
- Encontrar vizinhos mais próximos: Depois que as distâncias são calculadas, K vizinhos mais próximos são determinados com base em um valor definido de K.
- Prever o rótulo da classe de destino: depois de descobrir os K vizinhos mais próximos, podemos prever o rótulo da classe de destino para um novo ponto de dados obtendo a maioria dos votos deseus K vizinhos (no caso de classificação) ou obtendo a média de seus K vizinhos (no caso de regressão).

## Materiais

### Videos

- [StatQuest](https://www.youtube.com/watch?v=HVXime0nQeI)
  - Apresenta KNN usando um case de tumores em diferentes tipos celulares.
  - Demonstra a importância do parâmetro k, para a resposta final do algoritmo.
