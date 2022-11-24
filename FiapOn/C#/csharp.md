<div align="center">
<h1>CSharp</h1>
</div>

## Introdução

A  linguagem  C#  foi lançada no início do ano 2000 e, comparada com outras linguagens de programação, como Pascal, Basic etc.,é uma linguagem relativamente nova.

O   C#   é   uma   linguagem   simples,   orientada   a   objetos,que   combina a produtividade e o poder de linguagem,como C e C++. O fato de ser uma linguagem relativamente  nova  não  apresenta  problemas  com  documentação,  pois  oferece  um grande acerto de documentos e exemplos on-line, além de livros, artigos, fóruns de discussões, blogs, repositórios de exemplos e outros materiais de referência.

## Instruções básicas
### - Tipos de variáveis

O Quadro Tipos  primitivosmostraos  tipos  primitivos  de  variáveis  do  C#.  Os tipos listados são conhecidos como tipos primitivos ou valuetypes. Na linguagem C#, todas as variáveis e constantes são fortemente tipadas, toda declaração de método requer a  especificação do tipo de cada parâmetro de entrada e também a especificação do tipo do retorno.

<div align="center">
  <table>
    <tr>
      <td>Tipo</td>
      <td>Tamanho</td>
      <td>Valores aceitos</td>
    </tr>
    <tr>
      <td>bool</td>
      <td>1 byte</td>
      <td>True e false.</td>
    </tr>
    <tr>
      <td>byte</td>
      <td>1 byte</td>
      <td>0 a 255</td>
    </tr>
    <tr>
      <td>sbyte</td>
      <td>1 byte</td>
      <td>-128 a 127</td>
    </tr>
    <tr>
      <td>short</td>
      <td>2 bytes</td>
      <td>-32768 a 32767</td>
    </tr>
     <tr>
      <td>ushort</td>
      <td>2 bytes</td>
      <td>0 a 65535</td>
    </tr>
    <tr>
      <td>int</td>
      <td>4 bytes</td>
      <td>-2147483648 a 2147483647</td>
    </tr>
    <tr>
      <td>uint</td>
      <td>4 bytes</td>
      <td>0 to 4294967295</td>
    </tr>
    <tr>
      <td>long</td>
      <td>8 bytes</td>
      <td>-922337203685477508 a 922337203685477507</td>
    </tr>
    <tr>
      <td>ulong</td>
      <td>8 bytes</td>
      <td>0 a 18446744073709551615</td>
    </tr>
    <tr>
      <td>float</td>
      <td>4 bytes</td>
      <td>-3.402823E38 a 3.402823E38</td>
    </tr>
    <tr>
      <td>double</td>
      <td>8 bytes</td>
      <td>-1.79769313486232e308 a 1.79769313486232e308</td>
    </tr>
    <tr>
      <td>decimal</td>
      <td>16 bytes</td>
      <td>Números com até 28 casas decimais.</td>
    </tr>
    <tr>
      <td>char</td>
      <td>2 bytes</td>
      <td>Caracteres Unicode. Exemplos:‘a’,’b’,’ç’.</td>
    </tr>
    </table>
</div>

As informações de um tipo de variável podem conter detalhes como:
- Espaço em memória que o tipo utiliza.
- Tipo base que é herdado.
- Endereço de memória.
- Valor mínimo e valor máximo que pode armazenar.
- Operações permitidas.

Os tipos primitivos do C# são muito similares aos tipos primitivos do Java, por exemplo: byte, char, double, floatelong usam a mesma palavra reservada nas duas linguagens. Já o tipo boolean do Java foi abreviado para bool.
Com  os  tipos  primitivos  do  C#  apresentados,podemos  entender  como devemos declarar variáveis, como elasfuncionam na aplicação e como interagem em tipos de dadosdiferentes. 
O Código-fonte Declaração  de  variáveis  numéricasmostraa  declaração  de algumas variáveis numéricas e a interação entre elas.

``` C#
// Método de execução Main
static void Main(string[] args)
{
	int valorInt = 100;
	// convertendo inteiro para long
	long valorLong = valorInt;
	
	// convertendo long para double
	double valorDouble = valorLong;
	// Imprimindo conteúdo das variável
	Console.WriteLine("Valor Inteiro:" + valorInt);
	Console.WriteLine("Valor Long:" + valorLong);
	Console.WriteLine("Valor Double:" + valorDouble);
	// Para a execução até o usuário teclar Enter.
	Console.Read();
}
```
O caso anterior não apresenta incompatibilidade na associação das variáveis do tipo int, longe double, pois todas as interações são feitas atribuindo a variável de menor  tamanho  para  a  variável  de  maior  tamanho.  Vamos  adicionar  uma  linha  no exemplo e tentar associar o valor da variável longpara a variável int. <br>Segue o exemplo:</br>

``` C#
static void Main(string[] args)
{
	int valorInt = 100;
	long valorLong = valorInt;
	double valorDouble = valorLong;
     // Tentando converter long para int
	valorInt = valorLong;
}
```
A  última  linha  de  código apontaum  erro,  impossibilitando  a  compilação  do projeto. A variável do tipo <b>int</b> não aceita um valor do tipo <b>long</b> sem a declaração de uma conversão.Dessa forma, vamos alterar a última linha para adicionar a conversão e executar o programa de exemplo. Segue o Código-fonte a seguir:

``` C#
static void Main(string[] args)
{
	int valorInt = 100;
	long valorLong = valorInt;
	double valorDouble = valorLong;
     // declaração de conversação (Parse)
	valorInt = (int) valorLong;
	Console.WriteLine(valorInt);
	Console.WriteLine(valorLong);
	Console.WriteLine(valorDouble);
	Console.Read();
}
```

## Operadores
Vimos, na seção anterior,os tipos de dados da linguagem C# e a associação e a simples conversão entre os  tipos. Nesta seção, serão apresentadas algumas operações  básicas  de  atribuição e cálculos numéricos,  lógicos e relacionais. Os atributos do tipo lógico e relacional são encontrados junto com estruturas de controle e repetição e serão abordados futuramente,  para  os  operadores  numéricos  e  de atribuições, seguem os códigos-fonte abaixo como exemplos:

``` C#
static void Main(string[] args)
{
	// Operadores para Cálculos 
	int soma = 10 + 15 + 3;
	int subtracao = soma - 10;
	int multiplicacao = soma * subtracao;
	double divisao = multiplicacao / subtracao;
	Console.WriteLine(soma);
	Console.WriteLine(subtracao);
	Console.WriteLine(multiplicacao);
	Console.WriteLine(divisao);
	Console.Read();
}
```

``` C#
static void Main(string[] args)
{
	// Atribuição 
	int soma = 10;
	soma += 1; // Valor final 11
	int subtracao = soma;
	subtracao -= 10; // Valor final 1
	int multiplicacao = soma * subtracao;
	multiplicacao *= 3; // Valor final 33
	double divisao = multiplicacao;
	divisao /= soma; // Valor final 3
	// ... Inserir bloco para impressão dos valores 
	Console.Read();
}
```
## Precedência de Operadores