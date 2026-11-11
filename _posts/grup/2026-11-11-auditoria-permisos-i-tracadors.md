---
title: "Auditoria de permisos i traçadors d’aplicacions d'ús habitual"
author: "Tot el grup"
date: 2026-11-11 18:30:00 +0100
bloc: "Encàrrec propi"
---

En aquest post analitzarem quins permisos i traçadors estan presents en una selecció de les aplicacions més usades. Per això hem seleccionat analitzar amb Exodus Privacy les següents 7 aplicacions: WhatsApp, Clash Royale, ChatGPT, Google Maps, Tinder, Mullvad VPN, i Facebook. Exodus Privacy és una organització sense ànim de lucre que analitza la privacitat d’aplicacions Android, enregistrant-ne quins rastrejadors usen (i per tant, quines dades col·leccionen), i quins permisos demanen.

## Resultats principals

En la següent taula podem veure el nombre de traçadors, permisos i permisos perillosos per a les set aplicacions. Exodus Privacy considera perillosos aquells permisos classificats amb l’etiqueta “d’alta privacitat” segons la documentació d’Android.

{% include figura.html src="/assets/img/grup/auditoria-resum.png" alt="Taula resum de l'auditoria amb Exodus Privacy: versió, data de l'informe, nombre de traçadors, de permisos i de permisos perillosos de WhatsApp, Clash Royale, ChatGPT, Maps, Tinder, Mullvad VPN i Facebook" %}

El següent gràfic ens indica que hi ha una manca de correlació entre el nombre de traçadors i de permisos, així com la seva perillositat:

{% include figura.html src="/assets/img/grup/auditoria-permisos-i-tracadors.png" alt="Gràfic de dispersió: nombre de permisos declarats (eix horitzontal) davant del nombre de traçadors (eix vertical); la mida del punt és proporcional als permisos perillosos" %}

Aquesta falta de correlació és deguda a la naturalesa tan diversa de les aplicacions triades: missatgeria instantània, joc de mòbil, IA, aplicació de cites, VPN, etc. Cal, doncs, un anàlisi més exhaustiu de quins traçadors i permisos, atenent a diverses categories, són útils per cada respectiva empresa. Alhora, el fet que Mullvad VPN no demani pràcticament permisos ni tingui cap traçador se sustenta en què es tracta de l’única aplicació de pagament i per tant, no només el seu públic és més selectiu, sinó que part de la recollida de dades és executada a partir de vies externes, com ara el propi pagament online. Exodus, però, no és capaç de recollir aquesta informació.

## Anàlisi dels traçadors

Un rastrejador o traçador és una peça de programari que té com a tasca recopilar informació sobre la persona que utilitza l'aplicació, sobre com l'utilitza o sobre el telèfon intel·ligent que s'utilitza. Un tracker normalment es distribueix per les empreses com un SDK (Software Development Kit). A més, cal destacar que hi ha rastrejadors de "codi obert": el seu codi està disponible i obert a tothom. Si vols saber-ne més sobre els mecanismes d’obtenció de dades, et convidem a llegir el nostre post [Sé qui ets: construint perfils]({{ '/2026/11/11/se-qui-ets-construint-perfils/' | relative_url }}).

A continuació podem veure els traçadors coneguts per a les aplicacions estudiades i la seva classificació per categoria. Cal tenir en compte que la presència d’un traçador no implica necessàriament un ús abusiu de dades, i la taula no indica quines dades s’envien realment ni amb quin consentiment.

{% include figura.html src="/assets/img/grup/auditoria-tracadors-per-app.png" alt="Taula dels traçadors detectats per aplicació, amb la categoria de cada traçador i el percentatge d'apps d'Exodus que el porten" %}

{% include figura.html src="/assets/img/grup/auditoria-tracadors-per-categoria.png" alt="Gràfic de barres del nombre de traçadors per aplicació i categoria: Facebook 8, Tinder 8, Clash Royale 4, ChatGPT 2, Maps 1, Mullvad VPN 0, WhatsApp 0" %}

Tot seguit, analitzem per categories els traçadors del nostre estudi:

### Publicitat

**Facebook Ads, Google AdMob i IAB Open Measurement.** Serveixen per mostrar anuncis, mesurar-ne l’eficàcia i verificar que s’han vist realment, i tots permeten construir perfils a partir de l’identificador publicitari del dispositiu. Tinder els utilitza tots tres perquè combina publicitat i subscripcions, i els fa servir també per captar usuaris nous. Facebook només utilitza el seu propi sistema (Facebook Ads i els traçadors propis de Meta), ja que la publicitat és el seu model de negoci. Les altres apps no hi recorren perquè es financen amb compres dins del joc (Clash Royale), subscripcions (ChatGPT) o l’ecosistema de Google (Maps). Pel que fa a la privacitat, és la categoria més invasiva, perquè facilita el perfilatge entre apps i la cessió de dades a tercers.

