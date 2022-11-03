<img src="Apresentação e imagens/olist.jpg" align="left" width="30%"/>
<br/>
<br/>
<br/>
Status do projeto: ativo, em andamento

# Descrição Olist - Plataforma de e-commerce
<br/>
"Conjunto de dados públicos de comércio eletrônico brasileiro por Olist O conjunto de dados tem informações de 100 mil pedidos de 2016 a 2018 feitos em vários marketplaces no Brasil.

A Olist conecta pequenas empresas de todo o Brasil a canais sem complicações e com um único contrato. Esses comerciantes podem vender seus produtos através da Olist Store e enviá-los diretamente aos clientes usando os parceiros de logística da Olist.

Depois que um cliente compra o produto da Olist Store, um vendedor é notificado para atender esse pedido. Assim que o cliente recebe o produto, ou vence a data prevista de entrega, o cliente recebe uma pesquisa de satisfação por e-mail onde pode dar uma nota da experiência de compra e anotar alguns comentários."
"___"

# Fonte de dados
Neste projeto, utilizamos dados compartilhados pela Olist - plataforma brasileira de e-commerce. 
A base de dados pode ser acessada no Kaggle, em https://www.kaggle.com/olistbr/brazilian-ecommerce A base de dados completa conta com mais de 100 mil regitros de pedidos em 8 conjuntos de dados separados, sobre:

Consumidores | Vendedores | Produtos | Pedidos | Categoria de pedidos | Avaliação de pedidos |Pagamentos Geolocalização
Cada conjunto possui informações exclusivas sobre um assunto em questão, podendo ser cruzados de diversas maneiras a fim de se obter informações sobre o quesito escolhido. No caso deste trabalho, a abordagem será realizada com foco nos Consumidores.

* O arquivo  `olist_customers_dataset.csv` contem os seguintes recursos:

Feature | Description 
----------|---------------
**customer_id** | Id of the consumer who made the purchase.
**customer_unique_id**    | Unique Id of the consumer.
**customer_zip_code_prefix** | Zip Code of the location of the consumer.
**customer_city** | Name of the City from where order is made.
**customer_state** |  State Code from where order is made(Ex- sao paulo-SP).

* The `olist_sellers_dataset.csv` contains following features:

Feature | Description 
----------|---------------
**seller_id** |   Unique Id of the seller registered in olist.
**seller_zip_code_prefix** | Zip Code of the location of the seller.
**seller_city** | Name of the City of the seller.
**seller_state** | State Code (Ex- sao paulo-SP)


* The `olist_order_items_dataset.csv`  contain following features:

Feature | Description 
----------|---------------
**order_id** | A unique id of order made by the consumers.
**order_item_id** | A Unique id given to each item ordered in the order.
**product_id** |A unique id given to each product available on the site.
**seller_id** | Unique Id of the seller registered in olist.
**shipping_limit_date** | The date before which shipping of the ordered    product must be completed.
**price** | Actual price of the products ordered .
**freight_value** | Price rate at which a product is delivered from one point to another. 

* The `olist_order_payments_dataset.csv` contain following features:

Feature | Description 
----------|---------------
**order_id** | A unique id of order made by the consumers.
**payment_sequential** | sequences of the payments made in case of EMI.
**payment_type** |  mode of payment used.(Ex-Credit Card)
**payment_installments** | number of installments in case of EMI purchase.
**payment_value** | Total amount paid for the purshase order.



* The `olist_orders_dataset.csv`  contain following features:

Feature | Description 
----------|---------------
**order_id** | A unique id of order made by the consumers.
**customer_id** | Id of the consumer who made the purchase.
**order_status** | status of the order made i.e delivered, shipped etc.
**order_purchase_timestamp** | Timestamp of the purchase.
**order_approved_at** | Timestamp of the order approval.
**order_delivered_carrier_date** | delivery date at which carrier made the delivery.
**order_delivered_customer_date** | date at which customer got the product.
**order_estimated_delivery_date** | estimated delivery date of the products.


* The `olist_order_reviews_dataset.csv`  contain following features:

Feature | Description 
----------|---------------
**review_id** |Id of the review given on the product ordered by the order id.
**order_id** |  A unique id of order made by the consumers.
**review_score** | review score given by the customer for each order on the scale of 1–5. 
**review_comment_title** | Title of the review
**review_comment_message** | Review comments posted by the consumer for each order.
**review_creation_date** |Timestamp of the review when it is created.
**review_answer_timestamp** | Timestamp of the review answered.


* The `olist_products_dataset.csv` contain following features:

