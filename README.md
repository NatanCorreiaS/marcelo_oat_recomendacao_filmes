## marcelo-oat

Projeto Python com dependências gerenciadas via `pyproject.toml`.

### Requisitos

- Python **3.12+** (ver `requires-python` no `pyproject.toml`)
- `uv` (gerenciador de ambientes e dependências)

### Rodar localmente com `uv`

1) Instale o `uv`

- Linux/macOS:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

- Windows (PowerShell):

```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

2) (Opcional) Garanta um Python 3.12

Se você ainda não tiver Python 3.12 instalado localmente, o `uv` pode instalar:

```bash
uv python install 3.12
```

3) Instale as dependências

Na raiz do projeto:

```bash
uv sync
```

Isso cria/atualiza o ambiente virtual (normalmente em `.venv/`) e instala as dependências definidas no `pyproject.toml`.

4) Execute o programa

```bash
uv run python main.py
```

### Usar no Google Colab

Você pode usar principalmente o notebook `FilmeFlix_Desafio1_Recomendacao.ipynb`.

Observação: este projeto pede **Python 3.12+**. O Colab pode estar em Python 3.10/3.11 dependendo do runtime. Se o seu Colab não estiver em 3.12, prefira rodar o notebook instalando as dependências via `pip` (abaixo).

#### Opção A (mais simples): abrir o notebook e instalar via `pip`

1) Abra o notebook no Colab:
	- Faça upload do arquivo `FilmeFlix_Desafio1_Recomendacao.ipynb` no Colab, ou
	- Se o projeto estiver no GitHub, use **File → Open notebook → GitHub**.

2) Em uma célula no início do notebook, instale as dependências:

```python
!pip -q install numpy pandas scikit-learn scikit-surprise matplotlib seaborn
```

3) Rode as células do notebook normalmente.

#### Opção B: clonar o repositório no Colab e rodar scripts

1) Clone o repositório (se aplicável):

```python
!git clone <URL_DO_REPOSITORIO>
%cd <PASTA_DO_REPOSITORIO>
```

2) Instale as dependências (mesma ideia da opção A):

```python
!pip -q install numpy pandas scikit-learn scikit-surprise matplotlib seaborn
```

3) Execute o script:

```python
!python main.py
```
