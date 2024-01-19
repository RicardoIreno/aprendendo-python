# Python

### Iniciando um projeto
- Arquivos python são módulos python, e tem a extensão `.py`. 
- comando para executar arquivo `python arquivo.py`


## Basics

**Comentários**
```python
# comentário

'''
comentário DocString
'''

```


**Tipos primitivos** 
`str`, `int`, `float` e `bool` 


#### Strings

```python
Michael Jackson	
# | M| i| c| h| a| e| l|  | J| a| c| k| s| o| n|
# | 0| 1| 2| 3| 4| 5| 6| 7| 8| 9|10|11|12|13|14|15|
# |14|13|12|11|10| 9| 8| 7| 6| 5| 4| 3| 2| 1| 0| 1|

name[o:4] // Mich
name[8:12] // Jack

# this is strides
name[::2] # McalJcson (valores pares) 
name[:5:2] # Mca

# some string methods
b = a.upper()
a = "Michael Jackson is the best"
b = a.replace('Michael', 'Janet')
name.find('el') # 5
```

```python
len("Alguma coisa")

3 * "Michael Jackson"
```

##### f strings

```python

string = f'{name} tem {altura:.2f} de altura e {cash:,.2f} reais'


```

##### format

```python
a = 'A'
b = 'B'
c = 1.1

string = 'a={} b={} e c={.2f}'.format(a, b ,c)
```

#### tuples

Tuples are an ordered sequence

```python
tuple1 = ('disco', 10, 1.2)
tuple[0] # "disco"

# you can use negative index

tuple2 = tuple1 + ("hard rock", 10 )
# 'disco', 10, 1.2, "hard rock", 10 

tuple2[0:3]
```



```python
bool(' ') # false
bool('oi') #true
```


https://courses.cognitiveclass.ai/courses/course-v1:CognitiveClass+PY0101EN+v3/courseware/76d637cbe8024e509dc445df847e6c3a/da5e402e18d64a14b8c00a843bd07b75/?child=last



```python
print(r"Hello \"Word")
# r é utilizado para expressões regulares 

print( type('hello world') )

numero = int('10')
```



#### Operadores
```python
2 / 2 # divisão (sempre retorna float)
10 // 2.2 # divisão inteira
55 % 2 # módulo (resto da divisão)

2 ** 10 # exponenciação

print(10 % 8 == 0) # false
print(16 % 8 == 0) # true 


# concatenação
concatenação = 'Tenho' + ' ' + str(5) + ' ' + 'estrelas'

a_dez_vezes = 'A' * 10
```

**Precedência sobre operadores**
1. Parenteses `(n + n)`
2. Exponenciação `**`
3. Multiplicação, divisão, divisão inteira, módulo `*  /  //  %` da esquerda para a direita
4. Adição, subtração `+  -`


```python
'''
1. parenteses: (n + n)
2
'''

```