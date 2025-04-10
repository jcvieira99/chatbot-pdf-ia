# 🤖 Chatbot IA com PDFs | Projeto DIO + Azure AI

Este projeto tem como objetivo construir um chatbot inteligente que responde perguntas com base no conteúdo de arquivos PDF. A proposta nasceu de um cenário acadêmico: um estudante de Engenharia de Software que precisa revisar diversos artigos científicos para seu TCC, organizando ideias e cruzando informações de forma eficiente.

---

## 🚀 Visão Geral

Neste desafio, desenvolvemos um sistema interativo capaz de:

- 📄 Ler e interpretar o conteúdo de arquivos PDF
- 🧠 Criar embeddings e realizar buscas vetoriais inteligentes
- 🤖 Gerar respostas contextualizadas usando IA generativa
- 💬 Permitir interação via chat com base no conteúdo dos documentos carregados

---

## 🛠️ Tecnologias Utilizadas

- **Azure AI Foundry** – Para criação e consumo de modelos baseados em IA generativa
- **Azure Cognitive Search** – Para criação de índice vetorial a partir dos documentos
- **Python** – Para manipulação de dados, embeddings e lógica do chatbot
- **FAISS / LangChain / OpenAI API** – Para testes locais e estruturação do fluxo antes de escalar para o Azure
- **Aplicativo Web (opcional)** – Possível implementação com Streamlit ou Flask para visualização

---

## 🧠 Como Funciona

1. **Leitura e Extração de Texto**  
   Os arquivos PDF são carregados e o conteúdo textual é extraído para pré-processamento.

2. **Geração de Embeddings Vetoriais**  
   Utilizamos modelos de linguagem para transformar os trechos dos PDFs em vetores semânticos.

3. **Criação do Índice de Pesquisa no Azure**  
   Com os dados processados, criamos um índice vetorial usando **Azure Cognitive Search** com suporte a embeddings.

4. **Integração com Azure AI para Respostas**  
   Quando o usuário faz uma pergunta, o sistema busca os vetores mais relevantes no índice e usa o modelo da Azure OpenAI para gerar respostas contextualizadas.

5. **Interface de Chat**  
   Um chat interativo permite que o usuário pergunte livremente, obtendo respostas baseadas nos documentos carregados.

---

## 📂 Organização do Projeto

chatbot-pdf-ia/
│
├── inputs/                      # Onde você coloca os arquivos PDF e exemplos de sentenças
│   └── exemplo.txt              # Texto de exemplo extraído dos PDFs
│
├── src/                         # Código-fonte principal
│   ├── ingest.py                # Faz o parsing dos PDFs e gera embeddings
│   ├── chatbot.py               # Interface do chatbot
│   ├── utils.py                 # Funções auxiliares
│   └── config.py                # Configurações e chaves da API
│
├── requirements.txt             # Dependências do projeto
├── README.md                    # Documentação do projeto
└── .gitignore

