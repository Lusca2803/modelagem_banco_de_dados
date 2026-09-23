# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

Este arquivo é o esqueleto do README.md do repositório GitHub do seu grupo. Preencha cada seção abaixo. Não apague os títulos — apenas substitua as instruções em itálico pelo conteúdo do seu projeto. O DER é anexado separadamente ao repositório (em imagem), mas sua justificativa entra neste README.

A organização escolhida pode ser de qualquer natureza: empresa com fins lucrativos (livraria, lanchonete, pet shop), ONG, associação comunitária, cooperativa, instituições religiosas/comunitárias como igrejas, terreiros de religiões de matriz africana (candomblé, umbanda) ou outras. O que muda de um tipo para outro são os processos e as regras específicas — a estrutura do trabalho (levantamento de requisitos, modelagem conceitual, DER) é a mesma para todas. Termos como "empresa" e "negócio" usados abaixo devem ser lidos de forma ampla, no sentido técnico de modelagem de dados (ex.: "regras de negócio" = regras de funcionamento da organização, seja ela comercial, religiosa ou social).

Importante: a organização precisa existir de fato — não é permitido inventar uma organização fictícia. O levantamento de requisitos e regras de negócio deve ser feito por meio de pesquisa de campo na própria organização (visitas, entrevistas com responsáveis, observação dos processos reais), então o grupo só deve escolher uma organização à qual realmente tenha acesso. Ao escolher, tomem cuidado com o porte: nem tão pequena que não gere dados suficiente para o trabalho (poucos processos, poucas entidades), nem tão grande/complexa que fique inviável de modelar nesta primeira etapa do curso.

## Metadados

| Nome | RGM |
|---|---|
| LUCAS HENRIQUE ROQUE CRUZ | 4717892-2 |
| RENAN CORREIA FERREIRA DE SOUSA | 4702274-4 |
| VINICIUS SCHERER DI GIORNO | 4702823-8 |

## 1. Caracterização da Organização

**Nome e natureza da organização:** Waldesa Comércio, empresa com fins lucrativos que atua no comércio varejista de materiais elétricos e representações comerciais.

**Histórico:** A empresa existe desde 1966. Começou suas atividades focada no comércio varejista de materiais elétricos e representações comerciais, estabelecendo uma forte presença regional na Grande São Paulo, com destaque para a sede e filiais em cidades como Mogi das Cruzes e na tradicional região eletroeletrônica da Santa Ifigênia, na capital paulista.

**Contexto e porte:** A unidade da Santa Ifigênia possui cerca de 40 funcionários e realiza aproximadamente 40 a 50 vendas por dia, contando atendimentos presenciais (balcão), on-line e por plataformas de e-commerce.

**Meios de registro de informações:** As informações principais estão registradas em sistema, e pelo menos 90% também são registradas em planilhas, além do uso de WhatsApp e anotações manuais.

**Problemas e necessidades identificados:** O principal problema encontrado foi o controle de estoque. Muitas peças são registradas manualmente com quantidades incorretas, causando os chamados "furos de estoque". Como solução paliativa, a empresa costuma realizar contagens de estoque anuais, mas ainda não possui uma solução definitiva para o problema.

**Justificativa da escolha:** A empresa foi escolhida por ser uma organização real e acessível ao grupo, além de possuir processos que podem ser analisados e melhorados através da tecnologia.

**Evidências da organização:**

- Site: https://www.waldesa.com.br/
- Instagram: https://www.instagram.com/waldesaoficial?stkn=amJsaHRrcGN5eHB5
- As fotos da empresa serão adicionadas após autorização. Também será buscado um contato oficial para o acompanhamento do projeto (follow-up).

## 2. Processos de Negócio

### Principais processos mapeados
- Cadastro de clientes;
- Vendas;
- Entrada e controle de estoque;
- Separação de pedidos;
- Retirada de pedidos;
- Entregas.

### Responsáveis

| Processo | Responsável |
|---|---|
| Cadastro | Vendedor |
| Vendas | Vendedor |
| Estoque | Setor de Compras e Estoquistas |
| Entregas | Estoquistas, vendedores e motorista |

