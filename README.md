📦 Rota Inteligente: Otimização de Entregas com Algoritmos de IA
🚀 Desafio

A Sabor Express, uma pequena empresa de delivery de alimentos, enfrenta dificuldades para gerenciar suas entregas durante horários de pico (almoço e jantar). Atualmente, as rotas são definidas manualmente pelos entregadores, resultando em:

Rotas ineficientes;

Atrasos nas entregas;

Maior custo de combustível;

Insatisfação dos clientes.

A missão deste projeto é desenvolver uma solução inteligente baseada em algoritmos de IA para sugerir as melhores rotas, considerando restrições urbanas, tempo de deslocamento e agrupamento de pedidos próximos.

🎯 Objetivos

Representar a cidade como um grafo, onde os nós são bairros/endereços e as arestas são ruas com pesos (tempo/distância).

Implementar algoritmos de busca de caminhos mínimos (Dijkstra, A*).

Realizar agrupamento de entregas próximas usando K-Means.

Avaliar a eficiência da solução e sugerir melhorias.

Reduzir custos e aumentar a satisfação do cliente.

🧠 Abordagem Utilizada

Representação com Grafos

A cidade foi modelada como um grafo direcionado usando NetworkX.

Cada rota contém informações de tempo, distância e possíveis restrições (rua de mão única, obras, acidentes etc.).

Algoritmos de Busca

Dijkstra: encontra o menor caminho com base nos pesos das arestas.

A*: variação que considera heurística, permitindo otimizações na busca.

Clustering de Entregas

K-Means: aplicado para agrupar pedidos próximos em regiões, facilitando a atribuição a diferentes entregadores.

Machine Learning Supervisado

Random Forest: modelo treinado para prever se uma rota pode apresentar problemas (acidentes, obras etc.).

Visualizações

Gráficos de clusters das cidades.

Grafos mostrando rotas calculadas (Dijkstra e A*).

Importância de features no modelo de ML.

Curva ROC e matriz de confusão para avaliação do classificador.

⚙️ Tecnologias Utilizadas

Python 3

Bibliotecas:

pandas, numpy, matplotlib, seaborn

networkx (modelagem de grafos)

scikit-learn (machine learning e clustering)

🔑 Algoritmos Implementados

Busca em Grafos: Dijkstra, A*

Machine Learning: Random Forest

Clustering: K-Means

Outros conceitos explorados:

Heurísticas em grafos

Análise de importância de variáveis

Padronização de dados (StandardScaler)

📊 Resultados e Análise

O Random Forest obteve boa acurácia na previsão de problemas em rotas.

Os clusters formados pelo K-Means permitiram dividir entregas em regiões de forma lógica e eficiente.

O Dijkstra foi eficiente em encontrar rotas mínimas, mas o A* mostrou-se mais rápido em grafos maiores.

Visualizações gráficas permitiram identificar gargalos e oportunidades de melhoria.

Limitações:

Não considera trânsito em tempo real.

Heurística do A* implementada de forma simples (pode ser melhorada com distância geográfica real).

Uso de dados simulados (CSV), podendo ser estendido para dados reais via API de mapas.

Sugestões de melhoria:

Implementar heurísticas baseadas em coordenadas reais (Haversine).

Integrar com APIs como Google Maps / OpenStreetMap.

Explorar algoritmos de otimização de múltiplas rotas (ex.: Problema do Caixeiro Viajante, VRP).

🗂️ Estrutura do Repositório
📂 rota-inteligente
 ┣ 📂 data/              # CSVs e datasets usados
 ┣ 📂 src/               # Código-fonte do projeto
 ┣ 📂 docs/              # Documentação, imagens e diagramas
 ┣ README.md             # Documentação principal
 ┗ requirements.txt      # Bibliotecas necessárias

▶️ Como Executar

Clone o repositório:

git clone https://github.com/seu-usuario/rota-inteligente.git
cd rota-inteligente


Instale as dependências:

pip install -r requirements.txt


Execute o projeto no Google Colab ou localmente em Python:

python src/main.py

📌 Exemplos de Saída
🔹 Clusterização de Capitais

🔹 Rotas Dijkstra vs A*

🔹 Importância das Features (Random Forest)
