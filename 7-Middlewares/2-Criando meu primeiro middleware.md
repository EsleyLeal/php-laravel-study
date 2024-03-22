Para criar um novo middleware, use o make:middlewarecomando Artisan:

    php artisan make:middleware Nome


Uma vez que o middleware é utilizado , ele procura pela function handle

    public function handle(Request $request, Closure $next): Response
    {
        return $next($request);
    }

So é ativado quando chamado nas rotas ou controladores.

Lembrar também de dar um use 

    use App\Http\Middleware\LogAcessoMiddleware;

em web.php posso passar o middleware primeiro dessa forma

    Route::middleware([LogAcessoMiddleware::class])
    ->get('/', [\App\Http\Controllers\PrincipalController::class, 'principal'])
    ->name('site.index');



Digamos que eu manipule a reposta

    return Response('');  <<<< Alterando o conteudo da resposta

Metodo Response forma um objeto de resposta, response http que é a resposta dada a quem fez a solicitação.