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
---

## 📖 Glossário de Termos Técnicos (FMCG & Trade Marketing)

* **FMCG (Fast-Moving Consumer Goods):** Bens de consumo de rápido giro (bebidas e alimentos de consumo diário)[cite: 1].
* **PDV (Ponto de Venda):** Estabelecimentos comerciais atendidos pelas rotas (bares, restaurantes, mercearias, conveniências).
* **GDM (Glass Door Merchandiser):** Expositores e geladeiras de porta de vidro no PDV.
* **Curva ABC (Regra 80/20):** Método de classificação de estoque onde 20% do portfólio (Classe A) representa cerca de 80% do faturamento de vendas[cite: 1].
* **SOVI / Share of Shelf:** Porcentagem de espaço físico ocupado pelas marcas da empresa na geladeira ou prateleira do cliente em relação aos concorrentes[cite: 1].
* **Ruptura / Out of Stock (OOS):** Ausência do produto nas prateleiras/geladeiras no momento da compra pelo consumidor final[cite: 1].

---

## 📚 Fontes e Materiais de Apoio Utilizados

* **`2-Trade-Marketing-no-Brasil.pdf`**: Documento de conceitos e práticas de Trade Marketing, comportamento do shopper e execução no PDV.
* **`curva_abc_totvs.pdf`**: Guia técnico sobre o princípio de Pareto aplicado à gestão de portfólio, margem e giro em vendas FMCG[cite: 1].
* **NotebookLM (Google):** Plataforma utilizada para compilação das fontes, testes de instrução e geração dos cadernos de apoio ao Sales Copilot.

---

## 🔗 Entrega DIO
* **Autor:** Rubens Oliveira Silva
* **Projeto:** Miniguia de Estudos / Sales Copilot com IA Generativa
* **Ferramenta de Suporte:** Google NotebookLM
---

## 📑 Miniguia de Estudos & Prompts Reutilizáveis (Entrega Final)

### 1. Resumo Estruturado do Aprendizado
* **Giro vs. Margem:** Produtos de alto giro (Classe A) sustentam a rentabilidade global do PDV pelo volume acumulado, mesmo com margens unitárias menores.
* **Execução de Geladeira (GDM):** O espaço gelado deve refletir a Curva ABC de vendas; produto gelado na posição nobre garante conversão imediata.
* **Contorno de Objeções:** A resposta eficaz combina empatia inicial com ancoragem na matemática comercial do cliente final.

### 🛠️ Kit de Prompts Reutilizáveis (Para Uso Diário)

Estes prompts foram calibrados no NotebookLM e podem ser reutilizados diretamente por representantes de vendas:

1. **Prompt para Objeção de Preço/Margem:**
   > *"Atue como um Consultor de Vendas FMCG. O cliente do PDV alega que a margem do produto [NOME DO PRODUTO] é baixa em relação à concorrência. Gere uma resposta em 3 frases focando na velocidade de giro do estoque e rentabilidade no mês."*[cite: 1]

2. **Prompt para Objeção de Espaço em Geladeira:**
   > *"O cliente diz que não tem espaço na geladeira para colocar nossa marca. Com base no conceito de Curva ABC, monte um argumento mostrando como substituir um item de baixo giro por um Classe A aumentará o faturamento dele."*[cite: 1]

3. **Prompt para Checklist de Execução Comercial:**
   > *"Gere um checklist rápido de 5 pontos para eu auditar a execução da geladeira (GDM) e o Share of Shelf antes de iniciar a negociação com o cliente."*[cite: 1]
