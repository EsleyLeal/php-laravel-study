A ordenação pode ser feita com base em uma coluna de forma ascendente e descendente



use \App\Models\SiteContato

$contatos = SiteContato()->orderBy('nome')->get();      = ascendente padrão

$contatos = SiteContato()->orderBy('nome', 'desc')->get();      = descendente padrão