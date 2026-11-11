---
title: "Els mil·lisegons de la discòrdia"
author: "Sergi"
date: 2026-11-11 11:50:00 +0100
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "Com funciona el model de negoci de la publicitat basada en dades de localització i comportament?"
---

Diuen que el temps és or. Doncs bé, res més lluny de la realitat: l’or no és el temps, sinó tu. Una simple acció com obrir una aplicació gratuïta, comporta el viatge del teu perfil per mig món: desenes d’empreses han pujat per tu en una subhasta que dura **mil·lisegons**. Tu no hi has participat, ni t’has assabentat que se celebrava, però hi has posat la mercaderia. Però què ha passat en aquests ínfims instants de temps?

## 1. La publicitat programàtica: venent audiències.

La **publicitat programàtica** és el model més emprat de compra-venda d’espais publicitaris. Consisteix en l’automatització de la compra de mitjans i la creació d’anuncis digitals que siguin rellevants per a un determinat públic. L’any 2023, segons reporta Grand View Research, es van destinar 678 milers de milions de dòlars americans a nivell global en el mercat de la publicitat programàtica, una xifra amb un creixement mitjà per any que excedeix el 22%.

## 2. El model de la subhasta.

La publicitat programàtica segueix l’esquema econòmic de la llei d’oferta i demanda. L’oferta la conformen les diferents pàgines web, aplicacions mòbils i mitjans de comunicació, que disposen d’espai publicitari i es disposen a vendre’l. Quant a la demanda, hi ha involucrades múltiples empreses, negocis i marques que pretenen comprar aquests espais.

L’oferta empra una **SSP (Supply-Side Platform)** que els permet anunciar quins espais tenen lliures i fixar-ne un preu orientatiu. Com a intermediari, la SSP es connecta a l’**Ad Exchange**, que analitza els espais lliures i informació recopilada sobre els accessos a aquests i genera una oportunitat per als anunciants.

En aquest punt, la **DSP (Demand Side Platform)** inicia la puja que determina el preu de compra de la demanda. A més, la DSP compta amb algoritmes encarregats de filtrar les diferents oportunitats dels anunciants segons condicions. Alguns exemples rellevants de DSP són The Trade Desk i Google DV 360.

Hem destacat a posts anteriors la importància de l’ús de les dades en aquest sistema de negoci. Tota aquesta informació sobre els usuaris es troba repartida a la **Data Management Platform (DMP)**, a **grafs d’identitat** i alhora en control dels **Data Brokers**, i és emprada per ambdues parts, oferta i demanda. Aquest coneixement els permet crear audiències específiques (que alhora interessaran a un sector determinat de la demanda).

El final i l’inici d’aquest negoci el conformen els **Ad Servers**, que són el mitjà de llançament dels anuncis i que és customitzable per la demanda i els permet accedir al temps de visualització mitjà, nombre de clics, etc. En total, el procés transcorre en **menys de 100 ms**.

{% include figura.html src="/assets/img/sergi/esquema-subhasta.jpg" peu="Esquema de la suhasta. Font pròpia." alt="Esquema del procés de subhasta: usuari, Ad Server de l'editor, SSP, Ad Exchange, DSP i Ad Server de l'anunciant, amb DMP, grafs d'identitat i data brokers, en menys de 100 ms" %}

## 3. Diners: la base del negoci.

Analitzem ara des del punt de vista econòmic les diverses maneres en què es desenvolupen les puges dels anuncis que veiem. Distingim dos tipus de subhastes: les de primer i segon preu. En les de **primer preu**, el guanyador paga exactament la seva aposta, mentre que en les de **segon preu**, el guanyador paga poc més que la segona aposta més alta.

Ho exemplifiquem a l’exemple següent:

{% include figura.html src="/assets/img/sergi/subhasta-primer-preu.jpg" peu="Subhasta de primer preu." alt="Tres licitadors ofereixen 4,00, 4,50 i 4,20 dòlars; guanya B i paga 4,50 dòlars" %}

