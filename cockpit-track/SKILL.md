---
name: cockpit-track
description: Configura tracking server-side via Cloudflare Workers, enviando eventos pra Meta Conversions API (CAPI) e GA4 Measurement Protocol. Resolve gap de iOS 17+ que ferra o pixel padrão. Sobe Worker no domínio do cliente, recebe eventos de site, dispara pra Meta CAPI e GA4. Use quando o usuário disser "configurar tracking", "server-side", "CAPI", "Cloudflare track", "/cockpit-track setup", "tracking iOS 17", ou "resolver tracking quebrado". Disponível a partir do Cockpit Install (R$997).
---

# /cockpit-track — Tracking Server-Side via Cloudflare

## Status

🚧 **Em construção.** Placeholder pra integração com `cockpit-init` no tier Install.

## O que vai fazer

1. Pedir credenciais Cloudflare (API token, Account ID, Zone ID)
2. Pedir tokens Meta CAPI e GA4 (Measurement ID, API Secret)
3. Gerar Cloudflare Worker JavaScript pré-configurado
4. Subir Worker via API do Cloudflare
5. Configurar rota `track.[domínio]/*` → Worker
6. Gerar snippet pro cliente colar no `<head>` do site
7. Rodar evento de teste e validar recebimento em ambos (Meta + GA4)

## Comandos

```
/cockpit-track setup           # Configuração inicial completa
/cockpit-track adicionar [dominio]  # Adiciona novo domínio
/cockpit-track testar          # Dispara evento de teste
/cockpit-track auditar         # Compara eventos pixel vs server-side (gap report)
```

## Variáveis de ambiente

```bash
CLOUDFLARE_API_TOKEN=
CLOUDFLARE_ACCOUNT_ID=
CLOUDFLARE_ZONE_ID=
META_PIXEL_ID=
META_CAPI_TOKEN=
GA4_MEASUREMENT_ID=
GA4_API_SECRET=
```

## Próximos passos (a implementar)

- [ ] Template do Worker JavaScript em `templates/worker.js`
- [ ] Script de upload via API Cloudflare em `scripts/upload-worker.js`
- [ ] Validador de gap (pixel vs server-side) em `scripts/audit.js`
- [ ] Documentação dos eventos suportados (`page_view`, `lead`, `purchase`, etc)
