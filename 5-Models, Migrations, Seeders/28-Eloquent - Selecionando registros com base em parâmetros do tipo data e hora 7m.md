Função estatica 

    whereDate()


    > $contatos = SiteContato::whereDate('created_at', '2024-02-27')->get();


Posso pesquisar por dia

    whereDay

    

Pesquisas por mês

    whereMonth


Pesquisar por ano

    whereYear

Baseada no tempo

    whereTime

                                                Segundo parametro é um operador de comparação 
23:29:27
$contatos = SiteContato::whereTime('created_at', '=', '23:29:27')->get();
$contatos = SiteContato::whereTime('created_at', '>', '23:29:27')->get();