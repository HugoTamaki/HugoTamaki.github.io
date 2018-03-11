---
layout: post
title:  "Instalando o Package Control no Sublime Text 3"
date:   2018-03-10 20:05:40 +0300
img:
description: Uma ferramenta produtiva e funcionando perfeitamente é essencial para trabalhar com desenvolvimento, e até mesmo para estudar
categories: IDE e Editores
published: true
---

<p>Uma ferramenta produtiva e funcionando perfeitamente é essencial para trabalhar com desenvolvimento, e até mesmo para estudar</p>

<p>Este post visa mostrar como instalar o Package Control no Sublime Text 3</p>

<h1>O que é o Package Control?</h1>

<p>Package Control é um gerenciador de pacotes do sublime, e uma vez que você tenha ele instalado, poderá instalar ou remover facilmente quaisquer plugins ou temas do editor Sublime.</p>

<h1>Passos:</h1>

<h2>1 - Instalando</h2>

<p>Visite <a href="https://packagecontrol.io/installation">https://packagecontrol.io/installation</a> para ter acesso às instruções para instalação</p>

<p>Ao acessar o site, você verá este código:</p>

<p>
  <img src="{{ "/assets/img/package-control-install.png" | prepend: site.baseurl }}" alt="Package Control install" class="center-img">
</p>

<p>Copie o código todo que aparece abaixo de "Sublime Text 3". (Caso seu editor seja o Sublime Text 2, mude a aba e copie o outro código exibido).</p>

<p>Em seguida, abra o seu Sublime Text 3, acesse: View -> Show Console e cole o código onde o cursor aparece. Aperte Enter</p>

<p>
  <img src="{{ "/assets/img/show-console.png" | prepend: site.baseurl }}" alt="Console do Sublime Text 3" class="center-img">
</p>

<h2>2 - Acessando o Command Pallete</h2>

<p>Feito isto, reinicie seu Sublime, e acesse o Command Pallete (Interface do sublime onde você pode ativar ou executar ações através de uma busca pelos comandos) através do comando Ctrl + Shift + P (no mac, CMD + Shift + P)</p>

<p>Digite <strong>install package</strong>, e você verá que o comando que um dos comandos que aparece na busca será o <strong>Package Control: Install Package</strong>. Aperte Enter com a opção selecionada (ou selecione com o mouse)</p>

<p>
  <img src="{{ "/assets/img/command-pallete.png" | prepend: site.baseurl }}" alt="Command Pallete" class="center-img">
</p>

<p>Em seguida, o Package Control irá buscar os plugins disponíveis através da internet, o que pode levar alguns segundos, e logo em seguida uma lista com os plugins irá aparecer. Digite o nome do plugin que quer instalar e seja feliz :D</p>

<p>
  <img src="{{ "/assets/img/plugins-list.png" | prepend: site.baseurl }}" alt="Lista de Plugins" class="center-img">
</p>
