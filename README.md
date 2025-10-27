
# AI Math Assistant — Tool Calling com LangChain

Este projeto demonstra como construir um **assistente matemático inteligente** usando **LangChain** e **Tool Calling**, permitindo que um agente de IA resolva problemas matemáticos expressos em linguagem natural.  
O modelo interpreta instruções como “some 25 e 15, depois multiplique por 2” e executa o raciocínio passo a passo para chegar ao resultado correto.

---

## Visão Geral

Este notebook foi desenvolvido como um **lab educacional prático**, mostrando o poder da integração entre **LangChain**, **modelos de linguagem (LLMs)** e **ferramentas matemáticas**.  
A ideia é ensinar como agentes podem **usar raciocínio simbólico** (como somar, subtrair ou multiplicar) a partir de **instruções em texto**.

Durante o lab, o agente:
1. Recebe uma instrução em linguagem natural.
2. Analisa o texto e identifica as operações matemáticas.
3. Usa **tool calling** para invocar funções específicas.
4. Retorna a resposta com o raciocínio detalhado.

---

## Tecnologias Utilizadas

- **Python 3.10+**
- **LangChain** `v0.3.23`
- **LangChain IBM** `v0.3.10`
- **LangChain Community** `v0.3.16`
- **LangChain OpenAI** `v0.3.16`
- **OpenAI SDK** `v1.77.0`
- **Wikipedia** `v1.4.0`
- **IBM watsonx.ai** (modelo `ChatWatsonx`)

---

## Instalação

Clone o repositório:

```bash
git clone https://github.com/<seu-usuario>/AI-Math-Assistant.git
cd AI-Math-Assistant
````

Instale as dependências:

```bash
pip install -r requirements.txt
```

Ou, se preferir, instale manualmente as principais libs:

```bash
pip install langchain==0.3.23 langchain-ibm==0.3.10 langchain-community==0.3.16 langchain-openai==0.3.16 openai==1.77.0 wikipedia==1.4.0
```

---

## Estrutura do Projeto

```text
AI-Math-Assistant/
│
├── AI-Math-Assistant Tool Calling.ipynb  # Notebook principal
├── requirements.txt                      # Dependências do projeto
├── README.md                             # Documentação
└── assets/                               # (opcional) imagens ou diagramas
```

---

## Como Funciona

O fluxo geral do agente é:

1. **Input:** O usuário envia uma pergunta, ex: “qual é 12 vezes (8 + 2)?”
2. **Parsing:** O LLM entende a intenção e divide em operações.
3. **Tool Calling:** O LangChain chama funções Python de soma, subtração, multiplicação etc.
4. **Resposta:** O agente retorna o resultado calculado com explicação.

O notebook também mostra como:

* Configurar um **ChatWatsonx** para usar modelos da IBM.
* Combinar **LLMs** com **ferramentas específicas**.
* Avaliar o comportamento do agente em diferentes cenários.

---

## Exemplos de Uso

Exemplo de prompt:

```text
Pergunta: Quanto é (25 + 15) * 2 ?
Resposta: 80
```

Exemplo de diálogo:

```text
Usuário: some 3, 5 e 7
Assistente: 3 + 5 + 7 = 15 ✅
```

---

## Próximos Passos

* Adicionar novas ferramentas (ex: conversão de unidades, cálculo de porcentagem).
* Integrar com APIs externas para perguntas complexas.
* Criar uma interface web interativa (usando Gradio ou Streamlit).
* Avaliar respostas do modelo com métricas de precisão.

---

## Autor

Projeto baseado em laboratório da **IBM Skills Network**, adaptado e documentado para fins educacionais e práticos.
Mantido por [**@gama18k**](https://github.com/<gama18k>).

