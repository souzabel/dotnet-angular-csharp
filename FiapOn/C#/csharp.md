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
	<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203831168-13a5f768-aaf0-432d-9e19-f5974b19fb86.png">
		  <img height="200" src="https://user-images.githubusercontent.com/85114441/203831204-0fa1fb96-5ce9-44e5-b57a-a49ef2e7ce2f.png">
</div>

## Atributos

As propriedades definidas na seção anterior (código, nome do curso, nome do instrutor, carga horária, quantidade mínima e máxima de alunos) serão transformadasem atributos da nossa classe. Os atributos serão os responsáveis porarmazenar as informações do objeto. 

No  código  escrito  para  definir  a  classe,  os  atributos  são  declarados  como variáveis, podendo ser do tipo de um outro objetoou tipo primitivo do C#. A declaração de um atributo é igual àdeclaração de uma variável, porém na boa prática de C#,os atributos devem ser escritos com a primeira letra em maiúsculo <i>(UperCamelCase)</i>.

As  variáveis  que  definem  um  atributo  em  uma  classe  são  chamadas  de variáveis de instância, pois só é possível armazenar informação nessa variável após a  instanciação  da  Classe,  ou  seja,  no  objeto  (YAMAMOTO,  2017). Veja  aseguir  a imagem da classe Curso e suas propriedades:
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203831803-c3715a65-0c68-4e1a-a020-004e4b918d66.png">
</div>

## Métodos

São  os  responsáveis  pela  execução  das  ações  nos  objetos.  Eles  dão comportamento ao objeto e são executados ao receber uma mensagem em tempo de execução da classe. Diferentemente da  linguagem  Java,  em  C#  todo  método  deve  ter  seu  nome iniciado com letra maiúscula, assim como os atributos de uma classe. 

Todo o método tem acesso aos dados armazenados nas propriedades da instância, sendo capaz de controlá-los e alterá-los.

Todos os métodos necessitam de quatro informações para sua implementação, são elas: modificador de acesso, tipo de retorno, nome do método e argumentos (não obrigatório).

Para  nossa  classe  Curso,  vamos elaboraro  primeiro  método  que  terá  a responsabilidade de criar um novo curso.Esse método receberá o nome do curso e o nome do instrutor. 

Veja o Código-fonte Criação do método:
``` C#
public class Curso
{
	int Codigo;
	string NomeCurso;
	string NomeInstrutor;
	int cargaHorario;
	int minimoAlunos;
	int maximoAlunos;
	public void CriarCurso(string nome, string instrutor)
	{
		this.NomeCurso = nome;
		this.NomeInstrutor = instrutor;
	}
}
```
Note o uso da palavra reservada <b>void</b>.Ela indica que esse método não retorna nenhuma informação depois da execução. 

Agora  temos  a  necessidade  de  criar  dois  novos  métodos.  O  primeiro  é responsável por matricular um aluno no curso. O segundo tem a função de recuperar a quantidade máxima de alunos aceitos pelo curso, assim, precisamos definir um tipo de dado que será retornado no método e também codificar o método para retornar a informação necessária. O retorno de informações por um método é feito por meio da palavra reservada <b><i>return</b></i>.

Veja a seguir dois exemplos de criação dos métodos para a classe curso:
``` C#
public bool MatricularAluno(string nomeAluno)
{
	// Verificar a quantidade de alunos
	return true;
}
public int ConsultarMaximoAlunos()
{
	// Retorno o valor do atributo
	return this.maximoAlunos;
}
```
## Construtores

De forma resumida, um construtor é um método especial executado assim que uma  nova  instância da classe  é  criada.  Na  maioria  dos  casos,os  construtores  são responsáveis pela alocação de recursos e definição inicial dos atributos do objeto. 

Todas as classes possuem pelo menos um construtor. Caso o desenvolvedor não implemente nenhum construtor na classe, a linguagem cria o construtor-padrãoou default.Esse construtor não recebe nenhum parâmetro e não possui nenhum bloco de código implementado.

Existem três particularidades no construtor que o diferenciamde um método, são elas:
 - O construtor não tem especificação de retorno.
 - Não utiliza a palavra return, pois nunca retorna nenhum valor.
 - É obrigatório ter o mesmo nome da classe.

