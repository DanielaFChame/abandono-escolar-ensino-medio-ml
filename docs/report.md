# Análise de fatores institucionais e estruturais associados ao abandono escolar no Ensino Médio brasileiro: um estudo com dados do Censo Escolar 2025 e das Taxas de Rendimento Escolar 2024

**Gabriela Gomes Mattoso**, gabriela.mattoso@sga.pucminas.br
**Daniela Ferreira Chame**, daniela.chame@sga.pucminas.br
**Giovanna Brito Silva Ribeiro**, gbsribeiro@sga.pucminas.br
**Isabella Oliveira Araujo Barbosa Moreira**, isabella.moreira.1630865@sga.pucminas.br
**Lívia Hilbert de Oliveira**, livia.hilbert@sga.pucminas.br

**Professores:** Prof. Gabriel Barbosa da Fonseca e Prof. Marco Paulo Soares Gomes

Curso de Ciência de Dados, Unidade Praça da Liberdade
Instituto de Informática e Ciências Exatas – Pontifícia Universidade de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil

---

Este trabalho analisa a relação entre características institucionais e estruturais das escolas públicas de Ensino Médio e a ocorrência de abandono escolar no Brasil. Para isso, foram integradas informações do Censo Escolar 2025, contendo atributos de infraestrutura, localização, dependência administrativa, acessibilidade, recursos humanos e participação institucional, com as Taxas de Rendimento Escolar de 2024, das quais foi extraída a taxa oficial de abandono total do Ensino Médio por escola. A análise foi delimitada às escolas públicas que ofertam Ensino Médio regular, garantindo maior homogeneidade e relevância para políticas públicas. A partir dos dados integrados, foram aplicados dois modelos supervisionados com papéis complementares: uma Árvore de Decisão para identificação e interpretação dos fatores institucionais associados ao abandono, e um Random Forest otimizado para a construção de um sistema de alerta preditivo em cascata. O sistema classifica as escolas em três níveis de risco — Sem abandono, Risco moderado e Alto risco —, com base em atributos mensuráveis do Censo Escolar. Os resultados indicam que proporção de matrículas no turno noturno, presença de grêmio estudantil, carência pedagógica acumulada e disponibilidade de profissionais de apoio psicossocial são os fatores institucionais mais consistentemente associados ao risco de abandono. Os resultados devem ser interpretados como exploratórios e associativos, não causais, dado que fatores individuais como renda familiar e necessidade de trabalho não estão disponíveis na base analisada.

---

## Introdução

O abandono escolar no Ensino Médio é um dos desafios centrais da educação básica brasileira, pois representa a interrupção da trajetória escolar durante o ano letivo e pode anteceder situações posteriores de evasão. Embora a permanência dos estudantes dependa de múltiplos fatores, incluindo condições socioeconômicas, familiares e territoriais, as características internas das escolas também podem influenciar a experiência educacional dos alunos (NERI, 2009; UNICEF, 2021).

Nesse sentido, aspectos como infraestrutura física, disponibilidade de recursos pedagógicos, acessibilidade, presença de profissionais de apoio, organização institucional e localização da escola podem estar associados à maior ou menor capacidade da instituição de favorecer a permanência dos estudantes. No entanto, essas dimensões nem sempre são analisadas de forma integrada em bases educacionais de larga escala.

Este trabalho utiliza técnicas de Ciência de Dados para investigar a associação entre atributos institucionais das escolas e a ocorrência de abandono escolar no Ensino Médio. Foram utilizados dados do Censo Escolar 2025 e das taxas de rendimento escolar de 2024. O estudo adota dois objetivos complementares: (1) um objetivo descritivo, que busca identificar e explicar quais fatores institucionais estão associados ao abandono; e (2) um objetivo preditivo, que visa construir um sistema de alerta capaz de classificar cada escola em níveis de risco. Os resultados devem ser interpretados como associações exploratórias e não como evidência causal direta.

---

## Contextualização

A evasão escolar pode ser compreendida como parte de um processo mais amplo de exclusão educacional. Dentro desse processo, o abandono escolar é uma etapa especialmente relevante, pois ocorre quando o estudante deixa de frequentar a escola ao longo do ano letivo. Já a evasão se refere à não continuidade dos estudos no período subsequente (BRASIL, 1996; INEP, 2022).

Por esse motivo, a taxa de abandono escolar é uma medida relevante para estudar os riscos associados à permanência dos estudantes. Diferentemente de um índice sintético construído a partir de pesos atribuídos às variáveis institucionais, a taxa de abandono é um dado observado nas estatísticas oficiais de rendimento escolar. Assim, sua utilização como variável-alvo torna a análise mais diretamente conectada ao fenômeno educacional investigado.

---

## Problema

O abandono escolar é um fenômeno multifatorial, influenciado por fatores individuais, familiares, socioeconômicos, territoriais e institucionais. No entanto, muitas bases educacionais públicas disponíveis em larga escala não incluem informações individuais detalhadas dos estudantes, como renda familiar, necessidade de trabalhar, histórico de reprovação, condições de transporte ou contexto familiar.

Diante dessa limitação, torna-se relevante investigar em que medida os atributos disponíveis no nível da escola podem contribuir para diferenciar instituições com e sem registro de abandono escolar. Assim, o problema deste trabalho pode ser formulado da seguinte maneira:

> **Quais características institucionais e estruturais das escolas estão associadas à ocorrência de abandono escolar no Ensino Médio?**

---

## Objetivo Geral

Analisar se características institucionais e estruturais das escolas estão associadas à ocorrência de abandono escolar no Ensino Médio, utilizando a taxa oficial de abandono de 2024 como variável-alvo e os atributos institucionais do Censo Escolar 2025 como variáveis explicativas.

---

## Objetivos Específicos

