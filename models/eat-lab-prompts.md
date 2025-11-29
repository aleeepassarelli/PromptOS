# 📚 BIBLIOTECA UNIFICADA DE PROMPTS EAT-LAB

**Versão:** 3.0 (2025-11-14)  
**Autor:** EAT-Lab Collaborative Framework  
**Licença:** MIT  

***

## 📖 ÍNDICE GERAL

```
├── 00_INFRAESTRUTURA
│   ├── Sistema de Calibração
│   └── Parâmetros Operacionais
│
├── 01_EXTRAÇÃO_CIENTÍFICA
│   ├── 1.1 Engenharia Reversa Cognitiva (Cadeia Completa)
│   ├── 1.2 Árvore de Raciocínio Multi-Especialista
│   └── 1.3 Prompts de Diagnóstico Rápido
│
├── 02_ANÁLISE_SEMÂNTICA
│   ├── 2.1 Densidade Semântica (SD)
│   ├── 2.2 Score(P) Completo
│   └── 2.3 Métricas Geométricas
│
├── 03_RACIOCÍNIO_ESTRUTURADO
│   ├── 3.1 Exploração (ToT, GoT, SoT)
│   ├── 3.2 Decomposição (Least-to-Most)
│   └── 3.3 Parallelização (Skeleton-of-Thought)
│
├── 04_AUTO_CORREÇÃO
│   ├── 4.1 Reflexão (Reflexion, Self-Refine)
│   ├── 4.2 Verificação (CoVe, RCoT)
│   └── 4.3 Crítica Externa (CRITIC)
│
├── 05_INTERAÇÃO_FERRAMENTAS
│   ├── 5.1 Ação (ReAct)
│   ├── 5.2 Programação (PoT)
│   └── 5.3 RAG + Steering
│
├── 06_META_OTIMIZAÇÃO
│   ├── 6.1 Evolução (APE, PromptBreeder)
│   ├── 6.2 Busca Guiada
│   └── 6.3 Métricas Customizadas
│
├── 07_MULTI_AGENTE
│   ├── 7.1 Debate (MAD)
│   ├── 7.2 Simulação (ChatDev, DyLAN)
│   └── 7.3 Orquestração Dinâmica
│
├── 08_ABSTRAÇÃO_ANÁLISE
│   ├── 8.1 Step-Back Prompting
│   ├── 8.2 Análise Dialética
│   └── 8.3 Principles Extraction
│
├── 09_ESPAÇO_LATENTE
│   ├── 9.1 Exploração Vetorial
│   ├── 9.2 Fusão e Composição
│   ├── 9.3 Steering e Patching
│   └── 9.4 SAE e Decomposição
│
├── 10_NOTEBOOKLM_SÍNTESE
│   ├── 10.1 Prompts Canônicos (1-10)
│   ├── 10.2 Prompts Avançados (11-20)
│   └── 10.3 Prompts Complementares (21-30)
│
└── 11_UTILITÁRIOS
    ├── 11.1 Visualização
    ├── 11.2 Diagnóstico
    ├── 11.3 Explicação para Leigos
    └── 11.4 Templates Markdown
```

***

## 🏗️ 00_INFRAESTRUTURA

### Sistema de Calibração Base

```markdown
# PROMPT: Calibração Universal

Você é um sistema especializado em [DOMÍNIO]. Antes de responder:

1. **Step-Back:** Derive o princípio abstrato da pergunta
2. **Citação:** Use até 3 fontes (autor, ano, DOI/arXiv)
3. **Estrutura:** Responda em seções hierárquicas
4. **Validação:** Termine com "Evidência—Convergências/Conflitos"

**Parâmetros:**
- Temperatura: 0.0–0.3 (fidelidade) | 0.7–1.0 (exploração)
- Max tokens: 600–1200
- Densidade Semântica alvo: SD ≥ 0.8
- Ambiguidade: ≤ 0.18

**Confirme calibração:** "✓ Sistema calibrado. [Domínio] carregado."
```

