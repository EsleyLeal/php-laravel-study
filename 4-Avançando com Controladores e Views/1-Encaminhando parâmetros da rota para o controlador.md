Como receber os parametros nas rotas e encaminhar esses parametros nos controladores.



Em web.php eu crio uma rota de teste e passo dois parametros.


Route::get('/teste/{p1}/{p2}', [\App\Http\Controllers\TesteController::class, 'teste'])->name('teste');

Em App e em controller eu tenho TesteController e em minha funçao teste na função de callback eu tenho
dois parametros. 

Obs: Não precisa passar o parametros na função sendo o mesmo nome, so é preciso estar na ordem.




A ideia nao é receber mais parametros nas rotas e sim os dados da requisição.