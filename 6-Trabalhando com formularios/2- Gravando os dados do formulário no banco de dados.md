Dentro do Controller precisamos trazer o modelo que sera preenchido no banco de dados.

Exemplo

ContatoController ->     use App\Models\SiteContato;


Em seguida

        $contato = new SiteContato();
        $contato->nome = $request->input('nome');
        $contato->telefone = $request->input('telefone');
        $contato->email = $request->input('email');
        $contato->motivo_contato = $request->input('motivo_contato');
        $contato->mensagem = $request->input('mensagem');

        print_r($contato->getAttributes());

        Podemos executar com o metodo save() para salvar no banco de dados.


Outro modo com o Metodo fill(), preenche os atributos do contato com base em um array associativo que sera o $request->all();

    $contato = new SiteContato();
    $contato->fill($request->all());

    E para que a gente consiga esse array precisamos dar um protected fillable no modelo.

    Com o protected passamos um array indicando quais atributos do objeto pode ser preenchidos em massa.


Uso do create , que assim como fill, a variavel protected esteja definida no modelo indicando quais atributos podem ser preenchidos de modo massivo.

        $contato = new SiteContato();
        $contato->create($request->all());