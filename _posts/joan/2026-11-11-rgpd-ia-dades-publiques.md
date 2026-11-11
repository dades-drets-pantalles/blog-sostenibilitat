---
title: "Ningú no t'ha demanat permís: el RGPD davant la intel·ligència artificial"
author: "Joan Pascual"
date: 2026-11-11 13:20:00 +0100
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "què protegeix el RGPD i on arriben els seus límits en la pràctica quotidiana?"
---

La frenètica carrera per la frontera de la intel·ligència artificial necessita tota la informació possible per entrenar els models. És molt probable que les dades que hagis compartit de forma conscient o inconscient ara estiguin representades en els pesos de les neurones de la teva intel·ligència artificial favorita.

## Públic no vol dir lliure

El *web scraping* és la tècnica coneguda que fan servir els laboratoris frontera per aconseguir entrenar els seus models base. Consisteix a construir una màquina predictora tan precisa com sigui possible. Per fer això, entrenen amb totes les dades disponibles a l'internet. Sota la personalitat construïda del teu assistent d'IA, hi ha un monstre predictor que s'ha entrenat amb la teva informació personal.

El RGPD aplica la norma fins i tot quan les dades personals recollides són accessibles a tothom [1]. El Comitè Europeu de Protecció de Dades estableix que compartir una dada en línia no és consentir que es reculli [2]. Les persones no han d'esperar que les seves publicacions es reutilitzin en tots els casos i amb finalitat indiscriminada [2].

Llavors, com justifiquen aquestes empreses la seva activitat legalment? El CEPD admet que el consentiment no seria probablement una base aplicable [2]. L'opció és l'interès legítim (art. 6.1.f), que exigeix un interès legítim real, que el tractament sigui necessari i que els drets dels afectats no hi prevalguin [2, 3].

Tenim un problema. Els drets del RGPD estan pensats per a una relació entre persona i organització concreta, però en el *scraping* aquesta no existeix.

## Com t'hi oposes si no ho saps?

No cal permís per a l'interès legítim, però pots oposar-t'hi. Això no obstant, com pots oposar-t'hi si no saps que ocorre, ja que ningú et notifica? Les directrius del CEPD concedeixen que davant la impossibilitat de comunicar persona a persona, llavors l'entitat pot no estar obligada a fer-ho individualment [2]. I pot ser suficient publicar a la seva pròpia web [2].

A més, l'article 21 no és un dret absolut. Cal al·legar motius relacionats amb la teva situació particular, i l'empresa pot continuar si demostra motius legítims imperiosos que hi prevalguin [4]. Impracticabilitat legal en tot el seu esplendor.

Hi ha dos casos que ho exemplifiquen:

- **Meta (2025).** Va anunciar que entrenaria la seva IA amb contingut públic d'usuaris de la UE i els va avisar que podien oposar-s'hi abans del 27 de maig [5] (jo, personalment, no me'n vaig assabentar). El tribunal superior de Colònia va rebutjar frenar-ho de manera cautelar, en part per les mesures de protecció que oferia [5]. És a dir, el teu silenci (probablement ignorant) va ser suficient: passem del «sí» explícit al «no» que has de saber dir a temps.

- **LAION-5B (2024).** En aquest conjunt, Human Rights Watch va descobrir 170 imatges de nens brasilers sense el coneixement de les seves famílies, que s'havien utilitzat per entrenar una IA [6], i 190 imatges de nens australians. Moltes incloïen noms o ubicacions, i la revisió va examinar menys del 0,0001% dels 5.850 milions d'imatges: els nombres són escandalosos [6].

Com pot una família exercir el dret a objectar a una cosa que ni tan sols sap que ha passat? Qui ens protegeix de tot això?

## El model recorda (i costa molt fer-li oblidar)

Esborrar un *datapoint* d'una base de dades és generalment fàcil. Això no obstant, eliminar l'efecte sobre l'entrenament d'una xarxa neuronal (arquitectura base dels *Large Language Models*) que va tenir una dada és impossible.

I això és un problema. Perquè els models memoritzen. No perquè vulguin, sinó perquè el disseny dels procediments d'entrenament ho afavoreix. Si el teu número de telèfon és a l'internet, llavors es penalitzarà que el model s'equivoqui recitant-lo, això fa que l'aprengui. I no l'oblida. Un estudi de Nasr i coautors va aconseguir que ChatGPT donara informació personal en el 16,9% de les 15.000 sortides analitzades, contenint informació com telèfons i adreces associades a particulars [7]. És difícil no esmentar quan suposadament OpenAI va furtar les dades sobre el problema de Navier-Stokes [10].

El dret de supressió (art. 17) es veu profundament afectat per aquest fenomen. Les dades no es poden esborrar d'un model ja entrenat. Reentrenar un model base és caríssim (és entrenar amb tot l'internet i és una de les tasques per a les quals es necessiten tants centres de dades). El desaprenentatge és un problema extremadament difícil [8]. Hi ha qui proposa que la solució és filtrar les sortides. La llei diu «esborra» i la tecnologia respon «amaga».

