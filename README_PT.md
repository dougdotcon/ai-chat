# <img src="https://raw.githubusercontent.com/ksdev-pl/ai-chat/master/public/icon-192.png" alt="Logo" width="25" height="25"/> OpenAI Chat

[![Licença: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

🔗 **[aichat.ksdev.pl](https://aichat.ksdev.pl)**

![Captura de Tela](.github/screenshot.jpg)

## Visão Geral

**OpenAI Chat** é um cliente web moderno e *serverless* projetado para uma interação perfeita com os modelos de linguagem da OpenAI. Ele prioriza a privacidade do usuário ao operar inteiramente dentro do navegador, garantindo que nenhum dado seja enviado a um servidor de backend.

### Principais Recursos

*   **100% do Lado do Cliente:** Nenhum backend necessário. Executa diretamente no seu navegador.
*   **Privacidade Aprimorada:** Sua API key, histórico de bate-papo e configurações são armazenados localmente usando IndexedDB.
*   **Suporte a Markdown:** Formatação de texto avançada com renderização completa para código, listas e mais.
*   **Histórico de Conversas:** Sessões de chat persistentes salvas localmente.
*   **Interface Moderna:** Limpa, responsiva e rápida, construída com Vue.js.
*   **Pronto para Docker:** Implantação fácil com um único comando `docker compose`.

## Pré-requisitos

*   Node.js (v18+)
*   Uma [API Key da OpenAI](https://platform.openai.com/account/api-keys) válida.

## Começando

### Desenvolvimento

1.  **Instale as dependências:**
    sh
    npm install
    

2.  **Execute o servidor de desenvolvimento:**
    sh
    npm run dev
    

3.  Abra seu navegador e acesse a URL local fornecida (geralmente `http://localhost:5173`).

### Build para Produção

Para compilar e minificar para produção:

sh
npm run build


Os arquivos compilados estarão disponíveis no diretório `dist`.

### Implantação com Docker

Um arquivo `docker-compose.yml` está incluído para facilitar a configuração.

sh
# Inicia o container
 docker compose up


Para rodar em uma porta personalizada (ex: 8080):

sh
PORT=8080 docker compose up


A aplicação estará disponível em `http://localhost:5173` (ou na sua porta personalizada).

## Arquitetura e Segurança

*   **Serverless:** A aplicação é um SPA (Single Page Application) estático. Ela não possui um backend de API.
*   **Isolamento de Dados:** Todos os dados sensíveis são tratados no lado do cliente. A comunicação ocorre diretamente entre o seu navegador e os servidores da OpenAI.
*   **Gerenciamento de Estado:** Utiliza o `IndexedDB` do navegador para um armazenamento robusto e assíncrono de logs de chat e configurações.

## Licença

Este projeto é de código aberto e licenciado sob a licença MIT.
