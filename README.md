# cockpit-skills

Monorepo das **9 skills** do **Cockpit** — stack de IA pra agências de tráfego.

> Skill mestra (instalador): https://github.com/matheusmja1998-droid/cockpit-init

## As 9 skills

| Skill | Função | Status | Tier mínimo |
|---|---|---|---|
| `cockpit-onboarding` | Onboarda cliente novo (pasta, dossiê inicial, acessos, contrato) | ✅ | Kick R$497 |
| `cockpit-dossie` | Cria/completa dossiê do cliente via entrevista + pesquisa automática | ✅ | Kick R$497 |
| `cockpit-meta` | Gestão Meta Ads (Facebook/Instagram) por linguagem natural | ✅ | Kick R$497 |
| `cockpit-watch` | Monitor 24/7 Meta Ads. Alertas Telegram via n8n | ✅ | Install R$997 |
| `cockpit-track` | Tracking server-side via Cloudflare (Meta CAPI + GA4) | 🚧 | Install R$997 |
| `cockpit-google` | Gestão Google Ads por linguagem natural | 🚧 | Install R$997 |
| `cockpit-debrief` | Análise pós-campanha em 5 min (cruza Meta + planilhas) | ✅ | Install R$997 |
| `cockpit-report` | Relatório semanal automatizado (Meta + CRM + atividades) | ✅ | Install R$997 |
| `cockpit-creative` | Gera 10 criativos de imagem por demanda (Schwartz + Hormozi + compliance) | ✅ | Install R$997 |

## Como instalar

Skill individual:
```bash
npx skills add https://github.com/matheusmja1998-droid/cockpit-skills --skill cockpit-meta
```

Todas via instalador mestre (recomendado):
```bash
npx skills add https://github.com/matheusmja1998-droid/cockpit-init
# depois rodar /cockpit-init no Claude Code
```

## Esteira de produtos

```
COCKPIT KICK     R$497    Setup + 3 skills (Onboarding, Dossiê, Meta)
COCKPIT INSTALL  R$997    Stack completa (9 skills)
COCKPIT OPERATION R$1.997 Stack + Cockpit Brain (Obsidian) + 1 cliente real
COCKPIT BLACK    R$3.997  Operação inteira da agência redesenhada + SOPs
```

## Continuidade

```
COCKPIT MANUTENÇÃO  R$297/mês   Atualizações + comunidade
COCKPIT GESTÃO      R$697/mês   Servidor gerenciado + suporte direto
COCKPIT WHITE-LABEL R$5.000/mês Backend completo (WinVision opera tudo)
```

## Autor

Matheus Jardim — WinVision / L.M Agência

## Licença

Privado.