### Rubric de Avaliação

```markdown
**Critérios (0-5):**

1. **Fidelidade Factual** (30%) — ancoragem em fontes
2. **Coerência Estrutural** (20%) — lógica interna
3. **Rigor Conceitual** (20%) — precisão formal
4. **Capacidade Diagnóstica** (15%) — gaps e limitações
5. **Utilidade Operacional** (15%) — aplicabilidade

**Score Final:** Σ(pontuação × peso)
```

***

## 📋 01_EXTRAÇÃO_CIENTÍFICA

### 1.1 Engenharia Reversa Cognitiva

```markdown
# PROMPT: Cadeia de Extração Completa

## PARÂMETROS
- SD ≥ 0.8 | Ambiguidade ≤ 0.18
- Fontes: arXiv, Zenodo, GitHub, IEEE, ResearchGate
- Eliminação: especulação não-fundamentada

## CADEIA DE PROCESSAMENTO

### 🔴 ETAPA 1: IDENTIFICAR (O Caçador)
**Função:** pattern_detection → candidate_map

**Ações:**
1. Buscar em fontes primárias
2. Detectar padrões recorrentes
3. Mapear candidatos por relevância

**Output:** Lista top 10-15 com DOI/URL, citações, tipo

### 🧩 ETAPA 2: DESMONTAR (O Cirurgião)
**Função:** feature_extraction → semantic_components

**Ações:**
1. Extrair hipóteses (H₀, H₁)
2. Isolar metodologia (procedimentos, datasets)
3. Capturar métricas quantitativas
4. Rastrear código (GitHub + commit hash)

**Critérios:**
- Incluir: claims com evidência quantitativa
- Excluir: especulação ("possivelmente", "pode ser")
- Validar: reprodutibilidade (código + seeds)

**Output:** Componentes estruturados (hipóteses, métricas, código)

### 🧠 ETAPA 3: ABSTRAIR (O Filósofo)
**Função:** semantic_components → latent_representation

**Ações:**
1. Identificar padrões invariantes
2. Mapear relações causais (X → Y)
3. Derivar princípios generalizáveis

**Quality Gates:**
- SD ≥ 0.8
- Ambiguidade ≤ 0.18
- Coerência causal (sem contradições)

**Output:** Grafos, equações, algoritmos abstratos

### 💠 ETAPA 4: RECONFIGURAR (O Artífice)
**Função:** latent_representation → new_pattern

**Ações:**
1. Criar tabelas comparativas
2. Gerar classificações (★★★★★)
3. Formatar links rastreáveis
4. Sintetizar informação objetiva

**Output:** Estruturas prontas (tabelas, classificações, links)

### 🏛️ ETAPA 5: REAPLICAR (O Alquimista)
**Função:** new_pattern → integration → .md

**Ações:**
1. Consolidar em formato .md
2. Aplicar template estruturado
3. Adicionar metadados rastreáveis
4. Priorizar para integração

**Output:** Documento .md completo

## TEMPLATE DE SAÍDA

```
# [TÍTULO CURTO]

## 📊 Metadados
- Tipo: [paper|repo|método|framework]
- Ano: [YYYY]
- Fonte: [DOI/arXiv]
- Código: [GitHub + commit]

## 🎯 Resumo (1-3 frases)
[Problema → Método → Resultado]

## 🔬 Componentes Técnicos
### Hipótese
[H₀, H₁]

### Metodologia
```pseudocode
[algoritmo]
```

### Métricas-Chave
| Métrica | Valor | Baseline | Δ |
|---------|-------|----------|---|
| SD      | 0.85  | 0.72     | +0.13 |

### Equações
$$Score(P) = \sum_i \omega_i \cdot \rho_i \cdot \kappa_i - \beta \cdot S_H$$

## ✅ Reprodutibilidade
- Código: [link]
- Seeds:[1][2][3]
- Hardware: [specs]

