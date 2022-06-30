# Anotações Gerais:

## Intrudução a Kotlin

- linguagem oficial android 
- null check 
- type safe
- 100% interoperável com Java
- Desenvolve frontend e backend com Kotlin/Js e multiplataformas com KMM

### Tipos Básicos de dados:
Long
FlotDouble
Array
Boolean
Char
Byte
Short
String
Int
Null!

### Valor Máximo

println(Int.MAX_VALUE)
println(Double.MAX_VALUE)
println(Float.MAX_VALUE)
println(Byte.MAX_VALUE)

### Conversão 
toByte()
toShort()
toInt()
toLong()
toFloat()
toDouble()
toChar()

### Declaração de Variável
var (valor mutável, camelCase)
val (constante, valor imutável, camelCase)
cont val (valor imutável cujo o valor é atribuido durante a compilação, SNAKE_CASE)

var = camelCase - valor defino e alterado durante a execução
val = camelCase = valor definido durante a execução e não é modificadop
const val = SNAKE_CASE = valor definido durante a compilação

EX:
var idadeAtual = 22

var idadeAtuaL:Int?
idadeAtual = null ou 22

val idadeAtual = 22

val idadeAtuaL:Int?
idadeAtual = null ou 22

const val MIN_AGE = 15
conSt val MAX_AGE = 68

## Exemplo Manipulando Strings :

### Concatenação

`val name = "ana"`

`val s = "Olá"`

`println(s+name)`

`//imprime Oláana`

`println("${s}, ${name.capitalize()}!")`

`//Imprime Olá, Ana!`

`println("Bem vindo(a), $name!")`

`//imprime Bem vindo(a), ana!`

### Indexação

_String como array_:

First() = Retorna a primeira posição de caracter

Last() = retorna a última

String.length = Retorna a posição a partir da quantidade de caracteres -1

String[index] = 

`val s = "Olá, Mundo!"`

`println(s[0])`

`println(s.first())`

`//imprime O`

`println(s[s.length-1])`

`println(s.last())`

`//imprime !`

## Formatação

- ### Capitalização de strings

capitalize() = Ana

toUpperCase() = ANA

toLowerCase() = ana

decapitalize() = aNA

- ### Remoção de espaços

trimEnd()

trimStart()

trim()

- ### Substituição de caracteres

replace(x,y)

- ### Formatação

"padrão${valor}".format(valor)



## Empty X Blank

_Empty = Vazia = String com tamanho 0_

_Blank = Em Branco = Maior que 0 mais todos os caracteres são espaços em branco_

`val s=""`

`// blank e empty`

`val s= "         "`

`// blank but is not empty`

## Funções

_Prefixo da Função_

fun nameFunction(name:Type):TypeReturn{}

Função tipo void

fun nameFunction(name:Type)

### Funções single-line

`private fun getFullName(name:String, lastName:String):String{`

`val fullName = "$name $lastName"`

`return fullname}`

to

`private fun getFullName(name:String, lastName:String):String{`

`"return $name $lastName"`

`}`

to

`private fun getFullName(name:String, lastName:String) = "$name $lastName"`

### Funções ordem superior

- _Recebem outra função ou lambda por parâmetro_

- _Bastante úteis para a generalização de funções e tratamentos de erros_

`val x = calculate(12,4,::sum)`

`val y = calculate(12,4){a,b -> a*b}`

exemplo:

`//função pricipal`

`fun main() {`

`val z:Int`

`z = calculate(34, 90){a,b ->`

`println("Vou calcular" $a * $b * 2)`

`(a + b) * 2`

`  }`

`println(z)`

`}`

`fun sum(a1:Int,a2:Int) = a1.plus(a2)`

`fun calculate(n1:Int,n2:Int,operation:(Int,Int)->Int)= operation(n1.n2)`

### Funções extensões

Prefixo: fun Tipo.nomeDaFuncao()

`fun String.randomCapitalizedLetter()=`

`thus[(0..this.length-1.random()].toUpperCase()`

### Estruturas de Controle

_*Lembrete: e ( **& &** ) ou ( **| |** )_

if

else

else if

when

elvis operator ?:

- Exemplo **if** 

`if (expressão){`

`//bloco de código`

`}else if (expressão2){`

`//bloco de código 2`

`}else{`

`//bloco de código 3`

`}`

_Para mais de 3 expressões, utilizar **when**_

- Exemplo **when**

`when{`

`case1 -> {}`

`case2 -> {}`

`case3 -> {}`

`else ->{}`

`}`

- Exemplo Elvis

`val a:Int? = null`

`var number = a ?: 0`

`se a for não for mulo retorne a. Se a for nulo retorne 0`

### Repetição

_While,do..while,for,forEach, letters_

for(variavelindexadora in/until/downTo faixa de valores/condicional step intervalo)

**while **

`while (Condição){`

`}`

**do..while**

`do{`

`//bloco`

`} while(condição)`

**for** 

`for(j in 0..20 step 2){`

`println(j)`

`}`