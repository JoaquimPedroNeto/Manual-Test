# Manual-Test
Teste Manuais - Repositório com alguns teste Manuais de estudo.
________________________________________________________________

## Caso de Teste Manual: Teste Funcionais  – nopcommerce.com ##

Identificação
Projeto: nopcommerce.com Manual Test Cases

Título: Fluxo Completo de Criação de utilização da plataforma

Responsável: Joaquim Pedro

Status: Executado


## Descrição ##

O conjunto de testes a seguuir, representa testes funcionais manuais, voltados à validação de requisitos e fluxos principais do sistema nopCommerce. com abrangência em:

- Cenários positivos e negativos

- Fluxos de interface e usabilidade

- Testes de integração entre módulos

- Teste de fluxo completo (Checkout)

A planilha cobre testes manuais funcionais de caixa preta, focados em verificar se o sistema se comporta conforme os requisitos previstos e se as mensagens e respostas da interface são adequadas.


Pré-condições

Acesso ao demo: https://demo.nopcommerce.com/

Usuário administrador válido (Admin / admin123)

Navegador utilizado: Google Chrome


Passos: 

| ID Teste  | Caso de Teste | Pré Condição | Passos | Resultado Esperado | Status | Resultado Encontrado | 
| ------------- | ------------- | -------- | ------ | --------| ------ | ---- | 
| T001  | Cadastro de Novo Usuario  | Não estar logado | 1. Clicar em 'Register' 2- Preencher todos os campos 3- Clicar em Register |  Usário registrado, com mensagem de sucesso. | Passou | O registro foi realizado corretamente, conforme esperado. |
| T002  | Cadastro com email já existente  | Conta existente com mesmo email  | 1- Ir em 'Register' 2- Preencher email já cadastrado 3- Submeter |  Menagem de erro de email já cadastrado | Passou | O sitema retornou a mensagem de erro de email já cadastrado |


_________________________________________________________________
