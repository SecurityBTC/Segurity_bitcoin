https://github.com/bitcoin-core/bitcoincore.org/tree/38f40a5949cbdef8a0453c7d030268568b052424
Segurança
Percepções
bitcoin/ .style.yapf
@MarcoFalke
MarcoFalke test: .style.yapf: Set column_limit=160
 1 contributor
261 linhas (215 sloc)  7,76 KB
[estilo]
# Alinhar o suporte de fechamento com o recuo visual.
align_closing_bracket_with_visual_indent=Verdadeiro

# Permitir que as chaves do dicionário existam em várias linhas. Por exemplo:
#
#x = {
# ('este é o primeiro elemento de uma tupla',
# 'este é o segundo elemento de uma tupla'):
# valor,
# }
allow_multiline_dictionary_keys=Falso

# Permite que lambdas sejam formatados em mais de uma linha.
allow_multiline_lambdas=Falso

# Permite divisões antes do valor do dicionário.
allow_split_before_dict_value=Verdadeiro

# Número de linhas em branco ao redor da função e classe de nível superior
#definições.
blank_lines_around_top_level_definition=2

# Insira uma linha em branco antes de uma docstring de nível de classe.
blank_line_before_class_docstring=Falso

# Insira uma linha em branco antes de uma docstring do módulo.
blank_line_before_module_docstring=Falso

# Insira uma linha em branco antes de um 'def' ou 'class' imediatamente aninhado
# dentro de outro 'def' ou 'class'. Por exemplo:
#
#classe Foo:
# # <------ esta linha em branco
# método def():
#...
blank_line_before_nested_class_or_def=Falso

# Não divida colchetes consecutivos. Apenas relevante quando
# dedent_closing_brackets está definido. Por exemplo:
#
# call_func_that_takes_a_dict(
#{
# 'chave1': 'valor1',
# 'chave2': 'valor2',
# }
#)
#
# reformataria para:
#
# call_func_that_takes_a_dict({
# 'chave1': 'valor1',
# 'chave2': 'valor2',
# })
coalesce_brackets=Falso

# O limite da coluna.
column_limit=160

# O estilo para alinhamento de continuação. Os valores possíveis são:
#
# - ESPAÇO: Use espaços para alinhamento de continuação. Este é o comportamento padrão.
# - FIXED: Use um número fixo (CONTINUATION_INDENT_WIDTH) de colunas
# (ou seja: guias CONTINUATION_INDENT_WIDTH/INDENT_WIDTH) para continuação
#alinhamento.
# - MENOS: Ligeiramente à esquerda se não puder alinhar verticalmente as linhas de continuação com
# caracteres de recuo.
# - VALIGN-RIGHT: Alinha verticalmente as linhas de continuação com o recuo
# personagens. Ligeiramente à direita (mais um caractere de recuo) se não puder
# alinha verticalmente as linhas de continuação com caracteres de recuo.
#
# Para as opções FIXED e VALIGN-RIGHT estão disponíveis apenas quando USE_TABS é
# ativado.
continuation_align_style=ESPAÇO

# Largura do recuo usada para continuações de linha.
continuação_indent_width=4

# Coloque colchetes de fechamento em uma linha separada, dentada, se o colchete
# expressão não pode caber em uma única linha. Aplica-se a todos os tipos de suportes,
# incluindo definições de função e chamadas. Por exemplo:
#
#configuração = {
# 'chave1': 'valor1',
# 'chave2': 'valor2',
# } # <--- este colchete é denteado e em uma linha separada
#
# time_series = self.remote_client.query_entity_counters(
# entidade='dev3246.region1',
# key='dns.query_latency_tcp',
# transform=Transformation.AVERAGE(window=timedelta(seconds=60)),
# start_ts=now()-timedelta(days=3),
# end_ts=agora(),
# ) # <--- este colchete é denteado e em uma linha separada
dedent_closing_brackets=Falso

# Desabilite a heurística que coloca cada elemento da lista em uma linha separada
# se a lista for terminada por vírgula.
disable_ending_comma_heuristic=Falso

# Coloque cada entrada do dicionário em sua própria linha.
each_dict_entry_on_separate_line=Verdadeiro

# O regex para um comentário i18n. A presença deste comentário pára
# reformatação dessa linha, pois os comentários devem ser
# ao lado da string que eles traduzem.
i18n_comment=

# Os nomes de chamada de função i18n. A presença desta função pára
# reformatando nessa linha, pois a string que ela possui não pode ser movida
# longe do comentário i18n.
i18n_function_call=

