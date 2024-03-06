whereNull() e whereNotNull()

   Leva em consideração a existencia de um valor null em uma determinada coluna.

    No banco 

   select 
	* 
from 
	site_contatos 
where 
	updated_at is null;


Codigo tinker


     $contatos = SiteContato::whereNull('updated_at')->get(); - Todos os registro cujo os valores sejam null



Esses operadores podem ser encadeados

    


