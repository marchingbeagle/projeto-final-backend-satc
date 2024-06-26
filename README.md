# Medify

## Client Controller
Este controller lida com operações CRUD para a entidade Client usando uma API REST.
Componentes

    Anotações
        @RestController: Indica que a classe é um controller REST.
        @RequestMapping("/api/client"): Define o caminho base para as requisições.
        @Autowired: Injeta o serviço ClientService.

    Métodos do Controller
        getAllClient (@GetMapping): Retorna uma lista de todos os clientes.
        getClientById (@GetMapping("/{id}): Retorna um cliente específico pelo ID ou 404 se não encontrado.
        createClient (@PostMapping): Cria um novo cliente com os dados fornecidos e retorna o cliente criado com status 201.
        updateClient (@PutMapping("/{id}): Atualiza um cliente existente pelo ID ou retorna 404 se não encontrado.
        deleteClient (@DeleteMapping("/{id}): Remove um cliente pelo ID e retorna 204 se bem-sucedido ou 404 se não encontrado.

Entidade Client

Representa os dados do cliente:

    id, name, email, phoneNumber, cpf.

Possui um construtor que recebe um ClientDTO para criar instâncias a partir de dados de transferência (DTO).

## Employee Controller

Este controller lida com operações CRUD para a entidade Employee usando uma API REST.
Componentes

    Anotações
        @RestController: Indica que a classe é um controller REST.
        @RequestMapping("/api/employees"): Define o caminho base para as requisições.
        @Autowired: Injeta o serviço EmployeeService.

    Métodos do Controller
        getAllEmployees (@GetMapping): Retorna uma lista de todos os funcionários.
        getEmployeeById (@GetMapping("/{id}): Retorna um funcionário específico pelo ID ou 404 se não encontrado.
        createEmployee (@PostMapping): Cria um novo funcionário com os dados fornecidos e retorna o funcionário criado com status 201.
        updateEmployee (@PutMapping("/{id}): Atualiza um funcionário existente pelo ID ou retorna 404 se não encontrado.
        deleteEmployee (@DeleteMapping("/{id}): Remove um funcionário pelo ID e retorna 204 se bem-sucedido ou 404 se não encontrado.

## Students Controller
Este controller lida com requisições relacionadas a estudantes e fornece informações sobre o projeto "Medify".
Componentes

    Anotações
        @RestController: Indica que a classe é um controller REST.
        @Autowired: Injeta o repositório StudentRepository.

    Constantes
        PROJECT_NAME: Nome do projeto.
        PROJECT_THEME: Tema do projeto.

    Métodos do Controller
        getHelp (@GetMapping("/ajuda")):
            Mapeia para uma requisição GET na URL /ajuda.
            Retorna uma lista de nomes de estudantes, o nome do projeto e seu tema.