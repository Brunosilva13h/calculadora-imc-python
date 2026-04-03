nome = input("Digite o seu nome: ")

try:
    idade = int(input("Digite a sua idade: "))
    altura = float(input("Digite a sua altura: "))
    peso = float(input("Digite o seu peso: "))

    if altura <= 0 or peso <= 0:
        print("Altura e peso devem ser maiores que zero.")
    else:
        imc = peso / (altura ** 2)

        if imc < 18.5:
            classificacao = "Abaixo do recomendado"
        elif imc < 25:
            classificacao = "Normal"
        elif imc < 30:
            classificacao = "Sobrepeso"
        else:
            classificacao = "Obesidade"

        print(f"\nNome: {nome}")
        print(f"Idade: {idade}")
        print(f"IMC: {imc:.2f}")
        print(f"Classificação: {classificacao}")

except ValueError:
    print("Erro: digite apenas números válidos para idade, peso e altura.")
