# TRABALHO 3 - UNIDADE 2 💻

- Aluna : Anelma Silva da Costa
- Disciplina: Algortimo e Estrutura de Dados II
- Professor: Ivanovitch
- Engenharia de Computação - DCA (Departamento de Computação e Automação)
  
# Algoritmos Clássicos (Dijkstra e Kruskal) 💻💾📌

- O objetivo desta tarefa é analisar os algoritmos clássicos de Dijkstra e Kruskal. Antes de entrar nos detalhes, é importante compreender brevemente o funcionamento de cada um desses algoritmos.

**Algoritmo de Dijkstra**

- O algoritmo de Dijkstra é amplamente utilizado em ciência da computação para encontrar o caminho mais curto entre dois vértices em um grafo ponderado. Um grafo, nesse contexto, é uma estrutura de dados composta por um conjunto de nós (vértices) conectados por arestas, nas quais cada aresta possui um peso associado. Esse peso pode representar, por exemplo, a distância entre dois pontos em um mapa.

- O algoritmo tem diversas aplicações, como em redes de computadores, sistemas de navegação, planejamento de rotas, entre outras. Suas principais características incluem o uso de grafos ponderados, a determinação do caminho mais curto a partir de um vértice de origem para todos os outros vértices do grafo e a construção de árvores de caminhos mínimos.

- Quanto à sua complexidade, ela depende da estrutura de dados utilizada para representar o grafo e da implementação adotada. No caso mais geral, utilizando uma matriz de adjacência, a complexidade é O(V²), onde V é o número de vértices. No entanto, ao utilizar uma fila de prioridade, essa complexidade pode ser reduzida para O(E log V), onde E representa o número de arestas.

**Algoritmo de Kruskal**

- O algoritmo de Kruskal é um algoritmo clássico em teoria dos grafos, projetado para encontrar a árvore geradora mínima (MST) de um grafo conexo e ponderado. Uma MST é uma subgrafo que conecta todos os vértices do grafo original, usando apenas um subconjunto das arestas originais, e que possui o menor peso total possível (a soma dos pesos de todas as arestas).

- O algoritmo tem diversas aplicações em áreas como redes de comunicação, circuitos elétricos, infraestruturas, entre outras. Suas principais características incluem a ordenação das arestas, a construção gradual da solução, o uso de conjuntos disjuntos e a abordagem gananciosa (greedy), na qual o algoritmo toma decisões locais ótimas a cada passo, com a esperança de alcançar uma solução globalmente ótima.

- A complexidade do algoritmo de Kruskal depende da estrutura de dados utilizada para representar os conjuntos disjuntos e da maneira como as arestas são ordenadas. 

  - **Ordenação**: A ordenação das arestas é geralmente realizada com o uso de algoritmos eficientes, como quicksort ou mergesort, com complexidade O(E log E), onde E é o número de arestas.
  - **Conjuntos disjuntos**: A operação de união dos conjuntos disjuntos pode ser implementada por meio da estrutura de dados union-find, que oferece uma complexidade amortizada quase linear para uma sequência de N operações de união e busca.

# PARTE 1 📄

- Neste trabalho, busca-se aprofundar a análise de algoritmos de roteamento em grafos, com foco no algoritmo de Dijkstra. Utilizando a biblioteca OSMnx, serão selecionados 10 pares de pontos de interesse (PoI) na cidade do Natal-RN. Para cada par, o algoritmo de Dijkstra será aplicado, determinando o caminho mais curto entre os pontos.

- A implementação será realizada tanto utilizando a biblioteca NetworkX quanto através da estrutura de dados min-heap. As soluções obtidas serão comparadas visualmente no ambiente OSMnx, permitindo uma análise qualitativa dos resultados

- Os pontos de interesse escolhidos foram:
    - Ponta Negra
    - Praça 7 de Setembro
    - Shopping Midway Mall
    - Estádio Arena das Dunas
    - Parque da Cidade
    - UFRN
    - Norte Shopping
    - Praia do Forte
    - Hotel Majestic
    - Centro de Turismo

- Para avaliar o desempenho computacional das implementações do algoritmo de Dijkstra utilizando NetworkX e min-heap, foi introduzida uma biblioteca de medição de tempo. Os resultados obtidos para os 10 pares de pontos de interesse (POIs) indicam que a implementação do NetworkX apresentou um tempo de execução significativamente menor, como mostrado na figura abaixo.
  figura1
- Essa superioridade do NetworkX pode ser atribuída à sua otimização para lidar com grafos de grande escala, como os encontrados em ambientes urbanos. Ao contrário da implementação manual utilizando min-heap, que apresenta maior overhead, o NetworkX é projetado especificamente para realizar operações em grafos de forma eficiente.

- A próxima figura apresenta os grafos gerados com os caminhos mais curtos encontrados por ambos os algoritmos para um dos pares de POIs. É possível observar que, apesar de ambos os algoritmos encontrarem o caminho correto, a visualização pode auxiliar na comparação qualitativa das soluções, evidenciando, por exemplo, diferenças na quantidade de vértices visitados ou no comprimento total do caminho.
  figura2
