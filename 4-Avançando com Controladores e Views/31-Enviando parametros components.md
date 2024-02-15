Dentro de um component

<div class="contato-principal">
                @component('site.layouts._components.form_contato')
                @endcomponent
            </div>

Tudo que estiver dentro a gente encaminha para ser incluida dentro do component em algum local
especifico.

Exemplo

    @component('site.layouts._components.form_contato', ['classe' => 'borda-preta'])
                    <p>A nossa equipe analisará a sua mensagem e retornaremos o mais brevemente possivel.</p>
                    <p>Tempo medio de resposta é de 48 horas.</p>
                @endcomponent


Usando a Varivel     

    $slot 

    Usando parametro em component 


O formulario esta com a mesma cor e conseguir mudar isso com criando um array associativo com variavel de nome 
classe.
                                                            Array Associativo
                                                            
    @component('site.layouts._components.form_contato', ['classe' => 'borda-branca'])
    @endcomponent

So fiz passar essa variavel no input

    <input name="nome" type="text" placeholder="Nome" class="{{ $classe }}">

Dessa forma o css consegue identificar o estilo.