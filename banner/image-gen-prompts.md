# Banner Image Generation Prompts

O `banner.svg` / `banner.png` desse kit é vetorial — funciona, mas tem teto. Pra versão foto-realista (mais cinematográfica), gera no Midjourney, Bing Image Creator (DALL-E 3) ou Leonardo.AI usando os prompts abaixo.

**Specs LinkedIn**: 1584×396 px, proporção 4:1.

---

## Prompt principal — AI Engineer / Cosmic Network

```
Abstract visualization of an AI agent network in deep cosmic space:
glowing central node connected to a constellation of orbiting nodes via
luminous data streams. Multiple data flows converging toward a brilliant
core, then radiating outward as light particles. Background: deep
navy-black void with soft purple and blue nebula clouds, distant stars,
subtle hexagonal grid fading into depth.

Color palette: dark navy #1a1b27 base, electric blue #70A5FD primary
accents, cyan #06b6d4 secondary, white highlights, occasional purple
glow.

Style: cinematic sci-fi digital art, sophisticated and minimalist,
professional tech aesthetic. High contrast, atmospheric depth,
volumetric lighting, particle effects.

Composition: ultrawide cinematic banner, subject centered slightly
right, left third intentionally minimal and dark for profile photo
overlay. Strong horizontal flow.

No text, no logos, no faces, no human figures. Pure abstract atmosphere.

Aspect ratio: 4:1 ultrawide cinematic banner.
```

**Negativos pra Midjourney** (`--no` flag):
```
--no marvel, comic book character, superhero, copyrighted character, text, logo, watermark, human face, robot
```

---

## Variação — Mais minimalista

```
Minimalist abstract LinkedIn banner: a single glowing focal point
(intelligence core) with subtle radiating energy lines flowing
horizontally across deep cosmic black space. Sparse luminous particles
drifting. Tokyonight color palette — base #1a1b27, accent #70A5FD,
silver chrome highlights. Cinematic, atmospheric, sophisticated.
Left third empty/dark for profile photo overlay. No text, no figures,
pure abstract.

4:1 aspect ratio ultrawide.
```

---

## Variação — Circuit / Architecture vibe

```
Abstract architectural visualization: a deep cosmic technical schematic
with glowing nodes, data flow paths, and subtle blueprint grid.
Resembles a system architecture diagram blended with a cosmic nebula.
Multiple horizontal flowing data streams converging at a central
luminous hub. Tokyonight palette (#1a1b27, #70A5FD, #06b6d4),
volumetric lighting, atmospheric depth.

Style: technical sci-fi, Blade Runner meets system diagram.
Composition: ultrawide cinematic banner, focal hub center-right, left
third minimal. No text, no logos.

4:1 aspect ratio.
```

---

## Workflow recomendado

1. **Bing Image Creator** (`bing.com/create`, grátis) — começa aqui. DALL-E 3, 4 variações em ~30s.
2. Se nenhuma agradar → **Leonardo.AI** (`leonardo.ai`, grátis com créditos diários, suporta aspect ratio 4:1 nativo).
3. Se quer qualidade máxima → **Midjourney** (US$10/mês). Use `--ar 16:4 --style raw --v 6` ou versão atual.

---

## Pós-processamento

A maioria dos geradores não entrega exatamente 1584×396. Pra ajustar:

1. Abre no **Photopea** (`photopea.com`, grátis, tipo Photoshop web)
2. `Image → Canvas Size`, define **1584 × 396**
3. Posiciona focal point center-right
4. Se sobrar espaço, usa `Edit → Content-Aware Fill` ou estende com Clone Stamp
5. `File → Export As → PNG`

---

## Anti-padrões

- ❌ Imagem com face/figura humana — risco de uncanny valley
- ❌ Texto na imagem — gerador erra, fica amador
- ❌ Cliché "futuristic globe with circuits" — todo banner de dev tem
- ❌ Robot fofinho com olho azul — cliché de stock photo de IA
- ❌ Personagens copyrighted (mesmo "inspirado em") — risco e amador
