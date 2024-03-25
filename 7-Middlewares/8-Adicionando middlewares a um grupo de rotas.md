   
   Posso colocar o middleware em GRUPO
   
   
   
    Route::middleware('log.acesso','autenticacao')->prefix('/app')->group(function() {
    Route::get('/clientes', function() {return 'Clientes';})
    ->name('app.clientes');

    Route::get('/fornecedores', [\App\Http\Controllers\FornecedorController::class, 'index'] )->name('app.fornecedores');
    Route::get('/produtos', function() {return 'Produtos';})->name('app.produtos');
    );