Para  fixar  o  conhecimento,  vamos  adicionar  alguns  construtores àclasse Curso, com a ideia de inicializar os objetos com valores predefinidos.
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203833082-948060fe-5391-40ce-a8c0-4fb7a6142815.png">
</div>

Agora  podemos  criar  objetos  do  tipo  Curso  com três formas de instanciar  a classe. A primeira delas foi mantida como padrão;a segunda podemos afirmar que substitui o método “CriarCurso” implementado nos exemplos anteriores; e, por fim, o terceiro  construtor, que  inicializa  o  objeto  do  tipo  curso  com  nome  e  capacidades mínima e máxima já definidos. No código-fonte a seguir, podemos  visualizar  a  forma  de  uso,  com  os  três construtores sendo usados.

``` C#
static void Main(string[] args)
{
	// Construtor padrão
	Curso cursoXamarin = new Curso();
	cursoXamarin.CriarCurso("Xamarin", "Flavio Moreni");
	// Definindo nome do curso e instrutor
	Curso cursoIonic = new Curso("Ionic", "Antonio Coutinho");
	// Definindo nome do curso e capacidade mínima e máxima
	Curso cursoNode = new Curso("Node.js", 5, 40);
}
```
## Modificadores de acesso
O objetivo de se utilizar modificadores de acesso é prover segurança entre os componentes de um sistema. Os modificadores são palavras-chave que determinam o nível de acesso em classes, construtores, métodos e propriedades. 

A  linguagem  C#  possui  cinco  modificadores de acesso,  são  eles: <i>public, protected internal, protected, internal e private</i>. Para cada tipo de objeto,o C# tem um modificador-padrão, ou seja,   quando o desenvolvedor   não   declara   nenhum modificador, o framework.NET define automaticamente os seguintes modificadores:

 - Classes – padrão internal.
 - Atributos de classe – padrão private.
 - Membros de estrutura –padrão private.
 - Namespace,  interfaces  e  enumeradores – padrão public,  esses  tipos  não podemsofrer alteração nos modificadores, sempre serão públicos

Além  das  definições  de  modificadores-padrão,cada  modificador  tem  uma definição  de  acesso. O  quadro apresenta  todos  os  modificadores,  os  componentes que podem ser aplicados e os níveis de acesso permitidos

<table border="1" align="center">
   <tr><td><b>Modificador</b></td> <td> <b>Componentes</b> </td> <td> <b>Descrição de acesso</b></td> </tr>
   <tr><td><i> public </i></td><td> classe e atributos </td> <td> Nenhuma restrição </td> </tr>
   <tr><td><i> protected </i></td><td> atributos </td> <td> Acesso para classe e seus filhos </td></tr>
   <tr><td><i> internal </i></td><td> classe e atributos </td> <td> Sem restrição dentro do mesmo projeto. </td> </tr>
   <tr><td><i> protected internal </i></td><td> atributos </td> <td> Acesso dentro do mesmo projeto e classes filhas </td> </tr>
   <tr><td><i> private </i></td><td> atributos </td> <td> Acesso somente pela classe. </td> </tr>
</table>

Para validar os modificadores e os acessos permitidos, vamos aplicar algumas alterações na classe Curso. Nos atributos da classe,devemos aplicar cada um dos tipos do quadro;em um dos construtores,aplicaremos o modificador private, e assim faremos em cada um dos métodos. 

Observe o Código-fonte Modificadores de acesso:
``` C#
namespace FiapHelloWorld
{
    public class Curso
    {
        #region atributos
        int Codigo;
        internal string NomeCurso;
        public string NomeInstrutor;
        private int CargaHorario;
        protected int MinimoAlunos;
        protected internal int MaximoAlunos;
        #endregion
        public Curso()
        {
            // Construtor padrão.
        }
        protected internal Curso(string nome, string instrutor)
        {
            this.NomeCurso = nome;
            this.NomeInstrutor = instrutor;
        }
        private Curso(string nome, int minimo, int maximo)
        {
            this.NomeCurso = nome;
            this.MaximoAlunos = maximo;
            this.MinimoAlunos = minimo;
        }
        public void CriarCurso(string nome, string instrutor)
        {
            this.NomeCurso = nome;
            this.NomeInstrutor = instrutor;
        }
        private bool MatricularAluno(string nomeAluno)
        {
            // Verificar a quantidade de alunos
            return true;
        }
        private int ConsultarMaximoAlunos()
        {
            // Retorno o valor do atributo
            return this.MaximoAlunos;
        }
    }
}
```
Com as alterações na classe Curso, podemos usar nossa classe Program.cs para validar os acessos. Na classe Program.cs,vamos criar uma instância da classe Curso  e  tentar  acessar  todos  os  atributos, conforme  a Figura Erro  de  acesso  a atributosa seguir:
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203835728-e26e7b4b-1f02-4d9b-b71a-0393d84cdcba.png">
</div>