## ⭐ Classificação
|| Critério | Rating | Justificativa |
|----------|--------|---------------|
| Rigor    | ★★★★★ | Evidência robusta |

## 🚦 Prioridade
**ALTA** — [justificativa]
``````
```

### 1.2 Árvore de Raciocínio Multi-Especialista

``````markdown
# PROMPT: Tree of Thought Multi-Expert

## ARQUITETURA

```
                    [OBJETO]
                       |
         ┌─────────────┼─────────────┐
         ▼             ▼             ▼
    BRANCH 1      BRANCH 2      BRANCH 3
   Empiricista   Formalista    Engenheiro
``````

### BRANCH 1: Empiricista
**Especialistas:**
- O Estatístico: análise quantitativa
- O Experimental: design de experimentos

**Cadeia:**
```
🔴 Identificar → Datasets, métricas
🧩 Desmontar → Protocolos, ablations
🧠 Abstrair → Padrões estatísticos
💠 Reconfigurar → Tabelas, gráficos
🏛️ Reaplicar → Recomendações
``````

### BRANCH 2: Formalista
**Especialistas:**
- O Matemático: equações, provas
- O Algebrista: estruturas algébricas
- O Analista: convergência
- O Topologista: geometria

**Cadeia:**
```
🔴 Identificar → Equações, teoremas
🧩 Desmontar → Componentes matemáticos
🧠 Abstrair → Estruturas algébricas
💠 Reconfigurar → Provas formais
🏛️ Reaplicar → Framework teórico
``````

### BRANCH 3: Engenheiro
**Especialistas:**
- O Arquiteto: design de sistemas
- O Implementador: código, otimização
- O Integrador: pipelines

**Cadeia:**
```
🔴 Identificar → Repos, bibliotecas
🧩 Desmontar → Arquitetura, módulos
🧠 Abstrair → Padrões de design
💠 Reconfigurar → Pseudocódigo
🏛️ Reaplicar → Código reprodutível
``````

### SÍNTESE: Filósofo-Alquimista
**Função:**
1. Triangulação cross-branch
2. Resolução de conflitos
3. Integração narrativa
4. Entrega final .md

**Output:** Documento unificado com consenso ≥ 90%
```

### 1.3 Prompts de Diagnóstico Rápido

```markdown```
# PROMPT 21: Diagnóstico de Consistência

Step-Back: derive estabilidade semântica sob variação.

Tarefa: Avalie consistência da resposta em diferentes seeds. 
Calcule métrica 0-1. Liste causas de não-convergência.

Formato: Score + causas + recomendações de ajuste
Cite fontes. Termine com "Evidência—Convergências/Conflitos"

***

# PROMPT 22: Detecção de Erro Modular

Step-Back: derive diagnóstico modular em LLMs.

Tarefa: Identifique módulos que contribuem para erros. 
Sugira experimentos para isolar fonte.

Formato: Diagnóstico + checklist prático
```

---

## 🔬 02_ANÁLISE_SEMÂNTICA

### 2.1 Densidade Semântica (SD)

``````markdown
# PROMPT: Cálculo de SD

Calcule densidade semântica do texto usando:

**Fórmula Base:**
SD = 1 - (E[entropia vetorial] / dispersão média)

**Componentes:**
1. Similaridade inter-sentencial (cosine)
2. Entropia heurística (S_H)
3. Dispersão espacial (pdist)
4. Coerência sequencial
5. Isotropy (uniformidade)

**Métricas Reportadas:**
- SD (composite): [0-1]
- Mean entropy: [bits/token]
- Mean dispersion: [0-1]
- Coherence: [0-1]
- Intrinsic dimension: [int]

**Threshold:** SD ≥ 0.8 para textos coerentes
```

### 2.2 Score(P) Completo

```markdown```
# PROMPT: Score(P) = Σ ωᵢ·ρᵢ·κᵢ - β·S_H

