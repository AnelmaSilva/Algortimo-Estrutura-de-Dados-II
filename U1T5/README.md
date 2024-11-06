# Avaliação da Mobilidade no Entorno da UFRN (Natal-RN)

## Descrição
- Este projeto tem como objetivo analisar a mobilidade no entorno da Universidade Federal do Rio Grande do Norte (UFRN), localizada em Natal-RN, com foco em sugerir locais ideais para a instalação de dock-stations de compartilhamento de bicicletas. A análise será realizada utilizando conceitos de redes complexas, centralidade, e análise estatística dos graus dos nós da rede.

# Questões principais a serem abordadas:
- Quais bairros analisar?
- Onde colocar dock-stations de compartilhamento de bicicletas?
- Como avaliar a mobilidade sem considerar paradas de ônibus?
O trabalho utilizará métricas de centralidade para destacar as áreas mais conectadas da rede urbana e determinar os pontos de interesse para a instalação de bike-sharing.

## Objetivos
- Aplicar métricas de centralidade para identificar pontos de alta conectividade na região.
- Analisar a CDF (Função de Distribuição Cumulativa) e a PDF (Função de Densidade de Probabilidade) dos graus dos nós da rede para entender as características da conectividade entre os bairros.
- Realizar uma análise multivariada das métricas de centralidade para entender como diferentes critérios (como grau, betweenness, closeness) interagem e influenciam a rede.
- Identificar o core e o shell da rede para determinar os grupos de bairros mais integrados e aqueles mais periféricos.
  
## Metodologia
- A solução será baseada em uma abordagem de redes complexas, utilizando os seguintes passos principais:

### Criação do grafo de bairros:

- Consideração de bairros ao redor da UFRN, considerando sua proximidade e conectividade através de vias principais.
Construção de um grafo onde os bairros serão os nós, e as estradas/ruas entre eles serão as arestas.

### Cálculo das métricas de centralidade:

- Grau: Número de conexões diretas de cada bairro com outros bairros.
- Centralidade de intermediária (betweenness): Determina o quão central é um bairro em termos de seu papel como intermediário nas rotas de outros bairros.
- Centralidade de proximidade (closeness): Mede o quão próximo um bairro está de todos os outros bairros da rede.
- Centralidade de autovalor (eigenvector): Avalia a influência de um bairro na rede com base na conectividade dos seus vizinhos.
  
## Análise das distribuições dos graus

- Análise da CDF e PDF dos graus dos nós para entender o comportamento da rede (se ela segue uma distribuição de tipo "lei de potência", que é comum em redes complexas).
Análise multivariada das métricas de centralidade:

- Aplicação de técnicas de análise multivariada (como PCA ou análise de correlação) para observar como diferentes métricas de centralidade estão relacionadas e como elas podem ser usadas para identificar zonas de alta mobilidade.
  
## Identificação do core e shell da rede

- Através da análise de centralidade, será possível determinar quais bairros formam o "core" (núcleo central) da rede e quais fazem parte do "shell" (periferia), indicando os bairros mais e menos conectados.
Definição dos locais para dock-stations:

A partir das métricas de centralidade e da análise multivariada, sugerir os bairros ou interseções de alta centralidade como locais ideais para a instalação de dock-stations de bicicletas.

## Ferramentas e Técnicas Utilizadas
- Python: Linguagem de programação principal, utilizando bibliotecas como networkx para a criação e análise de grafos, matplotlib e seaborn para visualizações gráficas.
- Análise Estatística: Cálculos da CDF e PDF dos graus, análise de centralidade e visualização das distribuições.
- Análise Multivariada: PCA (Análise de Componentes Principais) para redução de dimensionalidade e análise de correlação entre diferentes métricas de centralidade.
  
## Resultados 
- - Grafo do bairro de Candelária
  - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T5/Candelaria.png"  width="600" height="700"/>
- - Grafo de Candelária com ruas para bike
  - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T5/Candelaria_bike.png"  width="600" height="700"/>
- - Grafo da métrica Degree e Closeness
  - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T5/Degree_Candelaria.png"  width="600" height="700"/>
  - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T5/Closeness_Candelria.png"  width="600" height="700"/>
  
- - Análise Multivariada
  - <img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T5/AnaliseMetricas_Candelaria.png"  width="800" height="900"/>
## Conclusão
A análise de redes complexas aplicada à mobilidade urbana no entorno da UFRN permitirá uma avaliação mais detalhada da conectividade entre os bairros e ajudará na escolha dos locais mais estratégicos para a implementação de dock-stations de bicicletas. A utilização das métricas de centralidade, juntamente com a análise das distribuições de graus e a análise multivariada, proporcionará uma solução robusta e fundamentada para melhorar a mobilidade sustentável em Natal.
