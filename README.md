# DeviceJS

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>
Linguagem: DeviceJS

## Resumo

**Propósito da linguagem:** 

O DeviceJS tem como objetivo permitir que desenvolvedores familiarizados com bibliotecas de desenvolvimento da Web apliquem algo que aconteça dinamicamente no mundo físico.

**Paradgima da linguagem:** 

Procedural, visto que segue o conceito de um estado e de ações que manipulam esse estado, nele encontramos procedimentos que servem de mecanismos de estruturação. Podemos denominá-lo procedural por incluir procedimentos para estruturação.

**Data de criação:**
dd de mês de 2015

**Principal mantenedor**: 
- KeystoneJS

## Instalação e uso

**Como instalar?**
- O DeviceJS é um sistema distribuído;
- O DeviceJS pode distribuir um script em qualquer retransmissão capaz de executar o DeviceJS run-time;
- Execute o comando a seguir na linha de comando:
```js
  $ npm install devicejs
```
**Como usar?**
- Pode ser usado: em um banco de dados JSON distribuído em tempo real, que atualiza diretamente para o tempo de execução do DeviceJS. Em API baseada em objetos, baseada basicamente em base2 e Prototype. Em ganchos de serviço para drivers de dispositivo nativos para protocolos como: 6loWPAN, Z-Wave e ZigBee. Em um Catálogo que permite que dispositivos de todos os tipos sejam categorizados e cruzados em uma variedade de maneiras, e em APIs para lidar com JavaScript complexo, assíncrono, semelhante no conceito de  async.js.
- Execução: Os scripts e aplicativos escritos para DeviceJS podem executar e consequentemente controlar dispositivos em muitos locais. 
   
**Comandos:**
   
**Seletores:**
- Transformar toda a iluminação em um local para vermelho:
```js
  dev$.byLocation("kitchen").setColor("red");
```
- Mudar todos os dispositivos marcados como uma "luz" para desligado:
```js
  dev$.byTag('light').setOff();
```
**Eventos:**
- Pop-up de alerta de caixa de diálogo em um 'clique':
```js
  dev$.byDeviceAlias('hallway-sensor').trigger('motion',function(){dev$.byLocation('hallway').setOn();});
```
- Sensor de movimento acionado de acordo com a movimentação no ambiente:
```js
  function func1(){dev$.byTag('light').setOn();}dev$.trigger('motion', func1);
```
## Sintaxe básica

**Variáveis e constantes:**
Como o devicejs é uma linguagem que deriva do javascript, suas sintaxes são semelhantes
- Variáveis: Podem ser declaradas de 3 formas
```js
  var x = 42;
```
Apenas variáveis globais:
```js
  x = 34;
```
Para declarar uma variável local de escopo de bloco:
```js
  let z = 92;
```
- Constantes: 
```js
  const a = 3;
```
A constante não altera seu valor:
```js
  const a = 3;
  a = 10
  console.log(a); //retorno: 3
```

- Operadores relacionais:
'<': Menor que, '>': Maior que, '<=': Menor ou igual, '>=': Maior ou igual, '==': Igual, '!=': Diferente (não igual).

- Operadores lógicos:
AND (&&), OR (||) e NOT (!).

- Operadores aritméticos:
Operadores aritméticos tomam valores numéricos (sejam literais ou variáveis) como seus operandos e retornam um único valor númerico. Os operadores aritméticos padrão são os de soma (+), subtração (-), multiplicação (*) e divisão (/). Além desses que são comuns a outras linguagens de programação, o devicejs disponibiliza as operações de: resto da divisão (%), Incremento (++), Decremento (--), Negação (-), Adição (+) e exponenciação (**).

- Estruturas de controle condicional:
  - Use ''if' para especificar um bloco de código a ser executado, se uma condição especificada for verdadeira
  - Use 'else' para especificar um bloco de código a ser executado, se a mesma condição for falsa
  - Use 'else if' para especificar uma nova condição para testar, se a primeira condição for falsa
  - Use 'switch' para especificar muitos blocos alternativos de código a serem executados

