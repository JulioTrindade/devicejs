# jQuery

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>

## Resumo

### Propósito da linguagem:

  JQuery é uma biblioteca de JavaScript, seu principal objetivo é ajudar os desenvolvedores na produção do código, dando a eles o foco da lógica e facilitando quanto as ferramentas do desenvolvimento. O JQuery reune uma quantidade enorme de funções que facilitam a vida de quem desenvolve em JavaScript. Seu lema é "write less, do more." 
  
  
### Paradgima da linguagem:

Utiliza vários paradigmas. Principalmente o funcional, como também o procedural.


### Data de criação:  

26 de agosto de 2006 no BarCamp de Nova York, por [John Resig](https://en.wikipedia.org/wiki/John_Resig ""). 


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

- `$ (.classe)` para selecionar uma classe;

- `$ (#id)` para selecionar um id;

- `$ ("*")` seleciona todos os elementos.

### Eventos

- São ações do visitante que uma página da web pode responder.Exemplos: Mover mouse sobre o elemento, selecionar um botão, clicar em um elemento, entre outros.

`click()`

`dblclick()`

`mouseenter()`

`mouseleave()`

`hover()`

### Vantagens

- Permitir uma maior compatibilidade de um mesmo código com diversos navegadores;

- Traz uma sintaxe mais "fluida" nas tarefas mais comuns ao programador: selecionar um elemento do documento e alterar suas características.

```
// JavaScript "puro"
var cabecalho = document.getElementById("cabecalho");

if (cabecalho.attachEvent) {
  cabecalho.attachEvent("onclick", function (event) {
    alert("Você clicou no cabeçalho, usuário do IE!");
  });
} else if (cabecalho.addEventListener) {
  cabecalho.addEventListener("click", function (event) {
    alert("Você clicou no cabeçalho!")
  }, false);
}

// jQuery
$("#cabecalho").click(function (event) {
  alert("Você clicou no cabeçalho!");
});
```

`$("#cabecalho").css({"margin-top": "20px", "color": "#333333"}).addClass("selecionado");`

### Seletores

- Um dos maiores poderes do jQuery está na sua capacidade de selecionar elementos a partir de seletores CSS.

`$('tbody td').hide();`

`$('#form').css('background', 'black');`

`$('.headline').hide();`

`$('p').text('John Resig');`

- Existem diversos seletores herdados do css que servem para selecionar elementos baseados no DOM.

```
$('div > p'); // <p>s imediatamente filhos de <div>
$('p + p'); // <p>s imediatamente precedidos por outro <p>
$('div:first-child'); // um elemento <div> que seja o primeiro filho
$('div:last-child'); // um elemento <div> que seja o último filho
$('div > *:first-child'); // um elemento que seja o primeiro filho direto de uma <div>
$('div > *:last-child'); // um elemento que seja o ultimo filho direto de uma <div>
$('div p:nth(0)'); // o primeiro elemento <p> filho de uma <div>
$('div:empty'); // <div>s vazios
```

### Funções

- Funções são a unidade básica de ação em jQuery. O principal ponto de entrada da maioria das aplicações em jQuery é um bloco de código semelhante ao que se apresenta abaixo:

```
$(document).ready(function() {
    Do Something
});

```
- `$(document)` é um objeto jQuery. O `$()` é, na verdade, uma função disfarçada. Ela transforma o document em um objeto jQuery.
- `.ready()` é um tipo de função. Você pode vê-la como um auxilío para executar o código dentro dos parênteses assim que o documento HTML estiver pronto.
- `function(){}` é a ação que `.ready()` vai desempenhar assim que o documento HTML estiver carregado. (No exemplo acima, o lugar onde está o `Do Something` (faça alguma coisa) é onde as ações devem ficar).


## Sintaxe Funcional

### O jQuery é uma biblioteca do JavaScript que adiciona funções para manipulação do html e css. Dentre elas:

- `hide()`: Esconder

```
$("#hide").click(function(){
    $("p").hide();
});
```

- `show()`: Exibir

```
$("#show").click(function(){
    $("p").show();
});
```

- `toggle()`: alterna entre `hide()` e `show()`

- `fadeIn()` e `fadeOut ()`: aparecer / desaparecer (gradualmente)

```
$("button").click(function(){
    $("#div1").fadeIn();
    $("#div2").fadeIn("slow");
    $("#div3").fadeIn(3000);
});
```

```
$("button").click(function(){
    $("#div1").fadeOut();
    $("#div2").fadeOut("slow");
    $("#div3").fadeOut(3000);
});
```

- `fadeToggle ()`: alterna entre `fadeIn()` e `fadeOut()`

- `animate ()`: criar animações personalizadas

```
$("button").click(function(){
    $("div").animate({left: '250px'});
}); 
```

- `slideDown ()`/ `slideUp ()`: deslizar um elemento para baixo/cima

```
$("#flip").click(function(){
    $("#panel").slideDown();
});
```

- `slideToggle()`: alterna entre `slideDown ()` e `slideUp ()`

- `stop ()`: interrompe uma animação ou efeito antes que ele seja concluído

```
$("#stop").click(function(){
    $("#panel").stop();
});
```

- `Text ()`: Define ou retorna o conteúdo do texto dos elementos selecionados

- `Html ()`: Define ou retorna o conteúdo dos elementos selecionados (incluindo marcação HTML)

```
$("#btn1").click(function(){
    alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
    alert("HTML: " + $("#test").html());
});
```

- Você pode também atribuir os valores

```
$("#btn1").click(function(){
    $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
    $("#test2").html("<b>Hello world!</b>");
});
```

- `AddClass ()`: Adiciona uma ou mais classes aos elementos selecionados

```
$("button").click(function(){
    $("h1, h2, p").addClass("blue");
    $("div").addClass("important");
});
```

- `RemoveClass ()`: Remove uma ou mais classes dos elementos selecionados

```
$("button").click(function(){
    $("h1, h2, p").removeClass("blue");
});
```

- `Css ()`: Define ou retorna o atributo de estilo

`$("p").css("background-color", "yellow");`
`$("a").first().css("background","#00f");//com o "first()" a propriedade é aplicada apenas para o 1° link do site`

- `each ()`: facilita a iteração em elementos de um Array 

```
var pessoas = ["João", "José", "Maria", "Antônio"];

$.each(pessoas, function(index, item) {
  alert(item);
})
```

- Mais em: [W3](https://www.w3schools.com/jquery/ "") e [jQuery API](http://api.jquery.com/ "").
