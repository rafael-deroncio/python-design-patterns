# Interpreter - Behavioural (Comportamental)

## Intenção

*Dada uma linguagem, definir uma representação para a sua gramática juntamente com um interpretador que usa a representação para interpretar sentenças dessa linguagem.*

*Geralmente este padrão é relacionado com [DSL](https://pt.wikipedia.org/wiki/Linguagem_de_dom%C3%ADnio_espec%C3%ADfico) (Domain Specific Language), por exemplo: você pode usá-lo para escrever um programa para interpretaria linguagens como HTML, SQL, Expressões regulares, ou qualquer Linguagem de domínio específico que você venha a desenvolver.*

---

# Estrutura

O padrão Interpreter oficial descrito no livro GoF Design Patterns original não indica como construir uma Árvore de Sintaxe Abstrata. Como sua árvore é construída dependerá das construções gramaticais de sua sentença que você deseja interpretar.

Árvores de sintaxe abstratas podem ser criadas manualmente ou dinamicamente a partir de um script de analisador personalizado. No primeiro código de exemplo abaixo, construo o AST manualmente.

Uma vez que o AST é criado, você pode escolher o nó raiz e, em seguida, executar a operação Interpret nele e deve interpretar toda a árvore recursivamente.

# Implementação

O processo é converter as informações de origem, em uma **Árvore de Sintaxe Abstrata (AST)** de expressões **Terminal** e **Não-Terminal** que implementam um _interpret()_ método.

- Uma expressão não-terminal é uma combinação de outras expressões não-terminais e/ou terminais.

- Terminal significa terminado, ou seja, não há processamento adicional envolvido.

- Uma raiz AST começa com uma expressão não-terminal e, em seguida, resolve cada ramificação até que todas as expressões terminem.