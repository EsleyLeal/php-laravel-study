Funciona como uma combinação do forEach e de um comando 
condicional pra verificar se array esta ou nao vazio.


Se nao houver itens no array o fluxo é desviado.

{
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
            $fornecedores = [];
        
        return view('app.fornecedor.index', compact('fornecedores'));
    }


    O array estando vazio o forElse desvia o fluxo para o empty



    @isset($fornecedores)

    @forelse ($fornecedores as $indice => $fornecedor )
        Fornecedor: {{ $fornecedor['nome'] }}
        <br/>
        Status: {{ $fornecedor['status'] }}
        <br/>
        CNPJ: {{ $fornecedor['cnpj'] ?? '' }}
        <br/>
        Telefone: ({{ $fornecedor['ddd'] ?? '' }}) {{ $fornecedor['telefone'] ?? '' }}
        <hr/>
    @empty
        Não consta nada em cadastro
    @endforelse
@endisset

