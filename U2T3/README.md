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

- De inicio, busca-se aprofundar a análise de algoritmos de roteamento em grafos, com foco no algoritmo de Dijkstra. Utilizando a biblioteca OSMnx, serão selecionados 10 pares de pontos de interesse (PoI) na cidade do Natal-RN. Para cada par, o algoritmo de Dijkstra será aplicado, determinando o caminho mais curto entre os pontos.

- A implementação será realizada tanto utilizando a biblioteca NetworkX quanto através da estrutura de dados min-heap. As soluções obtidas serão comparadas visualmente no ambiente OSMnx, permitindo uma análise qualitativa dos resultados.
  
- A NetworkX e Min Heap foram definidas como mostradas nas imagens abaixo
  - NetworkX:
    - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/NetworkX.png"  width="400" height="200"/>
  - Min Heap:
    - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Min_Heap.png"  width="400" height="400"/>
    
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

- Para avaliar o desempenho computacional das implementações do algoritmo de Dijkstra utilizando NetworkX e min-heap, foi introduzida uma biblioteca de medição de tempo. Os resultados obtidos para os 10 pares de pontos de interesse (POIs) indicam que a implementação do NetworkX apresentou um tempo de execução significativamente menor.

- A imagem que representa a comparação entre os algoritmos, mostra como foi desenvolvida a lógica com a biblioteca time.
- A figura com o resultados evidencia a diferença do NetworkX para com o Min Heap.
  - Comparação:
    - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Comparação_Dijkstra.png"  width="400" height="400"/>
  - Resultado do desempenho:
    -  <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Time_Algoritmos.png"  width="400" height="400"/>

- A próxima figura apresenta os grafos gerados com os caminhos mais curtos encontrados por ambos os algoritmos para um dos pares de POIs. É possível observar que, apesar de ambos os algoritmos encontrarem o caminho correto, a visualização pode auxiliar na comparação qualitativa das soluções, evidenciando, por exemplo, diferenças na quantidade de vértices visitados ou no comprimento total do caminho. Para observar às 10 imagens dos POIs por completo basta acessar o link que direciona para a pasta de imagens logo abaixo da figura.
  -  <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Grafo_Dijsktra.png"  width="400" height="400"/>
  - Link da pasta com todas as imagens 📂: https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/tree/main/U2T3/Imagens_Dijkstra
    
- Com base nos resultados obtidos, podemos concluir que a biblioteca NetworkX é uma ferramenta muito mais eficiente para encontrar o caminho mais curto em grafos de grande porte, como o grafo da cidade de Natal, quando comparada com uma implementação manual utilizando min-heap. As otimizações presentes no NetworkX permitem que ele execute o algoritmo de Dijkstra de forma significativamente mais rápida, tornando-o uma escolha ideal para aplicações que exigem alta performance em problemas de roteamento.

- Neste link você pode encontrar o código completo desenvolvido para a tarefa 🔗👩🏾‍💻 : https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Dijkstra.ipynb

# PARTE 2 📄

- Na segunda parte deste trabalho, propõe-se a aplicação do algoritmo de Kruskal em um problema prático: Otimização de rotas turísticas. O objetivo é encontrar a árvore geradora mínima (MST) que conecte os principais pontos turísticos de uma cidade, minimizando a distância total percorrida.

- Para tanto, foram selecionados como pontos de interesse (POIs) praias e parques da cidade do Natal. A partir do grafo da cidade, construiu-se um subgrafo contendo apenas os POIs e as arestas que os conectam. Em seguida, o algoritmo de Kruskal foi aplicado a este subgrafo para determinar a MST.

- A figura a seguir mostra o trecho de código responsável por encontrar os POIs:
   -  <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Trecho_POIs_Kruskal.PNG"  width="400" height="400"/>
- A figura abaixo apresenta a MST resultante, visualizando a rota turística otimizada que conecta os POIs selecionados. A visualização permite identificar a melhor forma de conectar os pontos turísticos, minimizando a distância percorrida e otimizando o tempo de visitação.
  -  <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Kruskal_Resultado.png"  width="400" height="400"/>

- A MST encontrada pelo algoritmo de Kruskal para os pontos turísticos de Natal representa a rota mais curta e eficiente para visitar todos os locais selecionados, considerando a infraestrutura viária da cidade. Este tipo de resposta utlizando o algoritmo pode ser usado para planejamento de viagens otimizados, realização de uma análise da infraestrutura turística em outras.

- Em outras palavras, a MST é uma ferramenta poderosa para otimizar a experiência turística em Natal e para auxiliar no planejamento urbano da cidade.

- Neste link você pode encontrar o código completo desenvolvido para a tarefa 🔗👩🏾‍💻 : https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U2T3/Kruskal.ipynb
- 
- Neste link você pode encontrar o vídeo desenvolvido para a tarefa 🔗👩🏾‍💻 : https://youtu.be/WCXYUXH1-qA
