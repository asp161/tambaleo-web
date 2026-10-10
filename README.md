# Web de Tambaleo

Esta carpeta es la web pública del juego. **No la edites a mano:** se genera con

```bash
python3 tools/build_web.py
```

a partir de `tools/web/` (página y estilos), `game/core/config.gd` (enlaces), `game/core/daily.gd` (fecha del reto #1) y `docs/legal/*.md` (textos legales).

- `index.html`: la página a la que lleva el enlace de cada resultado compartido. Con `?r=12&m=437` dice "Alguien ha apilado 4,37 m en el reto #12. ¿Puedes superarlo?" y enseña los botones de las tiendas.
- `privacidad.html`, `terminos.html` y `aviso-legal.html`: las tiendas piden la privacidad en una URL pública.

## Publicarla

Se publica gratis con GitHub Pages desde el repo **público** [`asp161/tambaleo-web`](https://github.com/asp161/tambaleo-web) (el del juego es privado), en `https://asp161.github.io/tambaleo-web/`, que es `Config.SITE_URL`.

Para actualizarla, desde el repo del juego:

```bash
bash tools/publicar_web.sh
```

Genera la web, la copia a `tambaleo-web` (lo clona junto a este repo si no está) y la sube. Si un día usas un dominio propio, cambia `SITE_URL` en `game/core/config.gd` y vuelve a publicar.
