ForEach

Recebe a variavel array, sem seguida as posições do indices 0, 1 , 2 etc... em seguida
colocamos isso => em uma variavel

 $fornecedores = 
        [
            0 => [
                'nome' => 'Fornecedor 1',
                 'status' => 'N',
                  'cnpj' => '0',
                  'ddd' => '11', // SP
                  'telefone' => '000-000'
            ],
            1 => [
                'nome' => 'Fornecedor 2',
                 'status' => 'S',
                 'cnpj' => '0',
                 'ddd' => '71', // BA
                 'telefone' => '000-000'
            ],
            2 => [
                'nome' => 'Fornecedor 2',
                 'status' => 'S',
                 'cnpj' => '0',
                 'ddd' => '83', // JP
                 'telefone' => '000-000'
                ]
        ];



        {{-- @dd($fornecedores) --}}
        @isset($fornecedores)
            @foreach ($fornecedores as $indice => $fornecedor )
                
                Fornecedor: {{ $fornecedor['nome'] }}
                <br/>
                Status: {{ $fornecedor['status'] }}
                <br/>
                CNPJ: {{ $fornecedor['cnpj'] ?? '' }}
                <br/>
                Telefone: ({{ $fornecedor['ddd'] ?? '' }}) {{ $fornecedor['telefone'] ?? '' }}
                <hr/>
            @endforeach
        @endisset



Lembrando que o forEach gera uma copia do array original
    Alterando a copia
com @php $fornecedor['nome'] = 'Outro nome para o fornecedor' @endphp  

    Alterando o original
com @php $fornecedores[$indice]['nome'] = 'Outro nome para o fornecedor' @endphp  