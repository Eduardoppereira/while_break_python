# Jogo da Adivinhação em Python

## Introdução

Este repositório contém um exemplo prático de como dominar o uso do While-Loop e do Break em Python. O objetivo é explorar o controle de fluxo preciso em cenários complexos, utilizando essas estruturas de controle de maneira inteligente.

## Desafio Proposto

Imagine que você está desenvolvendo um jogo onde os jogadores têm que adivinhar um número secreto. Neste projeto, vamos explorar como usar o While e o Break para controlar a repetição do jogo.

## Estruturas Chave

### While-Loop

- **While:** Executa um bloco de código repetidamente enquanto uma condição é verdadeira.
- **Break:** Permite sair do loop antes que a condição seja naturalmente falsa.

### Número Secreto Aleatório

Para fazer o Python gerar um número aleatório, usaremos a biblioteca random.
- Método randint(): Retorna um número inteiro do elemento selecionado do intervalo especificado.
- random.randint(1, 100): Gera um número aleatório entre 1 e 100 e armazena na variável "numero_secreto".
  
### Estrutura de Controle:

- If: Verifica se o palpite é igual ao número secreto.
- Elif: Trata casos em que o palpite é menor ou maior que o número secreto.
- Else: Executado se nenhuma das condições anteriores for verdadeira.

## Desenvolvimento do Jogo


```python
import random

numero_secreto = random.randint(1, 100)
tentativas = 0
limite_tentativas = 10

print("Bem-vindo ao Jogo da Adivinhação!")
print(f"Você tem {limite_tentativas} tentativas para adivinhar o número secreto.")

while tentativas < limite_tentativas:
    palpite = int(input("Digite seu palpite: "))

    if palpite == numero_secreto:
        print(f"Parabéns! Você acertou o número secreto {numero_secreto} em {tentativas + 1} tentativas.")
        break
    elif palpite < numero_secreto:
        print("Tente um número maior.")
    else:
        print("Tente um número menor.")

    tentativas += 1
else:
    print(f"Fim das tentativas. O número secreto era {numero_secreto}.")

