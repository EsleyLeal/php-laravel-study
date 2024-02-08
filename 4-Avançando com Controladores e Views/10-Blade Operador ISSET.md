Serve pra saber se uma variavel estao ou nao definidos, se existe ou nao.
No blade serve como atalho.

E no php é um metodo no operador if else.

Inclui também indices de arrays





Exemplo, no meu controller

{
    public function index() 
    {
        $fornecedores = 
        [
            0 => ['nome' => 'Fornecedor 1', 'status' => 'S']
        ];
        return view('app.fornecedor.index');
    }
}


e no blade 

@isset($fornecedores)
Fornecedor: {{ $fornecedores[0]['nome'] }}
<br/>
Status: {{ $fornecedores[0]['status'] }}
<br/>
@endisset

                    Ou seja ,  a variavel nao esta definida e com o operador @isset ele verifica isso 
                    fazendo a página ainda sim ficar no ar.


Outra forma de uso 

@isset($fornecedores)
Fornecedor: {{ $fornecedores[1]['nome'] }}
<br/>
Status: {{ $fornecedores[1]['status'] }}
<br/>
@isset($fornecedores[1]['cnpj'])
    CNPJ: {{ $fornecedores[1]['cnpj'] }}
@endisset
@endisset