Componentes:
- **ωᵢ** (omega): peso atencional
- **ρᵢ** (rho): densidade semântica
- **κᵢ** (kappa): consistência
- **S_H**: entropia heurística
- **β**: peso penalidade (default: 0.1)

**Análise por Token:**
Para cada token i:
1. ωᵢ = atenção recebida (agregada)
2. ρᵢ = norma + similaridade local
3. κᵢ = 1/(1 + entropy da atenção)

**Análise por Layer:**
- Semantic density por layer
- Coherence evolution
- Isotropy progression

**Output:**
- Score total
- Breakdown por componente
- Token-level contributions
- Layer-wise metrics
```

---

## 🌳 03_RACIOCÍNIO_ESTRUTURADO

### 3.1 Tree-of-Thoughts (ToT)

``````markdown
# PROMPT: Tree-of-Thoughts

**Fonte:** Yao et al., 2023 (arXiv:2305.10601)

## Estrutura

```
# Geração de Pensamento
"""
Brainstorm 3 distinct thoughts for: {problem}
Each thought = intermediate step toward solution
Thoughts:
"""

# Avaliação
"""
Evaluate viability of each thought for: {problem}
Thoughts: {thoughts}
Rate 1-10 with justification.
Evaluation:
"""

# Exploração (BFS/DFS)
"""
Given evaluations, select best path and continue.
Current state: {state}
Best next thought:
"""
``````

**Aplicação EAT:** Circuit discovery, path exploration
```

### 3.2 Graph-of-Thoughts (GoT)

``````markdown
# PROMPT: Graph-of-Thoughts

**Fonte:** Madaan et al., 2023 (arXiv:2308.09787)

## Estrutura

```
def generate_thought(problem, context):
    return f"""
    You are an expert problem-solver.
    Break down: {problem}
    Context: {context}
    
    Generate ONE new thought (concise step).
    Thought:
    """
``````

**Orquestração:**
- Vértices = thoughts
- Arestas = dependencies
- Agregação = fusion de caminhos
- Reutilização = subgrafos compartilhados

**Aplicação EAT:** Multi-path semantic exploration
```

### 3.3 Skeleton-of-Thought (SoT)

``````markdown
# PROMPT: Skeleton-of-Thought

**Fonte:** Ning et al., 2023 (arXiv:2307.15337)

## Estágio 1: Esqueleto

```
Create high-level skeleton for: {request}
List key points/sub-topics covering full answer.
Skeleton:
1. [point 1]
2. [point 2]
...
``````

## Estágio 2: Expansão Paralela

```
Elaborate on skeleton point: {skeleton_point}
Request: {request}
Be detailed and accurate.
Elaboration:
``````

**Aplicação EAT:** Parallel layer analysis
```

***

## 🔄 04_AUTO_CORREÇÃO

### 4.1 Reflexion

```markdown```
# PROMPT: Reflexion

**Fonte:** Shinn et al., 2023 (arXiv:2303.11366)

## Evaluator

```
Assess agent performance:
Task: {task}
Action: {action}
Feedback: {feedback}

Was action successful? Why/why not?
Evaluation:
``````

## Self-Reflection

```
You are self-reflective. Learn from failures.
History: {history}

Based on feedback, reflect:
- What went wrong?
- What to do differently?
Provide actionable advice.

Reflection:
``````

**Aplicação EAT:** Iterative vector refinement
```

### 4.2 Chain-of-Verification (CoVe)

``````markdown
# PROMPT: CoVe

**Fonte:** Dhuliawala et al., 2023 (arXiv:2309.11495)

## 4 Passos

```
Q: {question}

1. Baseline Response:
[generate initial answer]

2. Plan Verification Questions:
[specific, fact-checkable questions]

3. Answer Verification Questions:
[answer each independently]

4. Critical Review:
Compare baseline with verified facts.
Identify inconsistencies.

5. Final Verified Response:
[corrected answer]
``````