- Filtrar a base para escolas públicas que ofertam Ensino Médio regular, garantindo homogeneidade analítica e relevância para políticas públicas;
- Integrar os dados institucionais do Censo Escolar 2025 com as Taxas de Rendimento Escolar de 2024 pela chave `CO_ENTIDADE`;
- Construir variáveis compostas que capturam dimensões de carência institucional não disponíveis diretamente no Censo;
- Preparar variáveis explicativas relacionadas à infraestrutura, acessibilidade, localização, dependência administrativa, participação institucional e recursos humanos;
- Aplicar uma Árvore de Decisão como modelo descritivo para identificar regras interpretáveis de associação entre atributos institucionais e abandono;
- Aplicar um Random Forest otimizado como modelo preditivo para construir um sistema de alerta em cascata com três níveis de risco;
- Identificar os fatores institucionais mais relevantes pela convergência entre os dois modelos;
- Discutir as limitações da análise, especialmente a defasagem temporal entre abandono de 2024 e atributos institucionais de 2025, além da ausência de dados individuais dos estudantes.

---

## Justificativas

A utilização da taxa de abandono escolar de 2024 justifica-se pela disponibilidade das Taxas de Rendimento Escolar no momento da análise. Embora a base institucional utilizada seja referente ao Censo Escolar 2025, os dados de rendimento de 2025 ainda não estavam disponíveis para a construção da variável-alvo por escola durante o desenvolvimento deste trabalho.

Dessa forma, adotou-se a taxa oficial de abandono total do Ensino Médio de 2024 como indicador observável do fenômeno analisado. Os atributos institucionais foram extraídos da base escolar de 2025 porque essa base apresentava maior completude em relação às características estruturais consideradas no estudo, incluindo infraestrutura, acessibilidade, conectividade, recursos humanos, localização e dependência administrativa.

Essa escolha, no entanto, impõe uma limitação temporal relevante: a variável-alvo corresponde ao abandono observado em 2024, enquanto as variáveis explicativas correspondem às condições institucionais registradas em 2025. Por esse motivo, os resultados devem ser interpretados como associações exploratórias entre características escolares e abandono, e não como evidência causal direta.

A análise foi restrita às escolas públicas porque a distribuição da taxa de abandono nas escolas privadas apresentou comportamento muito distinto. Segundo os dados analisados, 93% das escolas privadas apresentaram taxa de abandono igual a zero, contra aproximadamente 28% das escolas públicas. A inclusão das escolas privadas poderia levar os modelos a capturar principalmente diferenças entre redes administrativas, reduzindo a capacidade de identificar padrões institucionais relevantes no conjunto de escolas públicas, que constitui o foco principal deste estudo.

A escolha de dois modelos com papéis distintos — Árvore de Decisão para interpretação e Random Forest para predição — decorre da dupla finalidade da pesquisa. A Árvore de Decisão permite identificar regras mais simples e interpretáveis, úteis para a compreensão dos padrões encontrados. O Random Forest, por sua vez, tende a apresentar melhor desempenho preditivo e maior robustez, sendo mais adequado para a construção de um sistema de alerta exploratório.

---

## Público-alvo

O público-alvo deste trabalho é composto por:

- **Gestores educacionais**, interessados em compreender como características institucionais impactam a permanência escolar;
- **Pesquisadores** das áreas de educação;
- **Formuladores de políticas públicas**: Ministério da Educação, Secretarias Estaduais de Educação, etc.

---

## Análise Exploratória dos Dados

### Dicionário de Dados

O projeto utiliza três bases de dados integradas pela chave `CO_ENTIDADE`, código único que identifica cada estabelecimento de ensino no Brasil (INEP, 2024; INEP, 2025):

| Base | Ano | Papel |
|------|-----|-------|
| `Tabela_Escola_2025.csv` | 2025 | Atributos institucionais das escolas (features) |
| `Tabela_Matricula_2025.csv` | 2025 | Quantitativo de matrículas no EM regular |
| `tx_rend_escolas_2024.xlsx` | 2024 | Taxa oficial de abandono do EM por escola (variável-alvo) |

As variáveis foram organizadas em grupos conforme sua natureza e dimensão institucional.

**Variáveis de identificação e controle:**

| Variável | Descrição | Tipo |
|----------|-----------|------|
| `CO_ENTIDADE` | Código único da escola | Identificador |
| `IN_COMUM_MEDIO_MEDIO` | Indica se a escola oferta ensino médio regular tradicional | Binária |
| `QT_MAT_MED_D` | Quantidade de matrículas no ensino médio regular diurno | Numérica |
| `QT_MAT_MED_N` | Quantidade de matrículas no ensino médio regular noturno | Numérica |
| `TP_DEPENDENCIA` | Dependência administrativa da escola: federal, estadual, municipal ou privada | Categórica |
| `TP_LOCALIZACAO` | Localização da escola: urbana ou rural | Categórica |
| `3_CAT_MED` (`TX_ABANDONO_MED`) | Taxa oficial de abandono total do EM em 2024 (%) | Numérica |

**Atributos institucionais por dimensão:**

| Dimensão | Atributos Utilizados | Tipos de dados |
|----------|---------------------|----------------|
| Infraestrutura básica | `IN_AGUA_POTAVEL`, `IN_ENERGIA_REDE_PUBLICA`, `IN_ESGOTO_REDE_PUBLICA`, `IN_ESGOTO_INEXISTENTE`, `IN_BANHEIRO`, `IN_BANHEIRO_PNE`, `IN_COZINHA`, `IN_REFEITORIO`, `IN_ALIMENTACAO` | Binário |
| Infraestrutura pedagógica e tecnológica | `IN_BIBLIOTECA`, `IN_SALA_LEITURA`, `IN_LABORATORIO_CIENCIAS`, `IN_LABORATORIO_INFORMATICA`, `IN_COMPUTADOR`, `IN_INTERNET`, `IN_INTERNET_ALUNOS`, `IN_BANDA_LARGA`, `IN_EQUIP_MULTIMIDIA` | Binário |
| Ambiente escolar | `IN_AREA_VERDE`, `IN_PATIO_COBERTO`, `IN_QUADRA_ESPORTES`, `IN_QUADRA_ESPORTES_COBERTA` | Binário |
| Acessibilidade | `IN_ACESSIBILIDADE_RAMPAS`, `IN_ACESSIBILIDADE_PISOS_TATEIS`, `IN_ACESSIBILIDADE_SINAL_VISUAL`, `IN_ACESSIBILIDADE_INEXISTENTE`, `IN_SALA_ATENDIMENTO_ESPECIAL` | Binário |
| Recursos humanos | `QT_PROF_COORDENADOR`, `QT_PROF_PSICOLOGO`, `QT_PROF_ASSIST_SOCIAL`, `QT_PROF_PEDAGOGIA`, `QT_PROF_BIBLIOTECARIO`, `QT_PROF_GESTAO` | Numérico |
| Participação institucional | `IN_ORGAO_CONSELHO_ESCOLAR`, `IN_ORGAO_GREMIO_ESTUDANTIL`, `IN_ORGAO_ASS_PAIS_MESTRES` | Binário |

