Repositório para Pesquisa sobre Segurança Pública 

Trabalho Destinado ao Grupo de Pesquisa de Ciência de Dados e Inteligência Artifical - PUC Minas - Campus Lourdes 

# Definição do Problema:

**Tema geral:** Segurança Pública

**Domínio:** Caracterização da violência e da criminalidade de um municipio

**Justificativa:**
A violência e a criminalidade são fenômenos complexos e desafiadores no contexto urbano brasileiro, afetando diretamente a qualidade de vida da população e a eficácia das políticas públicas. No entanto, a maioria dos estudos e intervenções ainda trata esses problemas de forma agregada, sem considerar nuances importantes como a idade e o gênero das vítimas.

A análise segmentada por faixa etária e gênero é essencial para entender quem são os grupos mais vulneráveis, como são afetados e em quais contextos a violência se manifesta. Por exemplo, adolescentes do sexo masculino podem estar mais expostos a homicídios relacionados ao tráfico, enquanto mulheres adultas podem ser mais vitimadas por violência doméstica ou sexual.

No nível municipal, essa abordagem permite identificar padrões locais, apoiar decisões estratégicas das gestões públicas e propor ações direcionadas que promovam segurança e justiça de forma mais equitativa. Além disso, a ausência de dados tratados com esse nível de detalhamento dificulta a formulação de políticas eficazes e sustentáveis.

Portanto, investigar a violência e criminalidade com recorte por idade e gênero é uma necessidade urgente para personalizar políticas públicas, monitorar indicadores locais com mais precisão, e ampliar a capacidade de resposta das instituições de segurança e assistência social.

# Objetivo geral:
Investigar padrões de criminalidade em diferentes faixas etárias e entre gêneros no município, buscando compreender como variam os tipos de violência, horários, locais e reincidência das ocorrências.

 Isso permite explorar:
Quais grupos sociais (ex: adolescentes do sexo masculino) são mais vulneráveis a determinados tipos de crime.

Se há diferença de abordagem policial conforme o perfil da vítima.

Como políticas públicas podem ser adaptadas conforme o recorte etário e de gênero.

Relação entre violência e desigualdade social entre homens e mulheres, ou jovens e adultos.

# Escala 

**Escala Espacial:**

Municipal – o foco está em um único município (por exemplo, “Município de X”), permitindo o uso de dados locais (boletins de ocorrência, dados da prefeitura, observações de campo, etc.).

**Escala Temporal:**

Análise de séries históricas curtas (por exemplo, últimos 5 anos), com a possibilidade de observar tendências e sazonalidades (ex: aumento de crimes em certas épocas do ano ou dias da semana).

**Escala Populacional:**

Segmentada por faixa etária e gênero – a análise será feita considerando categorias como:

Crianças e adolescentes (0–17 anos)

Jovens adultos (18–29 anos)

Adultos (30–59 anos)

Idosos (60+ anos)
Separando entre homens, mulheres e, se houver dados, outras identidades de gênero.

# Dimensão dos dados:

**Social:**

_Descrição:_
Foca na relação entre vítima e agressor e o impacto social do crime.
_Atributos associados: _
Relação entre os envolvidos, condição no momento do crime, situação de vulnerabilidade

**Demográfica:**

_Descrição:_
Foca nos perfis das vítimas e suas características individuais.
_Atributos associados: _
Idade, gênero, escolaridade, condição socioeconômica

**Espacial:**

_Descrição:_
Analisa o local onde os crimes ocorrem e suas características.
_Atributos associados: _
Bairro, rua, zona (central, periférica), reincidência no local

**Criminal:**

_Descrição:_
Observa o tipo de crime, gravidade e contexto.
_Atributos associados: _
Classificação do crime, uso de arma, número de envolvidos, vínculo com o agressor

**Temporal:**

_Descrição:_
Avalia os padrões ao longo do tempo.
_Atributos associados: _
Data, hora, dia da semana, período do ano

**Institucional:**

_Descrição:_
Permite entender a resposta do Estado à violência.
_Atributos associados: _
Tempo de resposta policial, presença de policiamento preventivo, número de boletins registrados


### Variáveis por Dimensão

