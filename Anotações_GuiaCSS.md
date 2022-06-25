

<!--Discover > Guia Estelar de CSS > Abertura (12-05-22)
**inicio**-->

Abertura dos estudos sobre CSS 

--> Conhecendo o CSS:

CSS - Cascading Style Sheet 
Código pra criar estilos no HTML 
HTML é a estrutura, e o CSS é a beleza (enfeite)
Não é linguagem de programação
É uma linguagem style sheet

Exemplo: 
Acessou o site codepen.io e começou a mostrar exemplos. 

Vou acompanhar abrindo na minha pagina tbm e vou transcrever ao final 
algum trecho que eu ache interessante.

--> Comentários:

Não irá agetar o seu código 
Ajuda a lembrar blocos de código 
Deixa dicas para leitura
Ajuda outros a entender
Nunca esqueça de fechar um comentário

Comentário no CSS começam com /* e terminam com */

Exemplo:

/* Aqui fica o comentário */

body{
  font: 1em/150% Helvetica, Arial, sans-serif;
  padding: 1em;
  margin: 0 auto;
  max width: 33em;
}

@media (min-width: 70em) {
/* cometario sobre o codigo que estou escrevendo */
  body {
    font-size: 130%;
  }
}

h1 {font-size: 1.5em;}


Tambem vale lembrar que os comentarios podem ser usados para desabilitar algum trecho de codigo 
durante algum teste ou permanentemente. (muito usado)


--> Anatomia:

- Selector - Procura no HTML alguma tag com aquele nome. No exemplo abaixo é o 'h1'
- Declaration - Está entre os {}
- Properties - Parte da esquerda de cada linha. Mostra a propriedade que vai ser alterada.
- Property Value - Parte da direita da linha. Mostra o valor da propriedade correspondente.

EXEMPLO:

h1 {
  color: blue;
  font-size: 60px;
  background: gray;
}

Observação: Quanto mais propriedades conhecemos mais conseguimos fazer alterações no site/tela.
Tem um curso somente sobre propriedades 


--> Seletores: 

Conecta um elemento HTML ao CSS.

Tipos

- Global selector - '*'
- Element/Type selector - 'h1, h2, p, div'
- ID Selector '#box, #container'
- Class Selector '.red, .m-4'
- Attribute selector, Pseudo-Class, Pseudo-element, e outros



--> Box model: 
São caixas. Os elementos na tela podem ser divididos em caixas. 

(Quase) tudo são caixas no CSS
Posicionamentos, tamanhos, espaçamentos, bordas, cores
Pode-se por exemplo posicionar uma caixa ao lado da outra e etc
Elementos HTML são caixas

--> Origem do CSS:
Como adicionar CSS no documento HTML 

Formas de se adicionar:
- inline -  * atributo 'style'
- <style> -  * tag html que irá conter o css
- <link> -  * arquivo css externo
- @import -  * arquivo css externo

Uma das melhores praticas do mercado é através do link.
Isto porque fica muito mais organizado.

Mostrou a possibilidade de utilizar o @import. 
Acessou o site "fonts.google.com", achou uma fonte que gostou e foi na parte de embed.
Lá estava o código para importar

A ideia que ele sugeriu foi de 

Pegou através do "font-family: 'Ranchers', 'cursive;"

Disse que deve-se dar preferência ao uso do <link>


--> A Cascata (Cascading): 

É a escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.
*Seu estilo é lido de cima para baixo. 
É levado em consideração 3 fatores
  - Origem do estilo
  - Especificidade
  - Importância

  

--> Especificidade:
--> Regra importante:
--> At rules:
--> Shorthand:
--> Funçoes:
--> Devtools:
--> Cuidados com a escrita:
--> Vendor prefixes:





<!--**FIM** 12-05-22->


<!--Discover > Guia Estelar de CSS > A Cascata (25-05-22)
**inicio**-->

# A Cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento. 
* Seu estilo é lido de cima para baixo. 
É levado em consideração 3 fatores 

1- Origem do estilo 
2- Especificidade
3- Importância 

### Origem do estilo 

inline > tag style > tag link 

### Especificidade 

É um cálculo matemático, onde cada tipo de seletor e origem do estilo, possuem valores a serem considerados. 

<!--**FIM** 25-05-22->

<!--Discover > Guia Estelar de CSS > A Cascata (25-05-22)
**inicio**-->

A partir de hoje meu intuito vai ser tentar seguir assistindo as aulas e tentar reproduzir oque for mostrado no momento de algum projeto ou em outro momento oportuno durante o proprio curso. 

O termo de Cascata ocorre porque a leitura e aplicação segue a ordem de cascata (de cima pra baixo)
ou do mais antigo para o mais recente.

<!--**FIM** 25-05-22->

<!--Discover > Guia Estelar de CSS > Especificidade (25-06-22)
**inicio**-->
Voltei a dinamica antiga em que anoto tudo normalmente. 
O importante é continuar. Um pouco todo dia. 

