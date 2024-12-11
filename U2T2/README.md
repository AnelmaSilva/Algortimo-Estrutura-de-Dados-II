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
        - INSERIR FIGURA DE EXEMPLO.
          
- O código de criação para uma BST : https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T2/BST.ipynb

## Explicação dos Algoritmos

- solver_closest: Este algoritmo busca o valor mais próximo de um número de entrada em uma árvore binária.

- solver_kth_largest: Este algoritmo encontra os três maiores valores em uma árvore binária.

Cada algoritmo foi projetado para ser eficiente, e o desempenho foi medido utilizando a biblioteca time para capturar o tempo de execução.

## Resultados

Após a execução, serão gerados gráficos que mostram a relação entre o tamanho do vetor e o tempo médio de execução, com intervalos de confiança como barras de erro.

## Análise

No vídeo anexo (com duração de até 5 minutos), explicamos detalhadamente os resultados obtidos a partir dos gráficos e discutimos o desempenho dos algoritmos para diferentes tamanhos de entrada.