### Descrição de Dados

A base de escolas do Censo Escolar 2025 contém 180.565 estabelecimentos. Após filtrar apenas as escolas com `IN_COMUM_MEDIO_MEDIO == 1`, foram identificadas 26.822 escolas com oferta de Ensino Médio regular tradicional, correspondentes a 14,86% da base original. Essa delimitação foi necessária para garantir comparabilidade entre as instituições e adequação ao objetivo do estudo.

A integração com a base de matrículas e com as taxas de rendimento de 2024 resultou em uma base final de 25.704 escolas. Dessas, foram mantidas apenas as escolas públicas (federais, estaduais e municipais), totalizando 18.179 escolas — a base efetiva de modelagem.

| Etapa de Filtragem | Escolas | % da base anterior |
|--------------------|---------|-------------------|
| Base original Censo Escolar 2025 | 180.565 | — |
| EM regular (`IN_COMUM_MEDIO_MEDIO == 1`) | 26.822 | 14,86% |
| Com matrícula no EM diurno ou noturno | 26.811 | 99,96% |
| Com dado de abandono 2024 disponível | 25.704 | 95,87% |
| Apenas escolas públicas (base de modelagem) | 18.179 | 70,72% |

Antes da modelagem, foi analisada a distribuição do abandono por rede administrativa. Os dados indicam que as escolas privadas apresentam uma distribuição muito distinta das escolas públicas: 93% das escolas privadas possuem taxa de abandono igual a zero, contra aproximadamente 28% das escolas públicas.

![Figura 1 — Taxa média de abandono e percentual de escolas com abandono zero por rede administrativa](images/figura1.png)

*Figura 1 — Taxa média de abandono e percentual de escolas com abandono zero por rede administrativa. 93% das escolas privadas apresentam uma taxa de abandono zero, por razões estruturalmente distintas das escolas públicas.*

| Rede | Escolas | Taxa média (%) | Mediana (%) | % com taxa zero |
|------|---------|---------------|-------------|-----------------|
| Estadual | 18.014 | 3,70 | 2,10 | 27,2% |
| Municipal | 107 | 3,14 | 0,80 | 40,2% |
| Federal | 58 | 1,23 | 0,00 | 56,9% |
| Privada | 7.525 | 0,15 | 0,00 | 93,0% |

A inclusão de escolas privadas poderia introduzir viés na modelagem, levando o algoritmo a associar a rede privada à ausência de abandono, em vez de identificar padrões institucionais relevantes entre as escolas públicas.

![Figura 2 — Distribuição da taxa de abandono nas escolas públicas do Ensino Médio Regular](images/figura2.png)

*Figura 2 — Distribuição da taxa de abandono nas escolas públicas do Ensino Médio Regular. À esquerda: histograma com limiar de 5% (alto risco) marcado em vermelho. À direita: número de escolas por nível de abandono.*

Das 18.179 escolas públicas, 5.029 (27,7%) apresentam taxa de abandono igual a 0%; 8.269 (45,5%) têm abandono baixo (0–5%); e 4.881 (26,8%) apresentam abandono elevado (acima de 5%). A distribuição é fortemente assimétrica à direita, com mediana de 2,1% e média de 3,69%. Esse padrão sugere que a relação entre atributos institucionais e abandono pode não ser linear. Por isso, modelos baseados em árvores de decisão são adequados para esta análise, pois conseguem capturar interações entre variáveis e padrões não lineares sem exigir pressupostos de linearidade.

### Análise das Variáveis Institucionais do Censo Escolar 2025

As análises a seguir consideram todas as 26.822 escolas com EM regular, não apenas as públicas, para descrever o panorama geral da infraestrutura escolar brasileira.

Buscando identificar associações exploratórias entre indicadores de matrícula, infraestrutura, acessibilidade, recursos humanos e participação institucional, foi construída uma matriz de correlação (Figura 3). No heatmap, tons avermelhados indicam correlações positivas, tons azulados indicam correlações negativas e tons próximos ao cinza indicam correlações próximas de zero. A diagonal principal aparece em vermelho intenso porque representa a correlação de cada variável consigo mesma, sempre igual a 1.

De modo geral, observa-se predominância de correlações fracas ou moderadas, indicando que os indicadores escolares analisados representam dimensões distintas da estrutura institucional. As variáveis de infraestrutura apresentam alguns agrupamentos positivos, sugerindo que determinados recursos — como biblioteca, laboratórios, computadores, internet, quadra esportiva e espaços de apoio — tendem a ocorrer de forma combinada em parte das escolas.

![Figura 3 — Matriz de correlação entre indicadores escolares](images/figura3.png)

*Figura 3 — Matriz de correlação entre indicadores escolares. O heatmap apresenta as correlações entre variáveis de matrícula, infraestrutura, acessibilidade, recursos humanos e participação institucional das escolas de ensino médio regular. Tons vermelhos indicam correlação positiva, tons azuis indicam correlação negativa e tons próximos ao cinza indicam correlação próxima de zero.*

#### Análise de Variáveis Binárias

Para o caso das variáveis binárias (0 = ausência, 1 = presença), a média representa a proporção de escolas com determinada infraestrutura.

Quanto à **infraestrutura básica** (Figura 4), recursos essenciais como água potável, energia elétrica, banheiro e internet apresentam alta cobertura entre as escolas analisadas. No entanto, outros elementos estruturais, como refeitório, alimentação escolar e esgotamento sanitário pela rede pública, podem apresentar percentuais menores, indicando que a disponibilidade de infraestrutura básica não é homogênea entre todos os aspectos avaliados.

