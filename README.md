# Análise de fatores institucionais e estruturais associados à vulnerabilidade educacional na educação básica brasileira: um estudo com microdados do Censo Escolar 2025

## Integrantes

* Nome completo do aluno 1
* Nome completo do aluno 2
* Gabriela Gomes Mattoso 
   gabriela.mattoso@sga.pucminas.br
* Isabella Oliveira Araujo Barbosa Moreira 
   isabella.moreira@sga.pucminas.br
* Lívia Hilbert de Oliveira
   livia.hilbert@sga.pucminas.br

## Professor(es)

* Gabriel Barbosa da Fonseca
* Marco Paulo Soares Gomes


## Síntese

Este trabalho analisa a relação entre fatores institucionais e estruturais das escolas e o risco de evasão escolar na educação básica brasileira, utilizando os microdados do Censo Escolar 2025. Considerando a ausência de variáveis socioeconômicas individuais, a pesquisa concentra-se em características internas das instituições de ensino, como infraestrutura, organização pedagógica e recursos humanos. A partir da integração de diferentes bases de dados, são construídos indicadores que permitem identificar padrões associados a contextos de maior vulnerabilidade educacional. Espera-se que os resultados contribuam para a compreensão do papel das condições escolares na permanência dos estudantes.

## Introdução

A evasão escolar é um dos principais desafios da educação básica no Brasil, impactando diretamente o desenvolvimento social e educacional do país. A permanência dos estudantes na escola está associada a múltiplos fatores, que vão desde condições socioeconômicas até aspectos institucionais e estruturais do sistema educacional.
Embora grande parte da literatura enfatiza fatores socioeconômicos como determinantes da evasão, há uma crescente necessidade de compreender o papel das condições internas das instituições de ensino, como infraestrutura, organização pedagógica e disponibilidade de recursos humanos. Esses fatores podem influenciar diretamente a qualidade da experiência escolar e, consequentemente, a permanência dos alunos.
Nesse contexto, o uso de dados educacionais em larga escala, como os microdados do Censo Escolar da Educação Básica (2025), permite analisar de forma sistemática as características das escolas e sua relação com contextos de maior vulnerabilidade educacional. Este trabalho insere-se na área de Ciência de Dados aplicada à educação, com foco na análise de fatores institucionais e estruturais associados ao risco de evasão escolar.

## Problema

A evasão escolar é um problema multifatorial, cuja análise frequentemente se concentra em fatores socioeconômicos. No entanto, essa abordagem pode limitar a compreensão do papel das condições institucionais e estruturais das escolas no processo de permanência dos estudantes. 

Apesar da disponibilidade de microdados educacionais detalhados, muitas análises não exploram de maneira integrada as características das instituições de ensino, como infraestrutura, organização pedagógica e distribuição dos recursos humanos. Além disso, os dados disponíveis dificultam a análise direta da evasão, exigindo a construção de indicadores indiretos. 

Diante deste cenário, torna-se necessário investigar como fatores institucionais e estruturais das escolas estão associados a contextos de maior risco de evasão escolar, mesmo na ausência de variáveis socioeconômicas individuais

## Objetivo geral

Analisar, com base nos microdados do Censo Escolar 2025, como fatores institucionais e estruturais das escolas estão associados a contextos de maior risco de evasão escolar na educação básica.

### Objetivos específicos

* Construir indicadores institucionais e estruturais das escolas, incluindo razão aluno/docente, tamanho médio das turmas e oferta de ensino em tempo integral.
* Desenvolver um índice de vulnerabilidade educacional baseado em características institucionais, como rede de ensino, localização, disponibilidade de recursos humanos e organização pedagógica.
* Analisar a distribuição do índice de vulnerabilidade entre as escolas, identificando padrões associados a diferentes contextos institucionais (público/privado, urbano/rural).
* Investigar a relação entre os indicadores estruturais das escolas e níveis mais elevados de vulnerabilidade educacional.



# Análise exploratória dos dados

## Dicionário de dados
## Descrição de dados
## Análise das variáveis institucionais do Censo Escolar 2025
## Análise de variáveis binárias

## Análise de variáveis numéricas 




A presença de profissionais de apoio e gestão foi analisada a partir da verificação de escolas com pelo menos um profissional registrado em cada categoria. Para isso, as variáveis quantitativas foram convertidas em indicadores de presença ou ausência, considerando valor maior que zero como presença do profissional. Essa análise permite identificar a cobertura institucional desses recursos humanos nas escolas de ensino médio regular (Figura 9).

