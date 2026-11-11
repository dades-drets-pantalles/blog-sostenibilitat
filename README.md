# Blog del treball de sostenibilitat (PEF1)

Web feta amb Jekyll i publicada amb GitHub Pages. Cada canvi a `main` es publica sol en 1-2 minuts.

## Afegir o editar una entrada (des del navegador)

1. Entra a la carpeta `_posts/` del repositori a github.com.
2. **Add file → Create new file**. Nom: `AAAA-MM-DD-titol-curt.md` (per exemple `2026-11-12-vigilancia-laboral.md`). La data del nom és la data de publicació i ordena les entrades; si és futura, l'entrada no surt fins aquell dia.
3. Copia la capçalera de `_posts/2026-11-11-plantilla.md` (el bloc entre `---`), omple-la i escriu el text a sota.
4. **Commit changes** directament a `main`. En un parell de minuts és a la web (pestanya *Actions* per veure'n l'estat).

Per editar una entrada existent: obre-la i clica el llapis.

## Imatges i gràfics

Puja la imatge a `assets/img/` i posa-la a l'entrada així (amb peu de figura):

```liquid
{% include figura.html src="/assets/img/nom.png" peu="Figura 1. Descripció i font de les dades." %}
```

Les cites `[1]`, `[2, 3]` es converteixen soles en enllaços a la llista de la secció «Referències».

## Entrades pendents

Si no vols fer la conversió tu, deixa el document (`.md`, `.docx`, `.txt`) a `pendents/` i es passarà al format del blog.

## Previsualitzar en local (opcional)

```bash
gem install jekyll jekyll-feed jekyll-seo-tag
jekyll serve
```

## Activar GitHub Pages (una sola vegada)

Settings → Pages → *Build and deployment* → Source: **Deploy from a branch**, branca `main`, carpeta `/ (root)`.
