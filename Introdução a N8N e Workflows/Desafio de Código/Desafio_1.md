# Desafio 1

Em um banco digital, a equipe de operações está revisando fluxos simples criados no n8n para treinar novos analistas. Um dos fluxos recebe eventos de transações e decide rapidamente se a automação deve continuar, aguardar revisão humana ou encerrar por erro. Antes de publicar o fluxo em produção, voce precisa implementar a mesma regra em código para validar se a lógica básica foi entendida.

Leia três informações: o tipo do evento, o status recebido e a etapa atual do fluxo. Seu programa deve retornar uma única mensagem de controle. As regras são: se o tipo for PIX, o status for OK e a etapa for validar, retorne PROCESSAR. Se o tipo for TED, o status for OK e a etapa for validar, retorne AGENDAR. Se o status for ERRO, independentemente dos outros campos, retorne FALHA. Se a etapa for revisar, retorne ANALISAR. Para qualquer outra combinação válida, retorne IGNORAR. O problema envolve comparações simples de strings e prioridade de regras, como em um fluxo inicial do n8n. Considere as palavras exatamente como fornecidas, com letras maiúsculas e minúsculas relevantes.

## Entrada

A entrada contem três linhas. A primeira linha traz o tipo do evento, podendo ser PIX, TED ou outro texto. A segunda linha traz o status do evento. A terceira linha traz a etapa atual do fluxo.

## Saída

Exiba uma unica linha com uma das mensagens: PROCESSAR, AGENDAR, FALHA, ANALISAR ou IGNORAR, conforme as regras descritas.

Exemplos
A tabela abaixo apresenta exemplos de entrada e saída:

| Entrada |Saída  |
|--|--|
| PIX<br>OK<br>validar	| PIX	|
|PIX<br>OK<br>validar	| AGENDAR	|
|PIX<br>ERRO<br>validar	| FALHA	|
|DOC<br>OK<br>revisar	| ANALISAR	|

