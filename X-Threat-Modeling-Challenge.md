# Desafio de Threat Modeling da Gi

## Atividade:

1. Identificar os ativos que quero proteger com base no case apresentado
2. Identificar as ameaças para o case apresentado
3. Identificar o nível de risco apresentado por cada ameaça a cada ativo
4. Indicar os controles que serão usados como contramedidas à essas ameaças
5. Indicar a priorização de aplicação desses controles sugeridos
6. Indicar os novos riscos após a implementação dos controles, se existentes

## Case:

A empresa XPTO está disponibilizando um serviço de PaaS de e-commerce que estará alocado em uma nuvem pública (AWS) e vai permitir aos seus usuários acessarem esse serviço sob demanda, pagando apenas pelos recursos utilizados, quando utilizados.

Esse PaaS irá oferecer as seguintes funcionalidades que poderão ser utilizadas pelos seus clientes:

1. **Vitrine de Produtos**: Permite o cadastro de novos produtos, imagens, filtros e campos de busca, valores.
2. **Segmentação de Produtos**: Permite dividir seus produtos por segmentos diferentes, podendo atribuir valores e descontos diferentes à esses segmentos.
3. **Cadastro e área logada**: Permite manter o cadastro e dados dos seus customers para utilização futura, data mining, propaganda etc.
4. **Estoque**: Permite fazer o controle de estoque da loja diretamente no PaaS, assim conforme os customers forem comprando os produtos é feita a baixa automática do estoque. 
5. **Carrinho e pagamento**: Permite todo processo de aquisição dos produtos da vitrine pelos customers, bem como todas as validações de pagamento, armazenamento do pedido feito e, caso contratada, vincula os dados de cartão/compra com o cadastro do customer.
6. **Fale Conosco**: Permite o envio de e-mails e mensagens de contato dos customers com o cliente.
7. **Mailing**: Permite o uso de uma base de customer para envio de mail marketing com promoções, novidades ou qualquer contato que o cliente queira fazer. Se contratado em conjunto com o cadastro, pode utilizá-lo como base de informações.

Existirão duas possibilidades de contratação para nosso cliente:

1. **Assinatura mensal com valor fixo**: Essa opção cobra um valor fixo mensal do cliente independente das funcionalidades e da quantidade de recursos utilizados do PaaS.
2. **Cobrança efetiva do que for utilizado**: Essa opção cobra um valor mensal variável de acordo com as funcionalidades contratadas e a quantidade de recursos utilizados do PaaS.

Existem duas formas de cobrança:

1. O cliente pode criar novos sub-clientes (Filhos) abaixo da sua conta Master, muito útil para marketplaces, sendo a cobrança nesse caso podendo ser feita:
    1. Diretamente ao cliente Master, com um consolidado único contendo o uso do cliente Master e seus sub-clientes.
    2. Diretamente ao cliente Master, com um relatório separando o uso do cliente Master e seus sub-clientes.
    3. Diretamente ao cliente Master, com segregação de links de pagamento individuais entre o cliente Master e seus sub-clientes.
2. O cliente não pode criar sub-clientes, sendo a cobrança feita diretamente cliente, muito utilizado para lojas individuais.
