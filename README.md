# 🏥 Assistente Médico Clínico com RAG (Retrieval-Augmented Generation), Prontuário Sintético & Fine-Tuning com qLoRA (Quantized Low-Rank Adaptation)

## 📌 Visão Geral
Este projeto implementa um **assistente clínico inteligente e auditável**, combinando:

- 📚 Conhecimento médico geral (MedQuAD + FAISS (Facebook AI Similarity Search))
- 🧾 Dados clínicos estruturados (EHR (Electronic Health Record) sintético)
- 🧭 Roteamento determinístico de intenções
- 🛡️ Guardrails clínicos rígidos
- 🧠 Fine-tuning eficiente com LoRA / QLoRA
- 🔎 Fontes rastreáveis e explicáveis

O objetivo é demonstrar uma **arquitetura segura e reprodutível** para aplicações de IA em saúde.

---

## 🧩 Pipeline Completo — Blocos 1 a 13

### 🔹 Bloco 1 — Setup e Estrutura de Diretórios
Configuração do Google Colab + Google Drive.

### 🔹 Bloco 2 — Download do Dataset MedQuAD
Clonagem e seleção de tópicos médicos relevantes.

### 🔹 Bloco 3 — Processamento do MedQuAD
Parsing XML, limpeza e geração do `medquad_qa.csv`.

### 🔹 Bloco 4 — Geração de EHR Sintético
Geração de pacientes, visitas, diagnósticos, prescrições e exames.

### 🔹 Bloco 5 — Funções Determinísticas de EHR
Camada segura de consulta clínica sem LLM.

### 🔹 Bloco 6 — FAISS + Tools + Router + LangGraph
Construção do RAG e roteamento de intenções.

### 🔹 Bloco 7 — Pipeline RAG Completo
Integração EHR + MedQuAD.

### 🔹 Bloco 8 — LLM com Guardrails Clínicos
Geração textual controlada, sem interpretação clínica.

### 🔹 Bloco 9 — Fine-Tuning com LoRA / QLoRA
Ajuste eficiente com fallback automático.

### 🔹 Bloco 10 — Integração do Modelo Fine-Tuned
Substituição transparente do modelo base.

### 🔹 Bloco 11 — Execução 'do zero'
Inicialização completa do sistema.

### 🔹 Bloco 12 — Geração de Demos
Geração de JSONL limpo para avaliação.

### 🔹 Bloco 13 — Comparação Modelos Base vs Fine-Tuned
Comparação qualitativa antes/depois do ajuste.

---

## ⭐ Diferenciais

- Separação clara entre dados clínicos e geração de linguagem
- Zero alucinação em prontuários (EHR) - Dados determinísticos
- Fontes auditáveis
- Guardrails clínicos explícitos
- Arquitetura modular e reprodutível

---

## 🚀 Potenciais Melhorias

- Integração FHIR (Fast Healthcare Interoperability Resources)) real
- Avaliação quantitativa
- Interface web
- Dados 100% em Português, tanto do prontuário, quanto das bases de perguntas e respostas

---

## 📁 Estrutura de Diretórios

```
Tech_Challenge_3/
├── data/
│   ├── raw/
│   ├── processed/
│   └── synthetic/
├── models/
├── logs/
├── demos/
├── eval/
└── README.md
```

---

⚠️ Esse projeto é a saída principal do Tech Challenge 3 (propósito educacional). Não utilizar para decisões clínicas reais.