# @contracorriente/ui

Tokens de ContraCorriente. La fuente que se edita es el Figma. `source/raw/` es el export. El CSS de `build/` se genera y se versiona para que el sitio no corra Python.

```bash
npm run verify
```

En el sitio, un solo grafo de `@import`, en este orden:

```css
@import "@contracorriente/ui/tokens.css";
@import "@contracorriente/ui/tokens-dark.css";
@import "@contracorriente/ui/theme-bridge.css";
```

`tokens-dark.css` vive bajo `.dark`. Sin esa clase, el sitio queda en claro. Las familias las carga `next/font` del sitio (`--typography-family-*`). Este paquete no trae `@font-face`.

El siguiente cliente no depende de este repo. Duplicá el Figma y este paquete, cambiá el `name`, corré `npm run verify` y tageá. La receta está en el sitio starter, `docs/runbooks/fork-de-cliente.md`.
