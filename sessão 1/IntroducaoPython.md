# Introdução á inguagem Phython

# Tipo Basicos

## Numeros inteiros
``` python
10
```
``` python
print(10)
```

### Numero Flutuantes
``` python
print(3.14)
```

## Strings
``` python
print('Olá Mundo!')
```
``` python
print("Olá Mundo!")
```
``` python
print('O Gabriel tem', 40,'anos de idade')
```

## Booleanos
``` python
print(True)
```
``` python
print(False)
```

# Variáveis e atribuição Simples
``` python
nome = 'Gabriel'
```
``` python
idade = 40
```
``` python
altura = 1.65
```

## Exibir os valores das Variaveis
``` python
print('Nome:',nome)
```
``` python
print('Idade:',idade)
```
``` python
print('Altura:',altura)
```

## Alterar o valor das Variáveis
``` python
nome = 'Arthur'
```
``` python
idade = 14
```
``` python
altura = 1.72
```
``` python
print('Nome:',nome)
```
``` python
print('Idade:',idade)
```
``` python
print('Altura:',altura)
```

## Regras Nomenclatura
[x] Não pode começar por numeros
``` python
7nome = 'Gabriel'
```
[x] Não pode ter espaços

``` python
nome completo = 'Gabriel'
```
[x] Não pode ser um nome reservado de uma função  da linguagem

``` python
print = 100
```
[x] As variaveis em Phython são case sensitive
[x] As variaveis são dinâmicas isto é um posso alterar de um string para um inteiro
[x] tipo ```None``` é um tipo null

# Operdores Matemáticos
-  Adição ```+```
``` python
10+5
```
``` python
n1 = 10
n2 = 5
resultado = n1 + n2
print(n1,"+",n2,"=",resultado)
```
-  Subtração ```-```
``` python
n1 = 10
n2 = 5
resultado = n1 - n2
print(n1,"-",n2,"=",resultado)
```
- Multiplicação ```*```
``` python
n1 = 10
n2 = 5
resultado = n1 * n2
print(n1,"*",n2,"=",resultado)
```
-  Divisão ```/```
``` python
n1 = 10
n2 = 5
resultado = n1 / n2
print(n1,"/",n2,"=",resultado)
```
- Retorna o resto ```%```
``` python
n1 = 10
n2 = 5
resultado = n1 % n2
print(n1,"%",n2,"=",resultado)
```
- Potencia ```**```
``` python
n1 = 10
n2 = 5
resultado = n1 ** n2
print(n1,"**",n2,"=",resultado)
```
- Retorna apena a parte inteira da divisão ```//```
``` python
n1 = 10
n2 = 5
resultado = n1 // n2
print(n1,"//",n2,"=",resultado)
```
**Nota:** *As operação em python seguem as mesmas regras que as orações matemáticas*
``` python
# Vai dar erro
print( 10 / 0)
```

## Ordem das Operações Matemáticas
A ordem matemática em python segue as mesmas regras da matemática
### Exemplos:
``` python
print(1 + 2 * 3)

# OutPut
# 7
```
``` python
print((1 + 2) * 3)

# OutPut
# 9
```
``` python
print((1 + 2) * 3 + 2)

# OutPut
# 11
```
``` python
print((1 + 2) * (3 + 2))

# OutPut
# 15
```
# Concatenação de string
``` python
nome = 'Gabriel ' + 'Artigas'

print(nome)

# OutPut
# Gabriel Artigas
```
``` python
nome = 'Gabriel'
sobrenome = 'Artigas'

nome_completo = nome + " " + sobrenome

print(nome_completo)

# OutPut
# Gabriel Artigas
```
# Conversão de tipos de dados
``` python
n1 = 10
n2 = 20

print( n1 + n2)

# OutPut
# 30
````
Mas ...
``` python
n1 = "10"
n2 = "20"

print( n1 + n2)

# OutPut
# 1020
````
Porem ...
``` python
n1 = "10"
n2 = 20

print( n1 + n2)

# OutPut
# TypeError: can only concatenate str (not "int") to str
```
Solução:
``` python
n1 = "10"
n2 = 20

print(int(n1) + n2)

# OutPut
# 30
```
- A função ```int()``` converte strings em inteiros
    - **Nota:** A string têm que ser convertivel para Inteiro
