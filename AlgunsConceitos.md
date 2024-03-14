Aula sobre os conceitos do Laravel que ja utilizei:

all();   <<<<<<<<<<<<<

    Função: Recupera todos os dados do formulário enviados através da requisição HTTP (request).
Retorno: Um array contendo todos os campos do formulário e seus respectivos valores.
Uso:
Acessar todos os dados do formulário para processamento.
Criar uma nova instância de modelo a partir dos dados do formulário.

    $dados = $request->all();

    $usuario = new Usuario;
    $usuario->nome = $dados['nome'];
    $usuario->email = $dados['email'];
    $usuario->save();

compact(): <<<<<<<<<<<<<

Função: Cria um novo array contendo apenas as variáveis especificadas e seus valores.
Uso:
Passar somente os dados necessários para funções ou views.
Simplificar a passagem de variáveis dentro de templates.

    $nome = $request->input('nome');
    $email = $request->input('email');

    return view('bem_vindo', compact('nome', 'email'));

$data = $request->all();:

    Como mencionado anteriormente, recupera todos os dados do formulário.

    Obs: $data é mais uma convenção e um padrão de nomenclatura do que uma obrigatoriedade. O nome $data geralmente é escolhido para representar um conjunto genérico de dados ou informações, especialmente quando se trata de manipulação de formulários ou requisições HTTP.

hasFile():

    Função: Verifica se um campo específico do tipo arquivo existe na requisição.

        if ($request->hasFile('foto')) {
        // Processar o arquivo enviado
        } else {
        // Tratar o caso onde nenhum arquivo foi enviado
        }

redirect()->route():

    Função: Redireciona o usuário para uma rota nomeada.
    Uso:
    Redirecionar após envios de formulário ou ações bem-sucedidas.

    return redirect()->route('pagina_inicial');

findOrFail()

    Função: Recupera uma instância de modelo com base no ID ou critérios fornecidos. Se não encontrar o registro, lança uma exceção ModelNotFoundException.
    Uso:
    Buscar recursos existentes para edição ou exclusão.

    $usuario = Usuario::findOrFail($id);

public function rules()

    Função: Define as regras de validação para um modelo. Normalmente usada dentro de um método de controller.
    Uso:
    Garantir a integridade dos dados e prevenir entradas inválidas.

        public function rules()
        {
            return [
                'nome' => 'required|string|max:255',
                'email' => 'required|email|unique:usuarios',
                // ... outras regras
            ];
        }


$fillable:

    Propriedade: Determina quais atributos do modelo podem ser preenchidos em massa a partir dos dados da requisição.
    Uso:
    Prevenir a vulnerabilidade de atribuição em massa.

        protected $fillable = [
        'nome',
        'email',
        // ... outros atributos permitidos
    ];


unique()

        unique():

    Restrição: Assegura que um valor de atributo do modelo seja único dentro da tabela do banco de dados.
    Uso:
    Evitar entradas duplicadas (por exemplo, email, nome de usuário).

->nullable():

    Modificador: Permite que um atributo do modelo seja nulo (vazio).
    Uso:
    Lidar com campos opcionais que podem não ter sempre um valor.

storage:

        Sistema: Sistema de armazenamento integrado do Laravel para gerenciar uploads de arquivos.
        Uso:
        Fazer upload, armazenar e recuperar arquivos.

        $caminho = $request->file('foto')->store('uploads'); // Armazena o arquivo no diretório 'uploads'


Criar model, migration e controller:

    php artisan make:model Cliente -mcr


    php artisan make:controller ClienteController --resource
--resource: Flag para gerar métodos de controlador de recursos.