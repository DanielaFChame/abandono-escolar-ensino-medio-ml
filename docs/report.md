# Análise de fatores institucionais e estruturais associados à vulnerabilidade educacional na educação básica brasileira: um estudo com microdados do Censo Escolar 2025
teste

**Gabriela Gomes Mattoso, gabriela.mattoso@sga.pucminas.br**

**Daniela Ferreira Chame, daniela.chame@sga.pucminas.br**

**Giovanna Brito Silva Ribeiro, gbsribeiro@sga.pucminas.br**

**Isabella Oliveira Araujo Barbosa Moreira, isabella.moreira@sga.pucminas.br**

**Lívia Hilbert de Oliveira, livia.hilbert@sga.pucminas.br**


---

Professores:

** Prof. Gabriel Barbosa da Fonseca **
** Prof. Marco Paulo Soares Gomes **

---

_Curso de Ciência de Dados, Unidade Praça da Liberdade_

_Instituto de Informática e Ciências Exatas – Pontifícia Universidade de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil_

---

**Síntese**. 
Este trabalho analisa a relação entre fatores institucionais e estruturais das escolas e o risco de evasão escolar na educação básica brasileira, utilizando os microdados do Censo Escolar 2025. Considerando a ausência de variáveis socioeconômicas individuais, a pesquisa concentra-se em características internas das instituições de ensino, como infraestrutura, organização pedagógica e recursos humanos. A partir da integração de diferentes bases de dados, são construídos indicadores que permitem identificar padrões associados a contextos de maior vulnerabilidade educacional. Espera-se que os resultados contribuam para a compreensão do papel das condições escolares na permanência dos estudantes.
---


## Introdução

A evasão escolar é um dos principais desafios da educação básica no Brasil, impactando diretamente o desenvolvimento social e educacional do país. A permanência dos estudantes na escola está associada a múltiplos fatores, que vão desde condições socioeconômicas até aspectos institucionais e estruturais do sistema educacional.
Embora grande parte da literatura enfatiza fatores socioeconômicos como determinantes da evasão, há uma crescente necessidade de compreender o papel das condições internas das instituições de ensino, como infraestrutura, organização pedagógica e disponibilidade de recursos humanos. Esses fatores podem influenciar diretamente a qualidade da experiência escolar e, consequentemente, a permanência dos alunos.
Nesse contexto, o uso de dados educacionais em larga escala, como os microdados do Censo Escolar da Educação Básica (2025), permite analisar de forma sistemática as características das escolas e sua relação com contextos de maior vulnerabilidade educacional. Este trabalho insere-se na área de Ciência de Dados aplicada à educação, com foco na análise de fatores institucionais e estruturais associados ao risco de evasão escolar.


###    Contextualização

A evasão escolar deve ser compreendida como parte de um processo mais amplo de exclusão educacional, que pode se iniciar com a infrequência e evoluir para o abandono e, posteriormente, para a evasão definitiva. De acordo com o Observatório de Educação do Instituto Unibanco, o abandono escolar ocorre quando o estudante deixa de frequentar a escola ao longo do ano letivo, enquanto a evasão se caracteriza pela não continuidade dos estudos no período subsequente.
A identificação de fatores associados ao abandono escolar pode contribuir para a compreensão e prevenção da evasão. Embora estudos apontem a forte influência de fatores socioeconômicos, também há evidências de que aspectos institucionais (como infraestrutura escolar, número de docentes, organização das turmas e oferta de ensino em tempo integral) desempenham papel importante na permanência dos estudantes na escola. Dessa forma, a análise desses fatores permite compreender como o ambiente escolar pode contribuir para contextos de maior ou menor vulnerabilidade educacional. 


###    Problema

A evasão escolar é um problema multifatorial, cuja análise frequentemente se concentra em
fatores socioeconômicos. No entanto, essa abordagem pode limitar a compreensão do papel
das condições institucionais e estruturais das escolas no processo de permanência dos
estudantes.
Apesar da disponibilidade de microdados educacionais detalhados, muitas análises não
exploram de maneira integrada as características das instituições de ensino, como
infraestrutura, organização pedagógica e distribuição dos recursos humanos. Além disso, os
dados disponíveis dificultam a análise direta da evasão, exigindo a construção de indicadores
indiretos.
Diante deste cenário, torna-se necessário investigar como fatores institucionais e estruturais
das escolas estão associados a contextos de maior risco de evasão escolar, mesmo na
ausência de variáveis socioeconômicas individuais.



### Objetivo geral

