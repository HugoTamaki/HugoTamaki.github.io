---
layout: post
title:  "Iniciando no desenvolvimento web - Conceitos básicos"
date:   2019-02-02 13:29:00 +0300
img:
description: Conceitos básicos para iniciar no desenvolvimento web do zero.
categories: Desenvolvimento Web
published: true
---

<p>Este post é voltado para você que não tem ideia do que é HTML, CSS ou JavaScript, mas gostaria de realizar um <strong>hello world</strong> em web.</p>

<h2>Entendendo o navegador</h2>

<p>Basicamente, o navegador é um programa que interpreta HTML, CSS e JavaScript, e transforma código em algo gráfico e fácil de ser entendido.</p>

<h2>Como funciona a web?</h2>

<p>De forma muito básica, quando você acessa uma url qualquer, uma requisição é feita do lado do <strong>Cliente</strong> (seu navegador), e chega até o seu destino que é no <strong>Servidor</strong>. O <strong>Servidor</strong> por sua vez identifica a requisição, autentica (se for necessário) e devolve a informação no formato de HTML para o <strong>Cliente</strong>, que por sua vez interpreta o HTML e exibe a página para o usuário.</p>

<p>Então, como o navegador consegue interpretar HTML, ele consegue interpretar também um arquivo com a extensão <strong>.html</strong>! Vamos para os testes então?</p>

<h2>Escolhendo seu editor de código</h2>

<p>Basicamente, é possível você usar o bloco de notas que já vem no sistema operacional que você usa, mas geralmente eles não possuem <strong>Syntax Highlight</strong> (coloração diferenciada para facilitar a leitura de código), então é mais recomendado usar um editor de código.</p>

<h3>Opções de editor de código</h3>

<ul>
  <li>Sublime Text 3 - <a href="https://www.sublimetext.com/3" target="_blank">https://www.sublimetext.com/3</a></li>
  <li>Atom - <a href="https://atom.io/" target="_blank">https://atom.io/</a></li>
  <li>Visual Studio Code - <a href="https://code.visualstudio.com/download" target="_blank">https://code.visualstudio.com/download</a></li>
  <li>Notepad++ - <a href="https://notepad-plus-plus.org/download/v7.6.3.html" target="_blank">https://notepad-plus-plus.org/download/v7.6.3.html</a></li>
</ul>


<p>De longe o <strong>Sublime Text 3</strong> é meu editor preferido, abre projetos e arquivos de forma rápida e raramente trava. Ele sozinho não faz muita mágica, mas ao instalar o Package Control (<a href="{{ "/instalando-package-control-sublime" | prepend: site.baseurl }}" target="_blank">mais detalhes aqui</a>), você pode instalar uma infinidade de plugins que agilizam seu desenvolvimento de uma forma inacreditavel! Segue <a href="{{ "/plugins-interessantes-sublime" | prepend: site.baseurl }}" target="_blank">aqui</a> um post com alguns plugins favoritos que costumo usar. A única desvantagem é que de vez em quando abre um popup para comprar a licença. Comprando a licença o popup para de aparecer, mas as funcionalidades pagando ou não pagando são as mesmas.</p>

<h2>Criando um arquivo .html</h2>

<p>Usando o editor novo, clique em <strong>New File</strong> (Novo arquivo), depois selecione <strong>Salvar como</strong> (Save as) ou digite <strong>Ctrl + S</strong> e salve seu arquivo com um nome qualquer, com a extensão <strong>.html</strong></p>

<figure>
  <p>
    <img src="{{ "/assets/img/saveas.png" | prepend: site.baseurl }}" alt="Nomeando um arquivo nome" class="center-img">
  </p>
  <figcaption>
    Nomeando um arquivo novo
  </figcaption>
</figure>

<h2>Agora vamos ao código!</h2>

<p>Agora podemos criar algum código nesse novo arquivo.</p>

<p>Você pode inserir o seguinte código:</p>

<script src="https://gist.github.com/HugoTamaki/0aeaaed3323d9cd8e71f8b91aa96007a.js"></script>

<p>Salve seu arquivo, clique nele com o botão direito do mouse, e escolha <strong>Abrir com</strong>, e selecione seu navegador favorito. Uma vez feito isto, o navegador irá exibir a sua página, interpretando o HTML que você colou no arquivo!</p>

<h2>Entendendo o HTML</h2>

<p>Você deve ter reparado que existem tags que abrem e que fecham. Por exemplo, a tag <strong>&lt;head&gt;</strong> e a tag <strong>&lt;/head&gt;</strong> marcam a sessão head, que contém meta informações que não são exibidos na página. A tag <strong>title</strong> diz qual vai ser o titulo exibido na aba do navegador, a tag <strong>meta</strong> pode conter varias informações, no caso do exemplo, qual o encoding usado pelo navegador para essa página (no caso, UTF-8, que reconhece acentos)</p>

<p>A tag <strong>body</strong> marca a sessão onde haverão coisas que aparecerão na página em si. A tag <strong>h1</strong> marca um cabeçalho, de nível 1 (para títulos principais). Experimente mudar para <strong>h2</strong>, <strong>h3</strong> ou <strong>h4</strong> por exemplo!</p>

<p>Já o <strong>&lt;!DOCTYPE html&gt;</strong> marca uma informação importante para o navegador, dizendo a ele que o código abaixo é em HTML5.</p>

<h2>Identação</h2>

<p>Reparou que há pequenos espaços em branco na frente de algumas linhas? Esses espaços em branco são chamados de <strong>identação</strong>, e são muito importante para leitura e melhor compreensão quando estiver codando, assim como para outras pessoas que forem ler seu código. Elas indicam que tudo que tem um certo espaço em quantidade igual está dentro de uma tag mais externa. É muito importante se habituar a escrever código bem identado desde o início. O código HTML no caso vai funcionar mesmo se não estiver identado, mas a boa prática é que ele seja identado para ajudar na manutenção do código. Veja o exemplo abaixo:</p>

<script src="https://gist.github.com/HugoTamaki/26cd6399a965805e07a3533faabf5cc8.js"></script>

<p>No exemplo, existe uma tag <strong>div</strong>, que contém uma tag <strong>ul</strong>, que por sua vez contém as tags <strong>li</strong>. Note que é possível observar rapidamente a hierarquia de pertencimento de cada uma delas.</p>

<h2>Pratique muito!</h2>

<p>Agora é questão de praticar! Crie seu próprio blog, crie uma loja para vender alguma coisa, crie um site sobre algum assunto e treine as diferentes tags, e estude pra que cada uma delas serve. Com o tempo você irá saber de cor o que cada uma delas faz.</p>
