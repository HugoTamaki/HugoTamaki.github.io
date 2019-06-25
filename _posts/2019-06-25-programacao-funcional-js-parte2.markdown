---
layout: post
title:  "Programação funcional com JS - Parte 2"
date:   2019-06-25 09:46:00 +0300
img:
description: Conceitos de programação funcional com JS - parte 2
categories: Desenvolvimento Web
published: true
---

<p>Este post é uma continuação do post sobre conceitos de programação funcional. Para ver a primeira parte, <a href="/programacao-funcional-js-parte1/">veja aqui</a>.</p>

<h2>Filter</h2>

<p>Na primeira parte sobre conceitos de programação funcional, vimos como conseguimos passar funções como argumentos, para serem executados dentro de outras funções. Vimos também um exemplo com a implementação customizada da função <strong>map</strong>, e também como funciona o <strong>map</strong> nativo do JS.</p>

<p>Agora, vamos ver como funciona o <strong>filter</strong>. O filter é uma função / método em que o resultado trazido é um array que pode ser menor do que o array original, já que passamos para ele uma função com uma <strong>condição</strong> que deve ser usada para filtrar o array original.</p>

<script src="https://gist.github.com/HugoTamaki/1e574ac5696872c842f981f950d9ef91.js"></script>

<p>Repare que no exemplo acima foi passado uma função anônima que recebe um argumento <strong>number</strong>, e retorna uma condição (<strong>se resto de número dividido por 2 é igual a 0, ou seja, se é par</strong>).</p>

<p>Nesse caso, a função que um filter geralmente recebe na maioria das vezes costuma a ser uma <strong>condição</strong> que deve ser checada para filtrar o array original.</p>

<p>Novamente, se formos comparar com uma versão <strong>for</strong>, o filter é bem mais simples de se escrever. Com o for, usaríamos 106 caracteres, com cerca de 6 linhas, e usando apenas um filter, conseguimos enxugar o código para apenas 69 caracteres e 3 linhas.</p>

<script src="https://gist.github.com/HugoTamaki/c52cb0377204f143326cbbb204ca73a6.js"></script>

<h2>Reduce</h2>

<p>O reduce é outra função que faz uso do paradigma funcional no JS, e pode ser usada para muitas aplicações.</p>

<p>O reduce permite que você trabalhe com um array de forma a retornar um resultado apenas, que pode ser a soma de todos os elementos, pode ser também algum tipo de rearranjo dos valores do array... Enfim, fica a cargo da sua criatividade.</p>

<p>Vamos aos exemplos? Um exemplo simples para começar seria retornar o somatório de um array.</p>

<script src="https://gist.github.com/HugoTamaki/ad9b1287f62f5e83b1316d1da27f61d1.js"></script>

<p>Hum, parece um pouco complicado, não?</p>

<p>O primeiro argumento que deve ser passado na função argumento para o reduce é o <strong>acumulador</strong>. No exemplo, ele é o <strong>acc</strong>. Essa variável é a que irá, dentro do reduce, acumulando os valores de qualquer operação que você fizer dentro da função que você passou como argumento.</p>

<p>O segundo argumento que deve ser passado na função argumento é o <strong>valor corrente</strong>. No caso do exemplo, é o <strong>value</strong>. Lembrando que você pode usar quaisquer nomes, já que o conceito não muda.</p>

<p>O <strong>0</strong> passado como segundo argumento do <strong>reduce</strong> (cuidado, aqui o 0 não é um argumento da função anônima, mas sim do reduce) é o valor inicial que o acumulador deve ter. Ele é opcional.</p>

<p>Mas o que acontece exatamente dentro do reduce? Por dentro do reduce, o acumulador recebe o resultado da interação que a função que você passou como argumento faz. Podemos verificar isso dando um print para cada iteração que o reduce faz.</p>

<script src="https://gist.github.com/HugoTamaki/512069bdd016b03c50ef53a9dc18556d.js"></script>

<p>O primeiro valor do acumulador é 0, que foi o valor passado como argumento de valor inicial do acumulador. O valor corrente no primeiro loop é 1 (primeiro valor do array).</p>

<p>No segundo loop, o acumulador recebeu o primeiro valor corrente, e passa a valer 1 (o valor corrente passa a ser 2, o segundo valor do array).</p>

<p>No terceiro loop, o acumulador vale 3, que é resultado do valor do acumulador + 2.</p>

<p>No quarto loop, o acumulador vale 6, e assim por diante... Repare que o acumulador se comporta exatamente como seria no caso de uma <strong>iteração</strong> que você faria para somar elementos de um array.</p>

<h2>Mais que apenas somatório de números...</h2>

<p>Bom, mas o reduce pode ser usado para inúmeros objetivos, e não apenas para somatórios de números. Vou mostrar um exemplo.</p>

<p>Digamos que você receba uma matriz de chaves e valores, e você queira transformar ele em um objeto. O reduce é uma ótima opção. Como?</p>

<script src="https://gist.github.com/HugoTamaki/cb48a174e62d03747eeb93f27e06f4ca.js"></script>

<p>Na função anônima que passo pro reduce, eu separo quem vai ser a chave e quem vai ser o valor (key recebe <strong>current[0]</strong>, e value recebe <strong>current[1]</strong>).</p>

<p>Em seguida, eu crio uma chave no objeto acc, recebendo o valor estabelecido para a chave (repare que eu inicio o acumulador como um objeto vazio <strong>{}</strong>).</p>

<p>Por fim, eu devo retornar o próprio acumulador, para que ele vá sendo atualizado em cada loop. No final de tudo eu tenho um objeto formado com as chaves e valores correspondentes.</p>

<p>O <strong>reduce</strong> é mais complexo que o <strong>map</strong> ou o <strong>filter</strong>, mas as possibilidades que ele oferece são infinitas, e creio que eu mesmo não aproveitei tudo que ele tem a oferecer ainda, mas é bacana tentar se desafiar a usar essas ferramentas nos seus projetos. Uma vez que você pegue o gosto, vai virar um <strong>addict</strong> também, hahaha. :P</p>

<p>No próximo post, pretendo falar sobre como você pode se aproveitar de funções para criar callbacks em funções próprias. Até mais!</p>
