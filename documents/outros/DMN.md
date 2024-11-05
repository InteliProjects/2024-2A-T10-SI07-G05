# 2.2. Procedimentos e Regras de Negócios

&emsp;&emsp; Esta seção visa listar as regras de negócios presentes na área de compras da G2 que ditam o seu funcionamento, deveres e necessidades. Por meio de diagramas DMN e outras representações, cada processo será apresentado e decomposto com o intuito de melhor analisar suas necessidades e possíveis melhorias, sejam de estrutura ou de decisão. <p>

&emsp;&emsp; As regras de negócios foram estruturadas seguindo as seguintes características:

- **Nome:** Nome dado à regra de negócio, com um título descritivo do que a regra se trata;

- **Código:** Código exclusivo para identificar a regra de negócio;

- **Evento:** Situação ou condição que aciona a aplicação da regra de negócio;

- **Exemplo:** Representação de como a regra de negócio seria aplicada.

## 2.2.1 Procedimento de compra de licenças

&emsp;&emsp; O processo de compra de licenças é uma operação crítica para assegurar que a organização possua os recursos necessários para desempenhar suas atividades com eficiência. A aquisição de novas licenças envolve uma série de etapas rigorosas que devem ser seguidas para otimizar os custos e evitar desperdícios.<p>

&emsp;&emsp; As regras de negócios que regem este processo têm início a partir de uma solicitação proveniente dos setores de Vendas ou Estoque. Estas regras visam garantir que todas as compras sejam realizadas de maneira ordenada, transparente e econômica, respeitando os limites orçamentários e garantindo que as necessidades de licenciamento sejam atendidas sem exceder a capacidade financeira ou gerar estoque excessivo. <p>


<p align="center">Tabela XX - Regra de negócios</p>

|Item|Descrição|
|---|---|
|**Nome**| Solicitação de compra de licenças SAP pelo setor de Vendas|
|**Descrição**|Toda solicitação deve ser verificada no estoque antes de iniciar o processo de aquisição com fornecedores. Caso tenha estoque disponível, a compra não deve ser realizada|
|**Código**|CP001|
|**Evento**|Vendas abre pedido de compras de novas licenças|
|**exemplo**|Vendas fez um pedido de compras de 100 lincenças, sendo que no estoque há licenças suficientes para suprir a necessidade. A compra não é realizada|

<p align="center">Fonte: Elaborado pelos Autores.</p>

<p align="center">Tabela XX - Regra de negócios</p>

|Item|Descrição|
|---|---|
|**Nome**| Cotação com mínimo de fornecedores|
|**Descrição**|O setor de Compras deve realizar cotações com no mínimo três (3) fornecedores diferentes para qualquer compra|
|**Código**|CP002|
|**Evento**|O procesos de compras é iniciado e é necessário a consulta com fornecedores|
|**exemplo**|Vendas fez um pedido de compras de 100 lincenças, sendo que no estoque há licenças suficientes para suprir a necessidade. A compra não é realizada|

<p align="center">Fonte: Elaborado pelos Autores.</p>

<p align="center">Tabela XX - Regra de negócios</p>

|Item|Descrição|
|---|---|
|**Nome**| Limite financeiro|
|**Descrição**|Caso a realização de uma compra ultrapassar o limite estipulado pelo financeiro é necessário entrar em contato para liberação|
|**Código**|CP003|
|**Evento**|A cotação é finalizada e os valores estão acima do estipulado pelo financeiro|
|**exemplo**|A cotação apresenta valores acima de 100 mil reais e extrapolou o limite imposto, então a foi enviado um apedido de revisão para o financeiro|

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Diagrama

&emsp;&emsp; O Diagrama de Decisão (DMN) a seguir ilustra o fluxo de trabalho e as regras de decisão que guiam o processo de compra de licenças. Ele detalha os critérios que devem ser considerados antes da autorização de qualquer nova aquisição, incluindo a verificação de estoque, a realização de cotações com fornecedores, e a consulta ao setor financeiro para compras que excedam determinados valores. <p>

<p align="center">Imagem XX - DMN  de compra de licenças</p>

<img src="../../assets/imagens/DMN.jpg">

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Decisão 1

&emsp;&emsp; As decisões são ações tomadas pelo funcionário no sistema. Cada ação possui uma ou mais regras de negócio vinculadas a ela. No caso da primeira ação, é possível visualizar as regras para Conferir o estoque. <p>

<p align="center">Imagem XX - Tabela DMN  estoque</p>

<img src="../../assets/imagens/Tabela_1.png">

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Decisão 2

&emsp;&emsp; Verificação da quantidade de fornecedores consultadas pela equipe de compras. <p>

<p align="center">Imagem XX - Tabela DMN  fornecedores</p>

<img src="../../assets/imagens/Tabela_2.png">

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Decisão 3

&emsp;&emsp; Verificação do orçamento liberado para a área de compras. <p>

<p align="center">Imagem XX - Tabela DMN  orçamento</p>

<img src="../../assets/imagens/Tabela_3.png">

<p align="center">Fonte: Elaborado pelos Autores.</p>

## 2.2.2 Procedimento de compra de internos

&emsp;&emsp;O procedimento de compra de materiais ou serviços internos é essencial para garantir que todos os setores da empresa tenham acesso aos recursos necessários para desempenhar suas funções de maneira eficiente e conforme os padrões da organização. Esse processo envolve a aquisição de itens que são de uso comum ou específico dentro da empresa, como materiais de escritório, ferramentas, ou serviços que auxiliam nas operações diárias.<p>

&emsp;&emsp; Segue as tabelas:<p>

<p align="center">Tabela XX - Regra de negócios</p>

|Item|Descrição|
|---|---|
|**Nome**| Reposição mensal|
|**Descrição**|A cada mês é necessário iniciar um pedido de reposição de produtos internos, caso não tenha problemas com caixa. Se for o caso, é necessário consultar o financeiro|
|**Código**|CP004|
|**Evento**|A cada fim de mês é acionado o pedido de novos produtos internos|
|**exemplo**|Ao chegar no primeiro dia do mês, verifica-se o caixa e se for possível a compra é realizada|

<p align="center">Fonte: Elaborado pelos Autores.</p>


<p align="center">Tabela XX - Regra de negócios</p>

|Item|Descrição|
|---|---|
|**Nome**| Pagamento adiantado|
|**Descrição**|No caso de pagamento adiantado (inteiro ou parcial) é necessário criar uma fatura de adiantamento.|
|**Código**|CP005|
|**Evento**|Fornecedor solicita pagamento adiantado|
|**exemplo**|Durante a compra, dependendo do fornecedor, é necessário realizar o pagamento adiantado, junto com a emissão da fatura de adiantamento.|

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Diagrama

&emsp;&emsp; O Diagrama de Decisão (DMN) a seguir ilustra o fluxo de trabalho e as regras de decisão que guiam o processo de compra de internos. Ele detalha os critérios seguidos, além de um caso de pagamento adiantado, que pode ocorrer também com a compra de licenças. <p>

<p align="center">Imagem XX - DMN  interno</p>

<img src="../../assets/imagens/DMN_interno.png">

<p align="center">Fonte: Elaborado pelos Autores.</p>

### Decisão 2

&emsp;&emsp; A decisão de realizar o pagamento adiantado é baseada no pedido do fornecedor e na disponibilidade do caixa da G2.<p>

<p align="center">Imagem XX - Tabela DMN adiantamento</p>

<img src="../../assets/imagens/Tabela_4.png">

<p align="center">Fonte: Elaborado pelos Autores.</p>

