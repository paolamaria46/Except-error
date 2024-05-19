# Except-error
from datetime import date

def obter_ano_nascimento():
    while True:
        try:
            ano = int(input("Digite o ano de nascimento (entre 1922 e 2021): "))
            if 1922 <= ano <= 2021:
                return ano
            else:
                print("Ano fora do intervalo permitido.")
        except ValueError:
            print("Ano inválido. Por favor, digite um número.")

def main():
    nome_completo = input("Digite seu nome completo: ")
    ano_nascimento = obter_ano_nascimento()
    idade = date.today().year - ano_nascimento
    print(f"Olá, {nome_completo}! Você completou ou completará {idade} anos no ano de 2022.")

# Chamada da função principal
main()
