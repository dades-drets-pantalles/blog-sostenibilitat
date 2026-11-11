# Entrades de Timothy

Pregunta guia: *Quins riscos específics tenen les persones en situació vulnerable: estafes, phishing, suplantació d'identitat, control per part de tercers?*

Aquesta carpeta és teva. Cada fitxer `.md` és una entrada del blog.

## Editar una entrada

Obre el fitxer, clica el llapis (✏️), canvia el que vulguis i fes **Commit changes** a `main`. En 1-2 minuts la web s'actualitza.

## Afegir una entrada

**Add file → Create new file** dins d'aquesta carpeta. Nom: `AAAA-MM-DD-titol-curt.md` (la data ordena les entrades; si és futura, l'entrada no surt fins aquell dia). Copia aquesta capçalera a dalt de tot:

```yaml
---
title: "Títol de l'entrada"
author: "Timothy"
date: AAAA-MM-DD 12:00:00 +0100
bloc: "Privacitat, vigilància i seguretat digital"
pregunta: "Quins riscos específics tenen les persones en situació vulnerable: estafes, phishing, suplantació d'identitat, control per part de tercers?"
---
```

i escriu el text a sota en Markdown (`## Apartat`, `**negreta**`, `*cursiva*`, `- llista`, `[text](https://enllaç)`). No repeteixis el títol al text.

Si no et ve de gust fer-ho tu, deixa el document (`.docx`, `.md`, `.txt` o `.pdf`) a la carpeta `pendents/` i es convertirà.

## Imatges i gràfics

Puja-les a `assets/img/timothy/` i posa-les així:

```liquid
{% include figura.html src="/assets/img/timothy/nom.png" peu="Figura 1. Descripció. Font: ..." %}
```

## Enllaçar una altra entrada

```liquid
[Títol]({% post_url eloi/2026-11-11-que-fa-el-teu-telefon %})
```

(carpeta de l'autor / nom del fitxer sense `.md`).
