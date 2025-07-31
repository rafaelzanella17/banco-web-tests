# banco-web-tests

## Objetivo

Este projeto tem como objetivo demonstrar aos alunos da Mentoria 2.0 como automatizar testes de aplicações web utilizando Cypress e JavaScript. Através deste repositório, você aprenderá a estruturar, implementar e executar testes automatizados de ponta a ponta, além de gerar relatórios detalhados dos resultados.

## Componentes do Projeto

- **Cypress**: Framework principal para automação dos testes end-to-end.
- **Custom Commands**: Comandos personalizados para reutilização de lógicas comuns nos testes, facilitando a manutenção e legibilidade do código.
- **cypress-mochawesome-reporter**: Geração de relatórios detalhados e visualmente amigáveis dos testes executados.
- **Estrutura de pastas**:
  - `cypress/e2e/`: Onde ficam os arquivos de testes automatizados.
  - `cypress/support/commands.js`: Onde estão definidos os Custom Commands.
  - `cypress/reports/`: Pasta onde são salvos os relatórios de execução.

## Pré-requisitos

- Node.js instalado
- Clonar e rodar a [API](https://github.com/juliodelimas/banco-api)
- Clonar e rodar a [aplicação Web](https://github.com/juliodelimas/banco-web)
- Depois de clonar o repositório, entrar dentro de cada pasta e instalar as dependências
   ```bash
   npm install
   ```

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/rafaelzanella17/banco-web-tests
   cd banco-web-tests
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```

## Execução dos Testes

1. Certifique-se de que a API e a aplicação Web estão rodando.
2. Execute os testes via terminal:
   ```bash
   npx cypress run
   ```
   Para abrir o Cypress em modo interativo:
   ```bash
   npx cypress open
   ```
3. Para gerar o relatório com o Mochawesome:
   ```bash
   npm test
   ```
   O relatório será gerado na pasta `cypress/reports`.

## Documentação dos Testes

### Exemplo de Teste: Login

Arquivo: `cypress/e2e/login.cy.js`

- **Login com dados válidos**: Garante que o usuário consegue acessar o sistema com credenciais corretas.
- **Login com dados inválidos**: Verifica se o sistema exibe mensagem de erro ao tentar logar com credenciais incorretas.

### Custom Commands

Arquivo: `cypress/support/commands.js`

- `cy.fazerLoginComCredenciaisValidas()`: Realiza login utilizando dados válidos.
- `cy.fazerLoginComCredenciaisInvalidas()`: Tenta login com dados inválidos para testar mensagens de erro.
- `cy.verificarMensagemNoToast(mensagem)`: Valida se uma mensagem específica aparece no componente de notificação (toast).

Esses comandos ajudam a deixar os testes mais limpos e reutilizáveis.

## Contribuição

Sinta-se à vontade para abrir issues ou pull requests para melhorias!

---
Mentoria 2.0 - Automação de Testes