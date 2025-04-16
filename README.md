Repositório para Pesquisa sobre Segurança Pública 

Trabalho Destinado ao Grupo de Pesquisa de Ciência de Dados e Inteligência Artifical - PUC Minas - Campus Lourdes 

# Definição do Problema:

**Tema geral:** Segurança Pública

**Domínio:** Caracterização da violência e da criminalidade no município X

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

![Modelo Conceitual Seguranca drawio](https://github.com/user-attachments/assets/dc8dbaf8-e232-4fb4-a7de-d28a2788df84)

# Etapas CAPTO
## Etapa 1 - Socialização

## Etapa 2 - Mapeamento
### Grupo 1: 
 ##### Integrantes
 Vitor, ...
 ##### Modelo Conceitual:
 ``image.png``

### Grupo 2:
 #### Integrantes
 ..., ...
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

**Nas dimensões sociais, demográficas, espaciais, criminais, temporais e institucionais:
**

**Estrutura social e dinâmica da violência:**

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


**Determinantes da criminalidade e suas características**
https://www.redalyc.org/pdf/218/21847202.pdf
