# 🧠 MutationForge — Guia 

Esse projeto é uma extensão do Sistema ExamForge (https://github.com/Gabriel-marques-araujo/ExamForge).

O objetivo é utilizar um sistema RAG consistente para validar benchmarks de testes aplicados a sistemas RAG e LLMs. Além disso, a proposta visa introduzir mutações propositais no sistema, permitindo avaliar a eficácia dos benchmarks na identificação de falhas e na mensuração da robustez e confiabilidade desses sistemas.

### 📥 1. Clonar o Repositório

```bash
git clone https://github.com/Gabriel-marques-araujo/ExamForge.git
```

-----

### 📁 2. Configuração do Backend

Primeiro, acesse a pasta do backend:

```bash
cd ExamForge/backend
```

#### 🌱 3. Criar o Ambiente Virtual

Escolha o comando de acordo com o seu sistema operacional:

  * **🪟 Windows:**

    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

  * **🐧 Linux / Mac:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

#### 📦 4. Instalar as Dependências

Com o ambiente virtual ativado, execute:

```bash
pip install -r requirements.txt
```

#### 🔑 5. Configurar Variáveis de Ambiente (.env)

> **Importante:** Para que o sistema funcione corretamente, você deve criar um arquivo chamado `.env` dentro da pasta `backend`.

Abra este arquivo e adicione a seguinte linha (substituindo pelo valor real da sua chave):

```env
GOOGLE_GEMINI_KEY=sua chave aqui
```

#### ▶️ 6. Rodar o Backend

Inicie o servidor localmente:

```bash
uvicorn main:app --reload
```

O backend estará disponível em: `http://127.0.0.1:8000`

-----

### 🎨 7. Configuração do Frontend

Abra um **novo terminal** para não fechar o backend e navegue até a pasta do frontend:

```bash
cd ExamForge/frontend
```

> ⚠️ **Nota:** É necessário ter o [Node.js](https://nodejs.org/) instalado em sua máquina.

#### Instalar dependências:

```bash
npm install
```

#### Executar o frontend:

```bash
npm run dev
```

A interface abrirá em um endereço semelhante a: `http://localhost:5173`

-----

### 🔍 8. Como Testar o Sistema

Para testar o fluxo completo corretamente:

1.  Mantenha o **Backend** rodando em um terminal.
2.  Mantenha o **Frontend** rodando em outro terminal.

**Fluxo de funcionamento:**
Frontend envia requisições ➡️ Backend processa (usando a API Key configurada) ➡️ Resposta aparece na tela.

