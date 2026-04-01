# AletheIA  
**Decision Layer for AI Systems**  
_From output to decision_

---

## Tese

Modelos de IA geram respostas.  
Não estruturam decisão.

AletheIA define uma camada entre **output e execução**, organizando contexto, interpretação, validação e decisão de forma explicável, rastreável e controlada.

---

## O que é

Uma decision layer para sistemas baseados em IA.

AletheIA estrutura o desenvolvimento de aplicações com IA — especialmente em fluxos de **vibe coding** e **agentic systems** — reduzindo improviso, retrabalho e risco operacional.

O framework organiza como decisões são formadas antes da execução, incluindo:

- seleção e uso de contexto  
- definição de spec e execution contracts  
- orquestração de runtimes  
- validação multicamada  
- policy enforcement  
- loops de aprendizado  
- portabilidade entre modelos e agentes  

---

## Problema

Fluxos de desenvolvimento com IA hoje falham não por falta de geração, mas por falta de estrutura de decisão.

Sistemas típicos:

- executam diretamente outputs de modelos  
- não explicitam por que algo foi executado  
- não controlam contexto de forma consistente  
- não possuem validação antes da ação  
- não mantêm memória confiável  
- não permitem auditoria real  

Resultado:

- comportamento imprevisível  
- retrabalho constante  
- dificuldade de escalar  
- risco operacional elevado  

---

## Abordagem

AletheIA organiza o fluxo:

Signal → Context → Interpretation → Decision → Execution

E define uma camada explícita entre:

Model Output → Execution

Essa camada transforma resposta em **ação governada**.

---

## Princípios

- IA sugere. O sistema decide como executar.  
- Toda decisão deve ser explicável.  
- Toda ação deve ser rastreável.  
- Contexto mínimo suficiente.  
- Segurança antes de automação.  
- Portabilidade antes de dependência de runtime.  

---

## Arquitetura (alto nível)

/engine  
  compiler/      → estrutura inputs em artefatos de decisão  
  policy/        → regras, limites e governança  
  simulator/     → cenários e validação  
  runtime/       → execução controlada  
  debugger/      → inspeção e rastreabilidade  

/adapters  
  codex/  
  claude/  
  goose/  

/schemas  
  decision.schema.json  

/starter-pack  
  docs/  
  features/  
  evals/  
  playbooks/  

---

## Componentes

**Compiler**  
Transforma inputs, contexto e intenções em estruturas formais de decisão.

**Policy Layer**  
Define regras de execução, limites e guardrails.

**Runtime**  
Executa decisões com controle e observabilidade.

**Simulator**  
Permite testar cenários antes da execução real.

**Debugger**  
Permite entender decisões após execução.

**Adapters**  
Integra com diferentes runtimes (Codex, Claude, agentes locais, etc.).

---

## O que este repositório entrega

- Estrutura base da decision layer  
- Schema de decisão (alpha)  
- DSL inicial para modelagem  
- Simulações de cenários  
- Pseudo-engine para implementação  
- Estratégias de memória e runtime  
- Starter pack para projetos  

---

## O que não está aqui

- UI final  
- integrações completas com APIs externas  
- datasets proprietários  
- modelos treinados específicos  

Este projeto define **como decisões são estruturadas**, não apenas executadas.

---

## Casos de uso

- desenvolvimento de aplicações com IA  
- sistemas multi-agente  
- copilotos e assistentes avançados  
- workflows críticos com IA  
- automações com necessidade de governança  
- ambientes com exigência de auditabilidade  

---

## Como usar

1. Explore `/starter-pack`  
2. Entenda `/schemas`  
3. Implemente `/engine`  
4. Rode `/simulator`  
5. Integre via `/adapters`  

---

## Estrutura conceitual

AletheIA atua como uma camada entre:

Model → Decision → Execution

Separando:

- geração  
- interpretação  
- decisão  
- execução  

Essa separação reduz acoplamento e aumenta controle.

---

## Status

Alpha — foco em:

- coerência do modelo  
- estrutura da decision layer  
- base para implementação  

Ainda não otimizado para produção.

---

## Roadmap

Curto prazo:

- consolidar schema de decisão  
- estruturar runtime mínimo  
- melhorar simulador  
- definir contratos de execução  

Médio prazo:

- suporte robusto a multi-agentes  
- taxonomia de decisões  
- validação automática mais forte  
- integração com mais runtimes  

Longo prazo:

- especialização por domínio  
- aprendizado baseado em execução  
- evolução para camada padrão em sistemas de IA  

---

## Direção

Este projeto não compete por melhores respostas.

Ele compete por:

- melhores decisões  
- decisões explicáveis  
- decisões confiáveis  

---

## Licença

Apache 2.0

---

## Nota final

IA responde.  
AletheIA estrutura como sistemas decidem.