![Figura 4 — Presença de infraestrutura básica nas escolas de ensino médio regular](images/figura4.png)

*Figura 4 — Presença de infraestrutura básica nas escolas de ensino médio regular. Percentual de escolas que possuem recursos básicos de funcionamento, como água potável, energia elétrica da rede pública, banheiro, cozinha, alimentação escolar, esgoto da rede pública e refeitório.*

A **infraestrutura pedagógica** (Figura 5) possui alta presença de recursos tecnológicos básicos, como internet, computadores e banda larga. No entanto, recursos diretamente associados ao apoio pedagógico especializado, como biblioteca, laboratório de informática, laboratório de ciências e sala de leitura, apresentam percentuais menores. Esse resultado sugere que o acesso à conectividade e equipamentos é mais amplo do que a presença de espaços pedagógicos estruturados para leitura, experimentação científica e atividades educacionais específicas.

![Figura 5 — Presença de infraestrutura pedagógica e tecnológica nas escolas de ensino médio regular](images/figura5.png)

*Figura 5 — Presença de infraestrutura pedagógica e tecnológica nas escolas de ensino médio regular. Percentual de escolas que possuem recursos pedagógicos e tecnológicos, como internet, computadores, banda larga, equipamentos multimídia, internet para alunos, biblioteca, laboratório de informática, laboratório de ciências e sala de leitura. Como as variáveis são binárias, os percentuais indicam a proporção de escolas em que cada recurso está presente.*

A análise dos **espaços físicos escolares** (Figura 6) sugere que estruturas voltadas a atividades esportivas e convivência estão presentes em parte expressiva das instituições, especialmente quadras esportivas, pátios cobertos e quadras cobertas. No entanto, a menor presença de áreas verdes indica uma limitação em relação a espaços de contato com o ambiente natural e de convivência ao ar livre.

![Figura 6 — Ambiente escolar e espaços físicos nas escolas de ensino médio regular](images/figura6.png)

*Figura 6 — Ambiente escolar e espaços físicos nas escolas de ensino médio regular. Percentual de escolas que possuem espaços físicos complementares, como quadra esportiva, pátio coberto, quadra coberta e área verde. Como as variáveis são binárias, os percentuais indicam a proporção de escolas em que cada estrutura está presente.*

Quanto aos **recursos de acessibilidade** (Figura 7), observa-se uma diferença importante entre adaptações mais básicas e recursos mais específicos de inclusão. A presença de rampas em grande parte das escolas indica algum avanço na adaptação física dos espaços, mas os percentuais menores de pisos táteis, sinalização visual acessível e salas de atendimento especializado sugerem que a acessibilidade ainda tende a ser parcial. Além disso, a presença de escolas com acessibilidade inexistente evidencia que ainda há instituições sem recursos mínimos registrados nessa dimensão.

![Figura 7 — Recursos de acessibilidade nas escolas de ensino médio regular](images/figura7.png)

*Figura 7 — Recursos de acessibilidade nas escolas de ensino médio regular. Percentual de escolas que possuem recursos de acessibilidade, como rampas, sala de atendimento especializado, pisos táteis e sinalização visual acessível.*

A **comparação entre escolas urbanas e rurais** (Figura 8) evidencia desigualdades territoriais na distribuição de infraestrutura escolar. De modo geral, as escolas urbanas apresentam maior presença de recursos como esgotamento sanitário pela rede pública, quadra esportiva, quadra coberta, laboratórios, banheiro acessível, pátio coberto, biblioteca e sala de leitura. A alimentação escolar aparece como exceção, com maior presença nas escolas rurais, o que pode estar relacionado à importância desse serviço em contextos de maior vulnerabilidade territorial.

![Figura 8 — Maiores diferenças de infraestrutura entre escolas urbanas e rurais](images/figura8.png)

*Figura 8 — Maiores diferenças de infraestrutura entre escolas urbanas e rurais. Comparação dos indicadores com maior diferença percentual entre escolas urbanas e rurais, considerando recursos de infraestrutura básica, pedagógica, tecnológica e de apoio escolar. As barras indicam a proporção de escolas que possuem cada recurso em cada localização.*

#### Análise de Variáveis Numéricas

A presença de profissionais de apoio e gestão foi analisada a partir da verificação de escolas com pelo menos um profissional registrado em cada categoria. Para isso, as variáveis quantitativas foram convertidas em indicadores de presença ou ausência, considerando valor maior que zero como presença do profissional.

![Figura 9 — Presença de profissionais de apoio e gestão nas escolas de ensino médio regular](images/figura9.png)

*Figura 9 — Presença de profissionais de apoio e gestão nas escolas de ensino médio regular. Proporção de escolas que possuem ou não possuem ao menos um profissional em cada categoria analisada, incluindo coordenação, psicologia, assistência social, pedagogia, biblioteconomia e gestão escolar. A presença foi considerada quando a escola registrou quantidade maior que zero para o respectivo profissional.*

A análise da presença de profissionais indica que os cargos ligados à organização pedagógica e à gestão são mais frequentes do que os profissionais de apoio psicossocial. Profissionais de pedagogia estão presentes em 80,0% das escolas, e profissionais de gestão escolar em 74,6%. Em contraste, apenas 25,1% das escolas possuem psicólogo e 9,34% possuem assistente social. Isso indica que a maior parte das escolas analisadas não conta com profissionais especializados em apoio psicossocial, aspecto relevante para estudos sobre o abandono escolar. Contudo, essa interpretação deve ser feita com cautela, pois a base registra apenas a presença ou ausência desses profissionais, sem informar carga horária, qualidade do atendimento ou demanda real de cada escola.

Considerando que a evasão escolar é um fenômeno multifatorial, a ausência de profissionais de apoio não pode ser interpretada isoladamente como causa de evasão. No entanto, a baixa cobertura de psicólogos e assistentes sociais pode indicar menor capacidade institucional de acompanhamento de estudantes em situações de vulnerabilidade, especialmente em escolas com grande número de matrículas.

![Figura 10 — Distribuição de alunos por profissional nas escolas que possuem cada categoria](images/figura10.png)

