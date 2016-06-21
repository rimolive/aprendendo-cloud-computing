---
layout: post
title: "Testes de carga em aplicações na Nuvem com Blazemeter"
date: 2016-06-21 19:00:00 -03:00
comments: true
---
Uma das maiores preocupações de empresas e startups sobre desenvolvimento de apps hoje em dia é se a sua aplicação
vai conseguir aguentar o número de usuários simultâneos ou se as aplicações irão se comportar da forma adequada quando
em altíssima carga. Isso não é diferente quando estamos falando de desenvolvimento de aplicações na nuvem. Existe um
serviço que resolve esses problemas oferecendo um serviço de testes de carga e stress de altíssimo volume de nome
Blazemeter. Tentarei explicar a idéia deles a seguir.

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-main-console.png"
        title="Console do Blazemeter"
        caption="Console do Blazemeter" %}

O serviço Blazemeter
--------------------
O [Blazemeter][blazemeter-page] é um serviço que oferece um servidor jMeter (mais informações em [http://www.apache.org/jmeter][jmeter-page])
em uma ambiente complexa de modo a criar testes de carga e stress com muitos usuários simultâneos e disponibiliza um
dashboard com os dados do teste. Através do Blazemeter, é possível criar os seguintes testes:

* Testes simples de acesso/disponibilidade com URL Test
* Testes complexos de carga utilizando JMeter
* Testes funcionais utilizando WebDriver (um plugin do JMeter)
* Testes automatizados com Taurus
* Uma combinação dos testes acima

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-create-test.png"
        title="Criando um novo teste no Blazemeter"
        caption="Criando um novo teste no Blazemeter" %}

As vantagens de se utilizar o serviço é que, a medida que os testes vão executando, blazemeter constrói toda a infraestrura 
de testes de acordo com a exigencia do teste (mais usuários simultaneos == mais servidores) e gera em tempo real um relatório
contendo diversas informações, como tempo médio de resposta da aplicação, throughput médio, largura de banda utilizada, etc.

Criando um teste simples de acesso
----------------------------------
Irei mostrar como criar um teste simples de URL usando o blazemeter. Abaixo a figura dos parametros utilizados:

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-create-test.png"
        title="Criando um teste simples de URL"
        caption="Criando um teste simples de URL" %}

Ao salvar os parametros e clicar em play, o blazemeter já pergunta se quer criar o ambiente de testes e informa o que será
feito.

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-start-test.png"
        title="Informação sobre o teste antes de executar"
        caption="Informação sobre o teste antes de executar" %}

Ao clicar em Launch Servers, o Blazemeter tratar de fazer build desse ambiente e dar inicio aos testes.

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-starting-test.png"
        title="Preparando o ambiente de testes"
        caption="Preparando o ambiente de testes" %}

Após a finalização do build do ambiente, o Blazemeter dá início aos testes e já gera o relatório em tempo real.

{% include image.html
        img="{{ site.url }}/images/blazemeter/blazemeter-starting-results.png"
        title="Relatório de testes"
        caption="Relatório de testes" %}

E com isso, é possível analisar as diversas informações que o Blazemeter coleta desse teste. Lembrando que esse foi um teste bem simples oferecido
pelo serviço, mas é possível criar testes mais complexos e que simulam interações do usuário com o sistema utilizando as opções anteriormente descritas.

Mas e se eu quiser fazer um teste simples de carga?
-------------------------------------------------
A Apache oferece uma ferramenta bem simples chamada [Apache Benchmark][ab-page], que permite fazer testes rápidos de carga em URLs. A sintaxe do comando
é bem simples:

```bash
$ ab -n 10000 -c 100 http://rimolive.github.com/aprendendo-cloud-computing
```

Onde:

* **-n**: número total de requisições a serem enviadas para o servidor
* **-c**: Número de usuários simultaneos

Bom, por ora é isso. Até o próximo post.


[blazemeter-page]: http://blazemeter.com/
[jmeter-page]: http://www.apache.org/jmeter
[ab-page]: http://httpd.apache.org/docs/2.2/programs/ab.html