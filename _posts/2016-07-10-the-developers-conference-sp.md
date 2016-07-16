---
layout: post
title: "The Developers Conference SP"
date: 2016-07-10 14:00:00 -03:00
author: Ricardo Martinelli Oliveira
comments: true
---

Entre os dias 5 e 9 de Julho ocorreu o [The Developers conference (TDC) 2016][tdc-site] em São Paulo. Particularmente]
é um dos melhores eventos de TI no Brasil e por isso faço questão de participar em todas as edições. Pra quem não
conhece, o TDC ocorre 3 vezes ao ano e em 3 cidades: Florianópolis, São Paulo e Porto Alegre.
O evento conta com diversas trilhas distribuídas durante a semana e abrange desde linguagens de programação, passando
por trilhas de arquitetura até por trilhas que falam de DevOps, Microservices, Educação e outros. É o evento de TI mais
completo e com uma diversidade enorme de tecnologias e por isso vale muito a pena conhecer.
Eu palestrei em duas trilhas - Education e Java -  e dei uma palhinha na trilha de .NET junto do mestre [Edson Yanaga][yanaga-perfil]
e também fiquei durante todo o evento ajudando o time do Red Hat Developers no estande.   

Red Hat Developers
------------------
A Red Hat (empresa onde trabalho) patrocinou o evento e trouxe ao público o seu programa [Red Hat Developers][redhat-dev]. 
O programa consiste em oferecer materiais para desenvolvedores utilizarem todas as ferramentas que a Red Hat disponibiliza 
a seus clientes que pagam por uma subscrição anual para uso porém aos desenvolvedores esse não tem custo.
No site você pode encontrar:

* Todas as ofertas de SO, Middleware e Cloud para uso sem custo para desenvolvimento
* Artigos técnicos de como desenvolver utilizando essas tecnologias
* Videos demonstrativos
* Livros em parceria com a O'Reilly sobre novas tecnologias
* Fóruns e um StackOverflow dedicado como um canal direto aos desenvolvedores das ferramentas


{% include image-local.html
        img="images/tdc2016-sp/equipe-redhat-developers.jpg"
        title="Equipe do Red Hat Developers"
        caption="Equipe do Red Hat Developers" %}

Carreira Open Source
--------------------
Uma das palestras que apresentei foi na trilha Education e trata de como é possível construir uma carreira sendo adepto a
tecnologias Open Source. Eu devo confessar que sou fã de Open Source desde que comecei a trabalhar na área de TI, e por
isso acredito que para criar um sociedade melhor devemos sempre buscar a filosofia que gira em torno do Open Source. O
que mais me atrai nessa filosofia é o que resume bem ela: colaboração. À medida que contribuímos com código Open Source 
nos sentimos mais incluídos na mudança que faz com que a sociedade evolua e podemos criar um mundo melhor para todos.
Porém, muitos ainda não se permitem abraçar a causa pois crêem que o mercado de trabalho ainda não está preparado. Por 
isso tive a idéia de apresentar algo sobre dados de como empresas (e também universidades) não só utilizam Open Source como
também já contribuem para eles, e com isso as empresas procuram por profissionais que já estão envolvidos com Open Source. 

{% include image-local.html
        img="images/tdc2016-sp/carreira-open-source.jpg"
        title="Minha palestra sobre o Thermostat"
        caption="Minha palestra sobre o Thermostat" %}


Thermostat: Uma ferramenta de monitoramento para JVM
----------------------------------------------------
Na trilha de Java eu palestrei sobre o [Thermostat][thermostat-site], uma ferramenta de monitoramento de JVMs em múltiplos
servidores. A palestra foi um tanto curta(eu só tinha 25 minutos) e por isso tudo que fiz foi uma demonstração utilizando
algumas VMs rodando no meu laptop e monitorando através da interface gráfica e do shell. O script está disponível no meu
[GitHub][thermostat-repo] caso alguém queira replicar e conhecer melhor. Estou também melhorando os scripts para fazer
isso ficar mais fácil de rodar, mas infelizmente terá que ter uma máquina boa.

{% include image-local.html
        img="images/tdc2016-sp/thermostat.jpg"
        title="Minha palestra sobre o Thermostat"
        caption="Minha palestra sobre o Thermostat" %}

Sobre o evento
--------------
Vou ser bem honesto: o TDC é o meu evento favorito. Foi onde eu consegui meu espaço dentro do mercado de TI e onde consegui
fazer o networking necessário para chegar onde estou atualmente. Além da gratidão pelo evento eu vejo que é o único que
traz toda a diversidade para assim poder conhecer não somente sobre as novidades da sua linguagem de programação favorita
como também conhecer outrar linguagens e também se atualizar em conceitos mais atuais, como DevOps, Microservices e IoT.
O Vinicius com suas parafernálias tecnologicas é um show a parte. =D

Bom, por ora é isso. Até o próximo post!


[tdc-site]: http://www.thedevelopersconference.com.br/
[yanaga-perfil]: https://www.linkedin.com/in/yanaga
[redhat-dev]: http://developers.redhat.com
[thermostat-site]: http://icedtea.classpath.org/thermostat
[slideshare-perfil]: http://www.slideshare.net/rimolive
[thermostat-repo]: https://github.com/rimolive/vagrant-machines/tree/master/thermostat-multi-machine-demo