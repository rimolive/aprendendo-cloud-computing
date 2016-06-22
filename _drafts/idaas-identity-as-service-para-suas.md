---
layout: post
title: "IDaaS (Identity-as-a-Service) para suas aplicações na nuvem"
date: 2016-06-21 22:00:00 -03:00
author: Ricardo Martinelli Oliveira
comments: true
---
No último [JUDCon][judcon-page] (JBoss Users and Developers Conference) Brasil 2014 eu fiz uma
apresentação bem bacana sobre IDaaS (Identity-as-a-Service) e sobre uma ferramenta chamada keycloak.
Para quem quiser ver minha apresentação, eu publiquei em minha conta do [slideshare][slideshare-deck]
o deck de slides.

A importância da Segurança e o IDaaS
====================================

<p>Segurança é, dentre outras preocupações ao implementar soluções de Cloud Computing, a que as pessoas falam
bastante. Isso se deve ao fato de que Cloud torna-se uma solução muito viável para provisionamento de
Serviços muito rápido e confiável, porém há diversas considerações a respeito. Atualmente os provedores de
Cloud possuem diversas certificações de Segurança para dar toda a confiaça a seus clientes e mostrar que
Segurança é coisa séria quando os provedores de Cloud oferecem seus serviços. Em uma solução de PaaS
(Platform-as-a-Service), obviamente ter certificações de segurança do provedor não significa nada uma vez
que as aplicações serão desenvolvidas pelo próprio cliente e por isso a segurança da aplicação depende do
desenvolvedor ou do time de DevOps (Developer Operations, expliquei isso em um post anterior) tratar desse
requisito em suas aplicações.</p>
<p>Por conta disso, surge um novo paradigma de aaS (as-a-Service) no mundo de Cloud Computing: IDaaS. Como o
próprio nome indica, a intenção desse novo modelo de serviço é prover uma solução de Segurança completa
para aplicações hospedadas em um ambiente de Cloud e assim trazer funcionalidades como SSO (Single-Sign-On),
Social Login (utilizando informações do usuário através das contas das redes sociais), TOTP (Two-phase
Authentication, a solução do Google baseada em tokens) ou até mesmo SAML e outros.</p>
<p>Particularmente, conheci algumas ferramentas para tentar criar um cartucho OpenShift para isso mas sem sucesso,
e até mesmo procurei por soluções gratuitas de IDaaS para utilizar no OpenShift. Um ano e meio depois, encontrei
finalmente uma solução completa e de Código Aberto para resolver esse problema
e já com deployment fácil no Openshift. Nesse artigo, quero apresentar o projeto keycloak.</p>

Keycloak
========
O projeto keycloak foi criado por uma das mais brilhantes mentes da JBoss - Bill Burke - como uma solução
IDaaS para deployment em instâncias locais e até mesmo para Cloud. A principal intenção foi criar um
serviço de segurança para autenticação de serviços REST, porém com o passar do tempo o projeto foi crescendo
e virou um projeto muito importante para a comunidade JBoss.
Para resumir, o keycloak se trata de uma aplicação escrita em Java que, ao fazer o deployment em um servidor
Java EE, fornece uma interface de gerenciamento de contextos de Segurança (ou realms) e com isso oferecendo
diversas funcionalidades, tais como:

* SSO e Single Log Out para aplicações web
* Social Broker. Permite utilizar o login do Google, Facebook, Yahoo e Twitter sem código adicional
* Integração opcional com LDAP/Active Directory
* Registro de usuários opcional
* Suporte a TOTP support (via Google Authenticator). Futuramente com suporte a Client cert
* Gerenciamento de sessóes de ambas perspectivas de administrador e usuário
* Temas customizáveis para páginas do usuário: login, permissão, gerenciamento da conta, emails, e o console administrativo
* Autenticação OAuth Bearer token para serviços REST
* Admin REST
* Suporte a CORS
* Entre outros...

O keycloak atualmente (ou melhor, no momento em que escrevo esse post) se encontra na versão 1.0.2.Final e você pode
encontrar maiores informações através do <a href="http://keycloak.jboss.org/">site do projeto</a>.

Fazendo o deployment no OpenShift
=================================



[judcon-page]: http://jboss.org/events/JUDCon/2014/brazil
[slideshare-deck]: http://www.slideshare.net/rimolive/idaas-ssoopenshift