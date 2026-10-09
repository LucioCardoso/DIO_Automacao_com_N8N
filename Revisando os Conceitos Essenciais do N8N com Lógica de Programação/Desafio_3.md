# Desafio 3


Em um banco digital, a equipe de automações usa fluxos no n8n para tratar eventos simples antes de enviar dados para outros setores. Um dos fluxos recebe o status de uma etapa e precisa decidir rapidamente qual sera a próxima ação. Como você está revisando os conceitos essenciais de lógica de programação aplicados ao n8n, sua tarefa é simular esse comportamento em um pequeno validador.

Implemente um programa que leia uma única string representando o status recebido pelo fluxo. Os valores válidos são: START, PROCESS, ERROR e END. O programa deve responder com a próxima ação correspondente: START gera VALIDATE, PROCESS gera SAVE, ERROR gera RETRY e END gera FINISH. Se a string informada não for exatamente um desses quatro valores, o programa deve retornar INVALID. A comparação deve ser exata, respeitando letras maiúsculas e minúsculas. O problema possui apenas uma decisão central: mapear corretamente o status de entrada para a resposta esperada, sem usar bibliotecas externas.

## Entrada

A entrada contem uma única linha com uma string representando o status recebido pelo fluxo bancário.

## Saída

Exiba uma única linha com a ação correspondente ao status informado, seguindo exatamente o mapeamento definido. Caso o valor seja inválido, exiba INVALID.

## Exemplos
A tabela abaixo apresenta exemplos de entrada e saída:

| Entrada |Saída  |
|--|--|
| START	| VALIDATE	|
|PROCESS	| SAVE	|
|ERROR	| RETRY	|
|process	| process	|

