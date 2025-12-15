# Você sabe a diferença entre Word Embedding, Chunking, Parsing e Tokenization?

## 🔥 Introdução

O universo da Inteligência Artificial, assim como em qualquer ramo da tecnologia, é cheio de termos, métodos e técnicas quem nem sempre são fáceis de se entender e diferenciar. Às vezes os ouvimos e até repetimos, mas sem compreender bem do que estamos falando.

Aqui temos três deles, muito aplicados aos contextos de Agentic AI e arquiteturas como RAG. Mas você entende o que são e sabe diferenciá-los? Neste artigo vamos conceituar e esclarecer estes pontos, bem como falar da importância e aplicabilidade de cada um deles.

Todos esses conceitos fazem parta da etapa de pré processamento de dados para NLP/PLN (Processamento de Linguagem Natural). São técnicas anteriores a popularização de Agentic AI, porém ganharam mais força devido seu papel neste contexto que está em alta.

Vamos abordar cada termo iniciando por sua definição teórica, usando citações da literatura especializada. Após, vamos discorrer sobre os eles em uma linguagem mais acessível, a fim de facilitar o entendimento.
  

## 🔍 Elementos linguísticos envolvidos

Para compreender bem os conceitos que são os alvos deste artigo, vamos revisar alguns elementos linguísticos importantes, tais como os Grupos Gramaticais e as Sintagmas. Ambos são utilizados para descrever diferentes aspectos da estrutura das frases e das palavras dentro de uma lingua.

### 🗂️ Grupos Gramaticais

Também chamados "Classes Gramaticais" ou "Classes de Palavras", são conjuntos de palavras que compartilham uma mesma função sintática ou morfológica dentro de uma frase. Exemplos de Grupos Gramaticais são substantivos, verbos, adjetivos, pronomes, artigos, numerais, advérbios, preposições, conjunções e interjeições, entre outros. Ou seja, as palavras são organizadas em Grupos Gramaticais com base em seu papel e em sua estrutura na linguagem.

Cada Grupo Gramatical exerce uma função específica como, por exemplo, nomear objetos, indicar ações, modificar significados, conectar ideias ou expressar sentimentos.​​ Em resumo, o Grupo Gramatical têm o propósito de agrupar todas as palavras de um mesmo tipo morfológico e funcional dentro de um idioma.

Em suma, sintagmas são grupos de elementos contíguos que funcionam juntos na construção de frases, estruturando o sentido e a grammática do enunciado.

### 🔠 Sintagmas

Sintagma é uma unidade linguística formada por uma ou mais palavras. As palavras são organizadas em torno de um núcleo e desempenham função sintática dentro da frase. O Sintagma, a depender do núcleo, pode ser verbal, nominal, adjetival, adverbial ou preposicional. As Sintagmas funcionam em conjunto para a construção das frases, estruturando o sentido e a gramática.​

O tipo de Sintagma, como dito, é definido pelo núcleo. Logo, um Sintagma nominal é um grupo de palavras cujo núcleo é um nome (substantivo). Uma Sintagm verbal têm como núcleo um verbo. E assim por diante.

Considere como exemplo a frase “Os alunos chegaram agora”. Nela, “os alunos” é um sintagma nominal e “chegaram agora” é um sintagma verbal.


## 🧩 Tokenization (Tokenização)

### ⚙️ Conceito e utilidade

É uma **etapa inicial do pré-processamento de textos** em linguagem natural (NLP) que faz a segmentação do texto. Em outras palavras, consiste em quebrar uma sequência de texto em unidades menores. Nesta etapa, o texto é dividido em **palavras**, **símbolos** ou **subpalavras**.

Jurafsky & Martin (2020), além de definir o conceito de Tokenization, dá também uma ideia da sua aplicabilidade, conforme abaixo:

> ...etapa inicial que divide o texto em unidades menores (tokens), como palavras, subpalavras ou caracteres, viabilizando análise automatizada e processamento eficiente de linguagem natural (Jurafsky & Martin, 2020).

Manning, Raghavan & Schütze (2008), em sua definição, abordam também um pouco do funcionamento da tecnica:

> Na tokenização, pegamos uma entrada (uma string) e um tipo de token (uma unidade significativa de texto, como uma palavra) e dividimos a entrada em partes (tokens) que correspondem ao tipo.