Feature | Description 
----------|---------------
**product_id** | A unique identifier for the proposed project.
**product_category_name** | Name of the product category
**product_name_lenght** | length of the string which specify the name given to the products ordered.
**product_description_lenght** | length of the description written for each product ordered on the site.
**product_photos_qty** | Number of photos of each product ordered available on the shopping portal.
**product_weight_g** | Weight of the products ordered in grams.
**product_length_cm** | Length of the products ordered in centimeters.
**product_height_cm** | Height of the products ordered in centimeters.
**product_width_cm** | width of the product ordered in centimeters.


# Métodos
Lista de métodos utilizados:

Pandas – Manipulação e análise de dados
NumPy – Manipulação de dados
Seaborn - Visualização gráfica
Matplotlib – Visualização gráfica
Pycaret - Aprendizado de modelo
Tableu - Visualização gráfica


# Tecnologias
Lista com tecnologias utilizadas:

MySQL
Tableu
Python

# Descrição do Projeto
A missão de cada empresa é satisfazer seus clientes. Com uma plataforma de comércio eletrônico em que a compra dos clientes é afetada pelo feedback do produto e pelas classificações dos vendedores, manter um ciclo de feedback positivo é crucial para o retorno do cliente e o crescimento das vendas. Portanto, neste projeto, estamos interessados em prever as pontuações das avaliações dos clientes, para entender melhor a experiência dos clientes por meio da qualidade do produto, reputação dos vendedores e processo de envio. Isso ajudaria a empresa a continuar selecionando melhores produtos para oferecer em sua plataforma, recomendar vendedores mais confiáveis, melhorar a operação de entrega e, principalmente, projetar o atendimento ao cliente e campanhas de marketing eficazes para diferentes clientes-alvo. 
___

## Passos
* Leitura dos arquivos originais (csv)
* Manipulação dos dados (limpeza, tratamento, manipulação)
* Agrupamento de dados
* Visualização dos dados agregados 
* Análise de insights
* Pré-processamento dos dados dividios em traino e teste utilizando a regressão para prever a probalilidade no conjunto de teste
* Interpretação dos resultados da regressão 
* Selecionar informações e respostas para elaboração da apresentação

___

## Considerações finais
<img src="Apresentação e imagens/Variable_importance.png" align="center" width="100%"/>
<br/>
O recurso com maior efeito é relativo ao processo de entrega: erro_estimativa_dias_entrega. Isso torna-se notável com uma de nossas primeiras hipóteses sobre o efeito do tempo de envio na satisfação do cliente. Quando o tempo de entrega real é maior do que o esperado (erro de estimativa > 0), o número de avaliações insatisfeitas aumenta, ou seja, entregas longas e atrasadas descontentam os clientes.

A Olist atua como uma plataforma de e-commerce conectando vendedores e compradores online, ao mesmo tempo em que fornece serviços logísticos, que inclusive foi o terceiro recurso com maior efeito. Garantir excelencia nos serviços de envio é um dos fatores fundamentais para atrair e manter vendedores e clientes.

A entrega dos produtos é processada através de várias etapas, portanto, é conduzido por vários fatores, como gerenciamento de estoque, velocidade de manuseio de pedidos e transporte. Sem muitas informações sobre a operação interna da Olist, nossa sugestão é que a empresa acompanhe efetivamente as etapas de envio para obter um tempo estimado de entrega mais preciso, ao mesmo tempo em que detecta procedimentos ineficientes para melhorar o desempenho geral do envio.

Através do modelo Regression entendemos a importancia de alguns parametros que podem influenciar no crescimento das vendas dos parceiros.
A Olist pode continuar a expandir sua reputação para atrair novos clientes através:

* Entrega do pedido antes ou até a data prevista
* O vendedor precisa comparar o valor do seu produto para deixá-lo mais competitivo 
* Preencher todos os campos com o máximo de detalhes do produto
* Publicar maior número de fotos
* Buscar o máximo de alternativas de transportadoras para reduzir o valor do frete
* Responder no menor tempo possivel as dúvidas dos clientes

Uma das tarefas mais importantes do projeto é identificar clientes satisfeitos. Clientes satisfeitos são mais propensos a voltar. Este é o grupo de clientes que a estratégia de marketing da Olist pode atingir, para obter melhores resultados com menos recursos. A empresa também pode estudar o hábito de clientes satisfeitos, as categorias de produtos e vendedores mais populares ​​para melhorar seu sistema de recomendação.
<br/>

___

Contato Claudia Garcia
* linkedin: www.linkedin.com/in/ claudia-garcia0204
* github: https://github.com/claudiagarcia0204

Contato Paulo Choi
* linkedin: linkedin.com/in/paulo-choi-69180a247/
* github: https://github.com/tchepaulo

![GitHub top language](https://img.shields.io/github/languages/top/claudiagarcia0204/Projeto-Final---Olist)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/claudiagarcia0204/Projeto-Final---Olist)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/claudiagarcia0204/Projeto-Final---Olist)
![GitHub last commit](https://img.shields.io/github/last-commit/claudiagarcia0204/Projeto-Final---Olist)



