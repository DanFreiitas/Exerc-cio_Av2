## 1) Faça função que calcule a área do trapézio, dados: a) Base maior b) Base menor c) Altura Lembrando que a área pode ser calculada por: O programa principal deve pedir os valores e usar a função para calcular a área.

def calcular(B,b,h):
    area = ((B+b)*h)/2
    return area

baseMaior = float(input("Informe a base maior: "))
baseMenor = float(input('Informe a base menor: '))
altura = float(input('Informe a altura: '))

area = calcular(baseMaior, baseMenor, altura)

print(f"A área do trapézio é de: {area}")


## 2) Faça um programa em Python com uma função chamada soma_imposto. A função possui dois parâmetros formais: a) taxa_imposto, que é a quantia de imposto sobre vendas expressa em porcentagem; e b) custo, que é o custo de um item antes do imposto. A função "altera" o valor de custo para incluir o imposto sobre vendas. O programa principal deve pedir os dados e usar a função para calcular preço do produto

def soma_imposto(custo, taxa_imposto):
    return  (custo*taxa_imposto/100) + custo
  
  
custoProduto = float(input("Informe o valor do produto: "))
taxaImposto = float(input("Informe a porcentagem da taxa de imposto: "))

precoProduto = soma_imposto(custoProduto, taxaImposto)

print(f"O valor do produto será {precoProduto}")


## 3)Faça um programa que converta da notação de 24 horas para a notação de 12 horas. Por exemplo, o programa deve converter 14:25 em 2:25 P.M. 
a) A entrada é dada em dois inteiros. 
b) Deve haver pelo menos duas funções: uma para a conversão e uma para a saída. 
c) Registre a informação A.M./P.M. como um valor "A" para A.M. e "P" para P.M. Assim, a função para efetuar as conversões terá um parâmetro formal para registrar se é A.M. ou P.M. d) Inclua um loop que permita que o usuário repita esse cálculo para novos valores de entrada todas as vezes que desejar, digitando um valor negativo para a hora quando quiser encerrar

def horario(horas,minutos):
  horaAtualizada = hora if hora <=12 else hora-12
  AP = "AM" if hora <12 else "PM"
  return str(horaAtualizada)+":"+str(minutos)+AP
  
while True:
   hora = int(input("Informe a hora ou digite 0 para sair "))
   if hora == 0:
    break
   minutos = int(input("Informe os minutos"))
   print(horario(hora,minutos))


