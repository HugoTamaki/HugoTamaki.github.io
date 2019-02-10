---
layout: post
title:  "Iniciando no desenvolvimento web - Conceitos básicos - CSS3"
date:   2019-02-09 13:29:00 +0300
img:
description: Conceitos básicos para iniciar no desenvolvimento web do zero.
categories: Desenvolvimento Web
published: true
---

<p>Este post é voltado para você que não tem ideia do que é HTML, CSS ou JavaScript, mas gostaria de realizar um <strong>hello world</strong> em web.</p>

<h2>Continuando com CSS3</h2>

<p>Você concluiu o hello world do post anterior? Se não, dá uma olhadinha lá! Só acessar <a href="{{ "/iniciando-web-conceitos-basicos-css" | prepend: site.baseurl }}" target="_blank">aqui</a>!</p>

<p>Bom, como fazer para adicionar algum estilo visual para o seu site?</p>

<p>Para esta tarefa, você pode usar CSS3 para o seu recém criado HTML.</p>

<h2>Testando com a tag style</h2>

<p>Para testarmos alguns conceitos de CSS, crie um arquivo com extensão html de acordo com código abaixo.</p>

<script src="https://gist.github.com/HugoTamaki/979af418c2004a34c541effb04481181.js"></script>

<p>Ao renderizar o código acima, veremos que algum estilo foi adicionado para os textos de <strong>h1</strong>, e dos conteúdos das <strong>divs</strong>.</p>

<p>Aqui temos uma tag nova, dentro da tag <strong>head</strong>. É a tag <strong>style</strong>. Essa tag pode receber código escrito em <strong>CSS</strong>.</p>

<p>O CSS tem basicamente duas estruturas. O <strong>seletor</strong>, logo em seguida se abre chaves e em seguida, você pode por uma série de chaves e valores, sendo a chave composta por um atributo (no exemplo, <strong>color</strong>), e o valor sendo qual valor você quer que esse atributo passe a ter (no exemplo, <strong>red</strong>, <strong>green</strong> e <strong>blue</strong>).</p>

<h2>Seletores</h2>

<p>Os seletores usados foram o <strong>h1</strong>, <strong>#meu-id</strong> e <strong>.div-com-classe</strong>.</p>

<p>O seletor nos indica qual elemento html será modificado. No caso do <strong>h1</strong>, quer dizer que todas as tags <strong>h1</strong> do documento vão adquirir a cor vermelha.</p>

<p>O seletor <strong>#meu-id</strong> tem uma característica especial. Ele irá mudar as características de qualquer tag que contenha o <strong>id</strong> igual a <strong>meu-id</strong>. No exemplo, a primeira div contém o atributo <strong>id</strong> como <strong>meu-id</strong> (note que é necessário um <strong>#</strong> para diferenciar esse seletor no CSS).</p>

<p>O seletor <strong>.div-com-classe</strong> mudará o estilo para todas as tags que contenham a classe <strong>div-com-classe</strong> na tag (note que é necessário um <strong>.</strong> para diferenciar esse seletor no CSS).</p>

<h2>Refatorando</h2>

<p>A ideia do CSS era de retirar a aplicação de estilos do HTML. Nas versões anteriores do HTML, o estilo era aplicado diretamente nas tags, e refatorar e replicar código de estilo era complicado e trabalhoso (imagine que cada texto em html em uns 20 arquivos html diferentes tenham a cor em verde, e de um dia para outro você tenha que muda-las para vermelho!).</p>

<p>Abaixo um exemplo de como era feito a mudança de cor, tamanho de fonte e estilo de fonte no HTML</p>

<script src="https://gist.github.com/HugoTamaki/7f4c0283f214efc78a79a5878ca98e81.js"></script>

<p>Então, podemos extrair o CSS que está dentro da tag <strong>style</strong>, do primeiro exemplo, e passa-lo para um arquivo com extensão css, que é o que faremos agora.</p>

<p>Crie um arquivo com extensão <strong>.css</strong>, no mesmo nível de pasta do seu arquivo html. Extraia o código css de dentro da tag <strong>style</strong>. Ele deverá ficar da seguinte forma.</p>

<script src="https://gist.github.com/HugoTamaki/6a6447905bf2bf74196dc96e93129acb.js"></script>

<p>Perfeito, agora você pode apagar a tag <strong>style</strong>, e todo seu conteúdo, e substituir por uma tag <strong>link</strong> que fará referência ao arquivo css que você criou (eu nomeei no exemplo como <strong>estilo.css</strong>, utilize o nome que você deu ao arquivo css).</p>

<script src="https://gist.github.com/HugoTamaki/47ee1446d48e14c4ab3b83dcba31c06a.js"></script>

<p>Recarregue o seu html no navegador, e verifique se os estilos de cor de texto continuam a ser aplicados no html.</p>

<p>Pratique adicionar mais estilos a seu html agora, o importante é praticar.</p>