``` python
n1 = int("ABC")
n2 = 20

print(n1 + n2)

# OutPut
# ValueError: invalid literal for int() with base 10: 'ABC'
```
- A função ```str()``` serve para converter para string
- A função ```float()``` serve para converter para float
- A função ```bool()``` serve para converter para booleano
## Caractristicas dos retornos de conversão de tipos
``` python
n1 = 0
n2 = 0.0
verdadeiro = True
texto = "Python"
```
``` python
# Converter para string

print(str(n1)) # '0'
print(str(n2)) # '0.0'
print(str(verdadeiro)) # 'true'
print(str(texto)) # 'Python'
```
``` python
# Converter para inteiro

print(int(n1)) # 0
print(int(n2)) # 0
print(int(verdadeiro)) # 1
print(int(texto)) # ValueError: invalid literal for int() with base 10: 'Python'
```
``` python
# Converter para o tipo float

print(float(n1)) # 0.0
print(float(n2)) # 0.0
print(float(verdadeiro)) # 1.0
print(float(texto)) # ValueError: could not convert string to float: 'Python'
```
``` python
# Conversão parao tipo booleano

print(bool(n1)) # False
print(bool(n2)) # False
print(bool(verdadeiro)) # True
print(bool(texto)) # True
```
# Metodo de entrada de dados (input)
O ```print()``` é um método de saída, isto porque mostra-nos o resultado de algo

O metodo ```input()``` vai abrir o prompt de comandos para que o utilizador possa escrever alguma imformação
``` python
input()
```
``` python
input('Digite seu nome: ')
```
Guaradar o valor numa variavel:
``` python
nome = input('Digite seu nome: ')

print('Olá',nome,'Seja bem-vindo(a)!')
```
O metodo ```input()``` devolve uma string então pode haver a necessidade de o converter:
``` python
nome = input('Digite seu nome: ')
ano = 2026

nascimento = input('Digite o seu ano de nascimento: ')

print('Olá',nome,'voce tem',ano - int(nascimento),'anos de idade.')
```
# Operadores de Comparação
-  Verifica se o operador do lado esquerdo é **igual** ao operador do lado direito ```==```
``` python
a = 5
b = 10

resultado = a == b

print(resultado)

# OutPut
# False

resultado = a * 2 == b

print(resultado)

# Output
# True
``` 
- Verifica se o operador da esquerda é **diferente** do operador da direita ```!=```
``` python
a = 5
b = 10

resultado = a != b

print(resultado)

# OutPut
# True
```
- Verifica se o operador da esquerda é **maior que** o operador da direita ```>```
``` python
a = 5
b = 10

resultado = a > b

print(resultado)

# OutPut
# False
```
- Verifica se o operador da esquerda é **menor que** o operador da direita ```<```
``` python
a = 5
b = 10

resultado = a < b

print(resultado)

# OutPut
# True
```
- Verifica se o operador da esquerda é **maior ou igual** que o operador da direita ```>=```
``` python
a = 5
b = 10

resultado = a >= b

print(resultado)

# OutPut
# False
```
- Verifica se o operador da esquerda é **menor ou igual** ao operador da direita ```<=```
``` python
a = 5
b = 10

resultado = a <= b

print(resultado)

# OutPut
# True
```
# Operadores Lógicos
São ussados para combinar expressões booleanas.

