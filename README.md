# Biblioteca LangChain

Este repositório tem como foco a realização de experimentos com a biblioteca LangChain para criar aplicativos poderosos usando modelos de LLM (Large Language Models).

O LangChain é um framework abrangente desenvolvido para a criação de aplicativos alimentados por modelos de linguagem. Ele vai além do simples uso desses modelos por meio de uma API, 
permitindo que os aplicativos tenham consciência dos dados e possam interagir com outras fontes de dados e o ambiente.

## LangChain

A parte referente ao Python na documentação do LangChain abrange vários módulos principais, cada um fornecendo exemplos, guias de como fazer, documentação de referência e guias conceituais. Tais módulos incluem:

1. **Modelos**: Este módulo aborda diversos tipos de modelos e integrações de modelos que são suportados pelo LangChain.
2. **Prompts**: Neste módulo, você encontrará informações sobre o gerenciamento, otimização e serialização de prompts, que são usados para interagir com os modelos de linguagem.
3. **Memória**: Aqui, a persistência de estado entre chamadas de cadeia ou agente é explicada. Isso inclui uma interface de memória padrão, implementações de memória e exemplos de como cadeias e agentes podem utilizar a memória para armazenar informações.
4. **Índices**: Esse módulo aborda a combinação de LLMs (Large Language Models) com dados de texto personalizados para aprimorar suas capacidades. Isso pode incluir a criação de índices para consultas eficientes.
5. **Cadeias**:  Este módulo se concentra em sequências de chamadas, que podem ser direcionadas a um LLM ou a uma utilidade diferente. Ele inclui informações sobre uma interface padrão, integrações e exemplos de como usar cadeias de chamadas do início ao fim.
6. **Agentes**: Neste último módulo, são discutidos os agentes que são baseados em LLMs. Eles tomam decisões sobre ações, observam os resultados e repetem o processo até a conclusão. A documentação inclui detalhes sobre a interface padrão, a seleção de agentes e exemplos de agentes de ponta a ponta.

## Casos de Uso
Com o LangChain, é possível fornecer soluções personalizadas que atendam às suas necessidades específicas. Por exemplo, as empresas podem se beneficiar de chatbots personalizáveis que lidam com consultas de clientes, 
ferramentas de criação de conteúdo personalizado para marketing ou sistemas internos de análise de dados que aproveitam o poder dos LLMs para extrair insights valiosos. As possibilidades são amplas e o framework flexível do 
LangChain o torna a escolha ideal para desenvolver e implementar aplicativos avançados de modelos de linguagem em diversas indústrias. Isso pode ajudar as empresas a melhorar a eficiência, oferecer experiências aprimoradas aos 
clientes e obter vantagem competitiva.

## Requisitos

- [Python 3.6 ou superior](https://www.python.org/downloads/)
- [Biblioteca LangChain](https://python.langchain.com/en/latest/index.html)
- [Chave de API da OpenAI](https://platform.openai.com/)
- [Chave de API SerpAPI](https://serpapi.com/)


## Instalação

#### 1. Clonar o repositório

```bash
git clone https://github.com/daveebbelaar/langchain-experiments.git
```

#### 2. Criar um ambiente Python
Python 3.6 ou superior usando `venv` ou `conda`. Usando `venv`:
```bash
cd langchain-experiments
python3 -m venv env
source env/bin/activate
```

Usando `conda`:
```bash
cd langchain-experiments
conda create -n langchain-env python=3.8
conda activate langchain-env
```
#### 3. Instalar as dependências necessárias
```bash
pip install -r requirements.txt
```
#### 4. Configurar as chaves em um arquivo .env
Primeiro, crie um arquivo `.env` na raiz do projeto. Dentro do arquivo, adicione sua chave de API da OpenAI:
```bash
OPENAI_API_KEY="sua_chave_api_aqui"
```

Salve o arquivo e feche-o. Em seu script Python ou notebook Jupyter, carregue o arquivo .env usando o seguinte código:
```bash
from dotenv import load_dotenv, find_dotenv
load_dotenv(find_dotenv())
```

Usando a convenção de nomenclatura correta para a variável de ambiente, você não precisa armazenar manualmente a chave em uma variável separada e passá-la para a função. 
A biblioteca ou pacote que requer a chave da API reconhecerá automaticamente a variável de ambiente `OPENAI_API_KEY` e usará seu valor.

Quando necessário, você pode acessar a `OPENAI_API_KEY` como uma variável de ambiente:
```bash
import os
api_key = os.environ['OPENAI_API_KEY']
```


