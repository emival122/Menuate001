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

![Imagem do Circuito](Lógico.png)


O diagrama representa um banco de dados para um sistema de pedidos em restaurantes. Ele contém as entidades Cliente, Restaurante, MenuMate e Sistema de Pagamento, conectadas por relacionamentos.
•	Cliente armazena informações do usuário, como nome, e-mail e senha.
•	Restaurante possui dados sobre comidas e bebidas disponíveis.
•	MenuMate gerencia promoções, sugestões e o cardápio.
•	Sistema de Pagamento contém métodos e valores das transações.
Os relacionamentos mostram que clientes interagem com restaurantes e fazem pedidos através do menu, enquanto o sistema de pagamento processa as compras.


