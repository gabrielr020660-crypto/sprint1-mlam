# Challenge Sprint 1 - Modelagem Linear para Aprendizado de Máquina

## 1. Introdução
Este projeto tem como objetivo realizar uma análise exploratória utilizando uma base de dados real do setor de e-commerce, aplicando tabelas de distribuição de frequência em Python. A análise permite compreender padrões de compra e comportamento do consumidor, auxiliando na tomada de decisão empresarial.



## 2. Base de Dados Utilizada
A base utilizada foi o dataset público **Brazilian E-Commerce Public Dataset by Olist**, disponível no Kaggle.  
Esse conjunto de dados contém registros reais de pedidos realizados em um marketplace brasileiro.

A escolha dessa base se justifica por ser confiável, possuir grande volume de registros e apresentar variáveis relevantes para análise de vendas e satisfação do cliente.

A base que foi obtida no Kaggle:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce


## 3. Arquivos Utilizados
A base final foi construída a partir da junção dos seguintes arquivos:

- olist_orders_dataset.csv
- olist_order_items_dataset.csv
- olist_order_reviews_dataset.csv



## 4. Variáveis Selecionadas

### 4.1 Variáveis Qualitativas Nominais
- `order_status` (status do pedido: delivered, shipped, canceled, etc.)
- `order_id` (identificador nominal do pedido)

### 4.2 Variáveis Qualitativas Ordinais
- `review_score` (nota de avaliação do cliente: 1 a 5)
- `faixa_preco` (classificação por faixa de preço: Baixo, Médio e Alto)

### 4.3 Variáveis Quantitativas Discretas
- `order_item_id` (posição do item dentro do pedido, utilizado para analisar frequência de itens)
- `review_score` (pode ser interpretado também como discreto)

### 4.4 Variáveis Quantitativas Contínuas
- `price` (preço do item)
- `freight_value` (valor do frete)



## 5. Tabelas de Distribuição de Frequência
Foram geradas tabelas de frequência para:

- **Variável discreta:** `order_item_id`
- **Variável contínua:** `price`

As tabelas foram construídas utilizando Python e a biblioteca Pandas.



## 6. Principais Insights Obtidos

### 6.1 Variável Discreta (order_item_id)
- A maioria dos pedidos possui poucos itens, pois os valores menores de `order_item_id` são os mais frequentes.
- Valores altos de `order_item_id` aparecem raramente, indicando que compras em grande volume são exceções.

### 6.2 Variável Contínua (price)
- A maior parte dos preços se concentra em faixas mais baixas, mostrando predominância de produtos com menor custo.
- As faixas finais apresentam baixa frequência, indicando produtos caros e possíveis outliers.



## 7. Aplicação para Tomada de Decisão Empresarial
Os resultados podem contribuir diretamente para a empresa em pontos como:

- Identificação de padrões de compra e quantidade média de itens por pedido
- Apoio para estratégias de precificação e promoções
- Segmentação de produtos com base em faixas de preço
- Melhor entendimento do perfil de consumo dos clientes



## 8. Conclusão
A análise estatística por tabelas de frequência foi eficiente para resumir e compreender o comportamento das vendas em um marketplace brasileiro. O uso do Python permitiu automatizar o processo e gerar insights relevantes, reforçando a importância da análise de dados para decisões empresariais e aplicações futuras de aprendizado de máquina.