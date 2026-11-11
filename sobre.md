---
title: Sobre el bloc
permalink: /sobre/
layout: page
---

Aquest bloc forma part del treball de sostenibilitat de *Projectes d'Enginyeria Física I* (ETSETB, UPC), sobre privacitat, vigilància i seguretat digital.

<!-- Completeu: context del projecte (VINCLE DIGITAL), objectiu del blog... -->

## Autoria

{% for q in site.data.preguntes %}- **{{ q.autor }}**: {{ q.pregunta }}
{% endfor %}

## Com hem fet servir la intel·ligència artificial

Hem utilitzat eines d'IA generativa (Claude, d'Anthropic) en aquest treball, i volem explicar exactament per a què.

**Sí que l'hem fet servir per a:**

- **Construir aquesta pàgina web.** L'estructura del blog, el codi i la publicació a GitHub Pages s'han fet amb l'ajuda de l'IA.
- **El disseny.** L'aspecte visual del blog (colors, tipografia, maquetació i la il·lustració de la portada) s'ha fet amb eines d'IA de disseny.
- **Buscar informació.** L'hem fet servir per trobar fonts, estudis i notícies. Cada dada que citem l'hem contrastada amb la font original, que apareix a la llista de referències de cada entrada.
- **Organitzar els blogs.** Passar les entrades al format de la web, agrupar-les per pregunta guia i enllaçar-les entre si.
- **Corregir l'ortografia** d'algunes entrades, sense canviar-ne el contingut.

**No l'hem fet servir per escriure les entrades.** Els textos, les idees i les opinions són nostres; cada entrada està signada pel membre del grup que l'ha escrit.
