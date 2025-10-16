## Caso de Teste Manual: Teste Funcionais  – nopcommerce.com ##

_____________________________________________________________________

## Identificação ##
- Projeto: nopcommerce.com  - Manual Test Cases - 

- Título: Fluxo Completo de Criação de utilização da plataforma

- Responsável: Joaquim Pedro

- Status: Executado


## Descrição ##


O conjunto de testes a seguuir, representa testes funcionais manuais, voltados à validação de requisitos e fluxos principais do sistema nopCommerce. com abrangência em:

- Cenários positivos e negativos

- Fluxos de interface e usabilidade

- Testes de integração entre módulos

- Teste de fluxo completo (Checkout)

A planilha busca cobrir testes manuais funcionais, do tipo caixa preta, focados em verificar se o sistema se comporta conforme os requisitos previstos, e se as mensagens e respostas da interface são adequadas.


 ## Pré-condições ##

- Acesso ao demo: https://demo.nopcommerce.com/

- Usuário administrador válido (Admin / admin123)

- Navegador utilizado: Google Chrome


## Passos: ##

| ID Teste  | Caso de Teste | Pré Condição | Passos | Resultado Esperado | Status | Resultado Encontrado | 
| ------------- | ------------- | -------- | ------ | --------| ------ | ---- | 
| T001   | Cadastro de Novo Usuario  | Não estar logado | 1. Clicar em 'Register' 2- Preencher todos os campos 3- Clicar em Register |  Usário registrado, com mensagem de sucesso. | Passou | O registro foi realizado corretamente, conforme esperado. |
| T002   | Cadastro com email já existente  | Conta existente com mesmo email  | 1- Ir em 'Register' 2- Preencher email já cadastrado 3- Submeter |  Menagem de erro de email já cadastrado | Passou | O sitema retornou a mensagem de erro de email já cadastrado |
| T003   | Login com Sucesso  | Usuário já Cadastrado  | 1- Clicar em 'Login in" 2- Prencher dados válidos 3- Submeter |  Login bem sucedido, nome do usuário visivel.  | Falhou | O sistema realiza o login, mas não apresenta o nome do usuário visivel.  |
| T004   | Login Inválido  | Usuário já Cadastrado  | 1- Clicar em 'Log in' 2- Entrar com um email/senha inválidos 3- Clicar no botão 'LOG IN' |  O sistema devera retornar mensagem de erro 'Login was unsuccessful'  | Passou | O sistema retornou a mensagem de erro 'Login was unsuccessful' após a tentativa de longin com as credenciais indevidadas. |
| T005   | Busca por produto existente  | Acessar a página e utilizar o campo 'Search store', e usar o termo 'Iphone'  | 1- Localizar o campo 'Search store' 2- Digitar o termo válido no campo de busca 'Iphone' 3- Clicar no botão 'Search' |  O sistema ira realizar a pesquisa e retornar os produtos relacionados de acordo com o item pesquisado  | Passou | O sistema realiza a pesquisa e retorna o resultado conforme o item pesquisado |
| T006   | Busca sem resultado  | Acessar a página e utilizar o campo 'Search store' | 1- Localizar o campo 'Search store' 2- Digitar um termo inexistente no campo de busca - 'porsche' 3- Clicar no botão 'Search' | O sistema retornar mensagem 'No products were found | Passou | O sistema retornou a mensgem 'No products were found that matched your criteria.' |
| T007   | Navegação por Categorias  | Acessar a página e nagevar entre as categorias | 1- Acessar a página inicial, e clicar em uma categoria - ex.: 'Computers' 2- Visualisar a lista referente |  O sistema deve retornar a lista de produtos referente a categoria 'Computers' | Passou | O sistema retornou corretamente lista de produtos referente a 'Computers' |
| T008   | Visualização dos detalhes do produto  | Localizar o produto 'Apple MacBook Pro 13-inch' e verificar se a página retorna os detalhes de visualização do produto selecionado | 1- Acessar a página inicial, e clicar na categoria : 'Computers', 'NOTEBOOKS' 2- Localizar o 'Apple MacBook Pro 13-inch' 3- Selecionar o Apple MacBook Pro 13-inch, e á pagina, responder retornando os delathes do item escolhido |  O sistema deve retornar a página de detalhes do produto, com nome, imagem, preço, estoque e descrição do produto | Passou | O sistema retornou corretamente lista de produtos referente item selecionado, apresentando os dados esperados.  |
| T009   | Adição de item no carrinho de compras  'Add to cart'  | Estar logado no sistema da página, e escolher um item e adicionar ao carrinho 'Add to cart' | 1- Acessar a página inicial, e clicar na categoria : 'Computers', 'DESKTOPS' 2- Localizar, e selecionar o protduto 'Digital Storm VANQUISH Custom Performance PC' 3- Adicionar o item 'Digital Storm VANQUISH Custom Performance PC' ao carrinho de compras 'ADD TO CART", e alterar a quantidade para 03 unidades do item. |  O sistema deve retornar a página do carrinho de compras 'ADD TO CART', mostrando SKU, Image do item, Product(s), Price, Qty - que deve ser alterada para 03 , Total e opção Remove e demais opções do ADD TO CART.  | Passou | Após realizar os passos solicitado, o sistema retornou corretamente o item, seus detalhes, valor unitario, quantidade e o valor total corretamente, demosntrando os dados solicitados. |
| T010   | Adicionar diversos itens e editar a quantidade de itens no carrinho de compras 'ADD TO CART'  | Produtos já no carrinho de compras 'ADD TO CART' | 1- Selecionar mais de um iten no catalogo de produtos, e colocar no carrinho de compras 'ADD TO CART' 2- No carrinho de compras, alterar as quantidades dos itens selecionados. 3- Atualizar a página do carrinho de compras 'ADD TO CART' |  O sistema deve retornar a página do carrinho de compras 'ADD TO MART' , mostrando os itens e quantidades secionados, permitindo editar as quantidades dos itens.  | Falhou | O sistema retornou a página do carrinho de compras com os itens selecionados, mas com bug no SKU N_1020_LU - sem o campo correspondente de quantidade, e o SKU SG_24_256B sem o campo referente a quantidades. |
| T011   | Remover itens que estejam no carrinho de compras 'ADD TO CART'  | Produtos já no carrinho de compras 'ADD TO CART' | 1- Ir no carrinho de compras com os itens já adicionados 2- Remover todos os itens do carrinho |  O sitema deverá remover os produtos e apresentar uma mensagem de confirmação | Passou | O sistema remove os itens selecionados, e apresentou a mensgaem de confirmação da operação. |
| T012   |Realizar o Checkout completo do carrinho de compras 'ADD TO CART'  | Usuário logado na página, e produtos selecionados já no carinho de compras 'ADD TO CART'  |1- Ir no carrinho de compras com os itens já adicionados 2- Clicar no 'Checkout' 3 -Preencher os dados solicitados 4- Finalizar o pedido no 'Checkout' |  O sitema deverá mostrar os produtos selecionados, apresentar uma mensagem de confirmação, e finalizar com o 'Checkout' | Passou | O sistema apresentou os itens dentro do carrinho de compras, e retornou corretamente com a mesagem de 'Tahnk you Your order has been successsfully processed! ORDE NUMBER:6'. |
_________________________________________________________________

## Evidências dos Testes ## 

T001

Incluir as prints das telas dos testes realizados como evidências dos testes. 





