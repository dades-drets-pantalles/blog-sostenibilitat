# Blog del treball de sostenibilitat (PEF1)

Jekyll + GitHub Pages (`main`, `/ (root)`). Web: https://dades-drets-pantalles.github.io/blog-sostenibilitat/

## Entrades noves

Quan algú pugi documents (al repo `uni`, a `PEF/El meu treball/Treball sostenibilitat/`, o aquí a `pendents/`):
1. Mira si són entrades del blog.
2. Passa-les a `_posts/<autor>/AAAA-MM-DD-slug.md` (carpeta de cada autor; imatges a `assets/img/<autor>/`) **sense canviar el contingut**: només format. El títol `# ...` passa a `title`, la línia «*Bloc: ... Pregunta guia: ...*» passa a `bloc` i `pregunta`, i s'afegeix `author` i `date`. El text, les cites `[n]` i les referències queden tal qual.
3. Si un document és un esborrany o té dubtes pendents, pregunta abans de publicar-lo (o posa `published: false`).
4. Compila (`jekyll build`), fes commit i push a `main`. Elimina l'original de `pendents/` un cop publicat.

## Estat de les entrades

Membres i pregunta guia a `_data/preguntes.yml` (1 Eloi Estévez, 2 Sergi López, 3 Timothy Skipper, 4 Joan Pascual, 5 Bernat Casajuana; segons el document d'organització del grup). 3 entrades cadascú.
- Joan: 2 publicades (consentiment; IA i dades públiques). Falta la tercera.
- Eloi: 3 publicades. Originals a `uni/PEF/El meu treball/Treball sostenibilitat/Eloi (originals)/`.
- Sergi: 2 publicades («Sé qui ets», «Els mil·lisegons»), del PDF `Treball_Sostenibilitat_2.pdf` (pàg. 13-20), amb 5 imatges.
- Timothy: 2 publicades (phishing; xarxes socials). Notes al peu passades a [n] + llista «Fonts».
- Bernat: 3 publicades (segona mà, esborrar no és destruir, NIST SP 800-88), del docx `Treball Sostenibilitat.docx`.
- Grup (`_posts/grup/`): auditoria de permisos i traçadors (encàrrec propi, 5 imatges a `assets/img/grup/`) i conclusions. Surten a la portada i a l'arxiu en una secció pròpia.

Totes les entrades tanquen amb una secció `## Fonts` (nom unificat; no feu servir «Referències», «Per saber-ne més», etc.).

Enllaços entre entrades: quan un autor escriu «-Post N Nom» vol dir un enllaç a aquella entrada. Si encara no existeix, es deixa el text amb un comentari `<!-- enllaç pendent: ... -->`; quan es publiqui l'entrada, substitueix-lo per `[títol]({{ '/2026/11/11/slug/' | relative_url }})` (l'adreça de l'entrada: data + nom del fitxer sense la data). **No facis servir `{% post_url %}`**: GitHub Pages (Jekyll 3.10) no hi afegeix `/blog-sostenibilitat/` i l'enllaç dona 404, mentre que Jekyll 4 en local sí, i així no es veu l'error. Després de compilar, comprova que tots els enllaços interns existeixen. Pendents ara: cap.

## Normes del treball (cal tenir-les en compte en revisar entrades)

L'enunciat complet no és al repositori: si es puja, resumeix-lo aquí. El que sabem:
- **Entrades:** més de 10 en total (menys de 10 → nota < 4). Organització del grup: 3 entrades per persona, una per pregunta guia; cadascú treballa de manera independent.
- **Visuals:** més de 2 gràfics o visuals propis al blog. Objectiu: que alguna entrada de cada persona en tingui un (fes servir `_includes/figura.html`).
- **Ús d'IA:** s'ha de declarar als crèdits (pàgina `sobre.md`). Text sense verificar ni declarar = 0.
- **Referències:** les repetides entre entrades compten una sola vegada al total del grup.
- **Encàrrec propi (pendent):** auditoria pròpia de permisos i traçadors de cinc aplicacions d'ús habitual (p. ex. amb Exodus Privacy o eines equivalents), amb resultats documentats i comparats. L'organització de l'encàrrec i les conclusions es decidirà més endavant.

En publicar, avisa (sense tocar el text) si una entrada no té referències, no declara IA o cita fonts que no apareixen a la llista.
