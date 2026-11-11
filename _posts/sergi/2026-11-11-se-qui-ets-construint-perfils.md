---
title: "Sé qui ets: construint perfils"
author: "Sergi López"
date: 2026-11-11 11:40:00 +0100
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "Com funciona el model de negoci de la publicitat basada en dades de localització i comportament?"
---

Oferir a la venda un producte revolucionari no és prou per assegurar un nombre elevat de vendes. La realitat és completament distinta: un bon producte no es ven sol: ha d’arribar a la persona adequada en el moment adequat. D’això se n’encarrega la publicitat, però per què les teves dades personals serien de tanta utilitat? I com les empreses aconsegueixen fer realitat la frase “allò barat, acaba sortint car”?

## El matís d’allò gratuït.

Abans d’introduir com es procedeix en publicitat digital, cal pensar per què és rellevant i quina és la trampa davant de qualsevol descàrrega o accés sense cost. Com és obvi, però sovint menyspreat, qualsevol aplicació o web que fem servir en el dia comporta un elevat cost de manteniment de servidors, equips i sous. El culpable principal de poder mantenir-los: la publicitat. Els elevats ingressos de la publicitat són clars: el darrer any Meta i Google van obtenir-ne pràcticament 200 i 300 milers de milions de dòlars americans, respectivament, i la tendència és clarament ascendent, en gran part recolzada per la potència de la IA en el tractament de dades:

<figure class="duo">
  <div class="duo-imgs">
    <img src="{{ '/assets/img/sergi/ingressos-meta.jpg' | relative_url }}" alt="Gràfic dels ingressos publicitaris de Meta, 2017-2025" loading="lazy">
    <img src="{{ '/assets/img/sergi/ingressos-google.jpg' | relative_url }}" alt="Gràfic dels ingressos publicitaris de Google en milers de milions de dòlars" loading="lazy">
  </div>
  <figcaption>
    Source: <a href="https://www.statista.com/statistics/266249/advertising-revenue-of-google/?srsltid=AYCX9vLczEDqI8EWkxNWq0de7TiYNIyUTcZ-GspTfrYb-uKIzqzyWFL9">https://www.statista.com/statistics/266249/advertising-revenue-of-google/?srsltid=AYCX9vLczEDqI8EWkxNWq0de7TiYNIyUTcZ-GspTfrYb-uKIzqzyWFL9</a><br>
    Source: <a href="https://resourcera.com/data/social/facebook-revenue/">https://resourcera.com/data/social/facebook-revenue/</a>
  </figcaption>
</figure>

La lògica darrere del seu funcionament és senzilla: la retribució d’un anunci és proporcional al seu ajust a l’usuari: quines pàgines visita freqüentment, quant temps hi dedica, què consumeix preferentment… A diferència d’un cartell al carrer, que té un enfocament genèric, la publicitat digital arriba en un temps i a un dispositiu concrets, però el preu a pagar és la recollida d’informació.

## El que viatja amb tu.

El procés de recopilació d’informació personal consta de múltiples capes interconnectades:

- **Recollida interna de la plataforma.** Cada aplicació o web té control absolut sobre les teves cerques, què es compra, quant temps hi inverteixes, etc. Sovint es coneixen com a dades pròpies i són directament acceptades sota la política de privacitat de cada plataforma.

- **Identificadors:** la segona capa de profunditat l’ofereixen els identificadors: codis únics que permeten rastrejar un dispositiu concret a la xarxa digital, així com un inici puntual de sessió. Avui dia es poden distingir dos identificadors principals: els MAIDs (Mobile Advertising IDs), que són els identificadors propis de cada sistema operatiu (per exemple, IDFA a Apple); i els Universal IDs (IDs Universals), que tenen un enfocament en la web i que són creats per empreses tecnològiques que empren el correu electrònic de l’usuari per rastrejar l’accés (l’exemple prototípic és UID2). Aquests darrers han anat substituint les cookies de tercers a mesura que se’n restringia l’ús i, en l’actualitat, els identificadors també es troben regulats sota polítiques estrictes i l’acceptació de l’usuari.