### Figura 9 — Presença de profissionais de apoio e gestão nas escolas de ensino médio regular. 

Proporção de escolas que possuem ou não possuem ao menos um profissional em cada categoria analisada, incluindo coordenação, psicologia, assistência social, pedagogia, biblioteconomia e gestão escolar. A presença foi considerada quando a escola registrou quantidade maior que zero para o respectivo profissional.

A análise da presença de profissionais indica que os cargos ligados à organização pedagógica e à gestão são mais frequentes do que os profissionais de apoio psicossocial. Profissionais de pedagogia estão presentes em 80,0% das escolas, e profissionais de gestão escolar em 74,6%. Em contraste, apenas 25,1% das escolas possuem psicólogo e 9,34% possuem assistente social. Isso indica que a maior parte das escolas analisadas não conta com profissionais especializados em apoio psicossocial, aspecto relevante para estudos sobre o abandono escolar. Contudo, essa interpretação deve ser feita com cautela, pois a base registra apenas a presença ou ausência desses profissionais, sem informar carga horária, qualidade do atendimento ou demanda real de cada escola.

Considerando que a evasão escolar é um fenômeno multifatorial, a ausência de profissionais de apoio não pode ser interpretada isoladamente como causa de evasão. No entanto, a baixa cobertura de psicólogos e assistentes sociais pode indicar menor capacidade institucional de acompanhamento de estudantes em situações de vulnerabilidade, especialmente em escolas com grande número de matrículas.

Ao analisar as escolas que possuem pelo menos um profissional de apoio ou gestão (Figura 10). O gráfico evidencia que a simples presença de profissionais de apoio ou gestão não garante a mesma disponibilidade relativa entre as escolas. Categorias como psicólogo e assistente social apresentam maior dispersão e maior número de alunos por profissional, indicando que, mesmo nas escolas que contam com esses profissionais, a capacidade de atendimento pode variar bastante. Já coordenadores e profissionais de pedagogia apresentam valores mais baixos, sugerindo maior cobertura proporcional em relação ao número de matrículas. Essa análise é relevante para o estudo do abandono escolar porque permite observar possíveis desigualdades na capacidade institucional de acompanhamento dos estudantes.

### Figura 10 — Distribuição de alunos por profissional nas escolas que possuem cada categoria. 

Distribuição de alunos por profissional, considerando somente as escolas que possuem pelo menos um profissional daquela categoria. A linha laranja dentro de cada caixa é a mediana. Quanto mais alta a mediana, maior o número típico de alunos por profissional.


A comparação por localização mostra que as escolas urbanas apresentam maior presença de profissionais de apoio e gestão em praticamente todas as categorias analisadas (Figura 11). A diferença é especialmente visível em funções como coordenação, psicologia, biblioteconomia e gestão escolar, sugerindo que escolas urbanas tendem a contar com uma estrutura institucional mais ampla. Nas escolas rurais, a presença desses profissionais é menor, o que pode indicar limitações no acesso a equipes de apoio pedagógico, administrativo e psicossocial. Essa desigualdade territorial é relevante para a análise do abandono escolar, pois a permanência dos estudantes pode depender não apenas da infraestrutura física, mas também da disponibilidade de profissionais capazes de acompanhar demandas pedagógicas, sociais e emocionais. 

### Figura 11 — Presença de profissionais por localização da escola. 

Percentual de escolas urbanas e rurais que possuem ao menos um profissional em cada categoria analisada, incluindo coordenação, psicologia, assistência social, pedagogia, biblioteconomia e gestão escolar.


Quanto à participação institucional considerou três instâncias formais de organização escolar: conselho escolar, grêmio estudantil e associação de pais e mestres. Essas variáveis indicam a presença ou ausência de mecanismos institucionais de participação da comunidade escolar, dos estudantes e das famílias. Como são variáveis binárias, suas médias foram interpretadas como a proporção de escolas que possuem cada instância.

Os resultados mostram que a participação institucional não está distribuída de forma homogênea entre as escolas. Embora o conselho escolar esteja presente na maioria das instituições, menos da metade das escolas possui grêmio estudantil, e aproximadamente um terço possui associação de pais e mestres. Isso pode indicar diferenças na estrutura formal de participação da comunidade escolar, dos estudantes e das famílias.

