# dog-api

document.querySelector('button').addEventListener('click', function () {
  fetch('https://dog.ceo/api/breeds/image/random')
    .then((response) => {
      return response.json();
    })
    .then((myContent) => {
      myImage.src = myContent['message'];
    });
},);



Explicação:



document.querySelector -> seleciona o documento a ser lido, no caso o botão ('button') .addEventListener('click', function ()) cria uma função que gera um evento 
chamado click ao se acionar o botão

fecth() acessa o endereço da API para utilizar o conteúdo de lá

.then() informa o que fazer depois de acessar a API, (response)=> cria uma função que solicita a devolução das informações da API no formato json e o
return response.json() armazena as informações acessadas e organizadas em json recebidas da API para devolver ao browser os valores encontrados e selecionados

o segundo .then(myContent)=> cria a função que busca a informação que recebeu o id="myImage" no HTML,   myImage.src = myContent['message']; busca o documento no HTML atribui
no id o arquivo com nome correspondente na API

O que foi feito?

A proposta é criar um botão que realiza uma pesquisa de informações em uma API e devolve uma imagem, o botão foi criado no HTML e recebeu um id, em outro documento criamos
um arquivo em JS que acessa o HTML, seleciona o botão, cria um evento ao ser clicado, esse evento pertencce a uma função, que acessa uma API atravez do método fetch, que
recebe o endereço que contem os dados a serem acessado e impressos no browser, posteriormente, criou-se uma função que organiza as informações com base no json o que
facilita a interpretação e devolução dos itens a serem mostrados na tela, em seguida se cria uma função que procura onde está o id que recebera o que foi encontrado
na API e realiza essa atribuição de valores.
