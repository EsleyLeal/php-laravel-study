Estrutura de repetição dentro do codigo.

Observação -  Diferente do for, while não tem incremento e para isso usamos a tag php pra criar
uma variavel de incremento.


{{-- @dd($fornecedores) --}}
@isset($fornecedores)
    @php $i = 0 @endphp       <<<<<<<<<<<<<<<<<<<<<<< tag de criação variavel
    @while(isset($fornecedores[$i]))
        Fornecedor: {{ $fornecedores[$i]['nome'] }}
        <br/>
        Status: {{ $fornecedores[$i]['status'] }}
        <br/>
        CNPJ: {{ $fornecedores[$i]['cnpj'] ?? '' }}
        <br/>
        Telefone: ({{ $fornecedores[$i]['ddd'] ?? '' }}) {{ $fornecedores[$i]['telefone'] ?? '' }}
        <hr/>
        @php $i++ @endphp  <<<<<<<<<<<<<<<<<<<<<<<  fechamento com incremento
    @endwhile
@endisset