Podemos notar que três linhas ficaram sinalizadas e apresentam problemas de compilação. A razão desses problemas é a permissão de acesso que foi concedida aos atributos “Codigo”, “CargaHoraria”e “MinimoAlunos”, impossibilitando o acesso pela classe Program.

Em  seguida,  vamos  efetuar  os  testes  com os  construtores.  A Figura Erro  de acesso  aos  construtoresa  seguir  exibe  três  objetos  do  tipo  Cursos  sendo  criados, cada um com um construtor diferente. 

Veja:
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203835872-783bc33a-1326-41a3-8f8e-8b1ba9f380d1.png">
</div>

Note  que  a  instância curso3 apresenta  erro,  pois  seu  perfil  de  acesso  foi declarado como <i>private</i>, assim, não é permitido o acesso de fora da classe Curso.

Para finalizar, o último exemplo trazos acessos aos métodos. Na Figura Erro de  acesso  a  métodos abaixo,é  possível  notar  que  os métodos <b>MatricularAluno</b> e <b>ConsultarMaximoAlunos</b> apresentarão acesso na chamada da classe Program.cs. Segue a Figura Erro de acesso a métodoscom o erro:
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203836154-d78ce1bd-7903-460e-83e1-60f3d35fdf4e.png">
</div>

A  forma  fácil  de  corrigir  esses  problemas  é  declarando  todos  os  atributos, construtores  e  métodos  como  públicos,  assim  não  teremos  mais  problemas  de acesso. 

Mas,muita  atenção,  essa  estratégia é  apenas  para  resolvermos  os  erros  e continuar  executando  nossa  aplicação.  Projetos  profissionais  requerem  níveis  bem definidos de acesso aos componentes.

`DICA:Não declare todos os atributos, métodos e construtores como públicos. Analise componente a componentee organize-os em namespaces de domínios similares.Essa estratégia facilitará as definições de acesso aseu sistema.`

## Herança
A vantagem do uso do conceito de herança é a reutilização de código. Assim como  o  encapsulamento  e  o  polimorfismo,  a  herança  é  uma  característica  da orientação a objeto.

Temos dois conceitos de classe para a herança. A primeira é a base, classe que   terá   seu   código   reaproveitado.   A   segunda   é   a   classe   derivada,   que   é especialização da classe base.

Toda  classe  derivada  é  formada  implicitamente  por  todos  os  membros  da classe base, exceto construtores e finalizadores. Assim,todo código da classe base fica  disponível  para  utilização  na  classe  derivada,além  de ser  possível adicionar novos  comportamentos  e  atributos,  tornando,assim,a  classe  derivada  uma  classe mais especializada da classe base.

Uma  classe  derivada  pode  ter  apenas  uma  classe  base,  porém  a  herança  é transitiva,  ou  seja,  se  sua  classe  base  for  uma  classe  derivada,  sua  classe  final herdará todos os membros declaradosnas duas classes base.

Para   entender   a   herança   em   C#,   vamos   criar   uma   classe   chamada CursoFerias,que será derivada da nossa classe Curso. A forma de implementar a herança no C# é usando o “:” depois do nome da classe seguido do nome da classe base. Segue o exemplo no Código-fonte Herança.

``` C#
using System;
namespace FiapHelloWorld
{
    public class CursoFerias: Curso
    {
    }
}
```

