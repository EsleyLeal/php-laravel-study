@component()

Inclusão de views dentro de outras views.

<div class="informacao-pagina">
            <div class="contato-principal">
                @component('site.layouts._components.form_contato')
                @endcomponent
            </div>

    Aqui esta meu component formulario
@component('site.layouts._components.form_contato')

