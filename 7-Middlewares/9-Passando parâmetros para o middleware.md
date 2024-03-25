Passando parâmetros para o middleware

Estabalecer logica padrão, usamos parametros para os nossos middleware.


Exemplo 
                                                AQUI

    Route::middleware('log.acesso','autenticacao:padrao')->prefix('/app')->group(function() {
    Route::get('/clientes', function() {return 'Clientes';})
    ->name('app.clientes');

    Route::get('/fornecedores', [\App\Http\Controllers\FornecedorController::class, 'index'] )->name('app.fornecedores');
    Route::get('/produtos', function() {return 'Produtos';})->name('app.produtos');
    });



No middleware 
                                                                AQUI

     public function handle(Request $request, Closure $next, $metodo_autenticacao): Response
    {
        echo $metodo_autenticacao. '</br>';

        if($metodo_autenticacao == 'padrao') {
            echo 'Verificar o usuario e senha no banco de dados'.'</br>';
        }

        if($metodo_autenticacao == 'ldap') {
            echo 'Verificar o usuario e senha no AD'.'</br>';
        }


        if(false) {
            return $next($request);
        } else  {
            return Response('Acesso negado! Rota exige autenticação!!!');
        }
        //return $next($request);      
    }
