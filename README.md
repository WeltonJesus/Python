# Python

#Criei um programa que jogou par ou impar com o computador

#Utilizando comando while True:

from random import randint

v = 0

while True:
    jogador=int(input('Digite um número :'))
    computador = randint(0, 10)
    total = jogador + computador
    tipo= ' '
    while tipo not in 'PI':
        tipo = str(input('O número é [P/I] ?')).upper().strip()[0]
    print(f'Você jogou {jogador} e o computador jogou {computador}. Deu o tatal de {total}', end= '')
    print('Deu PAR' if total % 2 == 0 else 'DEU IMPAR')
    if tipo == 'P':
        if total % 2 == 0:
            print('Você VENCEU!')
            v += 1
        else:
            print('Você PERDEU !')
            break
    elif tipo == 'I':
        if total % 2 == 1:
            print('Você VENCEU!')
            v +=1
        else:
            print('Você PERDEU!')
            break
    print('VAMOS JOGAR NOVAMENTE......!')
print(f' GAME OVER!. Você venceu {v} vezes !')
