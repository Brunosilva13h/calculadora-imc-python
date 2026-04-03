nome = input("Digite o seu nome: ")

try:
    idade = int(input("Digite a sua idade: "))
    altura = float(input("Digite a sua altura: "))
    peso = float(input("Digite o seu peso: "))

    imc = peso / (altura ** 2)

    if imc < 18.5:
        classificacao = "IMC abaixo do recomendado"
    elif imc < 25:
        classificacao = "Normal"
    elif imc < 30:
        classificacao = "sobrepeso"
    else:
        classificacao = "Obeso"

    print(f"\nnome: {nome}")
    print(f"idade {idade}")
    print(f"imc {imc:.2f}")
    print(f"classificaoco {classificacao}")
    
except ValueError:
    print("Voce digitou o valaor errado")
    
