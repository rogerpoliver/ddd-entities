# Atividade: Mapeando o domínio

<aside>
⚠️ Nessa atividade você irá ler uma conversa entre um Domain Expert e um desenvolvedor responsável por criar a aplicação. O seu objetivo é identificar as entidades e casos de uso para essa aplicação com base nessa conversa!

</aside>

Dev: Olá, obrigado por participar da entrevista. Para começar, quais são as principais funcionalidades que você gostaria de ver nesse sistema de gerenciamento de estoque?

Domain Expert: Precisamos de uma solução que nos permita rastrear cada produto individualmente, definir quantidades mínimas de estoque e receber alertas quando estivermos ficando sem um determinado produto. Também seria útil se pudéssemos visualizar o histórico de vendas e estoque para ajudar a tomarmos decisões futuras de compra.

Dev: Entendi. Você poderia me dar um exemplo de como você gostaria que a funcionalidade de rastreamento individual de produto funcionasse?

Domain Expert: Gostaríamos de poder atribuir um número de identificação único a cada produto, para podermos rastrear facilmente suas movimentações em nosso estoque. Também seria útil se pudéssemos adicionar informações extras, como tamanho e cor, para tornar o rastreamento ainda mais preciso.

Dev:  E quanto a funcionalidade de definição de quantidades mínimas de estoque, como você imaginaria isso funcionando?

Domain Expert: Gostaríamos de poder definir um limite mínimo para cada produto, de forma que pudéssemos receber um alerta quando o estoque estiver chegando próximo ao fim. Isso nos ajudaria a garantir que nunca fiquemos sem um produto popular e também nos permitiria fazer pedidos mais eficientes.

Dev: E como você gostaria de receber esses alertas? Por e-mail, SMS ou algum outro método?

Domain Expert: Seria ótimo se pudéssemos receber alertas por e-mail e também por meio de uma notificação em nosso sistema de gerenciamento de estoque.

Dev: Entendi. E quanto a funcionalidade de visualização de histórico de vendas e estoque, que tipo de informações você gostaria de ver?

Domain Expert: Gostaríamos de poder ver quantos produtos vendemos em um determinado período, qual foi o lucro gerado por produto e quais produtos estão vendendo melhor em cada período. Também seria útil se pudéssemos observar as tendências de estoque ao longo do tempo, para nos ajudar a tomar decisões de compra mais adequadas.

Dev:  Ok, e você tem alguma outra funcionalidade que gostaria de ver no sistema?

Domain Expert: Seria muito útil se o sistema pudesse nos permitir criar e gerenciar ordens de compra automaticamente, com base nas quantidades mínimas de estoque definidas e nas tendências de vendas. Também seria ótimo se pudéssemos integrar o sistema com nossos fornecedores, para que pudéssemos receber atualizações automáticas sobre os prazos de entrega de novas remessas.

## O que você deve procurar?

Dado o diálogo acima, você deve conseguir responder as seguintes perguntas:

- Quais as entidades de domínio?
- Quais as ações (casos de uso) que essa aplicação deve ter?

<hr>

# Respostas do Exercício

## 1. Quais as entidades de domínio?
As entidades principais identificadas no diálogo foram:

- **Produto** – Representa os itens armazenados no estoque.
- **Ordem de Compra** – Gerencia pedidos de reposição de estoque.
- **Ordem de Venda** – Registra as vendas realizadas.
- **Estoque** – Controla a quantidade disponível dos produtos.
- **Histórico de Movimentação do Estoque** – Registra todas as mudanças no estoque.
- **Vendedor** – Permite rastrear o desempenho individual de cada vendedor.
- **Fornecedor** – Para integração com sistemas externos e controle de entregas.

## 2. Quais as ações (casos de uso) que essa aplicação deve ter?
O sistema deve permitir as seguintes ações:

### **Gerenciamento de Produtos**
- Criar um produto com informações detalhadas.
- Definir um número mínimo de unidades no estoque.
- Atualizar o estoque ao comprar ou vender um produto.

### **Gerenciamento de Vendas**
- Registrar uma venda com código do produto, valor e data.
- Associar um vendedor à venda para análise de desempenho.
- Listar todas as vendas em um determinado período.
- Consultar quantas unidades de um produto foram vendidas.

### **Gerenciamento de Estoque**
- Consultar quantas unidades de um produto existem no estoque.
- Rastrear movimentações de um produto específico.
- Emitir alertas quando o estoque atingir o nível mínimo.

### **Gerenciamento de Compras**
- Criar uma ordem de compra quando o estoque estiver baixo.
- Atualizar o status da compra automaticamente via integração.
- Calcular tempo médio de entrega e ajustar níveis de estoque conforme necessidade.

### **Relatórios e Análises**
- Gerar relatório de vendas por período.
- Analisar desempenho de cada vendedor.
- Monitorar tendências de vendas e consumo de estoque.
- Ajustar estoque mínimo com base na demanda e tempo de reposição.