### Como os processos funcionam

**Cadastro e Vendas:** Vendedor pede dados do cliente como CPF/CNPJ, inscrição estadual, nome, data de nascimento, preenchendo tudo que o sistema pede; abre um pedido ou orçamento, procura pela descrição da peça, onde aparece se tem disponível em estoque ou não, seleciona a peça e quantidade, adiciona ao pedido, finaliza o processo e emite o pedido.

**Estoque:** O processo começa pela compra dos produtos. Quando as peças chegam, as notas fiscais são digitalizadas e todos os produtos são colocados no sistema, cada um identificado por seu código. Depois, os produtos são repostos em seus locais corretos nas prateleiras do estoque. Após feito o pedido no balcão de vendas, o vendedor informa pelo grupo do Teams o número do pedido, os separadores/estoquistas entram na aba "emissão de pedidos", abrem o pedido e tiram uma impressão para fazer a separação. Após isso, apenas informam o vendedor no grupo que está separado.

**Entrega:** Existe um grupo na plataforma Teams, onde os vendedores enviam seus pedidos junto com a forma como cada cliente irá receber: retirada na loja, entrega pela própria empresa ou envio pelos Correios. A partir daí, o responsável pelo estoque separa os pedidos de entrega e os organiza em uma planilha. No final do dia, o motorista tem o carro carregado com todas as notas fiscais e os endereços, e as entregas são realizadas no dia seguinte.

### O que pode dar errado?
A falta de estoque, principalmente por conta dos chamados "furos de estoque", além de os separadores não se comunicarem com os vendedores sobre a separação do pedido e o cliente esperar mais do que deveria.

### O que acontece após os processos?
- **Cadastro:** O cliente tem todos os seus dados armazenados no sistema.
- **Venda:** Para clientes já cadastrados, é gerada a nota fiscal; para clientes sem cadastro, é gerado o cupom fiscal.
- **Entrega:** Não gera nenhum documento adicional além da nota fiscal já emitida na venda.

### Como os processos se conectam?
- **Cadastro:** Conecta-se ao sistema, onde ficam registradas todas as compras do cliente, orçamentos gerados, notas fiscais e pedidos.
- **Vendas:** Conecta-se ao estoque, pois tudo o que está em um pedido é retirado automaticamente do sistema, com a redução da quantidade de peças disponíveis.
- **Entregas:** Estão diretamente ligadas às vendas, já que fazem parte do mesmo fluxo. Porém, todas as entregas finalizadas também ficam registradas em um grupo de WhatsApp.

### Etapa que poderia ser automatizada
A finalização do pedido no sistema; o registro e confirmação de entregas e retiradas.

## 3. Requisitos do Sistema

### 3.1 Requisitos Funcionais

- **RF01:** Permitir cadastrar clientes.
- **RF02:** Permitir cadastrar produtos.
- **RF03:** Registrar vendas.
- **RF04:** Consultar o estoque.
- **RF05:** Atualizar o estoque após uma venda.
- **RF06:** Registrar entrada de produtos.
- **RF07:** Relacionar a entrada com a nota fiscal.
- **RF08:** Registrar pedidos.
- **RF09:** Informar a forma de recebimento do pedido.
- **RF10:** Registrar entregas.
- **RF11:** Consultar movimentações do estoque.
- **RF12:** Identificar divergências no estoque.
- **RF13:** O sistema deve atualizar automaticamente os saldos de estoque a partir do registro de vendas e de entradas vinculadas a notas fiscais.
- **RF14:** O sistema deve permitir a localização do cadastro do cliente mediante nome, CPF/CNPJ ou número de pedidos previamente realizados.
- **RF15:** O sistema deve permitir a validação do status de pagamento associado ao pedido.

### 3.2 Requisitos Não Funcionais

