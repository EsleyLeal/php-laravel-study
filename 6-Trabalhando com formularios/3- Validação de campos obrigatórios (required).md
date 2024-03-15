 Como validar os dados do formulario do lado do back-end da aplicação.

            $request->validate([
                'nome' => 'required'
            ]);   

    
    Em Laravel, $request é um objeto que representa a requisição HTTP atual. O método validate() é usado para validar os dados recebidos na requisição de acordo com as regras especificadas.

    Por exemplo, se você estiver recebendo dados de um formulário HTML com um campo chamado 'nome', esse trecho de código garantirá que o campo 'nome' seja fornecido antes que qualquer outra ação seja executada. Se a validação falhar, Laravel retornará automaticamente uma resposta de erro, geralmente redirecionando o usuário de volta ao formulário com mensagens de erro para que possam corrigir os problemas.

    No laravel temos uma variavel errors,  e quando não passa no processo de validação , ele tras a variavel errors preenchida.

    Em web.php eu tenho

        Route::post('/contato', [\App\Http\Controllers\ContatoController::class, 'salvar'])->name('site.contato');


Varivel 

    {{ print_r($errors) }}  Disponivel no contexto das views.