### Analítica i atribució

**Google Firebase Analytics, AppsFlyer, Branch i Tinder Analytics.** Mesuren com s’utilitza l’app (pantalles vistes, retenció, compres) i quina campanya ha dut cada instal·lació. Clash Royale, Maps i Tinder els fan servir per optimitzar el producte i saber quines campanyes de captació són rendibles, sobretot Clash Royale i Tinder, que inverteixen molt en aconseguir jugadors i usuaris. ChatGPT i Facebook recorren a sistemes propis. Aquests traçadors envien dades a tercers i poden crear empremtes digitals per reconèixer l’usuari entre dispositius. En el cas de Tinder, les dades són especialment sensibles, perquè poden revelar orientació sexual, preferències i ubicació.

**Segment.** És un intermediari que distribueix una mateixa recollida de dades a molts altres serveis de màrqueting i analítica. ChatGPT l’utilitza per centralitzar dades d’ús, i és un cas notable perquè les converses amb un xatbot poden contenir informació molt personal.

### Informes d’errors

**Sentry i HelpShift.** Detecten fallades i gestionen el suport a l’usuari. Clash Royale, ChatGPT i Tinder utilitzen Sentry perquè són serveis complexos que necessiten corregir errors de pressa, i Clash Royale afegeix HelpShift per atendre una gran base de jugadors. Són els menys intrusius, però els informes poden incloure dades personals per accident si no es filtren bé, cosa més delicada si hi ha usuaris menors.

## Anàlisi dels permisos

Quan una aplicació requereix accés a dades o accions restringides, aquesta ha de demanar permisos al sistema operatiu. Android categoritza els permisos en diferents tipus, inclosos els permisos d'instal·lació, els permisos d'execució i els permisos especials.

Els permisos d’execució (o «perillosos») donen a l’aplicació accés a dades restringides o li permeten fer accions que afecten més el sistema i altres aplicacions. Quan l’app en necessita un, el sistema mostra una sol·licitud perquè l’usuari l’accepti o la rebutgi.

Molts d’aquests permisos donen accés a dades privades i potencialment sensibles, com la ubicació o la informació de contacte. El micròfon i la càmera són especialment delicats, per la qual cosa el sistema ajuda l’app a explicar per què hi vol accedir.

A continuació podem veure quins permisos perillosos utlitza cada aplicació:

{% include figura.html src="/assets/img/grup/auditoria-permisos-perillosos.png" alt="Taula dels tipus de permisos perillosos declarats per WhatsApp, Clash Royale, ChatGPT, Maps, Tinder i Facebook: càmera, localització, contactes, emmagatzematge extern, comptes, Bluetooth, número de telèfon, gravadora d'àudio, SMS, calendari, reconeixement d'activitat i aparèixer sobre altres aplicacions" %}

Recordem que per a que l’aplicació tingui accés a aquests permisos cal que aquest sigui concedit per l’usuari. Tot i això, és interessant recordar a què tenen accés aquestes aplicacions ja que moltes vegades donem aquests permissos sense pensar-hi gaire.

## Conclusions de l’estudi

L’anàlisi anterior ens porta a les conclusions següents:

- Tinder és l’app més carregada, amb set traçadors que combinen publicitat, analítica i atribució amb dades molt íntimes.
- Facebook compta amb menys dades de tercers, atès que ella mateixa és el seu propi sistema de rastreig.
- Maps, tot i emprar-ne pocs traçadors i no demanar massa permisos, pertany a Google i, alhora, disposa d’informació molt detallada de la ubicació de l’usuari.
- ChatGPT i WhatsApp en tenen pocs, però el context de converses privades fa que l’accés a informació privada via Segment (en el cas de ChatGPT) o via l’abundància de permisos a acceptar (per part de WhatsApp) sigui rellevant.
- Clash Royale i MullvadVPN tenen enfocs molt diferents a les aplicacions anteriors. D’una banda, Clash Royale, en ser un joc de mòbil, demana un nombre baix de permisos, ho compensa amb rastrejadors que analitzin i incentivin les compres dins l’aplicació. D’altra, MullvadVPN fa servir el pagament per fer-la servir com a mitjà d’obtenció de dades.

## Fonts

- Android Developers. *Permissions on Android* (visió general). <https://developer.android.com/guide/topics/permissions/overview>
- Exodus Privacy. *Exodus Privacy: analitzador de rastrejadors i permisos d’aplicacions Android*. <https://exodus-privacy.eu.org/en/>
- Exodus Privacy. *Trackers*. <https://reports.exodus-privacy.eu.org/en/info/trackers/>
