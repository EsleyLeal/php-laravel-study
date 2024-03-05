Metodo Estatico

Semelhante ao metodo all()

find() - Espera por parametro a a primeKey - Uma ou varias.

$fornecedores2 = Fornecedor::find();


A primeKey é a coluna ID

Por passar um ID ele retorna um unico objeto e não uma coleção de objetos

Com isso podemos utilizar de forma direta esse unico objeto retornado.

exemplo

            echo $fornecedores2->nome;



    Podemos passar com array e assim retornara uma coleção de objetos e com isso utilizamos o forEach
$fornecedores2 = Fornecedor::find([1,2]);



foreach($for as $f) {echo $f->nome; echo '-';}