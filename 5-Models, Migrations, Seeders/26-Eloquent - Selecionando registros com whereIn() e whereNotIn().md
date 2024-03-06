Filtros de consultas

whereIn() e whereNotIn()  - Suportam comparações com valores numericos, strings e datas.

    whereIn() - Espera dois parametros.
    Primeiro parametro é campo a ser comparado por igual
    Segundo parametro é o conjunto de parametros.

> $contatos = SiteContato::whereIn('motivo_contato',[1,3]); = Retorna um builder por nao ter passado o -get();

Então chamamos

$contatos->get();


Ja o 

whereNotIn() - $contatos = SiteContato::whereNotIn('motivo_contato',[1,3]); = Faremos a consulta inversa.