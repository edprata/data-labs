# 🧠 Por quê usar Markdown no System Prompt de seus Agentes?

Data Science | Generative AI | Agentic AI | IA | ML

## 💡 Introdução

Na era dos Agentes de AI, um dos assuntos mais importantes é o Prompt Engineering. Basicamente, o Prompt Engineering trata de técnicas para a construção de prompts com alta eficiência, que são essenciais para a criação de Agentes de IA com ótimo desempenho, economia de tokens e respostas consistentes.

Se você desconhece o tema, recomendo antes a leitura [deste documento da Amazon](https://aws.amazon.com/pt/what-is/prompt-engineering/), que faz uma excelente introdução e apresenta todos os conceitos.

### 🎯 Objetivo deste artigo

Neste artigo serão apresentados alguns estudos que embasam a afirmação de que o uso de formatos estruturados, em especial o Markdown, oferece vantagens com relação ao texto plano e com relação a outros formatos estruturados, tais como HTML, XML e JSON.

O objetivo é conscientizar a respeito da importância de se estruturar o prompt, em especial o System Prompt, além de fornecer o embasamento teórico necessário para outros trabalhos e para defender o uso desta técnica no seu ambiente de trabalho.

### 🔥 Motivação: Consequências de um prompt ruim

Um prompt mal estruturado resulta em um Agente eneficiente, caro e que produz respostas ruins, inconsistentes e pouco aderentes as instruções fornecidas ao modelo LLM.

Por este motivo, muitos pesquisadores têm se dedicado ao tema, realizando experimentos que comprovam as vantagens de se utilizar formatos estruturados para construção de prompts, tais como o JSON e o Markdown.


## 📝 Paper 1: The Prompt Report: A Systematic Survey of Prompt Engineering Techniques

Este paper, de fevereiro de 2025, acessível [neste link](https://arxiv.org/abs/2406.06608), é uma das mais completas revisões da área de Prompt Engineering para IA generativa. Ele compila um vocabulário de 33 termos, oferece uma taxonomia de 58 técnicas de prompting para LLMs e 40 técnicas para outras modalidades.

Além disso, o paper apresenta práticas recomendadas e diretrizes para os mais avançados modelos de linguagem no mercado, como ChatGPT. Sua leitura é altamente recomendada para quem deseja se aprofundar no tema.

O paper fornece validação científica e prática a respeito do emprego de Markdown para system prompts, apresentando a técnica como vantajosa em termos de clareza, organização e capacidade do modelo em seguir instruções multi-etapas e com exemplos complexos.

No entanto, o paper não apresenta experimentos que permitam mensurar eficiência específica (tokens ou desempenho). Neste paper, a recomendação é baseada em metanálise de práticas, relatos da comunidade e observações qualitativas. Mais adiante, contudo, outras fontes usadas neste artigo suprirão esta carência inicial.

### 📈 Uso crescente de formatos estruturados

A pesquisa documentada no paper reconhece o uso crescente de formatos estruturados, incluindo Markdown, na engenharia de prompts. Reforça que essa prática ajuda na “segmentação lógica” do input, aprimorando a legibilidade para humanos e também para o modelo. O uso de Markdown, como técnica para formatação do System Prompt, é citado entre as estratégias recomendadas para estruturar instruções sobre o papel do agente, regras a serem seguidas por ele e exemplos no input.

### ✅ Vantagens do Markdown

O Markdown melhora a organização, a clareza e a interpretabilidade das instruções do prompt, o que apresenta potencial para aumentar a qualidade das respostas em geral, especialmente para prompts complexos que possuem vários tópicos, funções ou exemplos encadeados.

> *A formatação de prompts usando Markdown ou marcação leve semelhante oferece uma estrutura legível que suporta organização hierárquica (por exemplo, por meio de títulos, marcadores, blocos de código) e atenua a ambiguidade em instruções de várias etapas.* <br>(Seção 3.3, Prompt Structure and Formatting, pág.14)

Quanto ao uso do formato Markdown para System Prompts, o artigo afirma que:

> *Todos os protocolos de experimentos e modelos de melhores práticas fornecidos nesta pesquisa recomendam o uso de cabeçalhos e marcadores Markdown para melhorar a clareza e a explicitude dos prompts.* <br>(Tabela 3, System Prompt Best Practices, pág.16)

### 💰 Economia de tokens e eficiência

Embora não apresente benchmarks quantitativos a respeito da economia de tokens ou sobre ganho de eficiência, o paper reforça o uso de Markdown como um padrão em projetos avançados de engenharia de prompt pela comunidade profissional.

Essa prática é apontada como uma técnica que leva a obtenção de maior controle sobre o agente e sobre sua conformidade com as instruções fornecidas (System Prompt).

> *No geral, o Markdown surge como um padrão de fato para formatação de prompts na indústria e na pesquisa, sendo creditado por facilitar a conformidade do modelo com instruções complexas e validação humana de componentes de prompts.* <br>(Conclusão, página 34)


## 📝 Paper 2: ReaderLM‑v2: Small Language Model for HTML to Markdown and JSON

Este segundo paper, acessível [neste link](https://arxiv.org/abs/2503.01151), apresenta evidências técnicas e experimentais que destacam as vantagens do uso de formatos estruturados, tais como Markdown e JSON, em pipelines de processamento e grounding de modelos de linguagem.

### 🗜️ Prompts compactos e redução de tokens

Segundo o paper, o Markdown resulta em documentos mais compactos e uso reduzido de tokens, se comparado a JSON e HTML.

> *Ao converter HTML bruto e ruidoso em Markdown estruturado, reduzimos significativamente o conteúdo não informativo e facilitamos a tokenização e o processamento posterior mais eficientes, especialmente para tarefas de LLM de longo contexto.* <br>(Seção 3, Model Effectiveness, páginas 3-4)

> *Testes empíricos mostram que a representação mais compacta do Markdown geralmente se traduz em contagens de tokens mais baixas (em comparação com HTML bruto ou JSON), oferecendo suporte a implantações de LLM econômicas.* <br>(Seção 3, Model Effectiveness, páginas 3-4)

### ⚡ Facilitação do aprendizado multitarefa

No artigo é discutido que o Markdown facilita o aprendizado multitarefa, devido oferecer uma representação sem ruídos, mais informativa do ponto de vista estrutural. Isso favorece tarefas de extração de informações e alinhamento semântico, que são recursos críticos para grounding de LLMs.

> *Descobrimos que a utilização do Markdown não apenas melhora a fidelidade da extração, mas também simplifica o alinhamento semântico para configurações multitarefa, pois a marcação fornece segmentação explícita de conteúdo, títulos e listas.* <br>(Seção 4, Training Framework and Objectives, páginas 4-5)

Por consequência, essa técnica evita a ambiguidade, aumenta a clareza e cria o cenário adequado para respostas mais aderente às instruções do System Prompt, com maior qualidade geral.

### ⚡ Melhorias na legibilidade e na consistência sintática

A conclusão do artigo é que o uso de Markdown melhora a legibilidade, a consistência sintática e a compatibilidade entre modelos, principalmente em contextos de extração e preparação de dados textuais para aplicações baseadas em IA generativa.

> *No geral, a transição para Markdown resulta em melhorias tanto na legibilidade quanto na consistência sintática, o que é benéfico para o alinhamento entre pequenos extratores de documentos e grandes LLMs. A ampla compatibilidade do formato também o torna uma opção natural para pipelines de vários estágios com modelos generativos ou discriminativos.* <br>(Discussion and Conclusion, páginas 7-8)

### ✅ Recomendação de uso do Markdown

Como observado, o uso do Markdown foi avaliado e defendido pelos autores do paper, tanto do ponto de vista de desempenho experimental quanto de benefícios práticos para legibilidade, estrutura e economia no contexto de IA generativa em larga escala.


## 📝 Paper 3: Does Prompt Formatting Have Any Impact on LLM Performance?

O paper, acessível [neste link](https://arxiv.org/abs/2411.10541), examina a forma como diferentes formatos de prompts, incluindo Markdown, JSON, YAML e texto simples, afetam o desempenho dos modelos GPT, com foco nas tarefas de raciocínio, geração de código e tradução.

### 💡 Captura da intenção da tarefa

O artigo apresenta o Markdown como um formato estruturado cujas vantagens são a combinação da legibilidade humana com uma hierarquia clara. Segundo o artigo, isso permite que o modelo capture melhor a intenção da tarefa. É destacado também que o uso de Markdown têm potencial para melhorar tanto a organização da informação quanto a interpretação do contexto pelo modelo.

> *Os templates em Markdown utilizam sintaxe de marcação leve para introduzir uma estrutura hierárquica e melhorar a legibilidade tanto para humanos quanto para modelos. Isso permite que os modelos interpretem melhor instruções multi-etapas e distingam entre exemplos, comentários e diretrizes dentro do prompt.* <br>(Seção 3.2, Prompt Templates, página 3)  

### ⚖️ Equilíbrio entre flexibilidade e estruturação

O formato Markdown é apontado como um formato que equilibra flexibilidade e estruturação, beneficiando tarefas complexas.

> *Markdown foi escolhido como um formato intermediário que equilibra expressividade e rigidez, oferecendo um prompt mais organizado que texto simples, mas evitando a verbosidade e rigidez de JSON ou YAML.* <br>(Seção 4.1, Experimental Setup, página 4)

### 🧘 Fidelidade às instruções

Os resultados dos experimentos apontam que o modelo GPT-3.5-turbo, por exemplo, apresenta até 40% de variação na performance em tarefas de tradução de código, dependendo do formato do prompt. Neste contexto, o Markdown é um dos formatos com melhor desempenho.

O paper sugere que o Markdown ajuda o modelo a seguir contexto e exemplos múltiplos com maior fidelidade, evitando ambiguidades e erros frequentes que ocorrem com formatos mais rígidos.

> *Observamos que a acurácia do GPT-3.5-turbo na tradução de código varia até 40% dependendo do formato do prompt. Prompts em Markdown superam consistentemente texto simples e JSON na maioria das tarefas, provavelmente devido a uma melhor clareza e sinais estruturais que ajudam o modelo a seguir instruções complexas.* <br>(Seção 5.2, Results and Discussion, página 6-8)

### 🔍 Maior legibilidade

Na conclusão do artigo são destacados a ótima legibilidade do formato Markdown e a consequente melhora no entendimento do modelo. 

> *Markdown se destaca como forte candidato para formatação de prompts devido à sua legibilidade, facilidade de criação e preservação efetiva da estrutura, que melhora o entendimento do modelo e o desempenho em tarefas de raciocínio e geração.* <br>(Conclusão, página 10)

### 🎯 Conclusão do Paper

O paper confirma, através de experimentos, que o Markdown é um formato que combina clareza, eficiência e robustez para LLMs, melhorando a qualidade dos outputs em diversas tarefas.


## 👥 Referências da Comunidade e Outras

[Essa thread](https://community.openai.com/t/markdown-is-15-more-token-efficient-than-json/841742) da comunidade OpenAI (2024), indica que o Markdown costuma consumir cerca de 15% menos tokens que JSON em prompts e respostas de LLMs, melhorando o desempenho e o custo computacional.

O artigo [MDEval: Evaluating and Enhancing Markdown Awareness in Large Language Models](https://arxiv.org/html/2501.15000v1) aborda diretamente os temas da eficiência, qualidade e clareza no uso de Markdown para prompts em LLMs, porém, analisando o uso do Markdown no output de dados. O documento chega a conclusões muito semelhantes a outras fontes apresentadas aqui, ou seja, que o uso do Markdown aumenta a eficiência geral e economiza tokens, comparado a outros formatos de dados estruturados.

## 🎯 Conclusão

Diversas fontes, bastante atuais, experimentando modelos de ML diferentes, confirmam que o uso de formatos estruturados, em especial o formato Markedown, oferece muitas vantagens quando aplicados ao System Prompt de Agentes de IA Generativa utilizando modelos LLM.

Entre as principais vantagens destacam-se:

1. Melhora a organização, a clareza e a interpretabilidade das instruções do prompt (entendimento do modelo);

2. Oferece uma estrutura legível que suporta organização hierárquica;

3. Proporciona prompts compactos e redução de tokens;

4. Facilita o aprendizado multitarefa;

5. Evita a ambiguidade;

6. Equilibra flexibilidade e estruturação, beneficiando tarefas complexas.

7. Permite ao modelos seguir contexto e exemplos múltiplos com maior fidelidade.


## 📚 Referências

1. [O que é engenharia de prompts?](https://aws.amazon.com/pt/what-is/prompt-engineering/)

2. [The Prompt Report: A Systematic Survey of Prompt Engineering Techniques](https://arxiv.org/abs/2406.06608)

3. [ReaderLM‑v2: Small Language Model for HTML to Markdown and JSON](https://arxiv.org/abs/2503.01151)

4. [Does Prompt Formatting Have Any Impact on LLM Performance?](https://arxiv.org/abs/2411.10541)

5. [MDEval: Evaluating and Enhancing Markdown Awareness in Large Language Models](https://arxiv.org/html/2501.15000v1)
