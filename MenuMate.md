# DESCRIÇÃO DO PROJETO
O MenuMate é o aplicativo perfeito para quem busca praticidade, rapidez e variedade ao fazer pedidos online. Com uma interface intuitiva e de fácil navegação, o app permite que você encomende alimentos, bebidas, produtos de supermercado, de maneira rápida e segura.
# OBJETIVO DO PROJETO
  Facilitar o processo de compra e entrega de produtos e serviços ao usuário, proporcionando uma experiência rápida, prática e segura. Seu foco principal é conectar consumidores a fornecedores locais (restaurantes, lojas, mercados, farmácias, etc.), permitindo que façam pedidos de forma conveniente e recebam suas compras diretamente no local desejado, com a opção de pagamento online e rastreamento em tempo real.
# FERRAMENTAS A UTILIZAR
•	SQL Server: Gerenciamento de banco de dados dos clientes, pedidos e catálogos.

•	Netbeans: Desenvolvimento do aplicativo para Android e iOS.

•	Pencil: Criação de wireframes e protótipos da interface do usuário.

•	GitHub: Controle de versão e colaboração entre desenvolvedores.

•	Miro (Kanban): Organização e gestão das tarefas do projeto.

# FUNCIONALIDADES DO PROJETO

1.	Cadastro e Login do Usuário
o	Criação de conta com nome, e-mail, senha e telefone.

2.	Sugestões Inteligentes
o	Recomendações baseadas em pedidos anteriores.
o	Sugestão de promoções personalizadas.

3.	Gerenciamento de Pedidos
o	Adicionar/remover itens do carrinho.
o	Resumo detalhado do pedido.
o	Confirmação e rastreamento do pedido.

4.	Pagamento e Confirmação
o	Múltiplos métodos de pagamento (crédito, débito, Pix, etc.).
o	Validação automática do pagamento.

5.	Histórico de Pedidos
o	Consulta de pedidos anteriores.
o	Avaliação de fornecedores e produtos adquiridos.

6.	Promoções e Ofertas
o	Exibição de ofertas personalizadas.
o	Notificações sobre promoções em fornecedores favoritos.

7.	Perfil do Cliente
o	Edição de informações pessoais.
o	Gerenciamento de preferências de compra.
o	Personalização das notificações.

![Imagem do Circuito](Casodeuso.png)


  O diagrama representa um caso de uso do sistema MenuMate, mostrando as interações dos usuários com suas funcionalidades.
•	O Login permite acesso ao sistema, podendo incluir o Registro.
•	A função Visualizar pode ser estendida para Filtrar informações.
•	Gerenciar pedidos inclui ações como Finalizar pedido, que por sua vez pode estender o Pagamento.
•	O sistema também permite visualizar o Histórico de Pedidos e acessar Promoções.

![Imagem do Circuito](logico.png)


  O diagrama representa um banco de dados para um sistema de pedidos em restaurantes. Ele contém as entidades Cliente, Restaurante, MenuMate e Sistema de Pagamento, conectadas por relacionamentos.
•	Cliente armazena informações do usuário, como nome, e-mail e senha.
•	Restaurante possui dados sobre comidas e bebidas disponíveis.
•	MenuMate gerencia promoções, sugestões e o cardápio.
•	Sistema de Pagamento contém métodos e valores das transações.
Os relacionamentos mostram que clientes interagem com restaurantes e fazem pedidos através do menu, enquanto o sistema de pagamento processa as compras.

