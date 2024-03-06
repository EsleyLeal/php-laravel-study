Como combinar duas ou mais operação de comparação utilizando o operador logico our


select 
	* 
from 
	site_contatos 
where 
	nome <> 'Fernando' 
    or motivo_contato in(1,2) 
    or created_at between '2020-08-01 00:00:00' and '2020-08-31 23:59:59';



Diferença entre and e or = 

    And - precisa que todas as condições e operações de comparação precisa ser verdadeiras para que os registro sejam retornados

    Or - Apenas uma condição de comparação precisa ser verdadeiro para qeu o registro seja retornado

    > $contatos = SiteContato::where('nome', '<>', 'Fernando')->orWhereIn('motivo_contato',[1,2])->orwhereBetween('created_at', ['2020-08-01 00:00:00', '24-02-27 23:29:27'])->get();