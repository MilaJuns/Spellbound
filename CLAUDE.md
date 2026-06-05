# Spellbound Marketing — Claude Code OS

## O que é esse workspace

Workspace operacional da **Spellbound Marketing** — marketing strategy studio de Mila Juns focado nos Países Baixos. Aqui se produz conteúdo, propostas, materiais de workshops, gestão financeira e operação de clientes recorrentes.

**Estrutura de pastas:**
- `_contexto/` — memória do sistema (não apagar)
- `clientes/` — uma pasta por cliente com briefing e proposta
- `workshops/` — materiais dos workshops e treinamentos
- `conteudo/` — produção por canal (redes-sociais, email, anuncios)
- `propostas/` — propostas comerciais geradas
- `financeiro/` — contratos, faturas e relatórios financeiros
- `marca/` — identidade visual, logo, fotos, design-guide
- `dados/` — arquivos para análise (CSV, PDF, XLSX, TXT)
- `templates/skills/` — templates de skills prontos para personalizar com /mapear
- `templates/ferramentas/catalogo.md` — APIs e ferramentas disponíveis para usar em skills

## Sobre o negócio

Spellbound Marketing é o studio de estratégia de marketing de Mila Juns para o mercado dos Países Baixos. Atende 100% online pequenos negócios, profissionais autônomos e equipes pequenas — especialmente brasileiros empreendendo na Holanda. Opera solo com assistente virtual Merlin.

## O que mais fazemos aqui

- Construção de website e planejamento estratégico
- Gestão de redes sociais + produção de conteúdo
- Setup e gestão de mídia paga (Meta/Google)
- E-mail marketing
- Workshops e treinamentos de Marketing e IA
- Gestão financeira da empresa (contratos, faturas, relatórios)

## Tom de voz

Arquétipo **Sábio Parceiro**: autoridade com proximidade, sem arrogância. Método e clareza — nunca hype ou promessas mágicas.
Idioma dos materiais: **inglês** (mercado NL). Português para operação interna.
Estrutura favorita: **Pergunta → Contexto → Insight → Ação/CTA**.
O sparkle ✦ é o único elemento decorativo — não usar emojis genéricos em materiais da marca.
Ver `_contexto/preferencias.md` para substituições de palavras e checklist editorial completo.

## Ferramentas conectadas

- [ ] Canva MCP
- [ ] Trello MCP
- [ ] Gmail MCP
- [ ] Mailchimp
- [ ] Notion

*(Marcar conforme os MCPs forem instalados)*

---

## Contexto do negócio

No início de toda conversa, ler os seguintes arquivos (se existirem e estiverem configurados):

1. `_contexto/empresa.md` — quem é a Mila, o que faz, como funciona o negócio
2. `_contexto/preferencias.md` — tom de voz, estilo de escrita, o que evitar
3. `_contexto/estrategia.md` — foco atual, prioridades, o que pode esperar

Usar essas informações como base para qualquer resposta ou decisão. Ao sugerir prioridades, formatos ou abordagens, considerar o foco atual descrito em `estrategia.md`.

Para qualquer tarefa visual (carrossel, proposta, slide, landing page), consultar `marca/design-guide.md` como referência de estilo.

Não é necessário listar o que foi lido nem confirmar a leitura. Apenas usar o contexto naturalmente.

---

## Fluxo de trabalho

Antes de executar qualquer tarefa, verificar se existe uma skill relevante em `.claude/skills/` ou `.claude/commands/`.
Se encontrar, seguir as instruções da skill.
Se não encontrar, executar a tarefa normalmente.

Ao concluir uma tarefa que não tinha skill mas parece repetível, perguntar:

> "Isso pode virar uma skill pra próxima vez. Quer que eu crie?"

Não perguntar para tarefas pontuais ou perguntas simples. Só quando o padrão de repetição for claro.

---

## Aprender com correções

Quando a Mila corrigir algo, melhorar uma resposta ou dar instrução permanente ("na verdade é assim", "não faça mais isso", "prefiro assim", "sempre que...", "evita..."), perguntar:

> "Quer que eu salve isso pra não precisar repetir?"

Onde salvar:
- **Sobre o negócio** → `_contexto/empresa.md`
- **Sobre preferências e estilo** → `_contexto/preferencias.md`
- **Sobre prioridades e foco** → `_contexto/estrategia.md`
- **Regra de comportamento nessa pasta** → este `CLAUDE.md`

Salvar com linha nova clara, sem reformatar o arquivo inteiro. Confirmar mostrando a linha adicionada.

---

## Manter contexto atualizado

Ao terminar tarefa que mudou algo relevante (novo cliente, nova skill, mudança de foco, ferramenta instalada), perguntar:

> "Isso mudou algo no teu contexto. Quer que eu atualize os arquivos de memória?"

- Novo cliente, serviço, ferramenta → `_contexto/empresa.md`
- Mudança de prioridade → `_contexto/estrategia.md`
- Correção de tom ou estilo → `_contexto/preferencias.md`
- Nova pasta, skill criada → `CLAUDE.md`
- Mudança visual → `marca/design-guide.md`

Mostrar o que vai mudar antes de salvar. Não reformatar o arquivo inteiro.

Rodar `/atualizar` para varredura completa quando necessário.

---

## Criar skills novas

1. Verificar se existe template em `templates/skills/`. Se existir, usar como base.
2. Perguntar: "Essa skill é específica pra Spellbound ou útil em qualquer projeto?"
   - Específica → `.claude/commands/nome-da-skill.md`
   - Global → `~/.claude/skills/nome-da-skill/SKILL.md`
3. Ler `_contexto/empresa.md` e `_contexto/preferencias.md` antes de criar
4. Consultar `templates/ferramentas/catalogo.md` para ver ferramentas disponíveis

---

## Criar visuais (carrossel, slide, proposta)

Sempre ler `marca/design-guide.md` antes de gerar qualquer visual.

Renderizar HTML em PNG com Playwright:
```bash
npx playwright install chromium  # instalar uma vez
npx playwright screenshot --viewport-size=1080,1350 --full-page "file:///caminho/slide.html" "slide.png"
```

Tamanhos: feed Instagram `1080x1350`, story `1080x1920`, slide 16:9 `1920x1080`, card quadrado `1080x1080`.
