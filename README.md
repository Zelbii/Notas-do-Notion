# Notas-do-Notion

15/02/22
Fiz do 5 exercicios do curso do Gustavo Guanabara (ex23 ao 27) estou sentindo dificuldade em perceber a estutura de manipulação de texto, talvez seja melhor rever essa materia antes de passar para as condições que é a próxima aula. 
17/02/22
Voltei a repetir os exercicios, porém ainda continuo com dificuldades em conseguir perceber a manipulação de texte.
aula 10-condições→ parte1
https://youtu.be/K10u3XIf1-Q?list=PLvE-ZAFRgX8hnECDn1v9HNTI71veL3oW0
#carro.sega()
#carro.esquerda()
#carro.siga()
#carro.direito()
#carro.siga()
#carro.direito()
#carro.siga()
#carro.esquerdo()
#carro.siga()
#carro.pare()
#todas essas ordens são sequências, acontecem de cima para baixo, não tem como pular etapa, só tem 1 caminha ou seja é uma estrutura sequência.
#carro.siga() aqui tem 2 opções, ou vira a direito ou a esquerda
#carroesquerda()        carro.direito()
#carro.siga()                carro.siga()
#carro.direito()            carro.esqueda()
#carro.siga()                carro.siga()
#carro.direito()            carro.esquerda()
#carro.esquerda()        carro.siga()
#carro.siga()                carro.pare()
#carro.direito()
#carro.siga()
#carro.pare()
exemplo:
tempo=int(input('Quantos anos tem o seu carro? '))
if tempo <=3:
print('carro novo')
else:
print('carro velho')
Da para fazer de uma outra maneira, uma forma mais simples com apenas 1 print
tempo=int(input('Quantos anos tem o seu carro? '))
print('carro novo'if tempo <=3 else 'carro velho')
print('--FIM--')
outro exemplo
n1=str(input('Qual o seu nome? '))
if n1=='Elber':
print('que nome lindooooooo <3')
print('Bom dia {}'.format(n1))
melhoria que fiz no código
n1=(input('Qual o seu nome? ')).upper()
if n1=='ELBER':
print('que nome lindooooooo <3')
else:
print('não é tão lindo esse nome.')
print('Bom dia {}'.format(n1))
programa que faz a média das tuas notas e te manda se ta aprovado ou reprovado
n1=float(input('digite a sua primeira nota '))
n2=float(input('digite a sua segunda nota '))
m=(n1+n2)/2
if m >=9.5:
print('aprovado com sucesso ')
else:
print('reprovado')
programa que da desconto se a pessoa fizer uma viagem de mais de 200km
from time import sleep
print('SEJA MUITO BEM VINDO')
sleep(2)
print('_.-.'30)
print('É um cliente sortudo! por ser a dua primeira compra receberá um desconto se fizer uma viagem maior que 200km')
n1=float(input('Insira a quantidade de Km que irá fazer '))
if n1 >200:
print('recebeu a promoção! a viagem de {} terá  o valor de {}€'.format(n1,n10.45))
else:
print('está preste a fazer uma viagem de {} terá o valor de {}€'.format(n1,n1*0.50))
programa que recebe um ano e diz se é bissexto ou não
import calendar
from datetime import date
ano = int(input('Digite o ano: '))
ano6 = calendar.isleap(ano)
if ano==0:
ano=date.today().year
if ano6 is True:
print(f'O ano de {ano} é bissexto')
else:
print(f'O ano de {ano} não é bissexto')
from datetime import date
ano=int(input('digite o ano que precisa analisar digite 0 caso precise ver a data atual do seu pc '))
if ano==0:
ano=date.today().year
if ano%4==0 and ano%100 !=0 or ano%400==0: # se o número for divisível por 4=0 por 100 !=0 OU 400=0 ELE É BISSEXTO
print('o {} é BISSEXTO '.format(ano))
else:
print('o ano {} não é BISSEXTO'.format(ano))
Programa que recebe 3 input e diz qual numero é maior
a=float(input('digite o primeiro número '))
b=float(input('digite o segundo número '))
c=float(input('digite o terceiro número '))
menor=a
if b<a and b<c:
menor=b
if c<a and c<b:
menor=c
if b>a and b>c:
maior=b
if c>a and c>a:
maior=c
print('o menor número é {}'.format(menor))
print('o maior número é {}'.format(maior))
n1 =int(input('digite o primeiro número:  '))
n2 =int(input('Digite o segundo número: '))
n3 =int(input ('Digite o terceiro número: '))
lista =[n1,n2,n3]
lista_ordenada = sorted(lista)
print('O menor número é {}'.format(lista_ordenada[0]))
print ('O maior número é {}'.format(lista_ordenada[2]))
Aula 12-Condições aninhadas
é quando dentro de um IF há duas opções.
#carroesquerda()                   carro.siga()                 carro.direito()
#carro.siga()                           carro.pare()                carro.siga()
#carro.direito()                                                        carro.esqueda()
#carro.siga()                                                            carro.siga()
#carro.direito()                                                        carro.esquerda()
#carro.esquerda()                                                   carro.siga()
#carro.siga()                                                            carro.pare()
#carro.direito()
#carro.siga()
#carro.pare()
exemplo:
If carro.esquerda():
carroesquerda()     
carro.siga()    
carro.direito()       
carro.siga()        
carro.direito()            
carro.esquerda()               
carro.siga()         
carro.siga()         
carro.direito()
carro.siga()
carro.pare()
else:
carro.direito()
carro.siga()
carro.esqueda()
carro.siga()
carro.esquerda()
carro.siga()
carro.pare()
elif: 
carro.siga() 
carro.pare()      
Exemplo
n=str(input('Qual o seu nome? ')).upper()
if n == 'ELBER':
print('Você ta gordo {}'.format(n))
elif n == 'JOANA' or n == 'JUUU':
print('Seu nome é lindo, assim como você {}'.format (n))
elif n == 'SILVIA':
print('SILVA SILVAAAAAAAAAAAAAAAAAAAAAAAAA!')
print('tenha um bom dia, {}'.format(n))
exercício 36 - Programa que aprova empréstimo se a mensalidade da casa for menor ou igual a 30% do seu salário.
casa=float(input('Qual o valor da casa que deseja comprar? '))
sal=float(input('Qual o seu salário atual? '))
anos=int(input('em quantos anos é que deseja pagar o empréstimo? '))
mensal=casa/(anos*12)
mini=sal*(30/100)
if mensal <= mini:
print('A casa que pretende comprar tem o valor de {} \nPara pagar essa casa em {:.2f} a mensalidade será de {} \nEmprestimo APROVADO  '.format(casa,anos,mensal))
else:
print('A casa que pretende comprar tem o valor de {} \nPara pagar essa casa em {:.2f} a mensalidade será de {} sendo menor ou igual a 30 porcento do seu salário \nempréstimo NEGADO '.format(casa,anos,mensal))
Exercício 37- Programa que lê um número e transforma em Binário/Octal/Decimal dependendo da sua escolha
num=int(input('digite um número inteiro: '))
print('''escolha uma das bases para a conversão:
[1] converter para BINÁRIO
[2] converter para OCTAL
[3] converter para DECIMAL''')
opção=int(input('Sua opção: '))
if opção==1:
    print('{} convertido para BINÀRIO é igual a {}'.format(num, bin(num)[2:])) #[2:] é para começar a contar depois do 2 número porque no python as funções BIN OCT HEX elas começam com caracteres estranhos tipo Bi110011
