---
layout: post
title:  "Aprendendo a usar a ferramenta do desenvolvedor no Chrome - Parte 1"
date:   2018-03-11 07:43:40 +0300
img:
description: Debugar seu código é importante, pois é preciso aprender onde está o problema de um código que não está funcionando como esperado, e a ferramenta do desenvolvedor do Chrome é uma ótima ferramenta para descobrir onde está o seu problema
categories: Navegadores
published: true
---

<p>Debugar seu código é importante, pois muitas vezes é preciso descobrir onde está o problema de um código que não está funcionando como esperado, e a ferramenta do desenvolvedor do Chrome é uma ótima ferramenta para descobrir onde está o seu problema. Este post vai te dar algumas dicas se você está iniciando nos estudos de <strong>HTML</strong>, <strong>CSS</strong> e <strong>Javascript</strong></p>

<p>Para ter acesso ao console do Chrome, você pode usar o atalho <strong>Ctrl</strong> + <strong>Shift</strong> + <strong>j</strong> no Windows, ou <strong>Cmd</strong> + <strong>Option</strong> + <strong>i</strong> no Mac OSX. Outra forma de acessar é clicar com o botão direito do mouse e selecionar a opção <strong>Inspecionar</strong></p>

<figure>
  <p>
    <img src="{{ "/assets/img/console-aberto.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<h2>Elements</h2>

<p>A aba elements mostra o código HTML da página atual que você está visualizando. É possível clicar nas setinhas para abrir ou fechar os blocos de código</p>

<figure>
  <p>
    <img src="{{ "/assets/img/elements-left.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>A sessão lateral à direita mostra também o css que está sendo aplicado no elemento que você selecionou no HTML. No exemplo da imagem, foi selecionado a tag <strong>H1</strong>, com o conteúdo <strong>Elements</strong>, e na direita verifica-se que ele possui <strong>font-size</strong> de 2em, e <strong>margin</strong> de 0.67em e 0</p>

<figure>
  <p>
    <img src="{{ "/assets/img/elements-right.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>Essa aba permite que você veja se o HTML está se comportando da forma esperada, então é possível verificar se as tags estão fechando corretamente caso a página esteja com um visual inesperado. Além disso é possível ver se os estilos estão sendo aplicados corretamente nas tags que você quer</p>

<p>Outra observação interessante é que você pode alterar os valores na sessão direita, mudando em tempo real o estilo da página que está sendo visualizada, para ajustes finos do seu css</p>

<h2>Console</h2>

<p>Esta aba está relacionada com o JavaScript. É possível digitar comandos em JavaScript onde o cursor aparece, e testar diretamente funções que você tenha carregado na sua página</p>

<figure>
  <p>
    <img src="{{ "/assets/img/console.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>Se seu código JavaScript não está funcionando corretamente, quaisquer erros que ocorrem durante a execução aparecem nesta aba. Uma dica para verificar se sua função está sendo chamada é por um <strong>console.log</strong> no seu código, e este também aparecerá nesta aba</p>

<h2>Sources</h2>

<p>Esta aba permite ver todos os arquivos que estão relacionados ao seu HTML, como arquivos JavaScript e arquivos CSS. Basta acessar eles a partir da árvore de arquivos na lateral esquerda</p>

<figure>
  <p>
    <img src="{{ "/assets/img/source.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>Além disso, uma ótima funcionalidade desta aba é para debugar o seu JavaScript. Se você usar a palavra-chave <strong>debugger</strong> no seu código JavaScript, com a ferramenta do desenvolvedor aberta, no momento que seu código JavaScript for chamado sua execução será pausada no local onde você inseriu esse comando</p>

<figure>
  <p>
    <img src="{{ "/assets/img/debugger1.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>Se você digitar <strong>ESC</strong>, você conseguirá trazer a funcionalidade da aba <strong>Console</strong> ao mesmo tempo que visualiza a aba <strong>Sources</strong>, e digitando no console o nome das variáveis, ou usando elas em outros comandos JavaScript, você consegue checar seus valores e verificar o que está acontecendo durante a execução</p>

<figure>
  <p>
    <img src="{{ "/assets/img/debugger2.png" | prepend: site.baseurl }}" alt="Emmet" class="center-img">
  </p>
</figure>

<p>Estas abas são extremamente úteis e serão muito usadas na sua vida como desenvolvedor Web. Em um outro post no futuro falarei um pouco das outras abas da ferramenta do desenvolvedor</p>