Criando  uma  instância  da  classe <b>CursoFerias</b>, é  possível  notar  que  temos acesso a todos os membros da classe Curso. A Figura Membros herdados da classe baseapresenta  a  tela  do  Visual  Studio  com  as  opções  dos  membros  da  classe <b>CursoFerias<b>.
<div align='center'>
  <img height="200" src="https://user-images.githubusercontent.com/85114441/203837288-433be9fe-07aa-4b57-ae3a-b689bcba7547.png">
</div>

# Virtuais
A palavra-chave <b>virtual</b> indica para o método que uma classe derivada pode substituir  o  método  por  sua  própria  implementação.  O  método  da  classe  derivada precisa ser declarado com a palavra-chave <b>override</b>. O não uso dos termos virtual e override não temerros de compilação, porém apresenta resultados diferentes.

Para   entender   melhor,vamos   usar   o Código-fonte Herança,   validando métodos.  Três  classes  são  criadas  para  o  exemplo:a  primeira  é  a  classe  base;a segunda é a classe derivada;e a terceira é a classe de execução. Segue o Código-fonte Herança, validando métodos sem o uso das palavras <b>virtual</b> e <b>override</b>:

``` C#
public class ClasseBase
{
	public void Metodo()
	{
		Console.WriteLine("Método ClasseBase");
	}
}
public class Derivada: ClasseBase
{
	public void Metodo()
	{
		Console.WriteLine("Método Derivada");
	}
}
public class Program
{
	static void Main(string[] args)
	{
		ClasseBase a = new ClasseBase();
		a.Metodo();
		Derivada b = new Derivada();
		b.Metodo();
		ClasseBase c = new Derivada();
		c.Metodo();
		Console.Read();
	}
}
```
Após a execução do programa, as mensagens impressas na tela mostramque a instância “c” executou o método da classe base. O resultado esperado são as três linhas   de   mensagem: Método   ClasseBase, Método   Derivadae Método ClasseBase.

Para  resolver  o  problema  da  última  execução  do  método,  vamos  usar  a declaração de virtual e override. A seguir,temos o código-fonte alterado:
``` C#
public class ClasseBase
{
	public virtual void Metodo()
	{
		Console.WriteLine("Método ClasseBase");
	}
}
public class Derivada: ClasseBase
{
	public override void Metodo()
	{
		Console.WriteLine("Método Derivada");
	}
}
public class Program
{
	static void Main(string[] args)
	{
		ClasseBase a = new ClasseBase();
		a.Metodo();
		Derivada b = new Derivada();
		b.Metodo();
		ClasseBase c = new Derivada();
		c.Metodo();
		Console.Read();
	}
}
```
Após  a  execução,é  possível  notar  que  a  última  impressão  foi  a  mensagem Método Derivada, ou seja, o método da classe base foi realmente substituídopelo método da classe derivada.

As palavras virtuale override têm comportamentos diferentes na linguagem Java.  Em  Java,quando  queremos  que  um  método  não  seja  sobrescrito,devemos declará-lo como final;sem o modificador final,qualquer método pode ser sobrescrito. Em  Java,não  temos  a  palavra override,  para  sobrescrever  um  método,bastar codificar na classe filho com o mesmo nome, retorno e parâmetros de entrada.

## Abstract
A palavra-chave abstract pode ser usada em classes e métodos.Seu objetivo ou   uso   é   permitir   que   classes   ou   métodos   que   estão   incompletos sejamimplementados nas classes que herdam a abstração, as classes derivadas.

Tanto    uma    classe    abstrata    quanto    um    método    abstrato    possuem particularidades, seguem algumas.
  ### Classe
   - Não pode serinstanciada. Não é permitido criar um objeto a partir de uma classe abstrata.
   - Geralmente,é usada como classe base para outras classes
   - Pode   conter   métodos   abstratos   e   métodos   comunsepossuir construtores e propriedades.
   - Não pode ser estática (static).
   - Pode herdar de outra classe abstrata

  ### Método
   - Não possui implementação na classe abstrata. É composto apenas por sua assinatura.
   - A classe que deriva de uma classe abstrata precisa implementar seus métodos   abstratos.   Caso   contrário,um   erro   de   compilação   é apresentado.
   - Método  abstrato  é virtuale  deve  ser  implementado  usando  o modificador override.
   - Somente pode existir em uma classe abstrata. 
   - Não pode usar os modificadores static e virtual.

