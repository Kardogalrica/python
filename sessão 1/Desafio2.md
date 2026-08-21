## Desafio 2
Crie um programa em Python quee simule **jogo de adivinhação de números.**


## **O programa deve:**
1. Gerar automaticamente um **número secreto entre 1 e 10** (o número será escolhido de forma aleatória).
2. Solicitar que o usuário digite palpites até acertar o número secreto.
3. A cada palpite incorreto, exibir a menssaguem **Errou, tente novamente!**
4. Contar quantas tentativas o usuário fez até acertar.
5. Ao final, quando o usuário descobrir o número secreto, exibir a menssaguem de parabéns junto com o número de tentativas realizadas.

Minha solução:
``` python
import random

numero_secreto = random.randint(1,10)

numero_utilizador = None
contador = 0

numero_utilizador = int(input('digite o número secreto: '))

while numero_secreto == numero_utilizador:
    contador += 1
    numero_utilizador = int(input('Errou, tente novamente! '))


print('Parabéns acertou em',contador,'tentativas')
```
Solução:
``` python
import random

numero_secreto = random.randint(1,10)
tentativas = 0

while True:
    palpite = int(input('Tente adivinha o número secreto (entre 1 e 10) '))
    tentativas += 1
    if palpite == numero_secreto:
        print('Parabéns! Você acertou o número em',tentativas,'tentativas.')
        break
    else:
        print('Errou! Tente novamente.')
```