# Sistema de Gestão de Créditos
## Documento de Especificação Funcional

**Versão:** 1.0
**Data:** 08/06/2025
**Preparado por:** Product Owner

## Sumário Executivo

Este documento apresenta a especificação funcional do Sistema de Gestão de Créditos, uma solução desenvolvida para gerenciar o processo completo de aquisição e acompanhamento de créditos provenientes de processos judiciais, trabalhistas, precatórios e NPL (Non-Performing Loans). O sistema abrange desde a identificação inicial de oportunidades até o monitoramento contínuo dos créditos adquiridos, proporcionando uma plataforma integrada para maximizar o retorno dos investimentos com governança e controle.

## Visão Geral do Sistema

O Sistema de Gestão de Créditos é uma plataforma que permite o gerenciamento completo do ciclo de vida de créditos adquiridos, desde a identificação de oportunidades até o monitoramento e cobrança dos créditos comprados. O sistema é projetado para suportar o fluxo de trabalho específico de empresas que negociam a compra de direitos creditórios oriundos de processos judiciais.

## Fluxo de Processos


PRIMEIRO DIAGRAMA

### 1. Identificação de Oportunidades

### 2. Cadastro de Dados de cada crédito – base “Prospect”

#### 2.1. Integração com Tribunais em casos de ativos judiciais - Avaliar APIs como Esaj, PJe, e-SAJ, Projudi, etc. Ou pensarmos numa base já vindo enriquecida, e essas integrações virem de outros sistemas / fornecedores / APIs

### 3. Busca de dados dos Cedentes e/ou Advogados de cada crédito. Pensar como fazer.

### 4. Classificação da Oportunidade – Cadastro em cada “Carteira”ou “Portfolio”

### 5. Cálculos de Atualização Monetária - Definir índices padrão (ex: IPCA, CDI, SELIC, IGPM, TR etc.)

### 6. Cálculo dos Juros – Juros compõe o valor. Lembrar que a fórmula de atualização tem 2 componentes. Permitir cenários de simulação com diferentes datas base, juros compostos/simples e taxas personalizadas.

### 7. Precificação

#### 7.1. Módulo de cenários de precificação (com sensibilidade a taxa de recuperação e tempo estimado).
Oportunidade Viável?
Não – Arquivamento na base “Prospect”

### 8. Sim - Negociação com Cedente
Negociação Positiva?
Não – Alimenta informação na base “Prospect”

### 9. Sim - Recepção de Documentos via GED (definir Plataforma e maneira de upload – Google forms)

### 10. Análise Técnica – Due Dliligence

### 11. Geração de Relatório – Gravar no GED

### 12. Validação por Perito – Quando for o caso
Aprovado?
Não - Revisão/Ajustes

### 13. Sim - Arquivamento de todos os arquivos e relatorios no GED, com log

### 14. Informação positiva ao investidor / administrador para confirmação

### 15. Coleta de Dados para Pagamento – Pode ser já no formulário de coleta dos documentos inclusive

### 16. Gera carta com dados da cessão para validação

### 17. Emissão de Contrato -

### 18. Subir em plataforma de assinatura – Clicksign ou escolher plataforma SAFE WEB

### 19. Contrato assinado arquivar no GED

### 20. Gerar pagamento ao Cedente – Condicionar ao contrato assinado. Gerar Borderô para o ADM do FIDC

### 21. Atualização para Status COMPRADO – Marcar data da compra, valor pago e valor do crédito no dia da compra.

### 22. Integração ao Portfólio

SEGUNDO DIAGRAMA

## Fluxo de Gestão

### 1. Ter monitoramento automático de andamentos jurídicos e alertas de prazo – API c/ Legal ONE por exemplo

### 2. Cálculos

#### 2.1. Atualização de custo de capital por crédito

#### 2.2. Atualização da curva de cada crédito – Buscar ou dar sequência no cálculo do Onboarding – Segue a mesma curva

#### 2.3. Possibilidade de gerar relatórios de atualização com datas anteriores ou futuras. O input da data poderia ser pelo Power BI?

### 3. Base com acesso pelo Power BI

