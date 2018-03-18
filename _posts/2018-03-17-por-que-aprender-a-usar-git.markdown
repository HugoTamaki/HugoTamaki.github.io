---
layout: post
title:  "Por que aprender a usar o git?"
date:   2018-03-17 20:14:40 +0300
img:
description: O que é e por que aprender a usar o git? Qual a importância de usar um bom sistema de versionamento? Este post irá responder suas dúvidas
categories: Versionamento
published: true
---

<p>O que é e por que aprender a usar o git?</p>

<p>Bem, vamos por partes. Vou começar com algumas perguntas, levando em conta que você leitor ainda não conhece o git</p>

<h2>Como você versiona seus projetos?</h2>

<p>Bem, você já deve ter passado por alguma situação em que estava trabalhando com algum projeto grande de faculdade ou de algum curso, ou mesmo escrevendo algum TCC ou trabalho em grupo, e provavelmente já precisou guardar <strong>versões</strong> diferentes do projeto, pro caso de precisar voltar no tempo e ter diferentes estágios de desenvolvimento do projeto, certo?</p>

<figure>
  <p>
    <img src="{{ "/assets/img/versionamento-tosco.png" | prepend: site.baseurl }}" alt="Versionamento de arquivos" class="center-img">
  </p>
  <figcaption>
    Provavelmente isso te parece familiar...
  </figcaption>
</figure>

<h2>Como você compartilha seus projetos?</h2>

<p>Na mesma situação acima, provavelmente ao trabalhar em grupo, precisou também <strong>compartilhar</strong> seu projeto com seu colega, e enquanto você faz a parte A, seu colega faz a parte B. Depois que seu colega terminou sua parte, precisou copiar e colar o trecho que ele fez para o seu projeto de forma que o mesmo passasse a ter tanto a parte A quanto a parte B</p>

<p>Agora imagine isto quando se trata de um projeto web, ou algum outro projeto que envolva códigos. Imagine a chance de copiar e colar trechos errados, ou sobrescrever algum trecho do seu colega. Como você resolve este problema?</p>

<h2>Como você mantém um histórico de desenvolvimento do seu projeto?</h2>

<p>Provavelmente, sem uma ferramenta de versionamento, você NÃO mantém um <strong>histórico</strong> de desenvolvimento do seu projeto. Você não lembrará em que dia quais linhas foram adicionadas ou removidas do seu projeto, também não lembrará quem adicionou uma funcionalidade, ou que trechos de código uma pessoa modificou, a não ser que anote tudo a mão em uma espécie de <strong>change log</strong> (um histórico de modificações), que mesmo assim é de forma macro, contendo apenas funcionalidades que foram adicionadas ou removidas, não chegando ao ponto de linhas de código adicionadas ou removidas</p>

<h2>Como o git resolve as três questões de uma vez?</h2>

<p>O git é uma ferramenta de versionamento voltado para o desenvolvedor, e permite que você guarde uma série de <q>retratos</q> das modificações que você faz em um projeto</p>

<p>Esses <q>retratos</q> são chamados de <strong>commits</strong>, e eles podem conter adições, remoções ou modificações de trechos de código</p>

<p>Além das modificações, o commit permite guardar uma mensagem pequena, explicando com poucas palavras o contexto das suas modificações. Exemplo: <q>Adding description to home page</q> me faz entender que esse commit tem modificações referentes a adição de código para dar uma descrição a minha home page</p>

<figure>
  <p>
    <img src="{{ "/assets/img/commit-tree.png" | prepend: site.baseurl }}" alt="árvore de commits" class="center-img">
  </p>
  <figcaption>
    Uma sequencia de commits
  </figcaption>
</figure>

<p>Na imagem acima é possível ver uma representação gráfica de uma árvore de commits feita no git. Cada bolinha representa um conjunto de modificações que foi <q>fotografada</q> em um <strong>commit</strong></p>

<figure>
  <p>
    <img src="{{ "/assets/img/diff.png" | prepend: site.baseurl }}" alt="árvore de commits" class="center-img">
  </p>
  <figcaption>
    A diff em um commit
  </figcaption>
</figure>

<p>A figura acima é uma visualização dos <strong>diffs</strong> de um <strong>commit</strong>. Um <strong>diff</strong> ou <strong>delta</strong> é a variação que ocorreu entre o commit atual e o estado anterior do projeto. Na imagem, a linha <strong>vermelha</strong> é a que foi removida, e a linha <strong>verde</strong> é a que foi adicionada. Como elas ocorrem na mesma linha (linha 47), então na verdade a linha foi modificada. Antes ela continha um texto (a que está em vermelho) e com esse commit passou a ter outro (a que está em verde)</p>

<p>Essas duas funcionalidades resolvem o problema do <strong>histórico</strong> e das <strong>versões</strong>. É possível retornar o seu projeto para um commit passado e deixa-lo como ele estava naquela data, e cada <strong>commit</strong> possui um histórico de quais modificações foram realizadas, aonde elas foram feitas e quem foi o autor</p>

<figure>
  <p>
    <img src="{{ "/assets/img/branches.png" | prepend: site.baseurl }}" alt="branches" class="center-img">
  </p>
  <figcaption>
    Branches no git
  </figcaption>
</figure>

<p>Uma coisa fantástica que o git permite também é o uso de <strong>branches</strong>. Branch é <q>galho</q> ou <q>ramificação</q> em inglês, ou seja, o git permite que modificações em um projeto sejam feitas em ramificações separadas. Você consegue trabalhar em uma <strong>branch</strong> ou ramificação, enquanto seu amigo trabalha em outra <strong>branch</strong>, e quando seu amigo ou você termina as modificações necessárias, uma <strong>branch</strong> pode ser mesclada com a outra, ou seja, sofrer um <strong>merge</strong>. Quando isto acontece, as alterações que seu amigo fez em uma branch, por exemplo, passam a existir na branch que você está trabalhando.</p>

<p>Na figura acima, a linha vermelha é uma <strong>branch</strong>, e a linha verde é outra <strong>branch</strong>. No ponto em que uma se junta com a outra, ocorreram <strong>merges</strong>, e isso resolve o problema de <strong>compartilhar</strong> e trabalhar em conjunto em um projeto</p>

<h2>O git e o github são a mesma coisa?</h2>

<p>Não, o git é a ferramenta de versionamento que roda na sua máquina, já o github é um serviço para criar repositórios remotos.</p>

<p>E o que seria um repositório remoto? Um repositório remoto é como se seu projeto estivesse guardado com um histórico de git, mas na nuvem. Resumindo, o <strong>github</strong> é um serviço que permite guardar o seu projeto e todos os commits dele na nuvem. O git é excelente para projetos open source, já que os repositórios são abertos e qualquer usuário pode acessá-los</p>

<p>Muitas empresas pedem para ver seus projetos no github para poderem ver como você escreve códigos, então é um ótimo portfólio</p>

<p>O <strong>github</strong> também entra na solução de trabalhar em conjunto também, já que é através de um repositório remoto que um desenvolvedor A consegue sincronizar o projeto com o desenvolvedor B. Em outro post explicarei de forma mais específica como acontece essa colaboração entre mais de um desenvolvedor com o <strong>github</strong></p>

<h2>Resumindo...</h2>

<p>Se você está iniciando com desenvolvimento, tire um tempo para ver o que é o <strong>git</strong>, como instalar e como usá-lo em seus projetos. Faça também um perfil seu no <strong>github</strong>. Em outro post entrarei em mais detalhes de funcionamento do git, já que este post foi mais uma descrição por alto do que é o git e de sua importância</p>
