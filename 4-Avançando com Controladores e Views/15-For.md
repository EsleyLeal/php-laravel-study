Estruturas de repetição

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


                    Loop

@isset($fornecedores)  ---- Lembrando que o operador isset
                            serve pra saber se uma variavel esta ou nao definidos, se existe ou nao.

    @for($i = 0; isset($fornecedores[$i]); $i++)
        Fornecedor: {{ $fornecedores[$i]['nome'] }}
        <br/>
        Status: {{ $fornecedores[$i]['status'] }}
        <br/>
        CNPJ: {{ $fornecedores[$i]['cnpj'] ?? '' }}
        <br/>
        Telefone: ({{ $fornecedores[$i]['ddd'] ?? '' }}) {{ $fornecedores[$i]['telefone'] ?? '' }}
        <hr/>
    @endfor

@endisset