Analisar, com base nos microdados do Censo Escolar 2025, como fatores institucionais e estruturais das escolas estão associados a contextos de maior risco de evasão escolar na educação básica.

#### Objetivos específicos

* Construir indicadores institucionais e estruturais das escolas, incluindo razão aluno/docente, tamanho médio das turmas e oferta de ensino em tempo integral.
* Desenvolver um índice de vulnerabilidade educacional baseado em características institucionais, como rede de ensino, localização, disponibilidade de recursos humanos e organização pedagógica.
* Analisar a distribuição do índice de vulnerabilidade entre as escolas, identificando padrões associados a diferentes contextos institucionais (público/privado, urbano/rural).
* Investigar a relação entre os indicadores estruturais das escolas e níveis mais elevados de vulnerabilidade educacional.



###    Justificativas

Este trabalho surge da necessidade de analisar a evasão escolar a partir de uma perspectiva institucional, investigando como características das escolas podem estar associadas a contextos de riscos, mesmo na ausência de variáveis socioeconômicas individuais, visto que o afastamento escolar representa um dos principais desafios do sistema educacional e retrata desigualdades socieconômicas. Essa abordagem é particularmente relevante considerando que os microdados do Censo Escolar disponíveis são agregados por estabelecimento de ensino, o que exige a construção de indicadores indiretos para análise do fenômeno.
Além disso, a utilização de técnicas de Ciência de Dados aplicadas à bases educacionais em larga escala permite a integração de múltiplas dimensões do sistema educacional, contribuindo para a identificação de padrões e para a geração de evidências que podem auxiliar na formulação de políticas públicas e estratégias educacionais mais eficazes.




##    Público alvo

O público alvo deste trabalho é composto por:

- Gestores educacionais, interessados em compreender como características institucionais impactam a permanência escolar;
- Pesquisadores das áreas de educação;
- Formuladores de políticas públicas: Ministério de educação, Secretarias Estaduais de Educação, etc;
- Estudantes em risco de evasão,principalmente em contextos de vulnerabilidade.



## Análise exploratórida dos dados

###    Dicionário de dados

Apresente uma descrição das bases de dados a serem utilizadas. 
Dicionários de dados devem conter as bases de dados, os nomes dos atributos 
com seu significado, seu tipo (inteiro, real, textual, categórico, etc).

Este projeto deve utilizar pelo menos duas fontes de dados. Uma fonte principal e 
uma fonte para enriquecimentos dos dados principais.


###    Descrição de dados

Utilize a análise descritiva baseada em estatística de primeira ordem para descrever os dados.
Como descrever dados numéricos: média, desvio padrão, mínimo, máximo, quartis, histograma, etc.
Como descrever dados qualitativos (categóricos): moda (valor mais frequente), quantidade de valores distintos (categorias), distribuição das categorias (histograma), etc.


## Preparação dos dados

A preparação dos dados consiste dos seguintes passos:

> - Seleção dos atributos
> - Tratamentos dos valores faltantes ou omissos: remoção, substituição, indução, etc.
> - Tratamento dos valores inconsistentes: conversão, remoção de dados duplicados, remoção ou tratamento de ouliers.
> - Conversão de dados: p. ex. numérico para categórico, categórico para binário, etc.


## Indução de modelos

## Modelo 1: Árvore de Decisão (Descritivo)

### Justificativa
A **Árvore de Decisão** foi escolhida como modelo descritivo por gerar regras explícitas e interpretáveis sem necessidade de intermediação técnica. 

> **Exemplo prático:** Um gestor educacional pode ler diretamente uma regra como: *"Escolas sem grêmio estudantil com mais de 12% de matrículas noturnas têm alto risco de abandono"*. 

Essa característica é essencial para o objetivo descritivo do trabalho e para a comunicação direta com o público-alvo (gestores e formuladores de políticas públicas). Além disso, o pré-processamento preserva os valores na escala original, mantendo o sentido real nas regras geradas pela árvore.

### Hiperparâmetros
Os parâmetros foram definidos para garantir a explicabilidade e evitar o *overfitting* (sobreajuste) do modelo:

* **`max_depth` (Profundidade Máxima):** `5` (Etapa 1) / `4` (Etapa 2).
  * *Motivo:* Manter árvores rasas para evitar que o modelo memorize os dados de treino, além de preservar a interpretabilidade das regras.
