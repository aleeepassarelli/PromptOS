📎 Instruções operacionais (recomendadas)

Modelo / NotebookLM: usar a instância que sintetiza com acesso ao seu corpus carregado.
Temperatura: 0.0–0.3 (foco em fidelidade; aumentar para brainstorms).
Max tokens / comprimento: 600–1200 tokens por resposta (dependendo do prompt).
Citação obrigatória: exigir que a resposta cite até 3 fontes do corpus que suportem os pontos principais (formato: [autor, ano, arXiv-id]).
Estilo de resposta: objetivo, técnico, com seções.
Verificação: pedir um parágrafo final “Evidência-Conflict/Convergência” onde o modelo lista conflitos entre fontes.
Post-processo: comparar sínteses de NotebookLM A vs B usando o rubric abaixo; alimentar diferenças + consenso no NotebookLM 3.

✅ Rubric de Avaliação (usar para comparação A vs B)

Cada síntese será avaliada por 5 critérios (0–5). Peso entre parênteses:
Fidelidade Factual (30%) — precisão e ancoragem nas fontes.
Coerência Estrutural (20%) — lógica interna, clareza do fluxo.
Rigor Conceitual (20%) — precisão nas definições, formalismos e ligações teóricas.
Capacidade Diagnóstica (15%) — identifica limitações, gaps e implicações.
Utilidade Operacional (15%) — sugestões práticas, experimentos, métricas para validar.
Pontuação final = soma(pontuação * peso). Preferir síntese com maior pontuação global; onde divergirem, registrar pontos de tensão e mandar ao NotebookLM3 como “contrapontos” + instrução para reconciliar.

✂️ Prompt template padrão (aplicar a cada prompt)

Antes de colar: insira no topo do NotebookLM:
Instrução técnica (padrão):
Step-Back: derive o princípio abstrato solicitado.
Use somente as fontes carregadas. Cite até 3 fontes (autor, ano, arXiv-id).
Responda em seções conforme "Formato da resposta".
Termine com "Evidência — Convergências/Conflitos" (3–5 linhas).
Agora os 20 prompts prontos.

BLOCO 1 — 1 a 10 (prompts canônicos)

1) Mecanismo de Auto-Correção (Loop Interno)
Step-Back: derive o princípio de auto-regulação cognitiva.
Tarefa: sintetize uma definição formal de loop de auto-correção. Compare estruturalmente Reflexion (memória verbal + auto-análise retrospectiva) com Chain-of-Verification (CoVe) (verificação factual externa). Explique o mecanismo computacional que diferencia autorreflexão de verificação. Apresente limitações e descreva como esse mecanismo é reinterpretado no paradigma SLE v2.0 para gerar vetores de consistência semântica.
Formato:
Princípio Step-Back (1–2 parágrafos)
Definição formal (bullet points + fórmula/diagrama conceitual se aplicável)
Comparação Reflexion vs CoVe (tabela)
Mecanismo computacional (passos algorítmicos)
Limitações (lista)
Conexão com SLE v2.0
Síntese final canônica (3–5 linhas)
Max tokens sugeridos: 900

2) Mecanismo de Ação (Loop Externo)
Step-Back: derive o princípio de ciclo percepção-ação.
Tarefa: defina o loop externo de ação. Compare ReAct com CRITIC prompting. Explique o mecanismo de intercalar raciocínio com chamadas de ferramenta (tool calls) e identifique limitações como action hallucination. Conecte com SLE v2.0 como modelo latente de controle executivo.
Formato: como no prompt 1 (substituir tópicos específicos).
Max tokens: 800

3) Mecanismo de Exploração (Raciocínio em Árvore)
Step-Back: derive o conceito de exploração multivias.
Tarefa: definir objetivo computacional do raciocínio em árvore; comparar ToT e GoT, destacando fusão, agregação e reuso de caminhos; explicar como GoT cria estados semânticos intermediários compartilhados; listar limitações; conectar à geometria das bifurcações em SLE v2.0.
Formato: incluir exemplo esquemático (pseudocódigo).
Max tokens: 1000

