Apos a chamada do metodo get, colocamos o metodo ->name('qualquer nome');

Os names podem ser utilizados atraves de uma função help do framework laravel.

Os names aplicados as rotas são processados e podem ser utilizados apenas dentro da propria logica 
da nossa aplicação, ou seja ... 

    Tendo isso aqui 

Route::prefix('/app')->group(function() {
    Route::get('/clientes', function() {return 'Clientes';})->name('app.clientes');
    Route::get('/fornecedores', function() {return 'Fornecedores';})->name('app.fornecedores');
    Route::get('/produtos', function() {return 'Produtos';})->name('app.produtos');
});

            Nao consigo acessar app.clientes, so consigo acessar a rota sendo  >>>  app/clientes




            Em views eu tenho isso e com o metodo name eu consigo passar esse apelido no li  <a abrindo
            duas chaves e chamando o metodo route

            <ul>
    <li>
       <a href="{{ route('site.index') }}">Principal</a>
    </li>
    <li>
        <a href="{{ route('site.sobrenos') }}">Sobre-nos</a>
    </li>
    <li>
        <a href="{{ route('site.contato') }}">Contato</a>
    </li>
</ul>




