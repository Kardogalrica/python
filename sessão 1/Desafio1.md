# Desafio prova final

# Enunciado desafio prático - Verificando se o aluno pode fazer a prova final
Você foi contratado para desenvolver uma **ferramenta simples de verificação de aprovação para a prova final**. O sistema deve avaliar se um aluno poderá ou não realizar a prova final com base em dois critérios:

1. **Média final do aluno** (um número decimal).

2. **Entrega das atividades extras** (sim ou não).

## Regras de aprovação:
Se a média final do aluno for **maior ou igual a 7**, ele terá direito de realizar a prova final.

Caso o aluno não tenha alcançado a média 7, ele ainda poderá fazer a prova final **se tiver entregue todas as atividades extras**.

Caso nenhuma dessas condições seja atendida, o aluno **não poderá realizar a prova final**.

## Objetivo do desafio:
Solicitar a média final do aluno.

Perguntar se ele realizou todas as atividades extras.

Exibir a mensagem adequada:

- ```"Você pode fazer a prova final."```

- ```"Você não pode fazer a prova final."```

## Observação Importante:

Tente resolver o desafio por conta própria primeiro. Mas não se preocupe se não conseguir: na próxima aula, vamos mostrar uma possível solução completa e explicada para este desafio.

## Solução
Minha Solução:
``` python
media = float(input('Por favor indique a média final do aluno: '))

if media >= 7:
    print('Você pode fazer a prova final.')

if media == 7:
    actividades_extras = input('Entregou todas as atividades extras? (sim/não): ')
    if actividades_extras == 'sim':
        print('Você pode fazer a prova final.')
    else:
        print('Você não pode fazer a prova final.')

if media < 7:
    print('Você não pode fazer a prova final.')
```
Solução do Desafio:
``` python
media = float(input('Digite sua média final: '))
atividades_extras = input('Você fez todas as atividades extras? (sim/não): ')

fez_atividades = atividades_extras == 'sim'

if media >= 7 or fez_atividades :
    print('Você não pode fazer a prova final.')
else:
    print('Você não pode fazer a prova final.')
```