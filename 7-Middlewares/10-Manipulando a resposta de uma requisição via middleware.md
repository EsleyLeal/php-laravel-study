Posso manupular as respostas atraves do next ou seja...

Em LogAcessoMiddleware eu tenho um retorno

    return $next($request);

Eu posso armazenar esse objeto do $request em uma variavel 

    $resposta - $next($request);

E com isso posso manipular o que eu quiser.

    dd($resposta) - Para visualizar o objeto 

Manipular o status 

        $resposta = $next($request);
        

        $resposta->setStatusCode(201, 'O status e o texto foram modificados');
        dd($resposta);


OS Middleware sao feitos de modos sequenciais.

Obs: Next sempre empurra a requisição, mas sempre temos uma resposta.