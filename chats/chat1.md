# Remoções MAIA

_Started 2026-05-07 00:51 UTC_

---

## User



## Assistant

I'll start by exploring the MAIA Clay Design System to understand the tokens and components available.

_[tool: list_files]_

_[tool: read_file]_

Now let me peek at marketing UI kit and key previews.

_[tool: list_files]_

_[tool: read_file]_

Let me view several key components and previews in parallel.

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

I have a great handle on the design system now. Let me build the MAIA institutional website. I'll structure it as a single HTML file using the marketing UI kit's patterns.

_[tool: copy_files]_

I have what I need. Let me snip the design system exploration outputs and build the site.

_[tool: snip]_

Now let me build the MAIA website. Single HTML file with inline CSS/JS, vanilla JS (no React needed for an institutional site — keeps it lightweight, more editable).

_[tool: write_file]_

_[tool: done]_

_[tool: snip]_

_[tool: fork_verifier_agent]_

Built the MAIA institutional website as a single deployable HTML file. Highlights:

- **Cream canvas + saturated cards** following the MAIA Clay design system (no gradients/shadows; depth from color contrast)
- **Sticky blurred navbar** with scroll-triggered border + active link tracking
- **Hero** with claymation-style SVG scene, tilted phone mockup showing the app, and floating notification cards
- **Social proof bar** in dark ink (the only dark surface — used for emphasis)
- **Como Funciona** as a pink/teal split with numbered steps for each audience
- **Para Talentos / Para Diretores** alternating splits, each with a custom illustrated mockup (profile cards / casting pipeline)
- **Planos** with the annual plan elevated in dark ink + "Mais popular" pink tag
- **Parceiros** featuring Wolf Maya prominently with placeholders for future partners
- **FAQ** accordion (8 questions covering pricing, LGPD, casting flow, minors, commission)
- **Footer** in cream surface-soft (per the system's "no dark footer" rule)

All copy in Brazilian Portuguese, "você" throughout, semantic HTML5, full SEO meta tags, mobile-responsive with burger menu, scroll reveal animations, no external deps beyond the Inter font.

## User

Verifier agent check completed

## Assistant

Let me fix the reveal animation issue. The IntersectionObserver isn't firing reliably for above-the-fold elements.

_[tool: str_replace_edit]_

_[tool: snip]_

_[tool: done]_

_[tool: fork_verifier_agent]_

Fixed the reveal-on-load issue: above-the-fold content now reveals immediately on page load, while below-the-fold elements still fade in via IntersectionObserver as you scroll, with a 1.5s safety-net timeout to guarantee nothing stays hidden.

## User

Vamos remover:

1. Em parceria com Wolf Maya no Hero
2. Vamos retirar a seção (Ver Anexo 1)
3. Vamos retira a seção de Parceiros
4. Vamos retirar do FAQ, as perguntas: Como vocês verificam os talentos?, Como funciona o processo de casting?, Posso usar a MAIA sendo menor de idade?
5. Vamos retirar os icones de Instagram e LinkedIn no rodapé

## Assistant

_[tool: read_file]_

_[tool: snip]_

_[tool: grep]_

Now let me read the relevant sections to make precise edits.

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: snip]_

_[tool: str_replace_edit]_

_[tool: done]_

_[tool: snip]_

Pronto. Removi:

1. ✅ Eyebrow "Em parceria com Wolf Maya" do Hero
2. ✅ Barra de social proof (7.000+ / Wolf Maya / R$ 32,7 bi)
3. ✅ Seção inteira de Parceiros
4. ✅ Três FAQs (verificação, processo de casting, menor de idade) — restaram 5 perguntas
5. ✅ Ícones Instagram e LinkedIn do rodapé

## User

No rodapé, ao clicar em imprensa, abra o email, assim como o botão de contato faz.

Vamos adicionar o CNPJ no footer, ao lado do nome da empresa: 66.318.397/0001-72.

Vamos criar as telas para as politicas de Privacidade, Termos de Uso e LGPD (Ver anexos)

## Assistant

_[tool: read_file]_

_[tool: read_file]_

_[tool: read_file]_

I'll create a shared CSS file and three legal pages styled with the MAIA design system, then update the footer.

_[tool: snip]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

Now let me update the main site footer to wire the new pages, add CNPJ, and make Imprensa open email.

_[tool: grep]_

_[tool: snip]_

_[tool: str_replace_edit]_

_[tool: done]_

Pronto:

- ✅ **Imprensa** agora abre `mailto:imprensa@plataformamaia.com`
- ✅ **CNPJ 66.318.397/0001-72** adicionado ao copyright do rodapé
- ✅ **Três páginas legais** criadas (`politica-de-privacidade.html`, `termos-de-uso.html`, `lgpd.html`) com a identidade MAIA — display Inter, canvas creme, accent rosa, cards de direitos LGPD em grid
- ✅ Links do rodapé do site principal apontando para as novas páginas
- ✅ Cada página legal tem nav slim "Voltar ao site" + footer com cross-links e CNPJ