- **RNF01:** O sistema deve ser fácil de utilizar.
- **RNF02:** Deve possuir controle de acesso.
- **RNF03:** Deve apresentar as informações rapidamente.
- **RNF04:** Os dados devem ser protegidos.
- **RNF05:** Deve evitar registros incorretos ou duplicados.
- **RNF06:** Deve possuir backup dos dados.
- **RNF07:** Deve permitir o crescimento da quantidade de produtos, clientes e vendas.
- **RNF08:** Deve restringir a visualização das informações conforme o setor do usuário, sendo a gerência o único perfil com acesso a todas as informações do sistema.
- **RNF09:** Deve impedir que os dados dos clientes sejam copiados ou compartilhados sem autorização.
- **RNF10:** Deve funcionar off-line ao menos para o registro de saída de peças em pedidos.
- **RNF11:** Deve garantir estabilidade e disponibilidade do sistema, principalmente nas semanas de pagamento e vale.

### 3.3 Levantamento de Requisitos com a Organização (Sistema Ideal)

Em conversa com a organização sobre como seria um sistema ideal, foram levantados os seguintes pontos:

- **Funcionalidades obrigatórias:** O sistema precisaria agrupar automaticamente todos os materiais que chegam e que saem do estoque, atualizando as quantidades sem a necessidade de lançamentos manuais, facilitando o ajuste de estoque e tornando o processo o menos manual possível: finalização de pedido do estoque; confirmação de entrega dos motoristas para os vendedores.
- **Perfis de uso:** A ideia é que todos os setores da empresa sejam beneficiados pelo sistema, como atendente, gerente, administrador, entre outros.
- **Visibilidade das informações:** Cada setor deve visualizar apenas as informações referentes ao que envolve seu próprio trabalho. A gerência é o único perfil com acesso a todas as informações, além dos encarregados de cada setor, que terão acesso ao que é necessário para o funcionamento de sua área de atuação.
- **Segurança e privacidade:** Os dados dos clientes precisam ser protegidos, sem possibilidade de serem copiados ou compartilhados sem autorização.
- **Funcionamento off-line:** É importante que ao menos a parte de saída de peças em pedidos funcione mesmo sem conexão com a internet. Não há exigência de que o sistema todo funcione off-line.
- **Momentos críticos:** O sistema não pode falhar principalmente nas semanas de pagamento e vale, quando a movimentação é maior.

## 4. Regras de Negócio

### Regras operacionais
- Cada produto deve possuir um código (vem da distribuidora).
- Produtos recebidos devem ser registrados no sistema.
- A entrada deve estar relacionada à nota fiscal.
- O estoque deve ser atualizado nas entradas e saídas.
- Uma venda deve possuir os produtos e quantidades vendidos.
- Todo pedido deve possuir uma forma de recebimento.
- Pedidos de entrega devem ser separados antes de serem enviados ao motorista.
- As entregas realizadas devem ser registradas.
- **É vedada a liberação de qualquer pedido sem que o respectivo pagamento tenha sido previamente confirmado.**
- A emissão de nota fiscal constitui exigência legal a ser observada nas operações de venda aplicáveis.

### Restrições organizacionais
A empresa utiliza sistema, planilhas, Teams, WhatsApp e anotações. A utilização de vários meios pode dificultar a organização das informações.

O registro manual dos produtos também pode causar erros e contribuir para os furos de estoque.

### Observações adicionais sobre as regras
Atualmente não há limites definidos de quantidade, valor ou tempo em nenhum dos processos, nem regras não escritas que sejam seguidas apenas na prática. As regras vigentes são as descritas acima. Essas regras podem vir a mudar futuramente, conforme forem identificadas novas falhas ou problemas no funcionamento e na forma como os processos são realizados.

## 5. Dicionário de Dados Conceitual (Preliminar)

