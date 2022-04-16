Iniciando novamente. 
<!--Discover > Guia Estelar de HTML > Conceitos (16-04-22)
**inicio**-->
Recomendações de extensões:
HTML Preview (para mostrar o preview do resultado em aba separada de forma ao vivo)
primeiro arquivo criado é de extensão .HTML e o nome do arquivo não tem espaço nem acentuação.
Exemplo: "Rocketseat2.html"

Mostrou como ele usa o preview. 
Eu uso com os comandos (Ctrl+k depois v). Desta forma o prreview fica a direita. 

HTML - Hyper Text Markup Language.
Mostrou o html através do inspect da pagina do browser. 
falou de comentários. (Pra fazer comentários no html devemos escrever os sinais a frente, unidos:
'< ! - -'
desta forma o simbolo muda para '<!--' --> O final daquela sessão de comentários acaba após os sinais:
'- - >'. Bastante intuitivo.

Anatomia das tags:
abertura de tags, fechamento de tags, conteudo, elementos. 
abertura<h1>
conteudo 
fechamento</h1>

O todo é um elemento

Elemento vazio: <img src="" alt"">
<input type="text">
Imagem é um tipo de elemento vazio, ou seja, não tem conteudo. Mesma coisa ocorre com input
É errado "fechar" elementos vazios 

Elementos possuem atributos. Atributos podem ser informações extras ou configurações. 
exemplo: <img src="imagem.png" alt="Texto alternativo: 'Imagem com erro. Recarregue a pagina'">

No exemplo, vemos que caso a imagem esteja com algum erro, o alt (alternativo) será o conteudo mostrado na pagina. 
De forma que a frase entre aspas vai ser mostrada sugerindo o refresh da pagina.  

Existem tambem os atributos boleanos. Esses atributos não precisam de conteudo. 
Exemplo: <input type="text" disabled>
Desta forma não é necessário colocar "disabled='alguma coisa'"
Isto porque o disabled é um atributo boleano.

Falando sobre aspas. 
<a href=""> link</a> 
o href mostra "pra onde" vai levar 
Caso coloque <a href=https://google.com> link</a> e não coloque aspas poderá ser um problema caso tenha outra tag. 
Exemplo: <a href=https://google.com target=""> link</a>

Isto se pode ser errado porque o navegador pode interpretar isso da forma errada. 
Deu exemplo sobre o quanto temos que ficar atento ao uso das aspas. Padronizar um tipo de aspas para separar o trecho escrito 
e depois escolher o outro tipo de aspas para marcar as aspas internamente ao trecho. Exemplo:

"estou usando aspas duplas pra marcar o texto e no cao escolheria aspas simples pra mostrar as aspas, 
por exemplo, caso eu mencione o uso da expressão inglesa isn't. Desta forma não haveria problema."

Dica dada no curso é de priorizar o uso das aspas duplas. 

Falando de atributos globais. 
Atributos globais mais utilizados são:
class, contenteditable, data-*, hidden, id, style, tabindex, title. 

<div class="carrinho">

Aqui viriam elementos (conteudo)

</div>

Class é usada para poder usar os estilos no CSS e tbm para poder acessar através do Javascript. 

outro atributo é o contenteditable

ficaria :

<div class="carrinho" contenteditable="true">
conteudo
</div>

Desta forma ficaria editavel a classe do carrinho

atributo data nos permite adicionar oque quisermos desde que com traço ou tudo junto. 
exemplo: 

<div class="carrinho" data-qualquercoisaqueeuquiser="">
conteudo
</div>

OU 

<div class="carrinho" data-qualquer-coisa-que-eu-quiser="">
conteudo
</div>

data é um atributo muito utilizado mais tarde no Javascript e tbm utilizado no CSS 

Continuando para o atributo Hidden. Obviamente, ele esconde a tag. 
Exemplo:

<div class="carrinho" hidden>
conteudo
</div>

Atenção, se for repetir algum nome devemos repetir a classe e não algum atributo, exemplo o id.

tag style ajuda a já aplicar a estilização direto no html. 

tab index é interessante, porque após "marcar" algum item com o atributo tab index fica possível navegar pela pagina utilizando o tab index. 
Ou seja, o usuario pode navegar na pagina utilizando a tecla tab. Exemplo que gostei de imaginar é para paginas com muitos formulários.
Mais facil para pessoas que não tem acesso ao mouse ou que não conseguem navegar legal. 


Por fim o atributo title. Obviamente esse atributo categoriza um titulo. 

Para estudar outros atributos sugeriu o site "developer.mozilla.org"

Seguindo para falar de aninhamento de tags:
Exemplos mostrados: Fluxo, hierarquia, posicionamento dos elementos.

Exemplo abaixo mostra um paragrafo.
<p>
  vou escrever um paragrafo
</p>

Exemplo abaixo mostra um paragrafo com aninhamento, adicionando tag de enfase(transforma conteudo em italico).

<p>
  vou <em>escrever</em> um paragrafo
</p>

Temos que nos atentar para abrir e fechar as tags nos locais corretos. Sempre buscando manter um padrão para que o codigo fique mais coerente.
No exemplo a tag em deve ser fechada dentro da tag p. Isto porque senão o conteudo destacado como enfase acaba se espalhando para outros itens para além 
dos que realmente eram os desejados. 

Desta forma fica evidente a necessidade da hierarquia das tags. Cada tag é lida na ordem que aparece na pagina. 

Atenção para utilizar cada tag. Tentar entender a função. Por exemplo, deve-se posicionar a tag p da forma correta para quebrar a linha, por se tratar de um paragrafo. 

tag br quebrar a linha (break em ingles)
br é diferente porque ele tem fechamento automatico e pode ser usado de forma diferente. 

Hora do praticar. (exemplos de praticas estarão no documento "Rocketseat2.html" na parte que identifica a data de hoje.)


pratiquei e consegui entender tranquilamente. 

Seguindo para conteudo de caracteres reservados:

Exemplos sobre os caracteres reservados como 
- - - - - - - - - -
&nbsp;
<
&lt;
>
&gt;
&
&amp;
""
&quot;
&apos;
- - - - - - - - - -

Seguindo falando sobre Anatomia de um documento HTML 

Começar com o"<!DOCTYPE html>"
Isso serve para que alguns navegadores possam identificar que estamos trabalhando com conteudo HTML 

Outro exemplo é a tag "<html> </html>"
Essa tag, tbm chamada de elemento root (o mais importante) contem 2 importantes elementos, que sao o head e o body. Abaixo mostrados. 

<head></head>
<body></body>

 Exemplo de uso das tags mencionadas: 

 <!DOCTYPE html>
 <html> 
  <head>
    <title> Anatomia do Documento</title>

  </head>
  <body></body>
 
 </html>

Neste exemplo acima a pagina criada terá o nome da aba no navegador como "Anatomia do Documento"

Outro exemplo de tags é o uso do charset.

 <!DOCTYPE html>
 <html> 
  <head>
    <meta charset="urf-8">
    <title> Anatomia do Documento</title>

  </head>
  <body>
    <h1>Titulo</h1>
    <p> Exemplo de conteudo para a primeira pratica. <em>Exemplificando a importância da enfase</em> e de deixar <strong>uma parte do texto destacado com importância.
    </strong> </p> 
    <p> Sem mencionar a parte de um paragrafo e citar um possivel link para o google (<a href="https://google.com"> link</a>) para poder direcionar para mais informações profundas. 
    </p> 
  </body>
 
 </html>

Para ter o "basico" pode-se iniciar o documento html com o comando "!" que o VSCode, 
através da ferramenta emmet completa com o que ele considera sendo o mínimo/basico. 

Exemplo desta exclamação ("!) ficou como abaixo: 


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device=width,
  initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>

lang é a linguagem do site para o navegador. 

A tag name com as informações de content está configurando para que seja visivel 
tanto em dispositivos maiores quanto em mobiles

Por fim mostrando como criar projetos. 
Mostrou a parte de criar documento, pastas, nome de projeto, etc. 


<!--**FIM** 16-04-22->


<!--Discover > Guia Estelar de HTML > Trabalhando com Elementos (xx-xx-xx)-->












