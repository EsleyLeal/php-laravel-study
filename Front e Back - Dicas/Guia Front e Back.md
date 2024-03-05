Usando o Vite 
Instalar o yarn global primeiro

npm install -g yarn


    yarn create vite app--template vue

    yarn install = instalar todos os mods

    yarn dev = subir ambiente de desenvolvimento

------------------------------------------------------------

Instalar back-end laravel

    laravel new api
    composer create-project laravel/laravel api

===========================

    Mundo real -  Front em um Dominio e o Back em um subDominio

    Isso é uma convenção tendo o back em subDominio.

--------------------------------------------------------------------------

https://www.npmjs.com/package/ohmyfetch - Chegando agora

Pra fazer a conexão entre o Front e o Back

https://axios-http.com/ptbr/docs/intro

    Utilizamos Axios
 
----

Acesso a pasta do front e instalo o axios

    yarn add axios

    ... Import axios from "axios"; no App.vue

Depois fazer a conexão 

    axios.get( url: '')
    .then(( response )=>{
    console.log(response)
    }) 

    --- 

    Temos que ir ate o nosso back-end e criar nosso End-Point e criar a nossa conexão.

    Laravel
                routes/api.php

                    Exemplo de teste
    Route::get('/users', function (Request $request) {
    return [
        'data' => [
            [
                'id' => 1,
                'name' => 'Leal'
            ]
        ]
    ];
});


-------------------------

No axios acessamos o data   

        axios.get( url: '')
        .then(( response )=>{
        console.log(response.data)
        }) 


Quando subir o projeto , o ideal é ter o front em um repositorio e o back end em outro repositorio.


=========================

Conectar no github os dois projetos

Entrar na pasta API e na pasta front

git status
git add . && git coomit
git remove 
git branch -M main
git remove add origin
git push origin main

==========================

Em app/Models temos nosso User.php

Temos tambem em database migrations nossas migrations
E em seeders, nossos seeders que conecta com o banco de dados.



Quando descomentei isso 


            public function run(): void
    {
        \App\Models\User::factory(10)->create();

        \App\Models\User::factory()->create([
            'name' => 'Test User',
            'email' => 'test@example.com',
        ]);
    }

dei o comando php artisan migrate:fresh --seed    Ele atualizou o banco trazendo 10 usuarios alatorios pra teste