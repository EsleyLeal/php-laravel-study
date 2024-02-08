Bastante util, podemos aplicar controller para que as rotas sejam processadas apenas se os parametros
passados esteja dentro das condições especificadas nas expressões regulares.


Route::get(
    '/contato/{nome}/{categoria_id}', 
    function (
        string $nome = 'Desconhecido', 
        int $categoria_id = 1
    ) {
        echo "Estamos aqui: $nome - $categoria_id";
    }
)where('categoria_id', '[0,9]+');


Expressão Regulares
    1 - Referencia o ID       2-  A expressao a ser usadaa
->->where('categoria_id', '[0,9]+');