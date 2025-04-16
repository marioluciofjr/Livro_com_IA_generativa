# Livro_com_IA_generativa
Este repositório é para informações do código `gerarLivro.ipynb`

## 📑 Índice

* [Introdução](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#introdu%C3%A7%C3%A3o)
* [Estrutura do Projeto](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#estrutura-do-projeto)
* [Tecnologias Utilizadas](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#tecnologias-utilizadas)
* [Requisitos](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#requisitos)
* [Como obter a API_KEY no Google AI Studio](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#como-obter-a-api_key-no-google-ai-studio)
* [Como configurar a API_KEY no Google Colab](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#como-configurar-a-api_key-no-google-colab)
* [Como Executar](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#como-executar)
* [Orientações](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#orienta%C3%A7%C3%B5es)
* [Links Úteis](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#links-%C3%BAteis)
* [Disclaimer](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#disclaimer-uso-respons%C3%A1vel-e-revis%C3%A3o-humana)
* [Contribuições](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#contribui%C3%A7%C3%B5es)
* [Licença](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#licen%C3%A7a)
* [Contato](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#contato)

## 📝 Introdução

Este projeto utiliza inteligência artificial generativa para superar o bloqueio criativo na escrita de livros. Por meio de três agentes inteligentes (Autor, Editor Literário e Revisor), o sistema gera obras completas sobre qualquer tema. É uma ferramenta poderosa para escritores que precisam de um ponto de partida, professores que desejam criar material didático ou qualquer pessoa com uma ideia de livro mas sem tempo ou habilidade para estruturar o conteúdo. O código automatiza o processo criativo inicial, permitindo que você foque na revisão e personalização do conteúdo.

## 🧩 Estrutura do Projeto

A ideia para este projeto surgiu de um tweet: [@_avichawla](https://x.com/_avichawla/status/1900434649673064753), que demonstrou como diferentes agentes de IA poderiam colaborar para criar conteúdo de qualidade.

O desenvolvimento seguiu o método "vibe coding" (mais detalhes disponíveis na seção de [Links Úteis](https://github.com/marioluciofjr/Livro_com_IA_generativa/tree/main?tab=readme-ov-file#links-%C3%BAteis)), onde o código foi gerado no [Cursor IDE](https://www.cursor.com/) utilizando o modelo Claude 3.7 Sonnet. Para definir os papéis e personalidades dos agentes, utilizei as regras geradas pelo GPT personalizado do CrewAI.

O sistema opera por meio de três agentes especializados em um fluxo sequencial:

1. **Agente Autor**: Responsável pela criação da estrutura inicial e conteúdo do livro
2. **Agente Editor Literário**: Refina e melhora o texto, focando na qualidade narrativa
3. **Agente Revisor**: Realiza a revisão final, garantindo correção gramatical e ortográfica

Cada agente tem sua personalidade, objetivos, regras e expertise definidos, permitindo que colaborem efetivamente para criar um resultado coerente.

O código também inclui a funcionalidade de extrair conteúdo de URLs como referência e salva o livro gerado em formato Markdown para fácil edição posterior.

## 🛠️ Tecnologias Utilizadas

<div>
  <img align="center" height="60" width="80" src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Google_Colaboratory_SVG_Logo.svg" />&nbsp;&nbsp;&nbsp
  <img align="center" height="60" width="60" src="https://raw.githubusercontent.com/lobehub/lobe-icons/refs/heads/master/packages/static-png/light/cursor.png" />&nbsp;&nbsp;&nbsp
  <img align="center" height="60" width="60" src="https://registry.npmmirror.com/@lobehub/icons-static-png/1.44.0/files/dark/aistudio-color.png" />&nbsp;&nbsp;&nbsp
  <img align="center" height="60" width="80" src="https://github.com/user-attachments/assets/1d62c98f-8f78-49d1-b330-901f0f72b4e6" />&nbsp;&nbsp;&nbsp
  <img align="center" height="60" width="80" src="https://github.com/user-attachments/assets/b50a667a-a3cc-4a8c-8cff-83fe5bf9cdd5" />&nbsp;&nbsp;&nbsp;
  <img align="center" height="60" width="80" src="https://github.com/user-attachments/assets/03d84c1b-dba8-490d-b29f-085029eeb1df" />&nbsp;&nbsp;&nbsp;
  <img align="center" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original-wordmark.svg" />&nbsp;&nbsp;&nbsp;
  <img align="center" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/markdown/markdown-original.svg" />&nbsp;&nbsp;&nbsp;
</div>

## 📋 Requisitos

Para utilizar este projeto, você precisa de:

- **Conta Google**: Necessária para acessar o Google AI Studio e o Google Colab
- **Chave de API do Google AI Studio (Gemini API)**: Instruções para obtenção abaixo
- **Bibliotecas**: `google-generativeai`, `beautifulsoup4`, `requests`, `markdown` (instaladas por meio do código)

> [!IMPORTANT]
> O código está configurado para ser executado no Google Colab, que fornece todos os recursos computacionais necessários gratuitamente.

## 🔑 Como obter a API_KEY no Google AI Studio

Para utilizar este código, você precisará de uma chave de API do Google Gemini:

1. Acesse o [Google AI Studio](https://ai.dev/app/apikey)
2. Faça login com sua conta Google
3. Clique no botão "Criar chave de API"
4. Aceite os termos de serviço, se solicitado
5. Copie a chave gerada e guarde-a em local seguro

> [!IMPORTANT]
> Atualmente, o Google AI Studio oferece um uso gratuito da API para testes. Sobre demais detalhes da API do Gemini, leia a [documentação oficial](https://ai.google.dev/gemini-api/docs/pricing?hl=pt-br#:~:text=O%20uso%20do%20Google%20AI,em%20todos%20os%20pa%C3%ADses%20dispon%C3%ADveis)

## 🔐 Como configurar a API_KEY no Google Colab

Para utilizar sua chave API no Google Colab de forma segura:

1. Abra seu notebook no Google Colab
2. Na barra lateral esquerda, clique no ícone 🔑 (Secrets)
3. Clique em "+ Adicionar novo secret"
4. No campo "Nome", digite `sua_api`
5. No campo "Valor", cole sua chave API do Google AI Studio

> [!TIP]
> O código está configurado para acessar a chave por meio de `userdata.get('sua_api')`. Se preferir usar outro nome, modifique esta linha no código: 

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

> [!CAUTION]
> Este sistema foi desenvolvido como uma ferramenta para auxiliar na criação de conteúdo, não para substituir a criatividade humana.

- O conteúdo gerado deve ser considerado como um **ponto de partida** ou um **primeiro rascunho**
- A **revisão humana é essencial** para garantir qualidade, precisão e originalidade
- O sistema serve principalmente para **superar bloqueios criativos** e **acelerar o processo inicial** de escrita
- A **autoria final** e o **olhar crítico** permanecem responsabilidades humanas
- Recomenda-se fortemente uma **revisão completa** por um escritor ou editor humano antes de qualquer publicação

Nenhum modelo de IA generativa, por mais avançado que seja, pode substituir completamente a sensibilidade, experiência e julgamento humanos na criação literária de qualidade.

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