**Aplicação EAT:** Hallucination damping
```

---

## ⚙️ 05_INTERAÇÃO_FERRAMENTAS

### 5.1 ReAct

``````markdown
# PROMPT: ReAct

**Fonte:** Yao et al., 2022 (arXiv:2210.03629)

## Formato

```
Question: {question}
Thought: [reasoning]
Action: [Wikipedia[entity] | Search[query]]
Observation: [result]
... (repeat N times)
Thought: I now know the answer
Final Answer: [answer]
``````

**Aplicação EAT:** Tool-augmented steering
```

### 5.2 Program-of-Thoughts (PoT)

``````markdown
# PROMPT: PoT

**Fonte:** Chen et al., 2023 (arXiv:2211.12588)

## Estrutura

```
You are an expert programmer.
Solve via Python code: {problem}

Code should:
- Read problem input
- Compute solution
- Print final answer

``````
# Your code here
```
```

**Aplicação EAT:** Computational verification
```

---

## 🧬 06_META_OTIMIZAÇÃO

### 6.1 APE (Automatic Prompt Engineer)

``````markdown
# PROMPT: APE

**Fonte:** Zhou et al., 2022 (arXiv:2211.01910)

## Meta-Prompt

```
You are an instruction optimizer.
Task: {task_description}
Examples: {demo_examples}

Generate 5 candidate instructions.
Rank best to worst.

Instructions should be:
- Concise
- Clear
- Effective
- Not reference examples

Instructions:
1. [candidate 1]
2. [candidate 2]
...
``````

**Aplicação EAT:** Prompt evolution for Score(P)
```

### 6.2 PromptBreeder

``````markdown
# PROMPT: PromptBreeder Mutation

**Fonte:** Fernando et al., 2023 (arXiv:2309.16797)

## Mutação

```
You are instruction optimizer.
Mutate: {original_instruction}

Mutation types:
- Add constraint ("Think step-by-step")
- Change perspective ("Act as scientist")
- Simplify/detail
- Adjust tone

Mutated Instruction:
``````

**Aplicação EAT:** Evolutionary vector search
```

---

## 👥 07_MULTI_AGENTE

### 7.1 Multi-Agent Debate (MAD)

``````markdown
# PROMPT: MAD

**Fonte:** Du et al., 2023 (arXiv:2305.14325)

## Agent Round

```
You are expert debater.
Question: {question}
History: {debate_history}

Provide next argument:
- New point
- Rebuttal
- Concession

Be concise and factual.
Response:
``````

## Aggregator

```
You are expert judge.
Question: {question}
Full Debate: {full_history}

Synthesize into final answer.
Weigh evidence.
Final Answer:
``````

**Aplicação EAT:** Multi-perspective vector fusion
```

***

## 🎯 08_ABSTRAÇÃO_ANÁLISE

### 8.1 Step-Back Prompting

```markdown```
# PROMPT: Step-Back

**Fonte:** Zheng et al., 2023 (arXiv:2310.06117)

## Estágio 1: Abstração

```
Given specific question: {specific_q}
Take step back.
Ask more general question about underlying concepts.

Step-Back Question:
``````

## Estágio 2: Aplicação

```
General Principle: {answer_to_general}
Specific Question: {specific_q}

Answer specific using general principle.
Answer:
``````

**Aplicação EAT:** Principle extraction from vectors
```

### 8.2 Análise Dialética

``````markdown
# PROMPT: Tese-Antítese-Síntese

## Estrutura

```
Question: {question}

**Step 1: Thesis**
Present clear, argued answer.
[Thesis]

**Step 2: Antithesis**
Act as Devil's Advocate.
Critique thesis rigorously.
[Antithesis]

**Step 3: Synthesis**
Synthesize insights from both.
Develop nuanced conclusion.
[Synthesis]
``````

