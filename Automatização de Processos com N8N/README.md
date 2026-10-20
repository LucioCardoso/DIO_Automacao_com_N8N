# AUTOMATIZAÇÃO DE PROCESSOS COM N8N

# Desafio Criativo: Planejando Automações com N8N Usando Apenas Bons Prompts

Nesta atividade, você seguirá algumas etapas simples que, ao final, irão ajudar a planejar uma automação em N8N a partir de um prompt claro e estruturado.

## 1. Sobre o Exercício

Um bom prompt nasce de intenção clara, contexto e instruções específicas. Durante o desafio, você irá organizar suas ideias e transformá-las em comandos claros.

## 2. Construção Passo a Passo
Cada etapa adicionará uma nova peça ao seu prompt final. Ao concluir todas, você terá um prompt capaz de orientar uma IA a produzir exatamente o que você imaginou.

## 3. Como Resolver
Siga cada passo com atenção, registre suas respostas e, ao final, una todos os elementos para formar seu prompt final. Aproveite o processo criativo!

### Passo 1: Defina a automação desejada

Nesta etapa, você vai descrever qual processo deseja automatizar e quem será beneficiado por ele.

#### a. O que fazer?

Responda:

- Qual tarefa repetitiva você deseja automatizar?
- Quem utilizará ou será impactado pela automação?
- Qual resultado final deve acontecer?

#### b. Modelo para você adaptar

Copie o bloco abaixo no seu editor de texto e preencha os campos entre colchetes:

> Quero criar uma automação no N8N para *[processo]*.
> 
> Público ou responsável:
> *[quem utilizará]*
> 
> Resultado esperado:
> *[resultado desejado]*

#### c. Modelo preenchido

> **Objetivo:** Quero criar uma automação no N8N para tomada de ação de compra e/ou venda de ações.
> 
> **Público:** investidores iniciantes de Bolsa de Valores
> 
> **Resultado esperado:** a partir de uma lista (planilha) com ações desejadas / adquiridas, um preço de aquisição, data de aquisição, status de comprada ou não, um preço base definido e uma % de lucro definida, decidir se é hora de comprar e/ou vender determinada ação.  A automação deve enviar um aviso para o cliente avisando que é hora de comprar e/ou vender determinada ação.  As transações de compra e/ou venda, bem como, do lucro e/ou prejuízo alcançado devem ser anotadas numa planilha de transações.

###  Passo 2: Adicione contexto e regras

Nesta etapa, você vai  **informar os sistemas envolvidos, as etapas do fluxo e as restrições importantes**.

#### a. O que fazer?

Responda:

-   Quais ferramentas ou serviços participam da automação?
-   Quais etapas devem acontecer em sequência?
-   Existe alguma regra, validação ou exceção?

#### b. Modelo para você adaptar

Copie o bloco abaixo no seu editor de texto e preencha os campos entre colchetes:

> Ferramentas envolvidas:
> *[lista de ferramentas]*
> 
> Fluxo desejado:
> 1. *[etapa 1]*
> 2. *[etapa 2]*
> 3. *[etapa 3]*
> 
> Regras importantes:
> *[restrições, validações ou exceções]*

#### c. Modelo preenchido

> **Ferramentas envolvidas:** Google Sheets, brapi (https://brapi.dev/), Gmail e Telegram.
>
> **Fluxo desejado:**
> 1. Ler dados de uma planilha do Google Sheets na qual está listada uma relação códigos de ação, preço alvo aquisição, status de "Adquirida" ou "Desejo", preço de aquisição, data de aquisição, preço alvo de venda;
> 2. Obter valor das ações listadas na planilha via API brapi e salvar numa aba da planilha do Google Sheets;
> 3. Se valor da ação estiver igual ou inferior ao preço de aquisição, enviar mensagem ao Telegram avisando que é hora de comprar a ação desejada;
> 4. Atualizar a planilha com o preço de aquisição, data de aquisição e mudar status para "Adquirida";
> 5. Registrar a transação na aba "Transações" (data, código ação, ação - compra ou venda e valor da compra ou venda);
> 6. Se a ação já foi adquirida e o valor da ação estiver igual ou superior ao preço alvo de venda, enviar uma mensagem ao Telegram avisando que é hora de vender a ação;
> 7. Registrar a transação na aba "Transações" (data, código ação, ação - compra ou venda e valor da compra ou venda);
> 8. Enviar planilha do Google Sheets como anexo de um e-mail do Gmail para mim.
> **Regras importantes:** limite de uso da API = 15.000 requisições por mês.

###   Passo 3: Monte o prompt final

Nesta etapa, você vai  **unir todas as peças construídas anteriormente em um único prompt completo**.

#### a. O que fazer?

Revise:

-   O objetivo da automação está claro?
-   As etapas estão em ordem?
-   As regras e restrições foram informadas?

#### b. Modelo para você adaptar

Copie o bloco abaixo no seu editor de texto e preencha os campos entre colchetes:

> Atue como um especialista em N8N.
> 
> Crie uma automação para [processo].
> 
> Público:
> [público]
> 
> Ferramentas envolvidas:
> [ferramentas]
> 
> Fluxo:
> [etapas]
> 
> Regras:
> [regras]
> 
> Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.

## Prompt Final

**Atue como um especialista em N8N:**
>
> **- Objetivo:** Crie uma automação no N8N para tomada de ação de compra e/ou venda de ações.
> 
> **- Público:** investidores iniciantes de Bolsa de Valores.
> 
> **- Ferramentas envolvidas:** Google Sheets, brapi (https://brapi.dev/), Gmail e Telegram.
> 
> **- Fluxo desejado:**
> 1. Ler dados de uma planilha do Google Sheets na qual está listada uma relação códigos de ação, preço alvo aquisição, status de "Adquirida" ou "Desejo", preço de aquisição, data de aquisição, preço alvo de venda;
> 2. Obter valor das ações listadas na planilha via API brapi e salvar numa aba da planilha do Google Sheets;
> 3. Se valor da ação estiver igual ou inferior ao preço de aquisição, enviar mensagem ao Telegram avisando que é hora de comprar a ação desejada;
> 4. Atualizar a planilha com o preço de aquisição, data de aquisição e mudar status para "Adquirida";
> 5. Registrar a transação na aba "Transações" (data, código ação, ação - compra ou venda e valor da compra ou venda);
> 6. Se a ação já foi adquirida e o valor da ação estiver igual ou superior ao preço alvo de venda, enviar uma mensagem ao Telegram avisando que é hora de vender a ação;
> 7. Registrar a transação na aba "Transações" (data, código ação, ação - compra ou venda e valor da compra ou venda);
> 8. Enviar planilha do Google Sheets como anexo de um e-mail do Gmail para mim.
> 
> **- Regras importantes:** limite de uso da API = 15.000 requisições por mês.
> 
> **- Resultado esperado:** Explicação de quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.
