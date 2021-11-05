### Requisições HTTP

#### O que é AJAX e como funciona

AJAX significa Asynchronous JavaScript and XML, é um conjunto de técnicas que permite que aplicações trabalhem de modo assíncrono, processando qualquer requisição ao servidor em segundo plano.

*XML* -  é uma variação de linguagem de marcação no estilo do HTML, o XML armazena dados e transmite, enquanto o HTML exibe os dados.

##### Comparação
| Modelo convencional | Modelo AJAX |
------------------- | -----------
| 1. Uma requisição HTTP é enviada do navegador para o servidor. | 1. O navegador gera uma chamada do JavaScript que então ativa o XMLHttpRequest. |
| 2. O servidor recebe a requisição e busca os dados. | 2. Em segundo plano o navegador cria uma requisição HTTP para o servidor. |
| 3. O servidor envia os dados requisitados para o navegador. | 3. O servidor recebe a requisição, busca os dados e envia para o navegador. |
| 4. O navegador recebe os dados e recarrega a página para fazer com que apareçam. | 4. O navegador recebe os dados requisitados que irão aparecer imediatamente na página. Não é necessário recarregar. |


#### Fetch API
A Fetch API veio para substituir a antiga XmlHttpRequest.

~~~js 
    fetch('https://api.github.com/search/repositories?q=javascript')
    .then(response => response.json())
~~~

O parametro obrigatório do `fetch()` é uma string com a URL de onde irá fazer a requisição.
O `fetch` retorna uma promisse que retorna um objeto `response` com informações da resposta do servidor 

#### Configurando a requisição

O `fetch()` aceita um segundo parâmetro, onde podemos passar um objeto de configuração. É nele onde indicamos o método da requisição, cabeçalho, corpo, etc.

~~~js 
    fetch('https://myexample.com', {
        method: 'POST',
        headers: {'Content-Type':'application/x-www-form-urlencoded'}, 
        body: 'foo=bar&blah=1'
    })
    .then(response => response.json())
~~~
* method - GET | POST | PUT | DELETE | HEAD
* url - URL da requisição
* headers - cabeçalho
* body - corpo da requisição
* referrer - referência da requisição
* mode - cors | no-cors | same-origin
* credentials - indica se os cookies devem ser enviados junto com a requisição
* redirect - follow | error | manual
* integrity - valor de integridade da fonte
* cache - modo do cache (default | reload | no-cache)