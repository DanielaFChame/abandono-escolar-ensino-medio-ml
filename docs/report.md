# Análise de fatores institucionais e estruturais associados à vulnerabilidade educacional na educação básica brasileira: um estudo com microdados do Censo Escolar 2025


**Gabriela Gomes Mattoso, gabriela.mattoso@sga.pucminas.br**

**Daniela Ferreira Chame, daniela.chame@sga.pucminas.br**

**Giovanna Brito Silva Ribeiro, gbsribeiro@sga.pucminas.br**

**Nome completo do Aluno 4, email do aluno 4**

**Lívia Hilbert de Oliveira livia.hilbert@sga.pucminas.br**


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

Nesse momento você deve apresentar o problema que seu agente pretende resolver. 
No entanto, não é a hora de comentar sobre a aplicação.
Descreva também o contexto em que essa aplicação será usada, se  houver: 
empresa, tecnologias, etc. Novamente, descreva apenas o que de  fato existir, 
pois ainda não é a hora de apresentar requisitos  detalhados ou projetos.

O **problema** pode ser algo vivido em uma empresa específica. Neste caso, o aluno deve 
sucintamente apresentar o cenário de problema da empresa. A empresa só deve ser citada 
explicitamente se o aluno tiver autorização para tal.

> **Links Úteis**:
> - [Objetivos, Problema de pesquisa e Justificativa](https://medium.com/@versioparole/objetivos-problema-de-pesquisa-e-justificativa-c98c8233b9c3)


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

> **Links Úteis**:
> - [Como montar a justificativa](https://guiadamonografia.com.br/como-montar-justificativa-do-tcc/)



##    Público alvo

O público alvo deste trabalho é composto por:

- Gestores educacionais, interessados em compreender como características institucionais impactam a permanência escolar;
- Pesquisadores das áreas de educação;
- Formuladores de políticas públicas: Ministério de educação, Secretarias Estaduais de Educação, etc;
- Estudantes em risco de evasão,principalmente em contextos de vulnerabilidade.


> **Links Úteis**:
> - [Público-alvo](https://blog.hotmart.com/pt-br/publico-alvo/)
> - [Como definir o público alvo](https://exame.com/pme/5-dicas-essenciais-para-definir-o-publico-alvo-do-seu-negocio/)
> - [Público-alvo: o que é, tipos, como definir seu público e exemplos](https://klickpages.com.br/blog/publico-alvo-o-que-e/)
> - [Qual a diferença entre público-alvo e persona?](https://rockcontent.com/blog/diferenca-publico-alvo-e-persona/)


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

### Modelo 1: Algoritmo

Substitua o título pelo nome do algoritmo que será utilizado. P. ex. árvore de decisão, rede neural, SVM, etc.
Justifique a escolha do modelo.
Apresente o processo utilizado para amostragem de dados (particionamento, cross-validation).
Descreva os parâmetros utilizados. 
Apresente trechos do código utilizado comentados. Se utilizou alguma ferramenta gráfica, apresente imagens
com o fluxo de processamento.

### Modelo 2: Algoritmo

Repita os passos anteriores para o segundo modelo.


## Resultados

### Resultados obtidos com o modelo 1.

Apresente aqui os resultados obtidos com a indução do modelo 1. 
Apresente uma matriz de confusão quando pertinente. Apresente as medidas de performance
apropriadas para o seu problema. 
Por exemplo, no caso de classificação: precisão, revocação, F-measure, acurácia.

### Interpretação do modelo 1

Apresente os parâmetros do modelo obtido. Tentre mostrar as regras que são utilizadas no
processo de 'raciocínio' (*reasoning*) do sistema inteligente. Utilize medidas como 
o *feature importances* para tentar entender quais atributos o modelo se baseia no
processo de tomada de decisão.


### Resultados obtidos com o modelo 2.

Repita o passo anterior com os resultados do modelo 2.

### Interpretação do modelo 2

Repita o passo anterior com os parâmetros do modelo 2.


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




