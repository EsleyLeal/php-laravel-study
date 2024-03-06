Como utilizar dois ou mais wheres atraves do objeto builder

    Conectar duas ou mais operação atraves do operador logico = and ;


                Usando o tinker
     $contatos = SiteContato::where('nome', '<>', 'Fernando')->whereIn('motivo_contato',[1,2])->whereBetween('created_at', ['2020-08-01 00:00:00', '24-02-27 23:29:27'])->get();




     No banco de dados;

use sg;

select * from site_contatos where nome <> 'Fernando' and motivo_contato in(1,2) and created_at between '2020-08-01 00:00:00' and '2020-08-31 23:59:59';