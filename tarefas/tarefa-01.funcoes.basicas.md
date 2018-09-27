<!DOCTYPE html>
<html>
<title>Programação Funcional e Lógica - Prof. Ricardo da Rocha</title>

<xmp theme="simplex" style="display:none;">


# Tarefa 1 de Programação Funcional e Lógica

# Visão geral

Nesta tarefa você deverá implementar algumas funções para validação e geração de números de CPF. O algoritmo de geração e verificação dos dígitos verificadores pode ser encontrado em diversos lugares. Duas sugestões:

1. [Descrição do algoritmo na Wikipedia](https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas#D%C3%ADgitos_verificadores)
2. <https://laennder.com/como-e-feito-o-calculo-de-validacao-cpf/>

Neste exercício, consideraremos o dígito 0 o menos significativo, o dígito 9 o mais significativo do CPF, assim como assumido nesta [descrição do algoritmo](https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas#D%C3%ADgitos_verificadores).


# Descrição

Você deverá implementar as seguintes funções:

1. Implementar uma função `cpfParaLista` que recebe um número inteiro (`Integer`) descrevendo um CPF e gera uma lista de `Integer` com cada um dos dígitos do número de CPF. O CPF recebi pode ser de 9 dígitos (sem o dois dígitos de validação) ou de 11 dígitos. Observe que no caso de um número com menos de 9 dígitos, devem ser completados 0s à esquerda. Exemplos de aplicação:

   * `cpfParaLista(06948584933) => [0,6,9,4,8,5,8,4,9,3,3]`
   * `cpfParaLista(069485849) => [0,6,9,4,8,5,8,4,9]`
   * `cpfParaLista(69485849) => [0,6,9,4,8,5,8,4,9]`

2. Implementar uma função `contribDigitoV1` que dado um `Integer` entre 1 e 9, retorna a contribuição desse dígito na geração da componente V1 do validador, sendo que os dígitos do CPF são descritos de 9 até 1, assim para o CPF `069485849`, o dígito `9` é `0` e o dígito `2` é `4`.

   * `contribDigitoV1(9) => `
   * `contribDigitoV1(1) => `

3. Implementar uma função `contribDigitoV2` que dado um `Integer` entre 1 e 9, retorna a contribuição desse dígito na geração da componente V2 do validador, sendo que os dígitos do CPF são descritos de 9 até 1, assim para o CPF `069485849`, o dígito `9` é `0` e o dígito `2` é `4`.

   * `contribDigitoV2(9) => `
   * `contribDigitoV2(1) => `

4. Implementar uma função `v1Cpf` que calcula o valor de v1 para um dado CPF

   * `v1Cpf(06948584933) => `
   * `v1Cpf(069485849) => `

4. Implementar uma função `v2Cpf` que calcula o valor de v2 para um dado CPF

   * `v2Cpf(06948584933) => `
   * `v2Cpf(069485849) => `

5. Implementar uma função `digitosVerificaCpf` que gera os dois dígitos verificadores de um número de CPF

   * `digitosVerificaCpf(06948584933) => `
   * `digitosVerificaCpf(069485849) => `

6. Implementar uma função `cpfValido` que retorna verdadeiro se um CPF é válido, considerando inválidos todos os CPFs cujos nove dígitos são iguais.

   * `cpfValido(06948584933) => True`
   * `cpfValido(069485849) => False`
   * `cpfValido(000000000) => False`
   * `cpfValido(00000000000) => False`
   * `cpfValido(11111111111) => False`

7. Implementar uma função `geraCpfAleatorio()` que gera um número de Cpf válido aleatório (os 11 dígitos). Para isso, você terá que usar o pacote [System.Random](http://hackage.haskell.org/package/random-1.1/docs/System-Random.html) do Haskell para gerar números aleatórios.

   Observe que para realizar essa usar o pacote `System.Random`, essa biblioteca deve estar disponível para o Haskell, o que não ocorre na instalação mínima e no ambiente Haskell REPL.it. Utilizando o `stack` (ver documentação em [softwares](softwares.html)), você instala o pacote no ambiente Haskell com o seguinte comando:

        stack install random

   Para usar a biblioteca `Random`, adicione um `import System.Random` ao seu código. Então você pode usar o código abaixo (apenas uma sugestão):

        import System.Random
        g <- getStdGen
        take 10 (randoms g )

   A variável `g` é inicializada com um genrador de números aleatório e a última linha retira os 10 primeiros elementos (usando `take`) de uma lista de inteiros aleatórios, gerados a partir de `g`. A documentação de [System.Random](http://hackage.haskell.org/package/random-1.1/docs/System-Random.html) mostra outros exemplos de uso, mas esse é mais que o suficiente para você resolver a questão **7**.


# Requisitos

Reveja o [plano da disciplina](http://inf.ufg.br/~ricardo/pfl/plano/plano-PFL-2018.2.pdf) na seção "PROCESSOS E CRITÉRIOS DE AVALIAÇÃO", caso seja necessário relembrar como as tarefas serão avaliadas.

Os seguintes requisitos devem ser satisfeitos para o seu código ter o conceito **FINALIZADO**.

1. Todas as funções implementadas devem incluir código de teste, para além das funções indicadas acima.
1. O seu código deverá ser submetido pelo [GitHub Classroom](https://classroom.github.com/), no local que será indicado até o dia 20 de setembro. Acrescentarei também tutoriais sobre como usar o sistema.
2. As tarefas são individuais e nenhum tipo de cópia ou similaridade com código, seja de outro aluno, seja da Internet ou livros, será aceita.

# Prazo

O prazo **sugerido** para entrega da atividade é o dia 26/setembro. Você pode exceder esse prazo, mas nesse dia outra tarefa será lançada.

<!--
Validação de número de CPF


123456789-09
numero    9 8 7 6 5 4 3 2 1
digito    8 7 6 5 4 3 2 1 0
contrib. 10 9 8 7 6 5 4 3 2 (errado = tirado da tabela)



1. Encontrar os dígitos de um número de CPF na forma de uma lista de inteiros.
2. Retorna a colaboração do dígito `n` no cálculo do índice v1.

3. Gerar uma lista com todas as colaborações dos dígitos para cálculo de v1.

3. Retorna o valor de v1.

2. Retorna a colaboração do dígito n no cálculo do índice v2.

3. Gerar uma lista com todas as colaborações dos dígitos para cálculo de v2.

3. Retorna o valor de v2.

4. Testa se CPF é igual a 11111111 ou 00000 (todos os digitos iguais o CPF deve ser ocnsiderado inválido)

4. Verifica se um dado CPf está válido

5. Gera um número de CPF válido, aleatório.







https://pt.wikipedia.org/wiki/Cadastro_de_pessoas_f%C3%ADsicas

https://laennder.com/como-e-feito-o-calculo-de-validacao-cpf/


com os nove dígitos

1. Encontrar os dígitos de um número de CPF na forma de uma lista de inteiros.

paraInteiros
paraInteirosRev

paraDigitos 1234 == [1,2,3,4]

module Test where

import Data.Char

paraInteiros :: [Char] -> [Int]
paraInteiros (n:[]) = digitToInt n
paraInteiros (d:ds) = [0]

main = digitToInt (head "03148393724")

só deve considerar os 9 primeiros, no caso de validação.

2. Retorna a colaboração do dígito n no cálculo do índice v1.

3. Gerar ums lista com todas as colaborações dos dígitos para cálculo de v1.

3. Retorna o valor de v1.

2. Retorna a colaboração do dígito n no cálculo do índice v2.

3. Gerar uma lista com todas as colaborações dos dígitos para cálculo de v2.

3. Retorna o valor de v2.

4. Testa se CPF é igual a 11111111 ou 00000 (todos os digitos iguais o CPF deve ser ocnsiderado inválido)

4. Verifica se um dado CPf está válido

5. Gera um número de CPF válido, aleatório.

-->


</xmp>

<script src="http://strapdownjs.com/v/0.2/strapdown.js"></script>
</html>
