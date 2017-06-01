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

### o jQuery é uma biblioteca do JavaScript que adiciona funções para manipulação do html e css. Dentre elas:

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

- Uma parte muito importante do jQuery é a possibilidade de manipular o DOM. No jQuery existem métodos DOM que facilitam o acesso e manipulação de elementos e atributos.

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

Você pode também atribuir os valores

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

- `ToggleClass ()`: Alterna entre adicionar / remover classes dos elementos selecionados

```
$("button").click(function(){
    $("h1, h2, p").toggleClass("blue");
});
```

- `Css ()`: Define ou retorna o atributo de estilo

`$("p").css("background-color", "yellow");`



- Mais em: [W3](https://www.w3schools.com/jquery/ "").