* **`min_samples_leaf` (Amostras Mínimas por Folha):** `50` (Etapa 1) / `100` (Etapa 2).
  * *Motivo:* Garantir que as folhas finais tenham volume suficiente de amostras assegura que as regras descrevam padrões reais e estruturais, e não ruídos estatísticos.
* **`class_weight='balanced'`:** * *Motivo:* Compensa o desbalanceamento intrínseco entre as classes de forma automática, sem a necessidade de reamostrar os dados previamente.

### Estratégia de Validação Cruzada
Foi utilizada a validação cruzada estratificada com 5 partições (`StratifiedKFold`, `n_splits=5`).

Esse método preserva a proporção exata entre classes em cada *fold*. O uso de 5 *folds* é o padrão metodológico recomendado para bases com mais de 10.000 amostras, pois entrega estimativas de desempenho robustas e confiáveis sem gerar um custo computacional excessivo.

### Calibração dos Limiares de Decisão (*Thresholds*)
Os *thresholds* da Árvore de Decisão foram ajustados manualmente e fixados nos seguintes valores:

* **Etapa 1:** `0.35`
* **Etapa 2:** `0.45`

**Justificativa da Calibração:**
O ajuste foi feito com o objetivo de **aumentar a sensibilidade** do sistema na identificação de escolas com risco de abandono, reduzindo ao máximo os falsos negativos. Essa escolha reflete a lógica central de um sistema de alerta precoce: deixar de identificar uma escola em risco grave (falso negativo) tem um custo social muito maior do que sinalizar preventivamente uma escola que, no futuro, não se confirme como prioritária (falso positivo).


## Modelo 2: Random Forest (Preditivo)

### Justificativa
O **Random Forest** foi escolhido como modelo preditivo por combinar alta acurácia com robustez a *outliers*. O *ensemble* de 500 árvores treinadas com *bagging* e seleção aleatória de *features* reduz a variância do modelo, superando consistentemente a árvore de decisão única em métricas de classificação. 

Além disso, o modelo fornece a importância das variáveis (*feature importance*), calculada com base na redução de impureza (Gini), permitindo uma comparação direta com as regras da Árvore de Decisão descritiva.

### Otimização de Hiperparâmetros
Os hiperparâmetros do Random Forest foram otimizados por meio do `RandomizedSearchCV`, executando 40 iterações com validação cruzada estratificada de 5 *folds*. Esse procedimento testa combinações aleatórias dentro de um espaço de busca previamente definido.

O espaço de busca foi estruturado de forma controlada para reduzir o risco de *overfitting* e manter o custo computacional viável. Como o objetivo principal era construir um sistema de alerta interpretável e operacional (e não apenas maximizar o desempenho a qualquer custo), optou-se por testar valores moderados para o número e a profundidade das árvores.

| Hiperparâmetro | Valores Testados | Melhor Valor (Etapa 1 / Etapa 2) |
| :--- | :--- | :--- |
| `n_estimators` | `300`, `500` | `500` / `500` |
| `max_depth` | `None`, `20` | `20` / `20` |
| `min_samples_leaf` | `3`, `5` | `5` / `5` |
| `max_features` | `'sqrt'`, `'log2'` | `'sqrt'` / `'log2'` |
| `class_weight` | `'balanced'`, `'balanced_subsample'` | `'balanced_subsample'` / `'balanced'` |
| `max_samples` | `0.6`, `0.8`, `None` | `0.8` / `None` |

---

### Calibração dos Limiares de Decisão (*Thresholds*)
A calibração dos *thresholds* é uma das decisões metodológicas mais críticas de um sistema de alerta. Por padrão, a biblioteca Scikit-Learn adota um *threshold* de `0.50` (classificando como positivo quando a probabilidade é > 50%). Para um diagnóstico educacional, assumir esse padrão é subótimo.

#### Etapa 1 — Threshold = 0.35
O limiar da Etapa 1 controla a sensibilidade do sistema para detectar qualquer sinal de abandono. Durante os testes, um limiar de `0.25` (mais agressivo) atingiu um *recall* de 0.98, mas classificou 98% de todas as escolas como `Com_abandono`, tornando o filtro inútil. Por outro lado, `0.50` perderia muitas escolas com abandono real. 

**O valor de 0.35 foi escolhido por:**
* Manter um *recall* alto para a classe `Com_abandono` (0.95) — apenas 5% das escolas com abandono real escapam para o grupo `Sem_abandono`.
* Melhorar a especificidade em relação ao *threshold* de `0.25`, sinalizando incorretamente menos escolas sem abandono real.
* Refletir o princípio metodológico central do sistema: o custo de um falso negativo (não identificar uma escola em risco) é significativamente maior que o custo de um falso positivo (investigar uma escola desnecessariamente).

