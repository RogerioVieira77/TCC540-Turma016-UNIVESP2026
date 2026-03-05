# Sistema Inteligente Antifraude para Mitigação de Golpes Telefônicos Relacionados ao PIX em Smartphones

Trabalho de Conclusão de Curso em Engenharia de Computação - TCC540 - Turma 016 - Tcc

## Sumário

1 INTRODUÇÃO

1.1 Contextualização
1.2 Problema de Pesquisa
1.3 Hipótese
1.4 Objetivo Geral
1.5 Objetivos Específicos
1.6 Metodologia
1.7 Estrutura do Trabalho

2 FUNDAMENTAÇÃO TEÓRICA

2.1 Segurança da Informação
2.2 Engenharia Social
2.3 Sistema PIX e Vulnerabilidades
2.4 Machine Learning aplicado à Segurança
2.5 Sistemas Antifraude
2.6 Classificação e Modelos Preditivos
2.7 Aspectos Legais – LGPD

3 ANÁLISE DO PROBLEMA

3.1 Panorama das Fraudes no Brasil
3.2 Fraudes Relacionadas ao PIX
3.3 Impactos Econômicos
3.4 Limitações dos Sistemas Atuais

3.5 Justificativa Técnica

- Golpes exploram vulnerabilidade humana
- Sistemas antifraude atuais são reativos
- Bancos atuam após o dano financeiro
- Não existe interceptação inteligente pré-transação

3.6 Justificativa Social

- População idosa é altamente vulnerável
- Baixa alfabetização digital
- Crescente número de fraudes no Brasil

3.7 Justificativa Econômica

- Redução de perdas financeiras
- Diminuição de judicializações
- Redução de custos bancários

4 PROPOSTA DE SOLUÇÃO

5 DETALHAMENTO TÉCNICO

5.1 Visão Geral do Sistema
5.2 Tecnologias de IA
5.3 Arquitetura em Camadas
5.4 Modelo de Inteligência Artificial
5.5 Modelo Matemático de Scoring
5.6 Estratégia de Implementação
5.7 Segurança e Conformidade
5.8 Stack Tecnológica Recomendada
5.9 Implementação (Fases)

6 VIABILIDADE TÉCNICA E ECONÔMICA

6.1 Infraestrutura Necessária
6.2 Custos Estimados
6.3 Modelo de Negócio
6.4 Simulação de ROI

7 RESULTADOS ESPERADOS

7.1 Indicadores

8 CONCLUSÃO
8.1 Considerações
8.2 Riscos e Desafios

## 1. INTRODUÇÃO

1.1 Contextualização

O Brasil é um dos países com maior adoção do sistema de pagamentos instantâneos Banco Central do Brasil — o Pix — que revolucionou o sistema financeiro.

Entretanto, o crescimento do PIX trouxe aumento significativo de:

- Golpes via ligação telefônica
- Engenharia social
- Falsificação de identidade
- Fraudes com transferências induzidas
- Roubo de dados pessoais

Segundo relatórios da FEBRABAN, a maior parte das fraudes ocorre por engenharia social, não por falhas técnicas do sistema PIX.

1.2 Problema de Pesquisa

Como a Inteligência Artificial aplicada à Segurança da Informação pode reduzir fraudes telefônicas relacionadas ao uso do PIX em smartphones no Brasil?

1.3 Hipótese

1.4 Objetivo Geral

Desenvolver um modelo conceitual de um Sistema Inteligente Antifraude para Smartphones, capaz de:

- Interceptar ligações suspeitas
- Analisar padrões de fraude
- Classificar risco em tempo real
- Alertar o usuário antes que a engenharia social evolua

1.5 Objetivos Específicos
1.6 Metodologia
1.7 Estrutura do Trabalho

## 2 - FUNDAMENTAÇÃO TEÓRICA

2.1 Segurança da Informação

A Segurança da Informação baseia-se no tripé:

- Confidencialidade
- Integridade
- Disponibilidade

No contexto financeiro digital, adicionam-se:

- Autenticidade
- Não repúdio

2.2 Engenharia Social

Segundo Mitnick, engenharia social explora vulnerabilidades humanas, não tecnológicas.

Principais vetores:

