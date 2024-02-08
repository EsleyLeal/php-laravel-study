Um tipo de rota que vai ser disponibilizada ao usuario , caso a rota acessada por ele nao seja localizada!

--- Rota de fallback



Route::fallback(function(){
    echo'A rota acessada não existe. <a href="'.route('site.index').'">Clique aqui</a> para ir para a página inicial';
});

Essa função poderia ter uma view , um controller, página bem customizada.
    O legal é poder colocar um link para ser redirecionado por exemplo a página raiz.

    Observe que dentros das aspas <a href="'.route('site.index').

    tem mais uma aspa para que a gente possa colocar o route e no final tem o ponto pra concatenar.

