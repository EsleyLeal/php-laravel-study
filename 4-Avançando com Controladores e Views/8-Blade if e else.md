class FornecedorController extends Controller
{
    public function index() 
    {
        $fornecedores = ['Fornecedor 1'];
        return view('app.fornecedor.index', compact('fornecedores'));
    }
}



Impressão de variavel tipo array no blade usamos o @dd(aqui passamos a variavel).




Uso do if e else no blade

@if(count($fornecedores) > 0 && count($fornecedores) < 10)
    <h3> Existem alguns fornecedores cadastrados</h3>
@elseif(count($fornecedores) > 10)
    <h3> Existem vários fornecedores cadastrados</h3>
@else
    <h3> Ainda não existem fornecedores cadastrados</h3>
@endif