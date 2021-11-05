### Medidas

#### Medidas Absolutas

São medidas que não dependem de um valor de referência, essas unidades são fixas e não mudam de acordo com as especificações do dispositivo. 

Medidas absolutas: Pixel, Centímetro, Metro...


#### Medidas Relativas
Essas medidas são calculadas tendo como base uma outra unidade de medida definida.

Medidas relativas: em, rem...

##### ( em e rem )

Essas unidades facilitam a criação de layout fluídos e responsivos. Ela tem como referência o `font-size` do elemento pai.


```html
    <style>
        #div{
            font-size: 16px;
        }

        #filho{
            font-size: 2em;
        }
    </style>

    <div id="pai">
        div pai
        <div id="filho">
            div filho
        </div>
    </div>
```

Na div pai temos `font-size: 16px`, como o (em) toma como referência o tamanho da fonte do elemento pai, na div filho temos `1em = 16px`, seguindo a lógica `2em = 32px` e assim por diante.

###### Um pequeno problema ao usar ( em )!
Existe um problema ao usar ( em ) em muitos elementos aninhados, pois o elemento filho sempre terá referência do `font-size` do seu pai. Então se tivéssemos uma terceira div filho, 1em seria 32px pois seu elemento pai está configurado com `font-size: 2em`.

Para resolver esse problema, temos a unidade de medida (rem) ela utiliza a mesma lógica, pegando como referência o `font-size` do elemento pai, mas apenas do elemento root do html.

```html
    <style>
        :root {
            font-size: 16px;
        }

        #div{
            font-size: 1em;
        }

        #filho{
            font-size: 2em;
        }
    </style>

    <div id="pai">
        div pai
        <div id="filho">
            div filho
        </div>
    </div>
```

Então com o tamanho da fonte definido no root, todos os elementos filhos terão como base `1em = 16px`.
Existe uma forma de representar as medidas com um calculo mais fácil, definindo: `font-size: 62.5%` no root, apartir daí `1rem = 10px, 1.2rem: 12px`... sempre multiplicando por 10.