---
layout: post
title:  "Programação funcional com JS - Parte 1"
date:   2019-06-22 17:24:00 +0300
img:
description: Conceitos de programação funcional com JS
categories: Desenvolvimento Web
published: true
---

<p>Neste post, pretendo dar os conceitos básicos por tras do que é chamado programação funcional.</p>

<p>Pega algo para comer / beber, e leia com calma cada um dos exemplos e a explicação, pode ser um pouco maçante, mas vai valer a pena.</p>

<p>A programação funcional é um paradigma de programação que enfatiza a aplicação de funções. Não são todas as linguagens que suportam este paradigma.</p>

<p>Uma característica importante da linguagem para poder aplicar esse paradigma é que ela tenha <strong>funções de primeira classe</strong>. Nesse caso, as funções podem ser consideradas como valores, e podem ser passadas como parâmetro para outras funções.</p>

<p>Ficou complicado? Vamos ao código.</p>

<p>Abaixo, temos um código que mostra como criamos (definimos) uma função.</p>

<script src="https://gist.github.com/HugoTamaki/a775c77ecf2a8b8c75eb4b713133bcbe.js"></script>

<p>O <strong>function</strong> é uma palavra reservada do JavaScript, que indica que estamos iniciando a definição de uma função. O <strong>double</strong> é o nome que você está dando à função. Dentro da função, entre as chaves, está o código que a função irá executar. No caso do exemplo, ela receberá um número qualquer (<strong>number</strong>), e irá dobrar ele, ou seja, multiplicar por 2.</p>

<p>Em JavaScript também é possível atribuir uma função a uma variável, e essa variável passa a ser do tipo <strong>function</strong> (lembre-se que uma função pode ser um valor).</p>

<script src="https://gist.github.com/HugoTamaki/5f25950a064dc870588eaac074f0d158.js"></script>

<p>Uma vez que eu defino a função, eu consigo invocar ele a qualquer momento usando <strong>double(numero)</strong>. Note que se eu não usar os parenteses na hora de invocar, eu apenas estarei passando o seu valor.</p>

<script src="https://gist.github.com/HugoTamaki/368e0d69cce679e5b45020f7065bf448.js"></script>

<h2>Funções como argumento</h2>

<p>Se você ja viu codigos de JavaScript, já deve ter notado que em alguns momentos, uma função é passada para dentro outra função.</p>

<script src="https://gist.github.com/HugoTamaki/cc900f4effa5aa9af8828c79e1ceafb8.js"></script>

<p>Repare que <strong>setTimeout</strong> é uma função, e ela recebe dois argumentos. O primeiro é uma <strong>função anônima</strong> (ela não tem nome, é definida apenas por <strong>function () {...}</strong>), e o segundo argumento é <strong>1000</strong>.</p>

<p>Esse código faz com que depois de 1000 milisegundos, a função que você definiu no argumento seja executada. Ou seja, depois de 1 segundo, a string "Ping!" é printada no console.</p>

<p>Para ficar mais fácil de entender, eu poderia definir uma função qualquer, como a função que dá ping, e depois passar ela como argumento para o <strong>setTimeout</strong>.</p>

<script src="https://gist.github.com/HugoTamaki/a6bdcf30aff151b77822474597356007.js"></script>

<p>Repare que estou passando no argumento de <strong>setTimeout</strong> apenas <strong>ping</strong> ao invés de <strong>ping()</strong>. Quando eu passo como argumento <strong>ping</strong>, eu estou passando a definição da função como argumento, para que ela seja executada dentro de <strong>setTimeout</strong>. Se eu usasse <strong>ping()</strong>, eu executaria a função no momento em que passo ela como argumento, ao invés de dentro de <strong>setTimeout</strong>.</p>

<h2>Map</h2>

<p>Existem funções importantes no JS que fazem uso do paradigma funcional, um deles se chama <strong>map</strong>. Mas antes de apresentá-lo, eu vou criar uma função map para mostrar de que forma posso passar funções como argumentos, e usá-los dentro da função map. Ficou confuso? Vamos aos exemplos.</p>

<p>A função <strong>map</strong> tem como objetivo <strong>transformar</strong> um array em outro. Ou seja, se eu quiser que um padrão seja aplicado a todos os números de um array, o map é uma excelente opção.</p>

<p>"Ah, mas para isso eu poderia simplesmente iterar com um <strong>for</strong>, não é?"</p>

<script src="https://gist.github.com/HugoTamaki/8976228b4cbee26c344edfe0ae6ce0e7.js"></script>

<p>Sim, poderia usar um for, mas se eu quisesse triplicar os números do array por exemplo, ou aplicar qualquer outro padrão, teria que repetir o <strong>for</strong> toda vez que quisesse fazer essa modificação. Além do mais, estamos aprendendo programação funcional, certo?</p>

<p>Então, como eu criaria uma função <strong>myMap</strong> em que eu aplicaria um padrão para cada valor de um array, usando uma função?</p>

<script src="https://gist.github.com/HugoTamaki/685f072997c9782027764c5a56ce1818.js"></script>

<p>A função <strong>myMap</strong> recebe como argumentos o array e uma função qualquer (<strong>func</strong>).</p>

<p>Dentro de <strong>myMap</strong>, eu crio um array de resultado que recebe vazio, percorro o array que recebo como argumento, e para cada elemento desse array, aplico a função que recebi via argumento - <strong>func(arr[i])</strong>, e depois jogo o resultado dessa transformação pra dentro de result - <strong>result.push(transformedNumber)</strong>.</p>

<p>Agora aplicando a função <strong>myMap</strong>...</p>

<script src="https://gist.github.com/HugoTamaki/44152f55267938efa616ff446d85da60.js"></script>

<p>Nas duas vezes que eu defino a variável result, na primeira eu passo uma função que duplica um número qualquer, e na segunda eu passo uma função que triplica um número qualquer.</p>

<p>Dentro de <strong>myMap</strong>, essas funções que eu passei como argumento são de fato executadas e aplicadas para cada número do array.</p>

<figure>
  <p>
    <img src="https://media.giphy.com/media/26ufdipQqU2lhNA4g/source.gif" alt="blow mind" class="center-img">
  </p>
  <figcaption>
    Bummmmmmm!
  </figcaption>
</figure>

<p>"Aaah, mas isso pareceu muito complicado!"</p>

<p>Bom, de fato, como o paradigma é novo, pode parecer muito complicado, e aí temos a tendência de ficar na zona de conforto e não aprender coisas novas, mas aplicar esse paradigma é bem interessante pra inúmeras situações.</p>

<h2>Map (nativo do JS)</h2>

<p>O JS já tem uma função map nativa, o exemplo acima eu dei apenas como exemplo de como uma função pode ser usada como argumento.</p>

<p>Como na verdade o map é um método de um array, você não precisa passar o array como argumento, bastando chamar o map a partir do próprio array.</p>

<script src="https://gist.github.com/HugoTamaki/c09d6a755cb2ded88246e7dd749fd523.js"></script>

<p>Se você for comparar, entre usar o <strong>for</strong> e o <strong>map</strong>, com map você precisou de apenas 60 caracteres e 3 linhas para transformar o array, enquanto no for, foram necessários 4 linhas e 78 caracteres.</p>

<script src="https://gist.github.com/HugoTamaki/5d4b43ad1649554366cf8bfc94ba85e8.js"></script>

<p>Em um post mais para frente, veremos outras aplicações nativas de programação funcional do JS. Existem métodos prontos para filtrar, para somar elementos de arrays, e callbacks que fazem uso desse paradigma. Até mais!</p>