Considerando estas definições, podemos concluir que, no processo básico de tokenização por palavras, cada palavra corresponderá a um token. No exemplo "O rato roeu a roupa do rei de Roma", após o processo de tokenização, teremos o vertor de tokens abaixo:

```
["O", "rato", "roeu", "a", "roupa", "do", "rei", "de", "Roma"]
```

É mais fácil processar e analisar vetores do que longs testos em linguagen natural.

### 📌 Tokenization em modelos LLM

Nos contextos de Agentic AI e Generative AI, que envolvem o uso de LLMs (modelos de linguagem de grande porte), a tokenização funciona de modo diferente. Nesse caso, o conceito de "token" é mais flexível que o de "palavra", a quantidade de tokens de um texto vai depender do método de tokenização utilizado. Uma palavra pode ser representada por um ou mais tokens.

Em algoritmos como Byte-Pair Encoding (BPE) ou WordPiece palavras comuns ou curtas podem virar um token único, mas palavras longas, compostas, desconhecidas ou derivadas frequentemente são divididas em vários tokens menores, que podem ser subpalavras ou até caracteres individuais. Por exemplo, a palavra "darkness" pode ser dividida em dois tokens: “dark” e “ness”.

Em muitos casos, contudo, é interessante calcular quantos tokens estão sendo usados para, por exemplo, acionar modelos de LLM. Afinal, essa quantidade de tokens influencia no desempenho do modelo, em problemas como de alucinação e no valor da fatura a ser paga para os provedores de serviços em nuvem ou de modelos de ML.

### 💻 Exemplo de implementação para contagem de tokens

Caso você queira fazer uma medição básica, segue abaixo um código de referência. Isso pode ser útil para, por exemplo, estabelecer limites de consumo por segurança, gerar métricas de consumo para trabalhos analíticos ou fazer projeção de custos.

```
exemplo de implementação
```

## 🔤 Parsing

### 🔥 O que é Parsing?

Parsing é a tarefa de analisar um conjunto sequencial de símbolos, tokens ou palavras, a fim de determinar a estrutura gramatical e/ou compreender a relação entre os elementos do conjunto.

No contexto da PNL, o parsing é usado para interpretar sentenças segundo a gramática da língua em que essas sentenças se encontram. O Parsing é capaz de identificar elementos gramaticais, tais como sujeito, verbo e predicado.

O parsing é aplicável a diversos contextos. Por exemplo, pode-se utilizar o parsing para analisar queries SQL. Pode-se utilizar o parsing para a análise sintática da query ou para um algorítimo com objetivo de otimiza-la, entre outras aplicações possíveis.

O termo "Parsing" é usado para identificar tanto o processo de "parsing" quanto os algoritmos que implementam este processo.

### 🎯 Objetivo do Parsing

O objetivo do Parsing é transformar cadeias de texto em representações estruturadas, de acordo com a gramática da lingua ou linguagem em que se encontram. Essa é uma etapa fundamental para realizar tarefas como tradução automática, análise sintática e compreensão de textos e outros conjuntos de dados.

### 🏷️ Tipos de Parsing

Existem tipos diferentes de parsing, com objeticos específicos necessários a tarefa de interpretação de uma sentença, conforme abaixo:

- **Parsing Sintático:** Focado na estrutura da sentença;
- **Parsing Semântico:** Focado em encontrar o significado das relações entre os elementos da sentença;
- **Parsing Léxico:** Analisa menores unidades de entrada, que são os tokens.

### 🔬 Parsing completo e parcial (chunking)

Os conceitos de parsing completo e parcial são bastante discutidos no contexto e na literatura sobre PLN desde a década de 1980. Contudo, foi na obra entitulada “Parsing by Chunks”, de 1992, de Steven P. Abney, que a ideia de parsing parcial foi formalizada sob o nome de "chunking".

O chunking (parsing parcial) é uma alternativa ao parsing sintático completo que influenciou de forma significativa o desenvolvimento de métodos rápidos e práticos em PLN.

O **parsing completo** (ou "full parsing") é a **análise detalhada da estrutura sintática** de uma sentença. Ele produz um mapeamento sintático detalhado que mostra como cada parte da frase se relaciona com as demais.​

