# 🚀 Sales Copilot: Copiloto de Vendas com IA & Engenharia de Prompts

> **Desafio de Projeto — Digital Innovation One (DIO)**  
> **Tema:** Aprendizagem Ativa, Curadoria de Conteúdo e Engenharia de Prompts Aplicada a Vendas  
> **Autor:** Rubens Oliveira Silva  

---

## 📌 Contexto e Objetivos

No mercado de distribuição e vendas do setor de bebidas (FMCG), o contorno rápido e estratégico de objeções nos Pontos de Venda (PDVs) é determinante para a conversão de metas, giro de estoque e margem de lucratividade.

O objetivo deste projeto foi desenvolver uma **ferramenta prática de Copiloto de Vendas** baseada em IA, capaz de gerar roteiros persuasivos em 4 passos para vendedores em tempo real, cobrindo objeções comuns como giro de estoque, preço, espaço em geladeira e concorrência.

### Objetivos de Aprendizagem:
1. Mapear as principais objeções de clientes em PDVs para diferentes categorias de bebidas (Cervejas Premium, Mainstream, Refrigerantes Zero, RTD, etc.).
2. Aplicar técnicas avançadas de **Engenharia de Prompts** (Roleplay, Contextualização de Cenário, Ancoragem e Gatilhos Mentais).
3. Desenvolver uma interface web interativa (HTML5/CSS3/JavaScript) que simule o funcionamento do motor de IA e exiba o *Blueprint* do Prompt em tempo real.

---

## 📚 Curadoria de Fontes

Para alimentar a base de conhecimento do assistente e calibrar as diretrizes de resposta, foram utilizadas as seguintes fontes abertas e materiais de referência em gestão comercial e negociação:

1. **Metodologia de Vendas Consultivas em Bebidas (FMCG):** Matrizes de contorno de objeções focadas em giro vs. margem de lucro por categoria de produto.
2. **Modelo de Avaliação & Performance:** Conceitos aplicados de cultura organizacional, metas de cobertura e dinâmicas de PDV.
3. **Engenharia de Prompt para IA Generativa:** Documentação da OpenAI e Google DeepMind sobre estruturação de *System Prompts*, variáveis de contexto e poucas amostras (*few-shot prompting*).
4. **Artigos de Trade Marketing e Distribuição:** Guias práticos sobre execução de geladeira, *layouting*, Curva ABC de vendas e venda casada em pontos de dose e autosserviço.

---

## 🛠️ Engenharia de Prompts & "Cicatrizes" (Troubleshooting)

A construção dos roteiros passou por diversas iterações para garantir que a resposta da IA não fosse genérica, mas sim hipercontextualizada para a realidade do vendedor.

### 🧪 Testes de Prompts e Evolução

* **Prompt V1 (Genérico):** *"Crie um texto para convencer o cliente a comprar Spaten."*
  * **Problema:** A resposta gerava um texto muito longo, teórico e impossível de ser dito verbalmente em um balcão de bar.
* **Prompt V2 (Com Papel Definido):** *"Você é um supervisor de vendas. Crie um argumento contra a objeção 'está caro' para o produto Spaten."*
  * **Problema:** Focava apenas em dar desconto e não na proposta de valor ou na matemática comercial do cliente final.
* **Prompt V3 (Final / Mestre - Estruturado em 4 Passos):**
  ```text
  SYSTEM PROMPT:
  Você é um especialista em vendas e inteligência comercial no setor de bebidas.
  Gere um roteiro de contorno de objeções em 4 passos estruturados para o vendedor.

  PARÂMETROS DE ENTRADA:
  - Vendedor: "{vendedor}"
  - Cliente (PDV): "{cliente}"
  - Produto: "{produto}" (Categoria: {categoria})
  - Objeção: "{objecaoTexto}"

  ESTRUTURA DE RESPOSTA ESPERADA:
  Passo 1: Desarmar a objeção (Empatia / Gatilho Mental)
  Passo 2: Ancoragem de Valor / Matemática Comercial
  Passo 3: Ação Prática / Experiência no PDV
  Passo 4: Fechamento Comercial (Pergunta Diretiva)
