# Plano de Cutover

&emsp;&emsp;O plano de *Cutover* é um documento detalhado que orienta a transição de um sistema antigo para um novo, particularmente durante a implementação de soluções de ERP, como SAP. Ele inclui uma série de tarefas, cronogramas, recursos necessários e procedimentos que devem ser seguidos durante essa transição crítica. [(Sabino, 2024)](https://radardeprojetos.com.br/plano-de-cutover-o-segredo-para-uma-transicao-de-projetos-bem-sucedida/#:~:text=Um%20Plano%20de%20Cutover%20%C3%A9,seguidos%20durante%20essa%20transi%C3%A7%C3%A3o%20cr%C3%ADtica.)

&emsp;&emsp;Um plano de Cutover comum inclui atividades como:

1. **Preparação dos Dados**: Extração, limpeza e carregamento dos dados do sistema antigo para o novo.
2. **Testes Finais**: Execução de testes de aceitação do usuário (UAT) para garantir que tudo funcione corretamente.
3. **Treinamento**: Garantir que todos os usuários finais estejam familiarizados com o novo sistema.
4. **Cronograma Detalhado**: Definição de prazos e momentos exatos de cada etapa do plano.
5. **Planos de Contingência**: Procedimentos de recuperação em caso de falhas ou imprevistos.

Além de servir como um guia para a equipe técnica, o plano também envolve todas as partes interessadas, como o time de negócios, garantindo que todos estejam cientes de suas responsabilidades e de como responder a eventuais desafios.

<br>

## 1. Testes Unitários

&emsp;&emsp;Testes unitários são uma parte fundamental do processo de desenvolvimento de software, especialmente em projetos de implementação de ERP. Eles garantem que pequenas unidades do sistema, como funções ou módulos, funcionem conforme o esperado de forma isolada. 

&emsp;&emsp;Ao analisar funcionalidades específicas de forma independente, as organizações podem identificar e corrigir problemas em um nível granular antes que os componentes sejam integrados, minimizando o risco de falhas quando o sistema é implementado no ambiente de produção. [(Medium, 2023)](https://medium.com/1erp/testing-your-new-erp-system-bd4faa3d26fd)


## Objetivo

&emsp;&emsp;O propósito desta seção é oferecer uma descrição detalhada e sistemática de todos os processos relacionados às operações de compras no SAP Business One. Isso inclui a maneira como as solicitações de compras são feitas, como as notas fiscais de entrada são criadas e gerenciadas, e como os relatórios de compras são compilados e analisados para garantir eficiência e conformidade nas operações comerciais.


## Escopo

&emsp;&emsp;O escopo deste documento cobre todas as regras de negócio associadas ao módulo de compras, detalhando cada processo, seus requisitos, e os procedimentos de teste associados. O objetivo é assegurar que todos os aspectos das compras sejam compreendidos e seguidos corretamente, minimizando erros e maximizando a eficiência.

### Solicitação de Compra, Oferta de Compra
- **Módulo:** Compras → Solicitação de Compras

- **Objetivo:** Selecionar fornecedor e itens, especificar detalhes para adição.
- **Campos Obrigatórios:** Datas (Lançamento, Validade, Necessária), Solicitante, Filial G2, Conteúdo do item.
- **Condições de Teste:** 
  - **Pré-requisito:** Adição de Solicitação e Ofertas de Compras.
  - **Resultado Esperado:** Teste sem erro de adição ou atualização.
  - **Data de Teste:** 11/09/2024 às 11:07
  - **Responsável:** Otto Lima
  - **Status:** OK

### Criar Pedido de Compra
- **Módulo:** Compras → Pedido de Compras

- **Objetivo:** Gerar pedidos de reembolso, especificando fornecedor, funcionário, datas, e detalhes financeiros.
- **Campos Obrigatórios:** Fornecedor, Funcionário, Datas de Lançamento, Pedido, Quantidade, Preço Unitário.
- **Resultado Esperado:** Teste sem erro de adição ou atualização.
- **Data de Teste:** 11/09/2024 às 11:10
- **Responsável:** Otto Lima
- **Status:** OK

### Criar Nota Fiscal de Entrada
- **Módulo:** Compras → Pedido de Compras → Nota Fiscal de Entrada

- **Objetivo:** Registrar entradas fiscais, utilizando informações de pedidos existentes.
- **Campos Obrigatórios:** Uso e Código de Imposto, Condições de Pagamento, Número da Nota Fiscal.
- **Resultado Esperado:** Teste sem erro de adição ou atualização.
- **Data de Teste:** 11/09/2024 às 11:12
- **Responsável:** Otto Lima
- **Status:** OK

### Devolução da Nota Fiscal de Entrada
- **Processo:** Utilize a opção 'Copiar para' para criar uma devolução da Nota Fiscal de Entrada a partir da nota original.

- **Resultado Esperado:** Teste sem erro de adição ou atualização.
- **Data de Teste:** 11/09/2024 às 11:14
- **Responsável:** Otto Lima
- **Status:** OK

### Recebimento de Mercadoria
- **Módulo:** Compras → Pedido de Compras

- **Objetivo:** Adicionar recebimento de mercadoria com base em pedido de compra.
- **Campos Obrigatórios:** Item, se é de estoque, preço.
- **Resultado Esperado:** Teste sem erro de adição ou atualização.
- **Data de Teste:** 11/09/2024 às 11:18
- **Responsável:** Otto Lima
- **Status:** OK
- **Observações:** Importante verificar o depósito físico onde está sendo dado entrada no pedido de compra.

### Processo de Adiantamento

- **Módulo:** Compras

- **Objetivo:** Gerar um pedido de compras e então copiar para adiantamento para fornecedor, especificando o percentual do valor do adiantamento.
- **Resultado Esperado:** Teste sem erro de adição ou atualização.
- **Data de Teste:** 11/09/2024 às 11:21
- **Responsável:** Otto Lima
- **Status:** OK

### Relatórios de Compras
- **Módulo:** Compras → Relatório de Compras

- **Objetivo:** Executar os relatórios de compras, listando itens em aberto e vencimentos do contas a pagar.
- **Resultado Esperado:** "Relatórios do SAP - Lista de itens em aberto e vencimentos do contas a pagar."
- **Data de Teste:** 11/09/2024 às 11:23
- **Responsável:** Otto Lima
- **Status:** OK

### Checar Estoque de Licenças
- **Módulo:** Estoque → Relatórios de Estoque

- **Objetivo:** Verificar o estoque de licenças para evitar compras desnecessárias.
- **Resultado Esperado:** Não realizar compra caso haja licenças no estoque.
- **Data de Teste:** 11/09/2024 às 11:25
- **Responsável:** Otto Lima
- **Status:** OK

### Pedido de Reposição de Produtos Internos
- **Módulo:** Compras → Transações Recorrentes → Modelos

- **Objetivo:** Criar e manter pedidos de compra recorrentes para reposição interna.
- **Resultado Esperado:** Compra realizada ou travada + consultar FNXXX
- **Data de Teste:** 11/09/2024 às 11:26
- **Responsável:** Otto Lima
- **Status:** OK

### Resultado

&emsp;&emsp;Os testes realizados nas diversas regras de negócio do módulo de compras demonstraram que o sistema está apto a executar todas as funções conforme esperado, com poucas exceções. Todos os resultados esperados foram alcançados com sucesso, indicando que o sistema está configurado corretamente para suportar as operações de compras da organização.

### Conclusão 

&emsp;&emsp;A implementação e teste das regras de negócio no módulo de compras do SAP Business One revelam um sistema robusto, capaz de gerenciar eficientemente todas as operações relacionadas a compras. Este documento serviu para verificar e validar os processos, assegurando que os procedimentos estão alinhados com os padrões organizacionais e regulatórios. Continuaremos a monitorar e revisar os processos para garantir que permaneçam eficazes e eficientes.

# 2. Matriz Raci

&emsp;&emsp;A Matriz RACI é uma ferramenta de gestão de projetos que facilita a atribuição de responsabilidades entre os membros da equipe. Cada letra no termo "RACI" representa um tipo de papel desempenhado pelos participantes:

- **R** (Responsável): O responsável por executar a tarefa.
- **A** (Aprovador): A pessoa que deve aprovar o trabalho antes que ele seja considerado concluído.
- **C** (Consultado): Aqueles que fornecem informações ou consultoria sobre a tarefa.
- **I** (Informado): Aqueles que são informados sobre o andamento e o resultado da tarefa.

&emsp;&emsp;Ao dividir as tarefas entre os membros do grupo, a Matriz RACI ajuda a garantir clareza nas responsabilidades, evitando confusões e garantindo que todas as atividades sejam bem geridas.

| **Tarefas**                                | **Responsável (R)** | **Aprovador (A)**  | **Consultado (C)**   | **Informado (I)**   |
|--------------------------------------------|---------------------|--------------------|----------------------|---------------------|
| Testes Unitários                           | Otto Coutinho        | Henrique Cox        | Walquiria Novaes      | Keylla Oliveira     |
| Anotação dos Testes Unitários              | Keylla Oliveira      | Luiza Santana       | Walquiria Novaes      | Otto Coutinho       |
| Documentação dos Testes Unitários          | Luiza Santana        | Keylla Oliveira     | Walquiria Novaes      | João Brandão        |
| Passo a Passo dos Testes Unitários         | João Brandão         | Daniel Zular        | Walquiria Novaes      | Henrique Cox        |
| Análise Financeira - Custos para o projeto | Daniel Zular         | Keylla Oliveira     | Eduarda Santos        | Henrique Cox        |
| Análise Financeira - Custos operação (1 ano)| Henrique Cox        | Otto Coutinho       | Eduarda Santos        | Daniel Zular        |
| Análise Financeira - Receitas previstas    | João Brandão         | Daniel Zular        | Eduarda Santos        | Keylla Oliveira     |
| Análise Financeira - Tendências de Mercado | Luiza Santana        | Henrique Cox        | Eduarda Santos        | Daniel Zular        |
| Análise Financeira - ROI                   | Luiza Santana        | Keylla Oliveira     | Eduarda Santos        | Otto Coutinho       |
| Análise Financeira - Modelagem Sensibilidade| Otto Coutinho       | Keylla Oliveira     | Eduarda Santos        | Henrique Cox        |
| Passo a Passo - Treinamento                | Daniel Zular         | Henrique Cox        | Walquiria Novaes      | Keylla Oliveira     |
| Manual elaborado - Treinamento             | João Brandão         | Keylla Oliveira     | Walquiria Novaes      | Daniel Zular        |
| Lista de presença - Treinamento            | João Brandão         | Keylla Oliveira     | Walquiria Novaes      | Luiza Santana       |
| Revisão das Referências                    | Henrique Cox         | Henrique Cox        | Não aplicável         | Keylla Oliveira     |
| Revisão Critérios EP - Negócios            | Keylla Oliveira      | Keylla Oliveira     | Rafael Ricardo Jacomossi         | Henrique Cox        |
| Revisão Critérios EP - UX                  | Luiza Santana        | Luiza Santana       | Júlia Stateri         | Keylla Oliveira     |
| Revisão Geral da Sprint                    | Luiza Santana        | Luiza Santana       | Renato Penha          | Keylla Oliveira     |
| Matriz Raci                                | Henrique Cox         | Keylla Oliveira     | Afonso Brandão        | João Brandão        |
| Slides - Conteúdo                          | Henrique Cox         | Keylla Oliveira     | Renato Penha          | Otto Coutinho       |
| Apresentação                               | Henrique Cox, Keylla Oliveira | Renato Penha | Renato Penha         | Daniel Zular        |

&emsp;&emsp;A Matriz RACI é essencial para uma gestão eficiente das atividades em equipe, permitindo que cada membro saiba seu papel exato em cada tarefa. Atribuindo as responsabilidades de forma clara, ela ajuda a manter o foco no que é necessário para o sucesso do projeto, minimizando confusões e atrasos.

<br>

# 3. Estratégia de Cutover

&emsp;&emsp;A estratégia de Cutover é uma fase crítica no processo de implantação de sistemas. Ela envolve a transição final entre o sistema antigo e o novo, garantindo que todos os dados, funcionalidades e operações estejam preparados para o uso em ambiente de produção. Deve ser meticulosamente planejada e executada para minimizar riscos e garantir uma migração suave e sem interrupções nas operações diárias.

&emsp;&emsp;Esse planejamento inclui uma série de atividades coordenadas, como a conversão de dados, testes finais, treinamento de usuários, verificação de integrações e processos de backup. 

&emsp;&emsp;Uma boa estratégia de Cutover considera tanto a preparação técnica quanto a comunicação eficaz com todas as partes envolvidas, garantindo que todos saibam suas responsabilidades. [(SAP, 2024)](https://community.sap.com/t5/enterprise-resource-planning-blogs-by-sap/sap-project-manager-s-guide-to-sap-project-cutover/ba-p/13510809)


## Checklist Go Live

### Verificação de Backup
- [x] Confirmar que os backups foram configurados e testados adequadamente.
- [x] Realizar um teste de restauração para garantir a integridade do backup.

### Ações para Go Live
- [x] Realizar backup completo do sistema atual.
- [x] Implementar congelamento de mudanças no sistema legado.
- [x] Executar validação final dos dados migrados.
- [x] Configurar integrações finais.
- [x] Revisar a documentação de processos atualizada.
- [x] Comunicar o Go Live para todos os stakeholders.
- [x] Preparar equipe para monitoramento intensivo nas primeiras semanas após o Go Live


## Identificação dos Stakeholders

&emsp;&emsp; Uma etapa essencial para qualquer projeto é o mapeamento de seus stakeholders. Eles são pessoas, grupos ou organizações que têm interesse ou estão envolvidos em um projeto. Podendo ser impactados pelas decisões, resultados ou execução do projeto. [(Brandão, 2024)](https://afonsobrandaointeli.github.io/modulo7si/06stakeholders/)

&emsp;&emsp; Os stakeholders podem ser classificados em dois tipos:

- **Internos:** Membros da equipe, gerentes, diretores.
- **Externos:** Clientes, fornecedores, parceiros, governos, comunidades.

&emsp;&emsp; Considerando a definição apresentada, os stakeholders do projeto e seus tipos são:

- **Gerente de Projeto**: Renato Penha - Interno 
- **Líder Técnico:** Egon Daxbacher - Interno | Eduarda - Externo 
- **Usuários Finais**: Externo - G2
- **Equipe de Suporte:** Walquíria, Lucas e Gabriel - Externo
- **Equipe de Desenvolvimento:** Daniel Zular, Henrique Cox, João Moura, Keylla Oliveira, Luiza Santana - Interno
- **Gestores de Área:** Eduarda - Externo

<br>


## Plano de Comunicação

&emsp;&emsp; O plano de comunicação é um componente essencial para o sucesso da implementação do SAP B1 na G2. Ele visa garantir que todos os stakeholders estejam informados de maneira eficaz ao longo do processo, utilizando canais adequados e uma abordagem clara e eficiente. Este plano define os responsáveeis e os métodos de comunicação a serem utilizados, incluindo reuniões, e-mails e plataformas online, com uma frequência ajustada conforme a necessidade de cada grupo. A execução desse plano não só facilita a fluidez da comunicação, como também ajuda a monitorar o progresso e ajustar estratégias conforme necessário, assegurando o alcance ee cumprimento do plano de trabalho.

| **Stakeholder** | **Interesses** | **Influência** | **Impacto** | **Expectativas** |
|-----------------|----------------|----------------|-------------|------------------|
| Detalhamento    | Objetivos      | Poder e influência - de 1 a 5 | Impacto no projeto | O que espera que eu atinja para benefício dele |
| Gerente de Projeto: **Renato Penha** | Planejar o módulo e dar suporte aos alunos | 5 | Em poucos casos, pode influenciar nas decisões dos grupos | Aprendizado e boa nota dos alunos |
| Gerente de suporte: **Egon Daxbacher** | Manter o bom funcionamento do projeto | 4 | Assessora nas decisões do Gerente de Projeto | Sucesso no módulo |
| Líder Técnico e Gestor: **Eduarda** | Definir escopo e planejar processos | 4 | Influencia muito nas decisões dos grupos | Qualidade no trabalho |
| Equipe de Suporte: **Walquíria** | Suporte ao desenvolvimento | 3 | Orienta passos a serem seguidos | Entendimento do conteúdo |
| Equipe de Suporte: **Lucas** | Suporte ao desenvolvimento | 3 | Orienta passos a serem seguidos | Entendimento do conteúdo |
| Equipe de Suporte: **Gabriel** | Suporte ao desenvolvimento | 3 | Orienta passos a serem seguidos | Entendimento do conteúdo |
| Equipe de Desenvolvimento: **Daniel Zular** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |
| Equipe de Desenvolvimento: **Henrique Cox** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |
| Equipe de Desenvolvimento: **João Moura** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |
| Equipe de Desenvolvimento: **Keylla Oliveira** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |
| Equipe de Desenvolvimento: **Luiza Santana** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |
| Equipe de Desenvolvimento: **Otto Lima** | Desenvolvimento dos entregáveis | 3 | Estando no escopo, tem poder de decisão e desenvolve o projeto | Colaboração e qualidade no trabalho |

&emsp;&emsp;A implementação bem-sucedida do plano de comunicação depende de um monitoramento contínuo e ajustes constantes, com o objetivo de verificar a efetividade das mensagens, coletar feedback e analisar o impacto das ações tomadas. Este processo garante que as informações circulem de maneira fluida, promovendo um senso de colaboração entre a equipe de desenvolvimento, os gestores e os usuários finais. 

## Validação do Ambiente de Produção

### Integridade dos Dados

&emsp;&emsp; As verificações para garantir a integridade dos dados pós-migração foram executadas e validadas. O SAP Business One já realiza uma série de processos automáticos para assegurar que a consistência dos dados migrados em relação ao sistema legado seja mantida. Portanto, com base nessas avaliações internas e nos testes realizados, tanto unitários quanto integrados, confirmamos que a integridade dos dados está preservada e de acordo com os requisitos do projeto.

### Acesso de Usuários

&emsp;&emsp; Todos os papéis de usuário foram devidamente atribuídos, segundo as necessidades operacionais e a estrutura hierárquica definida para a G2. Os acessos de usuários críticos e as permissões estão configuradas corretamente. O SAP Business One possui mecanismos automáticos de controle de permissões, garantindo que os níveis de acesso estejam conforme as regras de segurança e operação da empresa.

### Validação Funcional

&emsp;&emsp; Foram realizadas verificações funcionais de ponta a ponta, assegurando que os fluxos de processos críticos de negócio sejam adequadamente testados. Por meio dos <a href="https://docs.google.com/spreadsheets/d/1I5oqatKUOyMItkKxnzUH9m8W-tIY3YtuN6QRIbMoPXc/edit?usp=sharing">testes integrados</a>, desenvolvidos entre os 5 módulos, esses fluxos foram postos à prova, permitindo identificar falhas, realizar correções e garantir a aprovação de cada etapa. Isso garantiu que todas as funcionalidades operacionais estejam funcionando conforme o esperado. 

### Testes de Carga

&emsp;&emsp; A realização de testes de carga tem o objetivo de avaliar o comportamento de um sistema quando submetido a uma quantidade de usuários ou transações simultâneas equivalente ao seu uso esperado em situações reais. O objetivo é garantir que o sistema pode lidar com a carga projetada sem degradação significativa de desempenho ou falhas.

&emsp;&emsp; Tendo isso em vista, por meio desses testes, é possível midir diversos parâmetrosdo sistema, como:

- Tempo de resposta das funções críticas

- Uso de recursos

- Comportamento sob diferentes cenários de usuários 
simultâneos

- Identificação de gargalos, permitindo otimizações e ajustes nas configurações.

&emsp;&emsp; Para a realização dos testes de carga na SAP B1, é necessário realizar uma lista de passos que são essênciais para a seu funcionamento, sendo esses passos:

- **Definir Cenários de Testes:** Identificando os processos críticos, como criação de pedidos, execução de relatórios e gestão de inventário. Além de estimar a carga esperada (usuários simultâneos e transações).

- **Preparar o Ambiente de Teste:** Configurar um ambiente de teste idêntico ao de produção e fazer o backup dos dados, garantindo que o ambiente seja seguro para testes.

- **Executar os Testes:** Simular carga com usuários executando tarefas ao mesmo tempo, utilizando diversos processos para estressar o sistema.

- **Repetir e Validar:** Após todos os passos, faz-se a análise de todos os dados coletados, possíveis erros e então, são feitas melhorias e os testes são refeitos.

&emsp;&emsp; O processo ajuda a identificar gargalos e ajustar o sistema para garantir que ele esteja preparado para lidar com a carga de trabalho prevista. É uma parte essencial do planejamento de capacidade e da preparação do sistema para uso em produção.

### Verificação de Backup

&emsp;&emsp; O **backup** é uma cópia de segurança dos dados armazenados no sistema, essencial para garantir a integridade e a disponibilidade das informações em caso de falhas, perda de dados ou corrupção. No contexto do SAP Business One, os backups podem ser gerenciados diretamente através do **Microsoft SQL Server**, que gerencia os dados do sistema, envolvendo a criação de cópias completas do banco de dados da empresa, e também por meio do **Service Manager**, uma ferramenta do próprio SAP B1, a qual permite a configuração de backups automáticos.

**SQL Server Agent**

Para garantir que os backups sejam realizados automaticamente via SQL Server, é recomendável configurar o SQL Server Agent: [(SAP Support, 2024)](https://help.sap.com/docs/SAP_BUSINESS_ONE_ADMIN_GUIDE_SQL/f6fb230cc90949d8b66586a39189992b/4ac95f18c2414ab28e87612d08280a5d.html)

- Acessar o SQL Server Management Studio (SSMS).
- Verificar o funcionamento do SQL Server Agent e iniciá-lo, se necessário.
- Criar um novo Job no SQL Server Agent para agendar os backups:
  - Nomear o Job e definir as etapas para realizar o backup do banco de dados.
  - Configurar o agendamento para backups periódicos (diários, semanais, etc.).
  - Monitorar a execução do Job e os logs gerados para garantir que os backups estejam sendo realizados conforme o planejado.

**Service Manager** 

Outra opção é gerenciar os backups através do Service Manager do SAP B1: [(SAP Community, 2024)](https://community.sap.com/t5/enterprise-resource-planning-blogs-by-sap/sap-project-manager-s-guide-to-sap-project-cutover/ba-p/13510809)

- Acessar o Service Manager em: *Start > Programs > SAP Business One > Server Tools.*
- Selecionar ‘SBO Backup’ no menu suspenso e clicar em ‘Schedule' para definir o agendamento do backup automático.
- Configurar o local onde os backups serão salvos clicando no botão ‘Setting’ e definindo o caminho.
- Fornecer os detalhes do servidor SQL na opção de conexão.
- Selecionar o banco de dados desejado e pressionar ‘Start’. O sistema fará o backup do banco de dados no horário e local especificados.

**Atualizações e Correções**

O Rapid Support Package (RSP) é uma ferramenta que auxilia na aplicação de correções e melhorias ao SAP Business One, contribuindo para a estabilidade do sistema e, indiretamente, para a eficácia dos backups: [(SAP Support, 2024)](https://support.sap.com/en/offerings-programs/support-small-medium-enterprises/business-one/remote-support.html?anchorId=section_90889002)

- **Instalação do RSP:** Garante que o sistema esteja livre de bugs que possam impactar o processo de backup.
- **Documentação:** O RSP também fornece informações sobre novas funcionalidades que podem melhorar a execução de backups.

**Confirmar Configuração e Testes de Backup**

- **Verificação de Configurações:** Confirme que os parâmetros de backup foram configurados corretamente no SQL Server e revise os logs para assegurar que os backups automáticos estão sendo realizados no horário previsto.
- **Teste de Restauração:** Realizar um teste de restauração em um ambiente de teste para garantir a recuperação dos dados:
  - No SSMS, selecionar Restore Database.
  - Escolher o arquivo de backup e definir um nome temporário para o banco de dados.
  - Verificar a integridade dos dados restaurados.
- Verificação de Integridade: Após a restauração, utilize o comando ‘DBCC CHECKDB’ para verificar a integridade do banco de dados restaurado.

&emsp;&emsp; Realizar a verificação regular dos backups é fundamental para garantir a segurança dos dados e a capacidade de recuperação em situações adversas. O uso de backups automáticos, juntamente com a aplicação de atualizações através do RSP, contribui significativamente para a eficiência e confiabilidade do processo de backup no SAP Business One. [(SAP Community, 2024)](https://community.sap.com/t5/enterprise-resource-planning-blogs-by-members/backup-atr%C3%A1ves-do-rsp/ba-p/13272984)



## Plano de Contigência

&emsp;&emsp;A implementação do SAP Business One é um processo complexo que envolve diversas etapas críticas e potenciais riscos que podem afetar o sucesso do projeto. O Plano de Contingência ajuda na antecipação desses riscos e estabelecer ações preventivas que garantam a continuidade das operações durante a estratégia de cutover. Este plano detalha os cenários possíveis, as medidas de contenção a serem adotadas, os responsáveis por cada ação e os prazos para sua execução, garantindo boa organização para a transição de sistemas. [(Sabino, 2024)](https://radardeprojetos.com.br/plano-de-cutover-o-segredo-para-uma-transicao-de-projetos-bem-sucedida/#:~:text=Um%20Plano%20de%20Cutover%20%C3%A9,seguidos%20durante%20essa%20transi%C3%A7%C3%A3o%20cr%C3%ADtica.)


| **Cenário**                                         | **Ação de Contenção**                                                                                                         | **Responsável**                   | **Prazo**                         |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|-----------------------------------|
| Desalinhamento entre a G2 e os Grupos               | Estabelecer checkpoints regulares para alinhamento, garantindo clareza nas expectativas e metas compartilhadas.               |  Equipes de Suporte e Desenvolvimento, Usuários Finais                | Imediato                          |
| Dificuldade na Customização do UX no SAP Business One | Realizar workshops focados na customização do UX, com suporte da G2 para garantir expertise nas personalizações necessárias.   | Equipe de Desenvolvimento e  Instrutor de UX     | Até 2 dias (Utilizar das reuniões regulares com a G2)                     |
| Falta de Participação de Membros na Daily           | Incentivar a participação ativa com lembretes e reforçar a importância das Dailys para o sucesso do projeto.                  | Equipe de Desenvolvimento                       | Imediato (Diário, durante as Dailys)         |
| Atraso na Entrega das Atividades                    | Implementar monitoramento rigoroso do cronograma com revisões regulares e ajustes durante o sprint para manter o prazo.        | Equipe de Desenvolvimento                       | Até 2 dias                   |
| Atraso na entrega de documentos por parte da G2     | Contatar o responsável da G2 e entender o prazo de entrega, reportar no Status Report e alinhar com a G2.                     | Líder Técnico e Gerente de Projeto                               | Imediato                    |
| Erros durante os testes integrados                  | Diagnosticar a causa do erro, corrigir, e reportar na planilha dos testes para consultas futuras.                             | Equipes de Desenvolvimento de todos os módulos                          | Até 2 horas (Durante os Testes Integrados)      |
| Configuração Incorreta de Parâmetros do Sistema     | Utilizar checklist detalhado, revisar definições com especialistas e realizar testes abrangentes para validar parâmetros.      | Equipe de Desenvolvimento                       | Imediato (pós identificação de erro)   |


&emsp;&emsp;Em suma, a preparação e a proatividade são elementos-chave para o sucesso na implementação do SAP Business One. O Plano de Contingência serve como um guia estratégico para lidar com adversidades, minimizando impactos e assegurando que a equipe preparada para desafios que surgirem. Através da colaboração e do comprometimento de todos os envolvidos, o projeto poderá atingir seus objetivos com eficiência e eficácia, garantindo uma transição bem-sucedida e a continuidade dos negócios.

## Suporte Pós Go-Live

&emsp;&emsp;**Go-live** é o momento em que um novo sistema, como o SAP B1, entra em operação no ambiente de produção. Esse estágio é crítico, pois envolve a transição completa dos processos antigos para o novo sistema.
Não obstante, a fase pós go-live é igualmente importante, pois é nesse momento que surgem ajustes e desafios que não foram previstos durante a implementação. A falta de um suporte adequado pode comprometer o desempenho do sistema e a adaptação dos usuários.

&emsp;&emsp;Ter um **plano de suporte pós go-live** é essencial para garantir o sucesso contínuo. Esse plano aborda o acompanhamento ativo, resolução de problemas, coleta de feedback, treinamento adicional e melhorias necessárias para estabilizar o sistema e extrair o máximo de benefícios da solução implementada. Isso evita riscos operacionais e assegura que a empresa mantenha suas atividades sem interrupções. [(EPI-USE, 2024)](https://www.epiuse.com.br/artigo/4-dicas-para-manter-seu-projeto-estrategico-pos-go-live)

&emsp;&emsp;Portanto, apesar de não fazermos parte do acompanhamento pós go-live do projeto, elaboramos um plano fictício, que pode ser acessado <a href="https://docs.google.com/spreadsheets/d/17HR58MR7N1MOzB7BWPU6WP1m683Th3d9f0LI7A-MfFU/edit?usp=sharing">aqui</a>, e que julgamos relevante para essa fase.
O suporte pós go-live é a base que sustenta o desempenho e evolução contínua de um sistema recém-implementado. Ao oferecer um acompanhamento constante, identificar melhorias e capacitar os usuários, a G2 pode maximizar o valor do projeto, mitigando riscos e assegurando um crescimento fundamentado.

<br>

# Referências

BRANDÃO, Afonso. **Stakeholders.** Disponível em: https://afonsobrandaointeli.github.io/modulo7si/06stakeholders/. Acesso em: 10 set. 2024.

EPI-USE. **4 dicas para manter seu projeto estratégico pós-Go-Live.** EPI-USE Brasil, 2024. Disponível em: https://www.epiuse.com.br/artigo/4-dicas-para-manter-seu-projeto-estrategico-pos-go-live. Acesso em: 27 set. 2024.

MEDIUM. **Testing your new ERP system.** Medium, 2023. Disponível em: https://medium.com/1erp/testing-your-new-erp-system-bd4faa3d26fd. Acesso em: 8 set. 2024.

MEHRABAN, P. **Backup & Restore SAP Business One 9.2 Database.** SAP Community, 2018. Disponível em: https://community.sap.com/t5/enterprise-resource-planning-blogs-by-members/backup-restore-sap-business-one-9-2-database/ba-p/13330441. Acesso em: 27 set. 2024.

SABINO, Gaby. **Plano de Cutover: o segredo para uma transição de projetos bem-sucedida.** 09 abr. 2023. Disponível em: https://radardeprojetos.com.br/plano-de-cutover-o-segredo-para-uma-transicao-de-projetos-bem-sucedida/. Acesso em: 27 set. 2024.

SAP Community. **SAP project manager’s guide to SAP project cutover.** SAP Community, 2023. Disponível em: https://community.sap.com/t5/enterprise-resource-planning-blogs-by-sap/sap-project-manager-s-guide-to-sap-project-cutover/ba-p/13510809. Acesso em: 27 set. 2024.

SAP Community. **Backup através do RSP. SAP Community, 2018.** Disponível em: https://community.sap.com/t5/enterprise-resource-planning-blogs-by-members/backup-atr%C3%A1ves-do-rsp/ba-p/13272984. Acesso em: 27 set. 2024.

SAP Support. **SAP Business One, Administrator's Guide SQL – Backup.** SAP Help Portal, 2023. Disponível em: https://help.sap.com/docs/SAP_BUSINESS_ONE_ADMIN_GUIDE_SQL/f6fb230cc90949d8b66586a39189992b/4ac95f18c2414ab28e87612d08280a5d.html. Acesso em: 27 set. 2024.

SAP Support. **Remote Support Platform for SAP Business One.** SAP Support Portal, 2024. Disponível em: https://support.sap.com/en/offerings-programs/support-small-medium-enterprises/business-one/remote-support.html?anchorId=section_90889002. Acesso em: 27 set. 2024.