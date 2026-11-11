---
title: "De la teva mètrica al mercat: qui té accés a les dades del teu mòbil i què en fa?"
author: "Eloi"
date: 2026-11-11 11:20:00 +0100
---

Al primer post vam veure que el telèfon genera dades sense parar: què fa, on és, com es mou i quin «número» porta. Ara toca la pregunta següent: on van a parar? Què poden saber de tu amb elles? I per a què les fan servir?

Encara no has llegit el primer post? El pots trobar aquí: [Què fa el teu telèfon quan no el veus?]({% post_url 2026-11-11-que-fa-el-teu-telefon %})

## 1. Qui les rep?

Hi ha tres destinataris principals:

- El fabricant i el sistema operatiu (Apple, Google, Samsung…): reben diagnòstics i dades de funcionament.
- L'operadora: sap a quina antena et connectes i, [segons Apple](https://support.apple.com/126101), pot situar-te a partir d'aquestes antenes. A diferència del Wi-Fi, on el telèfon pot fer servir una adreça aleatòria, a la xarxa mòbil et connectes amb la teva SIM, que identifica la teva línia. Cada connexió a una antena deixa un registre amb hora, que [el Tribunal Suprem dels EUA](https://www.eff.org/cases/carpenter-v-united-states) (2018) va descriure com una crònica detallada de la presència física d'una persona.
- Els intermediaris de dades (data brokers): són els qui acaben rebent les dades, i les obtenen a través de les apps que instal·les i de les llibreries de tercers (SDK, de publicitat o estadístiques) que porten dins. Quan dones permís d'ubicació a una app, les llibreries reben el mateix accés, perquè no hi ha permisos separats per a elles, i l'EFF en va trobar quatre, a Android, que comparteixen la ubicació per defecte quan l'app té permís. Les mateixes apps ja envien dades a tercers: [l'AEPD](https://www.aepd.es/prensa-y-comunicacion/notas-de-prensa/la-aepd-publica-dos-analisis-para-fomentar-la-privacidad-en) ho va il·lustrar el 2019, quan el simple fet d'obrir una app feia arribar a Facebook l'identificador publicitari, el nom de l'app, la ubicació, el model de telèfon i l'idioma, tant si l'usuari tenia compte com si no, i encara que hagués desactivat la personalització d'anuncis. Segons la FTC nord-americana, un d'aquests intermediaris i la seva filial deien recollir més de 17.000 milions de senyals al dia d'uns mil milions de telèfons.

## 2. Què poden saber de tu?

Dels destinataris mencionats anteriorment, el més preocupant són els intermediaris de dades, ja que són els que compilen grans quantitats de dades per a vendre-les en paquets. Una única dada pot semblar que no té gaire importància, però el que importa és el conjunt: una experta adverteix que la ubicació és sensible per la recopilació completa que en fa, no per cada punt. Amb aquest conjunt es pot deduir:

- On vius i on treballes. Quan un d’aquests intermediaris va patir una filtració el 2024, es van exposar els llocs on viu i treballa gent de tot arreu.
- Si visites llocs delicats, com hospitals, esglésies, centres d’addiccions o refugis. La FTC els considera «ubicacions sensibles»: centres mèdics, organitzacions religioses, presons o sindicats.
- Informació de salut. Alguns intermediaris connecten la ubicació amb altres dades i en dedueixen problemes de salut, per vendre’ls a empreses de tractaments dubtosos.
- Qui ets. Les dades «anònimes» ho són poc: la FTC va dir que les dades d’un d’aquests intermediaris no estaven anonimitzades i servien per identificar dispositius concrets. A Europa, uns periodistes van identificar centenars de dispositius de gent que treballa en zones sensibles de la UE a partir d’una mostra gratuïta.

## 3. Per a què s’utilitza?

- Perquè el servei funcioni. Un mapa, el temps o una actualització necessiten dades. Aquest és l’ús legítim i esperat.
- Publicitat i màrqueting. Els intermediaris creen llistes de consumidors classificats segons la ubicació dels seus aparells.
- Revendre-les a altres empreses. Les dades acaben en empreses que les reempaqueten i venen eines per vigilar ubicacions.
- Governs i seguretat. El director de l'FBI va reconèixer el març de 2026, en una audiència al Senat, que l'agència compra dades d'intermediaris per seguir moviments. A Europa, netzpolitik descriu una branca del sector (ADINT) que aprofita dades de la publicitat per a serveis d'intel·ligència.

Si vols saber més sobre el model de negoci de la publicitat basat en aquestes dades, llegeix els nostres articles:

- Els mil·lisegons de la discòrdia <!-- enllaç pendent: entrada no publicada -->
- Post 2 de Sergi <!-- enllaç pendent: segona entrada de Sergi -->

## En resum

La major part de les dades es queden entre tu, el sistema i l’app que fas servir. El problema comença quan una app comparteix amb tercers, i aquests amb uns altres, fins que una dada que ha sortit del teu telèfon ja no la controla ningú.

Vols saber més sobre quins rastrejadors porten les apps que usem diàriament? Llegeix el nostre post: Auditoria de permisos i traçadors aplicacions d'ús habitual. <!-- enllaç pendent: entrada de l'encàrrec propi -->

Vols saber quines són les lleis que regulen tot això? Llegeix el següent post: [Quines regles protegeixen les dades del teu mòbil?]({% post_url 2026-11-11-regles-dades-mobil %})

## Per saber-ne més

- EFF (2026). [Developers: Beware of Ad Libraries that Betray Your Users’ Location Privacy](https://www.eff.org/deeplinks/2026/07/developers-beware-ad-libraries-betray-your-users-location-privacy).
- TechCrunch (2025). [Phone location data of top EU officials for sale, report finds](https://techcrunch.com/2025/11/04/phone-location-data-of-top-eu-officials-for-sale-report-finds/).
- The Record. [FTC targets companies that collected and sold sensitive location data](https://therecord.media/ftc-location-data-brokers-gravy-venntel-mobilewalla).
- KFF Health News / WUSF (2026). [Your phone knows you’re at the doctor. So do data brokers](https://www.wusf.org/health-news-florida/2026-11-02/your-phone-knows-youre-at-the-doctor-so-do-data-brokers-and-they-profit-from-it).
- The Conversation (2026). [Yes, the government can track your location](https://theconversation.com/yes-the-government-can-track-your-location-but-usually-not-by-spying-on-you-directly-267808).
- PETS 2025. [The Impact of Default Mobile SDK Usage on Privacy and Data Protection](https://petsymposium.org/popets/2025/popets-2025-0042.pdf) (article acadèmic).