*Figura 10 — Distribuição de alunos por profissional, considerando somente as escolas que possuem pelo menos um profissional daquela categoria. A linha laranja dentro de cada caixa é a mediana. Quanto mais alta a mediana, maior o número típico de alunos por profissional.*

A comparação por localização mostra que as escolas urbanas apresentam maior presença de profissionais de apoio e gestão em praticamente todas as categorias analisadas (Figura 11). A diferença é especialmente visível em funções como coordenação, psicologia, biblioteconomia e gestão escolar, sugerindo que escolas urbanas tendem a contar com uma estrutura institucional mais ampla.

![Figura 11 — Presença de profissionais por localização da escola](images/figura11.png)

*Figura 11 — Presença de profissionais por localização da escola. Percentual de escolas urbanas e rurais que possuem ao menos um profissional em cada categoria analisada, incluindo coordenação, psicologia, assistência social, pedagogia, biblioteconomia e gestão escolar.*

Quanto à **participação institucional**, foram consideradas três instâncias formais de organização escolar: conselho escolar, grêmio estudantil e associação de pais e mestres. Os resultados mostram que a participação institucional não está distribuída de forma homogênea entre as escolas. Embora o conselho escolar esteja presente na maioria das instituições, menos da metade das escolas possui grêmio estudantil, e aproximadamente um terço possui associação de pais e mestres.

---

## Preparação dos Dados

### Filtragem da Base

A preparação dos dados foi organizada em duas etapas principais. A primeira etapa consistiu na construção da base institucional, a partir do Censo Escolar 2025. Foram selecionadas escolas que ofertam Ensino Médio regular e atributos relacionados à infraestrutura, localização, dependência administrativa, acessibilidade e recursos humanos, participação institucional e matrículas.

O Censo Escolar utiliza o valor `88888` como código sentinela para indicar "informação não disponível" nas variáveis de quantidade de profissionais. Esse valor foi identificado em 14 escolas (para `QT_PROF_COORDENADOR`). Por não representar um número real de profissionais, foi substituído por `NaN` e posteriormente preenchido com `0`, indicando ausência do profissional.

### Feature Engineering — Variáveis Derivadas

Além das variáveis originais do Censo, foram criadas variáveis compostas que capturam dimensões institucionais de forma mais abrangente:

| Variável derivada | Escala | Definição e justificativa |
|-------------------|--------|--------------------------|
| `QT_MAT_MED_TOTAL` | Contagem | Soma de matrículas diurnas e noturnas — representa o porte da escola |
| `PROP_MAT_NOTURNO` | 0 a 1 | Proporção de matrículas no turno noturno. Proxy do perfil de vulnerabilidade: alunos noturnos frequentemente conciliam trabalho e escola, aumentando o risco de abandono |
| `QT_PROF_APOIO` | Contagem | Soma de psicólogos, assistentes sociais, pedagogos e bibliotecários — representa a equipe de suporte psicossocial e pedagógico |
| `QT_PROF_GESTAO_COORD` | Contagem | Soma de profissionais de gestão e coordenação escolar |
| `ALUNOS_POR_PROF_APOIO` | Razão | Razão alunos por profissional de apoio (0 quando sem o profissional). Captura a disponibilidade relativa do suporte institucional em função do porte da escola |
| `ALUNOS_POR_GESTAO` | Razão | Razão alunos por profissional de gestão/coordenação |
| `SCORE_CARENCIA_PED` | 0 a 6 | Soma de ausências de: biblioteca, lab. ciências, lab. informática, internet para alunos, banda larga e quadra esportiva. Fundamentado no Plano Nacional de Educação (BRASIL, 2014) e na literatura sobre permanência escolar (INEP, 2022; TODOS PELA EDUCAÇÃO, 2024) |
| `SCORE_CARENCIA_APOIO` | 0 a 3 | Soma de ausências de: psicólogo, assistente social e alimentação escolar. A alimentação escolar (PNAE) é reconhecida pela literatura como fator diretamente associado à permanência, especialmente em contextos de vulnerabilidade socioeconômica (BRASIL, 2009) |

A Figura 12 apresenta a relação entre os scores de carência e a taxa média de abandono escolar. No caso da carência pedagógica, observa-se uma tendência geral de aumento da taxa média de abandono conforme cresce o acúmulo de carências, especialmente nos scores mais altos. Esses resultados sugerem que a associação entre carências institucionais e abandono escolar pode envolver padrões não lineares e efeitos de limiar.

![Figura 12 — Relação entre scores de carência e taxa média de abandono](images/figura12.png)

*Figura 12 — Relação entre scores de carência e taxa média de abandono. As barras indicam a taxa média de abandono em cada nível de carência, enquanto a linha laranja representa o número de escolas em cada grupo. A carência pedagógica apresenta tendência geral crescente em relação ao abandono médio, embora de forma não linear. A carência de apoio apresenta padrão menos regular, com maior oscilação entre os níveis do score. Esses resultados sugerem associação entre acúmulo de carências institucionais e abandono escolar, mas não permitem inferir causalidade.*

### Pré-processamento para Modelagem

O pré-processamento foi organizado em dois pipelines distintos:

| Transformação | Pipeline RF (preditivo) | Pipeline Árvore (interpretativo) |
|---------------|------------------------|----------------------------------|
| Variáveis binárias | passthrough (já em escala 0-1) | passthrough |
| Variáveis numéricas | StandardScaler (média≈0, desvio≈1) | passthrough (escala original) |
| Variáveis categóricas | OneHotEncoder (drop='first') | OneHotEncoder (drop='first') |
| Contagens (log1p) | Aplicado antes do pipeline | Não aplicado |

A decisão de usar `passthrough` (sem `StandardScaler`) no pipeline da Árvore de Decisão é deliberada: garante que os valores nos nós da árvore apareçam na escala original, tornando as regras diretamente interpretáveis (ex: "proporção de matrículas noturnas > 12%"). O Random Forest usa `StandardScaler` nas variáveis numéricas para garantir que a importância relativa das features não seja distorcida por diferenças de escala.

