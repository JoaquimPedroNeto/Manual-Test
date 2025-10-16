# Manual-Test
Teste Manuais - Repositório com alguns teste Manuais de estudo.
________________________________________________________________

## Caso de Teste Manual: Teste Funcionais  – nopcommerce.com ##

- Identificação
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
| T001  | Cadastro de Novo Usuario  | Não estar logado | 1. Clicar em 'Register' 2- Preencher todos os campos 3- Clicar em Register |  Usário registrado, com mensagem de sucesso. | Passou | O registro foi realizado corretamente, conforme esperado. |
| T002  | Cadastro com email já existente  | Conta existente com mesmo email  | 1- Ir em 'Register' 2- Preencher email já cadastrado 3- Submeter |  Menagem de erro de email já cadastrado | Passou | O sitema retornou a mensagem de erro de email já cadastrado |
| T003  | Login com Sucesso  | Usuário já Cadastrado  | 1- Clicar em 'Login in" 2- Prencher dados válidos 3- Submeter |  Login bem sucedido, nome do usuário visivel.  | Falhou | O sistema realiza o login, mas não apresenta o nome do usuário visivel.  |
| T004  | Login Inválido  | Usuário já Cadastrado  | 1- Clicar em 'Log in' 2- Entrar com um email/senha inválidos 3- Clicar no botão 'LOG IN' |  O sistema devera retornar mensagem de erro 'Login was unsuccessful'  | Passou | O sistema retornou a mensagem de erro 'Login was unsuccessful' após a tentativa de longin com as credenciais indevidadas. |

_________________________________________________________________
