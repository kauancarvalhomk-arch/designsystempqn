# Design System Rules

Cores → **Radix UI Colors**  
Tipografia e Espaçamento → **Material Design 3**

---

## 1. Cores — Radix UI Colors

### Os 12 steps de cada escala

| Step | Uso |
|------|-----|
| 1 | Background do app |
| 2 | Background sutil |
| 3 | Background de elemento UI (estado normal) |
| 4 | Background de elemento UI (hover) |
| 5 | Background de elemento UI (ativo / selecionado) |
| 6 | Bordas sutis e separadores |
| 7 | Borda de elementos interativos e focus rings |
| 8 | Borda hover de elementos interativos |
| 9 | Backgrounds sólidos (step mais puro, maior chroma) |
| 10 | Hover de backgrounds sólidos |
| 11 | Texto de baixo contraste |
| 12 | Texto de alto contraste |

### Detalhamento por grupo

**Steps 1–2 · Backgrounds**  
Para backgrounds do app e componentes sutis: app principal, tabelas listradas, blocos de código, cards, sidebars, canvas.  
> Em light mode, prefira branco. Em dark mode, use Step 1 ou 2 da sua escala de cinza/cor.

**Steps 3–5 · Backgrounds de componentes**  
- Step 3 → estado normal
- Step 4 → hover
- Step 5 → pressionado / selecionado

> Se o componente tem background transparente no estado padrão, use Step 3 como seu hover.

**Steps 6–8 · Bordas**  
- Step 6 → bordas sutis em elementos não interativos (cards, alerts, separadores, sidebars)
- Step 7 → bordas sutis em elementos interativos
- Step 8 → bordas fortes em elementos interativos e focus rings

**Steps 9–10 · Backgrounds sólidos**  
Step 9 é o step mais puro — maior chroma, menos diluído. Use para: backgrounds de seções, headers, componentes, gráficos, overlays, sombras coloridas, bordas de destaque.  
- Step 9 → estado normal
- Step 10 → hover do Step 9

> ⚠️ A maioria dos Step 9 exige texto **branco** no foreground.  
> Exceções que exigem texto **escuro**: `Sky`, `Mint`, `Lime`, `Yellow`, `Amber`.

**Steps 11–12 · Texto**  
- Step 11 → texto secundário, legendas, placeholders
- Step 12 → texto primário, headings, corpo

> Steps 11 e 12 garantem contraste Lc 60 e Lc 90 (APCA) sobre Step 2 da mesma escala.

---

### Composição da paleta

**Escala de cor de marca / accent**  
Escolha uma escala accent principal.

- Foreground **branco** no Step 9: `Bronze`, `Gold`, `Brown`, `Orange`, `Tomato`, `Red`, `Ruby`, `Crimson`, `Pink`, `Plum`, `Purple`, `Violet`, `Iris`, `Indigo`, `Blue`, `Cyan`, `Teal`, `Jade`, `Green`, `Grass`
- Foreground **escuro** no Step 9: `Sky`, `Mint`, `Lime`, `Yellow`, `Amber`

**Escala de cinza**  
Escolha um cinza e pareie com o seu accent por proximidade de matiz:

| Cinza | Accents naturais |
|-------|-----------------|
| `Gray` | Neutro — funciona com qualquer accent |
| `Mauve` | Tomato, Red, Ruby, Crimson, Pink, Plum, Purple, Violet |
| `Slate` | Iris, Indigo, Blue, Sky, Cyan |
| `Sage` | Mint, Teal, Jade, Green |
| `Olive` | Grass, Lime |
| `Sand` | Yellow, Amber, Orange, Brown |

> ⚠️ Ao usar cinzas saturados como background em dark mode, cuidado com componentes coloridos como `Badge` — podem conflitar.

**Escalas semânticas**

| Papel | Escalas recomendadas |
|-------|---------------------|
| **Error** | `Red`, `Ruby`, `Tomato`, `Crimson` |
| **Success** | `Green`, `Teal`, `Jade`, `Grass`, `Mint` |
| **Warning** | `Yellow`, `Amber`, `Orange` |
| **Info** | `Blue`, `Indigo`, `Sky`, `Cyan` |

**Texto colorido vs. neutro**  
- Steps 11/12 da escala accent → vibe mais colorida (bom para marketing)
- Steps 11/12 da escala cinza → vibe mais funcional (bom para app UI)

**Variantes alpha**  
Cada escala tem versão alpha (ex: `BlueA`, `SlateA`). Use sobre backgrounds coloridos ou transparentes.

**Overlays**  
`Black Alpha` e `White Alpha` são exclusivos para overlays e não mudam entre light/dark mode.

---

### Regras resumidas de cores

