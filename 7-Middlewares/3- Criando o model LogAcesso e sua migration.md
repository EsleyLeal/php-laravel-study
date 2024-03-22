Criando um model fazer os middlewares acessaos persistir no banco de dados ajuda a montar um cenario mais completo pra testes.

Criamos umn model e uma migration

    php artisan make:model LogAcesso -m


Na migration criamos uma tabela 
        
         $table->string('log', 200);

No model damos um       protected $fillable = ['log'];



Exemplo geral

    Usando o dd($request) eu pude ver o ip e a rota , depois criei isso

        $ip = $request->server->get('REMOTE_ADDR');  << armazenei em variaveis
        $rota = $request->getRequestUri();           << armazenei em variaveis


        LogAcesso::create(['log' => "IP $ip requisitou a rota $rota"]); <<< chamei
        
        return Response('Chegamos no middleware e finalizamos no proprio middleware');