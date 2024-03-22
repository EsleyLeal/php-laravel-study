Ajuste de feddbacks

No controller posso colocar um array dentro do validate e chamar os campos e as mensagens para aparecer caso tenha errors


    public function salvar(Request $request) {

            $request->validate([
                'nome' => 'required|min:3|max:40|unique:site_contatos',
                'telefone' => 'required',
                'email' => 'email',
                'motivo_contatos_id' => 'required',
                'mensagem' => 'required'
            ],
            [
                'nome.required' => 'O campo nome precisa ser preenchido'   <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
            ]

        );      
         SiteContato::create($request->all());
         return redirect()->route('site.index');
    }


Posso chamar apenas o campo de validação 

    'min' => 'O campo nome precisa ter no minimo 3 caracteres'

Posso chamar o metodo :attribute que subtitue o campo, exemplo

    'min' => 'O campo :attribute precisa ter no minimo 3 caracteres' , ou seja em atribute vai conter o nome do input >  name="nome"


    Posso customizar criando variaveis e passando o array de validação e depois é so chamar 

    $request->validate($regras, $feedback)  <<<<<<< exemplo