Abaixo, veja o Código-fonte Uso de classe e método abstract com umexemplo de uso do abstract:
``` C#
public abstract class ClasseBase
{
	public virtual void Metodo()
	{
		Console.WriteLine("Método ClasseBase");
	}
	public abstract void MetodoAbstrato();
}
public class Derivada: ClasseBase
{
	public override void Metodo()
	{
		Console.WriteLine("Método Derivada");
	}
	public override void MetodoAbstrato()
	{
		Console.WriteLine("Método MetodoAbstrato");
	}
}
public class Program
{
	static void Main(string[] args)
	{
		Derivada b = new Derivada();
		b.Metodo();
		ClasseBase c = new Derivada();
		c.Metodo();
		c.MetodoAbstrato();
		Console.Read();
	}
}
```
##  Interface

O conceito de interface tem uma leve semelhança com abstract. É outra forma de herança e de atribuir comportamentos.

A primeira diferença de uma interface para uma classe abstrata é que um podederivar  de  mais  de  uma  interface.  A  segunda  é  que  uma  interface  define  apenas assinaturas de métodos, nunca possuem a sua implementação. A terceira e última é que,por convenção,o C# usa a letra I como prefixo em todas as interfaces.

Veja um exemplo de uso de interfaces.
``` C#
public interface IAluno
{
	void CriarAluno();
}
public interface IInstrutor
{
	void CriarInstrutor();
}
public class Curso : IAluno, IInstrutor
{
	public void CriarAluno()
	{
		Console.WriteLine("Criando Aluno");
	}
	public void CriarInstrutor()
	{
		Console.WriteLine("Criando Instrutor");
	}
}
```
## Exceções

Exceções são condições de erro no fluxo de execuçãoeindicam que um evento inesperado  ocorreu  durante  a  execução.  Quando  eventos  inesperados  acontecem, objetos de exceção são criados e,em seguida,lançados para a classe que enviou a mensagem para a execução.

O  framework  .NET  é  responsável  pelo  lançamento  de  várias  exceções  (por exemplo: tentativa de abrir um arquivo inexistente no sistema de arquivos). Por outro lado,  os  desenvolvedores  podem  ou  devem  lançar  exceções  no  código.  Seguem algumas situações em que exceções devem ser lançadas:

- método não pode concluir toda a sua funcionalidade;
- valores de argumentos dos métodos estão incorretos;
- chamadas a componentes inexistentes ou sem instância em memória;
- falhas em conexão com recursos externos (por exemplo: banco de dados).

Para trabalhar e entender o uso de exceptions,é preciso tratar de três tópicos. O primeiro é o lançamento de exceptions;o segundo é o tratamento de exceptions;e o último é a criação de exceptions personalizadas.

### Lançamento de exception
O  lançamento  de  uma exception é  feito  pela  palavra  reservada throw.  A palavra throw sinaliza que uma situação não esperada aconteceu durante a execução. Todas as exceções em C# são herdadas da classe System.Exception
 
 Veja no Código-fonte Lançando uma exceção um exemplo de lançamento de uma exceção na validação de dados no parâmetro de um método.

 ``` C#
public void CriarAluno(string nome)
{
	if (nome == null)
	{
          // Lançando uma exceção
		throw new Exception("Nome do aluno inválido");
	}
}
```
### Tratamento de exception

A forma de tratar exception em C# é usando o bloco de código try...catch. O código a seguir apresenta umexemplo para capturar duas exceções, a primeira delas é System.NullReferenceException e a segunda é Exception. 

Segue o exemplo
``` C#
static void Main(string[] args)
{
	try
	{
		string nome = null;
		Console.WriteLine(nome.Substring(2));
		new Curso().CriarAluno(nome);
	}
     // Capturando uma exceção de referência nula.
     // Similar ao NullPointerExceptio do  Java
	catch (NullReferenceException)
	{
		Console.WriteLine("Nome do aluno incorreto");
	}
	catch (Exception)
	{
		Console.WriteLine("Problema na execução a operação");
		throw new Exception("Problema na execução a operação");
	}
}
```
### Personalizando exceptions
A linguagem C# permite o lançamento de exceções do namespaceSysteme também  a  criação  de  exceções  personalizadas  derivando  de System.Exception. Para  criar  uma  exceção  personalizada,  a  classe  derivada  precisa  definir  quatro construtores. Segue o exemplo deuma exception personalizada.