elif opção==2:
    print('{} convertido para OCTAL é igual a {}'.format(num, oct(num)[2:]))
elif opção==3:
    print('{} convertido para HEXADECIMAL é igual a {}'.format(num,hex(num)[2:]))
else:
    print('opção inválida. tenta novamento')
Exercício 38 - Programa lê 2 valores e diz se o valor x é maior que o y ou se são iguais
n1=int(input('digite o primeiro número '))
n2=int(input('digite o segundo número '))
if n1>n2:
    print('o Primeiro valor é maior')
elif n2>n1:
    print('o Segundo valor é maior')
elif n1==n2:
    print('Os valores são iguais')
Exercício 39 - Programa que lê o seu ano de nascimento e diz que está a tempo de alistar ou não, se já passou a data ou quanto tempo falta para se alistar no exercito 
from datetime import date
atual=date.today().year
n1=int(input('Digite o seu ano de nascimento '))
idade=atual-n1
    print('\033[1;33m Quem nasceu em {} tem {} em {} '.format(n1, idade, atual))
if idade==18:
    print('\033[1;33m você deve se alistar imediatamente ')
elif idade<18:
saldo=18-idade
    print('\033[1;32m ainda faltam {} para o seu alistamento '.format(saldo))
ano=atual+saldo
    print('o seu ano de alistamento  será em {} '.format(ano))