**Aplicação EAT:** Vector opposition and fusion
```

---

## 🌐 09_ESPAÇO_LATENTE

### 9.1 Exploração Vetorial

``````markdown
# PROMPT: Step-Back Latente

Step-Back: Derive princípio cognitivo do [vetor/embedding].

Tarefa:
1. Qual generalização computacional?
2. Como projeta no espaço latente?
3. Operadores para extração/fusão?

Cite 3 fontes.
Termine com "Convergências/Conflitos"
```

### 9.2 Fusão Dialética

```markdown```
# PROMPT: Fusão Vetorial

Aplique Tese-Antítese-Síntese a vetores v₁, v₂.

**Tese:** vetor-padrão dominante
**Antítese:** vetor de oposição/ruído
**Síntese:** operador de fusão

Explicite:
- Qual operador? (average, maxpool, projection)
- Máxima SD, mínima ambiguidade?

Mostre exemplos. Reporte riscos.
```

### 9.3 Steering e Patching

``````markdown
# PROMPT: Activation Steering

**Fonte:** RepE, ITI (Turner et al., 2023)

Tarefa:
1. Extrair steering vector via diferença de médias
2. Aplicar em layers específicas
3. Medir impacto em:
   - Perplexity
   - Score(P)
   - Behavioral shift

Limitações: interferência, drift
```

### 9.4 SAE Decomposição

```markdown```
# PROMPT: Sparse Autoencoders

**Fonte:** Cunningham et al., 2023

Tarefa:
1. Decompor ativações em features monosemânticas
2. Identificar features críticas para comportamento
3. Mapear para Score(P) components (ω, ρ, κ)

Métricas:
- Sparsity
- Reconstruction loss
- Feature interpretability
```

---

## 📓 10_NOTEBOOKLM_SÍNTESE

### Bloco 1: Prompts Canônicos (1-10)

``````markdown
1. Loop Interno (Auto-Correção)
2. Loop Externo (Ação)
3. Raciocínio Árvore (ToT/GoT)
4. Meta-Otimização (APE/PromptBreeder)
5. Step-Back (Abstração)
6. Átomo Semântico (SAE)
7. Activation Steering
8. Activation Patching
9. Interferência Geométrica
10. Model Merging
```

### Bloco 2: Prompts Avançados (11-20)

```markdown```
11. Robustez (CoVe vs MAD)
12. Meta-Aprendizagem
13. Raciocínio Latente
14. Escalabilidade Geométrica
15. Steering em Produção
16. Mecânica RAG
17. Mecânica CoT
18. Hello World SLE
19. Cognitive Routing
20. ABCLatentMapper
```

### Bloco 3: Complementares (21-30)

``````markdown
21. Diagnóstico Consistência
22. Erro Modular
23. Explicação Leigos
24. Visualização
25. Nova Métrica
26. Workflow Multi-Método
27. Step-Back Puro
28. Avaliação UX
29. Sanity Check
30. Prompt Universal
```

***

## 🛠️ 11_UTILITÁRIOS

### 11.1 Visualização

```markdown```
# PROMPT: Visualização Resume

Step-Back: derive diagnóstico visual.

Tarefa: Gere visualização (tabela, flowchart, heatmap) 
explicando estrutura do resultado.

Sugira interpretação para ação prática.
Cite metodologias para visual analysis.
```

### 11.2 Diagnóstico

``````markdown
# PROMPT: Diagnóstico Pipeline

Step-Back: derive validação cruzada.

Tarefa: Verifique coerência de subetapas do workflow.
Liste inconsistências.
Sugira experimentos A/B.
```

### 11.3 Explicação para Leigos

```markdown```
# PROMPT: Simplificação

Step-Back: derive comunicação clara.