# Preparação dos Dados
---
## Filtragem da base

A preparação dos dados foi organizada em duas etapas principais. A primeira etapa consistiu na construção da base institucional, a partir do Censo Escolar 2025. Foram selecionadas escolas que ofertam Ensino Médio regular e atributos relacionados à infraestrutura, localização, dependência administrativa, acessibilidade e recursos humanos, participação institucional e matrículas.
O Censo Escolar utiliza o valor 88888 como código sentinela para indicar "informação não disponível" nas variáveis de quantidade de profissionais. Esse valor foi identificado em 14 escolas (para QT_PROF_COORDENADOR). Por não representar um número real de profissionais, foi substituído por NaN e posteriormente preenchido com 0, indicando ausência do profissional. A identificação desse código foi possível pelo padrão de repetição exata do mesmo valor absurdo em múltiplas escolas distintas.

## Feature Engineering — Variáveis derivadas

Além das variáveis originais do Censo, foram criadas variáveis compostas que capturam dimensões institucionais de forma mais abrangente e que se mostraram as mais importantes nos modelos:

| Variável derivada | Escala | Definição e justificativa |
|---|---|---|
| QT_MAT_MED_TOTAL | Contagem | Soma de matrículas diurnas e noturnas — representa o porte da escola |
| PROP_MAT_NOTURNO | 0 a 1 | Proporção de matrículas no turno noturno. Proxy do perfil de vulnerabilidade: alunos noturnos frequentemente conciliam trabalho e escola, aumentando o risco de abandono |
| QT_PROF_APOIO | Contagem | Soma de psicólogos, assistentes sociais, pedagogos e bibliotecários — representa a equipe de suporte psicossocial e pedagógico |
| QT_PROF_GESTAO_COORD | Contagem | Soma de profissionais de gestão e coordenação escolar |
| ALUNOS_POR_PROF_APOIO | Razão | Razão alunos por profissional de apoio (0 quando sem o profissional). Captura a disponibilidade relativa do suporte institucional em função do porte da escola |
| ALUNOS_POR_GESTAO | Razão | Razão alunos por profissional de gestão/coordenação |
| SCORE_CARENCIA_PED | 0 a 6 | Soma de ausências de: biblioteca, lab. ciências, lab. informática, internet para alunos, banda larga e quadra esportiva. Fundamentado no Plano Nacional de Educação (BRASIL, 2014) e na literatura sobre permanência escolar (INEP, 2022; TODOS PELA EDUCAÇÃO, 2024) |
| SCORE_CARENCIA_APOIO | 0 a 3 | Soma de ausências de: psicólogo, assistente social e alimentação escolar. A alimentação escolar (PNAE) é reconhecida pela literatura como fator diretamente associado à permanência, especialmente em contextos de vulnerabilidade socioeconômica (BRASIL, 2009) |

A Figura 12 apresenta a relação entre os scores de carência e a taxa média de abandono escolar. No caso da carência pedagógica, observa-se uma tendência geral de aumento da taxa média de abandono conforme cresce o acúmulo de carências, especialmente nos scores mais altos. No entanto, essa relação não é perfeitamente linear, pois o aumento da taxa não ocorre de forma proporcional entre todos os níveis do score. 
Esses resultados sugerem que a associação entre carências institucionais e abandono escolar pode envolver padrões não lineares e efeitos de limiar. Por isso, modelos baseados em Árvores de decisão, como Random Forest, são metodologicamente adequados para essa análise, pois conseguem capturar relações não lineares e interações entre variáveis. 

### Figura 12 — Relação entre scores de carência e taxa média de abandono.

As barras indicam a taxa média de abandono em cada nível de carência, enquanto a linha laranja representa o número de escolas em cada grupo. A carência pedagógica apresenta tendência geral crescente em relação ao abandono médio, embora de forma não linear. A carência de apoio apresenta padrão menos regular, com maior oscilação entre os níveis do score. Esses resultados sugerem associação entre acúmulo de carências institucionais e abandono escolar, mas não permitem inferir causalidade.
---
## Pré-processamento para modelagem

O pré-processamento foi organizado em dois pipelines distintos:

