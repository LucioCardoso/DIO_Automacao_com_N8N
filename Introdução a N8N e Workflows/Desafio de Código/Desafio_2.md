# Desafio 2

Em um banco digital, a equipe de operações está revisando fluxos simples no n8n antes de liberar automações reais. Um dos testes simula um no de decisão que recebe o status de uma solicitação e precisa encaminhá-la corretamente. Como analista iniciante, sua tarefa e reproduzir essa regra com lógica de programação, garantindo que cada entrada gere exatamente uma resposta padronizada.

Implemente um programa que leia uma unica string representando o status recebido pelo fluxo. Os valores válidos são: APROVADO, PENDENTE e NEGADO. Se o status for APROVADO, o programa deve indicar que a automação segue para pagamento. Se for PENDENTE, deve indicar que a automação segue para análise manual. Se for NEGADO, deve indicar que a automação segue para encerramento. Qualquer outro valor deve ser tratado como erro de integração. Considere comparação exata, incluindo letras maiúsculas. O problema envolve apenas uma decisão simples, semelhante a um bloco condicional usado em automações básicas.

## Entrada

A entrada contem três linhas. A primeira linha traz o tipo do evento, podendo ser PIX, TED ou outro texto. A segunda linha traz o status do evento. A terceira linha traz a etapa atual do fluxo.

## Saída

Exiba uma única linha com uma das mensagens exatas: PAGAMENTO, ANALISE_MANUAL, ENCERRAMENTO ou ERRO_STATUS.

## Exemplos
A tabela abaixo apresenta exemplos de entrada e saída:

| Entrada |Saída  |
|--|--|
| APROVADO	| PAGAMENTO	|
|PENDENTE	| ANALISE_MANUAL	|
|NEGADO	| ENCERRAMENTO	|
|EM_ANALISE	| ERRO_STATUS	|


