Eloquent - Deletando registros (delete e destroy)


Como deletar esses registros.

use \App\Models\SiteContato;
> $contato = SiteContato::find(4);                  recuperado o id 

= App\Models\SiteContato {#5221
    id: 4,
    created_at: null,
    updated_at: null,
    nome: "Rosa",
    telefone: "(33) 92222-3333",
    email: "rosa@contato.com.br",
    motivo_contato: 1,
    mensagem: "Quando custa essa aplicação?",
  }

> $contato->delete();                       Ele ja sabe qual deve deletar



Temos o metodo destroy que espera por parametro o ID a ser removido.


                    ID
SiteContato::destroy(5);  

É possivel encaminhar varios ID's separados por virgula. 

Também é possivel encaminhar um array ou uma collection de elementos inteiros que representam os ID's desejados.