Guia Estelar de CSS > Especificidade

### Especificidade 

É um cálculo matemático, onde cada tipo de seletor e origem do estilo, possuem valores a serem considerados. 

0. Universal selector, combinators e nagation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e attribute selectors ([type="radio"])
100. ID selector
1000. Inline

Seletor Universal que é um '*' não traz preferencia sobre os outros seletores. 
O entendimento é que quanto maior o numero mencionado na classificação acima, 
maior a preferencia do objeto sobre outros.

Exemplo de uso dessas preferencias (especificidade):

HTML 
<h1 class="title" id="mytitle"> Título <strong>alo<strong></h1>

CSS
#my-title {
  color: gray;
}

.title {
  color: red;
}

h1.title#my-title {
  color: blue;
}

* {
  color: green;
}


Neste exemplo acima temos que o elemento que menciona a cor blue será o elemento com preferencia.
Isto porque está com muitos elementos somados (h1 + title + #my-title)

No caso acima o titulo 'Título' vai ficar com os elementos acima, 
porém o titulo 'alo' vai ficar verde, por causa do *


### Regra important

* Cuidado, evire o uso
* não é considerado uma boa prática
* quebra o fluxo natural da cascata

Ao adicionar '!important' o elemento com essa regra fica priorizada entre TODAS as outras regras.

Exemplo: Caso esteja usando uma biblioteca de alguém e não consigo modificar a não ser a partir do !important.


# At-rules 
(At = @ [no ingles])

* Está relacionado ao comportamento do CSS
* começa com o sinal de '@' seguido do identificador e valor

## Exemplos comuns 

- @import     /* incluir um CSS externo */
- @media      /* regras condicionais para dispositivos */
- @font-face  /* fontes externas */
- @keyframos  /* Animation */

INICIO'''css1
@import "http://local.com/style.css";
@import url("http://local.com/style.css");

@media (min-width: 500px) {
  (adicionar as regras aqui)
}

@font-face {
  (adicionar as regras aqui) 
}

@keyframes nameofanimation {

}
FIM'''css1


#Shorthand 

* junção de propriedades
* resumido
* legível

INICIO'''css2
{
  /* background properties */
  background-color: #000;
  background-image: url(images/bg.gif);
  background-repeat: no-repeat;
  background-position: left top;

  /* background shorthand */
  background: #000 url(images/bg.gif)  no-repeat left top

  /* font properties */
  font-style: italic;
  font-weight: bold;
  font-size: .8em;
  line-height: 1.2;
  font-family: Arial, sans-serif;


  /* font shorthand */
  font: italic bold .8em/1.2 Arial, sans-serif;
}
FIM'''css2

## Detalhes 

* não irá considerar propriedades anteriores
* valores não especificados irão assumir o valor padrão
* geralmente, a ordem descrita não importa, mas, se houver muitas propriedades
com valores semelhantes, poderemos encontrar problemas


## Propriedades que aceitam shorthand

animation, background, border, border-bottom, border-color, border-left,
border-radius, border-right, border-style, border-top, border-width,
column-rule, columns, flex, flex-flow, font, grid, grid-area, grid-column,
grid-row, grid-template, list-style, margin, offset, outline,  overflow, padding,
place-content, place-items, palce-self, text-decoration, transition
**https://developer.mozilla.org/en-us/docs/web/CSS/shorthand_properties**

# Funções 

* nome seguido de abre e fecha parentesis
* recebe argumentos (valores dentro dos parentesis são os argumentos)

## Exemplos

INICIO'''css3
@import url ("http://urlaqui.com/style.css")
{
  color: rgb(255, 0, 100);
  width: calc(100% - 10px);
}

FIM'''css3

# DevTools

F12 no navegador abre o DevTools

No campo 'Elements' temos o HTML e o CSS 
Usar essa ferramenta para entender como os sites realmente estão. 

No campo 'Console' temos o Javascript


# Cuidados com a escrita
Temos que ter cuidado com a escrita do CSS, senão podemos estragar ou quebrar o codigo. 
Importante estar identado.
Exemplo de codigo da aula:

---inicio exemplo---
p {
  margin: 0 auto;
  padding-left: 15px;
}
---fim exemplo---

# Vendor prefixes

Permite que browsers adicionem 'features'
a fim de colocar em uso alguma novidade que vemos no CSS

## Exemplo

INICIO'''css4
p {
  -webkit-background-clip: text; /* Chrome, Safari, IOS e Android */
  -moz-background-clip: text;    /* Mozilla (Firefox) */
  -ms-background-clip: text;     /* Internet Explorer */
  -o-background-clip: text;      /* Opera */
}
FIM'''css4

# Consultas 

.[http://ireade.github.io/which-vendor-prefix/].
.[http://caiuse.com].

<!--**FIM** 25-06-22->