A transformação `log1p` foi aplicada nas variáveis de contagem (`QT_MAT_MED_TOTAL`, `QT_PROF_APOIO`, etc.) antes do pipeline do Random Forest. Essa transformação comprime distribuições com cauda longa sem eliminar os outliers.

### Variáveis-alvo do Sistema em Cascata

O sistema de alerta opera em duas etapas com variáveis-alvo distintas:

- **Etapa 1 — Tem abandono:** variável binária. `Com_abandono` para escolas com taxa > 0%; `Sem_abandono` para escolas com taxa = 0%.
- **Etapa 2 — Nível de risco:** aplicada apenas às escolas com abandono > 0%. `Alto_risco` para escolas com taxa > 5%; `Risco_moderado` para escolas com taxa entre 0% e 5%.

> **Justificativa do limiar de 5%:** O limiar de 5% foi adotado como critério analítico, e não como ponto de corte oficial definido pelo Inep. Essa escolha se justifica porque a mediana da taxa de abandono entre escolas públicas da amostra foi de 2,1%. Além disso, taxas em torno de 5% aparecem em divulgações e séries educacionais brasileiras como patamares relevantes para o Ensino Médio: segundo divulgação do Inep sobre a 2ª etapa do Censo Escolar 2021, a taxa de abandono do Ensino Médio alcançou o pico de 5,0% em 2021 (INEP, 2022).

---

## Indução de Modelos

### Estratégia Metodológica

A análise adota dois modelos supervisionados com objetivos complementares:

| Modelo | Papel | Vantagem principal | Limitação |
|--------|-------|-------------------|-----------|
| Árvore de Decisão | Descritivo — explica QUAIS fatores estão associados ao abandono | Regras interpretáveis diretamente por gestores e formuladores de política | Menor acurácia preditiva |
| Random Forest | Preditivo — classifica escolas em níveis de risco | Alta acurácia, robusto a outliers, importância das variáveis (feature importance) | Caixa preta, sem regras explícitas |

### Sistema de Alerta em Cascata

Ambos os modelos operam em um sistema em cascata de duas etapas:

| Etapa | Pergunta | Saída |
|-------|----------|-------|
| Etapa 1 | Esta escola tem abandono? (taxa > 0% vs. 0%) | `Com_abandono` → entra na Etapa 2; `Sem_abandono` → nível: Sem abandono |
| Etapa 2 | O abandono é alto? (taxa > 5% vs. ≤5%) | `Alto_risco` ou `Risco_moderado` |

**Divisão treino/teste usada em ambos os modelos:**
- 80% treino — 14.543 escolas
- 20% teste — 3.636 escolas
- Divisão estratificada (`stratify=y`) — garante que a proporção entre classes é mantida em ambos os conjuntos

**Para a Etapa 2 (apenas escolas com abandono > 0):**
- Base: 13.150 escolas públicas com abandono > 0%
- 80% treino — 10.520 escolas
- 20% teste — 2.630 escolas

**Validação cruzada:**
- 5-fold estratificado aplicado sobre o conjunto de treino
- Cada fold usa ~80% do treino para ajuste e ~20% para validação interna

### Modelo 1: Árvore de Decisão (descritivo)

**Justificativa**

A Árvore de Decisão foi escolhida como modelo descritivo por gerar regras explícitas interpretáveis sem intermediação técnica. Um gestor educacional pode ler diretamente: "escolas sem grêmio estudantil com mais de 12% de matrículas noturnas têm alto risco de abandono". O pré-processamento preserva os valores na escala original nas regras da árvore.

**Hiperparâmetros**

- `max_depth=5` (Etapa 1) / `max_depth=4` (Etapa 2): árvores rasas para evitar overfitting e manter interpretabilidade;
- `min_samples_leaf=50` (Etapa 1) / `min_samples_leaf=100` (Etapa 2): folhas com no mínimo 50/100 amostras garantem que as regras descrevam padrões reais, não ruído;
- `class_weight='balanced'`: compensa o desbalanceamento entre classes sem necessidade de reamostrar os dados.

**Calibração dos thresholds — Árvore de Decisão**

Os thresholds de decisão da Árvore de Decisão foram fixados em:
- Etapa 1: threshold = 0,35
- Etapa 2: threshold = 0,45

Os thresholds foram ajustados manualmente com o objetivo de aumentar a sensibilidade do sistema para escolas com abandono, reduzindo falsos negativos. Essa escolha é coerente com a lógica de um sistema de alerta, no qual deixar de identificar uma escola em risco pode ser mais grave do que sinalizar uma escola que posteriormente não se confirme como prioritária.

### Modelo 2: Random Forest (preditivo)

**Justificativa**

O Random Forest foi escolhido como modelo preditivo por combinar alta acurácia com robustez a outliers. O ensemble de 500 árvores treinadas com bagging e seleção aleatória de features reduz a variância do modelo, superando consistentemente a árvore única em métricas de classificação. Além disso, fornece importância das variáveis (feature importance), baseada em redução de impureza (Gini), permitindo comparação direta com as regras da Árvore de Decisão.

**Otimização de Hiperparâmetros**

Os hiperparâmetros do Random Forest foram otimizados por meio do `RandomizedSearchCV`, com 40 iterações e validação cruzada estratificada com 5 folds.

| Hiperparâmetro | Valores testados | Melhor valor (Et1 / Et2) |
|----------------|-----------------|--------------------------|
| `n_estimators` | 300, 500 | 500 / 500 |
| `max_depth` | None, 20 | 20 / 20 |
| `min_samples_leaf` | 3, 5 | 5 / 5 |
| `max_features` | 'sqrt', 'log2' | 'sqrt' / 'log2' |
| `class_weight` | 'balanced', 'balanced_subsample' | 'balanced_subsample' / 'balanced' |
| `max_samples` | 0,6 / 0,8 / None | 0,8 / None |

**Calibração dos thresholds — Random Forest**

A calibração dos thresholds é uma das decisões metodológicas mais importantes do sistema de alerta. Por padrão, o scikit-learn usa threshold = 0,5.

*Etapa 1 — threshold = 0,35:*

