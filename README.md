# 🧪 Gerador de Testes Unitários com IA

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Flet](https://img.shields.io/badge/UI-Flet-02569B)
![IA](https://img.shields.io/badge/IA-Google%20Gemini-8E75B2?logo=googlegemini&logoColor=white)

Aplicativo **desktop** (interface em [Flet](https://flet.dev/)) que gera
**testes unitários automaticamente** a partir do seu código, usando um modelo de
**IA generativa (Google Gemini)**. O resultado pode ser salvo em **`.txt`** ou **`.pdf`**.

> A ideia é acelerar a escrita de testes: você escolhe o que quer testar (banco de
> dados, função ou valores), a IA analisa e devolve o código de teste pronto para revisar.

---

## ✨ Funcionalidades
- 🖥️ Interface gráfica simples feita com **Flet**.
- 🤖 Geração de testes por **IA** a partir do seu código.
- 🎯 Três modos de análise: **banco de dados**, **função** e **valores**.
- 💾 Exportação do log/resultado em **TXT** ou **PDF**.

---

## 🗂️ Estrutura

| Arquivo | Descrição |
| :--- | :--- |
| `main.py` | Aplicação principal (interface Flet + chamada à IA). |
| `db.py` | Exemplo de código com operações de banco de dados (SQLite). |
| `function_return.py` | Exemplo de função geradora, usada como alvo dos testes. |
| `.env` | **Não versione!** Guarda suas chaves de API (veja abaixo). |

---

## ⚙️ Instalação

Pré-requisito: [Python](https://www.python.org/) 3.10+.

```bash
git clone https://github.com/Ka1ux/LangChain-Azure_ChatGPT_UnitTesting.git
cd LangChain-Azure_ChatGPT_UnitTesting

# (recomendado) ambiente virtual
python -m venv venv
source venv/bin/activate      # Linux/macOS
venv\Scripts\activate         # Windows

pip install flet google-generativeai python-dotenv fpdf
```

---

## 🔑 Configuração da chave de API

Crie um arquivo **`.env`** na raiz do projeto (ele **não deve ir para o Git**):

```env
GEMINI_API_KEY=sua_chave_aqui
GEMINI_API_URL=url_base_da_api
```

Pegue sua chave gratuita no [Google AI Studio](https://aistudio.google.com/app/apikey).

> ⚠️ **Nunca** faça commit do arquivo `.env`. Adicione-o ao `.gitignore`. Se uma
> chave já foi exposta publicamente, **revogue e gere outra** imediatamente.

---

## ▶️ Como usar

```bash
python main.py
```

1. Digite/informe o arquivo ou trecho de código a ser analisado.
2. Escolha o **tipo de teste** (banco de dados, função ou valor).
3. Escolha o **formato do log** (`.txt` ou `.pdf`).
4. Gere os testes e revise o resultado.

---

### 👤 Autor
**Kauã Barroso** · [@Ka1ux](https://github.com/Ka1ux)