### CLIENTE
```text
CLIENTE = @ID_CLIENTE + NM_CLIENTE + [CD_CPF | CD_CNPJ] + (DT_NASCIMENTO) + (DT_ABERTURA) + {NR_TELEFONE} + (DS_EMAIL) + DS_ENDERECO + CD_CEP + IN_ATIVO
```
* **Leitura da Notação:** `@ID_CLIENTE` é o identificador único da entidade. `NM_CLIENTE`, a escolha entre `CPF` ou `CNPJ`, `DS_ENDERECO`, `CD_CEP` e `IN_ATIVO` são obrigatórios. `NR_TELEFONE` permite múltiplos contatos.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_cliente** | Identificação exclusiva do cliente | Único (Chave Primária). Tipo: `integer`. |
| **nome** | Nome completo (PF) ou razão social (PJ) | Obrigatório. Tipo: `varchar(120)`. |
| **cpf_cnpj** | Documento de identificação fiscal | Obrigatório (Escolha exclusiva: CPF para PF ou CNPJ para PJ). Único. Tipo: `varchar(18)`. |
| **data_nascimento** | Data de nascimento (PF) ou fundação (PJ) | Opcional. Tipo: `date`. |
| **telefone** | Telefone de contato com DDD | Obrigatório. Permite múltiplas ocorrências (iteração). Tipo: `varchar(20)`. |
| **email** | Endereço de correio eletrônico | Opcional. Deve possuir formato válido. Tipo: `varchar(100)`. |
| **endereco** | Logradouro, número, bairro e cidade | Obrigatório. Tipo: `varchar(200)`. |
| **cep** | Código de Endereçamento Postal | Obrigatório. Padrão 8 dígitos. Tipo: `varchar(9)`. |
| **status_ativo** | Indicador de cadastro ativo | Obrigatório. Domínio: 'S' (Ativo) ou 'N' (Inativo). Tipo: `varchar(1)`. |

---

### VENDEDOR
```text
VENDEDOR = @ID_VENDEDOR + NM_VENDEDOR + CD_MATRICULA + IN_ATIVO
```
* **Leitura da Notação:** `@ID_VENDEDOR` identifica exclusivamente o vendedor. Todos os campos são de preenchimento obrigatório no cadastro do funcionário.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_vendedor** | Identificação exclusiva do vendedor | Único (Chave Primária). Tipo: `integer`. |
| **nome** | Nome completo do vendedor/atendente | Obrigatório. Tipo: `varchar(120)`. |
| **matricula** | Código funcional de matrícula | Obrigatório. Único na empresa. Tipo: `varchar(20)`. |
| **status_ativo** | Indicador de situação funcional | Obrigatório. Domínio: 'S' (Ativo) ou 'N' (Desligado). Tipo: `varchar(1)`. |

---

### PEDIDO
```text
PEDIDO = @ID_PEDIDO + DT_PEDIDO + TP_STATUS + [TP_DINHEIRO | TP_PIX | TP_CARTAO | TP_BOLETO]
```
* **Leitura da Notação:** `@ID_PEDIDO` identifica o pedido. Exige a escolha obrigatória entre uma das formas de recebimento aceitas.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_pedido** | Identificação exclusiva do pedido | Único (Chave Primária). Tipo: `integer`. |
| **data_pedido** | Data e horário de emissão do pedido | Obrigatório. Gerado automaticamente pelo sistema. Tipo: `timestamp`. |
| **status_pedido** | Situação do processamento do pedido | Obrigatório. Domínio: 'Pendente', 'Aprovado', 'Cancelado'. Tipo: `varchar(20)`. |
| **forma_recebimento** | Meio de pagamento selecionado | Obrigatório (Escolha exclusiva: Dinheiro, Pix, Cartão ou Boleto). Tipo: `varchar(20)`. |

---

### PRODUTO
```text
PRODUTO = @ID_PRODUTO + CD_PRODUTO + DS_PRODUTO + VL_PRECO + DS_UNIDADE_MEDIDA + IN_ATIVO
```
* **Leitura da Notação:** `@ID_PRODUTO` é a chave primária. `CD_PRODUTO` representa o SKU do item. Todos os atributos são obrigatórios para comercialização.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_produto** | Identificação exclusiva do produto | Único (Chave Primária). Tipo: `integer`. |
| **codigo_sku** | Código comercial / SKU ou código de barras | Obrigatório. Único. Tipo: `varchar(30)`. |
| **descricao** | Nome comercial e descrição detalhada do produto | Obrigatório. Tipo: `varchar(150)`. |
| **preco** | Preço unitário de venda cadastrado | Obrigatório. Valor numérico maior que zero. Tipo: `numeric(10,2)`. |
| **unidade_medida** | Unidade de comercialização | Obrigatório. Domínio: 'UN', 'KG', 'CX', 'PC'. Tipo: `varchar(10)`. |
| **status_ativo** | Indicador de disponibilidade no catálogo | Obrigatório. Domínio: 'S' (Ativo) ou 'N' (Inativo). Tipo: `varchar(1)`. |

