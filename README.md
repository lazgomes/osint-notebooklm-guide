# OSINT (Open Source Intelligence)
 
## 📌 1. Contexto e Objetivos
 
O assunto escolhido para este caderno temático é **Open Source Intelligence (OSINT)**, focado em sua aplicação para segurança cibernética, investigações e privacidade.
 
### Objetivos de Estudo:
 
▸ Compreender o Ciclo de Inteligência e a diferença entre dados brutos e inteligência analisada.
 
▸ Dominar a configuração de um ambiente seguro (OPSEC) utilizando Máquinas Virtuais e VPNs.
 
▸ Aprender técnicas de reconhecimento e busca avançada (Google Dorking) para identificar infraestruturas e pessoas.
 
▸ Explorar ferramentas de investigação de mídias sociais e metadados para geolocalização.
 
---
 
## 📚 2. Curadoria de Fontes
 
Durante o desenvolvimento deste caderno temático sobre OSINT, foram selecionadas fontes confiáveis e amplamente utilizadas na área de cibersegurança:
 
| # | Fonte | Link | Contribuição |
|---|---|---|---|
| 1 | **SANS Institute** | [Must-Have Free Resources for OSINT](https://www.sans.org/blog/-must-have-free-resources-for-open-source-intelligence-osint-) | Visão geral das principais ferramentas e recursos gratuitos utilizados em investigações OSINT |
| 2 | **IntelTechniques** | [inteltechniques.com](https://inteltechniques.com/index.html) | Plataforma prática com diversas ferramentas e técnicas utilizadas por profissionais de investigação |
| 3 | **Vídeo Educacional** | [YouTube](https://www.youtube.com/watch?v=taGkRbVuNf4) | Explicação visual e prática sobre conceitos de OSINT, facilitando o entendimento inicial |
| 4 | **OSINT Framework** | [osintframework.com](https://osintframework.com/) | Estrutura organizada de ferramentas OSINT categorizadas por tipo de coleta de informação |
 
---
 
## 🤖 3. Engenharia de Prompts e "Cicatrizes"
 
Durante a interação com a IA, foram testados diversos prompts para extrair informações específicas. Abaixo, documento a evolução das perguntas e as dificuldades encontradas.
> **Nota de Curadoria:** Decidi remover o HackTricks do escopo para evitar o desvio de finalidade (Pentest de Exploração) e manter o foco estrito em Inteligência de Fontes Abertas (OSINT).
---
 
### 🔎 Prompt 1 — Filtragem de Fontes
 
**Pergunta:**
> "Quais dessas fontes poderia excluir por não falar de OSINT?"
 
**Resposta obtida:**
A IA identificou que o HackTricks era mais voltado a pentest genérico do que OSINT puro, sugerindo sua substituição por fontes mais específicas.
 
**💀 Cicatriz:**
No início, as fontes escolhidas eram muito amplas, incluindo o HackTricks que era mais voltado a pentest genérico do que OSINT puro. Foi necessário removê-la e "limpar" o repositório para focar exclusivamente em inteligência de fontes abertas.
 
---
 
### 🔎 Prompt 2 — Definição e Arsenal Técnico

**Pergunta:**
> "Explique o que é OSINT com exemplos práticos usados em pentest e cite ferramentas comuns utilizadas por profissionais."

**Resposta obtida:**
A IA detalhou o papel do OSINT na fase de reconhecimento (passivo e físico), citando ferramentas como **Hunter.io**, **Epieos**, e **Jimpl**, além de destacar o uso de **Breach Data** para validar credenciais expostas.

**💀 Cicatriz:**
Este prompt foi essencial para sair da teoria e entender como o OSINT é aplicado no "mundo real". A IA inicialmente focou apenas em ferramentas web; precisei forçar a contextualização para Pentest para que ela trouxesse exemplos de reconhecimento físico e infraestrutura.

---

### 🔎 Prompt 3 — Aplicação Prática
 
**Pergunta:**
> "Simule um cenário real onde o Google Dorking seria usado em um pentest."
 
**Resposta obtida:**
A IA conectou a técnica de **Google Dorking** à descoberta de arquivos sensíveis e ao mapeamento de infraestrutura de alvos.
 
**📌 Referência:** Baseado nos módulos de busca avançada do [Learn OSINT Online](https://freeosint.github.io)
 
---
 
### 🔎 Prompt 4 — Troubleshooting de Erros
 
**Pergunta:**
> "Quais erros iniciantes cometem em OSINT?"
 
**Resposta obtida:**
 
A IA focou em falhas de **OPSEC**, como:
- Usar contas pessoais durante investigações
- Não validar as fontes coletadas
- Deixar rastros digitais no alvo

**💀 Dificuldade de Resposta:** A IA inicialmente misturou erros de estudo com erros de prática. Foi necessário reformular o prompt para separar dois contextos distintos:

- **Segurança do investigador** → OPSEC, anonimato, rastros digitais
- **Metodologia de análise** → validação de fontes, cruzamento de dados
---
 
## 📖 4. Miniguia de Estudo 
 
### 📋 Resumo Estruturado do Assunto
 
O OSINT é definido como a coleta e análise de informações de fontes públicas para gerar inteligência acionável. O processo não é aleatório — ele segue uma metodologia estruturada chamada **Ciclo de Inteligência**:
 
| Etapa | Nome | Descrição |
|---|---|---|
| 1️⃣ | **Definição de Objetivos** | Alinhamento com o cliente sobre o que deve ser descoberto |
| 2️⃣ | **Coleta de Dados** | Uso de ferramentas como OSINT Framework e motores de busca |
| 3️⃣ | **Verificação** | Cruzamento de dados para evitar informações falsas ou plantadas |
| 4️⃣ | **Análise** | Criação de cronogramas e gráficos de relacionamento (Link Analysis) |
| 5️⃣ | **Relatório** | Documentação clara das descobertas para fins técnicos ou executivos |
 
---
 
### 📝 Glossário de Principais Conceitos
 
| Termo | Definição |
|---|---|
| **OPSEC** | Práticas para proteger a identidade do investigador, como uso de VPNs e máquinas virtuais |
| **Sock Puppets** | Identidades falsas criadas para investigar sem alertar o alvo ou expor o perfil real |
| **Google Dorking** | Uso de operadores avançados (ex: `filetype:pdf`) para encontrar dados específicos indexados |
| **Metadados (EXIF)** | Dados embutidos em arquivos de imagem que podem conter data, hora e geolocalização |
| **Breach Data** | Informações de vazamentos de segurança usadas para validar perfis ou testar vulnerabilidades |
| **Virtual Machine (VM)** | Ambiente isolado (ex: CSI Linux) que protege o computador principal durante investigações |
 
---

### 🛠️ Arsenal de Ferramentas OSINT
 
Com base na curadoria e na interação com a IA, as seguintes ferramentas foram identificadas como essenciais para a prática:
 
| Categoria | Ferramenta | Aplicação Prática |
|---|---|---|
| **Investigação de E-mail** | Hunter.io / Epieos | Identificar padrões corporativos e perfis sociais vinculados. |
| **Geolocalização/Imagens** | Jimpl / PimEyes | Extração de metadados EXIF e reconhecimento facial. |
| **Pessoas e Usuários** | WhatsMyName / IntelTechniques | Rastreamento de nicknames em múltiplas plataformas. |
| **Infraestrutura** | Google Dorking / Shodan | Descoberta de servidores e arquivos sensíveis expostos. |
| **Ambiente Seguro** | CSI Linux / KeePass XC | Sistema operacional isolado e gestão de credenciais. |

---

### 🔁 Prompts Reutilizáveis para Revisão
 
> Utilize estes prompts para futuras consultas e revisões sobre o tema:
 
**Prompt 1 — Simulação Prática**
```
"Simule um cenário de investigação de um e-mail corporativo 
utilizando as ferramentas citadas nas fontes."
```
 
**Prompt 2 — Configuração de Ambiente**
```
"Quais são os passos exatos para configurar uma Máquina Virtual 
segura para OSINT segundo as fontes?"
```
 
**Prompt 3 — Google Dorking**
```
"Explique como o Google Dorking pode ser usado para encontrar 
currículos expostos e quais dados podem ser extraídos."
```
 
**Prompt 4 — Limitações Técnicas**
```
"Liste as limitações do uso de metadados EXIF em fotos 
vindas de redes sociais."
```
 
---

<p align="center">
  Desenvolvido durante o <b>Bootcamp Riachuelo - Cibersegurança</b> em parceria com a <a href="https://www.dio.me/">Digital Innovation One</a>.
</p>
