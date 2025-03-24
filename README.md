Esse repositório contém um notebook baseado no tutorial [Machine Translation and Dataset](https://pt.d2l.ai/chapter_recurrent-modern/machine-translation-and-dataset.html).  

## Respostas dos Exercícios

### 9.5.7.1 - Impacto de `num_examples` no vocabulário

Ao aumentar `num_examples` na função `load_data_nmt`, observei que os tamanhos do vocabulário dos dois idiomas aumentam. Com mais exemplos, aparecem mais palavras únicas, expandindo o vocabulário. Quando reduzo `num_examples`, o vocabulário diminui, pois há menos palavras diferentes no conjunto de dados.

### 9.5.7.2 - Tokenização para chinês e japonês  

Não considero uma boa ideia, pois esses idiomas não usam espaços para separar palavras. Determinar os limites das palavras é complexo e propenso a erros. A tokenização em nível de caractere é uma alternativa melhor, pois cada caractere tem significado próprio e gera um vocabulário menor e mais consistente. Outra abordagem eficiente é a tokenização em subpalavras que captura padrões sem depender da segmentação explícita de palavras. O próprio texto da seção 9.5.7 sugere a tokenização em subpalavras como solução para desafios na modelagem de idiomas.