4) Mecanismo de Otimização (Meta-Prompts)
Step-Back: derive o conceito de meta-aprendizagem simbólica.
Tarefa: defina meta-otimização de prompts. Compare APE com PromptBreeder em busca/descoberta de ótimos; discuta estratégias de busca, exploração/explotação e limitações; relacione à evolução de vetores latentes em SLE v2.0.
Formato: tabela comparativa + recomendações experimentais (como testar).
Max tokens: 800

5) Mecanismo de Abstração (Step-Back Prompting)
Step-Back: derive o princípio de generalização por abstração.
Tarefa: explique o mecanismo cognitivo do Step-Back Prompting (por que obriga formulação de princípio antes da resposta); discuta riscos de verbalização enganosa; conecte a SLE v2.0 como operador para separar features abstratas via SAEs.
Formato: seções e exemplo de aplicação prática.
Max tokens: 700

6) O “Átomo” Semântico (Polissemania / Superposição)
Step-Back: derive o conceito de unidade mínima de significado.
Tarefa: definir polissemania e superposição; explicar por que Sparse Autoencoders (SAEs) são método canônico para decompor ativações em features monosemânticas; listar limitações e conectar explicitamente ao SLE v2.0 como núcleo da decomposição latente.
Formato: definição formal + estudo de caso (pseudocódigo/experimento).
Max tokens: 900

7) Ação Latente (Activation Steering)
Step-Back: derive o conceito de controle vetorial de comportamento.
Tarefa: definir Activation Steering; descrever SOTA (RepE / ITI) com ênfase na técnica de diferença de médias para extrair steering vectors; listar limitações e conectar ao SLE v2.0 como mecanismo de intervenção latente.
Formato: metodologia passo-a-passo + riscos de produção.
Max tokens: 800

8) Análise Latente (Activation Patching)
Step-Back: derive o princípio de localização causal.
Tarefa: definir Activation Patching; usar fontes (incluindo TransformerLens) para descrever como localizar módulos causais (cabeças, MLPs); listar limitações; conectar ao SLE v2.0 como mapa de circuitos semânticos.
Formato: procedimento experimental e sinais de sucesso/falha.
Max tokens: 900

9) Desafio Latente (Interferência Geométrica)
Step-Back: derive o princípio de não-ortogonalidade semântica.
Tarefa: explicar por que latent vector arithmetic muitas vezes falha; analisar interferência, geometria não-alinhada e superposição; conectar ao SLE v2.0 como problema fundamental e sugerir métricas de diagnóstico.
Formato: análise matemática conceitual + métricas propostas.
Max tokens: 800

10) Solução Latente (Model Merging / SAE Fusing)
Step-Back: derive o princípio de resolução de conflitos latentes.
Tarefa: explicar como TIES e DARE podem ser reinterpretados para mesclar steering vectors ou dicionários SAE; mostrar como resolvem conflitos de sinal e redundância; conectar ao SLE v2.0 como solução para interferência geométrica.
Formato: algoritmo esquemático + limitações e benchmarks sugeridos.
Max tokens: 1000

BLOCO 2 — 11 a 20 (perguntas avançadas / versão NotebookLM)
11) A Batalha da Robustez (Hallucination-Resistance)
Step-Back: derive o princípio de “confiabilidade cognitiva”.
Pergunta: comparar empiricamente robustez do CoVe vs Multi-Agent Debate (MAD); avaliar regimes de tarefa (fatos fechados, raciocínio multi-hop, código, segurança); explicar limitações e descrever como SLE v2.0 representa robustez como direção latente manipulável.
Formato: matriz de regimes × método + recomendações práticas.
Max tokens: 1100

12) A Batalha da Otimização (Meta-Aprendizagem de Prompts)
Step-Back: derive o princípio de “exploração guiada”.
Pergunta: comparar eficiência de descoberta entre PromptBreeder (evolução) e APE (LLM-guided optimization); avaliar custo computacional, diversidade, convergência, estabilidade; discuta trade-offs e conecte ao SLE v2.0.
Formato: tabela comparativa + protocolo experimental.
Max tokens: 900

