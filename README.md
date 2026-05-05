# Career Rebrand Kit

> Um kit prático pra desenvolvedor brasileiro se reposicionar como **AI Agent Engineer** e fechar contratos remotos em **USD**.

Esse repo é um *case study + framework*. Eu (Felipe) usei isso pra reposicionar meu próprio perfil de "full stack genérico" pra "AI Agent Engineer com produção rodando". As peças aqui são as que eu apliquei. Você pode forkar, adaptar e usar.

---

## Por que isso existe

Boa parte de dev brasileiro com 3-5 anos de experiência ganha entre R$8k e R$15k/mês trampando pra empresa nacional. A mesma stack, posicionada pra mercado internacional como contractor USD, vale **2 a 4 vezes mais**. O gargalo raramente é técnico — é posicionamento, portfolio público, e canal de aplicação.

Esse kit ataca os três:

- **Posicionamento**: headline, About do LinkedIn, GitHub README, banner
- **Portfolio público**: estrutura de repos que conta tua história ao invés de só listar tech
- **Canal**: roadmap de plataformas, gaps de aprendizado pra fechar antes de aplicar

Foco específico: **AI Agent Engineering** — porque é o nicho mais quente em 2026 e tem assimetria boa (demanda alta, oferta baixa de gente que entende produção, não só tutorial de RAG).

---

## Estrutura

```
career-rebrand-kit/
├── README.md                    # você está aqui
├── SETUP.md                     # checklist pra customizar pra ti
├── LICENSE                      # MIT
│
├── linkedin/
│   ├── headline.md              # a linha sob o nome
│   ├── about.md                 # a bio longa (campo About)
│   ├── short-pitch.md           # versão curta pra DM/email
│   └── audit-prompt-claude-code.md  # prompt pra Claude Code + Playwright MCP auditar e atualizar teu LinkedIn automaticamente
│
├── github/
│   ├── profile-readme.md        # o README do repo especial <user>/<user>
│   └── username-ideas.md        # se tu tá pensando em trocar o handle
│
├── banner/
│   ├── banner.svg               # banner LinkedIn (vetorial, editável)
│   ├── banner.png               # banner LinkedIn (1584×396, pronto pra subir)
│   └── image-gen-prompts.md     # prompts pra gerar versão foto-realista no Midjourney/Bing/Leonardo
│
└── strategy/
    ├── 7-month-roadmap.md       # plano mês a mês: posicionamento → pipeline → transição
    └── platforms.md             # Turing, Toptal, Arc.dev, Lemon.io, Braintrust + táticas de cold outreach
```

---

## Quick start

1. Lê o [`SETUP.md`](./SETUP.md) — checklist de customização.
2. Lê [`strategy/7-month-roadmap.md`](./strategy/7-month-roadmap.md) — entenda o plano antes de mexer nas peças.
3. Adapta os arquivos de `linkedin/` e `github/` com teus dados.
4. Sobe o banner novo no LinkedIn e o README novo no GitHub.
5. Roda o [`linkedin/audit-prompt-claude-code.md`](./linkedin/audit-prompt-claude-code.md) no Claude Code pra automatizar a aplicação no LinkedIn.
6. Começa a aplicar nas plataformas listadas em `strategy/platforms.md`.

---

## Quem isso serve

- Dev brasileiro com **2+ anos** de experiência sólida em backend (Python/Node/Java/Go)
- Inglês ao menos intermediário (precisa pra entrevista técnica em inglês)
- Já mexeu com APIs de LLM, ou tem vontade de mexer e construir agente de verdade
- Tem 4-6 meses de runway pra transição (não vai virar overnight)

**Não serve** se você:

- Tá começando agora em programação
- Quer "trabalhar com IA" mas não construiu nada além de chatbot tutorial
- Espera resultado em 30 dias

---

## Case study

Esse kit nasceu da minha própria transição. Os arquivos aqui são as versões finais que apliquei no meu perfil. Não invento — uso. Se quiser ver o contexto de cada decisão, lê os comentários inline em cada arquivo.

Meu perfil: [github.com/[YOUR_GITHUB]](https://github.com/[YOUR_GITHUB])

---

## Contribuir

Se você usar isso e funcionar (ou não), abre uma issue compartilhando o que aprendeu. Esse kit fica melhor com mais cases.

PR também são bem-vindos pra:

- Tradução pra outras línguas
- Adicionar templates pra outros nichos (ML engineering, DevOps, security)
- Listar mais plataformas

---

## License

MIT. Forka, modifica, publica versão própria. Só não vende kit pago baseado nisso (rola karma ruim).