{% include figura.html src="/assets/img/sergi/subhasta-segon-preu.jpg" peu="Subhasta de segon preu." alt="Tres licitadors ofereixen 4,00, 4,50 i 4,20 dòlars; guanya B i paga 4,21 dòlars" %}

Aquests dos models comporten maneres de procedir diferents per part de la demanda, per exemple, a una subhasta de segon preu és viable sobrepagar el preu real o almenys apropar-se, i, alhora, comporta certa falta de transparència: un intermediari pot manipular la puja i inflar el segon preu més alt. Aquests són alguns motius pel qual a partir de 2019 moltes SSP independents i d’altres d’àmplia rellevància com Google AdManager van transicionar a les subhastes de primer preu. Davant aquest canvi, la demanda va haver d’adaptar les seves estratègies, donant pas al **bid shading**; algorismes que permeten optimitzar la compra per intentar pagar exactament allò necessari per guanyar. Alhora, els venedors juguen les seves cartes mitjançant la imposició de **price floors** més o menys estrictes, els quals fixen un preu mínim o orientatiu a pagar.

## 4. El repartiment del pagament.

La pregunta natural que tot lector es farà a continuació és on van a parar els diners que diposita l’empresa anunciant. Bé és cert que la transparència del model és sovint qüestionable, fet que ha portat a nombrosos estudis al Regne Unit (com ara PwC o ISBA), Estats Units i altres sobre el flux d’aquest pagament. Un dels més recents, l’estudi ANA dels Estats Units va analitzar 23 mercats diferents, corresponent a 123 milions de dòlars pagats. Aquest va determinar que només 36 % dels diners que entren a una DSP arriben a l’ofertant, mentre que un 29 % es destina a intermediaris (DSP, SSP…) i la resta, a mitjans de baixa qualitat. No obstant això, aquestes dades són rarament publicades, mantenint la realitat de les dades en l’anonimat i convidant els usuaris a pensar que part dels diners que s’inverteixen tenen destí desconegut (l’anomenat unknown delta, datat en un 15 % al 2020, segons l’estudi ISBA) i sovint esbiaixat segons plataformes.

## 5. La regulació: un actor protagonitzant més d’un paper.

Per acabar, tot i que la publicitat programàtica és avui dia força opaca, diverses actuacions han tingut lloc per reduir l’aglutinació de poder. El cas recent més rellevant data del setembre de 2025, després que la UE multés Google amb 2.95 milers de milions d’euros a causa del seu abús dominant. En concret, segons va decretar un tribunal dels Estats Units, Google havia mantingut il·legalment monopolis en els servidors d’anuncis dels editors i en les borses d’anuncis, tot lligant AdX, la seva borsa, al seu servidor d’anuncis. El setembre del 2026 es va decidir, però, no obligar-la a vendre AdX, sinó aplicar mesures de conducta durant 6 anys. Aquest, doncs, és un exemple clar de la necessitat de col·locar sota un marc legal més estricte qui i de quina manera té control sobre les DSP, les SSP i els Ad Exchange i com, avui dia, els ingressos publicitaris d’empreses pioneres com Meta o Google són desmesurats.

## Recull de fonts

- <https://www.avenga.com/magazine/first-price-second-price-auction/>
- <https://www.adissey.com/flow/conexiones/publicidad-programatica-como-funciona>
- <https://www.adsmurai.com/es/articulos/que-es-la-publicidad-programatica-y-como-funciona>
- <https://advertising.amazon.com/es-es/blog/programmatic-advertising>
- <https://newormedia.com/blog/what-is-bid-shading/>
- <https://www.mi-3.com.au/11-01-2024/omnicom-media-group-claims-its-ad-outperform-ana-programmatic-media-supply-chain>
- <https://www.computing.co.uk/news/2025/google-fined-2-95bn-by-eu-over-ad-tech-antitrust-abuses>
