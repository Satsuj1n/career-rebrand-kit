# Currículos

Versão currículo do rebrand. Espelha o pitch do `linkedin/about.md` e do `github/profile-readme.md`: **Mid-level AI Agent Engineer** (Pleno, em PT-BR) com fundação backend, projetos em destaque (Cosmic Trader, Claude Code Toolkit) e tier explícito de **USD remote contracts**.

## Arquivos

| Source (`.md`) | Output (`.pdf`) | Quando usar |
|---|---|---|
| `resume-en.md` | `resume-en.pdf` | **Padrão** pra recrutador estrangeiro / contratos USD remote em IA. Tipografia profissional, minimalista. |
| `curriculo-pt.md` | `curriculo-pt.pdf` | Aplicações BR minimalistas. Mesma estrutura, prosa em PT-BR, jargão técnico mantido em inglês (`rate limiting`, `circuit breaker`, `agent evals` etc.). |
| `resume-en-ats.md` | `resume-en-ats.pdf` | Quando o ATS (Greenhouse, Workday, Taleo, Lever) for o filtro. Sem Unicode, sem formatação rica, URLs cruas, números com palavras (`10000 plus`, `99.98 percent`). |
| `curriculo-pt-designed.md` | `curriculo-pt-designed.pdf` | Aplicações BR mid-market (Gupy, Solides) onde o visual ajuda. Acentos verdes, accent bar nas seções, skill pills, cargos coloridos. **Não** use pra recrutador internacional de eng/AI — o visual designed contradiz a voz anti-fluff do rebrand. |

Os quatro arquivos são paralelos por desenho — qualquer mudança de conteúdo deve ser refletida em todos.

## Como gerar PDF

Não há build versionado (o repo é content-only por design — ver `CLAUDE.md` da raiz). PDFs estão checados in junto com os `.md` (mesmo padrão de `banner/banner.svg` + `banner/banner.png`).

Pra regenerar:

```bash
# via venv + markdown-pdf (sem deps de sistema)
python3 -m venv /tmp/cv-pdf-venv
/tmp/cv-pdf-venv/bin/pip install markdown-pdf

# script disposable em /tmp/render_cvs.py — recriar conforme necessário
/tmp/cv-pdf-venv/bin/python /tmp/render_cvs.py
```

Alternativas: pandoc + weasyprint (`pandoc resume-en.md -o resume-en.pdf --pdf-engine=weasyprint`), ou colar em Typora/Marked/Obsidian → Export PDF.

## Convenções

- **Featured Projects acima de Experience** — quebra deliberada da ordem clássica de CV. O headline promete "AI Agent Engineer"; o leitor precisa ver a prova logo abaixo. Coco Bambu/iZJob sozinhos não justificam o título — eles são a *fundação*, mostrada em seguida.
- **Bullets de experiência factualmente intactos vs. o currículo original**. Reframar microserviços ou RPA como "agent infrastructure" colapsaria em entrevista. A integridade técnica é a sustentação do rebrand.
- **Sem laundry list de skills**. A stack é ordenada por relevância pro pitch (AI/Agents primeiro), não por tempo de uso. Tech irrelevante pro role-alvo (React Native, Spring, etc.) foi removida — está no GitHub README pra quem quiser cavar.
- **"USD remote" aparece duas vezes** — no header e em "What I'm looking for". Proposital, mesma calibragem do `linkedin/about.md`.

## Branch hygiene

Esses arquivos contêm dados pessoais reais (nome, email, projetos). São válidos pra `main` (case study). Antes de portar pra `template`, substituir:

- `Felipe Campello D'Albuquerque Lima` → `[YOUR_NAME]`
- `felipenehz2003@gmail.com` → `[YOUR_EMAIL]`
- `(61) 99286-4664` → `[YOUR_PHONE]`
- `Brasília` / `Brasília, DF` → `[YOUR_CITY]`
- `felipecampellolima` → `[YOUR_LINKEDIN_SLUG]`
- `Satsuj1n` → `[YOUR_GITHUB]`
- `Cosmic Trader` → `[YOUR_PROJECT_1]`
- `Claude Code Toolkit` → `[YOUR_PROJECT_2]`
- `Coco Bambu Restaurante`, `iZJob`, `Universidade de Brasília` → genéricos `[COMPANY_1]`, `[COMPANY_2]`, `[UNIVERSITY]`

Ver `CLAUDE.md` da raiz pra a regra completa do modelo de duas branches.