- Falsa central bancária
- Golpe do falso funcionário
- Falso sequestro
- Clonagem de WhatsApp

A falha ocorre antes da transação — no convencimento.

2.3 Sistema PIX e Vulnerabilidades
A massificação do Pix, desenvolvido pelo Banco Central do Brasil, ampliou a superfície de ataque baseada em engenharia social.

2.3 Machine Learning Aplicado à Segurança

Machine Learning permite:

- Identificação de padrões anômalos
- Classificação preditiva
- Análise comportamental

Técnicas aplicáveis:

- Random Forest
- Gradient Boosting
- Redes Neurais MLP
- Detecção de Anomalias

2.4 Sistemas Antifraude Modernos

Empresas como:

- ClearSale
- Serasa Experian

Utilizam modelos preditivos para transações, mas não atuam preventivamente em chamadas telefônicas.

2.5 Sistemas Antifraude

2.6 Classificação e Modelos Preditivos

2.6.1 Classificação (Scouring)

Vamos propor um modelo formal:

Definimos:

- x1 = Frequência de chamadas
- x2 = Número denunciado (binário)
- x3 = Horário incomum
- x4 = Padrão de repetição
- x5 = Score coletivo

Modelo Logístico:

$$\frac{1}{P(Fraude)=1+e−(β0​+β1​x1​+β2​x2​+...+β5​x5​)1​}$$

Classificação:

- P < 0.30 → Seguro
- 0.30 ≤ P < 0.70 → Suspeito
- P ≥ 0.70 → Alto Risco

🔎 Modelo Alternativo (Ensemble)

Score Final =

$$Score=0.4(RandomForest)+0.3(XGBoost)+0.3(MLP)$$

2.7 Aspectos Legais – LGPD

## 3 - ANÁLISE DO PROBLEMA

3.1 Panorama das Fraudes no Brasil
3.2 Fraudes Relacionadas ao PIX
3.3 Impactos Econômicos
3.4 Limitações dos Sistemas Atuais

## 4 - PROPOSTA DE SOLUÇÃO

4.1 Proposta: Criar um Sistema de Interceptação Inteligente de Chamadas (SIIC) que utilize:

## 5 - DETALHAMENTO TÉCNICO

5.1 Visão Geral do Sistema

- Recebimento da ligação
- Sistema analisa número, metadata e padrões
- IA calcula score de risco
- Interface alerta o usuário:
  - Seguro
  - Suspeito
  - Alto Risco (Possível golpe)

5.2 Tecnologias de IA

- Machine Learning
- Análise comportamental
- Reconhecimento de padrões
- Classificação de risco
- Banco de dados de números suspeitos

5.3 Arquitetura Conceitual - Arquitetura em Camadas

5.3.1 Camadas do Sistema:

- Camada Cliente (Mobile)
- Aplicativo Android / iOS
- Permissões de acesso a chamadas
- Interface de alerta

5.3.2 Camada de Inteligência:

- Modelo de Machine Learning
- Classificador supervisionado
- Análise de padrões temporais

5.3.3 Camada de Dados

- Base de números denunciados
- Base colaborativa
- Integração com APIs públicas

5.3.4 Visão Conceitual

[ Smartphone ]
       ↓
[ Camada de Interceptação ]
       ↓
[ Motor de IA ]
       ↓
[ API Backend ]
       ↓
[ Banco de Dados + Inteligência Colaborativa ]

Camada 1 – Dispositivo (Mobile)

- Captura metadados da chamada
- Identificação de número
- Histórico local
- Android → Kotlin
- iOS → Swift + CallKit

Camada 2 – Motor de Classificação

Modelo treinado com:

- Variáveis:
  - Frequência de chamadas
  - Horário
- Reputação
- Duração média
- Score coletivo

Camada 3 – Backend

- API REST (FastAPI)
- Banco PostgreSQL
- Redis para cache
- Docker + Kubernetes

Camada 3 – Backend

5.4 Modelo de Inteligência Artificial

5.4.1 Modelo de Machine Learning

Tipo de problema:

- Classificação binária (Fraude / Não fraude)

Features possíveis:

- Número já denunciado
- Origem geográfica
- Frequência de ligações
- Horário incomum
- Duração média
- Padrão de repetição
- Histórico de denúncias