- Estruturas de repetição:
  - 'for' : Repetições através de um bloco de código com um número determinado de vezes;
  - 'for / in' : Repetições através das propriedades de um objeto;
  - 'while' : passa por um bloco de código enquanto uma condição especificada for verdadeira;
  - 'Do / while' : também executa repetidamente através de um bloco de código enquanto uma condição especificada é verdadeira.

- Vetores, matrizes e strings:
  - Vetores: 
```js
  var frutas = ["Melancia", "Melão", "Goiaba"];
```
  - Matrizes: O devicejs não suporta a criação de matrizes, mas podem ser feitos vetores de vetores.
  - strings: 
  ```js
  var nomeMateria = "POS";
```
- Funções:
  - Uma função JavaScript é um bloco de código projetado para executar uma tarefa específica. 
  - Uma função JavaScript é executada quando "algo" a chama.
- Exemplo: 
```js
  function multiplica(num1, num2) {
    return num1 * num2; // a função retorna o produto de num1 e num2
  }
```
## Sintaxe OO
- Classe
  - Define as características do objeto. Uma classe é uma definição modelo das propriedades e métodos de um objeto.
    ```js
    function MyClasse(value) {
      var atributo = value;
    }
    ```
- Objeto
  - Um exemplar de uma classe.
  
- Atributo
  - Uma característica do objeto, como idade, altura, nome, caso estivéssemos tratando de pessoas.
  ```js
  var Pessoa = function(nome)
  {
    this.nome = nome;
  };
  var pessoa1 = new Pessoa('Alice');
  var pessoa2 = new Pessoa('Bob');

  console.log('pessoa1 é ' + pessoa1.nome); // envia "pessoa1 é Alice" ao log
  console.log('pessoa2 é ' + pessoa2.nome); // envia "pessoa2 é Bob" ao log
```
- Método
  - Uma ação do objeto, como ligar, desligar, frear se estivemos representando um veículo, por exemplo. 
  ```js
  var Pessoa = function (genero) {
    this.genero = genero;
    alert('Pessoa instanciada');
  }

  Pessoa.prototype.dizerOla = function()
  {
    alert ('hello');
  };

  var pessoa1 = new Pessoa('Masculino');
  var pessoa2 = new Pessoa('Feminino');

  // Chamando o método dizerOla em Pessoa .
  pessoa1.dizerOla(); // hello
  ```
- Construtor
  - Um método chamado assim que um novo exemplar do objeto for criado. Ele geralmente tem o mesmo nome da classe que o contém.
  ```js
  var Pessoa = function () {
    console.log("exemplar criado"); 
  }

  var pessoa1 = new Pessoa();
  var pessoa2 = new Pessoa();
```
- Herança
  - Uma classe pode herdar características de outra classe.
  ```js 
  // define a classe Pessoa
  function Pessoa() {}

  Pessoa.prototype.caminhar = function(){
    alert ('Estou Caminhando!');
  };
  Pessoa.prototype.dizOi = function(){
    alert ('Oi!');
  };

  // define a classe  Estudante
  function Estudante() {
    // Chama o método pai
    Pessoa.call(this);
  }

  // herda de Pessoa
  Estudante.prototype = new Pessoa();

  // corrige o ponteiro construtor, que aponta para Pessoa
  Estudante.prototype.constructor = Estudante;
 
  // adiciona o método dizOi
  Estudante.prototype.dizOi = function(){
    alert('Oi, eu sou estudante');
  }

  // adiciona o método dizTchau 
  Estudante.prototype.dizTchau = function(){
    alert('tchau');
  }

  var estudante1 = new Estudante();
  estudante1.dizOi();
  estudante1.caminhar();
  estudante1.dizTchau();

  // checa a herança
  alert(estudante1 instanceof Pessoa); // true 
  alert(estudante1 instanceof Estudante); // true
  ```
- Polimorfismo
  - Diferentes classes podem definir o mesmo método ou propriedade.
- Sobrecarga

