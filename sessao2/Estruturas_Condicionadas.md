# Estrutura condicional(if-elif-else)
Exemplos:
``` python
nota = int(input('Digite a nota: '))

if nota >= 60:
    print('Aprovado.')
else:
    print('Reprovado.')
```

E se tivesse uma verificação extra?
``` python
nota = int(input('Digite a nota: '))

if nota >= 70:
    print('Aprovado.')
elif nota >= 50:
    print('Recuperação.')
else:
    print('Reprovado.')
```

**Nota:** eu posso ter varios ```elif```s no código
# Estrutura condicional aninhada
Nada mais é de um if edntro do outro, Exemplo:
``` python
idade = 21
tem_carteira = True

if idade >= 18:
    if tem_carteira:
        print('Pode dirigir.')
    else:
        print('Precisa de tirar a carteira de habilitação.')
else:
    print('Não pode dirigir.')
```
# Uso de Operadores lógicos na estrutura condicional
Exemplo com ```and```:
``` python
idade = 21
tem_carteira = True

if idade >= 18 and tem_carteira:
    print('Pode dirigir.')
else:
    print('Não pode dirigir.')
```

Exemplo com ```or```:
``` python
nota = 60
presenca = 80

if nota >= 70 or presenca > 75:
    print('Aprovado.')
else:
    print('Reprovado.')
```

Exemplo com ```not```:
``` python
chovendo = False

if not chovendo:
    print('Pode sair para passear')
else:
    print('Não pode sair para passear')
```
# Avaliação de operadores lógicos na estrutura condicional
Valores avalidados como ```False```:
``` pythom
0, 0.0, '', [], {}, Nome
```

Qualquer outros valores vão ser avaliados como ```True```,

Podemos utilizar isso para validar se alguma variaveis está preenchida ou não:
``` phython
nome = ''

if nome:
    print('Nome preenchido')
else:
    print('Nome está vazio')
```

Exemplo em que o Utilizador precisa de preencher o email:
``` python
email = input('Digite o seu e-mail: ')

if email:
    print('Email registado.')
else:
    print('Você não digitou o email.')
```
# Comparação encadeada
Exemplo:
``` python
n = 5

# É a mesma coisa:
print(2 <= n and n <= 10)
print(2 <= n <= 10)

if 2 <= n <= 10:
    print('n está dentro do intervalo')
else:
    print('n está fora do intervalo')
```