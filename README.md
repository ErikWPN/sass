# jQuery
'Write less, do more'
- Biblioteca de Javascript
- Carregamento rápido
- converte pra JS (ECMAScript) padrão
- Crossbrowser: funciona em diversos navegadores
- Escrever um código para todos os navegadores
- Rápida captura e transmissão de dados
- Minipula o DOM
- Facilita a consulta (query) a elemnetos
- Extensível com plugins
- instalação: https://jquery.com/download/

## Seletores
### Simples

```
    $('h4') // tag
    $('.faeture-item') // class
    $('#featured') //ids

```

### Compostos

```
    $('H4, H6')

    $('div h4')
```

### Manibulação de HTML
- .append > Para adicionar ao final da frase
- .prepend > Para adiconar ao Inicio da frase
- .addclass > Para adicionar class para o HTML
- .removeClass > Para removeer class do HTML
- .after > para adicionar texto
- .before > para adionar texto antes
- .hide > para ocutar algo!
- .show > para exibir algo oculto
- .removo > para remover cod!

### Minupulação de CSS
- .fade > para adicionar animação (fadeIn (2000) - faz entrada. fadeout (2000) - faz a saida)
- .css('color', '#FF0000') > para alterar a cor do elemento!
- .css('backgroud', '#FF0000') > para alterar a cor do fundo do elemento!

### Eventos
- .mouseenter + this > ultilizado para realizar evendo com o mouse
Exemplo:

´´´
    $('.featured-item').mouseenter(function(){
        console.log($(this).find('h4).text());
    });

´´´
- (+'-'+) > para adicionar um espaço entre um elemento e outro
- bluer > ação dominada apos tirar o mouse do elemento

### Validação com .Elem

´´´
function validate(elem){
        if(elem.val() == ''){
            console.log('O campo de'+ elem.attr('name')+'é obrigatorio')
            elem.parent().fin('text-muted').show()
            elem.addClass('invalid')

            return false
        }else{
            elem.parent().find('.text-muted').hide()
            elem.removeClass('invalid')
        }
    }
    $('body').on('submit', '.modal-body .form', function(e){
        e.preventDefault()
        const inputName = $('#name')
        const inputEmail = $('#email')

        validate(inputName)
        validate(inputEmail)

        if(inputEmail.hasClass('invalid') || inputName.hasClass('invalid')){
            console.log('Verificar campos Obrigatorios')
            return false
        }else{
            $(this).submit()
        }
    })

´´´

´´´
    $('.form').on('submit', function(e){
                e.preventDefault()

                const name = $('.#nome').val()
                const email = $('.#email').val()

                if(inputName.val() == '') {

                    console.log('Os campos obrigatórios estão vazios')

                    $('#inputName').addClass('invalid')

                    return false
                }

            })

´´´