Já o **parsing parcial** (o "chunking", também chamado "shallow parsing") se refere a identificação dos **principais sintagmas**, tais como grupos nominais e verbais, sem detalhar hierarquias internas.​ Obviamente, essa abordagem é mais rápida. Ela é útil para tarefas onde é necessário representar toda a estrutura sintática da sentença.​


## 🔡 Chunking

### 🔥 O que é Chunking?

Chunking, como citado anteriormente, é o termo definido na obra “Parsing by Chunks”, de Abney (1992). O Chunking é uma dentre outras formas disponíveis para se implementar a técnica do parcing parcial.

Logo, o Chunking é a técnica que consiste em agrupar tokens em blocos gramaticais, tais como Sintagmas Nominais ou Sintagmas Verbais. Um boa definição de Chunking, que cita os conceitos de parsing completo e parcial, é a seguinte:

> No uso geral, os termos parsing e parser acabaram sendo adotados para se referir ao parsing completo. Já o parsing parcial é conhecido como chunking e a ferramenta como chunker, embora chunking seja uma dentre várias abordagens para a implementação do parsing parcial (...). O conceito de chunk foi proposto por Abney (1992) como uma unidade formada por uma única palavra ou por um conjunto de palavras. Em um chunk, há uma palavra de conteúdo circundada por palavras funcionais (Jurafsky & Martin, 2023). 

### 🎯 Objetivo do Chunking

Seu objetivo é faciliar a análise sintática e realizar extração de informação, conforme citação abaixo:

> Método que segmenta textos em partes ou "chunks" maiores que palavras (ex.: frases, sintagmas), facilitando análise sintática e tarefas como extração de informação (Ramshaw & Marcus, 1995).

### Alternativas ao Chunking

Alguns dos métodos mais usados para **parsing parcial** são baseados em técnicas que combinam **regras linguísticas** e **modelos estatísticos ou de aprendizado de máquina**. A seguir um resumo com alguns exemplos:

1. **Regras baseadas em gramática regular:** Usam **expressões regulares** ou **gramáticas de dependência superficial** para identificar padrões de sintagmas nominais (NP), verbais (VP) e preposicionais (PP). Pode ser implementada usando a bibliotecas **NLTK** (classe `RegexpParser`).

2. **Hidden Markov Models (HMMs)**: Modelo Estatístico que trata o chunking como um problema de rotulagem sequencial, estimando a sequência mais provável de chunks dados os tokens e suas etiquetas.

3. **Maximum Entropy Models (MEMMs):** Modelo Estatístico 

4. **Conditional Random Fields (CRFs)**: Modelo Estatístico ampliam os HMMs considerando dependências condicionais e recursos contextuais para maior precisão. São usados em tarefas como o *CONLL-2000 shared task*, referência clássica para chunking supervisionado.[2]

5. **Perceptrons e Support Vector Machines (SVMs):** treinados sobre corpora anotados (como o CoNLL corpus), eficazes para identificar fronteiras e tipos de chunks (NP, VP, PP).[3]

6. **Modelos baseados em Redes Neurais (como LSTMs ou BiLSTMs):** aplicam arquiteturas sequenciais profundas que consideram o contexto inteiro da frase para segmentação de chunks de forma mais robusta.[4]

7. **Métodos Probabilísticos e Híbridos:** Combinam **heurísticas linguísticas** (gramáticas superficiais) com **probabilidade estatística** sobre corpora anotados, buscando equilibrar velocidade e precisão — prática comum em sistemas atuais de PLN em larga escala.[5][3]

Em síntese, os métodos mais proeminentes atualmente são os **Modelos de Markov Ocultos (HMMs)**, **Conditional Random Fields (CRFs)** e as **redes neurais recorrentes (RNNs/BiLSTMs)**, frequentemente combinados com pré-processamentos gramaticais e POS tagging. Esses métodos assumiram a liderança devido à sua **eficiência computacional** e **precisão em identificar constituintes superficiais** de frases complexas.


## 🔢 Word Embedding

Depois que o texto é tokenizado, cada token (palavra, subpalavra etc.) é **convertido em vetor numérico contínuo**. Esses vetores permitem que o modelo “entenda” semelhanças semânticas e sintáticas entre as palavras.

A ideia é transformar palavras, que são entidades simbólicas, em números que um computador consiga manipular de forma eficiente, preservando **relações semânticas e sintáticas**.

### Características principais:

