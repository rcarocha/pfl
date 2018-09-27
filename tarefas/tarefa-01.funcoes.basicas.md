<!DOCTYPE html>
<html>
<title>Programa��o Funcional e L�gica - Prof. Ricardo da Rocha</title>

<xmp theme="simplex" style="display:none;">


# Tarefa 1 de Programa��o Funcional e L�gica

# Vis�o geral

Nesta tarefa voc� dever� implementar algumas fun��es para valida��o e gera��o de n�meros de CPF. O algoritmo de gera��o e verifica��o dos d�gitos verificadores pode ser encontrado em diversos lugares. Duas sugest�es:

1. [Descri��o do algoritmo na Wikipedia](https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas#D%C3%ADgitos_verificadores)
2. <https://laennder.com/como-e-feito-o-calculo-de-validacao-cpf/>

Neste exerc�cio, consideraremos o d�gito 0 o menos significativo, o d�gito 9 o mais significativo do CPF, assim como assumido nesta [descri��o do algoritmo](https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas#D%C3%ADgitos_verificadores).


# Descri��o

Voc� dever� implementar as seguintes fun��es:

1. Implementar uma fun��o `cpfParaLista` que recebe um n�mero inteiro (`Integer`) descrevendo um CPF e gera uma lista de `Integer` com cada um dos d�gitos do n�mero de CPF. O CPF recebi pode ser de 9 d�gitos (sem o dois d�gitos de valida��o) ou de 11 d�gitos. Observe que no caso de um n�mero com menos de 9 d�gitos, devem ser completados 0s � esquerda. Exemplos de aplica��o:

   * `cpfParaLista(06948584933) => [0,6,9,4,8,5,8,4,9,3,3]`
   * `cpfParaLista(069485849) => [0,6,9,4,8,5,8,4,9]`
   * `cpfParaLista(69485849) => [0,6,9,4,8,5,8,4,9]`

2. Implementar uma fun��o `contribDigitoV1` que dado um `Integer` entre 1 e 9, retorna a contribui��o desse d�gito na gera��o da componente V1 do validador, sendo que os d�gitos do CPF s�o descritos de 9 at� 1, assim para o CPF `069485849`, o d�gito `9` � `0` e o d�gito `2` � `4`.

   * `contribDigitoV1(9) => `
   * `contribDigitoV1(1) => `

3. Implementar uma fun��o `contribDigitoV2` que dado um `Integer` entre 1 e 9, retorna a contribui��o desse d�gito na gera��o da componente V2 do validador, sendo que os d�gitos do CPF s�o descritos de 9 at� 1, assim para o CPF `069485849`, o d�gito `9` � `0` e o d�gito `2` � `4`.

   * `contribDigitoV2(9) => `
   * `contribDigitoV2(1) => `

4. Implementar uma fun��o `v1Cpf` que calcula o valor de v1 para um dado CPF

   * `v1Cpf(06948584933) => `
   * `v1Cpf(069485849) => `

4. Implementar uma fun��o `v2Cpf` que calcula o valor de v2 para um dado CPF

   * `v2Cpf(06948584933) => `
   * `v2Cpf(069485849) => `

5. Implementar uma fun��o `digitosVerificaCpf` que gera os dois d�gitos verificadores de um n�mero de CPF

   * `digitosVerificaCpf(06948584933) => `
   * `digitosVerificaCpf(069485849) => `

6. Implementar uma fun��o `cpfValido` que retorna verdadeiro se um CPF � v�lido, considerando inv�lidos todos os CPFs cujos nove d�gitos s�o iguais.

   * `cpfValido(06948584933) => True`
   * `cpfValido(069485849) => False`
   * `cpfValido(000000000) => False`
   * `cpfValido(00000000000) => False`
   * `cpfValido(11111111111) => False`

7. Implementar uma fun��o `geraCpfAleatorio()` que gera um n�mero de Cpf v�lido aleat�rio (os 11 d�gitos). Para isso, voc� ter� que usar o pacote [System.Random](http://hackage.haskell.org/package/random-1.1/docs/System-Random.html) do Haskell para gerar n�meros aleat�rios.

   Observe que para realizar essa usar o pacote `System.Random`, essa biblioteca deve estar dispon�vel para o Haskell, o que n�o ocorre na instala��o m�nima e no ambiente Haskell REPL.it. Utilizando o `stack` (ver documenta��o em [softwares](softwares.html)), voc� instala o pacote no ambiente Haskell com o seguinte comando:

        stack install random

   Para usar a biblioteca `Random`, adicione um `import System.Random` ao seu c�digo. Ent�o voc� pode usar o c�digo abaixo (apenas uma sugest�o):

        import System.Random
        g <- getStdGen
        take 10 (randoms g )

   A vari�vel `g` � inicializada com um genrador de n�meros aleat�rio e a �ltima linha retira os 10 primeiros elementos (usando `take`) de uma lista de inteiros aleat�rios, gerados a partir de `g`. A documenta��o de [System.Random](http://hackage.haskell.org/package/random-1.1/docs/System-Random.html) mostra outros exemplos de uso, mas esse � mais que o suficiente para voc� resolver a quest�o **7**.


# Requisitos

Reveja o [plano da disciplina](http://inf.ufg.br/~ricardo/pfl/plano/plano-PFL-2018.2.pdf) na se��o "PROCESSOS E CRIT�RIOS DE AVALIA��O", caso seja necess�rio relembrar como as tarefas ser�o avaliadas.

Os seguintes requisitos devem ser satisfeitos para o seu c�digo ter o conceito **FINALIZADO**.

1. Todas as fun��es implementadas devem incluir c�digo de teste, para al�m das fun��es indicadas acima.
1. O seu c�digo dever� ser submetido pelo [GitHub Classroom](https://classroom.github.com/), no local que ser� indicado at� o dia 20 de setembro. Acrescentarei tamb�m tutoriais sobre como usar o sistema.
2. As tarefas s�o individuais e nenhum tipo de c�pia ou similaridade com c�digo, seja de outro aluno, seja da Internet ou livros, ser� aceita.

# Prazo

O prazo **sugerido** para entrega da atividade � o dia 26/setembro. Voc� pode exceder esse prazo, mas nesse dia outra tarefa ser� lan�ada.

<!--
Valida��o de n�mero de CPF


123456789-09
numero    9 8 7 6 5 4 3 2 1
digito    8 7 6 5 4 3 2 1 0
contrib. 10 9 8 7 6 5 4 3 2 (errado = tirado da tabela)



1. Encontrar os d�gitos de um n�mero de CPF na forma de uma lista de inteiros.
2. Retorna a colabora��o do d�gito `n` no c�lculo do �ndice v1.

3. Gerar uma lista com todas as colabora��es dos d�gitos para c�lculo de v1.

3. Retorna o valor de v1.

2. Retorna a colabora��o do d�gito n no c�lculo do �ndice v2.

3. Gerar uma lista com todas as colabora��es dos d�gitos para c�lculo de v2.

3. Retorna o valor de v2.

4. Testa se CPF � igual a 11111111 ou 00000 (todos os digitos iguais o CPF deve ser ocnsiderado inv�lido)

4. Verifica se um dado CPf est� v�lido

5. Gera um n�mero de CPF v�lido, aleat�rio.







https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas

https://laennder.com/como-e-feito-o-calculo-de-validacao-cpf/


com os nove d�gitos

1. Encontrar os d�gitos de um n�mero de CPF na forma de uma lista de inteiros.

paraInteiros
paraInteirosRev

paraDigitos 1234 == [1,2,3,4]

module Test where

import Data.Char

paraInteiros :: [Char] -> [Int]
paraInteiros (n:[]) = digitToInt n
paraInteiros (d:ds) = [0]

main = digitToInt (head "03148393724")

s� deve considerar os 9 primeiros, no caso de valida��o.

2. Retorna a colabora��o do d�gito n no c�lculo do �ndice v1.

3. Gerar ums lista com todas as colabora��es dos d�gitos para c�lculo de v1.

3. Retorna o valor de v1.

2. Retorna a colabora��o do d�gito n no c�lculo do �ndice v2.

3. Gerar uma lista com todas as colabora��es dos d�gitos para c�lculo de v2.

3. Retorna o valor de v2.

4. Testa se CPF � igual a 11111111 ou 00000 (todos os digitos iguais o CPF deve ser ocnsiderado inv�lido)

4. Verifica se um dado CPf est� v�lido

5. Gera um n�mero de CPF v�lido, aleat�rio.

-->


</xmp>

<script src="http://strapdownjs.com/v/0.2/strapdown.js"></script>
</html>
