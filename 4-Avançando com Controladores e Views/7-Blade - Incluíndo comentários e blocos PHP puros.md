

            {{-- --}}

{{--Fica o comentario que seta descartado pelo interpretador do blade --}}




@php

As informações contidas dentro nesse codigo são interpretadas pelo blade como nativas do PHP.

@endphp



@php 
    // Para comentarios de uma linha

    /*
        Para comentarios de multiplas linhas
    */

@endphp



{{ 'Texto' }} = <?= 'Texto' ?>  sinonimos   e dentro do bloco php usamos o echo.