# 🏥 OrtoGuide: Agente de IA para Triagem Ortopédica

O **OrtoGuide** é um assistente virtual inteligente desenvolvido para otimizar o acolhimento de pacientes ortopédicos no SUS (foco inicial: Curitiba/PR). O sistema atua como uma ponte entre o paciente na sala de espera e a equipe de enfermagem, fornecendo educação em saúde e monitoramento de sintomas críticos em tempo real.

## 🎯 O Problema Resolvido
Em emergências ortopédicas, o tempo de espera pode gerar ansiedade e riscos clínicos. O OrtoGuide acolhe o paciente, lê a sua ficha de triagem, explica os possíveis cenários clínicos (sem dar diagnósticos) e alerta a enfermagem imediatamente caso o paciente relate sintomas de emergência (ex: Síndrome Compartimental Aguda).

## ⚙️ Arquitetura do Sistema
O projeto foi construído utilizando uma arquitetura baseada em eventos (Event-Driven) e microsserviços:

* **Front-end (Interface do Paciente):** Telegram Bot API.
* **Orquestrador (Backend/Middleware):** n8n (Node-based automation).
* **Cérebro (LLM):** Llama 3 (via Groq API) para processamento de linguagem natural com *Prompt Engineering* focado em restrições médicas de segurança (Guardrails).
* **Banco de Dados:** Google Sheets API (simulando o sistema de prontuário eletrônico do hospital).
* **Roteamento de Alertas:** Canal segregado no Telegram exclusivo para o "Painel da Enfermagem".

## 🚀 Principais Funcionalidades
- **Onboarding Automatizado:** Captura de CPF e busca instantânea no banco de dados.
- **Educação em Saúde:** Explicações sobre procedimentos ortopédicos, jejum e janelas de espera.
- **Detecção de Risco (Os 6 Ps):** O Agente de IA monitora ativamente palavras-chave (ex: "dedos frios", "dor insuportável") e executa um sub-fluxo de emergência.
- **Roteamento Inteligente:** Separa a comunicação B2C (Bot -> Paciente) da B2B (Bot -> Enfermagem).
- **Tratamento de Alucinações:** LLM estritamente contido por "Role-Boundary Jailbreaks" para não receitar medicamentos ou gerar falsas promessas de retorno em background.

## 🛠️ Como replicar
*(Aqui você pode adicionar instruções básicas de como importar o arquivo .json do seu n8n, se quiser disponibilizá-lo)*
