Repopulando o formulário (Request Old Input) parte 1

Recuperar dados que foram preenchidos no form , mesmo apos um erro eles sejam recarregados no formulario.

Funcão old() - Recebe por parametro um numero de um determinado input para ter acesso a uma informação que foi preenchida em uma requisição anterior.



Isso fazemos na propria view
    -----------------------------

                     <input name="nome" value= "{{ old('nome') }}"" type="text" placeholder="Nome" class="{{ $classe }}">


    <textarea name="mensagem" class="{{ $classe }}">{{(old('mensagem') != '') ? old('mensagem') : 'Preencha aqui a sua mensagem'}}</textarea>


Resumindo, quando não preenchido o campo, o old devolve com o resquest passado atraves do input informado.

        value= "{{ old('nome') }}


No select fica diferente sendo assim

            <select name="motivo_contato" class="{{ $classe }}">
        <option value="">Qual o motivo do contato?</option>
        <option value="1" {{ old('motivo_contato') == 1 ? 'selected' : '' }} >Dúvida</option>
        <option value="2" {{ old('motivo_contato') == 2 ? 'selected' : '' }}>Elogio</option>
        <option value="3" {{ old('motivo_contato') == 3 ? 'selected' : '' }}>Reclamação</option>
            </select>