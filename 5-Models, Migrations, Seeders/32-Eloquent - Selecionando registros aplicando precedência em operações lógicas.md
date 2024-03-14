

Passamos uma função de callBack 


php artisan tinker

use \App\Models\SiteContato;

$contatos = SiteContato::where(function($query){ $query->where('nome', 'jorge')->orWhere('nome','Ana'); })->where(function($query){$query->whereIn('motivo_contato', [1,2])->orWhereBetween('id',[4,6]); })->get();