- **SDK:** una tercera capa menys visible la constitueix l’anomenat SDK (Software Development Kit). Es tracta de mòduls de software incorporats a l’aplicació, que poden alhora imposar un determinat anunci i incorporar dades específiques capaces d’ignorar les polítiques de privacitat, com ara identificadors de dispositiu o localització precisa. Aquesta informació és després compartida amb tercers de manera fraudulenta i inevitable.

  L’informe *Out of Control*, publicat pel Consell de Consumidors de Noruega el gener del 2020, va documentar certs usos fraudulents analitzant el trànsit de dades de deu aplicacions populars. D’entre les troballes hi havia una aplicació de maquillatge que enviava les coordenades GPS exactes dels seus usuaris, i aplicacions de seguiment del cicle menstrual que compartien dades íntimes amb Facebook i Google, entre d’altres. Segons una nota de premsa, Facebook rebia dades de nou de les aplicacions analitzades, i el servei publicitari de Google en rebia de vuit. El que ho fa pertorbador és el fet que la majoria d’aquestes aplicacions oferia una solució per limitar aquest compartiment de dades amb tercers.

- Finalment, cal destacar l’ús freqüent de **fingerprinting**, que pretén complementar els mètodes anteriors aprofitant el fet que l’empremta digital és única i inesborrable, fet que permet, igual que SDK, ignorar l’acceptació de permisos.

## Desxifrant perfils.

Un cop recollides les dades, però, el problema fonamental a què s’enfronta una empresa és la síntesi d’aquestes: com identificar si dos usuaris d’aplicacions diferents són o no la mateixa persona?

En termes tècnics, s’anomena **identity resolution** (resolució d’identitat) al procés de recombinació de dades fragmentades per crear un perfil precís d’una determinada persona física, amb l’objectiu de poder fer inferència sobre ella. En destaquen dos mètodes ben diferenciats:

- **Emparellament determinista (deterministic matching):** permet connectar el perfil dels usuaris mitjançant dades exactes com ara l’obtinguda a partir d’identificadors. Són dades deterministes l’adreça electrònica, el número de telèfon… Ofereix informació molt acurada d’aquells usuaris que han decidit fer-la accessible, però té l’inconvenient que no aporta informació sobre aquells internautes reticents a compartir les seves dades.

- **Emparellament probabilista (probabilistic matching):** empra models estadístics per inferir les connexions entre perfils, basant-se en senyals i prediccions de comportament, fent servir la informació recopilada, usualment amb SDK o fingerprinting.

La pràctica habitual és aplicar el que es coneix com **cross-device identity resolution**, que combina els dos mètodes anteriors. La informació anterior és recollida en grafs d’identitat, una estructura de dades que permet emmagatzemar i trobar correlacions entre els usuaris i la seva activitat, i així predir els seus interessos, tot mantenint una xarxa activa i que s’actualitza cada poc temps. Alhora, aquestes estructures permeten fer la distinció entre usuaris coneguts i anònims, per així adaptar-ne l’enfocament. Finalment, part d’aquesta informació és redirigida als data brokers, que satisfan una doble funció, permetent enriquir-la amb més dades externes i donar-li un ús publicitari.

Així, allò que aparenta ser una aplicació gratuïta acaba sent una cadena: la publicitat paga el servei, el servei necessita dades, i les dades, un cop recombinades, donen lloc a un perfil molt complet que permet anticipar què t’interessarà o què faràs. Aquí és on rau el valor: en la capacitat de predir i conèixer algú més que la pròpia persona.

Amb el perfil construït, hi manca un últim pas: algú l’ha de comprar. I això passa en l’instant en què obres una aplicació, en una subhasta de la qual no en sabies res. Què hi ha exactament en joc, i qui s’hi enriqueix? Ho veurem al [proper post]({{ '/2026/11/11/els-milisegons-de-la-discordia/' | relative_url }}).

## Recull de fonts i pàgines vàries

- <https://www.openrightsgroup.org/press-releases/news-release-mobile-adtech-out-of-control/>
- <https://techcrunch.com/2020/01/14/dating-and-fertility-apps-among-those-snitching-to-out-of-control-adtech-report-finds/>
- <https://oit.utk.edu/security/learning-library/article-archive/what-is-a-data-broker/>
- <https://usercentrics.com/guides/data-privacy/data-privacy-examples/>
- <https://www.kaspersky.com/blog/disable-mobile-app-ad-tracking/53096/>
- <https://nhimg.org/glossary/advertising-sdk/>
- <https://www.statista.com/statistics/266249/advertising-revenue-of-google/?srsltid=AYCX9vLczEDqI8EWkxNWq0de7TiYNIyUTcZ-GspTfrYb-uKIzqzyWFL9>
- <https://freestar.com/what-is-an-sdk-and-why-they-matter-in-ad-tech/>
- <https://www.braze.com/resources/articles/identity-resolution>
- <https://iabeurope.eu/wp-content/uploads/2022/07/What-Are-Advertising-Identifiers-July-2022.pdf>
