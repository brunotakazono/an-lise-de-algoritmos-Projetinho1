# Análise de Algoritmos Projetinho

Neste projeto você vai comparar dois algoritmos de ordenação. Na comparação, você
vai apresentar um gráfico no qual o eixo horizontal representa o tamanho do vetor de
entrada e o eixo vertical representa o tempo de execução. Seu código deve escolher
aleatoriamente 10 tamanhos de vetores de forma que cada tamanho n seja tal que 10 ≤
n ≤ 10.000.
Para o tempo de execução de cada tamanho de entrada n, você deve executar os
algoritmos com m entradas de tamanho n de forma que m  ́e escolhido aleatoriamente
tal que 10 ≤ m ≤ 20. O m escolhido aleatoriamente deve ser o mesmo para todos os
tamanhos de entrada. Note que, para uma comparação mais justa, todos os algoritmos
devem ser executado com o mesmo conjunto de entradas. Além disso, para um vetor
de tamanho n, cada um dos seus elementos A[i], para 1 ≤ i ≤ n, deve ser um ponto
flutuante escolhido aleatoriamente tal que −2n ≤ A[i] ≤ 2n.



# *Merge Sort* chamando o *Insertion Sort* para entradas pequenas*

Apesar do *Merge Sort* executar em tempo Θ(nlgn) no pior caso e o *Insertion Sort*
rodarem tempo Θ(n²) no pior caso, os fatores constantes no *Insertion Sort* podem fazer com
que ele seja mais rápido na prática para entradas de tamanho pequeno. Dessa forma,
faz sentido usar o *Insertion Sort* dentro do *Merge Sort quando* as entradas se tornam
suficientemente pequenas. Considere uma modificação do *Merge Sort* na qual o caso
base usa o *Insertion Sort* para entradas de tamanho até 100.
