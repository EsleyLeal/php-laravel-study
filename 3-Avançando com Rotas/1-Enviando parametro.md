em routes/web.php

Route::get('/contato/{nome}', function(string $nome)
{
    echo 'Estamos aqui: ' .$nome;

});


Com parametros



// Enviando parametros
// nome, categoria, assunto, mensagem

Route::get(
    '/contato/{nome}/{categoria}/{assunto}/{mensagem}', 
    function(string $nome, string $categoria, string $assunto, string $mensagem)
{
    echo "Estamos aqui: $nome - $categoria - $assunto - $mensagem ";
});

