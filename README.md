## Caso de Teste Manual: Teste Funcionais  – nopcommerce.com ##


Link para acesso ao Caso de Teste no Google Sheets - Planilhas:


https://docs.google.com/spreadsheets/d/1RaR0bIBcNcMlt2uP1Z3Ct9LxYfzMBImo9JBk0wKerJM/edit?usp=sharing


Detalhamento do arquivo:

- Planilha criada para a realização do processo completo de Testes para a plataforma, abordando Testes Funcionais, afim de validar seus requisitos e os fluxos principais do sistema de E-commerce.

- O arquivo está exposto nas seguintes confdições: 08 Páginas (abas) distintas, sendo cada uma abortando uma fase do Case de Teste, estruturada da seguinte forma:
- 01: Análise de Critésrios de Aceite
- 02: Análise de Negócios
- 03: Epic (Epíco)
- 04: Histórias
- 05: Critérios de Aceite
- 06: Planejamento para a execução dos testes
- 07: Manual Test - Testes Manuais
- 08: Bug Report
- 09: Test Report
  
_____________________________________________________________________


Aqui, segue a estruturação completa dos Case de Teste elaborado para esse estudo:

------------------------

## Identificação ##
- Projeto: nopcommerce.com  - Manual Test Cases - 

- Título: Fluxo Completo de Teste da plataforma

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

## T001 ##

![01](https://github.com/user-attachments/assets/50445f9d-6d8f-4c1a-8221-98fdae74fea6)

![01 1](https://github.com/user-attachments/assets/d7a27abb-70bc-4767-9aa3-055e3e63304a)

![01 2](https://github.com/user-attachments/assets/caed9cb9-e97a-4b60-853b-c5da45df5bd5)

## T002 ##

![02](https://github.com/user-attachments/assets/adaf33a1-cbae-43fe-95c3-1c13169cbc41)

## T003 ## 

![03](https://github.com/user-attachments/assets/1bc1732d-21de-418f-b9b1-96febea0ad2e)

## BUG Evidência ## 

![03 BUG](https://github.com/user-attachments/assets/e13678fc-d839-4729-9827-406a283140cc)

## T004 ## 

![04](https://github.com/user-attachments/assets/f99427de-ff9f-49c5-b0d8-b4d48e45fd18)

![04 1](https://github.com/user-attachments/assets/f3e39086-b83b-4dd2-8d04-90fc7a252c36)

## T005 ##

![T005 0](https://github.com/user-attachments/assets/94841c9f-5a3c-4d5c-aedf-22d975d709c3)

![T005 1](https://github.com/user-attachments/assets/4c25e0da-dc93-40de-a141-60d1b3be2c0f)


## T006 ##

<img width="1238" height="854" alt="image" src="https://github.com/user-attachments/assets/6886c0d1-2f3a-4c64-bd14-e5ee27a9e19a" />


## T007 ##

 <img width="1239" height="960" alt="image" src="https://github.com/user-attachments/assets/817d46dc-a6cb-408a-845f-4a18c92ceba6" />
                  
## T008 ##

<img width="1243" height="947" alt="image" src="https://github.com/user-attachments/assets/eb43cf30-3be1-4332-a7cb-599e4408c947" />

## T009 ##

<img width="1204" height="947" alt="image" src="https://github.com/user-attachments/assets/50ca83af-dae0-4361-98df-1aca5ea651fd" />

## T010 ##

<img width="1238" height="942" alt="image" src="https://github.com/user-attachments/assets/6c035247-639c-45ba-80ec-ce4bc44e578e" />

## T011 ##

<img width="1225" height="940" alt="image" src="https://github.com/user-attachments/assets/3843fad6-0c4d-446c-bd08-04c5a1234bca" />


## T012 ##

<img width="1227" height="952" alt="image" src="https://github.com/user-attachments/assets/5b7199ce-be2a-4089-b1d0-4652ecc6b10f" />

## BUG REPORT 01 ##

|BUG REPORT |        | 
| --------- | ------ | 
| Passos para Reprodução | 1- Clicar em 'Login in"   2- Prencher dados válidos 3- Submeter | 
| Resultado Esperado | Login bem sucedido, nome do usuário visivel.   | 
| Resultado Encontrado | O sistema realiza o login, mas não apresenta o nome do usuário visivel. |
| Ambiente de Teste | DEV - https://demo.nopcommerce.com/cart  | 
| Prioridade | Baixa  | 
| Tipo | Funcionalidade  | 
| Evidência | Print de Tela | 

![03](https://github.com/user-attachments/assets/1bc1732d-21de-418f-b9b1-96febea0ad2e)

![03 BUG](https://github.com/user-attachments/assets/e13678fc-d839-4729-9827-406a283140cc)


## BUG REPORT 02 ##

|BUG REPORT |        | 
| --------- | ------ | 
| Passos para Reprodução | 1- Selecionar itens no catalogo de produtos, e colocar no carrinho de compras 'ADD TO CART'  2- No carrinho de compras, alterar as quantidades dos itens selecionados. 3- Atualizar a página do carrinho de compras 'ADD TO CART' | 
| Resultado Esperado | O sistema deve retornar a página do carrinho de compras 'ADD TO MART' , mostrando os itens e quantidades secionados, permitindo editar as quantidades dos itens.    | 
| Resultado Encontrado | O sistema retornou a página do carrinho de compras com os itens selecionados, mas com bug no SKU N_1020_LU - sem o campo correspondente de quantidade, e o SKU SG_24_256B sem o campo referente a quantidades.  |
| Ambiente de Teste | DEV - https://demo.nopcommerce.com/cart  | 
| Prioridade | Alta  | 
| Tipo | Funcionalidade  | 
| Evidência | Print de Tela | 

<img width="1238" height="942" alt="image" src="https://github.com/user-attachments/assets/6c035247-639c-45ba-80ec-ce4bc44e578e" />


