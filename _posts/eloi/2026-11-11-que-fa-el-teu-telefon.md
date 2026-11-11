---
title: "Què fa el teu telèfon quan no el veus?"
author: "Eloi Estévez"
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "Quines dades genera un mòbil sense que la persona usuària faci res? Qui hi té accés i amb quina base legal?"
date: 2026-11-11 11:10:00 +0100
---

Saps quantes dades genera el teu mòbil ara mateix, mentre llegeixes això? I a qui les està enviant sense que tu ho hagis demanat?

En aquesta sèrie de posts veurem quines dades produeix el teu telèfon de manera automàtica, qui hi té accés, què en fa i amb quina base legal. En aquest primer post ens centrem en el primer pas i parlarem de quins tipus de dades genera.

## 1. Què fa el telèfon

El sistema operatiu envia dades a Apple/Google. Un estudi de 2021 va mesurar un iPhone i un Pixel en repòs, amb la configuració mínima, i va veure que contactaven amb Apple o Google cada 4,5 minuts de mitjana, enviant identificadors com l'IMEI o els números de sèrie, fins i tot amb l'enviament d'analítiques desactivat. Un estudi publicat el 2023 va trobar que els Android de Samsung, Xiaomi, Huawei i Realme envien molt volum de dades al fabricant i a tercers, i que tots recullen la llista d'apps instal·lades. Les mesures són de fa uns anys i amb versions antigues dels sistemes, però mostren que una part d'aquest tràfic no depèn del que tu facis.

## 2. On ets

Per tenir cobertura, el mòbil ha d'avisar la xarxa de la seva posició, així que la teva operadora sap, a grans trets, a quina antena et connectes. A més, les apps poden calcular on ets amb el GPS, el Wi-Fi o el Bluetooth. Alguns iPhone recents (iPhone Air, 16e i 17e) tenen una funció (Limit Precise Location) que redueix la precisió de la ubicació que veuen les operadores: poden saber només el barri i no l'adreça exacta. Cal activar-la manualment, només funciona amb operadores compatibles i no afecta la ubicació que comparteixes amb les apps, que continuen podent recollir la teva posició per altres vies.

Una bona notícia: des d'Android 10 el telèfon fa servir per defecte una adreça Wi-Fi aleatòria en connectar-se a una xarxa, i a l'iPhone l'adreça privada ve activada des d'iOS 14. Això dificulta que et segueixin per les xarxes Wi-Fi del carrer o d'un centre comercial.

## 3. Com et mous

El telèfon porta sensors que detecten moviment i orientació, com els que fan girar la pantalla o compten passos. Una recerca recent explica que cada sensor té petites imperfeccions de fabricació que el fan únic, fins al punt que uns quants minuts de dades poden bastar per reconèixer un telèfon amb més del 90 % d’encert. És a dir, només amb les dades dels sensors, un actor malvolent podria identificar i rastrejar el teu dispositiu a través de diferents plataformes sense demanar-te permís. A més, les defenses actuals de privadesa no poden aturar aquests atacs sense inutilitzar les dades dels sensors per a aplicacions legítimes. Tot i això, aquest tipus d’atacs tenen limitacions, ja que en escenaris més realistes la precisió baixa significativament si la població coneguda és petita.

## 4. Qui ets

Cada telèfon porta números que l'identifiquen, com una matrícula. Entre ells hi ha l'identificador publicitari, que serveix perquè els anunciants reconeguin el teu aparell entre apps. Hi tens un control parcial:

- A l'iPhone, les apps han de demanar permís abans d'usar-lo i, si el rebutges, el sistema els dona una cadena de zeros.
- A Android, el pots restablir o eliminar des dels ajustos d'anuncis. Però, això no és una garantia, l'AEPD ja va advertir el 2019 que desactivar la personalització d'anuncis no impedeix que algunes apps enviïn l'identificador, i recomana restablir-lo sovint.

A més de l’identificador publicitari, hi ha moltes dades que recullen les aplicacions, sobretot a través de llibreries de programari (Software development kits o SDKs) de ús molt habitual. Una recerca de 2025 va concloure que les llibreries publicitàries només expliquen poc més del 30 % de les tècniques per fer una empremta del dispositiu, i que un 24 % ve de llibreries amb una finalitat poc clara. A més un altre estudi, també del 2025 va concloure que l’us de moltes d’aquestes llibreries resulta en recol·lecció de dades potencialment en violació de la legislació actual. Pel fet que els desenvolupadors tenen una influència mínima sobre les dades que transmeten aquestes llibreries, aquests han de decidir entre usar la llibreria o evitar-la completament.

Si tens Android, pots veure quins rastrejadors porta cada app amb l'eina Exodus Privacy, d'una organització francesa sense ànim de lucre. Només detecta rastrejadors ja identificats i no diu quines dades envien, però és un bon punt de partida.

Vols saber més sobre quins rastrejadors porten les apps que usem diàriament? Llegeix el nostre post: Auditoria de permisos i traçadors aplicacions d'ús habitual. <!-- enllaç pendent: entrada de l'encàrrec propi -->

## En resum

El teu telèfon no és mai del tot en repòs: sempre està informant de qui és, on és i què fa. La part important no és només què genera, sinó qui ho rep. Vols saber qui rep tota aquesta informació i què en pot fer? Llegeix la part 2: [De la teva mètrica al mercat: qui té accés a les dades del teu mòbil i què en fa?]({% post_url eloi/2026-11-11-de-la-metrica-al-mercat %})

## Per saber-ne més

- Leith, D. J. (2021). [Mobile Handset Privacy: Measuring the Data iOS and Android Send to Apple and Google](https://www.scss.tcd.ie/doug.leith/apple_google.pdf).
- Liu, H., Patras, P., Leith, D. J. (PLOS ONE, 2023). [On the data privacy practices of Android OEMs](https://www.pure.ed.ac.uk/ws/portalfiles/portal/322300736/On_the_Data_LIU_DOA_28122022_VOR_CC_BY.pdf).
- Apple. [Limit precise location from cellular networks](https://support.apple.com/126101).
- Documentació d'[Android](https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior) i d'[Apple](https://support.apple.com/en-tm/102076) sobre adreces Wi-Fi privades.
- Sulbaran Fandino, C., Kouam, A. J., Rieck, K. (MSWiM 2025). [Tiny Sensors, Big Threats: Assessing Motion Sensor-based Fingerprinting in Mobile Systems](https://lacuna.tiptreesystems.com/work/tiny-sensors-big-threats-assessing-motion-sensor-based-fingerprinting-in-mobile/wrk_558bc1d795ab9331792f3eb5148ead87) (resum a Lacuna; [DOI de l'article](https://doi.org/10.1109/mswim67937.2025.11309009)).
- Moburst. [IDFA in 2026](https://www.moburst.com/blog/idfa-att-update/).
- AEPD (2019). [La AEPD publica dos análisis para fomentar la privacidad en dispositivos Android](https://www.aepd.es/prensa-y-comunicacion/notas-de-prensa/la-aepd-publica-dos-analisis-para-fomentar-la-privacidad-en).
- Exodus Privacy. [Què és i com funciona](https://exodus-privacy.eu.org/en/page/what/).
- PETS 2025. [The Impact of Default Mobile SDK Usage on Privacy and Data Protection](https://petsymposium.org/popets/2025/popets-2025-0042.pdf).
- ACM CCS 2025. [Fingerprinting SDKs for Mobile Apps and Where to Find Them](https://arxiv.org/html/2506.22639v1).