1. Sempre use steps semânticos — nunca escolha um step por estética
2. Uma escala accent — defina uma cor de marca e aplique de forma consistente
3. Um cinza — pareie com o hue do seu accent
4. Uma escala por papel semântico (error, success, warning, info)
5. Foreground branco no Step 9, exceto: `Sky`, `Mint`, `Lime`, `Yellow`, `Amber`
6. Dark mode background → alias `AppBg` mapeado para Step 1 ou 2
7. Não customize escalas Radix — adicione escalas customizadas separadas se necessário

---

## 2. Tipografia — Material Design 3

### Type scale (15 tokens)

| Token | Tamanho | Peso | Uso |
|-------|---------|------|-----|
| Display Large | 57px | Regular | Texto curto de grande impacto, numerais. Melhor em telas grandes |
| Display Medium | 45px | Regular | Idem, hierarquia intermediária |
| Display Small | 36px | Regular | Idem, menor escala |
| Headline Large | 32px | Regular | Texto de alta ênfase em telas menores, marcação de seções principais |
| Headline Medium | 28px | Regular | Idem, hierarquia intermediária |
| Headline Small | 24px | Regular | Idem, menor escala |
| Title Large | 22px | Regular | Texto de média ênfase, curto. Divide seções secundárias |
| Title Medium | 16px | Medium | Idem, hierarquia intermediária |
| Title Small | 14px | Medium | Idem, menor escala |
| Body Large | 16px | Regular | Parágrafos e textos longos |
| Body Medium | 14px | Regular | Idem, hierarquia intermediária |
| Body Small | 12px | Regular | Idem, menor escala |
| Label Large | 14px | Medium | Texto dentro de componentes, labels interativos |
| Label Medium | 12px | Medium | Idem, hierarquia intermediária |
| Label Small | 11px | Medium | Idem, menor escala, captions |

### Quando usar cada role

- **Display** → Hero sections, numerais grandes, títulos de splash screens
- **Headline** → Títulos de página, seções primárias, cards de destaque
- **Title** → Subtítulos, headers de seção, toolbars, diálogos
- **Body** → Parágrafos, descrições, conteúdo de leitura
- **Label** → Botões, chips, tabs, badges, captions, texto auxiliar

### Adaptação ao design system do projeto

O projeto usa **Inter** (e **Be Vietnam Pro** para Body) em vez de Roboto. Os roles do M3 se aplicam da seguinte forma:

| Role M3 | Equivalente no projeto |
|---------|----------------------|
| Display | Display (Bold) — Inter Extrabold, 32–72px |
| Headline | Heading — Inter Extrabold/Bold/Semibold, 16–32px |
| Body | Body — Inter Bold/Semibold/Medium/Regular, 12–20px |

---

## 3. Espaçamento — Material Design 3

### Grid base

- **Componentes e layout** → grid de **8dp**. Todos os tamanhos, margens e paddings são múltiplos de 8
- **Tipografia** → grid de **4dp**. Line heights devem ser múltiplos de 4

### Escala de espaçamento

| Token | Valor | Uso típico |
|-------|-------|-----------|
| 4dp | 4px | Espaço mínimo, gap entre ícone e label |
| 8dp | 8px | Gap entre elementos pequenos, padding interno compacto |
| 12dp | 12px | Padding interno de componentes pequenos |
| 16dp | 16px | Padding padrão de componentes, margem lateral de tela |
| 24dp | 24px | Espaço entre grupos de elementos, padding de cards |
| 32dp | 32px | Separação entre seções, espaço vertical entre blocos |
| 48dp | 48px | Altura mínima de touch targets, espaço entre seções grandes |
| 64dp | 64px | Espaços maiores entre seções |

### Regras de touch target

- Tamanho mínimo de touch target: **48 × 48dp**
- Espaço mínimo entre touch targets: **8dp**

### Regras de margem de tela (mobile)

| Elemento | Valor |
|----------|-------|
| Margem lateral (esquerda e direita) | 16dp |
| Conteúdo após ícone ou avatar | 72dp a partir da borda |

### Densidade

Material Design 3 suporta 3 densidades, ajustadas em incrementos de **4dp**:

| Densidade | Altura de componentes |
|-----------|----------------------|
| Default | altura padrão (ex: botão 40dp) |
| Comfortable | −4dp |
| Compact | −8dp |

### Regras resumidas de espaçamento

1. Todo espaçamento de layout e componente é múltiplo de **8dp**
2. Line heights de texto são múltiplos de **4dp**
3. Tamanho mínimo de touch target: **48 × 48dp**
4. Margem lateral de tela mobile: **16dp**
5. Use 4dp como sub-unidade apenas para gaps muito pequenos (ícone ↔ label)
6. Evite valores arbitrários — sempre escolha o múltiplo mais próximo de 4 ou 8
