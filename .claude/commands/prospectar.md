---
name: prospectar
description: >
  Processo completo de prospecção de clientes para a Spellbound Marketing:
  define perfil de lead, indica onde encontrar (LinkedIn e Instagram NL),
  qualifica, gera mensagens de primeiro contato e follow-up, e registra em leads/leads.md.
  Use quando a Mila disser "quero prospectar", "buscar clientes", "encontrar leads",
  "abordar alguém no LinkedIn/Instagram", ou chamar /prospectar.
---

# /prospectar — Prospecção de Clientes

## Dependências

- `_contexto/empresa.md` — ICP e serviços da Spellbound
- `_contexto/preferencias.md` — tom de voz e estilo editorial
- `leads/leads.md` — lista de leads para atualizar

---

## Workflow

### Fase 1 — Definir o perfil da campanha

Perguntar, uma de cada vez:

1. "Qual serviço você quer vender nessa rodada de prospecção? (gestão de redes, mídia paga, workshop, planejamento estratégico, outro)"
2. "Tem algum segmento específico que você quer focar? (ex: restaurantes, profissionais de saúde, lojas, coaches, prestadores de serviço)"
3. "Qual é o momento ideal do negócio que você quer atingir? (ex: negócio novo querendo presença digital, negócio estabelecido sem estratégia, empreendedor brasileiro chegando na Holanda)"

Com as respostas, montar e apresentar o **perfil do lead ideal** para essa campanha:

> "Pra essa rodada, o lead ideal é:
> - **Segmento:** [ex: restaurantes brasileiros em Amsterdam]
> - **Momento:** [ex: aberto há menos de 2 anos, presença digital fraca ou inexistente]
> - **Sinal de oportunidade:** [ex: perfil no Instagram com menos de 500 seguidores, sem site, posts sem padrão]
> - **Serviço de entrada:** [ex: planejamento estratégico + gestão de redes]
>
> Faz sentido?"

Ajustar conforme feedback antes de continuar.

---

### Fase 2 — Onde encontrar esses leads

Com base no perfil definido, apresentar guia prático de busca nos dois canais:

#### LinkedIn

**Strings de busca sugeridas** (adaptar ao segmento):
- `"[segmento]" "Netherlands" OR "Amsterdam" OR "Den Haag" OR "Rotterdam"`
- `"owner" OR "founder" OR "eigenaar" "[segmento]" "Netherlands"`
- `"Brazilian" OR "Brasil" "[segmento]" "Netherlands"`

**Filtros a usar:**
- Localização: Netherlands
- Conexão: 2º grau (mais fácil de abordar com ponto em comum)
- Setor: conforme o segmento escolhido

**Sinais de oportunidade no perfil:**
- Negócio listado no LinkedIn mas sem página da empresa estruturada
- Sem estratégia de conteúdo aparente (posts irregulares ou inexistentes)
- Bio genérica sem proposta de valor clara

**Grupos relevantes para prospecção passiva:**
- Grupos de brasileiros empreendendo na Holanda
- Grupos de networking de pequenos negócios em NL
- Grupos do setor específico (ex: "Hospitality Netherlands")

#### Instagram

**Hashtags para encontrar o segmento em NL:**
- `#[segmento]netherlands` / `#[segmento]amsterdam` / `#[segmento]denhaag`
- `#brasileirosnoholanda` / `#braziliansinnetherlands`
- `#smallbusiness[cidade]` / `#[segmento]rotterdam`

**Busca por geolocalização:**
- Pesquisar a localização da cidade-alvo no Instagram e filtrar por negócios do segmento

**Sinais de oportunidade no perfil:**
- Feed sem padrão visual
- Frequência irregular de posts
- Bio sem CTA ou link funcional
- Poucos seguidores para o tempo de conta
- Comentários não respondidos

---

### Fase 3 — Qualificar o lead

Antes de abordar, verificar com este checklist rápido:

- [ ] O negócio existe e está ativo (perfil atualizado, posts recentes)
- [ ] Está claramente nos Países Baixos
- [ ] Parece ter capacidade de investir (não é conta de hobby, tem produto/serviço real)
- [ ] Tem problema visível que a Spellbound resolve (presença fraca, sem estratégia, conteúdo sem padrão)
- [ ] Não é concorrente nem parceiro atual

Se passar em pelo menos 4 de 5 critérios: vale abordar.

---

### Fase 4 — Primeira abordagem

Perguntar:

1. "Qual é o nome do lead e o negócio dele?"
2. "Onde você vai abordar — LinkedIn ou Instagram?"
3. "Tem alguma coisa específica que você notou no perfil dele que pode ser usada como gancho?"

Gerar **duas versões** da mensagem de primeiro contato:

**Versão A — mais direta** (para LinkedIn onde o tom é mais profissional)
**Versão B — mais próxima** (para Instagram onde o tom é mais informal)

**Estrutura de ambas:**
- Gancho específico sobre o negócio deles (nunca mensagem genérica)
- Observação sobre algo que viu no perfil (sem parecer invasivo)
- Uma pergunta aberta — não uma oferta
- Máximo 3-4 linhas. Sem links, sem proposta no primeiro contato.

**Tom:** Sábio Parceiro — próximo, sem hype, sem "ei, posso te ajudar a explodir suas vendas"

**Idioma:** inglês para neerlandeses; português para brasileiros na Holanda (avaliar pelo perfil do lead).

Apresentar as duas versões e deixar a Mila escolher ou combinar.

---

### Fase 5 — Follow-up (se não houver resposta)

Gerar sequência de 3 follow-ups com intervalo sugerido:

| # | Quando enviar | Tom | Objetivo |
|---|--------------|-----|----------|
| 1 | 5 dias após o primeiro contato | Leve, adiciona valor | Reabrir conversa com uma insight ou referência relevante |
| 2 | 10 dias após o primeiro contato | Direto, mas não insistente | Última tentativa com CTA claro |
| 3 | 30 dias depois | Neutro, portas abertas | Manter o relacionamento sem forçar |

Após o 3º sem resposta: marcar como "Descartado (por ora)" em `leads/leads.md` e não abordar por pelo menos 60 dias.

---

### Fase 6 — Registrar o lead

Salvar a abordagem em `leads/abordagens/[nome-do-lead].md`:

```markdown
# [Nome do Lead] — [Negócio]

**Canal:** LinkedIn / Instagram
**Perfil:** [URL ou @]
**Segmento:** 
**Serviço de interesse:** 
**Data da primeira abordagem:** 

## Mensagem enviada

[Colar a mensagem escolhida]

## Follow-ups

- [ ] Follow-up 1 — [data prevista]
- [ ] Follow-up 2 — [data prevista]
- [ ] Follow-up 3 — [data prevista]

## Notas

[Observações sobre o lead, respostas recebidas, próximos passos]
```

Adicionar o lead na tabela de `leads/leads.md` com status "Abordado".

---

## Regras

- Nunca gerar mensagem genérica — sempre personalizar com algo específico do perfil do lead
- Primeiro contato sem proposta, sem links, sem pitch de venda — só abrir conversa
- Tom sempre alinhado a `_contexto/preferencias.md` — Sábio Parceiro, nunca hype
- Inglês para neerlandeses, português para brasileiros na Holanda (avaliar pelo perfil)
- Após gerar as mensagens, perguntar se a Mila quer abordar outro lead ou encerrar
- Se a Mila trouxer um perfil (URL ou @), analisar antes de gerar a abordagem
