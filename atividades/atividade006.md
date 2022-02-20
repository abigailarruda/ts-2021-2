# Tarefa 006
Atividade de Grafo de Fluxo de Controle.

Aula do dia 15/02/2022.

## Código

~~~java
public class Avaliacao {
1    public String avalia(double nota1, double nota2, int faltas, int cargaHoraria) throws ValoresInvalidosException {
2        String result;
3        double percentualFaltas = (faltas * 100 / cargaHoraria);
4        double media = (nota1 + nota2) / 2;
5        if ((nota1 < 0.0 || nota1 > 10) || (nota2 < 0.0 || nota2 > 10) || (faltas < 0 || faltas > cargaHoraria) || cargaHoraria < 0) {
6            throw new ValoresInvalidosException(); //result = "Valores Inválidos.";
7        } else if (percentualFaltas > 25.0) {
8           result = "Reprovado por Falta.";
9        } else if (media < 3.0) {
10           result = "Reprovado por Média.";
11       } else if (media >= 3.0 && media < 6.0) {
12           result = "Prova Extra.";
13       } else {
14           result = "Aprovado.";
15       }
16       return result;
17    }
18 }
~~~

## Grafos de Fluxo de Controle

<p align="center">
  <img src="https://i.imgur.com/SywJoga.png" width="70%"/>
</p>

### Grafo com o plugin no Eclipse

<p align="center">
  <img src="https://i.imgur.com/sfglIxl.png" width="70%"/>
</p>

## Complexidade ciclomática do código

V(G) = E – N + 2

V(G) = 16 - 13 + 2

V(G) = 5

## Caminhos de execução

Os caminhos possíveis são:

- ABCK
- ABDEK
- ABDFGK
- ABDFHIK
- ABDFHJK

## Casos de testes

|CT  |Valor de Entrada      |Resultado Esperado                                      |
|:--:|----------------------|--------------------------------------------------------|
|CT01|-1.0, 11.0, 0, -8     |Valores Inválidos.                                      |
|CT02|8.0, 7.0, 64, 20      |Reprovado por Falta.                                    |
|CT03|2.0, 1.0, 48, 2       |Reprovado por Média.                                    |
|CT04|5.0, 6.0, 128, 4      |Prova Extra.                                            |
|CT05|9.0, 10.0, 64, 16     |Aprovado.                                               |

- **CT**: Caso de Teste, seguido de um valor sequencial;
- **Valor de entrada**: valor informado para as variáveis na ordem nota1, nota2, cargaHoraria e faltas;
- **Resultado esperado**: resultado que se espera da execução da função;