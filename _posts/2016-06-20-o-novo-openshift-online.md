---
layout: post
title: "O novo OpenShift Online"
date: 2016-06-20 10:35:00 -0300
comments: true
---
O time do OpenShift lanço o programa Developer Preview do novo OpenShift Online. Ele é baseado no OpenShift v3, que possui as seguintes funcionalidades:

* Baseado no modelo the containerização com Docker
* Utiliza o Kubernetes para orquestração de containers
* Arquitetura baseada microservices, tornando a administração da aplicação mais fácil.
* Por ser baseado em container, boa parte das imagens Docker disponíveis no [Docker Hub][docker-hub] podem ser usadas para compor sua aplicação.

O serviço ainda não previsão para se tornar GA, porém acredito que seja em breve. O time de operações está trabalhando para adicionar cada vez mais funcionalidades para o serviço, mas um feedback é sempre bem-vindo.

{% include image.html
            img="https://www.openshift.com/images/marketecture.svg"
            title="Arquitetura do Openshift v3"
            caption="Arquitetura do Openshift v3" %}

O que mais mudou?
=================

Além da arquitetura do OpenShift ter sido reescrita do zero e o time da engenharia ter adotado a linguagem Go (OpenShift v2 era desenvolvido em Ruby), a ferramenta de linha de comando mudou. Para baixar, você pode acessar a [página de Downloads][download-page] e baixar a última versão. 

**IMPORTANTE:** Essa página irá mostrar todas as versões do cliente, inclusives as versõres alpha e beta.

Como consigo acesso?
====================
 
 Essa nova versão utiliza o serviço do gitHub para autenticação e portanto irá solicitar sua permissão para acessar suas informações do GitHub. Para se registrar, entre no site do [OpenShift Online][openshift-online] e aceite as permissões solicitadas. Vale lembrar que esse é ainda o programa "Developer Preview", ou seja, ainda é um serviço muito limitado e portanto pode sofrer alterações ao longo do caminho. Vale também reforçar que o seu feedback é muito importante para melhorar o serviço.  
 
 [docker-hub]: https://hub.docker.com/
 [download-page]: https://github.com/openshift/origin/releases/
 [openshift-online]: https://www.openshift.com/devpreview/