#### Etapa 2 — Threshold = 0.50 (Determinado automaticamente)
O limiar da Etapa 2 foi estabelecido por meio de busca automática, avaliando valores entre `0.30` e `0.60` para selecionar aquele que maximiza o *F1-score* específico da classe `Alto_risco`:

| Threshold | F1 (Alto Risco) | Recall (Alto Risco) | Precisão (Alto Risco) | Erros Críticos |
| :---: | :---: | :---: | :---: | :---: |
| 0.30 | 0.518 | 0.974 | 0.353 | 24 |
| 0.35 | 0.567 | 0.951 | 0.404 | 46 |
| 0.40 | 0.620 | 0.906 | 0.471 | 88 |
| 0.45 | 0.660 | 0.842 | 0.543 | 148 |
| **0.50** | **0.680** | **0.745** | **0.624** | **239** |
| 0.55 | 0.651 | 0.617 | 0.688 | 360 |
| 0.60 | 0.591 | 0.485 | 0.756 | 484 |

> **Justificativa da Seleção Automática:** > O *threshold* `0.50` foi selecionado por atingir o pico de F1-score para a classe de Alto risco (`0.680`). Quando comparado a um limiar mais agressivo como `0.30` (que minimiza os erros críticos para apenas 24), o valor de `0.50` agrupa escolas com uma taxa de abandono média real de 6,99% (uma margem segura acima do limiar crítico de 5%). Em contraste, o *threshold* de `0.30` resultava em uma taxa média de apenas 4,29%, indicando que o grupo de Alto Risco estava sendo inflado com escolas *borderline*. Portanto, o limiar ótimo de `0.50` representa o equilíbrio ideal entre a precisão do alerta e a real capacidade de detectar escolas criticamente vulneráveis.

## Resultados

### Desempenho dos Modelos

| Modelo | F1-macro CV (Etapa 1) | F1-macro CV (Etapa 2) | Erros Críticos | Vantagem Principal |
| :--- | :--- | :--- | :--- | :--- |
| Árvore de Decisão | 0.598 ± 0.009 | 0.626 ± 0.013 | 366 | Regras interpretáveis |
| Random Forest | 0.653 ± 0.006 | 0.659 ± 0.012 | 304 | Maior acurácia preditiva |

> **Nota sobre Erros Críticos:** Refere-se ao número de escolas com alto risco real que foram classificadas incorretamente pelo sistema de alerta como *Sem abandono* ou *Risco moderado*. O Random Forest apresenta superioridade em todas as métricas quantitativas, resultando em **17% menos erros críticos** em comparação com a Árvore de Decisão.

---

### Resultado Final (Random Forest)

| Nível de Alerta | Escolas | % do Total | Taxa Média Real | Mediana Real |
| :--- | :---: | :---: | :---: | :---: |
| Alto Risco (> 5%) | 1.121 | 30,9% | 6,99% | 6,1% |
| Risco Moderado (até 5%) | 2.186 | 60,2% | 2,17% | 1,4% |
| Sem Abandono (0%) | 329 | 9,1% | ~0%* | 0,0% |

> **\*** A média do grupo *Sem abandono* (2,94%) é levemente superior ao *Risco moderado* (2,17%) devido a um pequeno número de escolas com abandono real que escapam para esse grupo (resultado do *threshold* conservador definido na Etapa 1). No entanto, a mediana de **0,0%** confirma que a vasta maioria das escolas desse grupo genuinamente não tem abandono. A lógica geral do sistema é validada de forma robusta pela progressão da mediana: **Sem abandono (0,0%) < Risco moderado (1,4%) < Alto risco (6,1%)**.

*Figura 13: Matrizes de confusão do sistema de alerta. À esquerda: Árvore de Decisão. À direita: Random Forest. O RF acerta 700 de 1.004 escolas de alto risco real (69,7%), com apenas 65 escapando para "Sem abandono" — o erro mais grave que o sistema pode cometer. A Árvore acerta 638 (63,5%), mas comete 117 erros graves (Alto risco → Sem abandono).*

---

### Fatores Institucionais Identificados

#### Árvore de Decisão — Regras Interpretáveis
As principais regras geradas pela Árvore de Decisão para a Etapa 2 (classificação de *Alto risco* vs. *Risco moderado*) são:

