# Tarefa 005
Atividade de Grafo de Causa e Efeito/Tabela de Decisão.

Aula do dia 08/02/2022.

## Cenário

Uma corretora de seguros concede desconto sobre o prêmio anual de seguro de automóvel, aos seus segurados conforme as regras a seguir:

|Regra |Sexo     |Idade (Anos)|Estado Civil|Desconto (%)|
|:----:|:-------:|:----------:|:----------:|:----------:|
|01    |Masculino|< 25        |Solteiro    |0           |
|02    |Masculino|< 25        |Casado      |5           |
|03    |Masculino|> 25        |Solteiro    |10          |
|04    |Masculino|> 25        |Casado      |15          |
|05    |Feminino |< 25        |Solteira    |5           |
|06    |Feminino |< 25        |Casada      |10          |
|07    |Feminino |> 25        |Solteira    |15          |
|08    |Feminino |> 25        |Casada      |20          |

## Grafo de Causa e Efeito

<p align="center">
  <img src="https://i.imgur.com/56ed2cF.png"/>
</p>

## Tabela de Decisão

|           |Descrição                 |Regra 01|Regra 02|Regra 03|Regra 04|Regra 05|Regra 06|Regra 07|Regra 08|
|:---------:|--------------------------|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
|**Causas** |                          |        |        |        |        |        |        |        |        |
|C01        |É do sexo masculino       |V       |V       |V       |V       |F       |F       |F       |F       |
|C02        |Idade é maior que 25 anos |F       |F       |V       |V       |F       |F       |V       |V       |
|C03        |Estado civil é solteiro(a)|V       |F       |V       |F       |V       |F       |V       |F       |
|**Efeitos**|                          |        |        |        |        |        |        |        |        |
|E01        |0% de desconto            |X       |        |        |        |        |        |        |        |
|E02        |5% de desconto            |        |X       |        |        |X       |        |        |        |
|E03        |10% de desconto           |        |        |X       |        |        |X       |        |        |
|E04        |15% de desconto           |        |        |        |X       |        |        |X       |        |
|E05        |20% de desconto           |        |        |        |        |        |        |        |X       |

## Casos de Teste

Considerando o valor do seguro de R$2000,00 (dois mil reais).

|                         |CT1      |CT2      |CT3      |CT4      |CT5      |CT6      |CT7      |CT8      |
|-------------------------|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|
|**Entradas**             |         |         |         |         |         |         |         |         |
|C01                      |True     |True     |True     |True     |False    |False    |False    |False    |
|C02                      |False    |False    |True     |True     |False    |False    |True     |True     |
|C03                      |True     |False    |True     |False    |True     |False    |True     |False    |
|**Resultados Esperados** |         |         |         |         |         |         |         |         |
|E01                      |R$2000,00|-        |-        |-        |-        |-        |-        |-        |
|E02                      |-        |R$1900,00|-        |-        |R$1900,00|-        |-        |-        |
|E03                      |-        |-        |R$1800,00|-        |-        |R$1800,00|-        |-        |
|E04                      |-        |-        |-        |R$1700,00|-        |-        |R$1700,00|-        |
|E05                      |-        |-        |-        |-        |-        |-        |-        |R$1600,00|
