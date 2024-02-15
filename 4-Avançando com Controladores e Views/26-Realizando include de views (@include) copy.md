Realizar include de views , dentro de outras views.

A diferença entre o @include e o @extends  é que enquanto @extends extende uma determianda view
e passa parametro pra essa view atraves do section e do yield

o @include temos a inclusão de todo o conteudo dessa view no exato ponto aonde o include é feito na view 
que faz essa inclusão.


        Colocando o include no layout principal facilita a manutenção do codigo.
@include('site.layouts._partials.topo')


Dessa forma é replicada em todos as outras views deixando o codigo mais limpo.



    Duvida ?   Existe diferença entre @extend e @include

    @include é como uma inclusão básica de PHP, inclui uma visão "parcial" da sua visão.

    @extends permite "estender" um modelo, que define suas próprias seções, etc. Um modelo que você pode estender definirá suas próprias seções usando @yield, nas quais você poderá colocar seus próprios itens em seu arquivo de visualização.

        Exemplo
modelo.blade.php

<html>
    <body>
        @yield('header')
        @yield('content')
        @yield('footer')
    </body>
</html>

visualizar-one.blade.php

    @extends('template')

    @section('header')
        View one's header
    @endsection

    @section('content')
        View one's content
    @endsection

    @section('footer')
        View one's footer
    @endsection

O que resultará em:

    <html>
    <body>
        View one's header
        View one's content
        View one's footer
    </body>
</html>

Agora você pode criar outra visualização que estenda o mesmo modelo, mas forneça suas próprias seções.

Outro benefício de usar @extendé a herança. Você pode fornecer um modelo base e, em seguida, outro modelo filho que estenda aquele que posteriormente produz suas próprias seções. Você pode então estender esse modelo filho