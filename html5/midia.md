### Imagens Flexíveis

Adaptar imagens para os sites é muito importante, pois hoje podemos acessar de diversos dispositivos como Desktop, Celular, Tv's. Precisamos carregar imagens com tamanho e resolução de acordo com o tamanho da tela que está acessando nosso site para melhor experiencia do usuário

Para isso usamos as tags `<picture>` e `<source>`

#### Código:
~~~html
<picture>
    <source media="(max-width: 750px)" srcset="foto-p.png" type="image/png">
    <source media="(max-width: 1050px)" srcset="foto-m.png" type="image/png">
    <img src="./imagem-g.png" alt="Imagem flexível">
</picture>
~~~

A tag `<source>` possui três atributos:
- type: vai indicar o media type da imagem que usamos 
- srcset: vai configurar o nome da imagem que será carregada quando o tamanho indicado for atingido
- media indica o tamanho máximo a ser considerado para carregar a imagem indicada no atributo srcset

### Áudio
Para adicionar áudio utilizamos as tags `<audio>` e `<source>`

#### Código
~~~html
<audio preload="metadata" controls autoplay loop>
    <source src="audio01.mp3" type="audio/mpeg">
    <source src="audio01.ogg" type="audio/ogg">
    <source src="audio01.wav" type="audio/wav">
</audio>
~~~

#### Principais atributos da tag audio:
*preload:* indica se o áudio será pré-carregado ou não, aceita três valores:
- *metadata:* vai carregar apenas as informações sobre o arquivo (tamanho, tempo, informações de direitos)
- *none:* não vai carregar nada até que o usuário clique no botão play ou em script inicie a reprodução
- auto (padrão) vai carregar o arquivo de áudio inteiro assim que a página for carregada, mesmo que o usuário nunca aperte o play.

*controls:* vai apresentar o player na tela. Caso não seja colocado na tag `<audio>`, o controle será transparente e o usuário não poderá interagir com ele.

*autoplay:* quando inserido, vai iniciar a reprodução do áudio assim que a página for carregada.

*loop:* vai fazer com que o áudio seja repetido eternamente assim que terminar a reprodução.