O threshold de 0,35 foi escolhido por manter recall alto para `Com_abandono` (0,95) — apenas 5% das escolas com abandono real escapam para o grupo `Sem_abandono` — e por refletir o princípio de que, para um sistema de alerta educacional, o custo de um falso negativo é maior que o custo de um falso positivo.

*Etapa 2 — threshold = 0,50 (determinado automaticamente):*

| Threshold | F1 Alto risco | Recall Alto risco | Precisão Alto risco | Erros críticos |
|-----------|--------------|-------------------|---------------------|----------------|
| 0,30 | 0,518 | 0,974 | 0,353 | 24 |
| 0,35 | 0,567 | 0,951 | 0,404 | 46 |
| 0,40 | 0,620 | 0,906 | 0,471 | 88 |
| 0,45 | 0,660 | 0,842 | 0,543 | 148 |
| **0,50** | **0,680** | **0,745** | **0,624** | **239** |
| 0,55 | 0,651 | 0,617 | 0,688 | 360 |
| 0,60 | 0,591 | 0,485 | 0,756 | 484 |

O threshold 0,50 foi selecionado automaticamente por maximizar o F1 do Alto risco (0,680), produzindo um grupo Alto risco com taxa média real de 6,99% — acima do limiar de 5% com folga.

---

## Resultados

### Desempenho dos Modelos

| Modelo | F1-macro CV Etapa 1 | F1-macro CV Etapa 2 | Erros críticos | Vantagem |
|--------|--------------------|--------------------|----------------|----------|
| Árvore de Decisão | 0,598 ± 0,009 | 0,626 ± 0,013 | 366 | Regras interpretáveis |
| Random Forest | 0,653 ± 0,006 | 0,659 ± 0,012 | 304 | Maior acurácia preditiva |

> *Erros críticos = número de escolas de alto risco real classificadas incorretamente como Sem abandono ou risco moderado pelo sistema de alerta. O Random Forest apresenta superioridade em todas as métricas quantitativas, com 17% menos erros críticos que a Árvore de Decisão.*

### Resultado Final (Random Forest)

| Nível de alerta | Escolas | % do total | Taxa média real | Mediana real |
|----------------|---------|-----------|----------------|--------------|
| Alto risco (>5%) | 1.121 | 30,9% | 6,99% | 6,1% |
| Risco moderado (até 5%) | 2.186 | 60,2% | 2,17% | 1,4% |
| Sem abandono (0%) | 329 | 9,1% | ~0%* | 0,0% |

*\*A média do grupo Sem abandono (2,94%) é levemente superior ao risco moderado (2,17%) por conta de um pequeno número de escolas com abandono real que escapam para esse grupo (threshold conservador da Etapa 1). A mediana de 0,0% confirma que a maioria do grupo genuinamente não tem abandono. A lógica do sistema é validada pela mediana: Sem abandono (0,0%) < Risco moderado (1,4%) < Alto risco (6,1%).*

![Figura 13 — Matrizes de confusão do sistema de alerta](images/figura13.png)

*Figura 13 — Matrizes de confusão do sistema de alerta. À esquerda: Árvore de Decisão. À direita: Random Forest. O RF acerta 700 de 1.004 escolas de alto risco real (69,7%), com apenas 65 escapando para Sem abandono — o erro mais grave do sistema. A Árvore acerta 638 (63,5%) mas comete 117 erros graves (Alto risco → Sem abandono).*

### Fatores Institucionais Identificados

**Árvore de Decisão — regras interpretáveis**

As regras principais identificadas pela Árvore de Decisão para a Etapa 2 (Alto risco vs. Risco moderado):

| # | Condição institucional | Classificação |
|---|----------------------|---------------|
| 1 | Sem grêmio e matrículas noturnas > 12% | ALTO RISCO (incondicional) |
| 2 | Sem grêmio e noturno ≤ 12% e carência pedagógica > 5,5 | ALTO RISCO |
| 3 | Sem grêmio e noturno ≤ 12% e carência ≤ 5,5 e profissionais de apoio (log) > 1,24 | RISCO MODERADO |
| 4 | Com grêmio e matrículas noturnas ≤ 15% | RISCO MODERADO (incondicional) |
| 5 | Com grêmio e noturno > 15% e sem assoc. pais e mestres | ALTO RISCO |
| 6 | Com grêmio e noturno > 15% e com assoc. pais e mestres e com quadra coberta | RISCO MODERADO |
| 7 | Com grêmio e noturno > 15% e com assoc. pais e mestres e sem quadra coberta | ALTO RISCO |

**Random Forest — importância das variáveis**

![Figura 14 — Top 15 features por importância Gini — Random Forest Etapa 2](images/figura14.png)

*Figura 14 — Top 15 features por importância Gini — Random Forest Etapa 2. Proporção de matrículas no noturno e total de matrículas dominam, seguidos por razões aluno/profissional, presença de grêmio e associação de pais e mestres.*

As top 5 features do Random Forest são: (1) Proporção de matrículas no noturno; (2) Total de matrículas (log); (3) Alunos por profissional de apoio; (4) Alunos por gestão/coordenação; (5) Profissionais de apoio (log). A presença de grêmio estudantil e associação de pais e mestres aparecem na 6ª e 7ª posição, respectivamente, confirmando a convergência com as regras da Árvore.

### Comparação e Convergência entre os Modelos

A força metodológica do trabalho reside na convergência entre os dois modelos. Quando algoritmos com estratégias de aprendizado distintas identificam os mesmos fatores como mais relevantes, a evidência de associação é mais robusta.

| Fator institucional | Árvore de Decisão | Random Forest |
|---------------------|-------------------|---------------|
| Proporção de matrículas no noturno | Nó de 2ª divisão (limiar 12–15%) | Feature #1 em importância |
| Grêmio estudantil | Nó raiz (maior poder discriminativo) | Feature #7 em importância |
| Profissionais de apoio psicossocial | Regra de proteção (log > 1,24) | Features #3 e #5 (razão e quantidade) |
| Associação de pais e mestres | Fator protetor em 3 regras | Feature #6 em importância |
| Score de carência pedagógica | Regra de alto risco (score > 5,5) | Feature #9 em importância |
| Porte da escola (matrículas) | Presente em múltiplos nós | Feature #2 em importância |

