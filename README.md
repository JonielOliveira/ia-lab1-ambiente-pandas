# IA – Laboratório 1: Ambiente com Pandas

Repositório dedicado ao Laboratório 1 da matéria de Inteligência Artificial (IA), do curso de ADS da FATEC.

## Propósito

O objetivo deste laboratório é apenas criar um ambiente Python funcional com Pandas. A validação do ambiente é feita pelo notebook `lab/main.ipynb`, que deve ser executado para confirmar que as dependências foram instaladas corretamente.

## Estrutura do projeto

```text
.
+-- docs/
+-- lab/
|   +-- .python-version
|   +-- main.ipynb
|   +-- main.py
|   +-- pyproject.toml
|   +-- uv.lock
+-- README.md
```

## Pré-requisitos

- Python 3.12 ou superior
- uv instalado

Para instalar o `uv`, consulte a documentação oficial: https://docs.astral.sh/uv/getting-started/installation/

## Como executar após clonar o repositório

Clone o repositório e entre na pasta do projeto:

```bash
git clone <url-do-repositorio>
cd ia-lab1-ambiente-pandas
```

Entre na pasta do laboratório:

```bash
cd lab
```

Instale as dependências a partir do `uv.lock`:

```bash
uv sync
```

Esse comando cria o ambiente virtual local em `lab/.venv/` e instala as dependências do projeto, incluindo Pandas, Seaborn e IPython Kernel.

## Teste do ambiente

Para fazer uma validação rápida pelo terminal, execute:

```bash
uv run python main.py
```

Para validar pelo notebook no navegador, abra o Jupyter com o ambiente do projeto:

```bash
uv run --with notebook jupyter notebook
```

No navegador, abra o arquivo `main.ipynb` e execute as células. Se o notebook rodar sem erros, o ambiente Python com Pandas está funcionando corretamente.

Se estiver usando VS Code, também é possível abrir `lab/main.ipynb` diretamente e selecionar o kernel do ambiente `.venv` criado pelo `uv sync`.

## Observações

- O ambiente virtual `.venv/` não deve ser versionado.
- O arquivo `uv.lock` deve ser mantido no repositório para garantir que outras pessoas instalem as mesmas versões das dependências.
- Sempre execute os comandos do projeto a partir da pasta `lab/`.
