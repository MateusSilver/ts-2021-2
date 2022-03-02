<div align=center>
  <img src="brasaooficialcolorido.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>

#### <p style="text-align: center;">Instituto de Informática</p>

#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>

#### <p style="text-align: center;">Teste de Software - 2021/2</p>

#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>

#### <p style="text-align: center;"> Prova P1 - 16/02/2022</p>

Matrícula: 201905543
Nome: Mateus da Silveira Batista

<p><font color=red>Nota: 4,8.</font></p>

1. Quanto ao objetivo do Teste de Software, responda as duas questões seguintes:
   1. (**0,5 ponto**) Qual o objetivo primário da atividade de teste de software?
      Avaliar e garantir a qualidade e conformidade de um software com seus requisitos. <font color=red>Errado.</font>
   2. (**0,5 ponto**) O que acontece, quando não se atinge este objetivo primário?
      O software volta pra linha de produção para ser corrigido e reavaliado. <font color=red>Errado.</font>
2. (**1,0 ponto**) Explique o que é o teste exaustivo e porque sua execução não é possível.
   O teste exaustivo é literalmente testar todas as possiveis entradas que podem existir e se todas as saidas estão corretas, o que pode ser impossivel dependendo do dominio da entrada, como por exemplo qualquer numero real, o que pode gerar casos de teste infinitos. <font color=green>Certo.</font>
3. (**1,0 ponto**) Cite pelo menos duas limitações da Técnica de Teste Funcional e duas da Técnica de Teste Estrutural.
   O teste funcional não previne possíveis erros de código que podem passar despercebidos em trechos onde a execução não passa e podem não identificar falhas estruturais do código como loops nesses trechos de código ou trechos que podem estar, embora corretos, ineficientes. O teste estrutural por sua vez, não previne erros lógicos no sistema ou garante que as saídas são as esperadas, <font color=red>o teste estrutural apenas analisa o fluxo de dados</font>, esse teste também pode ser desnecessariamente complexo e precisa de um conhecimento de programação e tempo elevados. <font color=orange>Parcialmente correto. Nota 0,8.</font>
4. (**1,0 ponto**) Descreva pelo menos um dos quatro níveis de teste constantes da literatura especializada.
   O teste de unidade: Pode ser realizado em qualquer etapa do processo, se resume a testar a integridade de uma parte do projeto recem feita, pequena, verificando seu fluxo de controle e de dados estão conforme o planejado. <font color=green>Certo.</font>
5. (**1.0 ponto**)Descreva qual o propósito do critério de teste funcional Particionamento por Classes de Equivlência.
   Para realizar testes inxutos porém ainda consisos, é necessário retirar teste redundantes, com isso fazendo a divisão de classes de dados, assumindo que alguns testes identificam conformidades de mesmo modo, e são práticamente testes duplicados. Diminuindo os casos de testes não necessarios o teste se torna menor e ainda assim eficiente. <font color=orange>Parcialmente correto. Nota 0,5.</font>
6. (**1.00 ponto**) Existe algum tipo de hierarquia em relação aos critérios de teste estrutural, todos os nós, todos os arcos e todos os caminhos? Se sim, explique-a, considerando a perspectiva dos níveis de cobertura desejados.
   Há uma hierarquia no critério de teste funcional, ele deve cobrir todos os caminhos, todos nós, todos os arcos. <font color=red>Errado.</font>
7. Considere a especificação, a seguir, de um hipotético programa que objtiva a classificação de um triângulo, a partir dos valores informados para os seus três lados.

   a) Dado um triângulo cujos segmentos medem A, B e C, que são números inteiros positivos na faixa de 0 a 100. Esse triângulo somente existirá se: (A + B > C) ou (A + C > B) ou (B + C > A).
   b) Quanto às medidas dos seus lados o triângulo, poderá ser classicado em:
   • Isósceles = quando possui dois lados com a mesma medida;
   • Escaleno = quando todos os seus lados têm medidas diferentes;
   • Equilátero = quando todos os lados tem a mesma medida;
   DESCONSIDERADO:
   • Acutângulo = quando o quadrado de um dos seus lados é menor que a soma do quadrado dois outros dois. (A<sup>2</sup> < B<sup>2</sup> + C<sup>2</sup>).
   • Retângulo: quando o quadrado de um dos seus lados é igual à soma do quadrado dois outros dois. (A<sup>2</sup> = B<sup>2</sup> + C<sup>2</sup>).
   • Obtusângulo: quando o quadrado de um dos seus lados é maior que a soma do quadrado dois outros dois. A<sup>2</sup> > B<sup>2</sup> + C<sup>2</sup>.

7.1 (**2.0 pontos**) Definir uma tabela de decisão para o teste tanto da existência do triângulo, quanto para a definição do seu tipo. Consulte exemplo de tabela de decisão na tarefa 005.
![image](./tabela_decisao.pdf) <font color=red>Arquivo não disponibilizado.</font>

| -      | R1         | R2         | R3         | R4        | R5         | R6        | R7        | R8       |
| ------ | ---------- | ---------- | ---------- | --------- | ---------- | --------- | --------- | -------- |
| a=b    | SIM        | SIM        | SIM        | SIM       | NAO        | NAO       | NAO       | NAO      |
| b=c    | SIM        | SIM        | NAO        | NAO       | SIM        | SIM       | NAO       | NAO      |
| c=a    | SIM        | NAO        | SIM        | NAO       | SIM        | NAO       | SIM       | NAO      |
| efeito | equilatero | impossivel | impossivel | isosceles | impossivel | isosceles | isosceles | escaleno |

<font color=orange>Parcialmente correto. Está faltando a regra para validação se é ou não um triângulo. Nota 1,5.</font>

7.2 (**2.0 pontos**) Criar os conjunto de casos de teste necessários para a cobertura das combinações constantes da tabela de decisão, seguindo o seguinte padrão:

| CT   | Cenário                | resultado esperado | Resultado |
| ---- | ---------------------- | ------------------ | --------- |
| CT01 | a = b, b = c e a = c   | equilatero         |           |
| CT02 | a = b, b != c e a != c | isosceles          |           |
| CT03 | b = c, b != a e c != a | isosceles          |           |
| CT04 | a = c, a != b e c != b | isosceles          |           |
| CT05 | a != b, b != c, c != a | escaleno           |           |

<font color=red>Errado. Casos de teste devem conter valores e não condições.</font>

INSTRUÇÕES:

1. Tipo: Prova individual;
2. Local de Entrega: Plataforma Turing
3. Forma de Entrega: Entregar este arquivo, editado com suas respostas, no formato .md, nominado da seguinte forma: ts2021-2_prova-p1_mat.md, onde mat deverá ser substituído pelo número da sua matrícula.
4. **Entrega diferente da especificada não será avaliada.**
5. Data da Entrega: 22/02/2022, as 23h59min.
6. Critério de Aceitação: arquivo entregue, conforme solicitado.
