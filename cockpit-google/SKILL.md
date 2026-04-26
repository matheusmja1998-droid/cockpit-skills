---
name: cockpit-google
description: Gerencia campanhas Google Ads via API oficial. Lê campanhas, conjuntos, anúncios, palavras-chave, públicos. Cria, edita, pausa, duplica e deleta objetos. Configura conversões. Edita lances e orçamentos por comando de linguagem natural. Use quando o usuário disser "google ads", "campanha google", "search ads", "performance max", "/cockpit-google", "pausar google", "criar campanha google". Disponível a partir do Cockpit Install (R$997).
---

# /cockpit-google — Gestão de Google Ads por Linguagem Natural

## Status

🚧 **Em construção.** Placeholder pra integração com `cockpit-init` no tier Install.

## O que vai fazer

Mesma lógica da `cockpit-meta` (Meta Ads), mas pro Google Ads:

- Listar campanhas, ad groups, anúncios, palavras-chave
- Pausar/ativar por critério ("pausa palavras com CPA > R$50")
- Duplicar campanha trocando público/lance
- Editar orçamento e lance
- Adicionar/remover negativas
- Criar Performance Max
- Configurar conversões importadas
- Buscar insights (CPA, CPC, ROAS, conversões)

## Comandos

```
/cockpit-google setup              # Configuração inicial
/cockpit-google listar campanhas
/cockpit-google pausar [critério]
/cockpit-google duplicar [campanha]
/cockpit-google editar [campanha]
/cockpit-google insights [periodo]
```

## Pré-requisitos

- **Conta Google Ads** com acesso admin
- **MCC (Manager Account)** criada
- **Developer Token** aprovado (24-48h de espera após solicitação)
- **OAuth Client** criado no Google Cloud Console
- **Refresh Token** gerado (script auxiliar fornecido)

## Variáveis de ambiente

```bash
GOOGLE_ADS_CUSTOMER_ID=
GOOGLE_ADS_DEVELOPER_TOKEN=
GOOGLE_OAUTH_CLIENT_ID=
GOOGLE_OAUTH_CLIENT_SECRET=
GOOGLE_ADS_REFRESH_TOKEN=
```

## Próximos passos (a implementar)

- [ ] SDK base com `google-ads-api` (npm) ou `google-ads-python`
- [ ] Script `scripts/get-refresh-token.js` (OAuth flow interativo)
- [ ] Mapeamento de comandos naturais → API calls
- [ ] Templates de query (GAQL) pra insights
- [ ] Validações de compliance (políticas Google Ads)
- [ ] Suporte a Performance Max e Demand Gen