| # | Condição Institucional | Classificação |
| :---: | :--- | :--- |
| 1 | Sem grêmio e matrículas noturnas > 12% | **ALTO RISCO** (incondicional) |
| 2 | Sem grêmio e noturno ≤ 12% e carência pedagógica > 5,5 | **ALTO RISCO** |
| 3 | Sem grêmio e noturno ≤ 12% e carência ≤ 5,5 e profissionais de apoio (log) > 1,24 | **RISCO MODERADO** |
| 4 | Com grêmio e matrículas noturnas ≤ 15% | **RISCO MODERADO** (incondicional) |
| 5 | Com grêmio e noturno > 15% e sem assoc. de pais e mestres | **ALTO RISCO** |
| 6 | Com grêmio e noturno > 15% e com assoc. de pais e mestres e com quadra coberta | **RISCO MODERADO** |
| 7 | Com grêmio e noturno > 15% e com assoc. de pais e mestres e sem quadra coberta | **ALTO RISCO** |

#### Random Forest — Importância das Variáveis

*Figura 16 — Top 15 features por importância Gini — Random Forest Etapa 2. A proporção de matrículas no noturno e o total de matrículas dominam, seguidos por razões aluno/profissional, presença de grêmio e associação de pais e mestres.*

As **Top 5 variáveis** identificadas pelo Random Forest são:
1. Proporção de matrículas no noturno
2. Total de matrículas (log)
3. Alunos por profissional de apoio
4. Alunos por gestão/coordenação
5. Profissionais de apoio (log)

> **Convergência entre os modelos:** A presença de grêmio estudantil e a associação de pais e mestres aparecem na 6ª e 7ª posição do Random Forest, respectivamente. Esse dado confirma a convergência com as regras geradas de forma independente pela Árvore de Decisão, reforçando a validade dos fatores institucionais identificados.


## Análise comparativa dos modelos

Discuta sobre as forças e fragilidades de cada modelo. Exemplifique casos em que um
modelo se sairia melhor que o outro. Nesta seção é possível utilizar a sua imaginação
e extrapolar um pouco o que os dados sugerem.


### Distribuição do modelo (opcional)

Tende criar um pacote de distribuição para o modelo construído, para ser aplicado 
em um sistema inteligente.


## 8. Conclusão

Apresente aqui a conclusão do seu trabalho. Discussão dos resultados obtidos no trabalho, 
onde se verifica as observações pessoais de cada aluno.

Uma conclusão deve ter 3 partes:

   * Breve resumo do que foi desenvolvido
	 * Apresenação geral dos resultados obtidos com discussão das vantagens e desvantagens do sistema inteligente
	 * Limitações e possibilidades de melhoria


# REFERÊNCIAS

Como um projeto de sistema inteligente não requer revisão bibliográfica, 
a inclusão das referências não é obrigatória. No entanto, caso você 
tenha utilizado referências na introdução ou deseje 
incluir referências relacionadas às tecnologias, padrões, ou metodologias 
que serão usadas no seu trabalho, relacione-as de acordo com a ABNT.

Verifique no link abaixo como devem ser as referências no padrão ABNT:

http://www.pucminas.br/imagedb/documento/DOC\_DSC\_NOME\_ARQUI20160217102425.pdf

Por exemplo:

**[1]** - _ELMASRI, Ramez; NAVATHE, Sham. **Sistemas de banco de dados**. 7. ed. São Paulo: Pearson, c2019. E-book. ISBN 9788543025001._

**[2]** - _COPPIN, Ben. **Inteligência artificial**. Rio de Janeiro, RJ: LTC, c2010. E-book. ISBN 978-85-216-2936-8._

**[3]** - _CORMEN, Thomas H. et al. **Algoritmos: teoria e prática**. Rio de Janeiro, RJ: Elsevier, Campus, c2012. xvi, 926 p. ISBN 9788535236996._

**[4]** - _SUTHERLAND, Jeffrey Victor. **Scrum: a arte de fazer o dobro do trabalho na metade do tempo**. 2. ed. rev. São Paulo, SP: Leya, 2016. 236, [4] p. ISBN 9788544104514._

**[5]** - _RUSSELL, Stuart J.; NORVIG, Peter. **Inteligência artificial**. Rio de Janeiro: Elsevier, c2013. xxi, 988 p. ISBN 9788535237016._



# APÊNDICES

**Colocar link:**

Do código (armazenado no repositório);

Dos artefatos (armazenado do repositório);

Da apresentação final (armazenado no repositório);

Do vídeo de apresentação (armazenado no repositório).




