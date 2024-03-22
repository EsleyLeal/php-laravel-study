Usamos o metodo de validação if

@if( $errors->has('nome') )
    {{ $errors->firt('nome') }}
@endif


Boa usar a condição ternaria

 {{ $errors->has('nome') ? $errors->first('nome') : '' }}