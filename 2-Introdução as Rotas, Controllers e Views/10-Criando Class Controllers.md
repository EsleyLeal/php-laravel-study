
Na prática, controladores
são classes com padrão CamelCase e todas as classes de controle termina com Conttroler


No contexto de controladores, os metodos são conhecidos como actions.
Actions = Será associado as rotas



class PrincipalController extends Controller
{			Actions
    public function principal()
    {
        echo 'Olá';
    }
}