---

### ESTOQUE
```text
ESTOQUE = @ID_ESTOQUE + QT_SALDO + DS_LOCALIZACAO + DT_ULTIMA_ATUALIZACAO
```
* **Leitura da Notação:** `@ID_ESTOQUE` identifica o registro de saldo e controle físico dos itens no almoxarifado.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_estoque** | Identificação exclusiva do registro de estoque | Único (Chave Primária). Tipo: `integer`. |
| **quantidade_saldo** | Saldo físico atual disponível em estoque | Obrigatório. Valor inteiro maior ou igual a zero. Tipo: `integer`. |
| **localizacao** | Localização física no galpão/loja | Obrigatório. Identifica corredor/prateleira. Tipo: `varchar(50)`. |
| **data_atualizacao** | Data e hora da última movimentação | Obrigatório. Atualizado a cada entrada/saída. Tipo: `timestamp`. |

---

### VENDA
```text
VENDA = @ID_VENDA + DT_VENDA + VL_TOTAL
```
* **Leitura da Notação:** `@ID_VENDA` representa a efetivação comercial e faturamento da transação.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_venda** | Identificação exclusiva da transação de venda | Único (Chave Primária). Tipo: `integer`. |
| **data_venda** | Data e hora em que a venda foi finalizada | Obrigatório. Tipo: `timestamp`. |
| **valor_total** | Somatório final do valor dos itens comercializados | Obrigatório. Calculado a partir dos produtos. Tipo: `numeric(10,2)`. |

---

### NOTA_FISCAL
```text
NOTA_FISCAL = @ID_NOTA + CD_NUMERO_NOTA + CD_CHAVE_ACESSO + DT_EMISSAO + NM_FORNECEDOR
```
* **Leitura da Notação:** `@ID_NOTA` identifica o documento fiscal oficial de entrada de mercadorias.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_nota** | Identificação exclusiva do registro da Nota Fiscal | Único (Chave Primária). Tipo: `integer`. |
| **numero_nota** | Número oficial impresso no documento fiscal | Obrigatório. Tipo: `varchar(30)`. |
| **chave_acesso** | Chave eletrônica de acesso da NF-e (SEFAZ) | Obrigatório. Código único de 44 dígitos. Tipo: `varchar(44)`. |
| **data_emissao** | Data de emissão do documento pelo fornecedor | Obrigatório. Tipo: `date`. |
| **fornecedor** | Razão social ou nome do fornecedor emissor | Obrigatório. Tipo: `varchar(150)`. |

---

### MOTORISTA
```text
MOTORISTA = @ID_MOTORISTA + NM_MOTORISTA + ({NR_TELEFONE}) + IN_ATIVO
```
* **Leitura da Notação:** `@ID_MOTORISTA` é o identificador exclusivo do motorista. `NR_TELEFONE` é opcional e iterativo para contato.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_motorista** | Identificação exclusiva do motorista | Único (Chave Primária). Tipo: `integer`. |
| **nome** | Nome completo do motorista | Obrigatório. Tipo: `varchar(120)`. |
| **telefone** | Telefone móvel para contato logístico | Opcional (iteração). Tipo: `varchar(20)`. |
| **status_ativo** | Indicador de situação operacional | Obrigatório. Domínio: 'S' (Ativo) ou 'N' (Inativo). Tipo: `varchar(1)`. |

---