Exemplos:
- Operador ```and```, só retorna ```True``` se **ambos os lados** forem ```True```
``` python
idade = 20

# A pessoa é maior de idade?
print(idade >= 18)
```
1ª situação:
``` python
# A pessoa pode dirigir?
tem_carta = True

print('A Pessoa pode dirigir?',idade >= 18 and tem_carta)

# OutPut
# A Pessoa pode dirigir? True
```
2ª situação:
``` python
# A pessoa pode dirigir?
tem_carta = False

print('A Pessoa pode dirigir?',idade >= 18 and tem_carta)

# OutPut
# A Pessoa pode dirigir? False
```
- Operador ```or```, retorna ```True``` se **pelo menos um** dos lados for ```True```
``` python
idade = 17
```
1ª situação:
``` python
acompanhado = True

print('Pode entrar no evento?', idade >= 18 or acompanhado)

# OutPut
# Pode entrar no evento? True
```
2ª situação:
``` python
acompanhado = False

print('Pode entrar no evento?', idade >= 18 or acompanhado)

# OutPut
# Pode entrar no evento? False
```
3ª situação:
``` python
idade = 21
acompanhado = False

print('Pode entrar no evento?', idade >= 18 or acompanhado)

# OutPut
# Pode entrar no evento? True
```
- Operador ```not``` ele **inverte o resultado** de uma verificação booleana
``` python
trabalhando = True

print('Pode passear?',not trabalhando)

# OutPut
# Pode passear? False
```
# Operadores de atribuição composta
Exemplo:
``` python
a = 10

a += 2 # em vez de a = a + 2

print(a)

# OutPut
# 12
```
```a = a += 2``` significa que a vai receber o seu proprio valor somando 2
``` python
a = 10

a -= 2 # em vez de a = a - 2

print(a)

# OutPut
# 8
```
```a = a -= 2``` significa que a vai receber o seu proprio valor subtraindo 2
``` python
a = 10

a *= 2 # em vez de a = a * 2

print(a)

# OutPut
# 20
```
```a = a *= 2``` significa que a vai receber o seu proprio valor multiplicando 2
```a = a -= 2``` significa que a vai receber o seu proprio valor subtraindo 2
``` python
a = 10

a /= 2 # em vez de a = a / 2

print(a)

# OutPut
# 5.0
```
```a = a /= 2``` significa que a vai receber o seu proprio valor dividido por 2
``` python
a = 10

a //= 3 # em vez de a = a // 3

print(a)

# OutPut
# 3
```
```a = a //= 3``` significa que a vai receber o seu proprio valor dividido por 3 devolvendo o numero inteiro
``` python
a = 10

a **= 2 # em vez de a = a ** 2

print(a)

# OutPut
# 100
```
```a **= 2``` significa que a vai receber o seu proprio valor elevado por 2
```a = a //= 3``` significa que a vai receber o seu proprio valor dividido por 3 devolvendo o numero inteiro
``` python
a = 10

a %= 2 # em vez de a = a % 2

print(a)

# OutPut
# 0
```
```a %= 2``` significa que a vai receber o seu proprio valor resto da divisão por 2
# Atribuição Múltipla
Exemplo:
``` python
a, b, c = 1, 2, 4

print(a)

# OutPut
# 1

print(b)

# OutPut
# 2

print(c)

# OutPut
# 4
```
Em vez de:
``` python
a = 1
b = 2
c = 4

print(a)

# OutPut
# 1

print(b)

# OutPut
# 2

print(c)

# OutPut
# 4
```
**Nota:** se tivermos varias variaveis que irão receber o mesmo valor então podemos fazer o seguinte:
``` python
x = y = z = 0

print(x)

# OutPut
# 0

print(y)

# OutPut
# 0

print(z)

# OutPut
# 0
```
# Estrutura condicional simples (if-else) (introdução)
Exemplo:
``` python
idade = 20

if idade >= 16:
    print('No Brasil você já pode votar')
    print('Mas lembre-se de que é o voto é secreto')

```
Mas sse mudar a Idade para 14, nada será mostrado:
``` python
idade = 14

if idade >= 15:
    print('No Brasil você já pode votar')
    print('Mas lembre-se de que é o voto é secreto')

```
Caso seja preciso um bloco ```False```, então podemos criar um ```else```:
``` python
print('Inicio do programa')

idade = 17

if idade >= 15:
    print('No Brasil você já pode votar')
    print('Mas lembre-se de que é o voto é secreto')
else:
    print('No Brasil você ainda não pode votar')

print('Fim do programa')
```
# Funções (introdução)
Funções são blocos de código reutilizaveis que executão uma tarefa especifica, ajuda a organizar o código e a evitar repetições, melhorando a legibilidade do código.

