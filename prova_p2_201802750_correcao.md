<div align=center>
  <img src="https://i.imgur.com/Tgr9mLM.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>
#### <p style="text-align: center;">Instituto de Informática</p>
#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>
#### <p style="text-align: center;">Teste de Software - 2021/2</p>
#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>
#### <p style="text-align: center;"> Prova P2 - 12/04/2022</p>

Matrícula: 201802750

Nome: Abigail de Jesus Arruda

<p><font color="green">Nota 6,3</font></p>

1. Quanto ao Processo de Teste de Software, responda as duas questões seguintes:

    1.1. (**0,5 ponto**) Defina os seguintes conceitos Processo de Teste de Software, Projeto de Teste de Software e Plano de Teste de Sofware.

    **R:** Processo de Teste de Software é processo cujo como objetivo é a estruturação e determinação das etapas, das atividades, dos artefatos, dos papéis e das responsabilidades do teste, de forma a organizar e controlar todo o ciclo do teste, para diminuir os riscos e entregar valor ao software. Projeto de Teste de Software descreve a estrutura dos elementos de testes e a realização dos seus casos, especificando os detalhes da abordagem de teste para um requisito do software ou combinação deles e identifica casos de teste associados. Plano de Teste de Software é o documento produzido na condução de um projeto que age como agente integrador entre as atividades de testes, mecanismo de comunicação para os stakeholders e como um guia para execução e controle das atividades de testes.
    <p><font color="red">Nota 0,5</font></p>

   1.2. (**0,5 ponto**) Descreva o relacionamento existente entre estes conceitos.

   **R:** O Processo de Teste de Software aborda como entradas e/ou saídas de suas atividades o Plano de Teste de Software e o Projeto de Teste de Software. O Projeto de Teste de Software auxiliar a definir a abordagem de teste, os tipos, o ambiente e as ferramentas a serem usadas, enquanto o Plano de Teste de Software fornece informações completas sobre tarefas de teste relacionadas.
   <p><font color="red">Nota 0,3</font></p>

2. (**1,0 pontos**) Descreva as vantagens para a equipe de desenvolvimento ao se adotar um processo de teste ágil.

    **R:** As vantagens de se adotar um processo de teste ágil são: os bugs são encontrados, relatados e corrigidos em um curto espaço de tempo, as entregas são mais rápidas em curtas iterações, a gestão de defeitos é mais dinâmica pois é controlada pelo próprio desenvolvedor, entre outras.
    <p><font color="red">Nota 1,0</font></p>

3. (**1,0 ponto**) Cite pelo menos três características do Teste Exploratório.

    **R:** No Teste Exploratório,
      (1) testadores podem interagir com a aplicação da forma como quiserem e usar as informações obtidas para: reagir, alterar o curso e explorar funcionalidades da aplicação sem repressão,
      (2) são ideais para o teste de aplicações web modernas, desenvolvida seguindo metodologias ágeis e
      (3) o testador corre o risco de desperdiçar muito tempo procurando por coisas para testar e tentar consertar os defeitos.
      <p><font color="red">Nota 1,0</font></p>

4. Considere os arquivos .java (Banco.java, Agencia.java, Conta.java e BankValidator.java). Nos próprios arquivos .java estão definidas as regras para cadastramento de cada um deles (Banco, Agencia e Conta). Desta forma, pede-se:
   4.1. (2.0 Pontos) Definir os cenários de teste suficientes para testar o cadastro e movimentações financeiras envolvendo bancos, agências e contas, conforme especificado. Para cada cenário definir os critérios de teste adequados à definição dos seus casos de teste.

#### Banco
|Regra |Número                        |Nome                            |
|:----:|:----------------------------:|:------------------------------:|
|01    |Contém três dígitos inteiros  |Tamanho entre 5 e 100 caracteres|
|02    |Não contém letras             |Não contém números              |
|03    |Não contém números decimais   |Não contém caracteres especiais |

#### Agência
|Regra |Número                                    |Nome                            |Cidade                          |
|:----:|:----------------------------------------:|:------------------------------:|:------------------------------:|
|01    |Contém três e no máximo 5 dígitos inteiros|Tamanho entre 5 e 100 caracteres|Tamanho entre 5 e 100 caracteres|
|02    |Não contém letras                         |Não contém números              |Não contém números              |
|03    |Não contém números decimais               |Não contém caractere especial   |Não contém caracteres especiais |

#### Conta
|Regra |Número                        |Tipo                          |Limite                                             |
|:----:|:----------------------------:|:-----------------------------|:-------------------------------------------------:|
|01    |Contém seis dígitos inteiros  |Conta é do tipo "Poupanca"    |Se a conta é "Corrente", possui cheque especial    |
|02    |Não contém letras             |Conta é do tipo "Corrente"    |Se a conta é "Poupanca", não possui cheque especial|
|03    |Não contém números decimais   |Conta não é do tipo "Deposito"|-                                                  |

  <p><font color="red">Nota 1,0</font></p>
   4.2. (2.0) Definir os casos de teste suficientes para a cobertura do teste de cada um dos cenários definidos.

#### Banco
|CT  |Valores de Entrada             |Resultado esperado|
|:--:|-------------------------------|------------------|
|CT01|numero = 123; nome = BBBBB     |true              |
|CT02|numero = 1234; nome = BBBB     |false             |
|CT03|numero = 12344; nome = BBBBBB  |false             |
|CT04|numero = 123A; nome = BBBB1    |false             |
|CT05|numero = 1234.1; nome = BBBB%  |false             |

#### Agência
|CT  |Valores de Entrada                             |Resultado esperado|
|:--:|-----------------------------------------------|------------------|
|CT06|numero = 1234; nome = AAAAA; cidade = CCCCC;   |true              |
|CT07|numero = 123; nome = AAAA; cidade = CCCC;      |false             |
|CT08|numero = 12344; nome = AAAAAA; cidade = CCCCCC;|false             |
|CT09|numero = 123A; nome = AAAA1; cidade = CCCC2;   |false             |
|CT10|numero = 1234.1; nome = AAAA%; cidade = CCCC*; |false             |

#### Conta
|CT  |Valores de Entrada                |Resultado esperado|
|:--:|----------------------------------|------------------|
|CT11|numero = 123456; tipo = Poupanca  |true              |
|CT12|numero = 123456; tipo = Corrente  |true              |
|CT12|numero = 123456; tipo = Deposito  |false             |
|CT13|numero = 1235; tipo = Poupanca    |false             |
|CT14|numero = 123467; tipo = Corrente  |false             |
|CT15|numero = 12345A; tipo = Poupanca  |false             |
|CT56|numero = 123456.1; tipo = Deposito|false             |
<p><font color="red">Nota 1,0</font></p>
   4.3. (3.0 Pontos) Implementar (na linguagem de programação java) as classes para o teste da criação dos objetos e das movimentações financeiras envolvendo bancos e agências e contas.
**R:** Em anexo.
<p><font color="red">Nota 1,5</font></p>