### ENTREGA
```text
ENTREGA = @ID_ENTREGA + DT_PREVISTA + (DT_ENTREGA) + TP_STATUS_ENTREGA + DS_ENDERECO_ENTREGA
```
* **Leitura da Notação:** `@ID_ENTREGA` é o identificador logístico. `DT_ENTREGA` é opcional pois é preenchida apenas após a conclusão da entrega.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_entrega** | Identificação exclusiva da ordem de entrega | Único (Chave Primária). Tipo: `integer`. |
| **data_prevista** | Data limite prevista para a entrega | Obrigatório. Tipo: `date`. |
| **data_entrega** | Data e hora efetivas do descarregamento | Opcional (preenchido após entrega). Tipo: `timestamp`. |
| **status_entrega** | Situação logística do transporte | Obrigatório. Domínio: 'Pendente', 'Em Trânsito', 'Entregue'. Tipo: `varchar(20)`. |
| **endereco_entrega** | Endereço completo de destino | Obrigatório. Tipo: `varchar(200)`. |

---

### COMPRA
```text
COMPRA = @ID_COMPRA + DT_COMPRA + (ID_NOTA) + NM_FORNECEDOR
```
* **Leitura da Notação:** `@ID_COMPRA` identifica o registro da operação de compra/entrada de produtos.

| Atributo | Descrição | Regra de negócio associada |
| :--- | :--- | :--- |
| **id_compra** | Identificação | Único (Chave Primária). Tipo: `integer`. |
| **data_compra** | Data de entrada | Obrigatória. Tipo: `timestamp`. |
| **id_nota** | Nota fiscal | Relacionada à entrada. Associação com o documento fiscal. Tipo: `integer`. |
| **fornecedor** | Fornecedor | Identifica a origem. Razão social do fornecedor. Tipo: `varchar(150)`. |

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

### Entidades reconhecidas
As principais entidades são:

`Cliente`, `Vendedor`, `Pedido`, `Produto`, `Estoque`, `Venda`, `Nota_Fiscal`, `Motorista`, `Entrega` e `Compra`

Elas foram escolhidas por representarem os principais processos identificados na empresa.

De acordo com o levantamento feito junto à organização, os únicos tipos de "pessoa" que realmente precisam ser cadastrados no sistema são Clientes e Funcionários. Este último grupo engloba os perfis de Vendedor, Estoquista e Motorista já identificados nos processos mapeados.

### Atributos e classificações
Cada entidade possui atributos relacionados às informações que precisam ser armazenadas, como identificação, datas, quantidades, valores e informações de contato.

### Relacionamentos pertinentes
- Cliente realiza vendas e pedidos.
- Vendedor realiza vendas.
- Venda possui itens.
- Produto participa das vendas.
- Produto possui controle de estoque.
- Entrada possui itens.
- Produto participa das entradas.
- Entrada está relacionada à nota fiscal.
- Pedido pode possuir uma entrega.
- Motorista realiza entregas.

### Restrições e políticas organizacionais
O modelo considera principalmente o controle das entradas e saídas de produtos, buscando manter o estoque atualizado e diminuir os furos de estoque.

## 7. Diagrama Entidade-Relacionamento (DER)

O DER será anexado ao repositório em formato de imagem.

O diagrama deverá representar:
- Entidades;
- Atributos;
- Relacionamentos;
- Cardinalidades.

O modelo será baseado nos processos observados na empresa e dará atenção principalmente ao controle de estoque.

## 8. Justificativa Técnica

As entidades foram escolhidas com base nos processos observados na empresa.

Produto e Estoque são importantes para representar o controle das peças. `Venda` e `Item_Venda` foram separados porque uma venda pode possuir vários produtos.

A mesma ideia foi utilizada em `Compra`, já que uma entrada pode possuir vários produtos.

`Cliente` e `Vendedor` ajudam a identificar quem participa das vendas, enquanto `Pedido`, `Entrega` e `Motorista` representam o processo de entrega.

A modelagem também considera o problema dos furos de estoque, permitindo que as entradas e saídas dos produtos sejam controladas.

Como alternativa, cogitou-se a manutenção dos registros exclusivamente em planilhas, bem como a concentração das informações em um número reduzido de entidades genéricas. Tal abordagem foi, todavia, descartada por não viabilizar o rastreamento individualizado de entradas, saídas e itens de cada movimentação, o que constitui, precisamente, a causa dos "furos de estoque" atualmente enfrentados pela organização. Optou-se, portanto, pela separação em entidades específicas (`Venda/Item_Venda` e `Compra`), por proporcionar a granularidade necessária à auditoria individualizada de cada produto movimentado.

