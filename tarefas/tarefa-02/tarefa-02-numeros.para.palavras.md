<!DOCTYPE html>
<html>
<title>Programa��o Funcional e L�gica - Prof. Ricardo da Rocha</title>

<xmp theme="simplex" style="display:none;">


# Tarefa 2 de Programa��o Funcional e L�gica

# Vis�o geral

Nesta tarefa voc� dever� implementar algumas fun��es para exercitar o uso de recurs�o dos tipos b�sicos de Haskell. 


# Descri��o

1. Resolva as [tarefas de 7 a 10](labs/03-pf-tarefas-listas.hs), deixadas para o laborat�rio
2. Implemente uma fun��o `numeralParaExtenso n` (`n :: Integer`) que recebe um inteiro positivo e retorna o n�mero por extenso em uma `String`, at� n�mero limite de `9.999.999.999` (�ltima da casa dos bilh�es). Por exemplo:

   * `numeralParaExtenso 0 => zero`
   * `numeralParaExtenso 99 => noventa e nove`
   * `numeralParaExtenso 1121 => mil cento e vinte e um`
   * `numeralParaExtenso 1014 => mil e quatorze`
   * `numeralParaExtenso 1256759 => um milhao, duzentos e cinquenta e seis, setecentos e cinquenta e nove`

3. Implemente um fun��o `combinacoes n lista` que gera uma lista de todas as combina��es poss�veis de `n` elementos da lista `lista`. O n�mero poss�vel � a formula de combina��es C(p,n), onde p � o n�mero de elementos e p o tamanho da combina��o (para 12 elementos 3 a 3, h� 220 poss�veis valores). Exemplo:

   * `combinacoes 3 "123456" => ["123", "124", "125", ...`


# Requisitos

Reveja o [plano da disciplina](http://inf.ufg.br/~ricardo/pfl/plano/plano-PFL-2018.2.pdf) na se��o "PROCESSOS E CRIT�RIOS DE AVALIA��O", caso seja necess�rio relembrar como as tarefas ser�o avaliadas.

Os seguintes requisitos devem ser satisfeitos para o seu c�digo ter o conceito **FINALIZADO**.

1. Todas as fun��es implementadas devem incluir c�digo de teste, para al�m das fun��es indicadas acima.
1. O seu c�digo dever� ser submetido pelo [GitHub Classroom](https://classroom.github.com/), no local que ser� indicado at� o dia 8 de outubro. Acrescentarei tamb�m tutoriais sobre como usar o sistema.
2. As tarefas s�o individuais e nenhum tipo de c�pia ou similaridade com c�digo, seja de outro aluno, seja da Internet ou livros, ser� aceita.

# Prazo

O prazo **sugerido** para entrega da atividade � o dia 8/outubro. Voc� pode exceder esse prazo, mas nesse dia outra tarefa ser� lan�ada.

</xmp>

<script src="http://strapdownjs.com/v/0.2/strapdown.js"></script>
</html>

