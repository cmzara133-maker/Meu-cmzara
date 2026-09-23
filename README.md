# Meu-cmzara

Repositório com a skill de **copywriting** para o Claude Code.

Com ela instalada, qualquer sessão do Claude aberta neste projeto passa a operar como
especialista em copy: pesquisa de público, escolha de ângulo, estrutura, escrita,
revisão e checagem de promessas antes de entregar.

## Como usar

Abra o Claude Code na raiz deste repositório e peça o que precisa em linguagem normal:

```
escreve um anúncio pro Instagram do meu curso de confeitaria
melhora esse e-mail de proposta que eu mandei pro cliente
por que essa landing page não está convertendo?
preciso de 5 títulos melhores pra esse artigo
```

A skill é acionada sozinha quando o texto tem objetivo de convencer alguém a comprar,
clicar, se inscrever ou responder. Para forçar, use `/copywriting`.

Quanto mais contexto você der — produto, preço, público, prova, canal — melhor a peça.
O template `.claude/skills/copywriting/assets/briefing.md` lista tudo que ajuda.

## O que tem dentro

```
.claude/skills/copywriting/
├── SKILL.md                  fluxo de trabalho e regras de escrita
├── references/
│   ├── voz.md                inventário de voz da marca e regra do espelho
│   ├── pesquisa.md           níveis de consciência, sofisticação, voz do cliente
│   ├── frameworks.md         PAS, AIDA, BAB, PASTOR, 4Ps, FAB, página longa
│   ├── headlines.md          fórmulas de título, assuntos de e-mail, ganchos
│   ├── ofertas.md            preço, ancoragem, bônus, garantia, escassez
│   ├── gatilhos.md           gatilhos mentais, hierarquia de prova, limites
│   ├── canais.md             e-mail, LP, anúncios, VSL, social, e-commerce, DM
│   ├── revisao.md            checklist antes de entregar
│   ├── etica.md              promessas, saúde, dinheiro, LGPD, CDC
│   └── exemplos.md           três peças completas, do briefing ao texto final
└── assets/
    └── briefing.md           template de briefing
```

## Duas coisas que a skill não faz

- **Não inventa prova.** Número, depoimento ou caso que você não fornecer vira
  `[PROVA NECESSÁRIA: ...]` no texto, para você preencher antes de publicar.
- **Não maquia oferta fraca.** Quando o problema for preço, garantia ou posicionamento
  em vez do texto, ela diz isso junto com a copy.
- **Não troca a sua voz pela dela.** Se você mandar um texto seu para melhorar, ela
  mexe no argumento e preserva os seus emojis, a sua pontuação e os seus bordões.

---

# Skill de finanças pessoais

Em `.claude/skills/financas/` fica a skill de **finanças pessoais e do casal**: sair das
dívidas, organizar e priorizar contas, orçamento, divisão de contas em casal, reserva de
emergência e primeiros investimentos, com foco no Brasil. É acionada sozinha quando o
assunto é dinheiro da casa, ou com `/financas`.

```
.claude/skills/financas/
├── SKILL.md                         fluxo: diagnóstico → classificação → plano → revisão
├── references/
│   ├── prioridades.md               o que pagar primeiro quando não dá para tudo
│   ├── dividas.md                   estancar, avalanche/bola de neve, portabilidade, negociação
│   ├── casal.md                     modelos de divisão, regras, rotina de reuniões
│   ├── orcamento.md                 mapear gastos, 50/30/20, calendário de contas, cortes
│   ├── emergencia.md                quando a renda não cobre o básico
│   ├── reserva-e-investimentos.md   reserva de emergência e próximos passos
│   ├── calculos.md                  juros, parcela, prazo de quitação, comparar propostas
│   └── golpes.md                    armadilhas e golpes comuns
└── assets/
    └── diagnostico.md               template para levantar a situação
```