| Dimensão        | Variável                      | Tipo                   | Descrição                                                    |
|------------------|-------------------------------|------------------------|--------------------------------------------------------------|
| Demográfica      | Idade da vítima               | Quantitativa discreta  | Idade numérica da vítima                                     |
|                  | Faixa etária                  | Qualitativa ordinal    | Classificação por grupo de idade                             |
|                  | Gênero da vítima              | Qualitativa nominal    | Masculino, feminino, outro                                   |
|                  | Escolaridade                  | Qualitativa ordinal    | Fundamental, médio, superior, etc.                           |
|                  | Bairro de residência          | Qualitativa nominal    | Nome do bairro onde a vítima mora                            |
| Criminal         | Tipo de crime                 | Qualitativa nominal    | Homicídio, roubo, estupro, etc.                              |
|                  | Gravidade do crime            | Qualitativa ordinal    | Baixa, média, alta                                           |
|                  | Uso de arma                   | Qualitativa nominal    | Fogo, branca, nenhuma                                        |
|                  | Número de agressores          | Quantitativa discreta  | Total de agressores envolvidos                               |
|                  | Relação com o agressor        | Qualitativa nominal    | Familiar, parceiro, desconhecido, etc.                       |
| Espacial         | Local do crime                | Qualitativa nominal    | Rua, escola, transporte, etc.                                |
|                  | Bairro do crime               | Qualitativa nominal    | Nome do bairro onde ocorreu o crime                          |
|                  | Zona da cidade                | Qualitativa nominal    | Central, intermediária, periférica                           |
| Temporal         | Data do crime                 | Quantitativa contínua  | Data exata da ocorrência                                     |
|                  | Hora do crime                 | Quantitativa contínua  | Horário da ocorrência                                        |
|                  | Dia da semana                 | Qualitativa nominal    | Segunda, terça, etc.                                         |
|                  | Mês do crime                  | Qualitativa ordinal    | Janeiro, fevereiro, etc.                                     |
| Social           | Estava sozinha(o)?            | Qualitativa binária    | Sim ou não                                                   |
|                  | Situação de vulnerabilidade   | Qualitativa nominal    | Em deslocamento, alcoolizada(o), etc.                        |
|                  | Reincidência de vitimização   | Qualitativa binária    | Já foi vítima antes: sim ou não                              |
| Institucional    | Tempo de resposta policial    | Quantitativa contínua  | Tempo em minutos entre o chamado e o atendimento             |
|                  | Houve registro da ocorrência? | Qualitativa binária    | Sim ou não                                                   |


# Modelo Conceitual



# Etapas CAPTO
## Etapa 1 - Socialização

## Etapa 2 - Mapeamento
### Grupo 1: 
 ##### Integrantes
 Vitor, Leonardo
 ##### Modelo Conceitual:
 ``image.png``

### Grupo 2:
 #### Integrantes
 Augusto, Walker
 #### Modelo Conceitual:
 ``image.png``

## Etapa 3 - Combinação
### Mapa Conceitual Unificado
``image.png``

## Etapa 4 - Focalização
Indicar os atributos

## Etapa 5 - Congruência
Harmonização com a disponibilidade dos dados



# Literatura/Artigos Científicos:

**Estrutura social e dinâmica da violência:** (Lido)

https://www.scielo.br/j/rbepop/a/mbcYGX6j9j4xGc98xBYFnqP/?format=pdf&lang=pt 


**Segurança pública, criminalidade, violência e (re)produção do espaço urbano**
https://www.researchgate.net/publication/343894197_SEGURANCA_PUBLICA_CRIMINALIDADE_VIOLENCIA_E_REPRODUCAO_DO_ESPACO_URBANO_UMA_BREVE_DISCUSSAO_SOBRE_SUA_RELACAO


**Estatísticas oficiais, violência e crime no Brasil**