* Cada palavra é representada como um **vetor em um espaço de alta dimensão** (por exemplo, 50, 100, 300 dimensões).
* Palavras com significados semelhantes ficam próximas nesse espaço vetorial.
  👉 Exemplo: os vetores de **"rei"** e **"rainha"** ficam mais próximos que **"rei"** e **"banana"**.
* Captura não só a identidade da palavra, mas também relações como:
  [
  \text{vetor("rei")} - \text{vetor("homem")} + \text{vetor("mulher")} \approx \text{vetor("rainha")}
  ]

### Principais modelos de Word Embeddings:

* **Word2Vec (Google, 2013):** usa redes neurais simples (CBOW e Skip-Gram) para aprender embeddings.
* **GloVe (Stanford, 2014):** baseado em estatísticas globais de coocorrência de palavras.
* **FastText (Facebook, 2016):** leva em conta subpalavras (prefixos/sufixos), ajudando com palavras raras ou novas.

### Por que é útil?

Antes, as palavras eram representadas por **one-hot encoding** (vetores esparsos e de alta dimensão, sem semântica).
Os embeddings resolvem esse problema ao criar representações densas, permitindo que algoritmos de ML e Deep Learning entendam melhor o **contexto e o significado**.



## 🎯 Conclusão

* **Tokenização** = dividir.
* **Chunking** = agrupar em pedaços linguísticos (chuncks).

Essas etapas são **pré-processamento** do texto.

Word Embedding é uma **técnica de representação de palavras em forma de vetores numéricos contínuos**, usada em **Processamento de Linguagem Natural (PLN / NLP)**.


| Etapa           | O que faz                                                 | Exemplo                                       |
|:----------------|:----------------------------------------------------------|:--------------------------------------------- |
| **Tokenização** | Divide o texto em palavras, símbolos ou subpalavras       | "O gato dorme." → ["O", "gato", "dorme", "."] |
| **Chunking**    | Agrupa tokens em blocos gramaticais                       | `"O gato dorme"` → `[NP O gato] [VP dorme]`   |
| **Embedding**   | Transforma cada token em um vetor que captura significado | `"gato"` → `[0.12, -0.85, 0.33, ...]`         |


**exemplo prático em Python** mostrando claramente a diferença entre **tokenização**, **chunking** e **word embeddings**, usando a biblioteca **spaCy** (uma das mais populares em NLP).

---

### 💻 Exemplo completo com `spaCy`

```python
# Instale o modelo de linguagem do spaCy (apenas uma vez):
# !python -m spacy download pt_core_news_md

import spacy

# Carrega o modelo pré-treinado em português (com embeddings)
nlp = spacy.load("pt_core_news_md")

# Texto de exemplo
texto = "O gato dorme no sofá enquanto o cachorro observa."

# Processa o texto
doc = nlp(texto)

# --- 1️⃣ TOKENIZAÇÃO ---
print("=== TOKENIZAÇÃO ===")
for token in doc:
    print(token.text)

# --- 2️⃣ CHUNKING (agrupamento em sintagmas nominais) ---
print("\n=== CHUNKS (Sintagmas Nominais) ===")
for chunk in doc.noun_chunks:
    print(chunk.text)

# --- 3️⃣ WORD EMBEDDING ---
print("\n=== EMBEDDINGS (vetores numéricos) ===")
token_exemplo = doc[1]  # palavra "gato"
print(f"Palavra: {token_exemplo.text}")
print(f"Vetor (primeiros 10 valores): {token_exemplo.vector[:10]}")
print(f"Tamanho do vetor: {len(token_exemplo.vector)} dimensões")

# --- 4️⃣ SIMILARIDADE SEMÂNTICA ---
print("\n=== SIMILARIDADE ENTRE PALAVRAS ===")
gato = nlp("gato")[0]
cachorro = nlp("cachorro")[0]
sofa = nlp("sofá")[0]

print(f"similaridade(gato, cachorro) = {gato.similarity(cachorro):.3f}")
print(f"similaridade(gato, sofá) = {gato.similarity(sofá):.3f}")
```

---


### 🧪 Saída esperada (resumo):

