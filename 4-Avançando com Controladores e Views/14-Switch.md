Operador switch case funciona de forma analoga ao operador if.

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


    VIEW IN BLADE

    *O parametro que sera utilizado na condição.
    *A comparação por idêntico verifica o valor contido na variável e também o tipo da variável.




@switch($fornecedores[2]['ddd'])
    @case ('11')
        São Paulo - SP
        @break
    @case ('71')
        Salvador - BA
        @break
    @case ('83')
        João Pessoa - PB
        @break
    @default
        Estado não identificado
@endswitch