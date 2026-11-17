# Scroll-Film Studio

Uma skill para criar sites cinematogrÃ¡ficos em que a pÃ¡gina inteira se comporta como um filme contÃ­nuo controlado pelo scroll.

> **Isto nÃ£o Ã© um template de site.** Ã‰ uma skill: um pacote de instruÃ§Ãµes, referÃªncias e scripts que ensina um agente de IA a executar um processo especializado de ponta a ponta.

## ðŸ“– Guia de uso

Guia completo, com visÃ£o geral e passo a passo: **https://inematds.github.io/scroll-film-studio/guia/**

## O que Ã© uma skill?

Uma skill Ã© uma pasta autocontida que amplia a capacidade de um agente como o Codex. O arquivo `SKILL.md` informa quando a skill deve ser acionada e descreve o fluxo de trabalho. Arquivos complementares fornecem conhecimento detalhado e automaÃ§Ãµes reutilizÃ¡veis:

```text
skills/scroll-film-studio/
â”œâ”€â”€ SKILL.md          # gatilhos, decisÃµes e processo principal
â”œâ”€â”€ agents/           # metadados exibidos na interface do Codex
â”œâ”€â”€ references/       # leis de movimento, continuidade e acabamento
â””â”€â”€ scripts/          # montagem, validaÃ§Ã£o, screenshots e geraÃ§Ã£o encadeada
```

Ao receber um pedido como â€œcrie um site cinematogrÃ¡fico controlado pelo scrollâ€, o agente carrega esta skill, conduz uma entrevista curta, propÃµe conceitos criativos, define a direÃ§Ã£o visual, constrÃ³i o site e valida o resultado.

## O que esta skill faz

- Conduz o briefing e apresenta de dois a trÃªs conceitos nomeados antes da construÃ§Ã£o.
- Cria uma direÃ§Ã£o de arte prÃ³pria para cada marca.
- Oferece dois caminhos de produÃ§Ã£o:
  - **Lane A â€” pure code:** GSAP, ScrollTrigger e Lenis, sem geraÃ§Ã£o de vÃ­deo.
  - **Lane B â€” cinematic footage:** filme gerado em clipes encadeados, com continuidade verificada.
- Inclui gates para vetor de cÃ¢mera, continuidade, copy, montagem e captura visual.
- Define requisitos de performance, acessibilidade, responsividade e acabamento.

## InstalaÃ§Ã£o no Codex

Clone o repositÃ³rio e conecte a pasta da skill ao diretÃ³rio de skills do Codex:

```bash
git clone https://github.com/inematds/scroll-film-studio.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/scroll-film-studio/skills/scroll-film-studio" \
  ~/.codex/skills/scroll-film-studio
```

Reinicie a sessÃ£o do Codex para que a nova skill seja descoberta.

## Como usar

Invoque a skill explicitamente:

```text
Use $scroll-film-studio para criar um site cinematogrÃ¡fico contÃ­nuo
controlado pelo scroll para a minha marca.
```

Ou descreva naturalmente um pedido compatÃ­vel:

```text
Quero um site premium de scrollytelling em uma tomada contÃ­nua.
```

A skill comeÃ§a pelo briefing e, por padrÃ£o, oferece a modalidade pure code, que nÃ£o exige contas ou crÃ©ditos externos. A modalidade com footage sÃ³ Ã© usada quando vocÃª opta por ela e fornece acesso ao seu prÃ³prio mecanismo de geraÃ§Ã£o de vÃ­deo.

## Requisitos

Para a Lane A:

- navegador moderno;
- Node.js para os scripts de verificaÃ§Ã£o;
- Chrome ou Chromium para capturas automatizadas.

Para a Lane B, alÃ©m dos itens acima:

- FFmpeg;
- uma conta prÃ³pria e crÃ©ditos em um provedor compatÃ­vel;
- credenciais configuradas localmente, nunca versionadas no repositÃ³rio.

As dependÃªncias Node dos scripts ficam em `skills/scroll-film-studio/scripts/package.json`.

## Estrutura tÃ©cnica

| Caminho | FunÃ§Ã£o |
|---|---|
| `SKILL.md` | Processo completo, gatilhos e regras de decisÃ£o |
| `references/engine.md` | Arquitetura de scroll, renderizaÃ§Ã£o e performance |
| `references/playbook.md` | ProduÃ§Ã£o e encadeamento do filme cinematogrÃ¡fico |
| `references/finishing.md` | RevisÃ£o visual, acessibilidade e acabamento |
| `scripts/vector-check.py` | Audita a direÃ§Ã£o de cÃ¢mera do storyboard |
| `scripts/continuity-gate.sh` | Detecta quebras dentro dos clipes |
| `scripts/assemble.sh` | Monta e extrai os frames finais |
| `scripts/copy-gate.js` | Bloqueia copy metanarrativa e placeholders |
| `scripts/verify.js` | Captura e mede o comportamento da pÃ¡gina |

## SeguranÃ§a

O repositÃ³rio nÃ£o contÃ©m chaves. Para provedores externos, configure as credenciais apenas por variÃ¡veis de ambiente ou arquivos locais ignorados pelo Git.

## LicenÃ§a

Ainda nÃ£o definida.

---

Projeto adaptado da comunidade INEMA TDS - Marca Arckhe