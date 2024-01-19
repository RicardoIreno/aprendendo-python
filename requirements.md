# Requeriments
**Requeriments são ultrapassados quando se usa o poetry**

### Requeriments
Arquivo **requirements.txt** serve para determinar o que é necessário para rodar o seu projeto.

> pacote pip install pip-autoremove

`pip-automevove` -- remove a biblioteca com todas as biliotecas que ele instalou junto. Não remove dependências cruzadas.

### requirements_dev.txt

Requirements_dev.txt - separar todas as bibliotecas que não são usadas em produção.

``` # instala as libs de produção
-r requirements.txt

# instala as libs de desenvolvimento
black
pytest
...
```

### constransts.txt

Bibliotecas que TEM que estar em uma versão específica.