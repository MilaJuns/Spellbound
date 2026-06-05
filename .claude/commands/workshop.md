---
name: workshop
description: >
  Cria o conteúdo completo de um workshop da Spellbound Marketing: planejamento,
  slides, kit do aluno (PDF, checklist, templates, e-book) e trilha de email marketing.
  Use quando a Mila disser "vou criar um workshop", "quero montar um workshop sobre",
  "novo workshop", ou chamar /workshop diretamente.
---

# /workshop — Criação de Workshop Completo

## Dependências

- `_contexto/empresa.md` — contexto do negócio e público-alvo
- `_contexto/preferencias.md` — tom de voz e estilo editorial
- `marca/design-guide.md` — identidade visual para slides e kit
- `workshops/_modelo-workshop/conteudo.md` — template de planejamento

---

## Workflow

### Fase 1 — Brief do workshop

Começar com as perguntas essenciais, uma de cada vez:

1. "Qual é o tema do workshop?"
2. "Qual é o público? (nível de conhecimento, perfil, onde estão — NL, BR, online)"
3. "Qual é o formato e duração? (ex: 2h online ao vivo, gravado, presencial)"
4. "Qual é o resultado concreto que o aluno sai sabendo fazer?"
5. "Você já tem algum material de referência ou conteúdo base? (artigos, anotações, outro workshop)"

Se a Mila tiver material de referência (arquivos em `dados/` ou URLs), ler antes de continuar.

---

### Fase 2 — Estrutura de conteúdo

Com base nas respostas, montar a estrutura do workshop:

1. Dividir o conteúdo em **3 a 5 módulos** com progressão lógica
2. Para cada módulo: listar tópicos, exercício prático e duração estimada
3. Mapear materiais didáticos que podem ser acoplados (exemplos reais, dados de mercado, ferramentas)
4. Usar a estrutura favorita da Spellbound: **Pergunta → Contexto → Insight → Ação**

Apresentar a estrutura antes de continuar:

> "Aqui está como eu organizaria o conteúdo. Faz sentido pra você?"

Ajustar conforme o feedback. Só avançar depois de confirmado.

---

### Fase 3 — Criar pasta do workshop

Criar a pasta do workshop em `workshops/[slug-do-tema]/` copiando a estrutura do modelo:

```
workshops/[slug-do-tema]/
  conteudo.md      ← planejamento preenchido
  slides/          ← apresentação (HTML → PNG)
  kit-aluno/       ← materiais de entrega
  emails/          ← trilha de email marketing
```

Preencher `conteudo.md` com tudo que foi definido nas fases 1 e 2.

---

### Fase 4 — Slides da apresentação

Gerar os slides em HTML, um de cada vez, aplicando o design da Spellbound (`marca/design-guide.md`).

**Estrutura padrão de um deck de workshop:**

| Slide | Conteúdo |
|-------|----------|
| Capa | Nome do workshop + tagline + logo Spellbound |
| Agenda | Módulos e duração |
| Por módulo | 1 slide de abertura + slides de conteúdo + 1 slide de exercício |
| Encerramento | Próximos passos + CTA + contato |

**Padrão visual obrigatório (Spellbound):**
- Canvas: `#510000` (maroon-800)
- Texto principal: `#F5EDE0` (cream)
- Destaque/CTA: `#F95F00` (sparkle orange)
- Labels uppercase: `#D4600A` (amber)
- Fontes: Varela Round (títulos) + Nunito (corpo)
- Borda sutil: `rgba(212,96,10,0.18)`
- Sparkle ✦ como elemento decorativo e separador de seção
- Nunca usar emojis decorativos — só o ✦

Salvar cada slide em `workshops/[slug]/slides/slide-[N]-[tema].html`.

Renderizar com Playwright se disponível:
```bash
npx playwright screenshot --viewport-size=1920,1080 --full-page "file:///caminho/slide.html" "slide.png"
```

