No menu de opção: Contato ao ser clicado o evento de mostrar o formulário na página de origem
é mostrado e também ao ser clicado novamente ele oculta o formulário.
Segue o HTML:
                <li>
                    <a href="javascript:void(0);" id="mostrarFormularioContato">Trabalhe Conosco</a>
                </li>                           

        <script type="text/javascript" src="./meu_javascript.js"></script>
            Esse código HTML cria um link "Trabalhe Conosco" que não leva a outra página,
            mas, em vez disso, pode ser usado para acionar a exibição ou ocultação de um
            formulário de contato quando é clicado, usando código JavaScript. O 
            ID "mostrarFormularioContato" é usado para conectar o link ao código 
            JavaScript que controla o formulário de contato.
		
Segue o JS:
// Obtém os elementos do DOM
const formularioContato = document.getElementById("formulario-contato");
const mostrarFormularioContato = document.getElementById("mostrarFormularioContato");

// Adiciona um evento de clique ao link "Contato"
mostrarFormularioContato.addEventListener("click", function () {
    // Verifica o estado atual do formulário e alterna entre mostrar e ocultar
    if (formularioContato.style.display === "none" || formularioContato.style.display === "") {
        formularioContato.style.display = "block";
    } else {
        formularioContato.style.display = "none";
    }
});		