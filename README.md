# jQuery

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>

## Resumo

### Propósito da linguagem:

  JQuery é uma biblioteca de JavaScript, seu principal objetivo é ajudar os desenvolvedores na produção do código, dando a eles o foco da lógica e facilitando quanto as ferramentas do desenvolvimento. O JQuery reune uma quantidade enorme de funções que facilitam a vida de quem desenvolve em JavaScript. Seu lema é "write less, do more." 
  
  
### Paradgima da linguagem:

Utiliza vários paradigmas. Principalmente o imperativo ou procedural, mas também orientado a objetos e funcional.


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

- Além dessas, existem os operadores mais basicos: adição(+), subtração(-), multiplicação(*) e divisão(/);

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
