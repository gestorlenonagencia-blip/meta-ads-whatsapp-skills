# Meta Ads + WhatsApp Cloud API — Claude Skills (pt-BR)

Skills para o [Claude](https://claude.com) operar **Meta Ads** e o **WhatsApp oficial (Cloud API)** com segurança, escritas em português para agências e pequenos negócios brasileiros, principalmente clínicas de saúde e estética.

Elas nasceram do uso diário numa agência de tráfego que gerencia dezenas de contas de anúncio. Cada skill descreve, passo a passo, quais ferramentas dos MCPs oficiais da Meta chamar, em que ordem, e quais armadilhas evitar.

> **English:** Claude Skills (in Brazilian Portuguese) for safely operating Meta Ads and the official WhatsApp Cloud API through Meta's MCP servers. Built from daily use at a performance-marketing agency serving health and aesthetics clinics in Brazil. Read-first by default: every write is previewed and requires explicit user approval. Includes LGPD (Brazil's data-protection law) guardrails for customer lists.

## Princípios

- **Ler antes de escrever.** Toda alteração é mostrada antes e só acontece com o OK explícito do usuário.
- **Nada vai ao ar sozinho.** Campanhas são criadas em rascunho ou pausadas.
- **LGPD.** Dados de pacientes não saem do servidor; listas só com base legal, hash e sem dado de saúde.
- **Credenciais fora do chat.** Tokens e segredos ficam no `.env`, nunca em notas ou memória.

## Skills

| Skill | O que faz |
|---|---|
| [`meta-mcp`](skills/meta-mcp/SKILL.md) | Índice: qual skill usar e as regras gerais |
| [`ads-auditoria`](skills/ads-auditoria/SKILL.md) | Auditoria só leitura de todas as contas de anúncio |
| [`ads-diagnostico-cliente`](skills/ads-diagnostico-cliente/SKILL.md) | Raio-x de uma conta: métricas, tendência, benchmark, erros |
| [`ads-concorrencia`](skills/ads-concorrencia/SKILL.md) | Pesquisa na Biblioteca de Anúncios |
| [`ads-montar-campanha`](skills/ads-montar-campanha/SKILL.md) | Monta campanha em rascunho → prévia → OK → publicar |
| [`ads-publicos`](skills/ads-publicos/SKILL.md) | Públicos personalizados e lookalike com portão de LGPD |
| [`ads-sinal-conversao`](skills/ads-sinal-conversao/SKILL.md) | Saúde do pixel/dataset, CAPI e EMQ |
| [`ads-experimentos`](skills/ads-experimentos/SKILL.md) | Testes A/B e estudos de lift |
| [`wa-diagnostico`](skills/wa-diagnostico/SKILL.md) | Diagnóstico do WhatsApp oficial de uma BM |
| [`wa-numero`](skills/wa-numero/SKILL.md) | Adicionar, verificar e registrar número na Cloud API |
| [`wa-templates`](skills/wa-templates/SKILL.md) | Templates de mensagem (biblioteca primeiro, categoria certa) |
| [`wa-webhook`](skills/wa-webhook/SKILL.md) | Configurar e testar o webhook |
| [`wa-envio-teste`](skills/wa-envio-teste/SKILL.md) | Mensagem de teste, uma por vez, com confirmação |
| [`meta-app-saude`](skills/meta-app-saude/SKILL.md) | Conformidade, rate limit e depreciações dos apps Meta |

## Requisitos

- Claude Code ou Claude Desktop.
- Conectores MCP oficiais da Meta: Meta Ads, WhatsApp Business e Meta Developer Tools.

## Instalação

Copie as pastas de `skills/` para `~/.claude/skills/`:

```bash
git clone https://github.com/gestorlenonagencia-blip/meta-ads-whatsapp-skills.git
cp -r meta-ads-whatsapp-skills/skills/* ~/.claude/skills/
```

No Windows (PowerShell):

```powershell
Copy-Item .\meta-ads-whatsapp-skills\skills\* "$env:USERPROFILE\.claude\skills\" -Recurse
```

## Contribuindo

Issues e pull requests são bem-vindos, especialmente correções quando a Meta muda uma API ou ferramenta MCP.

## Licença

[MIT](LICENSE)
