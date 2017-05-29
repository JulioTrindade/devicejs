# jQuery

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>

## Resumo

### Propósito da linguagem:

  JQuery é uma biblioteca de JavaScript, seu principal objetivo é ajudar os desenvolvedores na produção do código, dando a eles o foco da lógica e facilitando quanto as ferramentas do desenvolvimento. O JQuery reune uma quantidade enorme de funções que facilitam a vida de quem desenvolve em JavaScript. Seu lema é "write less, do more." 
  
  
### Paradgima da linguagem:

Utiliza vários paradigmas. Principalmente o imperativo ou procedural, mas também funcional.


### Data de criação:  

Dezembro de 2006 no BarCamp de Nova York, por [John Resig](https://en.wikipedia.org/wiki/John_Resig ""). 


### Principal mantenedor:

[jQuery Foundation](https://jquery.org/team/ ""). 


## Instalação e uso

- O jQuery pode ser instalado usando uma CDN;

`<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>`

- Salvando-o como arquivo no seu diretório e chamando-o no seu código;

`<script src="jquery-3.2.1.min.js"></script>`

- Usando o [npm](https://www.npmjs.com/ "");

`npm install jquery`

- Usando [Bower](https://bower.io/ "");

`bower install jquery`

## Sintaxe Básica

A sintaxe jQuery é feita sob medida para selecionar elementos HTML e executar alguma ação sobre o(s) elemento(s).

`$ ( seletor ). Ação ()`

- Usa-se '$' para acessar jQuery;
- Usa-se '()' para consultar elementos HTML;
- Logo após é indicada uma ação jQuery a ser executada no(s) elemento(s).

`$ (". Test"). Hide ()`

`$ ("# Test"). Hide ()`

### Variáveis

`var nome = ‘John Resig’`

`var idade  = 33`

### Constantes

A versão mais recente do JavaScript, tem uma noção de const:

`const CONSTANTE = "VALOR";`

Isso funcionará em praticamente todos os navegadores.

### Operadores relacionais

- Igual (==);
- Não igual (!=);
- Maior que (>);
- Maior ou igual que (>=);
- Menor que (<);
- Menor ou igual que (<=);

### Operadores Lógicos

- E (&&);
```
if(a == 1 && b == 2){
  //condição só ocorre caso as duas expressões forem verdadeiras;
}
```

- OU (||);
```
if(a == 1 || b == 2){
  //condição ocorre caso uma das expressões forem verdadeiras;
}
```

- NOT (!);

```
if !(a == 1){
  //condição ocorre caso 'a' for diferente de 1;
}
```

### Operadores aritméticos

- Resto da divisão (%);

`var a = 29 % 10 //a = 9`

- Incremento (++);

`var a = 0; a++ //a = 1, equivale a 'a = a + 1'`

- Decremento (--);

`var a = 1; a--// a = 0, equivale a 'a = a - 1'`

- Operador de exponenciação (**): versão experimental;

`var a = 2 ** 3// a = 8`

- Além dessas, existem os operadores básicos: adição(+), subtração(-), multiplicação(*) e divisão(/);

### Estruturas de controle condicional

- If;

```
if ( condição ) {
 ação;
}
```

- If … else;

```
if ( chuva ) {
 alert('ficar em casa');
} else {
 alert('jogar futebol');
}
```

- Else if;

```
if ( condição ) {
 // Ação
} else if ( outra condição ) {
 // Ação
} else if ( outra condição ) {
 // Ação
} else if ( outra condição ) {
 // Ação
} else if ( quantas condições quiser ) {
 // Ação
} else {
 // Ação final se nenhuma condição for verdadeira
}
```

- Switch;

```
switch(expressão)
{
case valor1:
//código 1
break;
case valor2:
//código 2
break;
default:
//código padrão
break;
}
```

### Estruturas de repetição

- While;

```
var count = 0;
while ( count <= 10 ) {
 document.write( count );
 count++;
} 
```

- Do while;

```
var count = 11;
do {
 document.write( count );
 count++;
} while ( count <= 10 )
```

- For;

```
for ( var i = 0; i <= 10; i++ ) {
 document.write( i );
} 
```

- Break e continue;

### Vetores, matrizes e strings

#### Vetores:

`var cars = ["Saab", "Volvo", "BMW"];`

#### Matrizes:

- São feitas com vetores referenciando outros vetores;

```
var matriz[][]=[[1,2],[3,4]]

//document.write(matriz[0][1])
//2
```

#### Strings:

- Usada para armazenar uma cadeia de caracteres, pode ser usado aspas duplas ou simples;

`var nome = "John Resig"`

`var nome = 'John Resig'`

### Funções

- Funções são a unidade básica de ação em jQuery. O principal ponto de entrada da maioria das aplicações em jQuery é um bloco de código que se parece com isso:

```
$(document).ready(function() {
    Do Something
});

```
- $(document) é um objeto jQuery. O $() é, na verdade, uma função disfarçada; ela transforma o document em um objeto jQuery.
- .ready() é um tipo de função; você pode vê-lo como uma forma de ajudante que executa o código dentro dos parênteses assim que o documento HTML estiver pronto.
- function(){} é a ação que .ready() vai desempenhar assim que o documento HTML estiver carregado. (No exemplo acima, o lugar onde está o Do Something (faça alguma coisa) é onde as ações devem ficar).

## Sintaxe OO

- Não encontramos referência a sintaxe OO exclusiva do jQuery, logo aplica-se a sintaxe básica do JavaScript.

### Classes

```
function Aluno () {
 var nome;
 var idade;
 var curso;
}
```

### Objetos

```
var Aluno = new Aluno();

Aluno.nome("John Resig");
Aluno.idade("33");
Aluno.curso("INFOWEB");
```

### Atributos

- São elementos que definem a estrutura de uma classe.
- Ex: nome, idade e curso do aluno

### Métodos

- Os métodos determinam o comportamento dos objetos de uma classe.

```
function Aluno () {
 var nome;
 var idade;
 var curso;
 this.mostraDados = function () {
    alert("Nome do aluno: " + nome + "\nIdade: " + idade + "\nCurso: " + curso);
  }
}
```

### Construtores

- Definem a estrutura padrão de um objeto de determinada classe.

```
function carro(modelo, ano, preco) {
    this.modelo = modelo;
    this.ano = ano;
    this.preco = preco;
}
```


### Herança

```
function Conta() {
    this.saldo = 0;
    this.deposita = function(valor) {
        this.saldo += valor;
    };
} 

// caso for uma conta do tipo poupança, necessitaremos de multiplicar o valor depositado pela taxa.

function ContaPoupanca() {
    this.atualiza = function(taxa) {
        this.saldo += this.saldo * taxa;
    };
}

ContaPoupanca.prototype = new Conta();
ContaPoupanca.prototype.constructor = ContaPoupanca;

// assim "copiamos" tudo o que há em Conta para dentro de ContaPoupanca
```

### Polimorfismo

- Definimos Polimorfismo como um princípio a partir do qual as classes derivadas de uma única classe base são capazes de invocar os métodos que, embora apresentem a mesma assinatura, comportam-se de maneira diferente para cada uma das classes derivadas.

### Sobrecarga

- A sobrecarga (overload) consiste em permitir, dentro da mesma classe, mais de um método com o mesmo nome. Entretanto, eles necessariamente devem possuir argumentos diferentes para funcionar.

### Visibilidades

- Public;
- Private;
- Protected.

### Exceções

- Try: testa um bloco de código visando erros;
- Catch: manipula erros;
- Throw: permite que você personalize um erro;

