📊 Rede de Vulnerabilidades Socioeconômicas nas Regiões Metropolitanas do Brasil
📌 Descrição do Projeto

Este projeto aplica a metodologia de Análise de Redes Sociais (ARS) para investigar a estrutura relacional das vulnerabilidades socioeconômicas nas regiões metropolitanas do Brasil.

A partir de microdados da PNAD Contínua (2013–2023), foi construída uma rede de coocorrência entre dimensões econômicas, demográficas e territoriais, permitindo examinar como diferentes vulnerabilidades se articulam estruturalmente.

O estudo complementa abordagens tradicionais ao modelar desigualdades como um sistema relacional integrado.

🎯 Objetivo

Investigar:

* Como vulnerabilidades econômicas, educacionais, raciais e territoriais se organizam estruturalmente;

* O grau de integração entre essas dimensões;

* Quais variáveis ocupam posições centrais na rede;

* A existência (ou ausência) de comunidades estruturais distintas nas regiões metropolitanas.

🧠 Metodologia
🔹 Linguagens Utilizadas

* R (pipeline analítico e modelagem de rede)

* SQL (extração dos microdados via BigQuery)

🔹 Coleta de Dados

Os dados foram extraídos da PNAD Contínua utilizando consultas SQL no BigQuery (Base dos Dados), via pacote bigrquery.

Foram selecionadas observações referentes às regiões metropolitanas brasileiras no período de 2013 a 2023.

🔹 Bibliotecas Utilizadas

* bigrquery — acesso ao BigQuery

* dplyr, tidyr, stringr — manipulação de dados

* Matrix — construção de matriz esparsa

* igraph — modelagem da rede

* ggraph, ggplot2 — visualização

🏗 Construção da Rede

A rede foi construída a partir de:

* Matriz binária indivíduo × vulnerabilidade

* Produto matricial X'X para gerar matriz de coocorrência

* Grafo não direcionado e ponderado

🔹 Nós representam:

* renda_pc_baixa

* baixa_escolaridade

* analfabeto

* mulher

* raca_preta

* raca_parda

* eh_capital

* vulneravel_idoso

🔹 Arestas representam:

Número de indivíduos que apresentam simultaneamente duas vulnerabilidades.

📈 Principais Resultados

* Rede altamente densa (≈0,96);

* Um único componente conectado;

* Modularidade baixa (~0,02);

* Ausência de clusters bem delimitados.

🔹 Centralidade

* eh_capital apresentou maior força e maior centralidade de autovetor;

* renda_pc_baixa atua como eixo econômico estruturante;

* raca_parda e mulher ocupam posições centrais intermediárias;

* analfabeto aparece em posição relativamente periférica.

Os resultados indicam forte integração entre desigualdades territoriais, econômicas e raciais nas regiões metropolitanas.

📊 Visualizações

O projeto inclui:

* Rede de Coocorrência das Vulnerabilidades (layout Fruchterman-Reingold);

* Visualização de comunidades via algoritmo Louvain.

📌 Conclusão

A análise evidencia que a vulnerabilidade socioeconômica nas regiões metropolitanas brasileiras configura-se como um sistema multidimensional interdependente, no qual fatores territoriais e econômicos desempenham papel central.

A elevada densidade e a ausência de segmentação comunitária indicam que as desigualdades se acumulam e se reforçam mutuamente.

O uso da Análise de Redes Sociais mostrou-se ferramenta eficaz para examinar a arquitetura estrutural das vulnerabilidades, oferecendo subsídios relevantes para políticas públicas integradas.

📎 Referência

Caso utilize este projeto, cite como:

Meira, Maurício Almeida (2026). Rede de Vulnerabilidades Socioeconômicas nas Regiões Metropolitanas do Brasil.
