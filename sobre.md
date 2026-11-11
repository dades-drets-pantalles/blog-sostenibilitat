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

## Crèdits i ús d'IA

<!-- Obligatori: declareu aquí les eines d'IA que s'han fet servir, per a què i com s'ha verificat el contingut. -->