elif idade>18:
saldo=idade-18
    print('\033[1;31m você já deveria ter se alistado faz {} anos!! vai rápido procurar o quartel mais próximo de ti '.format(saldo))
ano=atual-saldo
    print('o seu ano de alistamento foi em {} '.format(ano))
Exercício 40 - Programa que lê a primeira e a segunda nova, diz a tua média e se foi aprovado ou não
n1=float(input('Qual a nota que obteve no primeiro teste? '))
n2=float(input('Qual a nota que obteve no segundo teste? '))
m=(n1+n2)/2
if m<8:
    print('\033[1;31m obteve {} e {} reprovado terrá que ir a exame {} '.format(n1, n2,m))
elif m>=9.5:
    print('\033[1;32m obteve {} e {} Parabéns!! você passou com {}'.format(n1,n2,m))
elif 8 <= m < 9.4:
    print('\033[1;33m obteve {} e {} será permitida a realização do segundo teste, sua média é de {}, '.format(n1, n2, m))
Exercício 41 - Programa que indica a sua categoria
from datetime import date
n1=int(input('em que ano nasceu? '))
atual=date.today().year
idade=atual-n1
print('\033[1;33m Quem nasceu em {} tem {} em {} '.format(n1, idade, atual))
if idade<=9:
    Categoria='MIRIM'
elif 9 < idade <= 14:
    categoria = 'INFANTIL'
elif 14 < idade <= 19:
    categoria='JUNIOR'
elif 19 < idade <= 25:
    categoria='SÊNIOR'
else:
    categoria='MASTERBLASTER'
print('Você tem {} logo a sua categoria é {}'.format(idade, categoria))
Exercício 42 - Programa que pede para você colocar 3 valores de segmento de retas e ele se esses segmentos de retas podem formar um triângulo ou não, se puderem formar um triângulo ele diz que tipo de triângulo é
s1=float(input('o primeiro segmento tem '))
s2=float(input('o segundo segmento tem '))
s3=float(input('o terceiro segmento tem '))
if s1 < s2 + s3 and s2 < s1 + s3 and s3 < s1 + s2:
    print('Os segmentos acima podem formar um trinângulo!', end='')
    if s1==s2==s3:
        print('EQUILÁTERO ')
    elif s1!=s2!=s3!=s1:
        print('ESCALENO')
    else:
        print('ISÓSCELES')
else:
print('Os segmentos acima não podem formar um triângulo!')
Exercício 43 - Programa que recebe um valor de peso e altura e retorna o Seu IMC junto com que categoria você se encontra
peso=float(input('Digite o seu Peso '))
altura=float(input('Digite a sua altura '))
imc=peso/(altura*altura)
if imc < 18.5:
print('O seu IMC é de {:.2f} você está a baixo do peso'.format(imc))
elif 18.5<=imc<24.9:
print('O seu IMC é de {:.2f} você está com o peso ideal '.format(imc))
elif 25<=imc<29.9:
print('O seu IMC é de {:.2f} você está com sobrepeso '.format(imc))
elif 30<=imc<34.9:
print('O seu IMC é de {:.2f} você está com Obesidade grau 1 '.format(imc))
elif 35<=imc<39.9:
print('O seu IMC é de {:.2f} você está com obesidade grau 2 '.format(imc))
elif imc >=40:
print('O seu IMC é de {:.2f} você está com obesidade grau 3' .format(imc))
Exercício 44 - Programa que recebe um valor e pergunta com que tipo de pagamento vai efetuar a compra, dependendo do tipo de pagamento o valor pode alterar tanto para cima como para baixo
print('=======Lojas Chaves=======')
n1=float(input('Digite o valor da sua compra '))
print('[1] à vista dinheiro/cheque\n[2] à vista cartão \n[3] 2x no cartão \n[4] 3x ou mais no cartão')
n2=int(input('como pretende fazer o pagamento? '))
if n2==1:
compra=n10.90
print('a sua compra que inicialmente era de {} teve um desconto 10% e o valor final é de {:.2f}'.format(n1,compra))
elif n2==2:
compra=n10.95
print('a sua compra que inicialmente era de {} teve um desconto de 5% e o valor final é de {:.2f}'.format(n1, compra))
elif n2==3:
parcela=n1/2
print('A sua compra que inicialmente era de {} parcelando em 2x o valor da parcela é de {}'.format(n1,parcela))
elif n2==4:
n3=int(input('Em quantas prestações pretende pagar? '))
parcela=n11.20/n3
preço=n11.20
print('A sua compra que inicialmente era de {} pagando em {} as parcelas finais serão de {} totalizando o valor de {}'.format(n1,n3,parcela,preço))
else:
print('opção inválida, escolha um número de 1 a 4 ')
Exercício 45 - Um programa de pedra papel e tesoura 
from random import randint
from time import sleep
itens=('Pedra', 'Papel', 'Tesoura')
computador=randint(0, 2)
print('Suas opções: \n[0] PEDRA \n[1] PAPEL \n[2] TESOURA ')
n1=int(input('Qual será a sua jogada? '))
print('.-.'*15)
print('pedra')
sleep(2)
print('papel')
sleep(2)
print('tesouraaaaaaaaaaa')
if computador ==0: # O computador jogou PEDRA
if n1==0:
print('\033[1;33ma jogada empatou!')
elif n1==1:
print('\033[1;32mVocê ganhou!!!!')
elif n1==2:
print('\033[1;31mVocê perdeu!!!!')
elif computador ==1: # O computador jogou PAPEL
if n1==0:
print('\033[1;31mVoce perdeu!!!!')
elif n1==1:
print('a jogada empatou!')
elif n1==2:
print('\033[1;32mVocê ganhou!!!!')
elif computador ==2: # o Computador jogou TESOURA
if n1==0:
print('\033[1;32mVocê ganhou!!!!')
elif n1==1:
print('\033[1;31mVocê perdeu!!!!')
elif n1==2:
print('\033[1;33mA jogada empatou!')
else:
print('Opção inválida')
print('.-.'*15)
print('O computador escolheu {}'.format(itens[computador]))
print('O jogador escolheu {}'.format(itens[n1]))
Pequenas observações e estudos sobre as estruturas de condições

