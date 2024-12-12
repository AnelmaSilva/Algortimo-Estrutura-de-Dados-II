# TRABALHO 2 - UNIDADE 2 💻

- Aluna : Anelma Silva da Costa
- Disciplina: Algortimo e Estrutura de Dados II
- Professor: Ivanovitch
- Engenharia de Computação - DCA (Departamento de Computação e Automação)
  
# Desafio de Algoritmos com Árvores 🌳💻🤯

Este repositório contém um trabalho acadêmico focado em avaliar o desempenho de dois algoritmos, `solver_closest` e `solver_kth_largest` utlizando árvores de busca binária e considerando diversas entradas aleatórias e reproduzíveis. A ideia é variar o tamanho do vetor de entrada até um valor N grande, com o intuito de observar o impacto no tempo de execução, usando árvores para resolver dois desafios distintos:

- Encontrar o valor mais próximo de um determinado número de entrada.
- Detectar os três maiores valores em um conjunto de dados.

## Árvore de Busca Binária 🌳🔍0️⃣1️⃣

- A Árvore de Busca Binária (BST - Binary Search Tree) é uma estrutura de dados hierárquica em que cada nó possui, no máximo, dois filhos, conhecidos como filho esquerdo e filho direito. A principal característica dessa árvore é a propriedade de ordenação:

  - Subárvore esquerda: Todos os valores dos nós na subárvore esquerda de um nó são menores que o valor do nó.
  - Subárvore direita: Todos os valores dos nós na subárvore direita de um nó são maiores que o valor do nó.
    
- Essa organização permite realizar operações como busca, inserção e remoção de forma eficiente, com complexidade média de O(log n), onde n é o número de nós na árvore. No entanto, no pior caso (quando a árvore está desbalanceada e se torna uma lista encadeada), a complexidade pode ser O(n).
    - Exemplo de uma BST:
        - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T2/BST.png"  width="400" height="400"/>
          
- O código de criação para uma BST : https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T2/BST.ipynb

## Explicação dos Algoritmos

- Solver Closest: Este algoritmo busca o valor mais próximo de um número de entrada em uma árvore binária.
  - Para ilustrar o funcionamento do algoritmo, considere o seguinte exemplo: Suponha que um usuário deseje encontrar o valor mais próximo de 48 em uma árvore de busca binária (BST). O algoritmo inicia a busca na raiz, que, neste caso, é o número 40. Sabendo-se que, devido às propriedades da BST, todos os valores à esquerda de 40 são menores que ele, e como o valor desejado é maior que a raiz, o algoritmo segue para o lado direito da árvore, como ilustrado na figura abaixo.
        - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T2/BST_RIGHT40.png"  width="400" height="400"/>

  - No próximo nó, ele encontra o valor 60. Assim, o algoritmo calcula que a diferença entre 60 e o valor desejado (48) é de 12, e conclui que o número mais próximo até o momento ainda é 40. Como mencionado anteriormente, ao seguir para a direita, os valores encontrados serão maiores que 60, resultando em uma diferença ainda maior. Portanto, o algoritmo começa a percorrer o lado esquerdo, com o objetivo de encontrar uma diferença menor que 12. Seguindo esse raciocínio, o algoritmo percebe que o valor 50 possui a menor diferença em relação ao valor fornecido pelo usuário, sendo, assim, o número mais próximo dentro da árvore.
        - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T2/BST_CORRECTVALUE.png"  width="400" height="400"/>

- Solver Kth Largest: Este algoritmo encontra os três maiores valores em uma árvore binária.
    - Neste algoritmo o funcionamento é diferente, o objetivo aqui é encontrar os três maiores valores em uma árvore, assim vamos usar um estrategia bastante utilizada em BST que é a busca Em Ordem.
    - A busca em ordem (ou in-order search) em uma Árvore de Busca Binária (BST) é um processo que percorre a árvore de uma forma específica. A ordem para percorrer é a seguinte:
      - Subárvore esquerda: Primeiro, explora-se a subárvore à esquerda.
      - Nó atual: Depois, visita-se o nó atual.
      - Subárvore direita: Finalmente, explora-se a subárvore à direita.
        
    - Realizando esse procedimento de busca encontramos os três maiores valores da BST. Mas na computação a busca por otimização é constante, pensando nisso, foi notado que é bem mais eficiente se realizamos está busca de forma reversa, pois a assim os k primeiros números já serão os maiores da BST 🙀💡.

Cada algoritmo foi projetado para ser eficiente, e o desempenho foi medido utilizando a biblioteca time para capturar o tempo de execução.

## Resultados

Após a execução, serão gerados gráficos que mostram a relação entre o tamanho do vetor e o tempo médio de execução, com intervalos de confiança como barras de erro.

- Foram realizados alguns testes variando o valor de entrada N, assim como os steeps e o tamanho das execuções. Nas imagens seguintes é possível notar a diferenças entre os algoritmos de acordo com o tamanho da entrada. Quando iniciamos em um valor pequeno, praticamento não faz diferença, na escolha do algoritmo, o que não ocorre para valores bem alto, já que o (NOME DO ALGORITMO) bem um desempenho melhor que o (NOME DO ALGORITMO).

## Análise

No vídeo anexo (com duração de até 5 minutos), explicamos detalhadamente os resultados obtidos a partir dos gráficos e discutimos o desempenho dos algoritmos para diferentes tamanhos de entrada.