Como defenir uma função:
``` python
def saudacao():
    print('Olá, seja bem vindo ao meu programa')
```
Para executar a função ```saudacao```, basta :
``` python
saudacao()
```
Para alem das funções 'simples', que não têm parametros, nem valores de retorno, tambem podemos passar parametros para as funções:
``` python
def bem_vindo(nome):
    print('Olá',nome,', bem vindo(a) ao meu programa')

bem_vindo('Ricardo')
```
**Nota:** a variavel ```nome``` só existe bem da função

Este parametro que passo para dentro da função tambem se pode chamar de *argumento*.

Tambem é possivel criar funções que retornam valores:
``` python
def pi():
    return 3.14159

valor_pi = pi()

print('O valor de pi é:',pi())
```
Outro exemplo:
``` python
def somar(n1,n2):
    return n1 + n2

soma = somar(10,20)

print('O resultado da soma é:',soma)
```
# Tipo de dados iteráveis (listas)
Ussado para guardar dados relacionados todos juntos, exemplo:
``` python
frutas = ['maçã','Laranja','Maracujá']

print(frutas)

# OutPut
# ['maçã','Laranja','Maracujá']
```
Tambem posso querer aceder só um elemento da list, e consigo fazer isso pelo index do elemento na lista que começa no ```0```:
``` python
frutas = ['maçã','Laranja','Maracujá']

print(frutas[1])

# OutPut
# Laranja
```
# Tipos de dados iteráveis (tuplas)
as tuplas são parecidas com as Listas, mas não podem ser alteraadas depois de serem criadas.


``` python
cores = ('vermelho','verde','azul')

print('cores:',cores)

# Mostrar a cor verde
print(cores[1])
```
**Nota:** isto já não é possivel e irá dar erro, porque a tupla é **imutável**
``` python
cores = ('vermelho','verde','azul')

cores[0] = 'amarelo'

# OutPut
# TypeError: 'tuple' object does not support item assignment
```
# Tipo de dados iteráveis (set)
O tipo set tambem chamado de **conjunto**, é um conjunto **sem ordem defenida** (sem indexação) e **sem elementos repetidos**.


Exemplo:
``` python
numeros = {1, 2, 3, 4, 5}

print(numeros)
```
Aqui os numeros repetidos irão ser ignorados:
``` python
numeros = {1, 2, 3, 3, 4, 5, 5}

print(numeros)
```
Tambem ao imprimir, não existe a garantia que mantenha a ordem:
``` python
nome = {'João','Maria','José','Maria'}

print(nome)
```
# Tipo de dados iteráveis (dicionário)
Dicionário armazena várias chaves e valores. Você acessa os dados pela chave e não pelo index. Exemplo:
``` python
aluno = {'nome':'Arthur','nota':10}

print(aluno)

# Para acessesar o valor nome
print(aluno['nome'])
```
Para alterar valores posso fazer assim:
``` python
aluno = {'nome':'Arthur','nota':10}

aluno['nota'] = 14

print(aluno['nota'])
```
**Nota:** Se tentarmos criar um novo valor para uma chave que não existe, então vai ser criado um novo conjunto de chave valor
``` python
aluno = {'nome':'Arthur','nota':10}

aluno['sexo'] = 'masculino'

print(aluno)

# OutPut
# {'nome': 'Arthur', 'nota': 10, 'sexo': 'masculino'}
```
# Estruturas de iteração for (introdução)
Serve para percorrer dados interativos e obter todas as imformações de uma vez só

Vamos supor que temos uma lista de nomes e quero mostrar cada um desses nomes no console:
``` python
nomes = ['João','Maria','José','Ana','Pedro']

for nome in nomes:
    print(nome)
```
Iteração no dicionário:
``` python
aluno = {
    'nome':'Arthur',
    'idade':14,
    'notas':[7.5, 8, 10]
    }

for chave in aluno:
    print(chave,':',aluno[chave])

# OutPut
# nome : Arthur
# idade : 14
# notas : [7.5, 8, 10]
```
# Operadores de associação (Membership)
Verifica se um determinado valor está presente numa determinada sequência.