``` C#
public class PersonalizadaException: Exception
{
	public PersonalizadaException() : base() { }
	public PersonalizadaException(string message) : base(message) { }
	public PersonalizadaException(string message, System.Exception inner) : base(message, inner) { }
	protected PersonalizadaException(
		System.Runtime.Serialization.SerializationInfo info,
		System.Runtime.Serialization.StreamingContext context) { }
}
```
Agora, podemos alterar a regra de validação do nome e substituir a exceção System.Exceptionpara a PersonalizadaException, assim,é necessário também a alteração  no  blocotry...catche  tratar  a  nova exception.  Veja  abaixo  como  ficou  o código-fonte:

``` C#
public void CriarAluno(string nome)
{
	if (nome == null)
	{
		throw new PersonalizadaException("Nome do aluno inválido");
	}
}
```
``` C#
public class Program
{
	static void Main(string[] args)
	{
		try
		{
			string nome = null;
			new Curso().CriarAluno(nome);
			Console.WriteLine(nome.Substring(2));
		}
		catch (PersonalizadaException p)
		{
			Console.WriteLine(p.Message);
		}
		catch (Exception ex)
		{
			Console.WriteLine("Problema na execução a operação");
			throw new Exception("Problema na execução a operação");
		}
	}
}
```

# COLEÇÕES 

## Arrays
Em  qualquer  linguagem  de  programação, a codificação  de arrays é  muito importante.  Um  dos  problemas  mais  comuns  no  uso  de arrays é  a  limitação  de tamanho,  é  necessário  ser  preciso  com  esse  detalhe,  caso  contrário,a  solução implementada com arrays pode virar um grande problema.

Em resumo, um array é uma estrutura de dados que facilita o armazenamento de vários elementos e torna a leitura e o acesso fáceis para os desenvolvedores. O exemplo  abaixo  apresenta  as  duas  formas  de  criação  de  um arraye  o  acesso  e a manipulação dos dados de algumas posições do array:

``` C#
static void Main(string[] args)
{
	// Exemplo 1
	string[] nomes1 = { "João", "Maria", "José" };
	// Exemplo 2
	string[] nomes2 = new string[3];
	nomes1[0] = "João";
	nomes2[1] = "Maria";
	nomes2[3] = "José";
}
```
Nota-se que foram criados dois arrays com valores iguais. O primeiro array foi inicializado  com  conteúdo  de  nomes  e  não  teve  seu  tamanho  especificado  pelo desenvolvedor.Já o segundo foi criado com o tamanho especificado e o seu conteúdo foi adicionado em cada posição. 

A criação de um array é semelhante à criação de uma instância de objeto, com a diferença do uso de colchetes “[ ... ]”,adicionado ao tipo do objeto.

`DICA:Aposição inicial de um arrayé 0 (zero), logo as posições vão de 0 (zero) até tamanho -1 (menos um).`

No exemplo anterior,criamos um array para armazenar uma lista de nomes, mas podemos enriquecer nosso exemplo e criar array de classes específicas do nosso sistema. Assim, no Código-fonte Acessando conteúdo do array, temos um exemplo de criação de array da classe curso e a utilização da estrutura de repetição foreach para acesso e exibição dos valores na tela.

``` C#
public class Curso
{
	public int Codigo;
	public string NomeCurso;
	public Curso(int cod, string nome)
	{
		this.Codigo = cod;
		this.NomeCurso = nome;
	}
}
public class Program
{
	static void Main(string[] args)
	{
		// Criando um array de curuso
		Curso[] listaCursos = new Curso[3];
		
		// Criando os items do array
		listaCursos[0] = new Curso(1, "Curso 1");
		listaCursos[1] = new Curso(2, "Curso 2");
		listaCursos[2] = new Curso(3, "Curso 3");
		// Navegando pelo array e imprimindo o conteúdo
		foreach (Curso curso in listaCursos)
		{
			Console.WriteLine(curso.NomeCurso);
		}
		Console.Read();
	}
}
```


