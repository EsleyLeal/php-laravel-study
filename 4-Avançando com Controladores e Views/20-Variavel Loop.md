Objeto loop é criado automaticamente pelo blade quando usamos o forEach e forElse

Porque em for e while nao tem ?
    Porq declaramos a variavel de controle do laço.




    Objeto loop -  Fornece informações importante sobre o loop que esta acontecendo.

                Iteração atual do laço
Iteração atual: {{ $loop->iteration }}



Atributos

interation - Iteração atual do laço
first - indica se a interação em questão é o primeiro indice do nosso array
last - indica se a interação em questão é o ultimo indice do nosso array
count - Total de registro

@dd($loop) - Consigo ver o que tem dentro do Objeto


@if($loop->first)
            Primeira iteração do loop
        @endif


 @if($loop->last)
            Ultima iteração do loop
        @endif     


 @if($loop->last)
            Ultima iteração do loop
            <br/>
            Total de registro - {{ $loop->count }}   <<<<<<<<<<<<<<<<<<<<
        @endif        