# Recua o valor do dicionário se não couber na mesma linha que o
# chave do dicionário. Por exemplo:
#
#configuração = {
# 'chave1':
# 'valor1',
# 'chave2': valor1 +
# valor2,
# }
indent_dictionary_value=Falso

# O número de colunas a serem usadas para recuo.
indent_width=4

# Junte linhas curtas em uma linha. Por exemplo, declarações 'se' de linha única.
join_multiple_lines=Verdadeiro

# Não inclua espaços em torno de operadores binários selecionados. Por exemplo:
#
# 1 + 2 * 3 - 4/5
#
# será formatado da seguinte forma quando configurado com "*,/":
#
# 1 + 2*3 - 4/5
#
no_spaces_around_selected_binary_operators=

# Use espaços em torno de atribuições padrão ou nomeadas.
espaços_around_default_or_named_assign=Falso

# Use espaços ao redor do operador de potência.
espaços_around_power_operator=Falso

# O número de espaços necessários antes de um comentário final.
espaços_antes_comment=2

# Insira um espaço entre a vírgula final e o colchete de fechamento de uma lista,
#etc
space_between_ending_comma_and_closing_bracket=Verdadeiro

# Dividir antes dos argumentos
split_all_comma_separated_values=Falso

# Dividir antes dos argumentos se a lista de argumentos for terminada por um
# vírgula.
split_arguments_when_comma_terminated=Falso

# Defina como True para preferir a divisão antes de '&', '|' ou '^' em vez de
# depois.
split_before_bitwise_operator=Verdadeiro

# Dividir antes do colchete de fechamento se uma lista ou literal dict não couber
# uma única linha.
split_before_closing_bracket=Verdadeiro

# Dividir antes de um dicionário ou gerador de conjunto (comp_for). Por exemplo, observe
# a divisão antes do 'for':
#
# foo = {
# variável: 'Olá mundo, tenha um bom dia!'
# para variável na barra se variável != 42
# }
split_before_dict_set_generator=Verdadeiro

# Dividido antes do '.' se precisarmos dividir uma expressão mais longa:
#
# foo = ('Esta é uma string muito longa: {}, {}, {}, {}'.format(a, b, c, d))
#
# reformataria para algo como:
#
# foo = ('Esta é uma string muito longa: {}, {}, {}, {}'
# .formato(a, b, c, d))
split_before_dot=Falso

# Dividir após o parêntese de abertura que envolve uma expressão se não o fizer
# cabe em uma única linha.
split_before_expression_after_opening_paren=Falso

# Se um argumento / lista de parâmetros vai ser dividido, então divida antes
# o primeiro argumento.
split_before_first_argument=Falso

# Defina como True para preferir dividir antes de 'e' ou 'ou' em vez de
# depois.
split_before_logical_operator=Verdadeiro

# Divida as atribuições nomeadas em linhas individuais.
split_before_named_assigns=Verdadeiro

# Defina como True para dividir as compreensões e geradores de listas que
# expressões não triviais e várias cláusulas antes de cada uma delas
# cláusulas. Por exemplo:
#
# resultado = [
# a_long_var + 100 para a_long_var em xrange(1000)
# if a_long_var % 10]
#
# reformataria para algo como:
#
# resultado = [
# a_long_var + 100
# para a_long_var em xrange(1000)
# if a_long_var % 10]
split_complex_comprehension=Falso

# A penalidade por dividir logo após a chave de abertura.
split_penalty_after_opening_bracket=30

# A penalidade por dividir a linha após um operador unário.
split_penalty_after_unary_operator=10000

# A penalidade por dividir logo antes de uma expressão if.
split_penalty_before_if_expr=0

# A penalidade de dividir a linha em torno de '&', '|' e '^'
# operadores.
split_penalty_bitwise_operator=300

# A penalidade por dividir uma compreensão ou gerador de lista
#expressão.
split_penalty_comprehension=80

# A penalidade para caracteres acima do limite da coluna.
split_penalty_excess_character=7000

# A penalidade incorrida ao adicionar uma divisão de linha à linha desempacotada. o
# mais divisões de linha adicionadas quanto maior a penalidade.
split_penalty_for_added_line_split=30

# A penalidade de dividir uma lista de nomes "importar como". Por exemplo:
#
# de a_very_long_or_indented_module_name_yada_yad import (long_argument_1,
# argumento_longo_2,
# argumento_longo_3)
#
# reformataria para algo como:
#
# de a_very_long_or_indented_module_name_yada_yad import (
# argumento_longo_1, argumento_longo_2, argumento_longo_3)
split_penalty_import_names=0

# A penalidade de dividir a linha em torno do 'e' e 'ou'
# operadores.
split_penalty_logical_operator=300

# 
