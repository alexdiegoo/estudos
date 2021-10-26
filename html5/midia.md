### Imagens Flexíveis

Adaptar imagens para os sites é muito importante, pois hoje podemos acessar de diversos dispositivos como Desktop, Celular, Tv's. Precisamos carregar imagens com tamanho e resolução de acordo com o tamanho da tela que está acessando nosso site para melhor experiencia do usuário

Para isso usamos as tags `<picture>` e `<source>`

#### Codigo:
~~~html
<picture>
    <source media="(max-width: 750px)" srcset="foto-p.png" type="image/png">
    <source media="(max-width: 1050px)" srcset="foto-m.png" type="image/png">
    <img src="./imagem-g.png" alt="Imagem grande">
</picture>
~~~

A tag `<source>` possui três atributos:
- type: vai indicar o media type da imagem que usamos 
- srcset: vai configurar o nome da imagem que será carregada quando o tamanho indicado for atingido
- media indica o tamanho máximo a ser considerado para carregar a imagem indicada no atributo srcset