#### 3.1. Possibilidade de download dos relatórios e armazenamento em GED

#### 3.2. Download em .xls e .pdf

#### 3.3. Base sempre atualizada com Legal ONE na parte jurídica para gerar alertas – Campos a definir. Precisa linkar o Legal ONE ao nosso portfólio para que o Power BI tenha acesso?

### 4. Integração com ERP ou sistema contábil para escrituração e cobrança. Tendo a base de dados, acredito que seja fácil integrar.

Interação e Fluxo de Trabalho

### 1. Prospecção ativa – Publicar base do PBI para analistas ou Ferramentas automáticas com bases pré cadastradas

### 2. Prospecção passiva – Chat e Whatsapp.

### 3. Formulário de Onbording com o MÁXIMO de dados possível – GED. Prever múltiplos cedentes ou inventário.

### 4. GED sobe com lastro em CPF, mas tem que converter para lastro por crédito / processo – Gravar na base “Prospect”

### 5. Cadastro Cedente na base “CRM” – Acesso aos doctos pessoais do GED para futuro

### 6. Deste ponto em diante só com informações completas, senão segue o LOOP em busca de informações. Pensar num check list.

### 7. Calculos “preliminares” – Apresentação de mascara do PBI ao cliente/advogado, qdo for o caso

### 8. Cotação indicativa, sujeito a certidões e confirmação de informações preliminares.

### 9. Obtenção de Certidões – SERASA e outras bases. Cabe API?

### 10. Check list 0k? Gerar arquivo para terceiros (Ex GPA caso BTG - VASP) - planilha por Email ou link para acesso?

### 11. Tudo aprovado? Segue para item 14 do “Fluxo Processo” acima

### 12. Coleta de Dados para Pagamento – Pode ser já no formulário de coleta dos documentos inclusive

### 13. Gera carta com dados da cessão para validação

### 14. Emissão de Contrato -

### 15. Subir em plataforma de assinatura – Clicksign ou escolher plataforma

### 16. Contrato assinado arquivar no GED

### 17. Gerar pagamento ao Cedente – Condicionar ao contrato assinado. Gerar Borderô para o ADM do FIDC

### 18. Sistema "Precatórios" do BTG – Exemplo de sistema de ctas a pagar que alguns administradores usam. Tem GED próprio. Pensar se teria como alimentar sem ser manual. Se justificar...

### 19. Tentar ter a confirmação do pagamento para atualizar status do item 21 do “FLUXO PROCESSO”. Se for manual, precisa ter uma entrada para marcar como “ok”.
 
 
## Requisitos Funcionais
 
### 1. Gestão de Oportunidades

#### 1.1. Identificação e Cadastro de Oportunidades
- **Descrição:** O sistema deve permitir o cadastro de novas oportunidades de crédito provenientes de diversas fontes.
- **Dados a serem registrados:**
• Número do processo
• Tipo de processo
• Valor inicial
• Multiplos cedentes? Inventário?
• Data de distribuição
• CPF e nome do cedente
• Informações adicionais relevantes
 
#### 1.2. Classificação de Oportunidades
- **Descrição:** O sistema deve permitir a classificação das oportunidades para definir a trilha de análise e riscos associados.
 - **Categorias de classificação:**
• NPL (Non-Performing Loans)
• Precatórios
• Processos Trabalhistas
• Processos Cíveis
• Outros tipos conforme necessidade – Pode deixar previsto um administrador criar?
 
#### 1.3. Cálculos de Atualização Monetária
- **Descrição:** O sistema deve possibilitar a realização de cálculos para determinar o valor atual do processo.
 
- **Funcionalidades:**
• Aplicação de cálculos a definir – Infos no “Fluxo Processo” itens  5 e 6
 
#### 1.4 Negociação com Cedentes
- **Descrição:** A negociação com cedentes deve ser feita diretamente pelo cliente, sem interação do sistema. Pode ser via chat ou Whatsapp sobre a intenção de ceder. Depois cedente sobe os documentos, e depois vai a cotação preliminar.
 
#### 2. Gestão Documental

#### 2.1. Recepção e Armazenamento de Documentos
 
