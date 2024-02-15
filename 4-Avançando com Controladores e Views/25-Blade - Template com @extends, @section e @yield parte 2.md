section - alem dos blocos html o section permite envios de parametros 

Variveis recebidas dos controladores!



    No meu layout basico irei criar isso aqui

<title>Super Gestão - @yield('titulo')</title>

    Pelo que entendi, cada view vai reconhecer os blocos atraves das rotas, o proprio laravel entende isso

Em por exemplo umas das views chamada sobre-nos eu referencio a sessão assim, passando o nome
da string titulo e o nome da view.

    @section('titulo','Sobre-Nos')



Podemos também passar variavel que vai vir dos controladores

    No controlador temos isso aqui 


        <?php
                                        Array associativo 
        return view('site.contato', ['titulo' => 'Contato (teste)']);           
                                    parametro


        na view eu tenho isso aqui 
        
     @section('titulo', $titulo)