#	BANCO DE DADOS
2.1.1	Banco de Dados: SQL Server
O SQL Server foi escolhido como banco de dados para o projeto por várias razões, incluindo:
1.	Confiabilidade e Desempenho: O SQL Server é amplamente utilizado em projetos corporativos por ser robusto, escalável e garantir alto desempenho no gerenciamento de grandes volumes de dados.
2.	Segurança: Ele oferece recursos avançados de segurança, como criptografia de dados, auditoria e controle de acesso granular, essenciais para garantir a proteção de dados dos clientes e informações financeiras.
3.	Integração com o .NET: O SQL Server integra-se bem com o ambiente de desenvolvimento baseado em .NET (com o uso do NetBeans para o backend), facilitando a comunicação entre o aplicativo e o banco de dados.
4.	Facilidade de Administração: O SQL Server tem ferramentas de administração poderosas, como o SQL Server Management Studio (SSMS), para facilitar a gestão do banco de dados.
________________________________________
2.1.2	Dados a serem armazenados
A seguir, estão os dados principais que serão armazenados no banco de dados:
1.	Clientes:
o	ID do Cliente: Identificador único para cada cliente.
o	Nome: Nome do cliente.
o	Email: Endereço de e-mail do cliente (para envio de promoções, notificações, etc.).
o	Telefone: Número de telefone de contato.
o	Histórico de Pedidos: Registro dos itens pedidos pelo cliente, para personalizar recomendações.
2.	Cardápio:
o	ID do Prato/Bebida: Identificador único para cada item no cardápio.
o	Nome do Prato/Bebida: Nome do item.
o	Descrição: Descrição detalhada do prato ou bebida.
o	Categoria: Categoria do item (ex: entrada, prato principal, sobremesa, bebida).
o	Preço: Valor do item.
o	Imagem: URL da imagem do item no cardápio.
3.	Pedidos:
o	ID do Pedido: Identificador único do pedido.
o	ID do Cliente: Relacionamento com a tabela de clientes.
o	Data/Hora do Pedido: Quando o pedido foi feito.
o	Status do Pedido: Status do pedido (ex: em preparo, concluído, cancelado).
o	Itens do Pedido: Itens específicos do pedido (relacionamento com a tabela de cardápio).
4.	Promoções:
o	ID da Promoção: Identificador único da promoção.
o	Nome da Promoção: Nome ou descrição curta da promoção.
o	Tipo de Promoção: Tipo de desconto ou oferta (ex: "compre uma pizza, ganhe uma sobremesa").
o	Data de Início: Quando a promoção começa.
o	Data de Término: Quando a promoção termina.
o	Itens Associados: Quais pratos ou bebidas estão vinculados à promoção.
5.	Preferências de Cliente:
o	ID da Preferência: Identificador único para cada conjunto de preferências.
o	ID do Cliente: Relacionamento com a tabela de clientes.
o	Preferências Alimentares: Ex: vegano, sem lactose, etc.
o	Gosto Pessoal: Preferências como "gosta de pratos doces", "prefere algo leve", etc.
________________________________________

CREATE DATABASE CardápioDigitalPersonalizado;
USE CardápioDigitalPersonalizado;


CREATE TABLE Usuario (
    id_cliente INT PRIMARY KEY IDENTITY(1,1),
    email VARCHAR(255) NOT NULL UNIQUE,
    senha VARCHAR(100) NOT NULL,
    nome VARCHAR(100) NOT NULL,
    cpf CHAR(14) NOT NULL UNIQUE,
    data_nascimento DATE
);
CREATE TABLE Produtos(
id INT PRIMARY KEY IDENTITY(1,1),
nome VARCHAR(50) NOT NULL,
estoque INT NOT NULL,
preco FLOAT NOT NULL, 
tamanho INT,
)
GO
CREATE TABLE Clientes(
id INT PRIMARY KEY IDENTITY(1,1),
nome VARCHAR(45) NOT NULL,
cpf CHAR(15) NOT NULL,
email VARCHAR(45) NOT NULL,
telefone VARCHAR(45) NOT NULL
)
GO

CREATE TABLE CarrinhoCompra(
id INT PRIMARY KEY IDENTITY(1,1),
idcliente INT NOT NULL,
idproduto INT NOT NULL,
idvendedor INT NOT NULL,
quantidade INT NOT NULL,
formadepagamento VARCHAR(45),
valor FLOAT,
datavenda VARCHAR(10)
)
GO

INSERT INTO Usuario (email, senha, nome, cpf, data_nascimento) 
VALUES 
('emival.araujo@aluno.senai.br', 'emival2006', 'Emival Junior Pinheiro', '883.379.261-71', '2006-10-31');
GO


SELECT * FROM Usuario;

select * from produtos

select * from Clientes

select * from CarrinhoCompra


