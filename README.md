# Blog del treball de sostenibilitat (PEF1)

Web feta amb Jekyll i publicada amb GitHub Pages. Cada canvi a `main` es publica sol en 1-2 minuts.

## Estructura: una carpeta per autor

| Autor | Entrades | Imatges |
|---|---|---|
| Eloi | `_posts/eloi/` | `assets/img/eloi/` |
| Sergi | `_posts/sergi/` | `assets/img/sergi/` |
| Timothy | `_posts/timothy/` | `assets/img/timothy/` |
| Joan | `_posts/joan/` | `assets/img/joan/` |
| Bernat | `_posts/bernat/` | `assets/img/bernat/` |

Cadascú edita només la seva carpeta. Al `README.md` de cada carpeta hi ha les instruccions i la capçalera ja omplerta amb la pregunta guia. La portada agrupa les entrades per pregunta guia segons aquestes carpetes (`_data/preguntes.yml`).

Per editar: obre el fitxer a github.com, clica el llapis i fes **Commit changes** a `main`. En 1-2 minuts la web s'actualitza (pestanya *Actions* per veure'n l'estat).

## Imatges i gràfics

Puja la imatge a `assets/img/` i posa-la a l'entrada així (amb peu de figura):

```liquid
{% include figura.html src="/assets/img/<nom>/fitxer.png" peu="Figura 1. Descripció i font de les dades." %}
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
