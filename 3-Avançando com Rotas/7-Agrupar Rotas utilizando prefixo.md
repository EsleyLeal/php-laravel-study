Permite organizar melhor toda parte de rotiamento da aplicação.


Aprender a separar uma dimensão publica
 e uma dimensão privada. O acesso dependera de algum metodo de 
autenticação.


----> Agrupar as rotas cujo o prefixo seja /app e poderia ter qualquer nome
----> E agrupar rotas


Teremos um prefix e um metodo grup que recebe por parametro uma função de callBack
Metodo grupo recebe todas as rotas que sera do prefix

Route::prefix('/app')->group(function() {
    Route::get('/clientes', function() {return 'Clientes';} );
    Route::get('/fornecedores', function() {return 'Fornecedores';} );
    Route::get('/produtos', function() {return 'Produtos';} );
});

Essa estrutura é usada para organizar e agrupar rotas de forma mais
 eficiente em aplicações web. Essa prática é comum em frameworks 
 modernos para manter o código limpo e modular.