Request 

Requisição que é feita do cliente um browser, para o back-end da aplicação.


Cliente ->  Requisição -> Back-End = Temos uma Request.

Pode ser recuperado do lado do back-end como sendo um objeto.

No controller temos isso use Illuminate\Http\Request;

Ele recupera o request aumaticamente 


    class ContatoController extends Controller
    {
        public function contato(Request $request)  <<<<<<<<< passamos o parametro com a tipagem, ela precisa esta tipada como Request
        {
            dd($request);  <<< recuperamos pra conseguir visualizar
            return view('site.contato', ['titulo' => 'Contato (teste)']);
        }
    }



    Com o metodo all() recuperamos um array associativo, as informações

        $request->all();

        echo '<pre>';
        print_r($request->all());
        echo '</pre>';


Podemos recuperar um dado especifico utilizando o metodo input('qual campo queremos recuperar')

        print_r($request->input('nome'));

    Obs: Quando enviado no formulario, os dados são encaminhados ao Form-Data