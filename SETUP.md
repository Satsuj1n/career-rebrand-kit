# SETUP — How to customize this kit for yourself

Esse kit foi escrito como case study (caso do Felipe). Pra adaptar pra ti, segue esse checklist.

---

## 1. Diagnóstico honesto antes de tudo (15 min)

Pega papel ou um doc e responde:

- **Qual minha stack real?** Liste linguagens/frameworks que você usou em produção, não em curso.
- **Qual meu inglês de verdade?** Se você não consegue passar 30 min de entrevista técnica em inglês falando alto, esse é o gargalo #1. Resolve antes de mexer no resto.
- **Qual projeto público meu mostra produção, não tutorial?** Se a resposta é "nenhum", esse é o trabalho real. Os arquivos do kit não substituem isso.
- **Quanto runway eu tenho?** Quantos meses você consegue sustentar a transição se ela demorar 4-6 meses (que é o normal)?
- **Qual nicho eu vou ocupar?** Esse kit é otimizado pra **AI Agent Engineering**. Se você quer outra direção (ML, DevOps, security, mobile sênior), o framework serve mas as palavras-chave mudam.

Se algum desses respondeu "tô atrás", trata isso primeiro. Não adianta polir LinkedIn com inglês ruim ou portfolio vazio.

---

## 2. Customizar `linkedin/headline.md`

Substitui o nicho se for diferente. Mantém:

- A categoria principal logo no início (recrutador busca por job title)
- O sinal de "Open to USD remote" no final — é o filtro mais importante pra recrutador estrangeiro

---

## 3. Customizar `linkedin/about.md`

Vai precisar mexer principalmente em:

- **Hook (primeiras 2 linhas)**: substitui pelo teu pitch. Mantém o padrão "eu construo X. Foundation em Y, agora aplicando em Z."
- **What I'm shipping**: lista 3 projetos teus, com 1 linha de arquitetura cada. Se você não tem 3 projetos públicos, esse é o trabalho real antes de subir esse About.
- **Stack**: ajusta com a tua.
- **Take pessoal**: a frase "agents are software, not just a clever prompt" funciona pro Felipe porque é coerente com o restante. Escreve uma tua, opinativa, específica do teu nicho.

**Anti-checklist** (coisas pra NÃO fazer):

- Não usa "passionate", "results-driven", "team player" — palavras vazias que recrutador filtra mentalmente.
- Não lista 30 skills. Top 5-8 que você realmente tem profundidade.
- Não escreve em inglês corporativo enferrujado. Lê em voz alta — se soa robótico, reescreve.

---

## 4. Customizar `github/profile-readme.md`

- Substitui meu nome, links, projetos
- A seção `## What I'm shipping` precisa apontar pra repos que **existam e estejam públicos**. Mentir aqui é tiro no pé — recrutador clica e vê.
- Os projetos referenciados (Cosmic Trader, Claude Code Toolkit) são meus. Substitui pelos teus ou remove a seção.

Esse README vai num repo especial chamado `<seu-username>/<seu-username>`. Se ainda não tiver, cria o repo com esse nome exato e adiciona o `README.md` na raiz.

---

## 5. Customizar `banner/banner.svg`

O banner é vetorial. Pra editar:

- Abre em qualquer editor SVG (Figma, Inkscape, ou direto no VS Code)
- Cores: troca `#70A5FD` (azul principal) e `#06b6d4` (cyan) pelas suas
- Pra regerar o PNG depois de editar, roda:

```bash
pip install cairosvg
python3 -c "import cairosvg; cairosvg.svg2png(url='banner.svg', write_to='banner.png', output_width=1584, output_height=396)"
```

Se quiser versão foto-realista (gerada com Midjourney/Bing/Leonardo), olha [`banner/image-gen-prompts.md`](./banner/image-gen-prompts.md).

---

## 6. Customizar `strategy/`

- `7-month-roadmap.md` é um calendário. Os meses são relativos — começa do mês 1 = agora.
- `platforms.md` lista plataformas que aceitam dev offshore. Confere se ainda tão ativas e adiciona/remove conforme tua experiência.

---

## 7. Rodar o audit prompt no Claude Code (opcional, mas recomendado)

Se você usa Claude Code com Playwright MCP, [`linkedin/audit-prompt-claude-code.md`](./linkedin/audit-prompt-claude-code.md) automatiza a aplicação das mudanças no LinkedIn. Lê o arquivo antes de rodar — tem hard rules importantes pra LinkedIn não te flaggar.

---

## 8. Antes de publicar tua versão

Checklist final:

- [ ] Substitui meu nome, email, GitHub, LinkedIn em todos os arquivos
- [ ] Confere que os projetos referenciados existem e estão públicos
- [ ] Lê o About em voz alta em inglês — soa fluido?
- [ ] Banner sobe no LinkedIn e a foto de perfil + headline ficam bem por cima?
- [ ] Headline tem palavras-chave que recrutador buscaria? (ex.: "AI Engineer", "Python", "Remote")
- [ ] Open to Work configurado em "recruiters only" (não público)?

---

## 9. Fork e compartilha

Se você adaptou e funcionou, considera:

- Forkar esse repo, customizar, e tornar público com teu nome
- Abrir issue no original compartilhando o que mudou no teu caso
- Mandar PR com melhorias no framework

Quanto mais cases públicos, mais útil o kit fica.
