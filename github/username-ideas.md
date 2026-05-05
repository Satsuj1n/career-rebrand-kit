# GitHub Username Ideas

Se você tá pensando em trocar handle pra algo mais profissional ou alinhado com pitch, considera:

---

## Critérios pra um bom username de dev

- **Pronunciável em inglês** — recrutador vai falar em call
- **Reconhecível ao lado do nome real** — facilita recrutador buscar você
- **Curto** — cabe melhor em badges, emails, links
- **Não-temático demais** — `quantumcoder42` envelhece mal
- **Disponível em GitHub, LinkedIn (URL), Twitter/X**

---

## Padrões que funcionam

| Padrão | Exemplo (genérico) | Quando usar |
|---|---|---|
| `<firstname><lastname>` | `johnsmith` | Você tem nome curto e disponível |
| `<firstname>-<lastname>` | `john-smith` | Hifenizado costuma estar disponível mesmo quando junto não está |
| `<initial><lastname>` | `jsmith`, `j-smith` | Nome longo + sobrenome curto |
| `<firstname><role>` | `johndev`, `johnbuild` | Quer sinalizar profissão |
| `<firstname><domain>` | `johnai`, `johnml` | Forte commit a nicho |

---

## Coisas pra evitar

- ❌ Números aleatórios: `dev_42`, `john1985`
- ❌ Misturar idiomas: `desenvolvedordev`
- ❌ Referências a personagens copyrighted (mesmo que pareça óbvio que não é literal): `tonyStark`, `silverSurfer`, `darthVader`
- ❌ Abreviações que ninguém fala: `xX_jhn_Xx`
- ❌ Letras trocadas por números cheap: `c0d3r`, `h4ck3r`

---

## Antes de migrar

1. **Confere disponibilidade** em GitHub, LinkedIn URL slug, Twitter/X
2. **Avisa colaboradores** — commits antigos ainda referenciam o handle antigo em alguns lugares
3. **Atualiza** SSH keys, email vinculado, perfil README badges
4. **GitHub redireciona** repos antigos por um período, mas links externos quebram. Atualiza CV, bio do Twitter, qualquer place onde tu citou o repo

---

## Como GitHub trata mudança de username

- Repos antigos ficam acessíveis via redirect por algum tempo
- Issues, PRs, commits permanecem associados ao username antigo até você atualizar git config local
- Stats e contribuições não são afetadas
- O perfil README tem que ser movido pro novo repo `<new-username>/<new-username>`

Detalhes oficiais: confere a doc do GitHub sobre changing username (regras mudam, melhor ler na fonte).
