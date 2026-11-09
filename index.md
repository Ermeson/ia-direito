---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 0
  theme: minimal
---

# Inteligência Artificial no Direito

## Não vamos falar sobre

- Engenharia de Prompts
- Alucinação de IA
- O que pode, o que não pode.

## Vamos falar sobre

- Otimizações
- Skills
- Agentes
- Artefatos

## Taxonomias

### Agentes de IA

#### O que são

Sistemas de IA que, a partir de um objetivo, planejam e executam ações de maneira autônoma (buscar informações, usar ferramentas, gerar documentos), tomando decisões intermediárias sem que cada passo precise ser instruído manualmente.

### Skills

#### O que são

Conjuntos de instruções, modelos e conhecimentos específicos, empacotados e reutilizáveis, que ensinam a IA a executar sempre da mesma forma uma tarefa recorrente (ex: elaborar uma petição), sem precisar reescrever o prompt a cada uso.

### Artefatos

#### O que são

Conteúdos ou aplicações gerados pela IA (documentos, páginas, interfaces interativas) que existem como produtos autônomos, podendo ser visualizados, editados e compartilhados fora da própria conversa com o modelo.

## Prática

### 1 - RAG

#### Preparação do corpus de conteúdo do modelo

##### Benefícios de preparar o corpus

Melhora a precisão e a relevância das respostas da IA, fornecendo o conteúdo jurídico correto (leis, contratos, jurisprudência) como base de consulta, o que reduz alucinações e permite respostas atualizadas e específicas ao domínio, sem precisar retreinar o modelo.

#### Formato Markdown

##### O que é

