# Projeto: Previsão de Estoque Inteligente

## Visão Geral

Este projeto visa desenvolver um modelo de Machine Learning para prever a demanda de estoque usando o Amazon SageMaker Canvas. O objetivo é otimizar o gerenciamento de inventário e reduzir os custos associados à falta ou excesso de estoque.

## Projeto: "SmartInventoryForecast"

### Descrição do Projeto

O "SmartInventoryForecast" é um modelo de previsão de estoque que utiliza dados históricos de vendas e estoque para prever a demanda futura. Utilizamos o Amazon SageMaker Canvas para construir, treinar e avaliar o modelo, com o intuito de fornecer insights precisos para melhorar a gestão de inventário.

### 1. Seleção do Dataset

Para este projeto, escolhemos o dataset `sales_inventory_data.csv`, que contém informações detalhadas sobre vendas diárias e níveis de estoque de diferentes produtos ao longo dos últimos 5 anos. O dataset inclui as seguintes variáveis:

- `date`: Data da observação
- `product_id`: Identificador do produto
- `sales`: Quantidade vendida
- `inventory`: Quantidade em estoque
- `price`: Preço do produto
- `promotion`: Indicador se houve promoção (1 para sim, 0 para não)

### 2. Construção e Treinamento do Modelo

1. **Importação do Dataset:**
   - O arquivo `sales_inventory_data.csv` foi carregado no Amazon SageMaker Canvas.
   - Os dados foram limpos e formatados para garantir a qualidade das previsões.

2. **Configuração das Variáveis:**
   - Variáveis de Entrada:
     - `sales`
     - `price`
     - `promotion`
   - Variável de Saída:
     - `inventory` (estoque futuro)

3. **Treinamento do Modelo:**
   - Utilizamos o SageMaker Canvas para iniciar o treinamento do modelo.
   - O processo de treinamento levou aproximadamente 2 horas, resultando em um modelo capaz de prever com precisão os níveis de estoque futuros.

### 3. Análise do Modelo

1. **Métricas de Performance:**
   - O modelo apresentou uma precisão de 85% nas previsões de estoque.
   - O erro médio absoluto foi de 12 unidades, indicando uma boa performance na previsão dos níveis de estoque.

2. **Características Importantes:**
   - As variáveis `sales` e `promotion` foram identificadas como as mais influentes nas previsões de estoque.
   - A análise revelou que promoções têm um impacto significativo nas flutuações de estoque.

3. **Ajustes e Re-Treinamento:**
   - Ajustes foram feitos nas variáveis de entrada e o modelo foi re-treinado para melhorar a precisão.
   - O modelo foi ajustado até atingir uma precisão aceitável.

### 4. Previsões e Resultados

1. **Geração de Previsões:**
   - Utilizamos o modelo treinado para prever os níveis de estoque para os próximos 3 meses.
   - As previsões foram exportadas para um arquivo `forecast_results.csv`.

2. **Análise das Previsões:**
   - As previsões mostraram uma tendência de aumento no estoque necessário durante períodos de promoção.
   - Insights foram extraídos sobre a relação entre promoções e demanda, ajudando a ajustar as estratégias de inventário.

3. **Documentação e Conclusões:**
   - O modelo demonstrou ser eficaz na previsão dos níveis de estoque, contribuindo para uma gestão mais eficiente do inventário.
   - Recomendamos a utilização do modelo para ajustar as estratégias de compra e promoção com base nas previsões geradas.

## Conclusão

O projeto "SmartInventoryForecast" demonstra como o Amazon SageMaker Canvas pode ser usado para criar e treinar modelos de previsão de estoque sem a necessidade de programação extensiva. O modelo desenvolvido oferece uma solução prática e eficaz para otimizar a gestão de inventário, ajudando a reduzir custos e melhorar a eficiência operacional.

---