Exemplo:
``` python
frutas = ['maçã','banana','uva']

print('banana' in frutas)

# OutPut
# True
```
Python é case sencitive, portanto se mudarmos uma letra de minusculo para maiusculo o resultado vai ser diferente, exemplo:
``` python
frutas = ['maçã','banana','uva']

print('Banana' in frutas)

# OutPut
# False
```
Se quisermos verificar se um elemento **não está contido** numa lista então ussamos ```not in```:
``` python
frutas = ['maçã','banana','uva']

print('abacaxi' not in frutas)

# OutPut
# True
```
Tambem podemos ussar em strings para encontrar palavras num texto:
``` python
mensaguem = 'Bem vindo ao curso de Python'

print('Java' in mensaguem)
```
# Estrutura de repetição condicional while (introdução)
A estrutura ```while``` é utilizada para interar uma determinada lista emquanto uma condição for verdadeira, exemplo:
``` python
contador = 1

while contador <= 5:
    print('Contador:',contador)
    contador += 1
```
**Atenção:** É preciso cuidado com Loop infinito, caso aconteça no *terminal* use ```Ctrl```+```c```
# Tipo de dados personalizados (classes e objetos - Introdução)
Uma classe é serve como modelo para defenir quais dados uma variavel terá. Esses dados são chamados de **atributos**.

Tambem define quais ações podem efetuar e essas ações são chamadas de **metodos**

Um objecto é uma instrancia de uma class, ou seja é algo concreto formado com aquele molde.

Exemplo:
``` python
# Defenir uma classe
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
    
    def apresentar(self):
        print('Olá! Meu nome é', self.nome,'e eu tenho',self.idade,'anos de idade')

# Criar Objetos derivados com esta classe
pessoa1 = Pessoa('Ricardo',33)

# Chama atributos
print(pessoa1.nome)

# Chama metodos
pessoa1.apresentar()
```
# Módulos (bibliotecas - Introdução)
Médulo, é um arquivo de python externo e podemos importar para a nossa aplicação para pudermos reutilizar o seu código.
``` python
import math

# calcula a raiz quadrada
print(math.sqrt(25))

# calcula a potência
print(math.pow(2, 3))

# Valor de pi
print(math.pi)
```
**Nota:** eu posso dar um apelido ao módulo para facilitar, exemplo:
``` python
import math as m

# calcula a raiz quadrada
print(m.sqrt(25))

# calcula a potência
print(m.pow(2, 3))

# Valor de pi
print(m.pi)
```
Podemos importar tambem só parte do módulo
``` python
from math import sqrt, pi

print(sqrt(25))
print(pi)
```
# Tratamento de erros com try-except (Introdução)
Exemplo:
``` python
n1 = float(input('Digite o primeiro numero:'))
n2 = float(input('Digite o segundo numero:'))

resultado = n1 / n2

print('O resultado da divisão de',n1,'por',n2,'é igual a',resultado)
```
Este código tem uma situação sencivel, porque que ```n2``` for 0, então o resultado vai ser é um numero divido por 0, o que vai produzir um erro.