| Transformação | Pipeline RF (preditivo) | Pipeline Árvore (interpretativo) |
|---|---|---|
| Variáveis binárias | passthrough (já em escala 0-1) | passthrough |
| Variáveis numéricas | StandardScaler (média=0, desvio=1) | passthrough (escala original) |
| Variáveis categóricas | OneHotEncoder (drop='first') | OneHotEncoder (drop='first') |
| Contagens (log1p) | Aplicado antes do pipeline | Não aplicado |

A decisão de usar passthrough (sem StandardScaler) no pipeline da Árvore de Decisão é deliberada: garante que os valores nos nós da árvore apareçam na escala original, tornando as regras diretamente interpretáveis (ex: "proporção de matrículas noturnas > 12%" em vez de "-0,21 desvios padrão"). O Random Forest, por sua vez, usa StandardScaler nas variáveis numéricas para garantir que a importância relativa das features não seja distorcida por diferenças de escala.
A transformação log1p foi aplicada nas variáveis de contagem (QT_MAT_MED_TOTAL, QT_PROF_APOIO, etc.) antes do pipeline do Random Forest. Essa transformação comprime distribuições com cauda longa sem eliminar os outliers, que são dados reais e válidos (escolas grandes coexistem com escolas pequenas no sistema público brasileiro).

## Variáveis-alvo do sistema em cascata

O sistema de alerta opera em duas etapas com variáveis-alvo distintas:

* Etapa 1: Tem abandono: variável binária. "Com_abandono" para escolas com taxa > 0%; "Sem_abandono" para escolas com taxa = 0%.
* Etapa 2: Nível de risco: aplicada apenas às escolas com abandono > 0%. "Alto_risco" para escolas com taxa > 5%; "Risco_moderado" para escolas com taxa entre 0% e 5%.
 
Justificativa do limiar de 5%: O limiar de 5% foi adotado como critério analítico, e não como ponto de corte oficial definido pelo Inep. Essa escolha se justifica porque a mediana da taxa de abandono entre escolas públicas da amostra foi de 2,1%, de modo que o uso da mediana classificaria como alto risco escolas com taxas pouco acima desse valor. Além disso, taxas em torno de 5% aparecem em divulgações e séries educacionais brasileiras como patamares relevantes para o Ensino Médio: segundo divulgação do Inep sobre a 2ª etapa do Censo Escolar 2021, a taxa de abandono do Ensino Médio alcançou o pico de 5,0% em 2021, relevante pelo impacto socioeconômico da pandemia (INEP, 2022).

# Introdução de Modelos 
---
# Resultados 
---
# Conclusões
---
## Principais achados

Este trabalho identificou três fatores institucionais que aparecem de forma consistente em ambos os modelos como os mais associados ao risco de abandono escolar nas escolas públicas de Ensino Médio brasileiro:

1. **Proporção de matrículas no turno noturno:** É o fator com maior poder discriminativo em ambos os modelos. Acima de 12-15%, o risco de abandono eleva-se de forma praticamente incondicional segundo a Árvore de Decisão. Este fator reflete o perfil de vulnerabilidade do aluno noturno, que frequentemente concilia trabalho e escola, estando sujeito a maior risco de abandono por razões externas à escola mas que se manifestam através do perfil de matrícula da instituição.

2. **Participação institucional (grêmio e associação de pais):** O grêmio estudantil é o nó raiz da Árvore de Decisão — o fator com maior poder de divisão de toda a base. Escolas com grêmio e perfil predominantemente diurno apresentam risco moderado independentemente de outros fatores, sugerindo que a participação estudantil institucionalizada funciona como mecanismo de pertencimento e retenção. A associação de pais e mestres atua como fator protetor complementar.

3. **Suporte psicossocial e pedagógico:** A ausência de profissionais de apoio (psicólogo, assistente social, pedagogo) e a carência pedagógica acumulada (score > 5,5 em 6 possíveis) estão consistentemente associadas ao alto risco. A razão alunos por profissional de apoio é a 3ª feature mais importante no Random Forest, indicando que não basta ter o profissional — a capacidade de atendimento relativa ao porte da escola é determinante.

## Sistema de alerta — síntese operacional

O Random Forest otimizado classifica as 18.179 escolas públicas de EM regular em três níveis de alerta, com as seguintes características do conjunto de teste:

