# jQuery

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>

## Resumo

**Propósito da linguagem:**  

  JQuery é um framework, seu principal objetivo é ajudar os desenvolvedores na produção do código, dando a eles o foco da lógica e facilitando quanto as ferramentas do desenvolvimento. O JQuery reune uma quantidade enorme de funções que facilitam a vida de quem desenvolve em JavaScript. Seu lema é "write less, do more." 
  
  
**Paradgima da linguagem:**

Utiliza vários paradigmas. Principalmente o imperativo ou procedural, mas também orientado a objetos e funcional.


**Data de criação:**  

Dezembro de 2006 no BarCamp de Nova York, por [John Resig](https://en.wikipedia.org/wiki/John_Resig ""). 


**Principal mantenedor:**  

[jQuery Foundation](https://jquery.org/team/ ""). 


## Instalação e uso

- O jQuery pode ser instalado usando uma CDN;

`<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>`

- Salvando-o como arquivo no seu diretório;

- Usando o [npm](https://www.npmjs.com/ "");

`npm install jquery`

- Usando [Bower](https://bower.io/ "");

`bower install jquery`

## Sintaxe Básica

- Um $ sinal para definir / jQuery acesso
- A(selector)para "consulta (ou encontrar)" elementos HTML
- Um jQuery action () a ser executada com o element(s)

- $(this).hide() - esconde o elemento atual.

- $("p").hide() - oculta todas <p> elementos.

- $(".test").hide() - esconde todos os elementos com class="test" .

- $("#test").hide() - esconde o elemento com id="test"

- $(document).ready(function(){

  // jQuery methods go here...  });
  
  -$(function(){

  // jQuery methods go here...  });
   
Exemplo:
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
