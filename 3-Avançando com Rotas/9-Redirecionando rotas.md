Redirecionamento de rota permite direcionar o fluxo de navegação do usuario pela aplicação web.

Pode usar , para levar o usuario a uma campanha em andamento.

Imagina que o usuario acesse a rota raiz da aplicação, e podemos redirecionar esse acesso a uma pagina web 
alternativa com os detalhes dessa campanha.


Existem dois metodos de direcionamento



        1- redirect


Route::get('/rota1', function() {
    echo 'Rota 1';
})->name('site.rota1');

Route::redirect('/rota2', '/rota1');   --- Recebe dois parametros, primeiro o nome da rota a ser 
                                            direcionado e o segundo recebe o nome da rota atual.
                                        



        2- Dentro da função de callback da rota ou dentro do controller que é mais comum


Route::get('/rota1', function() {
    echo 'Rota 1';
})->name('site.rota1');

            Se observar , colocamos o nome que colocamos no campo ->name
Route::get('/rota2', function() {
    return redirect()->route('site.rota1');
})->name('site.rota2');

