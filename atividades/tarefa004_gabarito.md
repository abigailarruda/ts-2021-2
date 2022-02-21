
## Tarefa 004 - 19/01/2022 - Análise do Valor Limte - Definição de casos de testes.

Vamos considerar o conjunto de classes de equivalência definidos na solução da tarefa 003, com as seguintes considerações:
  1. dentre as quatro variáveis de entrada, a variável "cargaHoraria" não será foco do teste, tendo em vista que os valores definidos para seu teste fazem parte de um conjunto de valores. Neste caso, não se aplica o critério "Análise do Valor Limite". Vamos usar aleatoriamente qualquer valor pertencente ao conjunto **ch = {32, 64, 96 e 128}**.
  2. Em relação à variável faltas, os limites testados serão, aqueles pertinentes ao tipo de dado, quanto aqueles valores referentes ao percentual de 25% da cargaHoraria, e ainda a situação em que a quantidade de faltas seja superior à carga horária.



a) Os três primeiros casos de teste, visam validar o valor imediatamente inferior ao limite inferior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:

|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT01|-0,01,7.00,64,8|"Valores Inválidos|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE38|
|CT02|7.00,-0.01,32,8|"Valores Inválidos|CE02,CE04,CE06,CE10,CE13,CE14,CE16,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE38|
|CT03|7.00,5.00,64,-1|"Valores Inválidos|CE02,CE04,CE06,CE10,CE13,CE14,CE16,CE20,CE23,CE24,CE27,CE29,CE30,CE32,CE37,CE38|

b) Os próximos três casos de teste, visam validar o limite inferior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|0,00,7.00,64,8|"Recuperação"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE41|
|CT04|7.00,0.00,32,8|"Recuperação"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE41|
|CT05|7.00,5.00,64,0|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|

c) Os próximos três casos de teste, visam validar o valor imediatamente superior ao limite inferior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|0,01,7.00,64,8|"Recuperação"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE41|
|CT04|7.00,0,01,32,8|"Recuperação"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE41|
|CT05|7.00,5.00,64,1|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|

d) Os próximos três casos de teste, visam validar o comportamento da variável faltas em relação ao percentual de 25% da carga horária. Desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|5,00,7.00,64,15|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT04|5.00,7.00,64,16|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT05|5.00,7.00,64,17|"Reprovado por Faltas"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE34,CE37,CE39|

d) Os três primeiros casos de teste, visam validar o valor imediatamente inferior ao limite superior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|9,99,7.00,64,15|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT04|5.00,9.99,64,16|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT05|5.00,7.00,64,63|"Reprovado por Faltas"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE34,CE37,CE39|

e) Os três primeiros casos de teste, visam validar o limite superior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|10,00,7.00,64,15|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT04|5.00,10.00,64,16|"Aprovado"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE42|
|CT05|5.00,7.00,64,64|"Reprovado por Faltas"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE34,CE37,CE39|

f) Os três primeiros casos de teste, visam validar o valor imediatamente superior ao limite superior das variáveis **nota1**, **nota2** e **faltas**, desta forma teremos:
|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT03|10,01,7.00,64,15|"Valores Inválidos"|CE02,CE04,CE08,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE38|
|CT04|5.00,10.01,64,16|"Valores Inválidos"|CE02,CE04,CE06,CE10,CE13,CE14,CE18,CE20,CE23,CE24,CE27,CE29,CE30,CE33,CE37,CE38|
|CT05|5.00,7.00,64,65|"Valores Inválidos"|CE02,CE04,CE06,CE10,CE13,CE14,CE17,CE20,CE23,CE24,CE27,CE29,CE35,CE34,CE37,CE38|
