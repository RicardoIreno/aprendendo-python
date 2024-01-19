# Instalação do Python em Linux

Este conteúdo é uma busca de síntese do que eu acho que entendi sobre uma boa maneira de se instalar Python, e claro, necessita de muita melhoria.

## Antes de instalar a bagaça, é uma boa olhar alguns componentes chave do ecossistema Python:

### Gerenciadores de pacotes/bibliotecas
**pip**, Python Install Package. Instala bibliotecas externas do repositório oficial de pacotes Python, o  [Pypip](https://pypi.org).  

Também há o **[pipx](https://github.com/pypa/pipx)**, um gerenciador de pacotes que pacotes globais de forma isolada, uma boa prática. 

O **Conda** que é voltado para o mundo ciêntífico, e que utiliza o [conda-forge](https://conda-forge.org/) como fonte.



### Mais dois tipos de gerenciadores
Instalar pacotes da forma mais simples, direto no sistema, vai bagunçando as coisas e causando conflitos. Uma boa prática na programação Python é utilizar as seguintes ferramentas: 

#### Gerenciador de versões do Python
O **Pyenv** serve para isolar O Python, e suas diferentes versões e interpretadores instalados na máquina. 

#### Gerenciadores de ambientes virtuais
Servem para isolar as dependências do projeto.
O **venv** e o **Virtualenv** , talvez sejam os mais usados no momento em que estou escrevendo isso, e por isso é importante entendê-los. Mais infos deles em [virtualenvs.md](virtualenvs.md) e [requeriments.md](requeriments.md)

No entanto, o **poetry** se mostra promissor simplificando o controle de pacotes.

## Instalação do Python já utilizando o Pyenv. 
Assim, nenhuma versão global padrão é definida, é possível trocar a versão global através do Pyenv.

**Dependências gerais para o ambiente de desenvolvimento**

```bash
sudo apt install git curl build-essential  -y

sudo apt install gcc make default-libmysqlclient-dev libssl-dev -y

sudo apt install -y zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev llvm \
  libncurses5-dev libncursesw5-dev \
  xz-utils tk-dev libffi-dev liblzma-dev python3-openssl git
```


**Instalando o Pyenv**

> [Instruções do repo pyenv-installler](https://github.com/pyenv/pyenv-installer)

**Via curl:**
```
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash  
```
Seguir as instruções do Pyenv. No momento em que escrevo são:


```
# adiciona isso no ~/.bashrc:

export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Restart your shell
```

### Instalação do Python pelo pyenv

`pyenv update`
`pyenv install -l` - lista todas as versões do Pyhton disponíveis para instalação.
`pyenv install 3.XX.XX` - Instalação do python

**Definindo as versões**
`pyenv global 3.xx.xx` - Definindo uma versão do Python no sistema
`pyenv local 3.XX.XX` - define a versão do Python no projeto
`python --version` mostra uma versão instalada.


## Instalando mais ferramentas essenciais

### Instalando o pipx
Instruções do repo https://github.com/pypa/pipx

```
sudo apt update
sudo apt install pipx
pipx ensurepath
```

Mais sobre o [pipx no no packaging-python-org](https://packaging.python.org/pt-br/latest/guides/installing-stand-alone-command-line-tools/)

### Instalando o poetry

> Poetry should always be installed in a dedicated virtual environment to isolate it from the rest of your system.

```bash
pipx install poetry
pipx upgrade poetry
```

**há mais para ser feito aqui
https://python-poetry.org/docs/



***...continua..***