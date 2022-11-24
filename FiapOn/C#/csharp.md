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
Vimos, na seção anterior,os tipos de dados da linguagem C# e a associação e a simples conversão entre os tipos. Nesta seção, serão apresentadas algumas operações básicas  de  atribuição e cálculos numéricos,  lógicos e relacionais. Os atributos do tipo lógico e relacional são encontrados junto com estruturas de controle e repetição e serão abordados futuramente,  para  os  operadores  numéricos  e  de atribuições, seguem os códigos-fonte abaixo como exemplos:

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
Quando  uma  expressão  C# é composta por vários operadores, a linguagem determina a sequência de execução de cada uma delas. O Quadro Precedência de operadoresilustra os operadores da linguagem e sua precedência, na ordem do mais alto para o mais baixo, ou seja, os primeiros da lista são executados antes


<table border="1" align="center">
 <tr><td>Categoria</td> <td> Operador </td> </tr>
 <tr><td>Primário</td> <td> (x), x.y, f(x), a[x], x++, x--, new, typeof, sizeof, checked, unchecked </td> </tr>
<tr><td> Unário </td><td> +, -, !, ~, ++x, --x, (T)x </td></tr>
<tr><td> Multiplicativos </td><td> *, /, % </td></tr>
<tr><td> Aditivos </td><td> +, - </td></tr>
<tr><td> Troca </td><td> <<, >> </td></tr>
<tr><td> Relacionais </td><td> <, >, <=, >=, is </td></tr>
<tr><td> Igualdade </td><td> == </td></tr>
<tr><td> Lógico AND </td><td> & </td></tr>
<tr><td> Lógico XOR </td><td> ^ </td></tr>
<tr><td> Lógico OR </td><td> | </td></tr>
<tr><td> Condicional AND </td><td> && </td></tr>
<tr><td> Condicional OR </td><td> || </td></tr>
<tr><td> Condicional </td><td> ?: </td></tr>
<tr><td> Associação </td><td> =, *=, /=, %=, +=, -=, <<=, >>=, &=, ^=, |= </td></tr>
</table>
<table>


O C# adota os mesmos operadores da linguagem Java, C e C++e também a mesma precedência.


## Controle de fluxo
O  controle  de  fluxo  é  o  tema  mais  comum  em  qualquer  projeto  de  software, assim  todas  as  linguagens  de  programação  possuemestruturas condicionais  muito similares. A estrutura <b>if...else</b> uma das mais utilizadas, e sempre é a primeira a ser introduzida  no  aprendizado  de  lógica  de  programação  ou  no  aprendizado  de  uma linguagem. Nos próximos parágrafos,vamos percorrer exemplos de código-fonte de estruturas,condições e operadores lógicos.

Segue um exemplo de condição <b>if...else</b> simples:

``` C#
static void Main(string[] args)
{
	int idade = 17;
	if (idade >= 18)
	{
		Console.WriteLine("É maior de idade");
	} else
	{
Console.WriteLine("Ação não permitida para menores de 18 anos");
	}
	Console.Read();
}
```
<b>Adicionando o operador condicional AND para validar o fluxo de uma condição mais complexa</b>

``` C#
static void Main(string[] args)
{
	int idade = 17;
	if (idade >= 18 &amp;&amp; idade < 21)
	{
		Console.WriteLine("Você pode jogar na categoria SUB-20");
	} else
	{
		Console.WriteLine("Você NÃO pode jogar na categoria SUB-20");
	}
	Console.Read();
}
```
- Com  a  estrutura if...else,é  possível  adicionar  mais  blocos  de  condição.No código-fonte condição else if, foram criadas condições para definir uma categoria de acordo com a idade. Para isso, usamos a estrutura else if. 

Segue o exemplo:

``` C#
static void Main(string[] args)
{
	int idade = 20;
	
	if (idade > 15 &amp;&amp; idade < 18)
	{
		Console.WriteLine("SUB-17");
	}
	else if (idade > 17 &amp;&amp; idade < 21)
	{
		Console.WriteLine("SUB-20");
	}
	else if (idade > 21 &amp;&amp; idade < 24)
	{
		Console.WriteLine("SUB-23");
	}
	Console.Read();
}
```

Por fim, temos a estrutura de controle para escolhas chamada Switch. Abaixo,é  apresentado  o  código  para a definição  da  categoria  com  o  uso  da  estrutura  do comando Switch.

