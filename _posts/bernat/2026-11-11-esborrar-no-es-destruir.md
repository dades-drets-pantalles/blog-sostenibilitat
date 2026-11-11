---
title: "Esborrar no és destruir"
author: "Bernat Casajuana"
date: 2026-11-11 18:10:00 +0100
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "Quins riscos afegeix un dispositiu de segona mà mal esborrat? Quins estàndards existeixen (NIST SP 800-88) i què impliquen?"
---

Per què quan eliminem un fitxer, formategem o restablim un mòbil de fàbrica, les dades no sempre desapareixen completament? Si no has llegit el [post anterior]({{ '/2026/11/11/perills-dispositius-segona-ma/' | relative_url }}) potser t’estaràs preguntant si això realment passa. T’animem a llegir-lo! Si ja l’has llegit, en aquest abordarem la pregunta anterior.

## Què significa realment eliminar un fitxer?

Posem un exemple senzill. Imagina que tens una fotografia guardada al teu ordinador i decideixes eliminar-la. La fotografia desapareix de la carpeta i també de la paperera de reciclatge. Aparentment, ja no existeix. Però el que ha passat és que el sistema operatiu ha deixat de mostrar aquella fotografia com un fitxer disponible. Això no significa necessàriament que tota la informació que la formava hagi estat eliminada del suport físic. De manera que eliminar un fitxer implica únicament que el sistema operatiu ja no pot mostrar-lo, però part de la informació del fixer pot seguir continguda en un dispositiu d'emmagatzematge després que s'hagi intentat eliminar. Aquest tipus d’informació s’anomena Data remanence (persistència de dades).

## Quina diferència hi ha entre eliminar, formatar i esborrar de manera segura?

Tot i que aquestes tres paraules sovint es puguin servir com a sinònims, són tres conceptes ben diferents:

- **Eliminar un fitxer:** Quan elimines un fitxer, normalment el sistema operatiu elimina la referència que permet localitzar-lo. L'espai que ocupava es considera disponible per guardar-hi informació nova. Però les dades originals poden continuar presents fins que s'hi escriu informació nova.
- **Formatar un dispositiu:** Formatar significa preparar un dispositiu perquè pugui tornar a emmagatzemar informació. Un formatatge ràpid, per exemple, pot eliminar les referències als fitxers sense sobreescriure tot el contingut anterior.
- **Sanititzar un dispositiu (esborrar de manera segura):** És un procediment que busca fer inviable la recuperació de les dades anteriors, tenint en compte els recursos i el nivell d'esforç que podria utilitzar algú per recuperar-les. Això és precisament el que busquem.

## L'esborrada criptogràfica (Cryptographic Erase)

Alguns dispositius xifren automàticament les dades quan s'escriuen. Si s'eliminen de manera segura les claus necessàries per desxifrar-les, les dades xifrades poden quedar inaccessibles sense necessitat de sobreescriure cada bloc d'emmagatzematge. De manera que per “esborrar correctament” algunes dades n’hi ha prou amb fer desaparèixer les seves claus de xifratge i totes les còpies d’aquestes. Però cal tenir en compte algunes coses:

- El dispositiu ha d'haver estat xifrat correctament.
- Les claus han de ser adequades i no poden continuar disponibles en còpies recuperables.
- S'ha de confiar en la implementació del fabricant.
- Cal verificar que el procediment s'ha executat correctament.

## La verificació

Un cop s’ha formatat o bé sanititzat un dispositiu, verificar que s’hagi pogut completar amb eficàcia és molt important: no n'hi ha prou amb executar una eina i assumir que ha funcionat. De fet, entre d’altres coses cal comprovar:

- Si el procés ha finalitzat correctament.
- Si el dispositiu admet el mètode utilitzat.
- Si hi ha àrees d'emmagatzematge que no s'han pogut tractar.
- Si el resultat és adequat per al nivell de confidencialitat de les dades

## Conclusió

Hem vist doncs que no és tan fàcil esborrar correctament la informació, i ni tan sols entendre amb claredat què vol dir “esborrar”. Però llavors, si no podem confiar simplement en l'opció de formatar o restablir de fàbrica, com podem saber quin procediment és realment segur? Si vols saber la resposta a aquesta pregunta llegeix el post **[NIST SP 800-88 i IEEE 2883: estàndards per a una esborrada segura]({{ '/2026/11/11/nist-sp-800-88/' | relative_url }})**.

## Fonts

- [https://www.sciencedirect.com/science/article/pii/S2666281723000963](https://www.sciencedirect.com/science/article/pii/S2666281723000963?utm_source=chatgpt.com)
- [https://www.ncsc.gov.uk/guidance/secure-sanitisation-storage-media](https://www.ncsc.gov.uk/guidance/secure-sanitisation-storage-media?utm_source=chatgpt.com)
- [https://csrc.nist.gov/pubs/sp/800/88/r2/final](https://csrc.nist.gov/pubs/sp/800/88/r2/final)
