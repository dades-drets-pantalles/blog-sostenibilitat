---
title: "Conclusions"
author: "Tot el grup"
date: 2026-11-11 18:40:00 +0100
bloc: "Conclusions"
---

L’objectiu del projecte Vincle Digital és la reutilització de mòbils usats perquè es puguin donar a persones que ho necessitin [1]. Els telèfons mòbils són gairebé essencials en la nostra vida, ja sigui per comunicar-se, fer tràmits, o qualsevol necessitat quotidiana. Però a més dels beneficis, s’han de tenir en compte els riscs d’ús d’aquestes tecnologies. En aquest projecte, hem investigat quins són aquests riscs en l’àmbit particular de la privacitat: la recollida i l’ús de les nostres dades personals.

En l’[expedient 1]({{ '/entrades/' | relative_url }}#pregunta-1), vam veure quines dades genera el nostre telèfon mòbil: què fa, on és, com es mou i altres formes en què es pot identificar. Tot seguit vam veure com aquestes dades arriben al fabricant, sistema operatiu, operadora i sobretot als intermediaris de dades que després les venen a tercers. En el mateix post vam també veure que amb aquestes dades es pot deduir informació delicada com on vius, on treballes i si tens problemes de salut. Finalment, vam comentar quina és la legislació actual i quines autoritats s'encarreguen que es compleixi.

Tot seguit, a l’[expedient 2]({{ '/entrades/' | relative_url }}#pregunta-2), vam aprofundir sobre l’ús d’aquestes dades per fer publicitat. Vam analitzar en detall l’ús que en fan les empreses per generar un perfil complet de l’usuari i estimar els seus interessos. Un cop inferits els gustos, la publicitat programàtica permet, en qüestió de mil·lisegons, automatitzar la publicació d’un anunci adequat, així com la seva compra a un preu assequible. L’expedient conclou detallant la rentabilitat econòmica del model, així com la seva manca de transparència i regulació.

Després, a l’[expedient 3]({{ '/entrades/' | relative_url }}#pregunta-3) vam investigar quins són els grups més vulnerables a ciberestafes i com la recollida de dades juga una part en aquestes situacions. Vam trobar que la gent gran i les persones en situacions de dificultat econòmica són més susceptibles a les estafes com el phishing, amb una pèrdua mediana elevada, però també que la gent jove és afectada significativament per les estafes per xarxes socials, si bé amb pèrdues medianes inferiors.

A l’[expedient 4]({{ '/entrades/' | relative_url }}#pregunta-4), vam analitzar què protegeix el RGPD i on arriben els seus límits. Vam veure que el consentiment sovint no és més que formalisme: ningú no llegeix les polítiques de privacitat i el disseny dels bàners condiciona la decisió. També vam comprovar que el RGPD té dificultats per protegir les dades davant l’entrenament de models d’intel·ligència artificial, perquè les dades recollides d’internet són impossibles d’esborrar d’un model ja entrenat. La llei dona eines per sancionar les pràctiques malignes, però sovint les persones no poden assumir aquestes responsabilitats, cosa que afecta les persones vulnerables especialment, com les del programa VINCLE DIGITAL.

Per acabar, a l’[expedient 5]({{ '/entrades/' | relative_url }}#pregunta-5), en relació als mòbils de segona mà, hem explorat les possibles conseqüències que pot tenir el fet que un dispositiu mòbil pertanyent a una persona/entitat vagi a parar a terceres persones (ja sigui per venda, regal, etc.) i la informació no estigui correctament esborrada. Hem vist que és possible recuperar dades que aparentment havien estat eliminades, o fins i tot en un mòbil que ha passat per un restabliment de fàbrica. També hem vist que no és el mateix eliminar informació d’un sistema operatiu que esborrar-la de manera irreversible (sanititzar). Finalment, hem vist que hi ha maneres de sanititzar un dispositiu seguint estàndards com el NIST SP 800-88.

Després d’aquests cinc expedients, vam realitzar una [auditoria de rastrejadors d’aplicacions Android]({{ '/2026/11/11/auditoria-permisos-i-tracadors/' | relative_url }}), i vam trobar que Exodus Privacy és un recurs fàcil d’utilitzar i transparent per informar-se de com es tracten les dades en cada aplicació.

## Recomanacions per a VINCLE DIGITAL

Amb el que hem trobat, doncs, recomanem a l’equip de VINCLE DIGITAL les següents accions per al procés de recondicionament:

- **Dur a terme un esborrat segur obligatori abans de cada lliurament:** cal incloure al protocol un pas de sanitització de dades seguint l’estàndard NIST SP 800-88, i no només un restabliment de fàbrica, amb un registre de verificació per a cada dispositiu.
- **Una fitxa informativa per al nou usuari:** una bona iniciativa seria augmentar la conciència, per exemple, tot lliurant amb cada mòbil una guia breu que expliqui què són els permisos d’una aplicació, com revisar-los i, en dispositius Android, com utilitzar Exodus Privacy per consultar els rastrejadors d’una aplicació. D’aquesta manera, reduïm el desconeixement envers aquests temes. Per a dispositius iPhone, Exodus encara és informatiu per als usuaris, ja que dona una bona idea del tipus de rastrejadors usat en les aplicacions, encara que no sigui completament idèntic en Google Play i l’App Store. Aquesta fitxa pot ser lliurada pels professionals que acompanyen la persona, que ja fan de mediadors digitals.

És impossible ser invisible i completament anònim en l’era actual d’internet, però es poden fer passos per reduir el factor de risc de les dades més sensibles, tant per mesures legals com per precaucions a nivell individual, facilitant un entorn més segur per a tothom.

## Fonts

1. <https://aucoop.upc.edu/vincle-digital/>
