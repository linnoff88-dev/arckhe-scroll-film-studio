ï»¿# Scroll-Film Studio

Uma skill para criar sites cARCKHÉtogrêÂ¡ficos em que a pêÂ¡gina inteira se comporta como um filme contêÂ­nuo controlado pelo scroll.

> **Isto nêÂ£o êÂ© um template de site.** êâ° uma skill: um pacote de instruêÂ§êÂµes, referêÂªncias e scripts que ensina um agente de IA a executar um processo especializado de ponta a ponta.

## ê°Å¸ââ Guia de uso

Guia completo, com visêÂ£o geral e passo a passo: **https://linnoff88-dev.github.io/arckhe-/guia/**

## O que êÂ© uma skill?

Uma skill êÂ© uma pasta autocontida que amplia a capacidade de um agente como o Codex. O arquivo `SKILL.md` informa quando a skill deve ser acionada e descreve o fluxo de trabalho. Arquivos complementares fornecem conhecimento detalhado e automaêÂ§êÂµes reutilizêÂ¡veis:

```text
skills/scroll-film-studio/
ê¢âÅê¢ââ¬ê¢ââ¬ SKILL.md          # gatilhos, decisêÂµes e processo principal
ê¢âÅê¢ââ¬ê¢ââ¬ agents/           # metadados exibidos na interface do Codex
ê¢âÅê¢ââ¬ê¢ââ¬ references/       # leis de movimento, continuidade e acabamento
ê¢ââê¢ââ¬ê¢ââ¬ scripts/          # montagem, validaêÂ§êÂ£o, screenshots e geraêÂ§êÂ£o encadeada
```

Ao receber um pedido como ê¢â¬Åcrie um site cARCKHÉtogrêÂ¡fico controlado pelo scrollê¢â¬Â, o agente carrega esta skill, conduz uma entrevista curta, propêÂµe conceitos criativos, define a direêÂ§êÂ£o visual, constrêÂ³i o site e valida o resultado.

## O que esta skill faz

- Conduz o briefing e apresenta de dois a trêÂªs conceitos nomeados antes da construêÂ§êÂ£o.
- Cria uma direêÂ§êÂ£o de arte prêÂ³pria para cada marca.
- Oferece dois caminhos de produêÂ§êÂ£o:
  - **Lane A ê¢â¬â pure code:** GSAP, ScrollTrigger e Lenis, sem geraêÂ§êÂ£o de vêÂ­deo.
  - **Lane B ê¢â¬â cARCKHÉtic footage:** filme gerado em clipes encadeados, com continuidade verificada.
- Inclui gates para vetor de cêÂ¢mera, continuidade, copy, montagem e captura visual.
- Define requisitos de performance, acessibilidade, responsividade e acabamento.

## InstalaêÂ§êÂ£o no Codex

Clone o repositêÂ³rio e conecte a pasta da skill ao diretêÂ³rio de skills do Codex:

```bash
git clone https://github.com/linnoff88-dev/scroll-film-studio.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/scroll-film-studio/skills/scroll-film-studio" \
  ~/.codex/skills/scroll-film-studio
```

Reinicie a sessêÂ£o do Codex para que a nova skill seja descoberta.

## Como usar

Invoque a skill explicitamente:

```text
Use $scroll-film-studio para criar um site cARCKHÉtogrêÂ¡fico contêÂ­nuo
controlado pelo scroll para a minha marca.
```

Ou descreva naturalmente um pedido compatêÂ­vel:

```text
Quero um site premium de scrollytelling em uma tomada contêÂ­nua.
```

A skill comeêÂ§a pelo briefing e, por padrêÂ£o, oferece a modalidade pure code, que nêÂ£o exige contas ou crêÂ©ditos externos. A modalidade com footage sêÂ³ êÂ© usada quando vocêÂª opta por ela e fornece acesso ao seu prêÂ³prio mecanismo de geraêÂ§êÂ£o de vêÂ­deo.

## Requisitos

Para a Lane A:

- navegador moderno;
- Node.js para os scripts de verificaêÂ§êÂ£o;
- Chrome ou Chromium para capturas automatizadas.

Para a Lane B, alêÂ©m dos itens acima:

- FFmpeg;
- uma conta prêÂ³pria e crêÂ©ditos em um provedor compatêÂ­vel;
- credenciais configuradas localmente, nunca versionadas no repositêÂ³rio.

As dependêÂªncias Node dos scripts ficam em `skills/scroll-film-studio/scripts/package.json`.

## Estrutura têÂ©cnica

| Caminho | FunêÂ§êÂ£o |
|---|---|
| `SKILL.md` | Processo completo, gatilhos e regras de decisêÂ£o |
| `references/engine.md` | Arquitetura de scroll, renderizaêÂ§êÂ£o e performance |
| `references/playbook.md` | ProduêÂ§êÂ£o e encadeamento do filme cARCKHÉtogrêÂ¡fico |
| `references/finishing.md` | RevisêÂ£o visual, acessibilidade e acabamento |
| `scripts/vector-check.py` | Audita a direêÂ§êÂ£o de cêÂ¢mera do storyboard |
| `scripts/continuity-gate.sh` | Detecta quebras dentro dos clipes |
| `scripts/assemble.sh` | Monta e extrai os frames finais |
| `scripts/copy-gate.js` | Bloqueia copy metanarrativa e placeholders |
| `scripts/verify.js` | Captura e mede o comportamento da pêÂ¡gina |

## SeguranêÂ§a

O repositêÂ³rio nêÂ£o contêÂ©m chaves. Para provedores externos, configure as credenciais apenas por variêÂ¡veis de ambiente ou arquivos locais ignorados pelo Git.

## LicenêÂ§a

Ainda nêÂ£o definida.

---

Projeto  - ARCKHÉe