## La IA s'equivoca (també amb qui ets)

Independentment de si es comunica de forma legal o consentida, la llei també exigeix que les dades siguin precises. OpenAI va ser denunciada perquè ChatGPT va inventar que un particular havia matat els seus dos fills, i ho va barrejar amb informació correcta sobre la seva vida [9]. Aquesta qüestió delicada requereix tractaments a l'altura, i no missatges en cursiva dient «Els nostres models cometen errors».

Com aplicar el dret de rectificació a un model probabilístic és una incògnita. És un exemple més de com la legislació va molt més lenta que la intel·ligència artificial. Tampoc culpo el sector polític o jurídic. És difícil no anar més lent que la intel·ligència artificial, en general. Però calen mesures i reformes.

## Què en podem concloure

Ja sabem que el RGPD no considera suficient que les dades siguin públiques, però els seus mecanismes són pràcticament irrealitzables. Es pressuposen individus conscients d'on són les seves dades i models capaços d'oblidar. Amb el paradigma actual de la IA, és impossible.

Per tant, aprenem que la protecció ha d'arribar abans de la recollida de dades. Els usuaris han d'evitar compartir aquestes dades en primer lloc. A més, la legislació s'ha de posar al dia i construir mecanismes eficaços per responsabilitzar les empreses de forma pràctica. Idealment, s'hauria de demanar responsabilitat moral per part de les grans tecnològiques. Idealment.

## Referències

1. Reglament (UE) 2016/679 (RGPD): arts. 5, 6, 14, 17 i 21. <https://eur-lex.europa.eu/eli/reg/2016/679/oj>
2. CEPD (2026). *Guidelines 03/2026 on web scraping in the context of generative AI*, versió 1.0 per a consulta pública, adoptada el 7 de juliol de 2026. <https://www.edpb.europa.eu/system/files/2026-07/edpb_guidelines_2020603_webscraping_v1_en_0.pdf>
3. CEPD (2024). *Opinion 28/2024 on certain data protection aspects related to the processing of personal data in the context of AI models*, adoptada el 17 de desembre de 2024. <https://www.edpb.europa.eu/system/files/2024-12/edpb_opinion_202428_ai-models_en.pdf>
4. RGPD, art. 21.1. <https://gdpr-info.eu/art-21-gdpr/>
5. Taylor Wessing (2025). *Meta vs Verbraucherzentrale NRW*. <https://www.taylorwessing.com/en/insights-and-events/insights/2025/05/meta-vs-verbraucherzentrale-nrw>
6. Xataka On. *AI Models Are Being Trained With Photos of Children*, sobre els informes de Human Rights Watch. <https://www.xatakaon.com/robotics-and-ai/ai-models-are-being-trained-with-photos-of-children-and-it-doesnt-matter-if-parents-try-to-avoid-it>
7. Nasr, M. et al. (2023). *Scalable Extraction of Training Data from (Production) Language Models*. <https://arxiv.org/abs/2311.17035>
8. Bourtoule, L. et al. *Machine Unlearning*. <https://arxiv.org/abs/1912.03817>
9. noyb (20 de març de 2025). *AI hallucinations: ChatGPT created a fake child murderer*. <https://noyb.eu/en/ai-hallucinations-chatgpt-created-fake-child-murderer>
10. TechStartups (9 de setembre de 2026). *OpenAI says it solved the 90-year-old Navier-Stokes math problem in 88 hours. Now it faces accusations of stealing researchers' work*. <https://techstartups.com/2026/09/09/openai-says-it-solved-the-90-year-old-navier-stokes-math-problem-in-88-hours-now-it-faces-accusations-of-stealing-researchers-work/>