Formato de texto simples que usa marcações leves (#, *, -, etc.) para estruturar títulos, listas e ênfases, sendo facilmente lido tanto por humanos quanto por modelos de IA, por isso é ideal para preparar documentos jurídicos como base de consulta.

#### Converter PDF em MD

Link para baixar o arquvi em pdf

#### Ferramenta

Gemini

#### Prompt

Construído na hora!

### 2 - Artefato para criar um contrato interativo

#### Preparação do conteúdo

##### Baixe o conteúdo do contrato em .md

[Baixe o material](materiais/proposta-servicos-advocaticios.md)

#### Ferramenta

Gemini Canvas

#### Prompt

```
Crie um web app interativo para uma proposta de prestação de serviços advocatícios. Ao topo, adicione 2 campos: Contratada e Contratante. Ao preencher estes campos, os demais são automaticamente preenchidos (replicando as informações). Além disso, adicione um campo para adicionar o valor total. A UI deve ter a anatomia de uma folha A4 para permitir baixar em PDF. O conteúdo da proposta está anexado em .md. Agora, atenção aos elementos de UI: Use técnicas de arquitetura da informação e visual law para representar os elementos. Use um visual minimalista light mode. Torne o campo de preenchimento de dados colapsável, para liberar espaço para ver o documento. O visual da proposta deve considerar seções em blocos:

- Um box ao topo determinando CONTRATADA E CONTRATANTE;
- Um box para o OBJETO;
- FLUXO DE TRABALHO deve ter o formato de timeline de eventos com ícones e textos explicativos;
- Um box de VALOR;
- Um box de DESPESAS;
- A seção de CONDIÇÕES deve ser uma lista com cada item numerado e a descrição da condição. O número em tamanho grande e ao lado a descrição. Use um visual de cards.
- A seção de ASSINATURAS deve ter 4 blocos de assinatura, em duas colunas, com linhas para assinatura e um ícone de caneta ao lado de cada linha.
- Na seção de INVESTIMENTO E HONORÁRIOS insira o valor cheio inserido no campo pelo usuário e calcule automaticamente o valor de entrada (considerando 30%) e o restante em 4 parcelas iguais.

Na parte inferior, um botão para baixar em PDF que deve exportar o documento tal qual o visual da página.
```

### 3 - Artefato Caso Penal Interativo

#### Preparação do conteúdo

Baixe o conteúdo do contrato em .md

#### Ferramenta

Gemini e Google Sites

#### Prompt

```
Atue como designer instrucional especializado em ensino de Direito e desenvolvedor front-end. Com base no processo penal anexado, analise o documento e crie uma experiência educacional interativa em um site estático, feito com HTML, CSS e JavaScript.

## Objetivo pedagógico

Ajudar o aluno a compreender o caso e percorrer suas etapas processuais, conectando fatos, provas, decisões, argumentos e fundamentos jurídicos. A experiência deve promover leitura ativa e reflexão: evite transformar o processo em um resumo longo ou em uma página de leitura estática.

## Regras de análise e fidelidade

1. Leia o processo na íntegra antes de definir as seções e os componentes do site.
2. Primeiro, extraia e organize o conteúdo pertinente. Só então planeje a experiência e escreva o código.
3. Não invente fatos, provas, argumentos, datas, atos processuais, decisões, dispositivos legais ou fundamentos que não constem no documento.
4. Diferencie com clareza:
   - fatos narrados e fatos reconhecidos na decisão;
   - alegações da acusação e da defesa;
   - elementos de prova e inferências;
   - decisões interlocutórias e decisão final;
   - entendimento do juízo e questões controvertidas.
5. Preserve o sentido e o contexto das citações. Identifique a página, folha, seção ou outro localizador disponível no documento. Se não houver paginação confiável, indique o trecho ou a seção de origem sem inventar referências.
6. Quando algo estiver ausente, ilegível ou ambíguo, sinalize isso. Não preencha lacunas por suposição.
7. Apresente conceitos jurídicos necessários à aprendizagem em linguagem acessível, sem distorcer o conteúdo nem substituir a análise do documento por explicações genéricas.
8. Não exponha dados pessoais desnecessários. Se houver informações sensíveis, use nomes ou identificadores abreviados na interface, sem alterar a compreensão jurídica do caso.

## Etapa 1 — Mapa analítico do processo

Antes de criar o site, produza um mapa conciso contendo:

- identificação geral do caso, conforme os dados disponíveis;
- questão central e questões secundárias;
- linha do tempo dos atos processuais;
- partes e papéis processuais;
- narrativa da acusação;
- versão ou teses da defesa;
- provas e o que cada elemento pode ou não demonstrar;
- decisões relevantes e seus fundamentos;
- resultado do julgamento e consequências indicadas no processo;
- divergências, limitações documentais ou pontos que exigem cautela;
- trechos essenciais, com localizadores e breve justificativa pedagógica.

Organize os itens de modo que o aluno consiga distinguir o que é alegação, prova, fundamento e conclusão judicial. Se o documento não contiver alguma informação, registre “não identificado no documento”.

## Etapa 2 — Desenho da experiência de aprendizagem

Com base no mapa, proponha um percurso didático que permita ao aluno explorar o caso do contexto ao julgamento. Selecione apenas as etapas que se aplicam ao processo analisado. Para cada etapa, indique:

- objetivo de aprendizagem;
- conteúdo do processo usado;
- interação que ajuda o aluno a pensar ou tomar uma decisão;
- feedback ou explicação revelada após a interação.

Considere, quando forem pertinentes, recursos como:

- abertura com uma pergunta-problema e orientação de navegação;
- linha do tempo clicável;
- painéis expansíveis para acusação, defesa, provas e decisão;
- caixas de diálogo para revelar explicações, excertos ou contexto;
- acordeões para aprofundar fundamentos sem sobrecarregar a tela;
- tooltips para termos jurídicos;
- comparação entre tese, evidência e resposta judicial;
- perguntas de checagem, ordenação de etapas ou associação entre provas e questões;
- pausas de reflexão antes de revelar a decisão;
- síntese final e questões para discussão.

Não use interações decorativas. Cada componente deve contribuir para a compreensão, a recuperação de informações ou a reflexão crítica do aluno. Dê destaque às partes centrais do caso, mantendo um caminho para explorar o restante do conteúdo relevante.

## Etapa 3 — Implementação do site

Entregue um site estático funcional, com:

- `index.html`;
- `styles.css`;
- `script.js`.

Use somente HTML, CSS, JavaScript e TailWind CSS via CDN, sem backend. Evite dependências externas; se alguma for indispensável, explique por quê e ofereça uma alternativa sem ela. Adote uma interface com cores carregadas, estilo cena do crime.

Requisitos de implementação:

- interface responsiva, legível e acessível;
- navegação clara entre etapas, com indicação de progresso;
- interações funcionais por teclado e mouse;
- elementos semânticos, foco visível, rótulos acessíveis e contraste adequado;
- JavaScript organizado e comentários nos trechos que ajudem a manutenção;
- conteúdo educacional separado da lógica de interação sempre que possível;
- sem botões ou controles que aparentem funcionar, mas não tenham ação;
- sem texto provisório, fatos fictícios ou referências inventadas.

O código deve abrir localmente em um navegador. Inclua instruções curtas para executar o site e explique a estrutura dos arquivos.

## Etapa 4 — Revisão final

Antes de concluir, confira se:

- o mapa analítico foi produzido antes da implementação;
- as afirmações e citações correspondem ao processo anexado;
- acusação, defesa, prova e decisão estão claramente diferenciadas;
- as interações funcionam e apoiam os objetivos de aprendizagem;
- o aluno consegue percorrer o caso sem precisar ler uma página inteira de texto estático;
- limitações e informações ausentes estão sinalizadas;
- o site funciona em telas pequenas e pode ser navegado por teclado.

Apresente o mapa analítico e o desenho didático junto com os arquivos do site. Se não for possível criar arquivos, forneça o conteúdo completo de cada arquivo em blocos separados, com o nome correspondente.
```

### 4 - Skill Engenheiro de Prompts Jurídicos

#### O que é

Skill que orienta a IA a elaborar e refinar prompts especializados para tarefas jurídicas, aplicando boas práticas de engenharia de prompts ao contexto do Direito para obter respostas mais precisas e consistentes.

#### Ferramenta

Claude ou Gemini

#### Prompt

Construído na hora!

### 5 - Skill de Petição Inicial Interativa Explicada

#### O que é

Skill que transforma uma petição inicial em um documento interativo, no qual cada seção ou termo pode ser explicado passo a passo, facilitando a compreensão do processo e do conteúdo jurídico pelo cliente ou leitor.

#### Ferramenta

Claude ou Gemini + Google Sites

#### Baixe o conteúdo

[Baixe o material](materiais/peticao-consignado-falso-emprestimo.md)

#### Prompt

```
# Petição Interativa

Você é um especialista em Legal Design, Visual Law e Pedagogia Jurídica. Sua tarefa é pegar o texto da petição inicial fornecida a seguir e transformá-lo em uma interface web interativa de aprendizagem (HTML/CSS/JavaScript standalone, responsiva e pronta para visualização).

Leve em consideração o tipo de petição anexado e ajuste-se conforme necessário.

### REQUISITOS DA INTERFACE INTERATIVA

1. **Layout em Painel Duplo (Side-by-Side):**
   - **Coluna Esquerda (Petição Inicial Navegável):** Apresente a estrutura da petição inicial dividida em blocos sanfonados (accordions/cards clicáveis). Cada bloco representa uma seção da peça (ex.: Endereçamento, Qualificação das Partes, Fatos, Fundamentação Jurídica/Direito, Tutela de Urgência, Pedidos e Valor da Causa).
   - **Coluna Direita (Box Estratégico & Pedagógico):** Painel dinâmico que atualiza automaticamente ao clicar em qualquer bloco da esquerda.

2. **Mecanismo de Interatividade:**
   - Inicialmente, os blocos da petição podem exibir um resumo ou o título. Ao clicar em um bloco:
     - O bloco se expande revelando a íntegra ou os trechos principais daquele segmento da petição.
     - A coluna direita carrega a **Análise Estratégica e Guiada** correspondente àquela seção específica.

3. **Conteúdo da Coluna Direita (Análise Estratégica):**
   Para cada bloco selecionado, a coluna direita deve exibir obrigatoriamente:
   - **Objetivo Estratégico:** Qual é a função processual dessa seção e o que o juiz/assessor busca ao lê-la.
   - **Dicas de Otimização & Visual Law:** O que adicionar ou destacar para aumentar a persuasão (ex.: uso de quadros resumidos, diagramas de fatos, grifos táticos).
   - **Erros Frequentes a Evitar:** Falhas comuns cometidas na prática forense nessa etapa.
   - **Checklist Prático:** Lista de verificação com o que não pode faltar no trecho.

4. **Design e Estética:**
   - Visual limpo, moderno e profissional (estilo dashboard/LMS jurídico).
   - Uso de cores sóbrias para o texto jurídico e destaques em cores contrastantes para os boxes pedagógicos.
   - Tipografia legível e botões intuitivos de expansão/revelação.
   - Estética minimalista e light mode.

5. *Stack*

   - Construa em formato de HTML estático, isto é: HTML, CSS e JavaScript;
   - Gere um único arquivo HTML;
   - Use Tailwind CSS via CDN.

### ESTRUTURA DA PETIÇÃO INICIAL PARA APLICAR O MODELO

[TEXTO DA PETIÇÃO EM ANEXO]
```

### 6 - Cofre de Prompts

#### O que é

Repositório organizado de prompts testados e reutilizáveis para tarefas jurídicas recorrentes, permitindo padronizar, armazenar e compartilhar as melhores instruções entre a equipe.

#### Ferramenta

Gemini e Google Sheets

#### Prompt

Construído na hora!
