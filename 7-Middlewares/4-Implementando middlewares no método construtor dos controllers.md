Implementando middlewares no método construtor dos controllers

Exemplo de implementação no controller

    class SobreNosController extends Controller
{
    public function __construct(){
        $this->middleware(LogAcessoMiddleware::class);
    }

    public function sobreNos()
    {
        return view('site.sobre-nos');
    }
}