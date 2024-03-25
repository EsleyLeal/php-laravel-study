Implementando um middleware para todas as rotas

Classe Kernel PHP

Responsavel por iniciar diversos middlewares e definir para grupos de rotas dentro da nossa aplicação.

    Existem dois tipos de grupos de rotas

1- ROTAS WEB
2- ROTAS API

Middlewares pode ser alocados a esses dois grupos de rotas de modo que possa funcionar para todas essas
rotas.


O que significa esses dois grupos no Middlewares? -> Kernel.php

Logo abaixo, são middlewares que sempre serão chamados, são middlewares associados a aplicação.

    protected $middlewareGroups = [
        'web' => [
            \App\Http\Middleware\EncryptCookies::class,
            \Illuminate\Cookie\Middleware\AddQueuedCookiesToResponse::class,
            \Illuminate\Session\Middleware\StartSession::class,
            \Illuminate\View\Middleware\ShareErrorsFromSession::class,
            \App\Http\Middleware\VerifyCsrfToken::class,
            \Illuminate\Routing\Middleware\SubstituteBindings::class,
            \App\Http\Middleware\LogAcessoMiddleware::class
        ],

Toda requisição e toda resposta ira passar por essa manipulação desses middlewares.

    middlewareGroups estao separados no grupo WEB e api.

    








----------------------------------------------------------
 Kernel HTTP tem uma lista definida de Middlewares os quais também processam e manipulam a requisição. Esses Middlewares são responsáveis por persistir Sessões, fazer as verificações de Token CSRF, prevenir SQL Injection, entre outras coisas.

 Provedores de Serviços (Service Providers)
Uma das coisas mais importantes a se saber é que o Kernel, em suas ações de inicialização, carrega os Service Providers, onde primeiro todos os Providers são registrados, uma vez que o registro foi finalizado, em seguida todos são inicializados.

Os Service Providers são responsáveis por inicializar todos os diversos componentes da estrutura, como os componentes de banco de dados, fila, validação e roteamento e também implementações próprias.

Como eles inicializam e configuram todos os recursos ofer