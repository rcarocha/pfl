<!DOCTYPE html>
<html>
<title>Programação Funcional e Lógica - Prof. Ricardo da Rocha</title>

<xmp theme="simplex" style="display:none;">


# Tarefa 2 de Programação Funcional e Lógica

# Visão geral

Nesta tarefa você deverá implementar algumas funções para exercitar o uso de recursão dos tipos básicos de Haskell. 


# Descrição

1. Resolva as [tarefas de 7 a 10](labs/03-pf-tarefas-listas.hs), deixadas para o laboratório
2. Implemente uma função `numeralParaExtenso n` (`n :: Integer`) que recebe um inteiro positivo e retorna o número por extenso em uma `String`, até número limite de `9.999.999.999` (última da casa dos bilhões). Por exemplo:

   * `numeralParaExtenso 0 => zero`
   * `numeralParaExtenso 99 => noventa e nove`
   * `numeralParaExtenso 1121 => mil cento e vinte e um`
   * `numeralParaExtenso 1014 => mil e quatorze`
   * `numeralParaExtenso 1256759 => um milhao, duzentos e cinquenta e seis, setecentos e cinquenta e nove`

3. Implemente um função `combinacoes n lista` que gera uma lista de todas as combinações possíveis de `n` elementos da lista `lista`. O número possível é a formula de combinações C(p,n), onde p é o número de elementos e p o tamanho da combinação (para 12 elementos 3 a 3, há 220 possíveis valores). Exemplo:

   * `combinacoes 3 "123456" => ["123", "124", "125", ...`


# Requisitos

Reveja o [plano da disciplina](http://inf.ufg.br/~ricardo/pfl/plano/plano-PFL-2018.2.pdf) na seção "PROCESSOS E CRITÉRIOS DE AVALIAÇÃO", caso seja necessário relembrar como as tarefas serão avaliadas.

Os seguintes requisitos devem ser satisfeitos para o seu código ter o conceito **FINALIZADO**.

1. Todas as funções implementadas devem incluir código de teste, para além das funções indicadas acima.
1. O seu código deverá ser submetido pelo [GitHub Classroom](https://classroom.github.com/), no local que será indicado até o dia 8 de outubro. Acrescentarei também tutoriais sobre como usar o sistema.
2. As tarefas são individuais e nenhum tipo de cópia ou similaridade com código, seja de outro aluno, seja da Internet ou livros, será aceita.

# Prazo

O prazo **sugerido** para entrega da atividade é o dia 8/outubro. Você pode exceder esse prazo, mas nesse dia outra tarefa será lançada.

</xmp>

<script src="http://strapdownjs.com/v/0.2/strapdown.js"></script>
</html>

