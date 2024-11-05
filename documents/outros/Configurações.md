# Configurações Iniciais e Análise dos Dados Mestres

&emsp;&emsp;Neste documento, será listado o passo a passo das configurações realizadas na plataforma.

# 1. Configurações SAP

## ASAP

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725240467/imagens%20inteli/Inteli.png)

## Sumário

1. [Configurações iniciais](#1-configurações-iniciais)
   1. [Configurações padrão](#11-configurações-padrão)
      1. [Administrar custo de item por depósito](#111-administrar-custo-de-item-por-depósito)
      
      2. [Ativar recursos de múltiplas filiais](#112-ativar-recursos-de-múltiplas-filiais)
      3. [Ativar determinação avançada](#114-ativar-determinação-avançada)

   2. [Configurações Específicas](#12-configurações-específicas)
      1. [Inscrição das filiais](#121-inscrição-das-filiais)
      2. [Definição de moedas](#122-definição-de-moedas)
      3. [Inicialização básica](#123-inicialização-básica)

         1. [Alteração de moedas](#1231-alteração-de-moedas)

         2. [Suporte Multilíngue](#1232-suporte-multilíngue)
         3. [Método de avaliação de grupos de itens](#1233-método-de-avaliação-de-grupos-de-itens)
         4. [Permissão de liberação do estoque sem custo de item](#1234-permissão-de-liberação-do-estoque-sem-custo-de-item)

      4. [Informações bancárias](#124-informações-bancárias)
      5. [Filial padrão](#125-filial-padrão)
      6. [Restrições da atividade do cliente](#126-restrições-da-atividade-do-cliente)
      7. [Definição de comissão](#127-definição-de-comissão)
      8. [Criação de condições de pagamento](#128-criação-de-condições-de-pagamento)
      9. [Preferência de pagamento](#129-preferência-de-pagamento)
      10. [Formato hora e data](#1210-formato-hora-e-data)
      11. [Exibição de casas decimais](#1211-exibição-de-casas-decimais)
      12. [Método de administração](#1212-método-de-administração)
      13. [Adição automática](#1213-adição-automática)
      14. [Determinação de conta do Razão](#1214-determinação-de-conta-do-razão)
      
      15. [Contabilidade de custo](#1215-contabilidade-de-custo)
         1. [Dimensões](#12151-dimensões)
         2. [Centros de custo](#12152-centros-de-custo)
      16. [Despesas de Importação](#1216-despesas-de-importação)
      17. [Despesas adicionais](#1217-despesas-adicionais)
      18. [Definição dos depósitos](#1218-definição-dos-depósitos)
      19. [Definição de grupos de itens](#1219-definição-de-grupos-de-itens)
      20. [Impostos](#1220-impostos)
      21. [Cartões de crédito](#1221-cartões-de-crédito)
      22. [Grupos de comissões](#1222-grupos-de-comissões)
      23. [Cadastro de vendedores](#1223-cadastro-de-vendedores)
      24. [Níveis de oportunidade](#1224-níveis-de-oportunidade)
      25. [Grupos de clientes](#1225-grupos-de-clientes)
      26. [Fornecedores](#1226-fornecedores)
      27. [Tipos de expedição](#1227-tipos-de-expedição)
      28. [Configurações finais](#1228-configurações-finais)
   3. [DTW](#13-dtw)

2. [Validação dos Dados Mestres](#2-validação-dos-dados-mestres)

   1. [OCRD](#21-OCRD)

   2. [CRD1](#22-CRD1)
   3. [CRD7](#23-CRD7)
   4. [OCRB](#24-OCRB)
   5. [DTW](#25-DTW)
   6. [Itens](#26-itens)

<br>

## 1. Configurações Iniciais
  
### 1.1. Configurações Padrão

&emsp;&emsp;As primeiras configurações são padrão do sistema SAP e devem ser implementadas em qualquer empresa que utilize a ferramenta. Estas configurações serão explicadas a seguir.

### 1.1.1 Administrar custo de item por depósito  

&emsp;&emsp;Durante esta etapa, são realizadas algumas regulamentações em relação a como os itens no depósitos serão gerenciados. Para acessá-la é necessário entrar, na barra superior, em Módulo -> Administração -> Inicialização do sistema -> Detalhes da empresa, como mostrado na imagem abaixo.
  
<p align="center">Imagem 1 - Administrar custo de item por depósito</p>

![](https://res.cloudinary.com/dgjhlonmk/image/upload/v1725231655/imagens%20inteli/Imagem%201%20-%20Administrar%20custo%20de%20item%20por%20dep%C3%B3sito.png)

<p align="center">Fonte: Autoria própria.</p>


### 1.1.2 Ativar recursos de múltiplas filiais

&emsp;&emsp;A segunda configuração é relativa à administração dos estoques baseada nos depósitos registrados. Novamente, é preciso marcar a opção “Administrar estoque por depósito”. O menu pode ser encontrado em Módulo -> Administração -> Inicialização do sistema -> Configurações do documento -> Aba Geral

<p align="center">Imagem 2 - Administrar estoque por depósito</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232133/imagens%20inteli/Imagem%202%20-%20Administrar%20estoque%20por%20dep%C3%B3sito.png)

<p align="center">Fonte: Autoria própria.</p>

&emsp;&emsp;**Importante:** Esta é uma configuração irreversível

### 1.1.3 Ativar recursos de múltiplas filiais 

&emsp;&emsp;O recurso de múltiplas filiais permite a adição de mais de um CNPJ ao sistema e deve ser sempre ativada. Para realizá-la é necessário entrar em Módulo -> Administração -> Inicialização do sistema -> Detalhes da empresa -> Aba Inicialização básica

<p align="center">Imagem 3 - Ativar recursos de múltiplas filiais</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232244/imagens%20inteli/Imagem%203%20-%20%20Ativar%20recursos%20de%20m%C3%BAltiplas%20filiais.png)

<p align="center">Fonte: Autoria própria.</p>

&emsp;&emsp;**Importante:** Esta configuração é irreversível

### 1.1.4 Ativar determinação avançada

&emsp;&emsp;Esta etapa realiza a configuração de algumas regras de contabilidade. É possível acessá-la em Módulo -> Administração -> Inicialização -> Detalhes da empresa ->

<p align="center">Imagem 4 - Ativar determinação avançada</p>

![](https://res.cloudinary.com/dgjhlonmk/image/upload/v1725232336/imagens%20inteli/Imagem%204%20-%20Ativar%20determinação%20avançada.png)

<p align="center">Fonte: Autoria própria.</p>

-  **Importante:** Uma janela de confirmação aparece. Selecione a primeira opção e salve

### 1.2. Configurações específicas

### 1.2.1 Inscrição das filiais  

&emsp;&emsp;Esta configuração se refere às etapas 1.01 a 1.05 do Business Blueprint (BBP). Agora, serão adicionadas as filiais. O caminho é Módulo -> Administração -> Definição -> Finanças -> Filiais

<p align="center">Imagem 5 - Inscrição das filiais</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232407/imagens%20inteli/Imagem%205%20-%20%20Inscri%C3%A7%C3%A3o%20das%20filiais.png)

<p align="center">Fonte: Autoria própria.</p>

&emsp;&emsp;A filial necessária já veio adicionada no banco de dados.


### 1.2.2 Definição de moedas

&emsp;&emsp;Esta configuração está relacionada com o tópico 1.08 do BBP e diz respeito às moedas que serão utilizadas pelo sistema. É possível acessá-la em Módulos -> Administração -> Definição -> Finanças -> Moedas

<p align="center">Imagem 6 - Definição de moedas</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232535/imagens%20inteli/Imagem%206%20-%20Defini%C3%A7%C3%A3o%20de%20moedas.png)

<p align="center">Fonte: Autoria própria.</p>


&emsp;&emsp;As moedas do sistema já vieram adicionadas.


### 1.2.3 Inicialização básica

&emsp;&emsp;As etapas a seguir serão configuradas na mesma aba, a qual pode ser acessada através do seguinte caminho: Módulos -> Administração -> Inicialização do Sistema -> Detalhes da empresa -> Aba Inicialização básica

### 1.2.3.1 Alteração de moedas

&emsp;&emsp;Nesse momento é necessário definir qual tipo de moeda será a corrente (tópico 1.08.02 do BBP) e qual será a do sistema (tópico 1.08.03 do BBP). Na aba “Inicialização básica” é possível definir “Moeda Corrente” e “Moeda do Sistema”, como mostra a imagem abaixo.

<p align="center">Imagem 13 - Alteração de moedas</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232749/imagens%20inteli/Imagem%2013%20-%20Altera%C3%A7%C3%A3o%20de%20moedas.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.3.2 Suporte Multilíngue

&emsp;&emsp;O segundo passo é definir se a plataforma deve aceitar o multilíngues, definição feita no tópico 1.09 do BBP. Conforme o BBP, ativamos o *checkbox* “Suporte multilíngue”, como mostra a imagem abaixo.

<p align="center">Imagem 14 - Suporte Multilíngue</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232877/imagens%20inteli/Imagem%2014%20-%20%20Suporte%20Multil%C3%ADngue.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.3.3 Método de avaliação de grupos de itens

&emsp;&emsp;Nesse momento é necessário definir qual será o método de avaliação utilizado pela empresa, dado contido no tópico 1.10 no BBP. Na aba “Inicialização básica” é possível escolher entre 3 opções de métodos: Preço médio móvel; Padrão e FIFO, como mostra a imagem abaixo. Seguindo o BBP, escolhemos “Preço médio móvel”.

<p align="center">Imagem 15 - Método de avaliação de grupos de itens</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725232967/imagens%20inteli/Imagem%2015%20-%20%20M%C3%A9todo%20de%20avalia%C3%A7%C3%A3o%20de%20grupos%20de%20itens.png)

<p align="center">Fonte: Autoria própria.</p>

### 1.2.3.4 Permissão de liberação do estoque sem custo de item

&emsp;&emsp;É necessário deixar o *checkbox* do item “Permitir liberação do estoque sem custo do item” desativado, conforme a definição da empresa no tópico 1.11 do BBP, como mostra a imagem abaixo.

<p align="center">Imagem 16 - Permissão de liberação do estoque sem custo de item</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725233110/imagens%20inteli/Imagem%2016%20-%20Permiss%C3%A3o%20de%20libera%C3%A7%C3%A3o%20do%20estoque%20sem%20custo%20de%20item.png)

<p align="center">Fonte: Autoria própria.</p>

### 1.2.4 Informações bancárias 

&emsp;&emsp;O quarto passo é definir as informações bancárias da empresa, dado contido no tópico 4 do BBP, para preencher os dados é necessário acessar: Módulos -> Administração -> Definição -> Banco -> Contas bancárias da empresa, como mostra a imagem abaixo. Atenção: no BBP existem duas colunas diferentes: “Dígito Agência” e “Nº da Conta” e no SAP essas colunas estão contidas em “Nº da Conta”.

<p align="center">Imagem 17 - Informações bancárias</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725233207/imagens%20inteli/Imagem%2017%20-%20Informa%C3%A7%C3%B5es%20banc%C3%A1rias.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 18 - Contas bancárias da empresa</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725233349/imagens%20inteli/Imagem%2018%20-%20Contas%20banc%C3%A1rias%20da%20empresa.png)

<p align="center">Fonte: Autoria própria.</p>
  
### 1.2.5 Filial padrão

&emsp;&emsp;O próximo passo é confirmar qual será a filial padrão da empresa, definido no tópico 1.12, para isso é necessário acessar Módulos -> Administração -> Inicialização do Sistema -> Detalhes da empresa, e acessar a aba “Inicialização básica” é possível definir a filial padrão, como mostra as imagens abaixo.
  
<p align="center">Imagem 19 - Filial padrão</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725233516/imagens%20inteli/Imagem%2019%20-%20Filial%20padr%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 20 - Filial padrão 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725233633/imagens%20inteli/Imagem%2020%20-%20Filial%20padr%C3%A3o%202.png)

<p align="center">Fonte: Autoria própria.</p>  

### 1.2.6 Restrições da atividade do cliente

&emsp;&emsp;É necessário ativar ou não o limite de crédito e limite de compromisso na aba: Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba PN, como mostra a imagem abaixo. A informação pode ser acessada no tópico 2.01 do BBP.

<p align="center">Imagem 21 - Restrições da atividade do cliente</p>

![](https://res.cloudinary.com/dgjhlonmk/image/upload/v1725234125/imagens%20inteli/Imagem%2021%20-%20Restri%C3%A7%C3%B5es%20da%20atividade%20do%20cliente.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 22 - Restrições da atividade do cliente 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234182/imagens%20inteli/Imagem%2022%20-%20Restri%C3%A7%C3%B5es%20da%20atividade%20do%20cliente%202.png)

<p align="center">Fonte: Autoria própria.</p> 

**Levantamento BBP:**

- Limite de Crédito e Limite de Compromisso: Conforme o documento BBP que o Limite de Crédito e Limite de Compromisso foi marcado como “Não”. O que significa que mesmo que o cliente esteja devendo um valor para a empresa, será aceita uma compra do mesmo. É importante revisar com o cliente se está certo.


### 1.2.7 Definição de comissão

&emsp;&emsp;Para definir quem irá receber a comissão, é necessário entrar em: Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba PN. O consultor deve acessar o tópico “Definir comissão para” e assinalar entre 3 opções: Vendedores; Itens e Clientes conforme o dado disponibilizado pela empresa no tópico 2.02 do BBP.

<p align="center">Imagem 23 - Definição de comissão</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234274/imagens%20inteli/Imagem%2023%20-%20%20%20Defini%C3%A7%C3%A3o%20de%20comiss%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 24 - Definição de comissão 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234351/imagens%20inteli/Imagem%2024%20-%20%20%20Defini%C3%A7%C3%A3o%20de%20comiss%C3%A3o%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.8 Criação de condições de pagamento

&emsp;&emsp;Nesse momento, é necessário procurar todas as condições de pagamento que já vem com o sistema, para isso é necessário acessar: Módulos -> Administração -> Definição -> Parceiro de Negócios -> Condições de pagamento, como mostrado na imagem abaixo. A seguir o consultor deve clicar no botão procurar e digitar “*” e procurar (Imagem 26). Após esse processo, o sistema abrirá uma aba nova com todas as condições já configuradas, e deve-se checar se todas informadas pelo cliente no tópico 11.01 estão no SAP B1 (Imagem 28). Importante: caso alguma não esteja, é possível cadastrar na aba Condições de pagamento, porém deve-se estar no modo “Adicionar”. (Imagem 29)


<p align="center">Imagem 25 - Criação de condições de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234478/imagens%20inteli/Imagem%2025%20-%20Cria%C3%A7%C3%A3o%20de%20condi%C3%A7%C3%B5es%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 26 - Criação de condições de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234537/imagens%20inteli/Imagem%2026%20-%20Cria%C3%A7%C3%A3o%20de%20condi%C3%A7%C3%B5es%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 27 - Criação de condições de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234642/imagens%20inteli/Imagem%2027%20-%20Cria%C3%A7%C3%A3o%20de%20condi%C3%A7%C3%B5es%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 28 - Criação de condições de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234765/imagens%20inteli/Imagem%2028%20-%20Cria%C3%A7%C3%A3o%20de%20condi%C3%A7%C3%B5es%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 29 - Criação de condições de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234832/imagens%20inteli/Imagem%2029%20-%20Cria%C3%A7%C3%A3o%20de%20condi%C3%A7%C3%B5es%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.9 Preferência de pagamento

&emsp;&emsp;A seguir, é necessário definir qual será o padrão de pagamento da empresa, para isso deve-se acessar: Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba PN, ir para “Preferências de Pagamento” e escolher a opção descrita no tópico 2.03 do BBP. A imagem abaixo mostra como realizar essa configuração. Lembre-se: existem 2 configurações que devem ser feitas aqui: “Condições padrão de pagamento para cliente” e “Condições padrão de pagamento para fornecedor”.

<p align="center">Imagem 30 - Preferência de pagamento</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234897/imagens%20inteli/Imagem%2030%20-%20Prefer%C3%AAncia%20de%20pagamento.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 31 - Preferência de pagamento 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725234947/imagens%20inteli/Imagem%2031%20-%20Prefer%C3%AAncia%20de%20pagamento%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.10 Formato hora e data

&emsp;&emsp;Para o sistema ficar ainda mais personalizado para a empresa, é possível definir o formato de data e de hora, conforme os tópicos 2.04 e 2.05 do BBP. Para configurar, é necessário acessar: 

- Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba Exibir, e definir nos campos “Formato da hora” e “Formato da data”, como mostra as imagens abaixo.

<p align="center">Imagem 32 - Formato hora e data</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235007/imagens%20inteli/Imagem%2032%20-%20Formato%20hora%20e%20data.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 33 - Formato hora e data 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235070/imagens%20inteli/Imagem%2033%20-%20Formato%20hora%20e%20data%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.11 Exibição de casas decimais 

&emsp;&emsp;A seguir, é possível configurar a quantidade de casas decimais que a empresa deseja visualizar para cada tipo de produto, como: 

- Valores; 
- Preços; 
- Taxas; 
- Quantidades; 
- Percentagem; 

&emsp;&emsp;Unidades e Decimais na consulta, conforme o tópico 2.06 do BBP. Para realizar essa configuração é necessário acessar: 

- Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba Exibir e definir na parte “Casas Decimais”, como mostra as imagens abaixo.

**Atenção:** O consultor não pode alterar o campo “Valores” para diferente de 2.

<p align="center">Imagem 34 - Exibição de casas decimais</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235152/imagens%20inteli/Imagem%2034%20-%20Exibi%C3%A7%C3%A3o%20de%20casas%20decimais.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 35 - Exibição de casas decimais 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235331/imagens%20inteli/Imagem%2035%20-%20Exibi%C3%A7%C3%A3o%20de%20casas%20decimais%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.12 Método de administração 

&emsp;&emsp;A próxima configuração é utilizada para definir em que momento deve ser pedido o número de série para a saída do depósito, o SAP fornece 2 opções: “Em todas as transações” e “ Apenas na liberação”, para defini-la é necessário seguir esse caminho: Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba Estoque. A configuração deve ser feita conforme o tópico 2.07 do BBP. As imagens abaixo demonstram como pode ser feita essa configuração.

<p align="center">Imagem 36 - Método de administração</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235419/imagens%20inteli/Imagem%2036%20-%20M%C3%A9todo%20de%20administra%C3%A7%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 37 - Método de administração 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235492/imagens%20inteli/Imagem%2037%20-%20M%C3%A9todo%20de%20administra%C3%A7%C3%A3o%202.png)

<p align="center">Fonte: Autoria própria.</p>


### 1.2.13 Adição automática

&emsp;&emsp;No mesmo caminho feito no passo anterior, Módulos -> Administração -> Inicialização do sistema -> Configurações gerais -> aba Estoque, é possível atribuir um depósito automático aos itens, conforme a resposta da empresa no tópico 2.08 no BBP. As imagens abaixo mostram como pode ser feita essa etapa.

<p align="center">Imagem 38 - Adição automática</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235571/imagens%20inteli/Imagem%2038%20-%20Adi%C3%A7%C3%A3o%20autom%C3%A1tica.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 39 - Adição automática 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725235766/imagens%20inteli/Imagem%2039%20-%20Adi%C3%A7%C3%A3o%20autom%C3%A1tica%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.14 Determinação de conta do Razão

&emsp;&emsp;A seguir o consultor deve verificar se todas as informações cadastradas no tópico 5.012do BBP também está cadastrada no SAP B1, seguindo o caminho: Módulos -> Administração -> Definição -> Finanças -> Determinação de conta do Razão -> Determinação de conta do Razão -> aba Vendas. As imagens abaixo demonstram como realizar essa etapa.

<p align="center">Imagem 40 - Determinação de conta do Razão</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236036/imagens%20inteli/Imagem%2040%20-%20Determina%C3%A7%C3%A3o%20de%20conta%20do%20Raz%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 41 - Determinação de conta do Razão 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236099/imagens%20inteli/Imagem%2041%20-%20Determina%C3%A7%C3%A3o%20de%20conta%20do%20Raz%C3%A3o%202.png)

<p align="center">Fonte: Autoria própria.</p>

### 1.2.15 Contabilidade de custo

### 1.2.15.1 Dimensões

&emsp;&emsp;Para essa etapa é necessário acessar: Módulos -> Finanças -> Contabilidade de custos -> Dimensões, e assim alterar a “Descrição” conforme o que a empresa descreveu no tópico 6.01 do BBP. As imagens abaixo demonstram a etapa.

<p align="center">Imagem 42 - Contabilidade de custo (dimensões)</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236181/imagens%20inteli/Imagem%2042%20-%20Contabilidade%20de%20custo%20%28dimens%C3%B5es%29.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 43 - Contabilidade de custo (dimensões 2)</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236245/imagens%20inteli/Imagem%2043%20-%20Contabilidade%20de%20custo%20%28dimens%C3%B5es%202%29.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.15.2 Centros de custo

&emsp;&emsp;A segunda etapa de Contabilidade de Custo pode ser definida em: Módulos -> Finanças -> Contabilidade de custos -> Centros de custo, conforme o tópico 6.02 do BBP. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 44 - Contabilidade de custo (Centros de custo)</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236343/imagens%20inteli/Imagem%2044%20-%20Contabilidade%20de%20custo%20%28Centros%20de%20custo%29.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 45 - Contabilidade de custo (Centros de custo 2)</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236420/imagens%20inteli/Imagem%2045%20-%20Contabilidade%20de%20custo%20%28Centros%20de%20custo%202%29.png)

<p align="center">Fonte: Autoria própria.</p>


**Levantamento BBP:**

- Cód. Ordenação: Códigos não foram preenchidos pelo cliente.
  

### 1.2.16 Despesas de Importação

&emsp;&emsp;A seguir é necessário cadastrar quais são as despesas que a empresa tem com a importação, essa etapa deve ser definida em: Módulos -> Administração -> Definição -> Compras -> Despesas de importação. Essas despesas são definidas no tópico 7.01 do BBP. As imagens abaixo demonstram essa etapa.

**Obs:** Impostos não são cadastrados aqui.

<p align="center">Imagem 46 - Despesas de Importação</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236502/imagens%20inteli/Imagem%2046%20-%20Despesas%20de%20Importa%C3%A7%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>
  

**Levantamento BBP:**

- Informações não foram preenchidas pelo cliente.


### 1.2.17 Despesas adicionais

&emsp;&emsp;As despesas adicionais estão presentes no tópico 7.02 do BBP, e o consultor deve clicar no campo em vermelho para acessar a aba do Excel específico, como mostra a imagem 47. Para configurar no SAP B1, é necessário acessar: Módulos -> Administração -> Definição -> Geral -> Despesas adicionais, como mostra a imagem 48.

<p align="center">Imagem 47 - Despesas de Importação</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236576/imagens%20inteli/Imagem%2047%20-%20Despesas%20de%20Importa%C3%A7%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 48 - Despesas adicionais</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236644/imagens%20inteli/Imagem%2048%20-%20Despesas%20adicionais.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 49 - Despesas adicionais 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236726/imagens%20inteli/Imagem%2049%20-%20Despesas%20adicionais%202.png)

<p align="center">Fonte: Autoria própria.</p>
 

**Levantamento BBP:**

- Informações não foram preenchidas pelo cliente.


### 1.2.18 Definição dos depósitos

&emsp;&emsp;Agora, a próxima etapa é utilizada para cadastrar quais depósitos a empresa tem disponível, por meio do caminho: Módulos -> Administração -> Definição -> Estoque -> Depósitos, conforme o tópico 8.01 do BBP. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 50 - Definição dos depósitos</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236907/imagens%20inteli/iht37oemk4hvjv3ovppr.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 51 - Definição dos depósitos 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725236994/imagens%20inteli/rx0kdwjfvbeafmjf7qr3.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.19 Definição de grupos de itens

&emsp;&emsp;O “grupos de itens” deve ser definido em: Módulos -> Administração -> Definição -> Estoque -> Grupos de itens, conforme o tópico 9.01 do BBP. Esses grupos de itens são todos os itens que a empresa vende. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 52 - Definição de grupos de itens</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237117/imagens%20inteli/Imagem%2052%20-%20Defini%C3%A7%C3%A3o%20de%20grupos%20de%20itens.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 53 - Definição de grupos de itens 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237350/imagens%20inteli/Imagem%2053%20-%20Defini%C3%A7%C3%A3o%20de%20grupos%20de%20itens%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.20 Impostos

&emsp;&emsp;A próxima configuração é feita em: Módulos -> Administração -> Definição -> Finanças -> Imposto -> Imposto retido na fonte, contido no tópico 10.01 do BBP. Caso algum imposto não esteja cadastrado, o consultor deve cadastrar uma nova linha seguindo o padrão do SAP B1. Além disso, caso o imposto esteja cadastrado, porém, com outra linha, o consultor também deve criar uma nova linha com esses dados. Importante: é de suma importância clicar na célula em vermelho para acessar a aba “Taxas” e entender as taxas de cada imposto.

<p align="center">Imagem 54 - Impostos</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237512/imagens%20inteli/Imagem%2054%20-%20Impostos.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 55 - Impostos 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237635/imagens%20inteli/Imagem%2055%20-%20Impostos%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.21 Cartões de crédito

&emsp;&emsp;A seguir é realizado o cadastro dos cartões que a empresa utiliza e que o sistema deve aceitar, essa etapa é feita em: Módulos -> Administração -> Definição -> Banco -> Cartões de crédito, o consultor deve acessar o tópico 12.01 para cadastrar. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 56 - Cartões de crédito</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237733/imagens%20inteli/Imagem%2056%20-%20Cart%C3%B5es%20de%20cr%C3%A9dito.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 57 - Cartões de crédito 2 (Definição)</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237828/imagens%20inteli/Imagem%2057%20-%20Cart%C3%B5es%20de%20cr%C3%A9dito%202%20%28%20Defini%C3%A7%C3%A3o%29.png)

<p align="center">Fonte: Autoria própria.</p>
  

### 1.2.22 Grupos de comissões

&emsp;&emsp;Agora, deve ser feito o cadastro dos grupos de comissões para serem selecionados no momento da criação dos vendedores, tópico 2.2.22 deste documento. Os dados estão contidos no tópico 14.02 do BBP e para realizar o cadastro, é necessário acessar: Módulos -> Administração -> Definição -> Geral -> Grupos de comissões, como mostra a imagem abaixo.

<p align="center">Imagem 58 - Grupos de comissões</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725237961/imagens%20inteli/Imagem%2058%20-%20Grupos%20de%20comiss%C3%B5es.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 60 - Grupos de comissões 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238046/imagens%20inteli/Imagem%2060%20-%20Grupos%20de%20comiss%C3%B5es%202.png)

<p align="center">Fonte: Autoria própria.</p>


### 1.2.23 Cadastro de vendedores

&emsp;&emsp;Em seguida deve ser feito o cadastro dos vendedores que a empresa tem, conforme o tópico 14.03 do BBP. No SAP B1 essa configuração é feita em: Módulos -> Administração -> Definição -> Geral -> Vendedores/Compradores. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 61 - Cadastro de vendedores</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238123/imagens%20inteli/Imagem%2061%20-%20Cadastro%20de%20vendedores.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 62 - Cadastro de vendedores 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238210/imagens%20inteli/Imagem%2062%20-%20Cadastro%20de%20vendedores%202.png)

<p align="center">Fonte: Autoria própria.</p>
  

**Levantamento BBP:**

- % da comissão: Não foi adicionada a porcentagem de comissão dos vendedores.
  

### 1.2.24 Níveis de oportunidade

&emsp;&emsp;A próxima configuração é feita em: Módulos -> Definição -> Oportunidades -> Níveis de Oportunidade, conforme o cadastro feito pela empresa no tópico 14.04 do BBP. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 63 - Níveis de oportunidade</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238372/imagens%20inteli/Imagem%2063%20-%20N%C3%ADveis%20de%20oportunidade.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 64 - Níveis de oportunidade 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238496/imagens%20inteli/Imagem%2064%20-%20N%C3%ADveis%20de%20oportunidade%202.png)

<p align="center">Fonte: Autoria própria.</p>


**Atenção:** A ordem importa nessa configuração
  

### 1.2.25 Grupos de clientes

&emsp;&emsp;Em seguida, deve-se criar grupos de clientes conforme o tópico 15 do BBP. No SAP B1, essa configuração deve ser feita em: Módulos -> Administração -> Definição -> Parceiros de negócios -> Grupos de Clientes, as imagens abaixo demonstram essa etapa.

<p align="center">Imagem 65 - Grupos de clientes</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238628/imagens%20inteli/xrarvdqsmpa2oe7cgcmz.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 66 - Grupos de clientes 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238689/imagens%20inteli/Imagem%2066%20-%20Grupos%20de%20clientes%202.png)

<p align="center">Fonte: Autoria própria.</p>


### 1.2.26 Fornecedores

&emsp;&emsp;A seguir, um grupo de fornecedores deve ser cadastrado conforme a lista disponibilizada pela empresa no tópico 16 do BBP. No SAP B1, essa configuração deve ser feita em: Módulos -> Administração -> Definição -> Parceiros de negócios -> Grupos de Fornecedores, as imagens abaixo demonstram essa etapa.

<p align="center">Imagem 67 - Fornecedores</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238789/imagens%20inteli/Imagem%2067%20-%20Fornecedores.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 68 - Fornecedores 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725238962/imagens%20inteli/Imagem%2068%20-%20Fornecedores%202.png)

<p align="center">Fonte: Autoria própria.</p>
 

### 1.2.26 Tipos de expedição

&emsp;&emsp;A penúltima configuração deve ser feita em: Módulos -> Administração -> Definição -> Estoque -> Tipos de envio, esta etapa deve ser realizada conforme o tópico 17 do BBP. Nela, deve ser cadastrado o nome e o Website do tipo de expedição. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 69 - Tipos de expedição</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725239199/imagens%20inteli/Imagem%2069%20-%20Tipos%20de%20expedi%C3%A7%C3%A3o.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 70 - Tipos de expedição 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725239372/imagens%20inteli/Imagem%2070%20-%20Tipos%20de%20expedi%C3%A7%C3%A3o%202.png)

<p align="center">Fonte: Autoria própria.</p>
 

### 1.2.28 Configurações finais

&emsp;&emsp;A última configuração deve ser feita em: Módulos -> Administração -> Inicialização do Sistema -> Configurações do documento, contida no tópico 18 do BBP. Essa configuração tem algumas etapas que irão finalizar a configuração do SAP B1. As imagens abaixo demonstram essa etapa.

<p align="center">Imagem 71 - Configurações finais</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725239518/imagens%20inteli/Imagem%2071%20-%20Configura%C3%A7%C3%B5es%20finais.png)

<p align="center">Fonte: Autoria própria.</p>

<br>

<p align="center">Imagem 72 - Configurações finais 2</p>

![](http://res.cloudinary.com/dgjhlonmk/image/upload/v1725239614/imagens%20inteli/Imagem%2072%20-%20Configura%C3%A7%C3%B5es%20finais%202.png)

<p align="center">Fonte: Autoria própria.</p>

### 1.3 DTW

&emsp;&emsp;O DTW, também chamado de Data Transfer Warehouse, é um programa do SAP B1 que permite a importação de dados, como por exemplo, telas, cadastro de itens e cadastro de fornecedores. Nesse momento, serão realizadas as seguintes importações: 2.3.1 Cadastro de Item; 2.3.2 Cadastro de Parceiro de Negócios.

&emsp;&emsp;O cliente deverá preencher uma planilha previamente encaminhada pela consultoria, com as colunas mostradas abaixo, essa planilha chamaremos de “Planilha Cliente”. A consultoria irá criar uma nova planilha para o tratamento dos dados, que chamaremos de “Planilha Consultoria”, esta será importada pelo DTW para o SAP B1.

<br>

# 2. Validação dos Dados Mestres

&emsp;&emsp;Os dados analisados nesta seção foram extraídos das planilhas Cadastro de Itens e Cadastro de PNs, sendo que a última contém as abas: “OCRD - Parceiros de Negócio”, “CRD1 - Informações de Endereço”, “CRD7 - Identificação Fiscal” e “OCRB - Dados Bancários”. Essas planilhas contêm informações essenciais sobre os parceiros de negócios da empresa, sejam eles clientes ou fornecedores. Além disso, o processo de importação dos dados para o SAP Business One foi realizado utilizando a ferramenta DTW (Data Transfer Workbench), garantindo a integridade e consistência das informações no sistema.

## 2.1 OCRD

&emsp;&emsp;A aba OCRD reúne os dados gerais dos parceiros de negócios, sejam eles clientes ou fornecedores. Esta planilha é fundamental para o cadastro inicial dos parceiros no SAP Business One, pois contém informações como:

- Código do parceiro de negócio: Código alfanumérico que identifica o parceiro dentro do sistema.
- Razão social: Nome registrado do parceiro de negócio.
- Tipo de Parceiro de Negócio: Identifica se o parceiro é um cliente ou fornecedor.
- Grupo do Parceiro: Categoria do parceiro dentro do sistema.
- Contatos: Telefone, e-mail e outros dados de contato essenciais.

&emsp;&emsp;Esses dados são cruciais para o gerenciamento das relações comerciais e logísticas da empresa.

## 2.2 CRD1

&emsp;&emsp;A aba CRD1 contém as informações de endereço dos parceiros de negócios. Estes dados são aplicáveis tanto para clientes quanto para fornecedores e incluem:

- Tipo de Endereço: Identifica se o endereço é de entrega, cobrança, ou outro.
- Nome do Endereço: Nome do local ou estabelecimento.
- Logradouro: Nome da rua, avenida, ou outro tipo de via.
- Número, Bairro, Cidade, Estado e CEP: Detalhes completos do endereço.
- Complemento: Informação adicional para localizar o endereço.

&emsp;&emsp;Essas informações são usadas para fins de entrega de produtos, correspondência, e pagamentos, assegurando que as operações logísticas ocorram sem falhas.


## 2.3 CRD7

&emsp;&emsp;A aba CRD7 concentra os dados de identificação fiscal dos parceiros de negócios, essenciais para o cumprimento das obrigações tributárias e fiscais. Os campos incluídos são:

- CNPJ/CPF: Cadastro Nacional de Pessoa Jurídica ou Física.
- Inscrição Estadual/Municipal: Registro oficial para fins fiscais e tributários.
- Código CNAE: Classificação Nacional de Atividades Econômicas.
- I.E.S.T: Inscrição Estadual Substituto Tributário.
- ID estrangeiro: Identificação usada para parceiros estrangeiros.
- Suframa: Registro para operações na Zona Franca de Manaus.

&emsp;&emsp;Essas informações são fundamentais para a emissão de notas fiscais, pagamento de impostos, e outras obrigações fiscais.

## 2.4 OCRB

&emsp;&emsp;A aba OCRB armazena os dados bancários dos parceiros de negócios, necessários para a execução de transações financeiras, tanto para clientes quanto para fornecedores. As informações incluem:

- Código do banco e Agência: Identificação da instituição bancária.
- Número da conta: Conta bancária do parceiro.
- Nome da conta: Titular da conta.
- Conta contábil: Conta usada para registrar as transações financeiras no sistema.

&emsp;&emsp;Esses dados garantem que todas as operações financeiras, como pagamentos e reembolsos, sejam realizadas de forma correta e eficiente.

## 2.5 DTW

&emsp;&emsp;DTW (Data Transfer Workbench) é a ferramenta utilizada para a importação em massa dos dados mestres para o SAP Business One. No contexto deste projeto, o DTW foi aplicado para transferir todos os dados contidos nas planilhas OCRD, CRD1, CRD7, e OCRB para o SAP Business One. 

&emsp;&emsp;Passos para uso do DTW:

1. Preparação dos Dados: As planilhas foram limpas e preparadas de acordo com os padrões passados pela G2.

2. Validação dos Dados: Verificação completa para assegurar a precisão e a integridade dos dados antes da importação, com correção de erros e levantamento de incompletudes.

3. Importação via DTW: Os dados foram carregados no SAP Business One, associando as colunas das planilhas com os campos correspondentes no sistema.

4. Verificação Pós-Importação: Após a importação, todos os dados foram revisados com uma pessoa da G2 no SAP Business One para garantir que a migração foi realizada com sucesso.

&emsp;&emsp;A utilização do DTW garantiu que os dados fossem importados com mínimos erros, respeitando o formato necessário, crucial para a integridade e consistência das informações no sistema.

## 2.6 Itens

&emsp;&emsp;A tabela cadastro de itens contém diversas colunas que representam os atributos dos itens, como código, nome, grupo de itens, fabricante, e várias outras propriedades relevantes para a gestão de estoque e compras no SAP.

&emsp;&emsp;Cada campo tem um papel específico no SAP, ajudando a definir como o item será gerido em termos de logística, finanças e operações.

&emsp;&emsp;Analisar os Dados Mestres pode fornecer insights valiosos para a gestão do negócio, tais como:

- Otimização de Estoque: Verificar se os itens são comprados em quantidade adequada para evitar excesso ou falta.

- Eficiência de Compras: Avaliar o método de aquisição para melhorar a negociação com fornecedores.

- Compliance: Garantir que os dados estejam alinhados com as regulamentações, evitando problemas legais.

### Campos e suas Descrições

1. **ItemCode**: Código único que identifica o item no sistema. Este código é essencial para rastreamento e referência em processos de compras, vendas e estoque.

2. **ItemName**: Nome ou descrição do item. Facilita a identificação do item por usuários que não estão familiarizados com o código.

3. **ForeignName**: Nome estrangeiro do item, se aplicável. Utilizado em transações internacionais ou quando o nome do item precisa ser registrado em outro idioma.

4. **ItemsGroupCode**: Código que agrupa itens similares em categorias. Ajuda na organização e na aplicação de políticas de compra e venda por grupo.

5. **ItemType**: Tipo de item (ex.: matéria-prima, produto acabado). Define a natureza do item e como ele será tratado nos processos de fabricação e estoque.

6. **PurchaseItem**: Indicador (Sim/Não) de se o item é comprável. Informa se o item pode ser adquirido através de pedidos de compra.

7. **SalesItem**: Indicador (Sim/Não) de se o item é vendável. Informa se o item pode ser incluído em ordens de venda.

8. **InventoryItem**: Indicador (Sim/Não) de se o item é controlado em estoque. Especifica se o item é sujeito a controle de inventário.

9. **Manufacturer**: Nome do fabricante do item. Importante para rastreabilidade e garantia de qualidade.

10. **ShipType**: Tipo de envio ou transporte do item. Pode ser usado para determinar o método de envio preferencial ou necessário.

11. **GLMethod**: Método de contabilização associado ao item. Determina como as transações financeiras relacionadas ao item serão tratadas na contabilidade.

12. **EvaluationSystem**: Sistema de avaliação do item (ex.: custo médio, FIFO). Define como o custo do item será calculado no inventário.

13. **ByWh**: Armazém específico associado ao item, se aplicável. Indica se o item é controlado em um ou mais armazéns específicos.

14. **PartiallyAP**: Indicador de aplicação parcial de AP. Pode indicar se o item permite tratamento de contabilidade parcial.

15. **CreatedBy**: Usuário que criou o item no sistema. Fornece rastreamento de auditoria e responsabilidade.

16. **CreateDate**: Data de criação do item no sistema. Importante para controle de tempo e ciclo de vida do item.

17. **UpdDate**: Data da última atualização do item. Ajuda a rastrear quando as informações do item foram modificadas pela última vez.

18. **ValidUntil**: Data até a qual o item é válido. Pode ser usado para itens que têm um ciclo de vida limitado ou data de expiração.

19. **FrozenFor**: Indicador de se o item está congelado para transações. Pode ser utilizado para bloquear temporariamente o item de ser utilizado em operações.

20. **FrozenFrom**: Data a partir da qual o item foi congelado. Mostra desde quando o item foi bloqueado para operações.

21. **ValidFrom**: Data a partir da qual o item é válido. Especifica quando o item começou a ser válido para uso no sistema.

22. **U_License**: Licença associada ao item, se aplicável. Pode ser usada para itens que exigem licenciamento especial.

23. **SWW**: Indicador ou código específico da empresa relacionado ao item (o significado exato depende da configuração da empresa).

24. **MaxInventory**: Quantidade máxima de inventário permitida para o item. Ajuda a evitar excesso de estoque.

25. **PlanningSystem**: Sistema de planejamento associado ao item (ex.: MRP, reabastecimento). Define como as necessidades de estoque para o item serão planejadas.

26. **ProcurementMethod**: Método de aquisição do item (ex.: produção interna, compra externa). Informa como o item será obtido.

27. **OrderMultiple**: Múltiplo de pedido, indicando a quantidade mínima que deve ser encomendada. Útil para otimizar pedidos e reduzir custos.

28. **MinOrderQuantity**: Quantidade mínima de pedido para o item. Ajuda a garantir que pedidos não sejam feitos abaixo de um valor economicamente viável.

29. **LeadTime**: Tempo de entrega ou produção do item. Crucial para planejamento de compras e produção.

30. **User_Text**: Campo de texto livre para o usuário adicionar informações adicionais sobre o item.

31. **U_SKILL_CEST**: Código Especificador da Substituição Tributária (CEST). Relacionado à tributação e compliance.

32. **U_SKILL_LisSer**: Lista de serviços associados ao item, se aplicável. Pode ser usada para definir serviços adicionais ligados ao produto.

33. **U_SKILL_SerMun**: Código de serviço municipal, relacionado à tributação local do item.

### Relação o Módulo de Compras

&emsp;&emsp;Na área de Compras, os Dados Mestres desempenham um papel vital, eles permitem que os compradores acessem informações precisas e atualizadas sobre os itens, como preços, condições de compra e dados de fornecedores. 

#### Impacto das Colunas Vazias

&emsp;&emsp;Colunas vazias na tabela de Dados Mestres podem ter impactos significativos no dia a dia e nos processos do módulo de compras, afetando tanto a eficiência operacional quanto a precisão das operações. A seguir, é explicado o impacto de cada grupo de colunas comumente encontradas vazias:

### 1. **Campos de Identificação e Descrição (ex.: ItemCode, ItemName, ForeignName)**
   - **Impacto**: Se esses campos estiverem vazios, o item pode não ser identificado corretamente no sistema, dificultando o processo de compra, rastreamento e análise. Isso pode levar a erros em pedidos, atrasos e até falhas na identificação de produtos durante as auditorias.

### 2. **Campos de Classificação e Agrupamento (ex.: ItemsGroupCode, ItemType)**
   - **Impacto**: Colunas vazias nesses campos podem causar problemas na categorização de itens, dificultando a aplicação de políticas de compras ou a análise de dados por grupo de produtos. Isso pode levar a uma gestão ineficaz de inventário e ao aumento dos custos operacionais.

### 3. **Campos de Controle de Estoque (ex.: PurchaseItem, SalesItem, InventoryItem)**
   - **Impacto**: Se o campo `PurchaseItem` estiver vazio, o sistema pode não reconhecer o item como comprável, impossibilitando a criação de pedidos de compra. Já o campo `InventoryItem` vazio pode impedir o controle adequado de estoque, resultando em falta de produtos ou excesso de estoque.

### 4. **Campos Relacionados ao Fornecedor e Método de Aquisição (ex.: Manufacturer, ProcurementMethod)**
   - **Impacto**: Colunas vazias relacionadas ao fabricante e ao método de aquisição podem levar à falta de informações críticas sobre como e de onde obter o item. Isso pode causar atrasos nos pedidos, aumentar o tempo de entrega e resultar em escolhas de fornecedores menos eficientes.

### 5. **Campos Financeiros e Contábeis (ex.: GLMethod, EvaluationSystem)**
   - **Impacto**: A ausência de informações nesses campos pode comprometer a correta contabilização de transações, resultando em inconsistências nos registros financeiros e dificuldade em realizar análises de custos e margens de lucro.

### 6. **Campos de Planejamento e Reabastecimento (ex.: PlanningSystem, MaxInventory, LeadTime)**
   - **Impacto**: Se campos relacionados ao planejamento e reabastecimento estiverem vazios, isso pode causar falhas no planejamento de compras e na gestão de estoque. O sistema pode não conseguir prever adequadamente as necessidades de reabastecimento, levando a faltas ou excessos de estoque.

### 7. **Campos de Compliance e Regulamentação (ex.: U_SKILL_CEST, U_SKILL_LisSer, U_SKILL_SerMun)**
   - **Impacto**: Campos vazios relacionados a compliance podem resultar em problemas com a conformidade fiscal e regulatória, o que pode levar a multas e complicações legais. Além disso, a ausência desses dados pode comprometer a correta tributação nas compras e vendas.

### 8. **Campos de Configuração e Parâmetros (ex.: OrderMultiple, MinOrderQuantity)**
   - **Impacto**: Campos vazios nesses parâmetros podem levar à criação de pedidos de compra em quantidades não ideais, resultando em custos adicionais, desperdício ou problemas de abastecimento.

### 9. **Campos de Auditoria e Controle (ex.: CreatedBy, CreateDate, UpdDate)**
   - **Impacto**: A falta de preenchimento desses campos pode dificultar o rastreamento de mudanças e a identificação de responsabilidades, comprometendo a integridade dos dados e complicando auditorias internas.

### Impactos Gerais:
- **Ineficiência Operacional**: Processos manuais, retrabalho e atrasos na cadeia de suprimentos.
- **Aumento de Custos**: Compras não otimizadas, excesso ou ruptura de estoque.
- **Problemas de Conformidade**: Risco de multas e penalidades devido à falta de dados fiscais ou regulamentares.
- **Dificuldade em Análises e Decisões**: Informações incompletas dificultam a análise e a tomada de decisões estratégicas.

&emsp;&emsp;Preencher adequadamente todas as colunas com informações precisas é importante para garantir que o sistema funcione de maneira eficiente e que os processos sejam executados sem problemas.
