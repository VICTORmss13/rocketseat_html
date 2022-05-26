

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
