# OrtoGuide - conceito acadêmico de acolhimento ortopédico

Documentação conceitual de um assistente virtual para educação e acolhimento de pacientes em uma fila de atendimento ortopédico. A proposta surgiu como exercício acadêmico sobre automação, linguagem natural e encaminhamento de alertas para uma equipe humana.

## Estado do projeto

- é um conceito de estudo, não um sistema clínico em funcionamento;
- o repositório não contém fluxo exportado do n8n nem integração implantada;
- não foi validado por profissionais de saúde e não deve orientar atendimento real;
- a idealização e a documentação tiveram apoio de ferramentas de IA.

## Fluxo imaginado

1. O paciente inicia uma conversa em um bot.
2. O fluxo consulta dados fictícios de uma planilha.
3. Um modelo de linguagem responde dentro de limites definidos no prompt.
4. Mensagens com sinais de alerta são encaminhadas para avaliação humana.

## Tecnologias consideradas

- n8n para orquestração;
- Telegram Bot para a interface de conversa;
- API de modelo de linguagem para gerar respostas;
- Google Sheets como fonte de dados fictícios.

## O que o projeto me ajudou a estudar

- desenho de fluxos no n8n;
- uso responsável de IA em um contexto sensível;
- limites entre orientação automatizada e decisão humana;
- necessidade de privacidade, validação profissional e tratamento de falhas.

## Próximos passos de aprendizado

- criar um fluxo mínimo somente com dados fictícios;
- versionar o arquivo exportado do n8n;
- documentar entradas, saídas e casos de erro;
- remover qualquer dado que possa identificar uma pessoa;
- testar o encaminhamento para atendimento humano sem simular diagnóstico.

Este repositório não substitui avaliação, triagem ou orientação de profissionais de saúde.
