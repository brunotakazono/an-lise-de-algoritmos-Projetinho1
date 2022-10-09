# Análise de Algoritmos Projetinho1
   ## Desenvolvido por:
      Auriane do Carmo Barbosa          Matricula: 20202045050480
      Bruno Matsuyama Pereira Takazono  Matricula: 20202045050439


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



# *Merge-Sort* chamando o *Insertion-Sort* para entradas pequenas

Apesar do *Merge-Sort* executar em tempo Θ(nlgn) no pior caso e o *Insertion-Sort*
rodarem tempo Θ(n²) no pior caso, os fatores constantes no *Insertion Sort* podem fazer com
que ele seja mais rápido na prática para entradas de tamanho pequeno. Dessa forma,
faz sentido usar o *Insertion-Sort* dentro do *Merge-Sort quando* as entradas se tornam
suficientemente pequenas. Considere uma modificação do *Merge-Sort* na qual o caso
base usa o *Insertion-Sort* para entradas de tamanho até 100.


Para entradas de tamanho k, o *Insert-Sort* é executado em Θ(k²) tempo do pior caso.
Então, o pior momento para classificar as sublistas n/k cada uma de comprimento k logo
n/k.Θ(k²) = Θ(nk)
Portanto, temos n elementos divididos em sublistas n/k classificadas cada uma de
comprimento k. Para mesclar essas sublistas n/k classificadas de comprimento n, tem-se
que pegar 2 sublistas de cada vez e continuar a mesclá-las que resultará em lg(n/k). E em
cada passo, vai-se essencialmente comparar os elementos. Assim, todo o processo será
executado em Θ(n.lg(n/k)). Portanto para que o algoritmo modificado tenha o mesmo
tempo de execução assintótico que a classificação de mesclam padrão, Θ(n.k+n.lg(n/k))
deve ser igual a Θ(n.lg(n)). Logo para satisfazer essa condição, k não pode crescer mais
rápido do que lg(n) assintoticamente, se isso acontecer, então por causa de n k termo, o
algoritmo será executado em um termo assintótico pior que Θ(n.lg(n)). Então supondo
que, k = Θ(lg(n)) e vamos analisar se pode-se atender ao critérios Logo temos:

    Θ(n.k + n.ln.(n/k)) = Θ(n.k+n.lg.(n)-n.lg.(lg(n)))
                        = Θ(2.n.lg(n) - n.lg(lg(n)))
                        = Θ(n.lg(n))
                        
Portanto, lg(lg(n)) é muito pequeno em relação a lg(n) para valores suficientemente maiores
de n.
OBS: Para determinar um valor prático para k ele deve ser o maior tamanho de entrada
onde o *Insert-Sort* é executado mais rapidamente do que o *Merge-Sort*.

Lembrando que:
O custo final de um algoritmo pode estar relacionado a diversos fatores: 
- Tempo de execução 
- Utilização de memória principal 
- Utilização de disco 
- Consumo de energia, etc...
 
Neste caso não existe um número fixo de operações! 
Um algoritmo pode rodar mais rápido para certos conjunto de dados do que para outros.
