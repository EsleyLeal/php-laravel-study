


            Esta sendo herdado de Model;
> print_r($contato->getAttributes());
                    Metodo


                    Criação com o Tinker

        > $contato2 = new \App\Models\SiteContato();

        $contato2->nome = 'Leal';
        = "Leal"

        print_r($contato2->getAttributes());
Array
(
    [nome] => Leal
    [telefone] => (71)987804523
    [email] => esleylealsantana@gmail.com
    [motivo_contato] => 2
    [mensagem] => Estou achando legal !
)
= true


            Quando inserido as informações , o laravel visualiza da seguinte forma a tabela.
            Se o nome for Fornecedor.php

            ele vai visualizar assim

            fornecedor
            fornecedores

        Nesse caso quando acontecer de dar um erro dizendo que a tabela fornecedors não existe.

        Temos que no models dar um protected na tabela 

        protect $table = 'fornecedores'