---

## Conclusões

### Principais Achados

Este trabalho identificou três fatores institucionais que aparecem de forma consistente em ambos os modelos como os mais associados ao risco de abandono escolar nas escolas públicas de Ensino Médio brasileiro:

**1. Proporção de matrículas no turno noturno**

É o fator com maior poder discriminativo em ambos os modelos. Acima de 12–15%, o risco de abandono eleva-se de forma praticamente incondicional segundo a Árvore de Decisão. Este fator reflete o perfil de vulnerabilidade do aluno noturno, que frequentemente concilia trabalho e escola, estando sujeito a maior risco de abandono por razões externas à escola, mas que se manifestam através do perfil de matrícula da instituição.

**2. Participação institucional (grêmio e associação de pais)**

O grêmio estudantil é o nó raiz da Árvore de Decisão — o fator com maior poder de divisão de toda a base. Escolas com grêmio e perfil predominantemente diurno apresentam risco moderado independentemente de outros fatores, sugerindo que a participação estudantil institucionalizada funciona como mecanismo de pertencimento e retenção. A associação de pais e mestres atua como fator protetor complementar.

**3. Suporte psicossocial e pedagógico**

A ausência de profissionais de apoio (psicólogo, assistente social, pedagogo) e a carência pedagógica acumulada (score > 5,5 em 6 possíveis) estão consistentemente associadas ao alto risco. A razão alunos por profissional de apoio é a 3ª feature mais importante no Random Forest, indicando que não basta ter o profissional — a capacidade de atendimento relativa ao porte da escola é determinante.

### Sistema de Alerta — Síntese Operacional

O Random Forest otimizado classifica as 18.179 escolas públicas de EM regular em três níveis de alerta, com as seguintes características do conjunto de teste:

- **Alto risco:** 1.121 escolas (31%) | Taxa média real: 6,99% | Mediana: 6,1% — grupo candidato a intervenção prioritária;
- **Risco moderado:** 2.186 escolas (60%) | Taxa média real: 2,17% | Mediana: 1,4% — grupo de monitoramento;
- **Sem abandono:** 329 escolas (9%) | Mediana real: 0,0% — grupo estável.

A lógica do sistema é validada pela mediana: Sem abandono (0,0%) < Risco moderado (1,4%) < Alto risco (6,1%). O sistema comete 304 erros críticos no conjunto de teste, o que representa uma taxa de erro crítico de 30,3% para a classe Alto risco. Esse resultado indica que o sistema possui utilidade como ferramenta exploratória de triagem, mas não deve ser utilizado isoladamente para tomada de decisão.

### Limitações

- **Gap temporal:** a variável-alvo é de 2024 e os atributos institucionais são de 2025. A análise é exploratória e associativa, não causal.
- **Fatores individuais ausentes:** renda familiar, necessidade de trabalho, distância da escola e histórico escolar do aluno não estão disponíveis nos microdados do Censo Escolar.
- **Qualidade vs. presença:** o Censo registra apenas a presença ou ausência dos recursos, sem informar qualidade, manutenção ou efetivo uso pelos alunos.
- **Escopo:** a análise cobre apenas escolas públicas com EM regular tradicional. Os resultados não são generalizáveis para EJA, ensino técnico integrado ou escolas privadas.
- **Causalidade:** os modelos identificam associações, não relações causais.
- O sistema de alerta não é determinístico: 15% das escolas do grupo Sem abandono apresentam algum nível de abandono real (média de 2,94%), reflexo do threshold conservador da Etapa 1.

### Contribuições

- Demonstração de que fatores institucionais mensuráveis pelo Censo Escolar carregam sinal real sobre o risco de abandono, mesmo na ausência de dados socioeconômicos individuais;
- Construção de um sistema de alerta operacional em cascata com interpretabilidade (Árvore) e acurácia (Random Forest) complementares;
- Identificação do grêmio estudantil como o fator com maior poder discriminativo — achado com implicação direta para políticas de fortalecimento da participação estudantil;
- Evidência quantitativa de que o turno noturno é o proxy institucional mais forte do perfil de vulnerabilidade do estudante.

---

## Referências

BRASIL. Lei nº 9.394, de 20 de dezembro de 1996. Estabelece as diretrizes e bases da educação nacional. *Diário Oficial da União*, Brasília, DF, 23 dez. 1996.

BRASIL. Lei nº 11.947, de 16 de junho de 2009. Dispõe sobre o atendimento da alimentação escolar e do Programa Dinheiro Direto na Escola aos alunos da educação básica (PNAE). *Diário Oficial da União*, Brasília, DF, 17 jun. 2009.

BRASIL. Lei nº 13.005, de 25 de junho de 2014. Aprova o Plano Nacional de Educação - PNE e dá outras providências. *Diário Oficial da União*, Brasília, DF, 26 jun. 2014.

FUNDO DAS NAÇÕES UNIDAS PARA A INFÂNCIA (UNICEF). *Cenário da Exclusão Escolar no Brasil: um alerta sobre os impactos da pandemia da covid-19 na Educação*. Brasília, DF: UNICEF, 2021. Disponível em: https://www.unicef.org/brazil/relatorios/cenario-da-exclusao-escolar-no-brasil. Acesso em: 1 jun. 2026.

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Resumo Técnico: Censo Escolar da Educação Básica 2021*. Brasília, DF: INEP, 2022.

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Microdados do Censo Escolar da Educação Básica 2025*. Brasília, DF: INEP, 2025.

INSTITUTO NACIONAL DE ESTUDOS E PESQUISAS EDUCACIONAIS ANÍSIO TEIXEIRA (INEP). *Indicadores de Rendimento Escolar da Educação Básica 2024*. Brasília, DF: INEP, 2024.

NERI, M. C. (Coord.). *Motivos da Evasão Escolar*. Rio de Janeiro: FGV/CPS, 2009. Disponível em: https://cps.fgv.br/evasaoscolar. Acesso em: 1 jun. 2026.

TODOS PELA EDUCAÇÃO. *Anuário Brasileiro da Educação Básica 2024*. São Paulo: Editora Moderna, 2024.

