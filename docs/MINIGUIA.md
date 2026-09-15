# IA Aplicada à Análise de Requisitos e Automação com n8n

## 1. Introdução
Este miniguia consolida os principais aprendizados do projeto desenvolvido com NotebookLM sobre o uso de Inteligência Artificial Generativa e automação no contexto de Engenharia de Requisitos.

A proposta central é demonstrar que a IA pode apoiar a triagem, organização e estruturação de solicitações, mas não deve substituir a análise crítica, a validação e a responsabilidade humana.

## 2. Fundamentos da Engenharia de Requisitos

### Requisito
Necessidade, condição ou capacidade que deve ser atendida para resolver um problema ou alcançar um objetivo.

### Elicitação
Processo de descobrir, levantar e esclarecer requisitos junto aos stakeholders e outras fontes.

### Stakeholder
Pessoa, grupo ou organização que influencia ou é afetada pelo sistema.

### Validação
Confirmação de que um requisito representa corretamente a necessidade do negócio.

### Rastreabilidade
Capacidade de relacionar um requisito à sua origem, evolução, implementação e testes.

### Regra de Negócio
Lógica ou restrição que orienta o funcionamento do negócio, frequentemente expressa no formato:

```text
SE [condição]
ENTÃO [ação]
```

## 3. Histórias de Usuário e Critérios de Aceite

Uma História de Usuário descreve uma necessidade sob a perspectiva do usuário.

```text
Como [persona]
Quero [objetivo]
Para [benefício]
```

Os Critérios de Aceite são condições claras, objetivas e verificáveis que precisam ser atendidas para que uma história ou requisito seja aceito.

Eles não devem ser confundidos com Definition of Done.

## 4. IA aplicada à Análise de Requisitos

A IA pode apoiar:
- organização de textos brutos;
- identificação de ambiguidades;
- identificação de lacunas;
- estruturação de informações;
- geração de perguntas para stakeholders;
- criação de rascunhos de histórias de usuário;
- apoio na criação de critérios de aceite;
- revisão de requisitos.

A IA deve atuar como assistente, não como aprovadora final.

## 5. Engenharia de Prompts

Um prompt profissional tende a conter:
- papel;
- objetivo;
- contexto;
- instruções;
- restrições;
- formato de saída.

### Prompt genérico

```text
Crie requisitos para um sistema de agendamento.
```

### Prompt estruturado

```text
Atue como Analista de Requisitos.

Antes de criar requisitos:
1. identifique informações ausentes;
2. separe fatos de suposições;
3. liste perguntas para stakeholders;
4. não invente regras;
5. marque informações não confirmadas como "Necessita validação".
```

## 6. Cicatrizes do Projeto

Durante os testes, foram identificados:
1. fontes insuficientes;
2. respostas genéricas;
3. mistura entre fatos e hipóteses;
4. cadeias de suposições;
5. cenários não sustentados;
6. confusão entre sugestão e regra confirmada.

Essas falhas levaram à melhoria da curadoria de fontes e do System Prompt.

## 7. Automação com n8n

```text
Formulário
→ Webhook
→ Validação
→ IA
→ Human-in-the-loop
→ Analista de Requisitos
→ Aprovar / Corrigir / Complementar / Rejeitar
→ Registro final
```

## 8. Human-in-the-loop

> A IA organiza e sugere. O Analista interpreta, valida e decide.

## 9. Estudo de Caso

```text
Quero que o aplicativo permita cancelar qualquer agendamento facilmente.
Acho que seria bom cobrar uma taxa quando a pessoa cancelar muito perto do horário.
```

```json
{
  "necessidade": "Permitir o cancelamento de agendamentos pelo aplicativo",
  "persona": "Usuário do aplicativo",
  "objetivo": "Permitir o cancelamento de agendamentos pelo aplicativo",
  "beneficio_esperado": "Necessita validação",
  "regras_negocio": [],
  "ambiguidades": [
    "facilmente",
    "muito perto do horário",
    "qualquer agendamento"
  ],
  "informacoes_ausentes": [
    "Confirmação se a cobrança de taxa será adotada como regra de negócio",
    "Definição das condições de antecedência para cancelamento"
  ],
  "perguntas_stakeholders": [
    "A cobrança de taxa será realmente adotada como regra de negócio?",
    "Quais tipos de agendamento poderão ser cancelados pelo aplicativo?"
  ],
  "cenarios_excecao": [],
  "status": "NECESSITA_REVISAO_HUMANA"
}
```

## 10. Riscos e Controles

| Risco | Controle |
|---|---|
| Invenção de regras | Restrições explícitas no prompt |
| Falta de contexto | Fontes confiáveis e contexto de negócio |
| Ambiguidade | Identificação de termos vagos |
| Cadeia de suposições | Perguntas em camadas |
| Automação excessiva | Human-in-the-loop |
| Informação ausente | Marcador `Necessita validação` |
| Perda de rastreabilidade | Registro estruturado e revisão humana |

## 11. Glossário

- **API:** interface de comunicação entre sistemas.
- **Critério de Aceite:** condição verificável para aceitação.
- **Elicitação:** descoberta e esclarecimento de requisitos.
- **História de Usuário:** necessidade descrita sob a ótica do usuário.
- **Human-in-the-loop:** revisão humana em etapas críticas.
- **IA Generativa:** IA capaz de gerar conteúdo a partir de instruções.
- **LLM:** modelo de linguagem de grande escala.
- **n8n:** plataforma de automação de workflows.
- **Prompt:** instrução enviada a um modelo de IA.
- **Rastreabilidade:** ligação entre origem, requisito, implementação e teste.
- **Regra de Negócio:** lógica que orienta o negócio.
- **Stakeholder:** parte interessada.
- **Webhook:** mecanismo de recebimento automático de dados.
- **Workflow:** sequência de etapas de um processo.

## 12. Prompts Reutilizáveis
Consulte `PROMPTS.md`.

## 13. Principais Aprendizados
- boas fontes são tão importantes quanto bons prompts;
- hipóteses não podem virar regras automaticamente;
- IA pode acelerar a análise sem substituir julgamento humano;
- prompts devem ser testados e refinados;
- revisão humana reduz riscos;
- automação deve preservar rastreabilidade;
- "Necessita validação" é preferível a inventar informação.

## 14. Conclusão

**Fontes confiáveis + Prompts estruturados + Automação n8n + Rastreabilidade + Análise crítica + Validação humana**

