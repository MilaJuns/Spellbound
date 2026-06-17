# Guia de Design — Spellbound Marketing

> Você pode editar esse arquivo a qualquer momento.
> As skills de carrossel, proposta e slide leem este arquivo antes de criar qualquer visual.

---

## Identidade

**Tagline:** Strategy that captivates.
**Vibe geral:** Sereno, premium, warm-dark, editorial. Calmo — nunca barulhento.
**Arquétipo visual:** Sábio. Profundidade marrom + toque de laranja como faísca de energia.

---

## Cores

**Paleta base (tema escuro — padrão):**
- **Fundo principal (canvas):** `#510000` (maroon-800)
- **Fundo profundo / page floor:** `#1A0000` (maroon-950)
- **Cards / surface:** `#3A0000` (maroon-900)
- **Surface elevada:** `#720000` (maroon-700)
- **CTA / maroon forte:** `#990000` (maroon-600)

**Acentos:**
- **Accent principal (sparkle orange):** `#F95F00` — CTAs, links, o sparkle ✦. Usar com parcimônia.
- **Accent secundário (amber):** `#D4600A` — labels em uppercase, bordas finas, tags de categoria
- **Borda assinatura:** `rgba(212,96,10,0.18)` — hairline amber em elementos escuros

**Texto:**
- **Texto principal sobre maroon:** `#F5EDE0` (cream)
- **Texto secundário:** `rgba(245,237,224,0.66)`
- **Captions / muted:** `rgba(245,237,224,0.42)`
- **Ink sobre cream (tema claro):** `#2A0B0B`

**Cor proibida:** gradientes roxos, texturas carregadas, qualquer cor que "grite"

**Tema claro (quando aplicável):** canvas `#F5EDE0`, texto `#2A0B0B`, bordas `#E2D5BE`

---

## Tipografia

- **Títulos / wordmark / display:** Geometry Soft Pro Bold → fallback: Varela Round
  - `font-family: "Varela Round", "Geometry Soft Pro", system-ui, sans-serif`
  - Geometry Soft Pro: `marca/fonts/Geometry_Soft_Pro-Bold_N.otf`
- **Corpo / UI / labels:** Nunito (300–800) — Google Fonts
- **Tagline / pull-quote (uso pontual):** Cormorant Garamond Italic — Google Fonts

**Tokens CSS completos:** `marca/css/colors_and_type.css` — importar em qualquer HTML com `<link rel="stylesheet" href="../../marca/css/colors_and_type.css">`.

**Tracking:**
- Wordmark: `0.06em`
- Display: `0.01em`
- Eyebrow/labels uppercase: `0.18em`

---

## Estilo geral

Flat solid maroon — sem gradientes pesados nem texturas. Decoração máxima: scatter de sparkles em baixo contraste.
Cards escuros: fill `#3A0000` + borda amber fina + leve lift no hover.
Fotos: retratos/lifestyle com luz Northern/Dutch. Aplicar overlay `linear-gradient(to top, rgba(81,0,0,.42), transparent)` sobre fotos para manter legibilidade.

---

## Elementos-chave

- **Bordas:** hairline amber fina (1px) em dark; warm cream hairline em light
- **Border-radius dos cards:** `8px` (padrão), `12–18px` para painéis maiores, `999px` para pills/botões
- **Botões primários:** fill `#990000`, hover `#FF7A26`, press `#B8500A`, glow `rgba(249,95,0,0.28)`
- **Sombras:** `0 6px 20px rgba(26,0,0,0.30)` — contidas e quentes; profundidade via borda + 2px lift
- **Motion:** fades + `translateY` suave, `cubic-bezier(0.16,1,0.3,1)`, 260–520ms. Sem bounce, sem loops infinitos

---

## Ícone / símbolo de marca

O sparkle ✦ de quatro pontas é o glifo assinatura da Spellbound:
- Arquivo SVG: `marca/spellbound-mark.svg`
- Divisor de seção: `marca/spellbound-sparkle-row.svg`
- Usar como bullet, divisor, ícone de card, end-mark, decoração centralizada acima de headlines
- **Nunca** substituir por emojis genéricos

---

## O que NUNCA fazer

- Hype vazio ou promessas mágicas no visual ou copy
- Gradientes púrpura / cores frias
- Sombras pesadas ou motion com bounce
- Emojis decorativos (só o ✦ é permitido como glifo de marca)
- Qualquer elemento que "grite" — o visual deve ser sereno e premium

---

## Logo

- **Arquivo principal:** `marca/assets/spellbound-logo-card.jpg`
- **Artwork original:** `marca/assets/Spelbound-Marketing.jpg` (logo lockup sobre maroon 1920×1080)
- **Mark SVG:** `marca/spellbound-mark.svg`
- **Spelling canônico: Spellbound** (dois L). O artwork original usa "SPELBOUND" (erro tipográfico) — ignorar; usar sempre "Spellbound"
- **Versão pra fundo escuro:** usar logo sobre maroon (padrão)
- **Onde usar:** slide final do carrossel (CTA), header de propostas, slides de apresentação
- **Tamanho sugerido:** largura 120–200px nos HTMLs

---

## Perfil do autor

- **Nome:** Mila Juns
- **Fotos:** `marca/fotos/` — founder-headshot.jpeg, founder-portrait.jpeg, founder-desk.jpeg, founder-mic.jpeg
- **Badge verificado:** a definir

---

## Relação com Mila Juns (marca BR)

Spellbound é a marca NL de Mila Juns — irmãs, não gêmeas.
Espinha compartilhada: canvas maroon · texto cream · Varela Round + Nunito · radius 8px · voz Sábio Parceiro.
O que diferencia a Spellbound: accent **laranja** (não amber) · sparkle ✦ como motif · toque de Cormorant Italic · layout mais arejado · inglês/NL.

---

## Estrutura da pasta marca/

```
marca/
  design-guide.md          ← este arquivo
  spellbound-mark.svg      ← sparkle mark (4 pontas)
  spellbound-sparkle-row.svg ← divisor de seção
  assets/
    spellbound-logo-card.jpg    ← logo lockup principal
    Spelbound-Marketing.jpg     ← artwork original (1920×1080)
  fonts/
    Geometry_Soft_Pro-Bold_N.otf
  fotos/
    founder-headshot.jpeg
    founder-portrait.jpeg
    founder-desk.jpeg
    founder-mic.jpeg
  css/
    colors_and_type.css    ← todos os tokens CSS (cores, tipografia, espaçamentos)
  exports/
    Spellbound-Flyer-A4.png
    Spellbound-Square-1080.png
    Spellbound-Story-1080x1920.png
  templates/
    slides/                ← pitch deck (7 slides HTML + slide.css)
    flyers/                ← flyer options, services infographic, social variations
```

## Observações adicionais