Perguntar depois de cada módulo se quer ajustar antes de continuar.

---

### Fase 5 — Kit do aluno

Gerar os materiais de entrega em HTML (para exportar como PDF ou imprimir):

#### 5.1 — PDF principal
Documento de apoio com os principais conceitos do workshop. Estrutura:
- Capa com nome do workshop e logo
- Resumo de cada módulo (máximo 1 página por módulo)
- Seção "O que fazer agora" com próximos passos práticos
- Contato e redes da Spellbound

Salvar em `workshops/[slug]/kit-aluno/[slug]-guia.html`

#### 5.2 — Checklist
Lista de ações práticas derivadas do workshop. Formato visual, imprimível.
- Título: "Checklist: [tema do workshop]"
- Agrupado por módulo ou por fase de implementação
- Caixas de seleção visuais (CSS)

Salvar em `workshops/[slug]/kit-aluno/[slug]-checklist.html`

#### 5.3 — Templates
Modelos prontos para o aluno usar. O tipo de template depende do tema do workshop.
- Exemplos: canvas de posicionamento, calendário editorial, planilha de métricas, roteiro de post
- Formato limpo, editável, com instruções breves de preenchimento

Salvar em `workshops/[slug]/kit-aluno/template-[nome].html`

#### 5.4 — E-book (quando aplicável)
Conteúdo expandido de um tópico do workshop que merece aprofundamento.
- Máximo 6 a 10 páginas
- Tom editorial da Spellbound — ensina, provoca reflexão, indica ação
- Inclui dados, exemplos reais e referências quando possível

Salvar em `workshops/[slug]/kit-aluno/[slug]-ebook.html`

---

### Fase 6 — Trilha de email marketing

Gerar a sequência de 5 emails de acompanhamento.

| # | Momento | Objetivo |
|---|---------|----------|
| 1 | Imediatamente após inscrição | Boas-vindas, o que esperar, como se preparar |
| 2 | 1 dia antes | Lembrete + dica de preparação |
| 3 | 1 dia após o workshop | Consolidar aprendizado + entregar kit |
| 4 | 1 semana depois | Estimular aplicação + tirar dúvidas |
| 5 | 2 semanas depois | Coletar resultado + abrir conversa sobre próximo passo |

**Para cada email:**
- Assunto direto e descritivo (nunca vago)
- Estrutura: Pergunta ou gancho → Contexto → Insight ou dica → CTA claro
- Tom Sábio Parceiro — próximo, sem hype
- Em inglês (mercado NL)
- Assinatura: Mila Juns, Spellbound Marketing

Salvar cada email em `workshops/[slug]/emails/email-[N]-[momento].md`

---

### Fase 7 — Resumo final

Ao concluir, apresentar o que foi gerado:

> "Workshop [nome] pronto. Aqui está o que foi criado:
>
> - `conteudo.md` — planejamento completo ([N] módulos)
> - `slides/` — [N] slides em HTML ([renderizados em PNG / prontos para renderizar])
> - `kit-aluno/` — guia PDF, checklist, [N] templates, e-book
> - `emails/` — trilha de 5 emails de acompanhamento
>
> Quer revisar alguma parte ou seguimos para o próximo processo?"

---

## Regras

- Sempre confirmar a estrutura de conteúdo (Fase 2) antes de gerar qualquer arquivo
- Gerar slides um módulo por vez — não gerar o deck inteiro de uma vez sem confirmação
- Todos os HTMLs devem usar apenas CSS inline e Google Fonts (sem dependências externas)
- O visual deve seguir rigorosamente o `marca/design-guide.md` — maroon, cream, orange, sparkle ✦
- Tom editorial sempre em inglês para materiais do aluno; comunicação com a Mila em português
- Nunca inventar dados ou referências — se precisar de dado de mercado, indicar onde buscar
- Se a Mila tiver material de referência, ler antes de estruturar o conteúdo
