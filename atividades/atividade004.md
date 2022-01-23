# Tarefa 004
Atividade de Análise do Valor Limite - Definição de Casos de Teste.

Aula do dia 18/01/2022.

## Classes de Equivalência

|  ID  | Descrição         | V/I |
|:----:| ----------------- |:---:|
| CE01 | nota1 < 0         |  I  |
| CE02 | nota1 > 10.00     |  I  |
| CE03 | 0 ≤ nota1 ≤ 10.00 |  V  |
| CE04 | nota2 < 0         |  I  |
| CE05 | nota2 > 10.00     |  I  |
| CE06 | 0 ≤ nota2 ≤ 10.00 |  V  |
| CE07 | cargaHoraria < 0  |  I  |
| CE08 | cargaHoraria ≥ 0  |  V  |
| CE09 | faltas < 0        |  I  |
| CE10 | faltas ≥ 0        |  V  |

- **CE**: Classe de Equivalência, seguido de um número sequencial;
- **Descrição**: define um cenário de teste;
- **V/I**: Válida ou Inválida.

## Conjunto de Casos de Teste

|  CT  | Valor de Entrada       | Resultado Esperado                                       | Classe de Equivalência |
|:----:| ---------------------- | -------------------------------------------------------- | ---------------------- |
| CT01 | -1.0, 6.0, 64, 4       | Parâmetro nota1 inválido                                 | CE01, CE06, CE08, CE10 |
| CT02 | 0.0, 6.0, 64, 4        | Recuperação                                              | CE03, CE06, CE08, CE10 |
| CT03 | 1.0, 6.0, 64, 4        | Recuperação                                              | CE03, CE06, CE08, CE10 |
| CT04 | 9.0, 6.0, 64, 4        | Aprovado                                                 | CE01, CE06, CE08, CE10 |
| CT05 | 10.0, 6.0, 64, 4       | Aprovado                                                 | CE03, CE06, CE08, CE10 |
| CT06 | 11.0, 6.0, 64, 4       | Parâmetro nota1 inválido                                 | CE02, CE06, CE08, CE10 |
| CT07 | 6.0, -1.0, 64, 4       | Parâmetro nota2 inválido                                 | CE01, CE06, CE08, CE10 |
| CT08 | 6.0, 0.0, 64, 4        | Recuperação                                              | CE03, CE06, CE08, CE10 |
| CT09 | 6.0, 1.0, 64, 4        | Recuperação                                              | CE03, CE06, CE08, CE10 |
| CT10 | 6.0, 9.0, 64, 4        | Aprovado                                                 | CE01, CE06, CE08, CE10 |
| CT11 | 6.0, 10.0, 64, 4       | Aprovado                                                 | CE03, CE06, CE08, CE10 |
| CT12 | 6.0, 11.0, 64, 4       | Parâmetro nota2 inválido                                 | CE02, CE06, CE08, CE10 |
| CT13 | 6.0, 6.0, -1, 0        | Parâmetro cargaHoraria inválido                          | CE03, CE05, CE07, CE10 |
| CT14 | 6.0, 6.0, 0, 0         | Aprovado                                                 | CE03, CE05, CE08, CE10 |
| CT15 | 6.0, 6.0, 1, 0         | Aprovado                                                 | CE03, CE05, CE08, CE10 |
| CT16 | 6.0, 6.0, 64, -1       | Parâmetro faltas inválido                                | CE03, CE05, CE08, CE09 |
| CT17 | 6.0, 6.0, 64, 0        | Aprovado                                                 | CE03, CE05, CE08, CE10 |
| CT18 | 6.0, 6.0, 64, 1        | Aprovado                                                 | CE03, CE05, CE08, CE10 |

- **CT**: Caso de Teste, seguido de um valor sequencial;
- **Valor de entrada**: valor informado para as variáveis na ordem nota1, nota2, cargaHoraria e faltas;
- **Resultado esperado**: resultado que se espera da execução da função;
- **Classe de Equivalência**: identificação de qual classe de equivalência está sendo exercitada pelo caso de teste.