 Eloquent - Collection first, last e reverse

 Ao executar o comando no tinker, temos um objeto do tipo builder e quando recuperamos temos um objeto collection.

 Atraves do objeto collection , podemos aplicar os metodos que sao nativos dele. first, last e reverse


 Metodo firts vai retornar o primeiro registro dessa relação de registro da nossa coleção.

$contatos->firts(); primeiro elemento
$contatos->reverse(); inverte a ordem
$contatos->last(); Ultimo elemento