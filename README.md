# Chatbot-com-Gemini-API-no-Google-Colab

# 🤖 Google Generative AI SDK - Exemplo de Uso com Gemini 1.0 Pro

Este projeto demonstra como instalar e utilizar o SDK da Google Generative AI para gerar conteúdo usando o modelo **Gemini 1.0 Pro**. O exemplo é executado em um ambiente como o Google Colab e utiliza uma chave de API armazenada de forma segura.

🔐 Autenticação
A autenticação é feita por meio de uma chave de API armazenada em um ambiente seguro no colab:

from google.colab import userdata
api_key = userdata.get('SECRET_KEY')

Configure o SDK com a chave:

import google.generativeai as genai
genai.configure(api_key=api_key)

📋 Listando Modelos Disponíveis
 Lista os modelos disponíveis e verificar quais suportam o método generateContent:

for m in genai.list_models(): 
  if 'generateContent' in m.supported_generation_methods:
    print(m.name)

⚙️ Configurações de Geração
Define parâmetros para controlar a geração de conteúdo:

generation_config = {
    "candidate_count": 1,
    "temperature": 0,5,
}

🛡️ Configurações de Segurança
Você pode ajustar os filtros de segurança conforme o necessário:

safety_settings = {
    "HARASSMENT": "block_none",
    "HATE": "block_none",
    "SEXUAL": "block_none",
    "DANGEROUS": "block_none",
}

🧠 Inicializando o Modelo
Crie uma instância no modelo Gemini 1.0 Pro com as configurações definidas:

model = genai.GenerativeModel(
    model_name="gemini-1.0-pro"
    generation_config=generation_config,
    safety_settings=safety_settings
)

✨ Gerando Conteúdo
Solicite ao modelo sugestões sobre Inteligência Artificial:

response = model.generative_content("Vamos aprender conteúdos sobre IA. Me dê sugestões. ")
print(response.text)

📎 Requisito
- Python 3.7+
- Ambiente compatível com Google Colab
- Chave de API válida da Google Generative AI

📘 Licença
Esse projeto é apenas um exemplo educacional e não possui licença específica. Para uso comercial, consulte os termos [Google Generative AI](https://ai.google.dev/).

💬 Contato
Para dúvidas ou sugestões, sinta-se a vontade para abrir uma issue ou contribuir com melhorias!



---

## 🚀 Instalação

Para instalar o SDK da Google Generative AI, execute

```python
!pip install -q -U google-generativeai





Geração de conteúdo criativo com o Google Gemini;
Resolução de problemas complexos;
Assistência em tarefas do dia a dia;
Integração com sistemas já existentes;
Leitura e reconhecimento de imagens, áudios e vídeos;
O que é IA Generativa;
Ética e Inteligência Artificial (IA);
Inteligência Artificial aplicada;
Guia para iniciar na linguagem Python;
Machine Learning;
Deep Learning;
Como gerar uma API KEY.



