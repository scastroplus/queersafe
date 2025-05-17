# Radar Queer Seguro

## 🏳️‍🌈 Sobre o Projeto

O **Radar Queer Seguro** é uma ferramenta desenvolvida em Python que utiliza o modelo de inteligência artificial Google Gemini em conjunto com a ferramenta de busca do Google para gerar relatórios de segurança e acolhimento para pessoas LGBT+ em diversos destinos ao redor do mundo. O objetivo é fornecer informações recentes e relevantes que ajudem viajantes a tomar decisões informadas sobre a segurança e a experiência em diferentes cidades, estados ou países.

O agente busca informações nos **últimos 6 meses** antes da consulta para garantir a relevância dos dados. Ele sintetiza os achados em um relatório estruturado, incluindo uma pontuação de segurança e a adaptação da linguagem com base na identificação de gênero da pessoa usuária.

## ✨ Funcionalidades

* **Análise Alimentada por IA:** Utiliza o Google Gemini para processar e sintetizar informações.
* **Busca em Tempo Real (Últimos 6 Meses):** Integração com a ferramenta de busca do Google para obter dados recentes.
* **Pontuação de Segurança LGBT+ Friendly:** Gera uma pontuação numérica (0.0 a 5.0) e uma representação visual com emojis de arco-íris (🌈).
* **Relatório Estruturado:** Apresenta as informações em seções claras: Visão Geral, Justificativa da Nota, Alertas de Segurança e Dicas Locais LGBT+.
* **Adaptação de Linguagem por Gênero:** Ajusta a linguagem do relatório com base na identificação de gênero fornecida pela pessoa usuária (masculino, feminino ou neutro).
* **Arquitetura Backend + Frontend:** O projeto é estruturado com um backend em Python (Flask) e um frontend básico em HTML/CSS/JavaScript para uma interface amigável.

## 🛠️ Tecnologias Utilizadas

* **Backend:** Python, Flask, Google Generative AI SDK, Google Search Tool.
* **Frontend:** HTML, CSS, JavaScript.
* **Ferramentas:** Google Gemini API, Google Search Tool API.

## 🚀 Configuração e Execução Local

Siga os passos abaixo para configurar e rodar o Radar Queer Seguro no seu ambiente local.

### Pré-requisitos

* Python 3.7+ instalado.
* `pip` (gerenciador de pacotes do Python).
* Uma chave de API válida do Google Gemini. Você pode obter uma [aqui](https://ai.google.dev/gemini-api/).

### Instalação

1.  Clone este repositório para o seu computador:
    ```bash
    git clone [https://github.com/desktop/desktop/issues/18661](https://github.com/desktop/desktop/issues/18661)
    cd [Nome da pasta do seu repositório]
    ```
2.  Instale as dependências do backend:
    ```bash
    pip install -r requirements.txt
    ```
    (O arquivo `requirements.txt` deve conter as bibliotecas `Flask`, `google-genai`, `requests`, `beautifulsoup4`).

### Configuração da API Key

Você precisa configurar sua chave de API do Google Gemini como uma variável de ambiente chamada `GOOGLE_API_KEY`.

* **Linux/macOS:**
    Abra o terminal e execute:
    ```bash
    export GOOGLE_API_KEY="SUA_CHAVE_AQUI"
    ```
    Para que a variável seja persistente, adicione esta linha ao seu arquivo `~/.bashrc`, `~/.zshrc` ou equivalente e reinicie o terminal.

* **Windows (Prompt de Comando):**
    Abra o Prompt de Comando e execute:
    ```cmd
    set GOOGLE_API_KEY="SUA_CHAVE_AQUI"
    ```
    Para torná-la persistente, use:
    ```cmd
    setx GOOGLE_API_KEY "SUA_CHAVE_AQUI"
    ```
    Você precisará abrir uma nova janela do Prompt de Comando para que a variável seja reconhecida.

* **Windows (PowerShell):**
    Abra o PowerShell e execute:
    ```powershell
    $env:GOOGLE_API_KEY="SUA_CHAVE_AQUI"
    ```
    Para torná-la persistente, você pode precisar adicioná-la às variáveis de ambiente do sistema através da GUI do Windows ou configurar um script de inicialização do PowerShell.

**Substitua `"SUA_CHAVE_AQUI"` pela sua chave de API real.**

### Executando o Backend

1.  No terminal, na pasta do projeto, execute o arquivo principal do backend (assumindo que você o chamou de `app.py`):
    ```bash
    python app.py
    ```
2.  O backend Flask iniciará e você verá uma mensagem indicando em qual endereço ele está rodando (geralmente `http://127.0.0.1:5000/`).

### Usando o Frontend

1.  Com o backend rodando, abra o arquivo `index.html` no seu navegador web (dê um duplo clique no arquivo ou use a opção "Abrir com" no seu navegador).
2.  A interface simples do frontend será carregada.
3.  Preencha os campos "Diga com qual gênero você se identifica:" e "Digite qual cidade, estado ou país você quer conhecer:" e clique no botão "Buscar Relatório".
4.  O frontend enviará os dados para o backend, aguardará a resposta e exibirá o relatório na tela.

## ☁️ Implantação (Para Tornar Acessível Online)

Para tornar o Radar Queer Seguro acessível online para outras pessoas, você precisaria implantar o backend e o frontend em plataformas de hospedagem:

1.  **Backend:** Implante o seu código Python (`app.py`, `requirements.txt`) em uma plataforma que suporte aplicações web Python, como Google Cloud Run, Heroku, PythonAnywhere, etc. Você precisará configurar a variável de ambiente `GOOGLE_API_KEY` na configuração da própria plataforma de hospedagem.
2.  **Frontend:** Implante os seus arquivos HTML, CSS e JavaScript (`index.html`, `style.css`, `script.js`) em uma plataforma de hospedagem de sites estáticos, como GitHub Pages, Netlify, Vercel, etc.
3.  **Conexão:** No arquivo `script.js`, você precisará atualizar a linha `const backendUrl = 'http://127.0.0.1:5000/generate_report';` para a URL real do seu backend hospedado.

Os passos específicos de implantação variam bastante dependendo das plataformas escolhidas.

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais detalhes. (Você pode precisar criar um arquivo LICENSE.md no seu repositório).

## ✨ Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues para reportar bugs ou sugerir melhorias, ou enviar Pull Requests com código.

## Agradecimentos

* Ao Google Gemini pela poderosa API de IA.
* À comunidade de código aberto pelas bibliotecas utilizadas.
