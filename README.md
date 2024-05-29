# calculadora-python
Calculadora simples onde eu adicionei um loop, para que você não precise excluir o terminal e fazer um novo calculo.

def menu():
    print("Escolha a operação")
    print("1. Adição")
    print("2. Subtração")
    print("3. Multiplicação")
    print("4. Divisão")




def Adicao (x, y):
    return x + y

def Subtracao (x, y):
    return x - y

def Multiplicacao (x, y):
    return x * y

def Divisao (x, y):
    return x / y



def obter_numero(prompt):
    while True:
        entrada = input (prompt)
        entrada = entrada.replace(',' ',' '.')
        try:
            return float(entrada)
        except ValueError:
            print("Entrada invalida, Por favor, digite um número válido")




def obter_numero(prompt):
    return float (input(prompt))

def obter_escolha():
    return input ("Digite a sua escolha (1/2/3/4) ")

menu ()
escolha = obter_escolha()

num1= obter_numero("Digite o primeiro número-> ")
num2= obter_numero("Digite o segundo -> ")



if escolha == '1':
    print (f"{num1} + {num2} = {Adicao(num1, num2)}")

elif escolha == '2':
    print (f"{num1} - {num2} = {Subtracao(num1, num2)}")

elif escolha == '3':
    print(f"{num1} * {num2} = {Multiplicacao(num1, num2)}")

elif escolha == '4':
    if num2 != 0:
        print (f"{num1} / {num2} = {Divisao(num1, num2 )}")

    else:
        print( "Erro: Divisão por zero não é permitido.")

else:
    print ("Opcão invalida.")



while True:
    menu()
    escolha = obter_escolha()


    if escolha == '5':
        print ("Saindo da calculadora, até logo!")
        break

    num1 = obter_numero ("Digite o primeiro número: ")
    num2 = obter_numero ("Digite o segundo número:")

    if escolha == '1':
        print (f"{num1} + {num2} = {Adicao(num1, num2)}")
    
    elif escolha == '2':
        print (f"{num1} - {num2} - {Subtracao(num1, num2)}")

    elif escolha == '3':
        print(f"{num1} * {num2} = {Multiplicacao(num1, num2)}")

    elif escolha == '4':
        if num2 == 0:
            print(f"{num1} / {num2} {Divisao(num1, num2)}")
        else:
            print( "Erro: Divisão por zero não é permitida!")

    else:
        print( " Opção invalida. Por favor, escolha uma operação invalida.")


