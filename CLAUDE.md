# Blog del treball de sostenibilitat (PEF1)

Jekyll + GitHub Pages (`main`, `/ (root)`). Web: https://dades-drets-pantalles.github.io/blog-sostenibilitat/

## Entrades noves

Quan algú pugi documents (al repo `uni`, a `PEF/El meu treball/Treball sostenibilitat/`, o aquí a `pendents/`):
1. Mira si són entrades del blog.
2. Passa-les a `_posts/AAAA-MM-DD-slug.md` **sense canviar el contingut**: només format. El títol `# ...` passa a `title`, la línia «*Bloc: ... Pregunta guia: ...*» passa a `bloc` i `pregunta`, i s'afegeix `author` i `date`. El text, les cites `[n]` i les referències queden tal qual.
3. Si un document és un esborrany o té dubtes pendents, pregunta abans de publicar-lo (o posa `published: false`).
4. Compila (`jekyll build`), fes commit i push a `main`. Elimina l'original de `pendents/` un cop publicat.

## Estat de les entrades

Membres: Joan Pascual, Eloi, Bernat, Sergi, Timothy (3 entrades cadascú).
- Joan: 1 publicada (consentiment). Pendents: entrada 2 (IA i dades públiques, a `uni`, amb dubtes oberts a `RGPD - Dubtes i revisió.md`) i una tercera.
- Eloi: 3 publicades (sèrie sobre les dades del mòbil). Originals a `uni/PEF/El meu treball/Treball sostenibilitat/Eloi (originals)/`.
- Bernat, Sergi, Timothy: cap encara.

Enllaços entre entrades: quan un autor escriu «-Post N Nom» vol dir un enllaç a aquella entrada. Si encara no existeix, es deixa el text amb un comentari `<!-- enllaç pendent: ... -->`; quan es publiqui l'entrada, substitueix-lo per `[títol]({% post_url slug %})`. Pendents ara: post 2 de Joan, post 2 de Sergi, «Els mil·lisegons de la discòrdia», «Auditoria de permisos i traçadors» (encàrrec propi).

## Normes del treball (cal tenir-les en compte en revisar entrades)

L'enunciat complet no és al repositori: si es puja, resumeix-lo aquí. El que sabem:
- **Entrades:** més de 10 en total (menys de 10 → nota < 4). Organització del grup: 3 entrades per persona, una per pregunta guia; cadascú treballa de manera independent.
- **Visuals:** més de 2 gràfics o visuals propis al blog. Objectiu: que alguna entrada de cada persona en tingui un (fes servir `_includes/figura.html`).
- **Ús d'IA:** s'ha de declarar als crèdits (pàgina `sobre.md`). Text sense verificar ni declarar = 0.
- **Referències:** les repetides entre entrades compten una sola vegada al total del grup.
- **Encàrrec propi (pendent):** auditoria pròpia de permisos i traçadors de cinc aplicacions d'ús habitual (p. ex. amb Exodus Privacy o eines equivalents), amb resultats documentats i comparats. L'organització de l'encàrrec i les conclusions es decidirà més endavant.

En publicar, avisa (sense tocar el text) si una entrada no té referències, no declara IA o cita fonts que no apareixen a la llista.
