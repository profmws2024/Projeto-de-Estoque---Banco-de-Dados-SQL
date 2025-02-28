# Sistema de Controle de Estoque em SQL

Este é um projeto simples de controle de estoque utilizando SQL. Ele permite gerenciar produtos, categorias, fornecedores e transações (compras e vendas) dentro de um banco de dados. O sistema é projetado para facilitar a gestão de inventário em um ambiente de negócios, registrando entradas e saídas de produtos e realizando consultas detalhadas.

## Funcionalidades

- **Cadastro de Categorias**: Permite registrar diferentes categorias para os produtos (ex: Eletrônicos, Alimentos, etc.).
- **Cadastro de Fornecedores**: Armazena informações sobre os fornecedores dos produtos.
- **Cadastro de Produtos**: Registra os produtos com informações como nome, descrição, preço e quantidade no estoque.
- **Gestão de Transações**: Registra transações de compra e venda, controlando as quantidades de produtos no estoque.
- **Consultas SQL**: Fornece consultas para extrair informações úteis, como o estoque atual, histórico de transações e vendas por produto.

## Estrutura do Banco de Dados

O banco de dados possui as seguintes tabelas:

1. **Categorias**: Armazena as categorias dos produtos.
    - `id_categoria`: Identificador único da categoria.
    - `nome_categoria`: Nome da categoria (ex: "Eletrônicos", "Alimentos").
  
2. **Fornecedores**: Contém informações sobre os fornecedores.
    - `id_fornecedor`: Identificador único do fornecedor.
    - `nome_fornecedor`: Nome do fornecedor.
    - `telefone_fornecedor`: Telefone do fornecedor.
    - `endereco_fornecedor`: Endereço do fornecedor.

3. **Produtos**: Armazena os produtos no estoque.
    - `id_produto`: Identificador único do produto.
    - `nome_produto`: Nome do produto.
    - `descricao_produto`: Descrição do produto.
    - `quantidade_estoque`: Quantidade do produto no estoque.
    - `preco_unitario`: Preço unitário do produto.
    - `id_categoria`: Relacionamento com a tabela de categorias.
    - `id_fornecedor`: Relacionamento com a tabela de fornecedores.

4. **Transações**: Registra as transações de compra e venda.
    - `id_transacao`: Identificador único da transação.
    - `tipo_transacao`: Tipo de transação (compra ou venda).
    - `data_transacao`: Data da transação.
    - `id_produto`: Relacionamento com a tabela de produtos.
    - `quantidade`: Quantidade de produtos movimentados.
    - `preco_unitario`: Preço unitário no momento da transação.
    - `valor_total`: Cálculo do valor total da transação.

## Como Rodar o Projeto

Para rodar este sistema, siga os passos abaixo:

1. **Criação do Banco de Dados**
   
   Execute o script SQL para criar o banco de dados e as tabelas. Você pode usar qualquer ferramenta de SQL (como MySQL Workbench, DBeaver ou PHPMyAdmin) ou executar diretamente no terminal.

   ```sql
   -- Criação do banco de dados
   CREATE DATABASE controle_estoque;

   -- Usando o banco de dados
   USE controle_estoque;

   -- Execute o script para criar as tabelas (conforme explicado acima)
