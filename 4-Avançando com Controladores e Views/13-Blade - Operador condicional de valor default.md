Valor deafault funciona como um atalho do operador condicional ternario.



@isset($fornecedores)

Fornecedor: {{ $fornecedores[1]['nome'] }}
<br/>

Status: {{ $fornecedores[1]['status'] }}
<br/>

CNPJ: {{ $fornecedores[1]['cnpj'] ?? 'Dado não foi preenchido' }}
<!--
    Se a variavel nao estiver definida ( isset ) ou possuir valor null, o valor default sera usado no 
    lugar da variavel em questão.
    O que é testado nao é o valor da variavel, mas a existência da variavel.
-->

@endisset