[Estatísticas+oficiais,+violência+e+crime+no+Brasil+(1).pdf](https://github.com/user-attachments/files/19638313/Estatisticas%2Boficiais.%2Bviolencia%2Be%2Bcrime%2Bno%2BBrasil%2B.1.pdf)


**Políticas públicas no combate à criminalidade e a violência - Ipea**

https://www.ipea.gov.br/sites/images/mestrado/turma4/RICARDO_WANNER_DE_GODOY.pdf


**Determinantes da criminalidade: arcabouços teóricos e resultados**

https://www.redalyc.org/pdf/218/21847202.pdf


**Análise demográfica das vítimas de violência**

https://www.scielo.br/j/rbepop/a/mbcYGX6j9j4xGc98xBYFnqP/?format=pdf&lang=pt


**Determinantes da criminalidade e suas características** (Lido)
https://www.redalyc.org/pdf/218/21847202.pdf


**FATORES FISCAIS E SOCIOECONÔMICOS QUE AFETAM A CRIMINALIDADE NO BRASIL**
https://www.scielo.br/j/cgpc/a/rhTv7DbF6qw8ndHZYYYFJ3K/?lang=pt


**Crime, sujeito e sujeição criminal: aspectos de uma contribuição analítica sobre a categoria "bandido"**
https://www.scielo.br/j/ln/a/sv7ZDmyGK9RymzJ47rD5jCx/?lang=pt


**O novo paradigma da violência**
https://www.scielo.br/j/ts/a/S4WmjGyW3Bqxd7Y6GYcPVhN/?lang=pt


**A Política Nacional de Segurança Pública: histórico, dilemas e perspectivas**
https://www.scielo.br/j/ea/a/HfX5ZwsFKW6wtzrMTTrhYwz/?lang=pt


**Concepções de violência e práticas de cuidado dos usuários da estratégia de saúde da família: uma perspectiva cultural**
https://www.scielo.br/j/tce/a/CYyQCNLcP5rQZJZVjg6zsXC/?lang=pt


**O conceito de Crime e Criminalidade para agentes de segurança da cidade de Curitiba**
https://seer.ufrgs.br/PolisePsique/article/view/23221


**Violência, Criminalidade e Sentimento de Insegurança**
https://agris.fao.org/search/en/providers/125162/records/67659e76829d7ef70f4916ed


**Determinantes da criminalidade em Minas Gerais**
https://www.scielo.br/j/rbcsoc/a/C7B6xjjfzkDBVbYkKnKgPYQ/#


**Os impactos da implementação do Big Data para a análise da criminalidade e definição de políticas públicas**
https://dspace.mackenzie.br/items/7b9324a7-703f-45de-92f6-ec1e6bede7b3


**Criminalidade Violenta: Da Sua Medição às Políticas Públicas de Segurança Interna**
https://www.proquest.com/openview/078f95e187d7e200f903f2e7c2d46c9e/1?cbl=2026366&diss=y&pq-origsite=gscholar


**Considerações sobre criminalidade: marginalização, medo e mitos no Brasil** (Leo está lendo)

https://revista.forumseguranca.org.br/index.php/rbsp/article/view/85


**Avanços na democracia brasileira: a participação da sociedade civil na Conferência Nacional de Segurança Pública**

https://revista.forumseguranca.org.br/index.php/rbsp/article/view/55


**LEVANTAMENTO E ESPACIALIZAÇÃO DA CRIMINALIDADE URBANA DO MUNICÍPIO DE MOSSORÓ-RN**

https://www2.ifrn.edu.br/ojs/index.php/HOLOS/article/view/4187


**Crime social, castigo social: desigualdade de renda e taxas de criminalidade nos grandes municípios brasileiros** (LEO ESTÁ LENDO)

https://www.scielo.br/j/ee/a/Wz4bLz5z3mFQWY6JhKcmhjz/?lang=pt


**Análise espacial dos condicionantes da criminalidade violenta no estado de Minas Gerais**

https://www.scielo.br/j/sn/a/3KT8G8mKStv5xg3bfv4xxbD/?lang=pt


**Criminalidade violenta: por uma nova perspectiva de análise**

https://www.scielo.br/j/rsocp/a/6W7KgY6yLBSJxtrrV7BycCs/?lang=pt


**Formas de pensar a sociedade**

https://dialnet.unirioja.es/servlet/articulo?codigo=4766705


**Conceitos, teorias e tipologias de violência: a violência faz mal à saúde individual e coletiva**

https://pesquisa.bvsalud.org/portal/resource/pt/biblio-1025139


**Refletindo sobre a violência**

https://periodicos.furg.br/rbhcs/article/view/10353


**Reflexões sobre a violência na condição moderna**(Vitor esta lendo)

https://www.scielo.br/j/ts/a/BM4wVbK9Fn7sPYzKTWCC6fr/?lang=pt


**Violência vivida: a dor que não tem nome**

https://www.scielosp.org/pdf/icse/2003.v7n12/41-54/pt


**INTERAÇÕES ENTRE VIOLÊNCIA E CIDADES: EM BUSCA DE UMA DEFINIÇÃO DE VIOLÊNCIA URBANA** (Lido)

https://revista.fct.unesp.br/index.php/cpg/article/view/3289


**Segurança e insegurança em Salvador: O que revelam os indicadores de segurança pública?**

https://www.scielo.pt/scielo.php?script=sci_arttext&pid=S2184-77702021000400079&lang=pt