```
=== TOKENIZAÇÃO ===
O
gato
dorme
no
sofá
enquanto
o
cachorro
observa
.

=== CHUNKS (Sintagmas Nominais) ===
O gato
O cachorro

=== EMBEDDINGS (vetores numéricos) ===
Palavra: gato
Vetor (primeiros 10 valores): [ 0.12, -0.32, 0.45, ...]
Tamanho do vetor: 300 dimensões

=== SIMILARIDADE ENTRE PALAVRAS ===
similaridade(gato, cachorro) = 0.78
similaridade(gato, sofá) = 0.32
```


## 📚 Bibliografia

ABNEY, Steven P. Parsing by Chunks. In: PRINCIPLE-BASED PARSING. Dordrecht: Springer, 1992. p. 257-278.

ABNEY, Steven P.; TENNY, Carol. Parsing by Chunks. In: Principle-Based Parsing. Dordrecht: Springer, 1992. p. 257-278.

BLOG RACKSPACE. Chunking NLP Techniques. 2024. Disponível em: <https://www.rackspace.com/blog/how-chunking-strategies-work-nlp>. Acesso em: 25 out. 2025.

BRASILEIRAESPLN. Capítulo 7 Ferramentas e recursos para o processamento sintático. Disponível em: <https://brasileiraspln.com/livro-pln/1a-edicao/parte4/cap7/cap7.html>. Acesso em: 25 out. 2025.

CAMACHO-COLLADOS, Jose; PILEHVAR, Mohammad Taher. Embeddings in Natural Language Processing. Draft. Disponível em: <https://josecamachocollados.com/book_embNLP_draft.pdf>. Acesso em: 25 out. 2025.

DATACAMP. O que é tokenização? Tipos, casos de uso e implementação. 2024. Disponível em: <https://www.datacamp.com/pt/blog/what-is-tokenization>. Acesso em: 25 out. 2025.

GOLDBERG, Yoav. Neural Network Methods for Natural Language Processing. San Rafael, CA: Morgan & Claypool, 2017.

JURAFSKY, Daniel; MARTIN, James H. Speech and Language Processing. 3. ed. draft (2023). Stanford University. Disponível em: <https://web.stanford.edu/~jurafsky/slp3/>. Acesso em: 25 out. 2025.

JURAFSKY, Daniel; MARTIN, James H. Speech and Language Processing. 3. ed. Stanford: Stanford University, 2023. Disponível em: <https://web.stanford.edu/~jurafsky/slp3/2.pdf>. Acesso em: 25 out. 2025.

JURAFSKY, Daniel; MARTIN, James H. Speech and Language Processing. 3. ed. preliminar. Stanford: Stanford University, 2020. Disponível em: <https://www.datacamp.com/pt/blog/what-is-tokenization>. Acesso em: 25 out. 2025.

MANNING, Christopher D.; RAGHAVAN, Prabhakar; SCHÜTZE, Hinrich. Introduction to Information Retrieval. Cambridge: Cambridge University Press, 2008. Disponível em: <https://smltar.com/tokenization.html>. Acesso em: 25 out. 2025.

MANNING, Christopher D.; SCHÜTZE, Hinrich. Foundations of Statistical Natural Language Processing. Cambridge: MIT Press, 1999.

MICHAELIS Dicionário. Sintagma. Disponível em: <https://michaelis.uol.com.br/moderno-portugues/busca/portugues-brasileiro/sintagma>. Acesso em: 25 out. 2025.

MIKOLOV, Tomas; CHEN, Kai; CORRADO, Greg; DEAN, Jeffrey. Efficient estimation of word representations in vector space. arXiv, 2013. Disponível em: <https://www.ibm.com/br-pt/think/topics/word-embeddings>. Acesso em: 25 out. 2025.

NVIDIA BLOG. Explicando Tokens: A Linguagem e a Moeda da IA. 2025. Disponível em: <https://blog.nvidia.com.br/blog/tokens-ia-explicados/>. Acesso em: 25 out. 2025.

RAMSHAW, Lance A.; MARCUS, Mitchell P. Text chunking using transformation-based learning. In: Very Large Corpora, 3., 1995, Cambridge. Proceedings... Cambridge: Cambridge University Press, 1995. Disponível em: <https://www.rackspace.com/blog/how-chunking-strategies-work-nlp>. Acesso em: 25 out. 2025.

TODAMATERIA. Sintagma nominal e verbal explicados com exemplos. 2022. Disponível em: <https://www.todamateria.com.br/sintagma-nominal-e-verbal/>. Acesso em: 25 out. 2025.