- **Alto risco:** 1.121 escolas (31%) | Taxa média real: 6,99% | Mediana: 6,1% — grupo candidato a intervenção prioritária;
- **Risco moderado:** 2.186 escolas (60%) | Taxa média real: 2,17% | Mediana: 1,4% — grupo de monitoramento;
- **Sem abandono:** 329 escolas (9%) | Mediana real: 0,0% — grupo estável.

A lógica do sistema é validada pela mediana: Sem abandono (0,0%) < Risco moderado (1,4%) < Alto risco (6,1%). O sistema comete 304 erros críticos no conjunto de teste (escolas de alto risco real classificadas em nível inferior), o que representa uma taxa de erro crítico de 30,3% para a classe Alto risco.

Esse resultado indica que o sistema possui utilidade como ferramenta exploratória de triagem, mas não deve ser utilizado isoladamente para tomada de decisão. A existência de erros críticos reforça a necessidade de validação externa, atualização dos dados e complementação com informações socioeconômicas e territoriais.

---

## Limitações

- **Gap temporal:** a variável-alvo é de 2024 e os atributos institucionais são de 2025. A análise é exploratória e associativa, não causal.
- **Fatores individuais ausentes:** renda familiar, necessidade de trabalho, distância da escola e histórico escolar do aluno explicam parte relevante do abandono e não estão disponíveis nos microdados do Censo Escolar. Um F1-macro de 0,65 com dados apenas institucionais é resultado esperado e defensável.
- **Qualidade vs. presença:** o Censo registra apenas a presença ou ausência dos recursos, sem informar qualidade, manutenção ou efetivo uso pelos alunos. Uma escola pode ter laboratório de ciências registrado mas em estado precário de uso.
- **Escopo:** a análise cobre apenas escolas públicas com EM regular tradicional. Os resultados não são generalizáveis para EJA, ensino técnico integrado ou escolas privadas.
- **Causalidade:** os modelos identificam associações, não relações causais. Fatores não observados podem explicar simultaneamente a carência institucional e o abandono.
- O sistema de alerta não é determinístico: 15% das escolas do grupo Sem abandono apresentam algum nível de abandono real (média de 2,94%), reflexo do threshold conservador da Etapa 1 e das limitações dos dados disponíveis.

---

## Contribuições

- Demonstração de que fatores institucionais mensuráveis pelo Censo Escolar carregam sinal real sobre o risco de abandono, mesmo na ausência de dados socioeconômicos individuais;
- Construção de um sistema de alerta operacional em cascata com interpretabilidade (Árvore) e acurácia (Random Forest) complementares;
- Identificação do grêmio estudantil como o fator com maior poder discriminativo — achado com implicação direta para políticas de fortalecimento da participação estudantil;
- Evidência quantitativa de que o turno noturno é o proxy institucional mais forte do perfil de vulnerabilidade do estudante.

---

# Referências

BRASIL. Lei nº 9.394, de 20 de dezembro de 1996. Estabelece as diretrizes e bases da educação nacional. *Diário Oficial da União*, Brasília, DF, 23 dez. 1996.

BRASIL. Lei nº 11.947, de 16 de junho de 2009. Dispõe sobre o atendimento da alimentação escolar e do Programa Dinheiro Direto na Escola aos alunos da educação básica (PNAE). *Diário Oficial da União*, Brasília, DF, 17 jun. 2009.

BRASIL. Lei nº 13.005, de 25 de junho de 2014. Aprova o Plano Nacional de Educação - PNE e dá outras providências. *Diário Oficial da União*, Brasília, DF, 26 jun. 2014.

FUNDO DAS NAÇÕES UNIDAS PARA A INFÂNCIA (UNICEF). *Cenário da Exclusão Escolar no Brasil: um alerta sobre os impactos da pandemia da covid-19 na Educação*. Brasília, DF: UNICEF, 2021. Disponível em: https://www.unicef.org/brazil/relatorios/cenario-da-exclusao-escolar-no-brasil. Acesso em: 1 jun. 2026. (Atualize a data de acesso se necessário)

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Resumo Técnico: Censo Escolar da Educação Básica 2021*. Brasília, DF: INEP, 2022.

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Microdados do Censo Escolar da Educação Básica 2025*. Brasília, DF: INEP, 2025.

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Indicadores de Rendimento Escolar da Educação Básica 2024*. Brasília, DF: INEP, 2024.

NERI, M. C. (Coord.). *Motivos da Evasão Escolar*. Rio de Janeiro: FGV/CPS, 2009. Di


  

