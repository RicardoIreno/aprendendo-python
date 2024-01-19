# INICIANDO UM PROJETO

1. Primeira coisa a pensar quando se inicia um projeto novo: usar a última versão do python possível.  **Pyenv**  é a ferramenta que nos auxilia aqui.

2. Segunda coisa é definir a ferramenta para gerenciar o ambiente virtual. O **poetry** trás vantagens de organização sobre o venv, virtualenv e o pipenv.

```bash

poetry new nome-do-projeto

```

Um arquivo `pyproject.toml`é criado. Esse arquivo documenta infos básicas do projeto e pacotes usados.

Eu quero adicionar o pacote pytest como ferramenta de desenvolvimento no projeto

```

poetry add --group dev pytest

```

continua...
https://python-poetry.org/docs/basic-usage/

..