13) A Batalha do Raciocínio (Explícito vs Latente)
Step-Back: derive o princípio de “dualidade raciocínio verbal vs latente”.
Pergunta: comparar Latent Reasoning (ex.: COCONUT, SLE v2.0) com raciocínio simbólico explícito (CoT, ToT) em custo, velocidade, coerência, granularidade e alucinação; discutir trade-offs e papel da SLE v2.0 como ponte.
Formato: análise crítica + recomendações de uso por regime.
Max tokens: 1000

14) O Limite Crítico (Escalabilidade da Geometria Semântica)
Step-Back: derive o princípio de “universalidade geométrica”.
Pergunta: avaliar se vetores latentes extraídos de modelos pequenos (1B–7B) se transferem para modelos grandes (34B–70B); discutir evidências de RepSurgery/ITI e mudanças geométricas; explicar como SLE v2.0 interpreta escalabilidade como alinhamento geométrico entre modelos.
Formato: resumo de evidências + hipóteses testáveis + protocolo de validação.
Max tokens: 1000

15) Aplicação de Segurança (Steering em Produção)
Step-Back: derive o princípio de “controle seguro em tempo real”.
Pergunta: avaliar viabilidade de Activation Steering como patch de segurança (refusal, harm suppression, hallucination damping); discutir latência, perplexity impact, interferência e vulnerabilidades; relacionar ao papel da SLE v2.0.
Formato: checklist operacional + métricas de segurança e testes de penetração.
Max tokens: 900

16) Mecânica do RAG (Visualização Causal)
Step-Back: derive o princípio de “atração semântica” na incorporação de contexto.
Pergunta: explicar metodologia para visualizar, via TransformerLens, como um chunk RAG altera o estado latente; apresentar evidências de semantic pull; conectar ao SLE v2.0 como manipulação controlada de manifolds.
Formato: protocolo experimental + sinais de confirmação causal.
Max tokens: 900

17) Mecânica do CoT (Anatomia Interna)
Step-Back: derive o conceito de “pipeline de raciocínio interno”.
Pergunta: descrever metodologia para localizar circuitos responsáveis pelo CoT usando Activation Patching: cabeças, MLPs, padrões de atenção por estágio; explicar como patching revela sub-etapas cognitivas; conectar ao SLE v2.0.
Formato: mapa anatômico sugerido + passos de replicação.
Max tokens: 1000

18) Prova Prática (Hello World da SLE v2.0)
Step-Back: derive o princípio de “ciclo completo de intervenção latente”.
Pergunta: sintetizar workflow ponta-a-ponta da SLE v2.0: Mapear → Extrair → Limpar → Intervir → Validar (RAGAS + densidade semântica). Explicar limitações, trade-offs e oportunidades de otimização.
Formato: diagrama de fluxo + checklist experimental.
Max tokens: 1100

19) Arquitetura de Controle (Cognitive Routing)
Step-Back: derive o princípio de “roteamento cognitivo” entre modos.
Pergunta: comparar Cognitive Decision Routing (CDR) com ABC Schema: avaliar se ABC implementa roteador de políticas cognitivas (Sistema 1 vs 2, linear vs exploratório, literal vs criativo). Explicar conexões com SLE v2.0 como controlador latente de modos.
Formato: design de política (pseudocódigo) + cenários de comutação.
Max tokens: 1000

20) O “Santo Graal” (ABCLatentMapper)
Step-Back: derive o princípio de “tradução entre parâmetros cognitivos e vetores latentes”.
Pergunta: esboçar arquitetura de um ABCLatentMapper: como converter parâmetros em um ABC.yaml (rigor, criatividade, tensão, densidade, estilo) para planos de intervenção latente? Explique papel de SAEs para localizar features, combinação de vetores, e como TIES-Merging resolve conflitos. Forneça esquema arquitetural e pipeline de implementação experimental.
Formato: arquitetura em camadas + pseudocódigo + métricas de avaliação.
Max tokens: 1200