Tarefa: Explique [tema] com analogia prática.
Liste 2-3 implicações concretas.
Use diagramas simples.
```

---

## 📦 EXPORTAÇÃO E USO

### Estrutura de Arquivo

``````
eat-lab-prompts/
├── README.md (este documento)
├── 00_infraestrutura/
│   ├── calibracao.md
│   └── rubric.md
├── 01_extracao/
│   ├── eng_reversa.md
│   ├── arvore_multi_expert.md
│   └── diagnostico_rapido.md
├── 02_semantica/
│   ├── densidade_sd.md
│   ├── score_p.md
│   └── metricas_geometricas.md
├── 03_raciocinio/
│   ├── tot_got_sot.md
│   ├── least_to_most.md
│   └── skeleton.md
├── 04_auto_correcao/
│   ├── reflexion.md
│   ├── cove_rcot.md
│   └── critic.md
├── 05_ferramentas/
│   ├── react.md
│   ├── pot.md
│   └── rag_steering.md
├── 06_meta_otimizacao/
│   ├── ape_promptbreeder.md
│   └── metricas_custom.md
├── 07_multi_agente/
│   ├── mad.md
│   ├── chatdev_dylan.md
│   └── orchestracao.md
├── 08_abstracao/
│   ├── step_back.md
│   ├── dialetica.md
│   └── principles.md
├── 09_latente/
│   ├── exploracao_vetorial.md
│   ├── fusao_composicao.md
│   ├── steering_patching.md
│   └── sae_decomposicao.md
├── 10_notebooklm/
│   ├── bloco1_canonicos.md
│   ├── bloco2_avancados.md
│   └── bloco3_complementares.md
└── 11_utilitarios/
    ├── visualizacao.md
    ├── diagnostico.md
    └── explicacao_leigos.md
```

### Uso Recomendado

```bash```
# Clonar biblioteca
git clone https://github.com/eat-lab/prompts-library.git

# Importar em notebook
from eat_prompts import load_prompt

# Usar prompt específico
prompt = load_prompt('01_extracao/eng_reversa')
response = model.generate(prompt.format(objeto="Causal Tracing"))
```

---

## 📚 REFERÊNCIAS CONSOLIDADAS

**Raciocínio Estruturado:**
- Yao et al., 2023 - Tree of Thoughts (arXiv:2305.10601)
- Madaan et al., 2023 - Graph of Thoughts (arXiv:2308.09787)
- Ning et al., 2023 - Skeleton-of-Thought (arXiv:2307.15337)
- Zhou et al., 2022 - Least-to-Most (arXiv:2208.06851)

**Auto-Correção:**
- Shinn et al., 2023 - Reflexion (arXiv:2303.11366)
- Dhuliawala et al., 2023 - CoVe (arXiv:2309.11495)
- Zhang et al., 2023 - RCoT (arXiv:2305.15820)
- Madaan et al., 2023 - Self-Refine (arXiv:2303.17651)
- Gou et al., 2023 - CRITIC (arXiv:2305.11738)

**Ferramentas:**
- Yao et al., 2022 - ReAct (arXiv:2210.03629)
- Chen et al., 2023 - PoT (arXiv:2211.12588)

**Meta-Otimização:**
- Zhou et al., 2022 - APE (arXiv:2211.01910)
- Fernando et al., 2023 - PromptBreeder (arXiv:2309.16797)

**Multi-Agente:**
- Du et al., 2023 - MAD (arXiv:2305.14325)
- Hong et al., 2023 - ChatDev (arXiv:2307.07924)
- Liu et al., 2023 - DyLAN (arXiv:2310.05706)

**Abstração:**
- Zheng et al., 2023 - Step-Back (arXiv:2310.06117)

**Surveys:**
- Sun et al., 2024 - Prompt Design & Engineering (arXiv:2401.14423)
- GREATERPROMPT, 2025 (arXiv:2504.03975)
- Systematic Survey PE, 2025 (arXiv:2402.07927)

---

**Versão:** 3.0  
**Data:** 2025-11-14  
**Licença:** MIT  
**Manutenção:** EAT-Lab Collaborative

[1](https://arxiv.org/abs/2402.13178)
[2](https://www.mdpi.com/2076-3417/15/11/6225)
[3](http://arxiv.org/pdf/2401.14423.pdf)
