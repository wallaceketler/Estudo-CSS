# Estudo-CSS

Em CSS, a maneira na qual fazemos as implementações varia entre três formas:

### Inline
--------------------------------------------------

A primeira delas é a inline, na qual podemos definir estilos para a página Web diretamente no código HTML, mais especificamente na definição de um parágrafo ou similar. Exemplo:

~~~HTML
<p style = "color : red"> Texto Qualquer </p>
~~~

### Internal
--------------------------------------------------


A segunda maneira de produzir estilos com CSS é a interna, na qual escrevemos os comandos no 'head' do código html, o que facilita, pela primeira vez, quando precisamos definir as informações para diversos parágrafos ou títulos de mesmo tamanho. Exemplo:

~~~HTML
<html>
  <head>
    <style type = "text/css" >
      p{
        color : red;
      }
    </style>
  </head>
</html>
~~~

Neste caso, o 'p' antes das chaves é o chamado seletor, pois seleciona qual parte do 'body' vai ser alterada. 
Também podemos misturar o inline com o interno com para criar exceções nas quais não queremos que fiquem com a configuração do seletor.
Entretanto, para exceções, o ideal é a utilização de classes e id's: As classes são definidas como '.nome' e os id's como '#nome'. 
Enquanto as classes servem para mais de uma exceção, cada id deve ser utilizado uma vez na página, apesar de podermos criar mais de um

~~~HTML
<html>
  <head>
    <style type = "text/css" >
      .paragrafo{
        color : green;
      }
      #cabecalho{
        color : blue;
        background : gray;
      }
    </style>
  </head>
  
  <body id = "cabecalho">
    <p class = "paragrafo">
      Qualquer Texto
    </p>
  </body>
</html>
~~~

Complementarmente, o CSS fornece as 'divs' e o 'span' que são formas de estruturar a página web, uma vez que cria blocos ou linhas para separações

~~~HTML
<html>
  <head>
    <style type = "text/css" >
      .divs{
        color : green;
        background : blue;
      }
      #spans{
        color : pink;
        background : gray;
      }
    </style>
  </head>
  
  <body>
    <div class = "divs">
      Texto Qualquer (Bloco)
    </div>
    <div class = "divs">
      Texto Qualquer 2 (Bloco)
    </div>
    
    <span id = "spans">
      Texto Qualquer (Linha apenas)
    </span>
    
  </body>
</html>
~~~

Perceba que, já que o 'span' é do tipo linha podemos colocar um na frente do outro, o contrário das 'divs', por serem do tipo bloco, podem ser colocadas apenas um abaixo do outro, por enquanto.