``` C#
static void Main(string[] args)
{
	int idade = 16;
	switch (idade)
	{
		case 15:
			Console.WriteLine("SUB-15");
			break;
		case 16:
			Console.WriteLine("SUB-17");
			break;
		case 17:
			Console.WriteLine("SUB-17");
			break;
		case 18:
			Console.WriteLine("SUB-20");
			break;
		default:
			Console.WriteLine("Categoria não definida");
			break;
	}
	Console.Read();
}
```
Se  compararmos  os  códigos-fonte com  um  exemplo  em Java,vamos notar que existem duas pequenas diferenças. A primeira é no nome do método Main,que,em Java,seria main, e a segunda é no comando para imprimir na tela o resultado. Ou seja, as palavras-chavee a estrutura de código para controlar o fluxo são iguais nas duas linguagens.

## Estruturas de repetições
Passamos das estruturas condicionais para o controle de fluxo e agora vamos falar  sobre  as  estruturas  de  repetição.  Essas estruturas  são  responsáveis  pela execução e pelo controle de comandos executados repetidamente. 
Também  conhecidas  como  laços,  as  estruturas  de  repetição  disponíveis  na linguagem C# são: <i>for, while, do...while e foreach</i>.

### Estrutura <i>for</i>
Para escrever um laço usando  a estrutura for, é necessáriaa declaração  de três  partes,  sendo  elas:  inicialização  de  uma  variável,  condição  e  atualização  da variável. A separação de cada uma das partes é feita pelo símbolo “;”, como pode ser visto no exemplo a seguir, no qual é executado uma contagem de 0 até 100.

``` C#
static void Main(string[] args)
{
	// Contando de 0 a 100
	for(int i = 0; i < 101; i += 1)
	{
		Console.WriteLine(i);
	}
	Console.Read();
}
```
### Estrutura <i>while</i>
Com  uma  sintaxe  diferente  do for,  a  estrutura <i>while</i> necessita  apenas  da declaração  da  condição.  É  uma  condição  mais  simples  de  entender,  porém  requer mais  linhas  de  código em comparação  com  a  estrutura <i>for</i>.  Segue  o  exemplo  do código-fonte anterior utilizandoa estrutura <i>while</i>.

``` C#
static void Main(string[] args)
{
	// Contando de 0 a 100
	int i = 0;
	while(i < 101)
	{
		Console.WriteLine(i);
		i += 1;
	}
	Console.Read();
}
```
### Estrutura <i> do...while</i>
Essaestrutura é uma variação da estrutura while, a diferença é que a condição é verificada após a execução do bloco de código. Assim, ao menos uma vez o bloco será executado. Segue o exemplo:

``` C#
static void Main(string[] args)
{
	// Contando de 0 a 100
	int i = 0;
	do
	{
		Console.WriteLine(i);
		i += 1;
	} while (i < 101);
	Console.Read();
}
```
### Estrutura <i>foreach</i>
O <i>foreach</i> é uma estrutura de laço utilizada basicamente para percorrer <i>arrays</i>, lista  e  coleção,  conceitos  que  serão  apresentados  em  capítulos  futuros.  Pode  ser considerado  uma  forma  resumida  do for para  percorrer  dados  em  uma  lista.  No exemplo a seguir, vamos percorrer uma lista de nomes e exibir cada um na tela.

``` C#
static void Main(string[] args)
{
	string[] lista = { "Fiap", "Fiap On", "Fiap School" };
	foreach (string nome in lista)
	{
		Console.WriteLine(nome);
	}
	Console.Read();
}
```
Mais uma vez,podemos notar a semelhança entre C# e Java nos comandose palavras-chave usadospara controle de repetições.

## Orientação a objeto
### Classe e objeto
A   definição   para   Classe   é   um   conjunto   de   objetos   com   as   mesmas características,  formado  de  propriedades  e  comportamentos  por  meio  dos  seus métodos. Podemos pensar em uma classe, como a forma de organizar o código eo nosso sistema.O objeto, também conhecido como instância de uma classe, é responsável por armazenar  os conteúdos desuas propriedades e executar  comportamento e ações por meio de seus métodos.Para entender melhor os conceitos de classe e objeto, vamos usar a linguagem C# e criar uma classe e algumas instâncias. Vamos  imaginar  a  necessidade  de  criação  de  uma  aplicação  para  controlar cursos.Para  cada  curso,precisamos  das  seguintes  informações:  código,  nome  do curso,  nome  do  instrutor,  carga  horária,  quantidade  mínima  e  máxima  de  alunos. Essas informações compõemo nosso modelo de curso para o nosso sistema.Uma classe na linguagem C# é criada a partir da descrição dos modificadores de acesso, acrescidada palavra class do nome da classe.
    <b>[modificador de acesso] class [NomeDaClasse] { }</b>.
    
A Figura Declaração de classe C#, a seguir,exibe a declaração da classe Curso e a forma de criar instâncias ou objetos:
