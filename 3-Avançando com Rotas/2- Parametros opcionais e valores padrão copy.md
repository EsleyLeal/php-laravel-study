

Parametros opcionais usa-se interrogação e uma mensagem padrão caso
a informação nao seja inserida



Route::get(				    Opcional
    '/contato/{nome}/{categoria}/{assunto}/{mensagem?}', 
    function(
        string $nome, 
        string $categoria, 
        string $assunto,     Caso nao seja informada
        string $mensagem = 'Mensagem não informada')
{
    echo "Estamos aqui: $nome - $categoria - $assunto - $mensagem ";
});


Nao consigo definir mais de um parametro opção , o laravel vai se perder na hora de referenciar os parametros.

Ele entende quando passa o opcional da direita pra esquerda.



Route::get(
    '/contato/{nome}/{categoria}/{assunto}/{mensagem?}', 
    function(
        string $nome = 'Desconhecido', 
        string $categoria = 'Informação', 
        string $assunto = 'Contato', 
        string $mensagem = 'Mensagem não informada')
{
    echo "Estamos aqui: $nome - $categoria - $assunto - $mensagem ";
});

