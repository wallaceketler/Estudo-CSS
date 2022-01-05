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

Outra propriedade além da cor que pode ser alterada é a borda, na qual escrevemos na seguinte sintaxe:

~~~html

<html>

  <head>
    <style type = "text/css">
      .exemplo{
        border : 15px solid green;
    </style>
</html>
~~~

Quanto às cores, podemos usar hexadecimal para definirmos algumas mais específicas.
A fonte também pode ser alterada a partir de alguns padrões :

~~~html
<html>
  <head>
    <style type = "text/css">
      .exemplo{
          color : #6A5ACD;
          font-size : 30px;
          font-weight : bold; /*representa o peso da fonte, no caso, negrito*/
          font-family : "Times New Roman", Times, serif;
          font-style : italic;
          text-decoration: underline; /* poderia ser overline, line-through... */
      }
    </style>  
  </head>
</html>
~~~
A fonte quando tiver nome composto deve estar entre aspas e devemos definir uma ordem de preferência de utilização para caso o usuário do Web Site não possua a primeira escolhida. Podemos definir uma específica e no fim uma genérica ( como a família serif ), para garantir que tenha em último caso.
O tamanho da fonte pode ser definido por píxels (px), % (relativa ao padrão) e 'em' (relativa ao container pai). Esse último se explica ao aplicarmos, por exemplo, ao 'head' um tamanho de fonte de 30px, se dentro do head tivermos um tamanho de fonte para um 'parágrafo' de 2em, o tamanho ser duas vezes 30px = 60px 
Também podemos definir a fonte em uma única linha, da forma 'font: bold 40px Times'

---------------------------------------------

Podemos também alterar as configurações de background de certo container:

~~~~html
<html>

  <head>
  
    <style type = "text/css">
      .exemplo{
          background-color;                   -> define cor de fundo do container que a classe trabalha
          background-image: url([local]);     -> pega imagem de algum locala
          background-repeat: no-repeat;       -> define se a imagem, quando não completa todo container vai repetir ou não
          background-attachment: scroll;      -> define se vai sumir ao rolar ou não(fixed)
          background-position: center center; -> define primeiro em X e depois em Y
       
      }
  </head>
  
</html>

~~~~






