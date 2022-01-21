# 📝 amostra de códigos

[Métodos Jquery]() |
[Métodos Jquery e JS]() |
[Métodos Javascript]() |
[📝 Legendas](https://github.com/H7-Dev/legendas/edit/master/legendas.md) |


### 01.00 [Jquery & JS]
```JS
const testeInit = {
    doc           : $(document),
    btnFechar     : '#inibtnFechar',
    init: () => {
        setTimeout(function () {
            console.log('init teste -g')
            testeInit.Ouvintes()
        }, 400);
    },
    Ouvintes: () => {
        // → exemplo de evento on, ou seja para els criados de forma dinâmica, neste caso, adicina o evento click a um els criado após o dom ser carregado
        testeInit.doc.on('click', testeInit.btnFechar, function (e) {
            console.log('Evento Click Funcional!')
            console.log('Inicial teste de calback')
            let $this = $(this)
            console.log($this)
            setTimeout(function () {
                testeInit.exe_callbackComParametros($this)
            }, 1000);
        })
    },
    exe_callbackComParametros: function (_el) {
        console.log(_el)
    },
}
testeInit.init()
```
