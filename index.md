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

{prompt}

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