No que concerne às cardinalidades, sua definição decorreu da observação criteriosa da forma como os processos efetivamente se realizam na organização. A título de exemplo, a cardinalidade **Cliente (1) — (N) Venda** justifica-se pelo fato de um cliente poder realizar múltiplas compras ao longo do tempo, ao passo que cada venda encontra-se vinculada a um único cliente registrado. De modo análogo, a cardinalidade **Pedido (1) — (N) Item_Venda** justifica-se porquanto um mesmo pedido pode compreender diversos produtos, sendo, contudo, cada item de venda associado a um único pedido.

Nesta etapa da modelagem, deliberou-se pela **omissão das Chaves Estrangeiras (FKs)** no diagrama conceitual. Tal decisão observa o nível de abstração inerente ao Modelo Entidade-Relacionamento conceitual, cuja finalidade consiste em representar entidades, atributos e relacionamentos sob a perspectiva do negócio, sem antecipar decisões concernentes à implementação física, as quais serão devidamente tratadas nas etapas subsequentes de modelagem lógica e física do projeto.

Por derradeiro, optou-se pela manutenção de Cliente, Vendedor e Motorista como entidades distintas, em detrimento de sua unificação sob uma entidade genérica "Pessoa". Referida escolha justifica-se na medida em que cada um dos papéis mencionados possui atributos próprios (a exemplo da matrícula, no caso do Vendedor, e do CPF/CNPJ e da inscrição estadual, no caso do Cliente) e participa de relacionamentos e processos de negócio distintos no âmbito da organização, de modo que a adoção de uma entidade genérica demandaria número excessivo de atributos e relacionamentos opcionais, comprometendo a clareza e a precisão semântica do modelo.

## 9. Uso de Inteligência Artificial

Foi utilizada a ferramenta ChatGPT para auxiliar na organização das informações e na estruturação do README.

| Item | O que registrar |
|---|---|
| Ferramenta e etapa | ChatGPT — organização do trabalho e revisão do texto. |
| Motivação | Ajudar a organizar as informações coletadas. |
| Prompt(s) utilizados | Foi solicitado que as informações da pesquisa fossem organizadas de acordo com o modelo de README da atividade. |
| Resposta recebida | A IA ajudou a organizar processos, requisitos, regras e entidades. |
| Fontes consultadas e verificadas | Informações obtidas através da pesquisa realizada na organização e canais oficiais da empresa. |
| Trechos rejeitados ou corrigidos | Informações não confirmadas pela empresa serão revisadas pelo grupo. |
| Justificativa da escolha final | A IA foi utilizada apenas como apoio, mantendo as informações coletadas pelo grupo como base. |
| Reflexão crítica | Algumas sugestões da IA podem não representar exatamente a realidade da empresa, por isso precisam ser conferidas pelo grupo. |

### Critérios Atitudinais
Os critérios serão avaliados através da avaliação 360º entre os integrantes e pelo histórico de commits do GitHub.

- **Participação:** participação nas decisões do grupo.
- **Comprometimento:** cumprimento das tarefas.
- **Colaboração:** trabalho em equipe.
- **Autonomia:** busca por soluções e melhorias.

### Fotos do local

**Foto ou print de registros**
Não tivemos autorização da empresa para usar imagens de planilhas, cadernos etc., pois continham dados pessoais de muitos clientes.

**Nome, cargo e contato do responsável**
Kauã Steter de Souza — kauasteter06@gmail.com — Suporte Técnico Júnior

**Link do Google Maps / site / rede social**
- https://maps.google.com/maps/place//data=!4m2!3m1!1s0x94ce591423db0ce7:0xa1f08048818de70a?entry=s&sa=X&ved=2ahUKEwi6tY2AooOXAxULObkGHawlNj8Q4kB6BAgZEAA&hl=pt
- https://www.waldesa.com.br/
- https://www.instagram.com/waldesaoficial?stkn=amJsaHRrcGN5eHB5