Simbologia usada nas condições para atribuir sentido de igualdade/diferença maior menor ou igual

Aqui da pra ver como é atribuído uma faixa, nesse caso de idade, colocamos a variável logo em seguida o sentido em seguida AND para atribuir outra vez a variável e um limite 
EX: if idade ≥=10 and idade <20 → se a idade for maior ou igual a 10 e menor que 20
Estrutura de repetição FOR parte 1
A estrutura de repetição é usada para quando queremos repetir 1 única ação várias vezes, sendo assim em vez de escrever “siga em frente siga em frente siga em frente” utilizamos Siga no intervalo(1.3)
EX:
for c in range(1.10):
Passo
pega
Em vez de fazer:
passo→pula→passo→pula→passo→pula→passo→pega
Faço:
for c in range(0.3):
passo
pula
passo
pega
Estrutura de repetição FOR com CONDICIONAL
for c in range(0.3):
IF==moeda:
Pega
passo
pula
passo
pega
print('oi')
print('oi')
print('oi')
print('oi')
print('oi')
print('oi')
for c in range(0,6): #no piton ele vai contar do 1 até o 5 e no 6 ele para, por isso que colocamos o 0, para fazer do 5 até o 5 contando 6 vezes de OI
print('oi')
print('fim')#vai escrever oi 6 vezes e depois dar print 'FIM
for c in range(0,6):
print('oi')
print('fim') #aqui o programa vai escrever oi fim 6 vezes só porque o "print('fim')" está na mesma camada que o "print('oi')"
for c in range (1,6):#contagem crescente de 1 até 5, ele ignora o 6
print(c)
print('fim')
for c in range (6,0,-1):# contagem decrescente de 6 até 1 o -1 é de quanto em quanto que vai ser pulado, nesse caso vai ser de -1, sendo assim vai decrescer
print(c)
print('FIM')
i=int(input('início: '))#insira o inicio da contagem
f=int(input('Fim: '))#insira o fim da contagem
p=int(input('Passo: '))#de quanto em quanto que vai pular o valor
for c in range(i,f+1,p):#0 f+1 é o fim da contagem, nesse caso queremos que ele pare de contar depois de F, sendo assim f+1
print(c)
print('FIM')
for c in range(0,3):
n=int(input('Digite um valor: '))#podemos colocar input dentro de FOR
print('fim')
s=0#atribuindo valor de s=0
for c in range(0,4):
n=int(input('Digite um valor: '))#possibilitando a entrada de 3 valores podemos fazer o somatório deles
s+=n#somatório dos valores (0+n)
print('o somatório de todos os valores foi {}'.format(s))
