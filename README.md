# Valida SICONFI — Design System

Sistema de design reconstruído a partir do arquivo Figma **"Projeto Siconfi"** (montado como filesystem virtual). O foco principal é replicar fielmente o frame **Hero [Landing]** (1600 × 6150) que apresenta o produto **Validador SICONFI**.

## Sobre o produto
**Validador SICONFI** é uma ferramenta independente que valida arquivos contábeis (MSC, DCA, RREO, RGF) **antes** do envio ao SICONFI. Roda 162 verificações organizadas em 4 dimensões — D1 (Entrega), D2 (Cobertura), D3 (...) e D4 (...) — e produz um relatório com referência normativa para correção.

- **Público:** prefeituras, contadores e equipes fazendárias municipais (5.500+ municípios no Brasil).
- **Promessa:** "Evite perder pontos no CAPAG por erros que podem ser prevenidos."
- **Velocidade:** menos de 1 minuto da MSC ao diagnóstico.

## Fontes consultadas
- Figma virtual: `/Design-LP/Hero-Landing/index.jsx` (frame `13:23792`)
- `/Componentes/components/Property1Default/...` (band da imagem do dashboard)
- `/Componentes/Logo-Azul/`, `/Componentes/Logo-Branco/`
- `/METADATA.md` (paleta + uso de fontes)

## Index
- `Hero [Landing].html` — replica completa do frame Hero [Landing]
- `colors_and_type.css` — tokens de cor + tipografia
- `assets/` — logos, imagens e marcas extraídas do Figma
- `preview/` — cards do Design System tab
- `SKILL.md` — manifesto cross-compatível (Agent Skills)

## Content Fundamentals
- **Idioma:** Português do Brasil. Não traduzir nomes técnicos (CAPAG, SICONFI, MSC, DCA, RREO, RGF, D1–D4).
- **Tom:** institucional-acessível, direto, sóbrio. Sem gírias publicitárias. Foco em risco evitado (perder pontos no CAPAG) e em controle ("envie com segurança").
- **Pessoa:** 2ª pessoa implícita ("Evite", "envie", "corrija"). A marca fala em 1ª pessoa do plural quando aparece ("Nossa equipe mostra como funciona").
- **Caixa:** títulos em caixa-baixa com inicial maiúscula. Eyebrows/pills em **CAIXA ALTA** curta ("O PROBLEMA", "FLUXO") ou caixa-baixa curta ("prova social", "próximo passo") — convivem.
- **Pontuação:** ponto final em headlines compridas ("Evite perder pontos no CAPAG por erros que podem ser prevenidos."). Travessão em em-dash para separação ("D1 — Entrega", "2026 Valida SICONFI — Todos os direitos reservados").
- **Números:** "5.500+", "< 1 min", "162", "57" — usar prefixos e separadores brasileiros.
- **Sem emojis.**
- **Exemplos:**
  - Headline: *"Evite perder pontos no CAPAG por erros que podem ser prevenidos."*
  - Sub: *"O ValidaSICONFI roda as verificações D1, D2, D3 e D4 nos seus arquivos antes do envio e entrega um relatório completo para você corrigir com segurança."*
  - Eyebrow: *"O PROBLEMA"*, *"FLUXO"*, *"prova social"*

## Visual Foundations
- **Cores primárias:** azul de marca `#2E61FF` (rgb 46/97/255) sobre branco. Tints suaves (`#EAEFFF`, `#E0E7FF`) para bandas e ícones. Textos em `#171717` (heading), `#5C5C5C` (corpo), `#6A7282` (meta), `#A3A3A3` (legenda).
- **Tipografia:** Inter Tight (display, 32–56px) + Inter (corpo, 12–16px) + Roboto Bold para o wordmark + Consolas/JetBrains Mono para códigos de verificação ("D1.04", "D1.05"). Tracking levemente negativo nos títulos (`-0.010em`) e no corpo (`-0.011em`).
- **Backgrounds:** brancos predominantes; uma banda de azul tint (`#EAEFFF`) com uma silhueta côncava esculpida no topo (forma do "navegador") destaca o card do produto. Imagens com **gradient overlay azul-para-transparente** no topo. Padrões decorativos: **diamond grids** com `opacity: 0.1` flanqueando o herói; **checker pattern** rotacionado na CTA azul.
- **Cards:** raio `24–28px`, sombra muito sutil em camadas (`shadow-card` empilha 5 níveis com cor `rgba(23,23,23,0.04)`). Sobre fundo azul `rgba(46,97,255,0.1)` para a "elevação branda" do mock.
- **Pills/badges:** raio `9999px`/`50px`, fundo branco-quente `#FEFEFF`, borda `#EAEFFF`, sombra `shadow-xs`. Sobre o azul de marca, viram outline transparente com texto branco.
- **Botões:** raio `8px`, altura `40px`. 4 variantes: Filled azul, Stroke neutro, Lighter (branco em fundo azul), Dark (ink quase preto `#0E121B`). Hover: escurece levemente o fill (`#335CFF`) ou adiciona tint suave.
- **Status:** verde escuro `#007A55` + fundo `#ECFDF5` (passou); vermelho `#C10007` + fundo `#FEF2F2` (reprovou); âmbar `#F6B51E` (alerta).
- **Bordas:** `1px` em `#EBEBEB`/`#E5E7EB`/`#F3F4F6`. Dividers entre stats são verticais finos.
- **Espaçamento:** padding lateral macro de **188px** nas seções principais; max-width interno 1224px. Gaps de seção: 80–96px verticais.
- **Animação:** sutil. Transições de 120ms ease em estados de hover; nenhuma animação obrigatória.
- **Transparência/blur:** botões over-image usam `rgba(255,255,255,0.16)` + `backdrop-filter: blur(4px)`. Overlays de imagem em testemunho usam degradê preto leve com blur.

## Iconography
- **Sistema:** o Figma referencia **Remix Icon** (`arrow-right-up-line`, `shield-line`, `shield-check-line`, `shield-user-line`, `swap-2-line`, `settings-6-line`, `equalizer-2-line`, `file-download-line`, `checkbox-circle-fill`, `instagram-fill`, `twitter-x-line`, etc.). Linha de 1.5–2px, cantos arredondados. Sem ícones preenchidos pesados.
- **Substituição:** os SVGs do Remix não foram extraídos no momento — usamos **inline SVGs equivalentes** (mesmo peso visual) no Hero [Landing].html. **Recomendado:** instalar `remixicon` via CDN `https://cdn.jsdelivr.net/npm/remixicon@4.2.0/fonts/remixicon.css` e trocar inline → `<i class="ri-shield-line"></i>`.
- **Sem emoji.**
- **Logos:** símbolo "S" estilizado em azul (`assets/logo-mark-blue.svg`) e branco (`assets/logo-mark-white.svg`). Acompanhado do wordmark "Validador SICONFI" em Roboto Bold 16px, cor `#032952`.

## Caveats
- O Figma usa Inter, Inter Tight (Display), Roboto e Consolas. **Inter Tight** foi mapeado para "Inter Display"/"Inter Variable" do Figma; **JetBrains Mono** substitui Consolas para web. Confirme se a fonte oficial é Consolas mesmo ou se há intenção de migrar.
- Os ícones Remix não foram baixados — substituídos por SVGs inline equivalentes. Para fidelidade total: instalar `remixicon`.
- O frame original é uma página única vertical de 6150 px. O HTML usa transform-scale para caber em viewports menores.
