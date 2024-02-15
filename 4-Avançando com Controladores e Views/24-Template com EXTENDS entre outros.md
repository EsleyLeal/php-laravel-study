Como trabalhar com template no blade.

Temmplates são modelos que servem como base pra criação de alguma coisa =  views.

A partir de um template podemos rearoveitar uma grande quantidade de código sem ter que ficar reescrevendo
tudo aquilo que é comum  entre páginas web.


Um Temmplate é nada mais que uma view com alguns truques , associação e passagem de parametros.



Como conectar o template com a VIEW ?

    intrução - Entre template e view

    @extends('coloca o caminho') -  Usa-se na view que vai receber o template. Qual template vai estender para rearoveitar.

    O extends vai direto para o diretorio view contido no diretorio resource


Pegar todo o conteudo da nossa view e direcionar para areas especificas do nosso layout.

Utilizamos o 

@section()

        Tudo que estiver aqui será direcionado pro template

@endsection


No layout 

usamos o @yield('conteudo') 


RESUMO

@extends - determina o template a ser utilizado na view
@section - envio dos blocos de codigo html para o template extendido
@yield -  Onde os blocos devem ser redenrizados