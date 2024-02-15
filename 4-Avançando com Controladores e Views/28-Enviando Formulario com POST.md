Uso de post

    Route::post('/contato', [\App\Http\Controllers\ContatoController::class, 'contato'])->name('site.contato');



O framework laravel permite que todos os formularios tenha um token.

o nome do token é @csrf

<form action={{ route('site.contato') }} method="post">
                    @csrf