O mesmo irá acontecer caso ```n1``` ou ```n2``` tiverem letras.
Como pudemos tratar?
``` python
try:
    n1 = float(input('Digite o primeiro numero:'))
    n2 = float(input('Digite o segundo numero:'))

    resultado = n1 / n2

    print('O resultado da divisão de',n1,'por',n2,'é igual a',resultado)
except:
    print('Digite numeros válidos')
```
# Criar Blocos de código vazios com a palavra chave pass
Exemplo:
``` python
def login():
    pass
```
A palavra ```pass```, não tem qualquer funcionalidade, serve só para puder preencher uma função e assim não dar erro ao compilar.
# Interromper um loop com a palavra chave beak
Exemplo:
``` python
contador = 0

while True:
    print(contador)
    if contador == 5:
        break
    contador += 1
```
Tambem se pode ussar com o ```for```:
``` python
nomes = ['Arthur','Danielle','Gabriel','Manuela','Ana']

for nome in nomes:
    if nome == 'Gabriel':
        print('Gabriel encontrado na lista')
        break
    print('Nome:',nome)
```
# Pular iterações com a palavra chave continue
Pula a interação atual diretamente para a proxima iteração, exemplo:
``` python
for numero in range(10):
    if numero % 2 == 0:
        continue
    print(numero)
```
Este código só imprime os numeros impares
# Método de saída print (mais detalhes)
O metodo ```print()``` imprime textos no terminal, exemplos:
``` python
print('Olá, Mundo!')

nome = 'Gabriel'
idade = 40
print('Nome:',nome,'Idade:',idade)
```
O separador neste caso é o ```,```, mas tambem podemos alterar isso com o parametro ```sep```
``` python
print('21', '07','2025', sep='/')

# OutPut
# 21/07/2025
```
Quebra de linha (```\n```):
``` python
print('Gabriel\nArtigas')

# OutPut
# Gabriel
# Artigas
```
Outros caracteris especiais ou código de escape que podemos utilizar:
``` python
print('Carregando', end='...')
print('Concluído')

# OutPut
# Carregando...Concluído
```
Tipo file, permite retornar o valor noutro ficheiro:
``` python
print('Gabriela Artigas', file = open('saida.txt','w'))
```
Neste caso caso não exista um ficheiro saida.txt, irá crá-lo, e vai imprir o valor que estiver no print.

Se eu quiser que o print não subscreva, mas que adicione um novo conteudo, basta alterar o modo para 'a':
``` python
print('Gabriela Artigas', file = open('saida.txt','a'))
```
forma mais aconselhável:
``` python
with open('saida.txt','a') as arquivo:
    print('Gabriel', file = arquivo)
```
```flush```, força a submissão imediata da menssaguem, isto é util para programas que precisam de atualizar em tempo real:
``` python
import time

for i in range(3):
    print('carregando...',i,end = '\r',flush=True)
    time.sleep(1)

```
```\r```, obriga retornar para o inicio da linha ou seja faz o contrário do ```\n```, fazndo com que apanhe o 1º print e o volte a subscreve-lo.

O ```flush``` garante que a tela é **atualizada**
# Operadores de identidade
Exemplo:
``` python
a = [1, 2, 3]
b = a

print(b)

# OutPut
# [1, 2, 3]

a[2] = 4

print(b)

# outPut
# [1, 2, 4]
```
Neste caso só temos uma lista e duas variaveis a apontar para ela, para verificar se duas variaveis apontam para a mesma lista podemos fazer:
``` python

a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)

# OutPut
# True

print( a is c)

# OutPut
# False

# Para comparar se são iguais em termos de conteudo
print(a == c)

# OutPut
# True
```
# Gerar números aleatórios com random
Exemplo:
``` python
import random

# retorna um numero aleatório entre 1 e 10
num_inteiro = random.randint(1,10)

print('Número inteiro:',num_inteiro)

# retorna um numero float entre 0 e 1
num_float = random.random()

print('Número float:',num_float)

# gera um numero float entre 5 e 15
num_uniform = random.uniform(5,15)

print(num_uniform)

# Espolha aletória de uma lista
lista = ['maçã','banana','uva','laranja']

index = random.randint(0,3)

print(lista[index])

# OU

escolha = random.choice(lista)

print(escolha)

# Emparalhar a lista
random.shuffle(lista)

print(lista)
```
# Executar comandos do sistema operacional
Exemplo:
``` python
import os

# limpar o terminar
if os.name == 'nt':
    os.system('cls')
else:
    os.system('clear')

print('primeira linha')
print('segunda linha linha')
print('terceira linha')
```
Eu posso reduzir isto para:
``` python
import os

# limpar o terminar
os.system('cls' if os.name == 'nt' else 'clear')

print('primeira linha')
print('segunda linha linha')
print('terceira linha')
```
# A variável especial ```__name__```
Server para puxar moduloes que estão importados de outros módulos:

1º app.py
``` python
def funcao_principal():
    print('Executando a função principal do módulo',__name__)

if __name__ == '__main__' :
    funcao_principal()

```
2º principal.py
``` python
import app

app.funcao_principal()
```