5.4.1 Técnicas de IA Aplicáveis

- Random Forest
- Gradient Boosting
- Rede Neural MLP
- Análise de grafos (rede de números interconectados)
- NLP (caso haja análise de fala futura)

5.4.2 Possível Evolução (Nível Avançado)

- Análise de voz em tempo real
- Detecção de scripts de golpe
- Modelos de LLM embarcados
- Aprendizado federado (Federated Learning)
- Sistema colaborativo entre usuários

5.5 Modelo Matemático de Scoring
5.6 Estratégia de Implementação
5.7 Segurança e Conformidade

5.8 Stack Tecnológica Recomendada

### Mobile

- Android: Kotlin + Android SDK
- iOS: Swift + CallKit
- Inteligência Artificial

### Python

- TensorFlow / PyTorch
- Scikit-Learn
- XGBoost

### Backend

- FastAPI (Python)
- Banco PostgreSQL
- Redis (cache)
- Docker

### Segurança

- Criptografia AES-256
- TLS 1.3
- Hash SHA-256
- LGPD compliance

5.9 - Implementação (Fases)

### Fase 1 – Prova de Conceito

- Dataset público de números fraudulentos
- Simulação de chamadas
- Treinamento offline

### Fase 2 – Protótipo Funcional

- App Android
- Classificação via API
- Score de risco

### Fase 3 – Escalabilidade

- Cloud (AWS / Azure / GCP)
- Microserviços
- Pipeline MLOps

## 6 VIABILIDADE TÉCNICA E ECONÔMICA

6.1 Infraestrutura Necessária
6.2 Custos Estimados

6.3 Modelo de Negócio

6.3.1 Modelo: B2B2C

- Venda para bancos
- Venda para operadoras
- Assinatura premium
- API antifraude para fintechs
- Diferencial Estratégico

6.3.2 Integração futura com:

- Banco Central do Brasil
- Serasa Experian
- ClearSale

6.4 Simulação de ROI

Premissas:

- 1 milhão de usuários
- Taxa de fraude anual: 2%
- Ticket médio fraude PIX: R$ 2.500
- Redução esperada com sistema: 35%

Cálculo:

- Usuários afetados: 20.000
- Prejuízo total: R$ 50 milhões
- Redução de 35%: Economia anual = R$ 17,5 milhões

Custo estimado anual sistema:

- Infraestrutura + IA + equipe: ≈ R$ 4 milhões

ROI:

$$ROI=\frac{17.5−4}{4} =3.37$$

Retorno de 337% ao ano.

## 7 RESULTADOS ESPERADOS

## 8 CONCLUSÃO

## DICAS GERAIS

### PADRÃO ABNT

### ELEMENTOS PRÉ-TEXTUAIS

- Capa
- Folha de rosto
- Folha de aprovação
- Dedicatória (opcional)
- Agradecimentos (opcional)
- Epígrafe (opcional)
- Resumo
- Abstract
- Lista de Figuras
- Lista de Tabelas
- Lista de Abreviaturas e Siglas

### EXTRAS - IDEIAS ADICIONAIS

- Propor framework nacional antifraude colaborativo
- Simular impacto estatístico
- Criar modelo matemático de risco
- Apresentar arquitetura em diagrama UML
- Criar fluxo de segurança LGPD detalhado

A aplicação de IA na interceptação preventiva de ligações fraudulentas representa:

- Evolução da Segurança da Informação
- Mudança de modelo reativo → preditivo
- Proteção financeira preventiva
- Inovação aplicada ao ecossistema PIX

### MODELO DE APRESENTAÇÃO ESTILO BANCA

- Slide 1 – Problema
  - Explosão de fraudes PIX via engenharia social
- Slide 2 – Impacto
  - Bilhões em prejuízo no Brasil
- Slide 3 – Falha Atual
  - Sistemas atuam após transação
- Slide 4 – Proposta
  - Interceptação Inteligente de Chamadas
- Slide 5 – Arquitetura
- Slide 6 – Modelo Matemático
- Slide 7 – Simulação Econômica
- Slide 8 – Viabilidade Técnica
- Slide 9 – Contribuição Acadêmica
- Slide 10 – Conclusão
