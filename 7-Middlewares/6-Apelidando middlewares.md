Apelidando middlewares

protected $middlewareAliases 


    Exemplo 

    'log.acesso' => \App\Http\Middleware\LogAcessoMiddleware::class


E em web.php nao é mais necessario passar a classe


    Route::get('/', [\App\Http\Controllers\PrincipalController::class, 'principal'])->name('site.index')->middleware('log.acesso');



No controller eu chamo assim 

        class SobreNosController extends Controller
    {
        public function __construct() {
            $this->middleware('log.acesso');
        }

        public function sobreNos()
        {
            return view('site.sobre-nos');
        }
    }
