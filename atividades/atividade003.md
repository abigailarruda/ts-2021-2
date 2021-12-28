# Tarefa 003
Atividade de Definição de Classes de Equivalência.

Aula ministrada no dia 21/12/2021.

## Classes de Equivalência

|ID  |Descrição         |V/I  |
|:--:|------------------|:---:|
|CE01|nota1 < 0         |I    |
|CE02|nota1 > 10.00     |I    |
|CE03|0 ≤ nota1 ≤ 10.00 |V    |
|CE04|nota2 < 0         |I    |
|CE05|nota2 > 10.00     |I    |
|CE06|0 ≤ nota2 ≤ 10.00 |V    |
|CE07|cargaHoraria < 0  |I    |
|CE08|cargaHoraria ≥ 0  |V    |
|CE09|faltas < 0        |I    |
|CE10|faltas ≥ 0        |V    |

- **CE**: Classe de Equivalência, seguido de um número sequencial;
- **Descrição**: define um cenário de teste;
- **V/I**: Válida ou Inválida.

## Conjunto de Casos de Teste

|CT  |Valor de Entrada      |Resultado Esperado                                      |Classe de Equivalência|
|:--:|----------------------|--------------------------------------------------------|----------------------|
|CT01|8.0, 7.0, 128, 8      |Aprovado                                                |CE03, CE06, CE08, CE10|
|CT02|8.0, 7.0, 64, 20      |Reprovado por Falta                                     |CE03, CE06, CE08, CE10|
|CT03|2.0, 1.0, 48, 2       |Reprovado por Média                                     |CE03, CE06, CE08, CE10|
|CT04|5.0, 6.0, 128, 4      |Recuperação                                             |CE03, CE06, CE08, CE10|
|CT05|9.0, 10.0, 64, 16     |Aprovado                                                |CE03, CE06, CE08, CE10|
|CT06|-1.0, 10.0, 32, 0     |Parâmetro nota1 inválido                                |CE01, CE06, CE08, CE10|
|CT07|3.5, -10.0, 32, 0     |Parâmetro nota2 inválido                                |CE03, CE04, CE08, CE10|
|CT08|15.8, 10.0, 48, 4     |Parâmetro nota1 inválido                                |CE02, CE06, CE08, CE10|
|CT09|2.7, 25.6, 128, 12    |Parâmetro nota2 inválido                                |CE03, CE05, CE08, CE10|
|CT10|6.0, 6.0, -256, 0     |Parâmetro cargaHoraria inválido                         |CE03, CE06, CE07, CE10|
|CT11|5.4, 8.0, 128, -20    |Parâmetro faltas inválido                               |CE03, CE06, CE08, CE09|
|CT12|-2.86, 74.5, -256, -64|Parâmetros nota1, nota2, cargaHoraria e faltas inválidos|CE01, CE05, CE07, CE09|
|CT13|5.0, 0.98, 64, 20     |Reprovado por Falta                                     |CE03, CE06, CE08, CE10|
|CT14|98.0, -2.7, -128, -4  |Parâmetros nota1, nota2, cargaHoraria e faltas inválidos|CE02, CE04, CE07, CE09|
|CT15|6.0, 0.2, 64, 16      |Recuperação                                             |CE03, CE06, CE08, CE10|

- **CT**: Caso de Teste, seguido de um valor sequencial;
- **Valor de entrada**: valor informado para as variáveis na ordem nota1, nota2, cargaHoraria e faltas;
- **Resultado esperado**: resultado que se espera da execução da função;
- **Classe de Equivalência**: identificação de qual classe de equivalência está sendo exercitada pelo caso de teste.