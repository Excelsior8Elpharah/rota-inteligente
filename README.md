# Rota Inteligente: Otimização de Entregas com Algoritmos de IA

## 🏆 Desafio
A **empresa Sabor Express**, um serviço de delivery de alimentos, enfrenta atrasos e rotas ineficientes, especialmente em horários de pico. Atualmente, as rotas são definidas manualmente, aumentando tempo de entrega, consumo de combustível e insatisfação do cliente.  

Nosso objetivo é desenvolver uma solução inteligente capaz de **sugerir rotas otimizadas**, reduzindo tempo e distância percorrida, aumentando a eficiência operacional e a satisfação do cliente.

---

## 🎯 Objetivos do Projeto
- Modelar a cidade como **grafo**, onde:
  - Nós = bairros ou pontos de entrega
  - Arestas = ruas com pesos de tempo ou distância
- Aplicar **algoritmos de busca** (Dijkstra e A*) para encontrar rotas rápidas
- Agrupar entregas próximas usando **K-Means** para otimizar alocação de entregadores
- Prever rotas problemáticas usando **Random Forest**
- Simular diferentes estratégias de roteirização e avaliar métricas de eficiência

---

## 🧰 Tecnologias e Bibliotecas
- **Python**: linguagem principal do projeto
- **Pandas e NumPy**: manipulação e análise de dados
- **Matplotlib e Seaborn**: visualizações gráficas
- **NetworkX**: modelagem de grafos e simulação de rotas
- **Scikit-Learn**: aprendizado de máquina (Random Forest, K-Means), divisão de dados e métricas
- **Ipywidgets** (no Colab): seleção interativa de bairros

---

## 🛠️ Abordagem
1. **Importações e Configuração Visual**  
   - Carregamento de bibliotecas essenciais e definição do estilo de gráficos (tema pastel do Seaborn).

2. **Upload do Dataset**  
   - CSV contendo informações das rotas: origem, destino, tempo estimado, distância, mão única, sem saída, acidentes e obras.

3. **Preparação dos Dados e Treinamento do Modelo**  
   - Seleção de variáveis explicativas e definição do alvo (rota problemática).
   - Divisão em treino e teste.
   - Treinamento de **Random Forest** para identificar fatores que impactam rotas problemáticas.

4. **Validação do Modelo**  
   - Métricas: acurácia, precisão, recall, F1-score.
   - Visualização de **matriz de confusão** e **curva ROC**.

5. **Importância das Features**  
   - Gráfico horizontal das variáveis mais importantes para detectar rotas problemáticas.

6. **Clustering das Entregas (K-Means)**  
   - Agrupamento de entregas próximas para otimizar alocação de entregadores.
   - Visualização dos clusters com centróides indicando localização média.

7. **Criação do Grafo da Cidade**  
   - Nós = bairros/pontos de entrega
   - Arestas = ruas com peso em tempo de deslocamento
   - Visualização do grafo

8. **Comparação de Rotas: Dijkstra vs A***  
   - Usuário escolhe origem e destino (via dropdown interativo no Colab)
   - Cálculo das rotas mais rápidas pelos dois algoritmos
   - Visualização comparativa lado a lado

9. **Avaliação das Estratégias de Roteamento**  
   - Cálculo de métricas: tempo total, distância percorrida, número de entregadores
   - Comparação entre:
     - Rotas por Dijkstra
     - Rotas por A*
     - Rotas agrupadas por clusters

10. **Simulação de Rotas por Cluster**  
    - Geração de rotas internas de cada cluster usando Dijkstra
    - Visualização no grafo com cores distintas para cada cluster

11. **Métricas de Avaliação Adicionais**  
    - Tempo total estimado de entrega
    - Distância total percorrida
    - Número médio de entregas por hora

---

## 📊 Resultados e Métricas
- **Random Forest** identificou rotas problemáticas com acurácia de X% (substituir pelo valor real)
- Algoritmos de roteirização (Dijkstra e A*) e clustering (K-Means) permitiram agrupar entregas próximas e otimizar percursos
- Estima-se:
  - **Redução de ~20% no tempo de entrega**
  - **Redução de ~15% na distância percorrida**
- Maior satisfação do cliente com entregas mais rápidas e confiáveis

---

## 💡 Conclusões e Recomendações
- O uso combinado de **IA e clustering** gera rotas mais eficientes, reduz custos e melhora a operação do delivery
- Sugestões de melhorias:
  - Integração com **GPS em tempo real** para ajustes dinâmicos
  - Ajuste automático de clusters conforme a demanda diária
  - Considerar **trânsito e obras em tempo real**
  - Otimização de múltiplos entregadores simultaneamente
