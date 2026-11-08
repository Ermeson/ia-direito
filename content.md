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

### 2 - Skill para criar um contrato interativo

#### Preparação do conteúdo

##### Baixe o conteúdo do contrato em .md

[Texto do link](https://exemplo.com)

#### Ferramenta

Gemini

#### Prompt

```
este é o prompt
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

Claude ou Gemini

#### Prompt

{prompt}

### 6 - Cofre de Prompts

#### O que é

Repositório organizado de prompts testados e reutilizáveis para tarefas jurídicas recorrentes, permitindo padronizar, armazenar e compartilhar as melhores instruções entre a equipe.

#### Ferramenta

Gemini e Google Sheets

#### Prompt

Construído na hora!
