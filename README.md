# Livro_com_IA_generativa
Este repositório é para informações do código `gerarLivro.ipynb`

## 📑 Índice

* [Introdução](#introdução)
* [Estrutura do Projeto](#estrutura-do-projeto)
* [Tecnologias Utilizadas](#tecnologias-utilizadas)
* [Requisitos](#requisitos)
* [Como obter a API_KEY no Google AI Studio](#como-obter-a-api_key-no-google-ai-studio)
* [Como configurar a API_KEY no Google Colab](#como-configurar-a-api_key-no-google-colab)
* [Como Executar](#como-executar)
* [Orientações](#orientações)
* [Links Úteis](#links-úteis)
* [Disclaimer](#disclaimer-uso-responsável-e-revisão-humana)
* [Contribuições](#contribuições)
* [Licença](#licença)
* [Contato](#contato)

## índice

* [Introdução](#introdução)
* [Resultado](#resultado)
* [Estrutura do projeto](#estrutura-do-projeto)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Links úteis](#links-úteis)
* [Contato](#contato)

## 📝 Introdução

Este projeto utiliza inteligência artificial para superar o bloqueio criativo na escrita de livros. Por meio de três agentes especializados (Autor, Editor Literário e Revisor), o sistema gera obras completas sobre qualquer tema. É uma ferramenta poderosa para escritores que precisam de um ponto de partida, professores que desejam criar material didático ou qualquer pessoa com uma ideia de livro mas sem tempo ou habilidade para estruturar o conteúdo inicial. O código automatiza o processo criativo inicial, permitindo que você foque na revisão e personalização do conteúdo.

## 🧩 Estrutura do Projeto

A ideia para este projeto surgiu de um tweet inspirador: [@_avichawla](https://x.com/_avichawla/status/1900434649673064753), que demonstrou como diferentes especialistas de IA poderiam colaborar para criar conteúdo de alta qualidade.

O desenvolvimento seguiu o método "vibe coding" (mais detalhes disponíveis na seção de [Links Úteis](#links-úteis)), onde o código foi gerado no [Cursor IDE](https://www.cursor.com/) utilizando o modelo Claude 3.7 Sonnet. Para definir os papéis e personalidades dos agentes, utilizei as regras geradas pelo GPT personalizado do CrewAI.

O sistema opera por meio de três agentes especializados em um fluxo sequencial:

1. **Agente Autor**: Responsável pela criação da estrutura inicial e conteúdo do livro
2. **Agente Editor Literário**: Refina e melhora o texto, focando na qualidade narrativa
3. **Agente Revisor**: Realiza a revisão final, garantindo correção gramatical e ortográfica

Cada agente tem sua personalidade, objetivos e expertise definidos, permitindo que colaborem efetivamente para criar um resultado superior ao que qualquer um deles conseguiria individualmente.

O código também inclui a funcionalidade de extrair conteúdo de URLs como referência, e salva o livro gerado em formato Markdown para fácil edição posterior.

## 🛠️ Tecnologias Utilizadas

<div>
  <img align="center" height="60" width="80" src="https://www.gstatic.com/images/branding/product/1x/colab_48dp.png" alt="Google Colab" />
  <img align="center" height="60" width="80" src="https://cursor.sh/apple-touch-icon.png" alt="Cursor IDE" />
  <img align="center" height="60" width="80" src="https://lh3.googleusercontent.com/HuPZAKGp08rLAno_OdwkRZCKW8SWnIZMXzBhLZ7G4JF-5qhEbU_t3QHw-bAZ-qVPeA5J-qYi7zw=e14-rj-sc0xffffff-h130-w32" alt="Google AI Studio" />
  <img align="center" height="60" width="80" src="https://www.anthropic.com/images/favicon.ico" alt="Claude" />
  <img align="center" height="60" width="80" src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Google_Gemini_logo.svg" alt="Gemini" />
  <img align="center" height="60" width="80" src="https://www.svgrepo.com/show/306500/openai.svg" alt="ChatGPT" />
  <img align="center" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" alt="Python" />
  <img align="center" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/markdown/markdown-original.svg" alt="Markdown" />
  <img align="center" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/beautifulsoup/beautifulsoup-original.svg" alt="BeautifulSoup" />
</div>

## 📋 Requisitos

Para utilizar este projeto, você precisa de:

- **Conta Google**: Necessária para acessar o Google AI Studio e o Google Colab
- **Chave de API do Google AI Studio (Gemini API)**: Instruções para obtenção abaixo
- **Bibliotecas**: google-generativeai, beautifulsoup4, requests, markdown (instaladas automaticamente pelo código)

> **Importante**: O código está configurado para ser executado no Google Colab, que fornece todos os recursos computacionais necessários gratuitamente.

## 🔑 Como obter a API_KEY no Google AI Studio

Para utilizar este código, você precisará de uma chave de API do Google Gemini:

1. Acesse o [Google AI Studio](https://ai.dev/app/apikey)
2. Faça login com sua conta Google
3. Clique no botão "Criar chave de API"
4. Aceite os termos de serviço, se solicitado
5. Copie a chave gerada e guarde-a em local seguro

> **Importante**: Atualmente, o Google AI Studio oferece um uso gratuito da API para testes. Sobre demais detalhes da API do Gemini, leia a [documentação oficial](https://ai.google.dev/gemini-api/docs/pricing?hl=pt-br#:~:text=O%20uso%20do%20Google%20AI,em%20todos%20os%20pa%C3%ADses%20dispon%C3%ADveis)

## 🔐 Como configurar a API_KEY no Google Colab

Para utilizar sua chave API no Google Colab de forma segura:

1. Abra seu notebook no Google Colab
2. Na barra lateral esquerda, clique no ícone 🔑 (Secrets)
3. Clique em "+ Adicionar novo secret"
4. No campo "Nome", digite `sua_api`
5. No campo "Valor", cole sua chave API do Google AI Studio

O código está configurado para acessar a chave por meio de `userdata.get('sua_api')`. Se preferir usar outro nome, modifique esta linha no código: 

```python
# Método 1: Usar chave armazenada no Google Colab
        API_KEY = userdata.get('sua_api')
```

## 🚀 Como Executar

- [ ] Obter a API_KEY no Google AI Studio
- [ ] Clicar no botão 'Open in Colab' dentro do arquivo 'gerarLivro.ipynb'
- [ ] Configurar a API_KEY em 'Secrets' no Google Colab
- [ ] Executar o primeiro bloco do código (instalações)
- [ ] Executar o segundo bloco do código (importações)
- [ ] Executar o terceiro bloco de código e preencher os inputs solicitados:
  - Tema do livro
  - Número de capítulos
  - Tom de voz desejado
  - Contexto e detalhes adicionais
  - URL de referência (opcional)
- [ ] Executar o quarto bloco do código

```python
start_time = time.time()
livro()
end_time = time.time()

elapsed_time = end_time - start_time
minutes, seconds = divmod(elapsed_time, 60)
centiseconds = (seconds - int(seconds)) * 100

print(f"Livro gerado em: {int(minutes)} minutos, {int(seconds)} segundos e {int(centiseconds)} centésimos")
```

## 📚 Orientações

Após a execução bem-sucedida, o livro gerado será:

1. Exibido na saída do Colab (apenas o primeiro capítulo como amostra)
2. Salvo na pasta `livro_pronto` no ambiente do Google Colab

Para acessar os arquivos gerados:
- Na barra lateral esquerda do Colab, clique no ícone 📁 (Arquivos)
- Navegue até a pasta `livro_pronto`
- Você verá os arquivos markdown de cada capítulo e a estrutura completa do livro
- Faça o download dos arquivos clicando com o botão direito e selecionando "Fazer download"

Os arquivos serão salvos em formato Markdown (.md), que pode ser facilmente convertidos para outros formatos ou mesmo utilizados no Google Docs e/ou Notion

## 🔗 Links Úteis

- [O que é vibe coding?](https://medium.com/@niall.mcnulty/vibe-coding-b79a6d3f0caa) - Explica como programar descrevendo o que você quer em linguagem natural
- [GPT personalizado do CrewAI](https://chatgpt.com/g/g-qqTuUWsBY-crewai-assistant) - Ajuda a definir papéis e personalidades para agentes de IA
- [O que são agentes de IA?](https://www.ibm.com/br-pt/think/topics/ai-agents) - Explicação da IBM sobre agentes inteligentes de IA
- [GPT personalizado do método LACJ](https://chatgpt.com/g/g-67f14c0f87f88191a15eb164efa7dc67-metodo-lacj) - Método para estruturar conteúdo didático e evitar bloqueio criativo
- [Artigo sobre 'Prompt Design Thinking'](https://www.linkedin.com/posts/marioluciofjr_promptdesign-ai-designthinking-activity-7315365303582900224-H7rE) - Como estruturar prompts eficientes a partir do 'Design Thinking'
- [Como funciona o Cursor?](https://hub.asimov.academy/blog/cursor-ide-com-ia/) - Guia sobre o IDE que facilita programação com IA
- [Tudo sobre o Secrets do Google Colab](https://medium.com/@parthdasawant/how-to-use-secrets-in-google-colab-450c38e3ec75) - Tutorial completo sobre armazenamento seguro
- [O que é uma API?](https://www.alura.com.br/artigos/api) - Guia da Alura sobre APIs

## ⚠️ Disclaimer: Uso responsável e revisão humana

> **Importante**: Este sistema foi desenvolvido como uma ferramenta para auxiliar na criação de conteúdo, não para substituir a criatividade humana.

- O conteúdo gerado deve ser considerado como um **ponto de partida** ou um **primeiro rascunho**
- A **revisão humana é essencial** para garantir qualidade, precisão e originalidade
- O sistema serve principalmente para **superar bloqueios criativos** e **acelerar o processo inicial** de escrita
- A **autoria final** e o **olhar crítico** permanecem responsabilidades humanas
- Recomenda-se fortemente uma **revisão completa** por um escritor ou editor humano antes de qualquer publicação

Nenhum sistema de IA, por mais avançado que seja, pode substituir completamente a sensibilidade, experiência e julgamento humanos na criação literária de qualidade.

## 🤝 Contribuições

Contribuições são bem-vindas! Se você tem ideias para melhorar este projeto, sinta-se à vontade para fazer um fork do repositório.

## 📄 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](https://github.com/marioluciofjr/Livro_com_IA_generativa/blob/main/LICENSE) para detalhes.

## 📬 Contato

Mário Lúcio - Prazo Certo®
<div>  	
  <a href="https://www.linkedin.com/in/marioluciofjr" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> 
  <a href = "mailto:marioluciofjr@gmail.com" target="_blank"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://prazocerto.me/contato" target="_blank"><img src="https://img.shields.io/badge/prazocerto.me/contato-230023?style=for-the-badge&logo=wordpress&logoColor=white"></a>
</div> 