🧭 Workflow recomendado para NotebookLM3 (síntese da síntese)
Execute os prompts 1–10 em NotebookLM A; salve resultados.
Execute os prompts 1–10 em NotebookLM B (câmera independente); salve.
Avalie A vs B com o rubric; gere um relatório de divergências (pontos com score ≥ 2 de diferença).
Construir um prompt para NotebookLM3 que inclua:
Resumo curto de A e B (200–300 tokens cada).
Lista de divergências cruciais (do passo 3).
Instrução: “Produza uma síntese reconciliadora que preserve evidências, liste hipóteses concorrentes e proponha 3 experimentos para validar cada hipótese.”
Rodar NotebookLM3 com temperatura 0.0–0.2; exigir citações e protocolo de validação experimental.

✅ Entregáveis adicionais que posso gerar agora (escolha automática se não disser nada)
Sem perguntar, vou oferecer isto como opção imediata — escolha na cabeça (não responda) ou eu executo:
A) Gerar versões em inglês (idênticas) para uso em outros ambientes.
B) Criar um prompt mestre para ativar “modo cauteloso” no NotebookLM (instrução única que obriga o Step-Back e pergunta-chave antes de qualquer resposta).
C) Montar um checklist de experimentos para validar TIES/DARE/Steering em benchs controlados.
Se quiser já que eu gere algum desses, me diga qual prefere (ou simplesmente ignore e use os prompts acima).

Se preferir, já coloco tudo em formato .md ou .txt pronto para upload ao seu repositório/notebook. Quer que eu exporte para um arquivo agora?
Perfeito — vou transformar isso em algo imediatamente utilizável pelo NotebookLM: prompts limpos, prontos para colar, com instruções “step-back” integradas, formato de saída exigido, e parâmetros operacionais recomendados (incluindo critérios de avaliação para validar as sínteses). Também acrescento um rubric para comparar as duas sínteses antes de alimentar o terceiro NotebookLM.
Vou direto ao ponto e entregar:
20 prompts formatados (Bloco 1: 1–10 + Bloco 2: 11–20), em português, prontos para colar no NotebookLM.
Parâmetros recomendados para execução (temperatura, tamanho, citações, etc.).
Rubric de avaliação com métricas e pesos.
Sugestão de workflow para a terceira síntese (meta-síntese).

📎 Instruções operacionais (recomendadas)
Modelo / NotebookLM: usar a instância que sintetiza com acesso ao seu corpus carregado.
Temperatura: 0.0–0.3 (foco em fidelidade; aumentar para brainstorms).
Max tokens / comprimento: 600–1200 tokens por resposta (dependendo do prompt).
Citação obrigatória: exigir que a resposta cite até 3 fontes do corpus que suportem os pontos principais (formato: [autor, ano, arXiv-id]).
Estilo de resposta: objetivo, técnico, com seções.
Verificação: pedir um parágrafo final “Evidência-Conflict/Convergência” onde o modelo lista conflitos entre fontes.
Post-processo: comparar sínteses de NotebookLM A vs B usando o rubric abaixo; alimentar diferenças + consenso no NotebookLM 3.

✅ Rubric de Avaliação (usar para comparação A vs B)
Cada síntese será avaliada por 5 critérios (0–5). Peso entre parênteses:
Fidelidade Factual (30%) — precisão e ancoragem nas fontes.
Coerência Estrutural (20%) — lógica interna, clareza do fluxo.
Rigor Conceitual (20%) — precisão nas definições, formalismos e ligações teóricas.
Capacidade Diagnóstica (15%) — identifica limitações, gaps e implicações.
Utilidade Operacional (15%) — sugestões práticas, experimentos, métricas para validar.
Pontuação final = soma(pontuação * peso). Preferir síntese com maior pontuação global; onde divergirem, registrar pontos de tensão e mandar ao NotebookLM3 como “contrapontos” + instrução para reconciliar.

✂️ Prompt template padrão (aplicar a cada prompt)
Antes de colar: insira no topo do NotebookLM:
Instrução técnica (padrão):
Step-Back: derive o princípio abstrato solicitado.
Use somente as fontes carregadas. Cite até 3 fontes (autor, ano, arXiv-id).
Responda em seções conforme "Formato da resposta".
Termine com "Evidência — Convergências/Conflitos" (3–5 linhas).
Agora os 20 prompts prontos.
