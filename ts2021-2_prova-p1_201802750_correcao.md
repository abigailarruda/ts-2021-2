<div align=center>
  <img src="https://i.imgur.com/mEEC95H.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>
#### <p style="text-align: center;">Instituto de Informática</p>
#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>
#### <p style="text-align: center;">Teste de Software - 2021/2</p>
#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>
#### <p style="text-align: center;">Prova P1 - 16/02/2022</p>

Matrícula: 201802750.

Nome: Abigail de Jesus Arruda.

<p><font color=green><b>Nota 10</b></font></p>

1. Quanto ao objetivo do Teste de Software, responda as duas questões seguintes:
   1. (**0,5 ponto**) Qual o objetivo primário da atividade de teste de software?
**R:** O objetivo primário do teste de software é revelar a presença de defeitos. <font color="green">Certo</font>

   2. (**0,5 ponto**) O que acontece, quando não se atinge este objetivo primário?
**R:** Quando não é revelada a presença de defeitos em um software, isso não significa que ele seja livre dos mesmos, mas sim que os testes não foram bem sucedidos. Todos os softwares têm defeitos, mas os bons não possuem defeitos críticos não corrigidos. <font color=green>Certo</font>

2. (**1,0 ponto**) Explique o que é o teste exaustivo e porque sua execução não é possível.

**R:** O teste exaustivo é aquele em que todas as possibilidades são testadas (todos os dados de entrada), de modo a encontrar a maior quantidade de defeitos provável. Apesar das diversas formas de se realizá-lo, sua execução não é possível devido ao grande número de combinações e situações que podem ocorrer, além de cenários e pré-condições dentro da aplicação. <font color=green>Certo</font>

3. (**1,0 ponto**) Cite pelo menos duas limitações da Técnica de Teste Funcional e duas da Técnica de Teste Estrutural.

**R:** Limitações da Técnica de Teste Funcional: depende de uma boa especificação de requisitos e para encontrar todos os defeitos é necessário utilizar o teste exaustivo. <font color=green>Certo</font>
Limitações da Técnica de Teste Estrutural: o número de caminhos pode ser infinito ou muito grande, como em casos em que cada decisão dobra e cada loop multiplica os caminhos, e defeitos podem existir mesmo com o fluxo de controle correto. <font color=green>Certo</font>

4. (**1,0 ponto**) Descreva pelo menos um dos quatro níveis de teste constantes da literatura especializada.

**R:** Os quatro níveis de teste constantes são: teste de unidade, de integração, de sistema e de aceitação. O teste de unidade tem como objetivo a exploração da menor unidade do projeto, de forma a provocar falhas ocasionadas por defeitos de lógica e implementação em cada módulo; seus alvos são os métodos dos objetos e pequenos trechos de código. <font color=green>Certo</font>

5. (**1.0 ponto**) Descreva qual o propósito do critério de teste funcional Particionamento por Classes de Equivalência.

**R:** O propósito do particionamento por classes de equivalência é diminuir a quantidade de casos de testes para garantir uma boa cobertura do código do produto. Ou seja, seu propósito é dividir o domínio de entrada de um software em classes de dados, a partir das quais os casos de teste podem ser derivados. <font color=green>Certo</font>

6. (**1.00 ponto**) Existe algum tipo de hierarquia em relação aos critérios de teste estrutural, todos os nós, todos os arcos e todos os caminhos? Se sim, explique-a, considerando a perspectiva dos níveis de cobertura desejados.

**R:** Sim, existe uma hierarquia definida por oito diferentes níveis de cobertura, definida por Copeland, em que quanto maior o nível, maior o rigor do critério. O nível que define critérios em relação a todos os nós é o de número 1, chamado de "todos-nós", enquanto o Nível 2 é chamado de "todos-arcos" e o Nível 7, "todos-caminhos". O Nível 1 define que cada instrução deve ser executada pelo menos uma vez. O Nível 2 faz com que cada comando de decisão assumir os valores true e false. O Nível 7, em programas sem loop, pode possuir um número de caminhos pequeno o suficiente. <font color=green>Certo</font>

7. Considere a especificação, a seguir, de um hipotético programa que objetiva a classificação de um triângulo, a partir dos valores informados para os seus três lados.

   a) Dado um triângulo cujos segmentos medem A, B e C, que são números inteiros positivos na faixa de 0 a 100. Esse triângulo somente existirá se: (A + B > C) ou (A + C > B) ou (B + C > A).
   b) Quanto às medidas dos seus lados o triângulo, poderá ser classicado em:
         • Isósceles = quando possui dois lados com a mesma medida;
         • Escaleno = quando todos os seus lados têm medidas diferentes;
         • Equilátero = quando todos os lados tem a mesma medida;
         • Acutângulo = quando o quadrado de um dos seus lados é menor que a soma do quadrado dois outros dois. (A<sup>2</sup> < B<sup>2</sup> + C<sup>2</sup>).
         • Retângulo: quando o quadrado de um dos seus lados é igual à soma do quadrado dois outros dois. (A<sup>2</sup> = B<sup>2</sup> + C<sup>2</sup>).
         • Obtusângulo: quando o quadrado de um dos seus lados é maior que a soma do quadrado dois outros dois. A<sup>2</sup> > B<sup>2</sup> + C<sup>2</sup>.

7.1 (**2.0 pontos**) Definir uma tabela de decisão para o teste tanto da existência do triângulo, quanto para a definição do seu tipo. Consulte exemplo de tabela de decisão na tarefa 005.

|           |Descrição                                 |Regra 1|Regra 2|Regra 3|Regra 4|Regra 5|Regra 6|Regra 7|Regra 8|Regra 9|
|:---------:|------------------------------------------|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|**Causas** |                                          |       |       |       |       |       |       |       |       |       |
|C01        |(A + B > C) ou (A + C > B) ou (B + C > A) |F      |V      |V      |V      |V      |V      |V      |V      |V      |
|C02        |A = B                                     |N/A    |V      |V      |V      |F      |F      |V      |F      |F      |
|C03        |A = C                                     |N/A    |V      |V      |F      |F      |V      |F      |V      |F      |
|C04        |B = C                                     |N/A    |V      |F      |F      |F      |V      |V      |F      |V      |
|**Efeitos**|                                          |       |       |       |       |       |       |       |       |       |
|E01        |Isósceles                                 |-      |-      |-      |X      |-      |-      |-      |X      |X      |
|E02        |Escaleno                                  |-      |-      |-      |-      |X      |-      |-      |-      |-      |
|E03        |Equilátero                                |-      |X      |-      |-      |-      |-      |-      |-      |-      |
|E04        |Impossível                                |-      |-      |X      |-      |-      |X      |X      |-      |-      |
|E05        |Não é triângulo                           |X      |-      |-      |-      |-      |-      |-      |-      |-      |

<font color=green>Certo</font>

7.2 (**2.0 pontos**) Criar os conjunto de casos de teste necessários para a cobertura das combinações constantes da tabela de decisão, seguindo o seguinte padrão:

|CT  |Lado A|Lado B|Lado C|Resultado      |
|:--:|:----:|:----:|:----:|:-------------:|
|CT01|9     |7     |14    |Escaleno       |
|CT02|13    |13    |13    |Equilátero     |
|CT03|13    |8     |25    |Não é triângulo|
|CT04|9     |9     |12    |Isósceles      |

<font color=green>Certo</font>

**Observações:** houve a inversão dos sinais nos critérios de existência de um triângulo. A questão também foi modificada, de acordo com o e-mail enviado pelo professor durante a avaliação.
