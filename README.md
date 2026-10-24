# Projeto-de-banco-de-dados

Repositório destinado a um trabalho da faculdade de banco de dados de uma biblioteca.

## Requisitos funcionais

| ID | Descrição |
| :--: | :--: |
|RF01|Cadastrar, consultar e atualizar novos leitores.
|RF02|Cadastrar livros com ISBN, título, ano e editora.
|RF03|Associar um livro a 1 ou mais autores e um autor a 1 ou mais livros.
|RF04|Registrar exemplares físicos de cada livro, com código de tombo e situação.
|RF05|Registrar um empréstimo para 1 leitor, com data de empréstimo e data prevista.
|RF06|Incluir um ou mais exemplares em um empréstimo.
|RF07|Registrar a data de devolução de cada exemplar emprestado.
|RF08|Consultar empréstimos ativos, atrasados e o histótico por leitor.
|RF09|Consultar diponibilidade de empréstimos por livro.
|RF10|Impedir que o mesmo exemplar esteja em mais de um empréstimo ativo.

## Requisitos não funcionais

| ID | Descrição |
| :-- | :--: |
|RNF01|Usar um SGBD relacional e SQL compatível com o SGBD escolhido.
|RNF02|Garantir integridade referencial por PKs, FKs  e restrições adequadas.
|RNF03|Usar nomes consistentes para tabelas e atributos e documentar eventuais convenções.
|RNF04|Entregar scripts reproduzíveis , executáveis na ordem indicada, sem depender de dados externos.
|RNF05|Armazenar datas em tipos próprios de datas, e não como texto.

## Regras de negócio

| ID | Descrição |
| :--: | :--: |
|RN01|Cada leitor possui um identificador único e um e-mail único.
|RN02|Cada livro possui um ISBN único, Se for adotada uma variação de edição, documente como ela é identificada.
|RN03|Um livro pode te vários autores, e um autor pode ter vários livros.
|RN04|Cada exemplar pertence a exatamente um livro, um livro pode nenhum ou vários exemplares.
|RN05|Cada empréstimo pertence a exatamente um leitor e contém 1 ou mais exemplares.
|RN06|Um exemplar pode participar de vários empréstimos ao longo do tempo, mas não pode estar em mais de 1 empréstimo sem devolução ao mesmo tempo.
|RN07|A data prevista de devolução deve ser igual ou posterior a data de empréstimo. A devolução, quando informada, não pode anteceder o empréstimo.
|RN08|Um exemplar só pode ser emprestado se estiver disponível. Exemplares danificados ou baixados não podem compor empréstimos ativos.
|RN09|O atraso é calculado comparando a data prevista com a data atual quando não há devolução; Não é necessário armazenar um indicador de atraso.
|RN10|Para simplificar, cada item de empréstimo corresponde a 1 exemplar e tem uma data de devolução própria.