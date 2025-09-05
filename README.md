Luke - Seu Assistente Pessoal de RAG
Este projeto é um assistente de chatbot pessoal, carinhosamente chamado Luke, construído com a plataforma de automação n8n. Luke foi projetado para analisar e responder a perguntas com base no conteúdo de documentos armazenados em seu Google Drive. Utilizando a arquitetura RAG (Generation Augmented Retrieval), Luke garante que suas respostas sejam precisas e relevantes, recuperando informações diretamente da fonte.

🚀 Funcionalidades
Análise de documentos: Luke pode ler e entender o conteúdo de documentos no Google Drive.

Respostas inteligentes: Ele fornece respostas informadas e diretas a perguntas, aproveitando o poder do Google Gemini.

Atualização automática: Os documentos são processados e indexados automaticamente sempre que um novo arquivo é criado ou um existente é atualizado em sua pasta designada do Google Drive.

Armazenamento de vetores: O Pinecone é usado para armazenar representações vetoriais dos seus documentos, permitindo buscas semânticas rápidas e eficientes.

⚙️ Configuração
Para que Luke funcione perfeitamente, você precisará configurar os seguintes serviços e credenciais:

1. Google Cloud e Vertex AI API
Crie um projeto no Google Cloud.

Ative a Vertex AI API para o seu projeto.

2. Chave de API do Google AI
Obtenha uma chave de API do Google AI Studio.

3. Pinecone
Crie uma conta gratuita no Pinecone.

Obtenha sua chave de API no painel.

Crie um índice chamado company-files no seu projeto do Pinecone.

4. Google Drive
Crie uma pasta dedicada no seu Google Drive, onde você irá armazenar todos os documentos que Luke deve analisar.

5. Credenciais no n8n
No seu ambiente n8n, configure as credenciais para:

Google Drive OAuth2

Google Gemini (PaLM) Api (usando sua chave de API do Google AI)

Pinecone API (usando sua chave de API do Pinecone)

6. Importe o fluxo de trabalho no n8n
Importe o arquivo rag-chatbot.json para o seu n8n.

7. Configure o fluxo de trabalho
Atualize os nós Google Drive Trigger para monitorar a pasta que você criou no seu Google Drive.

Configure os nós Pinecone Vector Store para usar o seu índice company-files.

🤝 Contribuições
Este projeto foi desenvolvido por Mihai Farcas em https://n8n.io/workflows/2753-rag-chatbot-for-company-documents-using-google-drive-and-gemini/ . Fiz minhas adaptações.
