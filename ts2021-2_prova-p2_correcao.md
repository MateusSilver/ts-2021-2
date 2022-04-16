<div align=center>
  <img src="brasaooficialcolorido.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>

#### <p style="text-align: center;">Instituto de Informática</p>

#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>

#### <p style="text-align: center;">Teste de Software - 2021/2</p>

#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>

#### <p style="text-align: center;"> Prova P2 - 12/04/2022</p>

Matrícula: <font color="red">??????????</font>

Nome: <font color="red">??????????</font>

<font color="red">Nota 3,9</font>

1. Quanto ao Processo de Teste de Software, responda as duas questões seguintes:
   1. (**0,5 ponto**) Defina os seguintes conceitos Processo de Teste de Software, Projeto de Teste de Software e Plano de Teste de Sofware.
      Processo de teste de software: Conjunto de atividades sequenciais e contínuas para realização de um teste em um software.
      Projeto de Teste de software: Descrição detalhada de um teste de software, tendo o que será testado, modelos de casos de teste e divisão de requisitos, mapeamento de artefatos a testar e baterias, estimativas de tempo e duração do processo, cronograma, riscos, custos, requisitos, etc.
      Plano de testes: Documento que especifica ações que serão tomadas em um processo de teste de software, o cronograma, responsaveis, o que e como será o processo, métodos e critérios para avaliação de resultados. <font color="red">Nota 0,5</font>
   2. (**0,5 ponto**) Descreva o relacionamento existente entre estes conceitos.
      No desenvolvimento de um software o processo de teste de software é uma ferramenta para assegurar a qualidade e conformidade do mesmo. Esse processo é realizado seguindo um projeto de teste de software que é feito seguindo um plano de teste de software definido previamente, no qual estão os criterios e dados necessarios para criação do projeto. O projeto então deve ser realizado com base nesse plano. <font color="red">Nota 0,4</font>
2. (**1,0 pontos**) Descreva as vantagens para a equipe de desenvolvimento ao se adotar um processo de teste ágil.
   A rápida localização de defeitos e não conformidades, prevenindo que crescam, eliminando possiveis bugs cedo antes que seja necessario grandes mudanças no codigo de um projeto já em estado avançado, quebrando o codigo. <font color="red">Nota 0,4</font>
3. (**1,0 ponto**) Cite pelo menos três características do Teste Exploratório.

- Depende da experiência do testador
- Geralmente não tem um plano definido previamente
- realizados junto ou logo após o desenvolvimento.
- Típicos de metodologias ágeis e projetos com pouca documentação. <font color="red">Nota 1,0</font>

4.  Considere os arquivos .java (Banco.java, Agencia.java, Conta.java e BankValidator.java). Nos próprios arquivos .java estão definidas as regras para cadastramento de cada um deles (Banco, Agencia e Conta). Desta forma, pede-se:

    1.  (2.0 Pontos) Definir os cenários de teste suficientes para testar o cadastro e movimentações financeiras envolvendo bancos, agências e contas, conforme especificado. Para cada cenário definir os critérios de teste adequados à definição dos seus casos de teste.

        - Dado que: Relizei um cadastro de uma conta
        - Quando: verificar a existencia da conta
        - Então: se o cadastro for valido deve ser criada uma conta com esse nome

        - Dado que: Tenho uma conta.
        - Quando: tento realizo um deposito.
        - Então: se o valor do deposito for valido deve ser efetuado.

        - Dado que: Tenho uma conta
        - Quando: tento realizar um saque.
        - Então: Se o valor do saque for menor que o saldo, deve ser efetuado.

        - Dado que: Tenho uma conta.
        - Quando: tento realizar uma transferencia.
        - Então: se o valor for menor que o saldo do remetente, deve ser efetuado.

        - Dado que: Tenho uma conta.
        - Quando: tento creditar rendimento
        - Então: se a conta for poupança, o valor sera creditado.

        - Dado que: Tenho uma conta.
        - Quando: tento debitar juros do cheque especial.
        - Então: se o valor for menor que o saldo
        - E: a conta for poupança;
        - Então: deve debitar os juros.

        <font color="red">Nota 0,5</font>

    2.  (2.0) Definir os casos de teste suficientes para a cobertura do teste de cada um dos cenários definidos. Documentar os casos de teste no seguinte padrão:

             Conta:

             | CT   | Valores de Entrada                                         | Resultado esperado |     |
             | ---- | ---------------------------------------------------------- | ------------------ | --- |
             | CT01 | cadastro de conta valido                                   | True               |     |
             | CT02 | cadastro de conta invalido                                 | False              |     |
             | CT03 | numero de conta > 6                                        | False              |     |
             | CT04 | numero da conta com caracteres                             | False              |     |
             | CT05 | tipo de conta = 'Corrente'                                 | True               |     |
             | CT06 | tipo de conta = 'Poupança'                                 | True               |     |
             | CT07 | tipo de conta != 'Poupança' ou tipo de conta != 'Corrente' | False              |     |

             Agencia:

        | CT   | Valores de Entrada                                | Resultado esperado |     |
        | ---- | ------------------------------------------------- | ------------------ | --- |
        | CT01 | cadastro de agencia valido                        | True               |     |
        | CT02 | numero de agencia com menos de 3 digitos          | False              |     |
        | CT03 | numero de agencia com mais de 5 digitos           | False              |     |
        | CT04 | nome da agencia com mais de 100 digitos           | False              |     |
        | CT05 | nome da agencia com menos de 5 digitos            | False              |     |
        | CT06 | nome da cidade da agencia com mais de 100 digitos | False              |     |
        | CT07 | nome da cidade da agencia com menos de 5 digitos  | False              |     |

        Banco:

        | CT   | Valores de Entrada                       | Resultado esperado |     |
        | ---- | ---------------------------------------- | ------------------ | --- |
        | CT01 | cadastro de banco valido                 | True               |     |
        | CT02 | numero de banco com menos de 3 digitos   | False              |     |
        | CT03 | numero de banco com mais de 3 digitos    | False              |     |
        | CT04 | numero de banco > 0                      | False              |     |
        | CT05 | nome de banco com mais de 100 caracteres | False              |     |
        | CT06 | nome de banco com mais de 5 caracteres   | False              |     |

        <font color="red">Nota 0,5</font>

    3.  (3.0 Pontos) Implementar (na linguagem de programação java) as classes para o teste da criação dos objetos e das movimentações financeiras envolvendo bancos e agências e contas.

    <font color="red">Nota 0,6</font>

INSTRUÇÕES:

1. Tipo: Prova individual;
2. Local de Entrega: Plataforma Turing.
3. Forma de Entrega: arquivo compactado contendo:
   1. Este arquivo md, respondido.
   2. Classes de teste para (BancoTest, AgenciaTest e ContaTest);
   3. O arquivo compactado deverá ter o seguinte nome prova_p2<mat>.zip, onde mat é o número da matrícula do aluno(a).
4. Data da Entrega: 12/04/2022, as 22hs.
5. Critério de Aceitação: arquivo entregue, conforme solicitado.
6. Obs: segue no mesmo pacote o arquivo "org.apache.commons.lang.StringUtils", que é uma dependência do projeto. É deve ser inserida no _classpath_ do projeto de implementação da questão 4, caso não esteja utilizando o _maven_.
