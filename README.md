# MVC

## Nome do Projeto: Abandono Zero

- Descrição:

&nbsp;&nbsp;&nbsp;&nbsp; Um projeto em parceria com o instituto INSPA busca entender as razões por trás da adoção, compra e abandono de animais de estimação. Estamos estão desenvolvendo uma aplicação web para coletar dados dos tutores e pesquisadores, visando preencher essa lacuna de conhecimento e reduzir o abandono de animais.

- Arquitetura: MVC (Model-View-Controller)

- Ferramenta de Diagramação: draw.io

### Modelos (Models):
#### Usuário e Administrador.

&nbsp;&nbsp;&nbsp;&nbsp; Como entidade, no usuário, coloquei ID, Nome, Email e Senha. Na parte dos formulário, adicionei além desses, as Perguntas. Já no modelo de administrador, escolhi usar Painel, Dados e Tabela.

### Controladores (Controllers):
#### Tela de Início:
- Funções do Controller: Gravar, Procurar e Validar.

&nbsp;&nbsp;&nbsp;&nbsp; Quando o usuário clica em "Gravar", o controlador chama o modelo correspondente para armazenar os dados. Ao clicar em "Procurar", o controlador solicita ao modelo os dados para exibição na view. E, durante a validação, o controlador interage com o modelo para verificar se os dados estão corretos.

- Views Relacionadas: A view correspondente exibirá os campos para entrada de dados e botões para as funções mencionadas.

#### Formulários:
- Funções do Controller: Armazenar e Listar.

&nbsp;&nbsp;&nbsp;&nbsp; Quando o usuário preenche o formulário e clica em "Armazenar", o controlador chama o modelo responsável, para salvar os dados. Para exibir os dados já armazenados, o controlador solicita ao modelo a lista correspondente.

- Views Relacionadas: Uma view será responsável por exibir o formulário para entrada de dados, enquanto outra exibirá a lista de dados armazenados.

#### Administrador:
- Funções do Controller: Gravar, Procurar, Filtrar e Baixar.

&nbsp;&nbsp;&nbsp;&nbsp; O controlador realiza operações semelhantes às da tela de início, como gravar e procurar dados. Ao filtrar dados, o controlador pode interagir com o modelo para obter resultados específicos com base nos critérios fornecidos. Para o download de dados, o controlador solicita ao modelo os dados desejados para serem disponibilizados ao usuário.

- Views Relacionadas: A view correspondente ao administrador exibirá opções para execução das funções mencionadas, além de exibir resultados de pesquisa e filtragem. O download será disponibilizado como opção ao usuário na view.

### Views (Views):
#### Lista das Views
Painel | Views 
--- | ---
Tela de Início | Header / Home / Sobre / Contatos / Imagens / Textos
Tela de Cadastro | Email / Senha / Confirmar Senha / Botão Cadastrar
Tela de Login | Email / Senha / Botão Entrar
Formulário | Perguntas direcionadas / Botão de responder / Botão de ir e voltar entre as perguntas / ID / Nul
Administrador | Relatório / Texto com informações / Tabela com dados / Botão Filtrar / Botão baixar dados / Imagens / Gráficos

### Infraestrutura:
&nbsp;&nbsp;&nbsp;&nbsp; Para armazenar as informações, utilizei como banco de dados o PostgreSQL. Além disso, por momento não decidimos nenhuma API (provavelmente usaremos uma API externa dos Correios). Para a programação, usaremos HTML, CSS e JavaScript, sendo React ou Angular como framework.

&nbsp;&nbsp;&nbsp;&nbsp; O banco de dados será acessado pelos modelos, realizando operações de leitura, escrita, atualização e exclusão. Quando aplicarmos a API, ela será "chamada" pelos controlados para autenticar os dados de endereço, por exemplo. E por fim, o view será aplicado por meio do front-end, através de requisições.

### Implicações da Arquitetura:
&nbsp;&nbsp;&nbsp;&nbsp; Por estar iniciando neste módulo e nunca ter realizado uma arquitetura de diagrama, podem ter alguns problemas de escabilidade e manutenção. Porém, realizei uma boa organização do diagrama, sendo de fácil entendimento o MVC. 
