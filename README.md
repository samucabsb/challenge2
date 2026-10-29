]# 🏥 SUS Cidadão (NavegaSUS)
> **Apoio Inteligente à Tomada de Decisão para Acesso Gratuito a Medicamentos e Exames no SUS**  
> *Challenge 2: Qualidade de Vida e Tomada de Decisão com IA* — **Instituto Eldorado | Residência em Inteligência Artificial (UnB / Softex)**
---
## 🎯 Sobre o Projeto
Milhões de famílias brasileiras comprometem parte expressiva de sua renda adquirindo medicamentos de uso contínuo no varejo privado por puro desconhecimento das regras públicas de gratuidade. 
O **SUS Cidadão** é uma solução de Inteligência Artificial desenhada para empoderar o paciente da rede pública e seus cuidadores familiares. A partir do envio de uma **receita médica digital (PDF)**, **foto do receituário** ou **mensagem de voz**, o sistema decodifica os itens prescritos e audita as regras oficiais do Ministério da Saúde e do Distrito Federal, entregando um roteiro prático e auditável:
1. **Onde retirar gratuitamente:** Diferenciação automática entre *Farmácia Popular* (drogaria privada com CPF), *Unidade Básica de Saúde - UBS* (Atenção Primária) e *Farmácia de Alto Custo* (Componente Especializado via processo LME).
2. **Checklist Documental e SISREG:** Documentos obrigatórios e critérios de regulação para consultas e exames especializados.
3. **Guardrail Ético Inegociável:** Atuação estritamente restrita à **navegação administrativa e cidadã**, sem realizar prescrição clínica, diagnóstico ou troca de remédios.
---
## 🏗️ Arquitetura Técnica & Roadmap (7 Semanas)

  

[ Usuário ] ──> (PDF / Imagem / Áudio)
│
▼
[ Pipeline Multimodal ]  ──>  Desidentificação LGPD (PII Masking)
│
▼
[ Orquestrador Multiagentes ]
├── 1. Agente Extrator & Triador Multimodal
├── 2. Agente Auditor Farmacêutico (RAG: RENAME 2024 + Farmácia Popular + REME-DF)
├── 3. Agente Consultor SISREG / SES-DF (RAG: Protocolos CPPAS)
└── 4. Agente Sintetizador do Roteiro Cidadão
│
▼
[ Painel de Apoio à Decisão & Gestão da Receita ]


  
* **Semana 1 (Atual):** Definição do Problema, Personas, Stakeholders, Riscos e Métricas (PDR ABNT).
* **Semana 2:** Base de Conhecimento e Recuperação (RAG Híbrido: CSV tabular + Chunks vetoriais de portarias).
* **Semana 3:** Avaliação Experimental Científica (LLM pura vs. RAG com framework RAGAS).
* **Semana 4:** Sistema Multiagentes Colaborativo (LangGraph / CrewAI).
* **Semana 5:** Pipeline Multimodal (PDFs digitais padrão CFM/ICP-Brasil + OCR + Transcrição Whisper).
* **Semana 6:** Integração Sistêmica Ponta a Ponta (API FastAPI + Interface).
* **Semana 7:** Bateria de Testes com Usuários, Métricas DCS e Demonstração Final.
---
## 📚 Bases de Dados Oficiais (100% Públicas)
* **RENAME 2024:** Relação Nacional de Medicamentos Essenciais (Portaria GM/MS nº 6.324/2024).
* **Programa Farmácia Popular do Brasil:** Elenco oficial de gratuidade expandida do Ministério da Saúde.
* **REME-DF:** Relação de Medicamentos do Distrito Federal (SES-DF).
* **SISREG III / CPPAS:** Protocolos de Encaminhamento e Regulação Ambulatorial da SES-DF e Ministério da Saúde.
---
## 👥 Squad MLOps / LLMOps
| Papel | Responsável |
| :--- | :--- |
| **Product Owner (PO)** | Samuel de Souza Rodrigues |
| **Arquiteto de Software** | Mickeias Charles de Oliveira Paiva |
| **Cientista de Dados** | Marlon Dias Marques |
| **Engenheira de Dados** | Jhiovana Silva Ribeiro |
| **MLOps / LLMOps** | Tayrine Hevellin Zitkoski |
---
## 📁 Documentação da Semana 1
* O **Documento de Definição de Produto e Requisitos (PDR)** oficial e completo da Semana 1 encontra-se na pasta [`docs/pdr_sus_cidadao_semana1.txt`](./docs/pdr_sus_cidadao_semana1.txt).