- **Descrição:** O sistema deve permitir o recebimento e armazenamento de documentos necessários para a análise e emissão de contrato.
 
- **Funcionalidades:**
• Integração com sistema/serviço cloud de terceiros para armazenamento
• Categorização de documentos
• Controle de versões
• Checklist de documentos necessários (a definir)
 
#### 2.2. Análise Documental e Processual
- **Descrição:** O sistema deve suportar o processo de análise técnica dos documentos e do processo.
 
- **Funcionalidades:**
• Registro de análises realizadas
• Avaliação de riscos
• Análise de garantias
• Determinação de recuperabilidade
• Definição de preço-alvo
 
#### 2.3. Geração de Relatórios
- **Descrição:** O sistema deve permitir a geração de relatórios com informações do processo e valores para envio ao perito.
 
- **Funcionalidades:**
• Modelos personalizáveis de relatórios – Power BI
• Exportação em diferentes formatos (PDF, Excel)
 
#### 2.4. Gestão de Pareceres Técnicos
- **Descrição:** O sistema deve permitir o registro e acompanhamento de pareceres técnicos emitidos por peritos.
 
- **Funcionalidades:**
• Cadastro de peritos (internos e externos)
• Registro de pareceres
• Tudo via documentos armazenados no sistema
 
### 5. Gestão de Contratos

### 5.1. Emissão de Contratos de Cessão
- **Descrição:** O sistema deve suportar a geração de contratos de cessão de créditos.
 
- **Funcionalidades:**
• Modelos de contratos personalizáveis
• Preenchimento automático com dados do processo
• Versionamento de contratos
 
#### 5.2. Assinatura Digital
- **Descrição:** O sistema armazenará os contratos assinados digitalmente por todas as partes envolvidas.
- **Funcionalidades:**
• O Máximo de interação possível nas ferramentas
• Armazenamento seguro em serviço cloud de terceiros
 
### 5.3. Coleta de Dados para Pagamento
- **Descrição:** O sistema deve permitir a coleta e armazenamento dos dados bancários e informações necessárias para efetuar o pagamento ao cedente.
 
- **Funcionalidades:**
• Cadastro de dados bancários do cedente
• Registro de informações fiscais necessárias (se necessário)
• Armazenamento seguro das informações financeiras
 
#### 5.4. Atualização de Status
- **Descrição:** O sistema deve permitir a atualização do status da oportunidade para COMPRADO (a definir) após a finalização do processo de aquisição.
- **Funcionalidades:**
• Workflow de aprovação
• Registro de data efetiva da compra
• Notificações automáticas
 
### 6. Gestão de Créditos Adquiridos

#### 6.1. Acompanhamento Processual
- **Descrição:** O sistema deve permitir o acompanhamento processual dos créditos adquiridos.
 
- **Funcionalidades:**
• Registro de movimentações processuais – Talvez seja melhor usar o Legal One
• Alertas de prazos
• Integração com sistemas de tribunais (quando disponível)
 
#### 6.2. Auditoria
- **Descrição:** O sistema deve suportar processos de auditoria dos créditos adquiridos.
 
- **Funcionalidades:**
• Registro de informações pertinentes a auditoria (usuários, data, ações, etc)
 
#### 6.3. Monitoramento
- **Descrição:** O sistema deve permitir o monitoramento contínuo dos créditos adquiridos.
 
- **Funcionalidades:**
• Dashboards
• Alertas
• Relatórios
• Usar Power BI

## Requisitos Não-Funcionais

### 1. Segurança
• Autenticação de usuários
• Registro de logs de auditoria
• Conformidade com LGPD

### 2. Usabilidade
• Interface intuitiva e responsiva
• Tempos de resposta adequados

### 3. Disponibilidade
• Disponibilidade 24/7 com manutenções programadas

### 4. Escalabilidade
• Capacidade de crescimento conforme aumento da base de dados

### 5. Integrações
• APIs para integração com sistemas externos
• Integração com serviços cloud para armazenamento de documentos

## Próximos Passos
 
1. Validação do documento com stakeholders
2. Detalhamento de requisitos específicos
3. Priorização de funcionalidades
4. Elaboração de cronograma