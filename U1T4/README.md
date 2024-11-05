# Trabalho 4 - UNIDADE 1

## Análise de Rede do Bairro da Lagoa Nova - Natal/RN com OSMnx 🛜

Este projeto tem como objetivo explorar as capacidades da biblioteca OSMnx para analisar a rede viária do bairro da Lagoa Nova, em Natal/RN. Através da implementação de diferentes métricas de rede, busca-se responder a perguntas relevantes sobre a estrutura e o funcionamento da infraestrutura viária local.

## Métricas Utilizadas

As seguintes métricas foram escolhidas para a análise da rede:

*Average Shortest Path Length*: Representa a distância média entre todos os pares de nós na rede.

*Diameter of Network*: Corresponde ao maior caminho mais curto entre qualquer par de nós na rede.

*Number Connected Components*: Contabiliza o número total de componentes conectados.


## Perguntas e Resultados 🙋🏽‍♂️

- Qual é a eficiência de comunicação na rede?

    - Analisando o Average Shortest Path Length, podemos determinar quão rapidamente os nós podem se comunicar entre si. Um valor menor indica uma comunicação mais eficiente.

- Quão coesa é a rede?

    - O Diameter of Network nos informa qual é a maior distância entre quaisquer dois nós na rede. Um diâmetro menor sugere que a rede é mais coesa, enquanto um diâmetro maior pode indicar que a rede é dispersa.

- Quantas sub-redes independentes existem?

    - O número de connected components revela quantas partes distintas existem na rede que não estão interconectadas. Isso pode indicar a fragmentação da rede ou a presença de grupos isolados.

## Implementação 👩🏽‍💻

O código completo da análise está disponível no notebook [U1T4.ipynb]. O notebook utiliza a biblioteca OSMnx para obter os dados da rede viária e realizar os cálculos das métricas.

### Imagens da rede do bairro de Lagoa Nova:
<img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T4/Lagoa_Nova.png"  width="600" height="700"/>

### Imagens das ruas principais do bairro:
<img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T4/Lagoa_Nova_Ruas_Principais.png" width="600" height="700"/>

### Histograma da rede:
<img src="https://github.com/AnelmaSilva/Algortimo-Estrutura-de-Dados-II/blob/main/U1T4/Histograma_Lagoa_Nova.png" width="600" height="700"/>

## Vídeo Explicativo

- Um vídeo detalhado explicando o processo de análise e os resultados obtidos está disponível em [link do vídeo].

## Conclusão

- A análise da rede viária do bairro da Lagoa Nova utilizando as métricas do OSMnx permitiu obter insights valiosos sobre a estrutura e o funcionamento da infraestrutura viária local. Os resultados obtidos podem ser utilizados para diversas aplicações, como planejamento urbano, análise de tráfego e desenvolvimento de aplicativos de navegação.
