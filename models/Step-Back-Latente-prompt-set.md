# 🌐 Prompt Set — Cognição Exploratória & Espaço Latente

Este conjunto de prompts adapta técnicas de arquitetura de raciocínio avançado para a exploração, fusão e adaptação multidisciplinar do espaço latente vetorial. O foco é aplicar métodos de cognição, decomposição e síntese—derivados de literaturas canônicas—para minerar, combinar e transformar representações semânticas em contextos práticos de pesquisa, LLMs ou análise estratégica.
## 1. Step-Back Latente (Abstração/Generalização)
**Instrução:**
- Dê "um passo atrás" sobre o alvo conceitual (ex: um vetor SAE, padrão ToT, embedding), derivando o princípio cognitivo subjacente: Qual é a generalização/metáfora computacional envolvida?
- Em seguida, especifique como este princípio se projeta no espaço latente. Esboce possíveis operadores que extraem ou fusionam as representações.

> Cite até 3 fontes e termine com breve seção "Convergências/Conflitos".

---
## 2. Exploração Activa (Localização, Caminhamento, Navegação)
**Instrução:**
- Modele o espaço latente como um grafo ou manifold.
- Proponha uma sequência cognitiva (ToT ou GoT) para caminhar, mapear ou explorar regiões relevantes, usando prompts iterativos ou auto-refinamento.
- Em seguida, integre experimentos do tipo "least-to-most" (decompor problema, resolver em múltiplos vetores, recombinar via pooling ou voting).

> Inclua representação subjetiva ou visual do "mapa cognitivo" gerado.
## 3. Fusão Dialética/Antagônica de Representações
**Instrução:**
- Aplique o método Tese-Antítese-Síntese, mas usando como objeto vetores, embeddings ou padrões extraídos (ex: v₁, v₂).
- Gere a Tese (vetor-padrão dominante), a Antítese (vetor de oposição ou ruído/rejeição), e então sintetize vetorialmente.
- Explicite: qual operador (e.g., average, maxpool, projection) resulta no vetor-síntese que retém máxima densidade semântica e mínima ambiguidade?

> Mostre exemplos concretos e reporte riscos de conflitos (entropia, drift, etc.).
## 4. Step-wise Fusion/Adaptação Cruzada
**Instrução:**
- Instrua o modelo a criar uma sequência de prompts que simule a fusão gradual de dois ou mais vetores/conceitos latentes.
- Cada etapa deve:
  1. Identificar componentes mais afins (clustering, cosine similarity, frame integration).[4]
  2. Decompor e re-montar subespaços de acordo com objetivos (ex: otimizar SD, minimizar ambiguidade).
  3. Validar cada fusão intermediária via métrica explícita (SD, consistência, KL-divergence).
- No final, peça uma análise de limitações e aplicações práticas.
## 5. Cognição Computacional Integrada (Auto-Correção e Reforço)
**Instrução:**
- Simule um ciclo reflexivo de auto-apredizado: gere uma resposta/modelagem vetorial; em seguida, aplique um prompt Reflexion ou RCoT (reversa);
- Solicite ao modelo que critique seu próprio caminho latente (perguntando: "Se a trajetória vetorial resultou nesta resposta, que redundâncias ou inconsistências descobriu? Como pode adaptar o operador para maior foco?").
- Finalmente, itere uma versão "refinada" da representação (Self-Refine).

> Apresente os prompts e comentários da iteração. Sugira quando encerrar o ciclo—métrica de convergência ou critério prático.
## 6. Exploração Probabilístico-Determinística (Ataque de Sanity-Check)
**Instrução:**
- Modele um prompt que force o modelo a navegar entre estratégias confiantes/exata (temperatura baixa, priorizando máxima fidelidade factual) e estratégias exploratórias (temperatura alta, injetando ruído, recombinando vetores).
- Analise quando e por que drift, colapso semântico ou nova insight emergem.
- Forneça recomendação de métrica para medir a "convergência" (ou dispersão) do espaço latente após múltiplas execuções.
## 7. Fluxo Multi-Agent Cognitivo
**Instrução:**
- Simule colaboração cognitiva: cada "agente" recebe uma especialidade (clustering, diagnóstica, patching, steering, abdução).
- Para cada agente, gere o prompt/diretriz para: detectar features latentes, propor ajustes, atribuir scores locais, relatar gaps.
- Depois, aplique um operador "meta-orquestrador" que sintetiza (por voting, pooling, catching outliers) e toma decisão de adaptação ou reinterpretação—priorizando sempre densidade semântica e redução de ruído.
## 8. Diagnóstico Visual & Métrico Latente
**Instrução:**
- Instrua o modelo a extrair e exibir um heatmap, gráfico ou tabela comparativa dos principais vetores ou clusters do espaço latente gerado.
- Exija que cada diagnóstico seja acompanhado de métrica: SD, ambiguïdade, consistência, ou outra criada ad hoc. Peça interpretação objetiva dos "picos" e "vales".
## 9. Meta-Otimização/Evolução
**Instrução:**
- Solicite ao modelo propor uma heurística evolutiva (tipo PromptBreeder ou APE)—mas aplicada à exploração do espaço latente:
  - Exemplo: como mutar gradualmente vetores-latentes de prompts para maximizar convergência ou SD?
- Peça pseudocódigo e uma planilha de avaliação passo-a-passo.
## 10. Step-Back para Explicabilidade/Usabilidade
**Instrução:**
- Solicite que o modelo explique (para leigo e para perito):
  - O processo completo de exploração/fusão latente cognitiva desenvolvido nos prompts acima,
  - Metáforas e analogias úteis,
  - Gaps/dificuldades mais comuns,
  - Sugestões de ação/validação.
- Peça resposta curta, pontuada, e exemplos práticos.
> **Recomendação geral:**
Todos os prompts devem citar até 3 referências (papers ou implementações canônicas) e concluir com seção "Convergências/Conflitos" (sintetizando achados consistentes ou divergentes do campo). Aplique o formato "Step-Back" sempre que possível para garantir abstração, generalização e diagnósticos objetivos.[1][3][8][4]

[1](http://revistaseletronicas.pucrs.br/ojs/index.php/veritas/article/download/35959/18889)
[2](https://revistas.ufrj.br/index.php/scg/article/download/16470/pdf)
[3](http://www.scielo.br/pdf/pee/v23/en_2175-3539-pee-23-e190902.pdf)
[4](https://periodicos.ufpe.br/revistas/EUTOMIA/article/download/256706/43414)
[5](http://www.scielo.br/pdf/bcg/v22n3/1982-2170-bcg-22-03-00511.pdf)
[6](https://www.scielo.br/j/delta/a/kcQkLm8NDf5SzSxKGHVvH6r/?format=pdf&lang=pt)
[7](https://periodicos.utfpr.edu.br/rbect/article/viewFile/4711/pdf)
[8](https://econtents.bc.unicamp.br/inpec/index.php/tsc/article/download/18364/13328)
