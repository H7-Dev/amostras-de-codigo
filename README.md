
![image](https://user-images.githubusercontent.com/93455937/167199212-4c2a58b3-099f-4eb6-9dcc-4675e3e5a969.png)


# 📝 amostra de códigos

[Métodos Jquery]() |
[Métodos Jquery e JS]() |
[Métodos Javascript]() |
[📝 Legendas](https://github.com/H7-Dev/legendas/edit/master/legendas.md) |


> ### 02.00 [html -> componente => btnDropdown]
> ```html
>     <div class="btnDropdown btnLogin" data-tab="tab-A" tab="3">
>        <button>
>             <!-- <img src="ASSETS/MIDIA/IMG/07.01 camera-fotografa.png" alt="" srcset=""> -->
>             <svg height="28px" viewBox="0 0 24 24"><path d="M23,8.2c0,3.7,0,7.5,0,11.2c-0.1,0.2-0.1,0.4-0.2,0.5c-0.4,0.7-1,1-1.7,1c-5.6,0-11.2,0-16.8,0c-0.5,0-1,0-1.5,0c-0.5,0-0.9-0.1-1.2-0.4c-0.4-0.3-0.5-0.7-0.6-1.1C1,15.7,1,12,1,8.2c0,0,0-0.1,0-0.1C1.2,7.4,1.6,7,2.3,6.8c0.3-0.1,0.6-0.1,0.9-0.1c0-0.6,0-1.2,0-1.8c0.7,0,1.5,0,2.2,0c0,0.6,0,1.2,0,1.8C5.9,6.7,5.9,6.7,6,6.3c0.4-1,0.8-2.1,1.2-3.1C7.3,3.1,7.4,3,7.5,3c3,0,6,0,9,0c0.2,0,0.2,0.1,0.3,0.2c0.4,1.1,0.9,2.2,1.3,3.3c0.1,0.1,0.1,0.2,0.3,0.2c0.9,0,1.9,0,2.8,0c0.5,0,1,0.1,1.3,0.5C22.8,7.5,22.9,7.8,23,8.2z M12,19.5c3.6,0,6.6-3,6.6-6.6c0-3.6-3-6.6-6.6-6.6c-3.6,0-6.6,3-6.6,6.6C5.4,16.6,8.4,19.5,12,19.5z M18.6,9.6c0,0.8,0.7,1.5,1.5,1.5c0.8,0,1.5-0.7,1.5-1.5c0-0.8-0.7-1.5-1.5-1.5C19.3,8.2,18.6,8.8,18.6,9.6z M4.6,6.7c0-0.4,0-0.7,0-1.1c-0.2,0-0.5,0-0.7,0c0,0.4,0,0.7,0,1.1C4.2,6.7,4.4,6.7,4.6,6.7z M16.4,12.9c0-2.4-1.9-4.4-4.4-4.4c-2.4,0-4.4,2-4.4,4.4c0,2.4,2,4.4,4.4,4.4C14.4,17.3,16.4,15.4,16.4,12.9z"/></svg>
>         </button>
>         <div class=" optsDropdown" data-painel="tab-A" painel="4" >
>             <div class="overFlowsDiv" onclick="event.stopPropagation()">
>
>             </div>
>         </div>
>     </div>
> ```
> ```css
>     .btnLogin {
>         background-color: transparent;
>         min-height: 48px;
>         min-width: 48px;
>
>         display: grid;
>         grid-template-rows: min-content min-content;
>
>         border: none;
>         outline: none;
>
>         >button {
>             background-color: gainsboro;
>             padding: 6px;
>             min-height: 48px;
>             width: 48px;
>             border-radius: 50%;
>             outline: none;
>             border: none;
>             z-index: 1;
>             > img {
>                 height: 32px;
>                 display: none;
>             }
>             > svg {
>                 height: 32px;
>                 width: 32px;
>                 fill: #555555;
>             }
>         }
>         > div.optsDropdown {
>             background-color: transparent;
>             padding: 4px;
>             min-height: 50px;
>             min-width: 50px;
>
>             position: absolute;
>             display: block;
>
>             > div {
>                 background-color: white;
>                 min-height: 400px;
>                 max-height: 400px;
>                 width: 475px;
>                 display: grid;
>                 grid-template-columns: 1fr 1fr;
>
>
>
>                 overflow: hidden;
>                 box-shadow: 0 5px 10px rgba(0, 0, 0, 0.20);
>                 border-radius: 4px;
>                 position: absolute;
>                 top: 70px;
>                 right: 10%;
>                 z-index: 9999;
>                 transition: 0.5s;
>
>
>
>             }
>         }
>     }
> ```


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
