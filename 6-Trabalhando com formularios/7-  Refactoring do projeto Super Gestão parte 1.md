 Refactoring do projeto Super Gestão parte 1

<select name="motivo_contato" class="{{ $classe }}">
        <option value="">Qual o motivo do contato?</option>
        @foreach ($motivo_contatos as $key => $motivo_contato )
            <option value="{{$motivo_contato->id}}" {{old('motivo_contato') == $motivo_contato->id ? 'selected' : '' }}>{{$motivo_contato->motivo_contato}}</option>
        @endforeach
    </select>


    