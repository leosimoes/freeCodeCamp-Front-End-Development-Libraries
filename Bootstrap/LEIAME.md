# freecodecamp - Bibliotecas de desenvolvimento em front-end - Bootstrap

O Bootstrap é um framework de front-end usado para projetar páginas da web e aplicativos responsivos. 
Ele adota uma abordagem mobile-first para o desenvolvimento na web e inclui estilos e classes CSS pré-construídos, 
além de algumas funcionalidades JavaScript.

Neste curso, você aprenderá a criar sites responsivos com Bootstrap, 
e usará as classes que ele tem para estilizar botões, imagens, formulários, navegação e outros elementos comuns.


### Usar design responsivo com contêineres fluidos do Bootstrap

Usar design responsivo com contêineres fluidos do Bootstrap
Na seção do HTML5 e CSS do freeCodeCamp nós construímos uma aplicação de Fotos de Gatos. 

Agora vamos voltar para ela. 
Dessa vez, nós estilizaremos usando o framework de CSS responsivo popular conhecido como Bootstrap.

O Bootstrap descobrirá a largura da tela e responderá redimensionando os elementos do HTML - 
daí o nome design responsivo.

Com um design responsivo, não há necessidade de projetar uma versão móvel do seu site. 
Ele terá uma boa aparência em dispositivos com telas de qualquer largura.

Você pode incluir o Bootstrap em qualquer aplicativo, adicionando o seguinte código ao topo do HTML:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" 
      integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" 
      crossorigin="anonymous"/>
```

Neste caso, já o adicionamos para você a esta página por trás dos panos. 
Note que usar a tag > ou /> para fechar a tag link é aceitável.

Para começar, devemos aninhar todo o HTML (exceto a tag link e o elemento style) em um elemento div com a 
classe container-fluid.

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
      integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u"
      crossorigin="anonymous"/>
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css"/>
<style>
    .red-text {
        color: red;
    }

    h2 {
        font-family: Lobster, Monospace;
    }

    p {
        font-size: 16px;
        font-family: Monospace;
    }

    .thick-green-border {
        border-color: green;
        border-width: 10px;
        border-style: solid;
        border-radius: 50%;
    }

    .smaller-image {
        width: 100px;
    }
</style>
<div class="container-fluid">
    <h2 class="red-text">CatPhotoApp</h2>

    <p>Click here for <a href="#">cat photos</a>.</p>

    <a href="#">
        <img class="smaller-image thick-green-border" 
             src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" 
             alt="A cute orange cat lying on its back.">
    </a>

    <p>Things cats love:</p>
    <ul>
        <li>cat nip</li>
        <li>laser pointers</li>
        <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
        <li>flea treatment</li>
        <li>thunder</li>
        <li>other cats</li>
    </ol>
    <form action="https://freecatphotoapp.com/submit-cat-photo">
        <label><input type="radio" name="indoor-outdoor"> Indoor</label>
        <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
        <label><input type="checkbox" name="personality"> Loving</label>
        <label><input type="checkbox" name="personality"> Lazy</label>
        <label><input type="checkbox" name="personality"> Crazy</label>
        <input type="text" placeholder="cat photo URL" required>
        <button type="submit">Submit</button>
    </form>
</div>
```

Testes:
- O elemento div deve ter a classe container-fluid.
- Aguardando:O elemento div deve ter uma tag de fechamento.
- Aguardando:Todos os elementos HTML após a tag de fechamento style devem estar aninhados dentro de .container-fluid.


### Tornar imagens responsivas a dispositivos móveis

Primeiro, adicione uma nova imagem abaixo da existente. 
Defina o seu atributo src como `https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg`.

Seria ótimo se essa imagem pudesse ser exatamente do tamanho da nossa tela do celular.

Felizmente, com o Bootstrap, tudo que precisamos fazer é adicionar a classe `img-responsive` para a nossa imagem. 
Faça isso, e a imagem deve encaixar perfeitamente na largura da página.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" class="img-responsive"/>
```

Testes
- Você deve ter o total de duas imagens.
- A nova imagem deve estar abaixo da antiga e ter a classe img-responsive.
- A nova imagem não deve ter a classe smaller-image.
- A nova imagem deve ter um src de `https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg`.
- O novo elemento img deve ter uma tag de fechamento.


### Centralizar o texto com Bootstrap

Agora que estamos usando Bootstrap, podemos centralizar nossos elementos de cabeçalho para deixá-los com melhor aparência. 
Tudo que precisamos fazer é adicionar a classe text-center ao nosso elemento h2.

Lembre-se de que você pode adicionar várias classes ao mesmo elemento separando cada uma delas com um espaço, assim:

```html
<h2 class="red-text text-center">your text</h2>
```

Testes:
- O elemento h2 deve estar centralizado ao aplicar a classe `text-center`;
- O elemento h2 ainda deve ter a classe `red-text`.


### Criar um botão do Bootstrap

O Bootstrap possui seus próprios estilos para elementos button, os quais ficam muito melhores do que aqueles 
botões em HTML puro.

Crie um novo elemento button abaixo da foto grande do gatinho.
Dê a ele as classes btn e btn-default, assim como o texto Like.

```html
<button class="btn btn-default">Like</button>
```

Testes:
- Você deve criar um novo elemento button com o texto Like.
- O novo botão deve ter duas classes: btn e btn-default.
- Todos os elementos button devem ter tags de fechamento.


### Criar um botão de elemento de bloco do Bootstrap

Normalmente, os elementos button com as classes btn e btn-default são apenas tão grandes quanto os textos que 
eles contêm. 

Por exemplo:
```html
<button class="btn btn-default">Submit</button>
```
Este botão seria apenas tão largo quanto a palavra Submit.

Tornando-os elementos de bloco com a classe adicional btn-block, o botão vai esticar para preencher todo o espaço
horizontal da sua página e qualquer elemento seguinte vai fluir para uma nova linha abaixo do bloco.

```html
<button class="btn btn-default btn-block">Submit</button>
```

Esse botão ocuparia 100% da largura disponível.

Note que esses botões ainda precisam da classe btn.

Adicione a classe btn-block do Bootstrap ao botão do Bootstrap.

```html
<button class="btn btn-default btn-block">Like</button>
```

Testes:
- O botão ainda deve ter as classes btn e btn-default.
- O botão deve ter a classe btn-block.
- Todos os seus elementos button devem ter tags de fechamento.


### Experimentar o botão do Bootstrap com as cores do arco-íris

A classe btn-primary tem a cor principal que você utilizará no seu app. 
É útil para destacar ações que você deseja que o usuário faça.

Substitua a classe btn-default do Bootstrap por btn-primary no botão.

Observe que esse botão ainda precisa das classes btn e btn-block.

```html
<button class="btn btn-primary btn-block">Like</button>
```

Testes:
- O botão deve ter a classe btn-primary.
- O botão ainda deve ter as classes btn e btn-block.
- Todos os elementos button devem ter tags de fechamento.


### Chamar ações opcionais com btn-info

O Bootstrap vem com diversas cores predefinidas para botões. 
A classe btn-info é usada para chamar atenção para ações opcionais que o usuário pode tomar.

Crie um botão do Bootstrap com nível de bloco abaixo do botão Like com o texto Info, adicionando a ele a 
classe btn-info do Bootstrap.

Note que esses botões ainda precisam das classes btn e btn-block.

```html
<button class="btn btn-info btn-block">Info</button>
```

Testes
- Você deve criar um novo elemento button com o texto Info.
- Ambos os botões do Bootstrap devem ter as classes btn e btn-block.
- O novo botão deve ter a classe btn-info.
- Todos os elementos button devem ter tags de fechamento.


### Avisar os usuários sobre uma ação perigosa com btn-danger

O Bootstrap vem com diversas cores predefinidas para botões. 
A classe btn-danger é a cor de botão que você usará para notificar seus usuários de que o botão executa uma 
ação destrutiva, como excluir uma foto de gato.

Crie um botão com o texto Delete e dê a ele a classe btn-danger.

Note que esses botões ainda precisam das classes btn e btn-block.

```html
<button class="btn btn-danger btn-block">Delete</button>
```

Testes:
- Você deve criar um novo elemento button com o texto Delete.
- Todos os botões do Bootstrap devem ter as classes btn e btn-block.
- O novo botão deve ter a classe btn-danger.
- Todos os elementos button devem ter tags de fechamento.


### Usar o Bootstrap Grid para colocar elementos lado a lado

Bootstrap usa o sistema responsivo de grid de 12 colunas, o que torna superfácil colocar elementos em linhas 
e especificar cada largura relativa de um elemento. 

A maioria das classes do Bootstrap pode ser aplicada a um elemento div.

O Bootstrap possui atributos de largura de colunas diferentes, que são utilizados dependendo da largura 
da tela do usuário. 

Por exemplo, celulares possuem telas estreitas, enquanto laptops possuem telas mais largas.

Tome como exemplo a classe `col-md-*` do Bootstrap. 
Aqui, md significa médio, e * é um número especificando quantas colunas de largura o elemento deve ter. 
Nesse caso, a largura da coluna de um elemento em uma tela de tamanho mediano, como um laptop, está sendo especificada.

No app de Fotos de Gatos que estamos construindo, utilizaremos `col-xs-*`, onde xs significa extrapequeno 
(como uma tela extrapequena de um telefone móvel), e * é um número de colunas especificando quantas colunas de 
largura o elemento deve ter.

Coloque os botões Like, Info e Delete lado a lado ao aninhar todos os três em um elemento `<div class="row">`. 
Em seguida, coloque cada um deles dentro de um elemento `<div class="col-xs-4">`.

A classe row é aplicada à div. Os próprios botões podem ser aninhados dentro dela.

```html
<div class="row">
    <div class="col-xs-4">
        <button class="btn btn-primary btn-block">Like</button>
    </div>
     <div class="col-xs-4">
        <button class="btn btn-info btn-block">Info</button>
    </div>
    <div class="col-xs-4">
        <button class="btn btn-danger btn-block">Delete</button>
    </div>
</div>
```

Testes:
- Os botões devem estar aninhados dentro do mesmo elemento div com a classe row.
- Cada um dos botões do Bootstrap deve estar aninhado dentro do próprio elemento div com a classe col-xs-4.
- Cada um dos elementos button deve ter uma tag de fechamento.
- Cada um dos elementos div deve ter uma tag de fechamento.


### Limpar o CSS customizado para o Bootstrap

Nós podemos limpar nosso código e fazer o aplicativo de fotos de gato parecer mais convencional ao utilizar os 
estilos nativos do Bootstrap ao invés dos estilos customizados que criamos mais cedo.

Não se preocupe - haverá muito tempo para customizar nosso CSS depois.

Exclua as declarações CSS `.red-text`, `p` e `.smaller-image` do elemento style para que as únicas declarações restantes
no elemento style sejam `h2` e `thick-green-border`.

Em seguida, exclua o elemento p que contem um link morto. 
Depois disso, remova a classe `red-text` do elemento h2 e substitua-a pela classe `text-primary` do Bootstrap.

Finalmente, remova a classe `smaller-image` do primeiro elemento img e substitua-a pela classe `img-responsive`.

Testes:
- O elemento h2 não deve mais conter a classe red-text.
- O elemento h2 deve ter agora a classe text-primary.
- Os elementos de parágrafo não devem mais usar a fonte Monospace.
- A classe smaller-image deve ser removida da imagem superior.
- Você deve adicionar a classe img-responsive à imagem superior.


### Usar um span para apontar para elementos na mesma linha

Você pode usar spans para criar elementos na mesma linha. 
Lembra-se de quando usamos a classe btn-block para fazer o botão preencher toda a linha?

Isso ilustra a diferença entre um elemento "em linha" (inline) e de um elemento de "bloco" (block).

Ao usar o elemento inline span, você pode colocar diversos elementos na mesma linha, e até estilizar diferentes 
partes da mesma linha de forma diferente.

Usando um elemento span, aninhe a palavra love dentro do elemento p que atualmente possui o texto Things cats love. 
Em seguida, dê ao span a classe `text-danger` para tornar o texto vermelho.

Aqui está como você faria isso para o elemento p que possui o texto Top 3 things cats hate:

```html
<p>Top 3 things cats <span class="text-danger">hate:</span></p>
```

```html
<p>Things cats <span class="text-danger">love</span>:</p>
```

Testes:
- O elemento span deve estar dentro do elemento p.
- O elemento span deve ter apenas o texto love.
- O elemento span deve ter a classe text-danger.
- O elemento span deve ter uma tag de fechamento.


### Criar um título personalizado

Vamos fazer um título simples para nossa foto de gato ao colocar na mesma linha o título e a imagem do gato relaxando.

Lembre-se: o Bootstrap usa o sistema de grade responsiva, o que torna fácil colocar elementos em linha e 
especificar cada largura relativa de um elemento. 

A maioria das classes do Bootstrap podem ser aplicadas a um elemento div.

Aninhe sua primeira imagem e seu elemento h2 dentro de um único elemento `<div class="row">`. 

Aninhe o seu elemento h2 dentro de uma `<div class="col-xs-8">` e sua imagem em uma `<div class="col-xs-4">`
para que eles estejam na mesma linha.

Notou como a imagem agora está no tamanho exato para encaixar com o texto?

```html
<div class="row">
    <div class="col-xs-8">
        <h2 class="text-primary text-center">CatPhotoApp</h2>
    </div>
    <div class="col-xs-4">
        <a href="#">
            <img class="img-responsive thick-green-border"
                 src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg"
                 alt="A cute orange cat lying on its back."/>
        </a>
    </div>
</div>
```

Testes:
- O elemento h2 e o elemento img mais acima devem estar aninhados juntos dentro de um elemento div com a classe row.
- O elemento img superior deve estar aninhado dentro de uma div com a classe col-xs-4.
- O elemento h2 deve estar aninhado dentro de uma div com a classe col-xs-8.
- Todos os elementos div devem ter tags de fechamento.

### Adicionar ícones de Font Awesome para nossos botões

Adicionar ícones de Font Awesome para nossos botões
Font Awesome é uma biblioteca conveniente de ícones. 

Estes ícones podem ser fontes da web ou gráficos vetoriais. 
Estes ícones são tratados assim como as fontes. 
Você pode especificar seu tamanho utilizando pixels, e eles assumirão o tamanho de fonte de seus elementos pais no HTML.

Você pode incluir o Font Awesome em qualquer aplicativo, adicionando o seguinte código ao topo do seu HTML:

```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css" 
      integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf" 
      crossorigin="anonymous">
```
Neste caso, já o adicionamos para você a esta página por trás dos panos.

O elemento i foi usado originalmente para fazer outros elementos itálicos, mas agora é comumente usado para ícones. 

Você pode adicionar as classes Font Awesome ao elemento i para transformá-lo em um ícone, por exemplo:
```html
<i class="fas fa-info-circle"></i>
```

Observe que o elemento span também é aceitável para uso com ícones.

Use o Font Awesome para adicionar um ícone thumbs-up ao botão like, 
doando-o um elemento i com as classes `fas` e `fa-thumbs-up`. 
Certifique-se de manter o texto Like ao lado do ícone.

```html
<button class="btn btn-primary btn-block">
    <i class="fas e fa-thumbs-up">Like</i>
</button>
```

Testes:
- Você deve adicionar um elemento i com as classes fas e fa-thumbs-up.
- O ícone fa-thumbs-up deve estar localizado dentro do botão Like.
- O elemento i deve estar dentro do novo elemento button.
- O elemento de ícone deve ter uma tag de fechamento.


### Adicionar ícones de Font Awesome para todos os botões

Font Awesome é uma biblioteca conveniente de ícones. 
Estes ícones podem ser fontes da web ou gráficos vetoriais. 
Estes ícones são tratados assim como as fontes. 
Você pode especificar seu tamanho utilizando pixels, e eles assumirão o tamanho de fonte de seus elementos pais no HTML.

Utilize Font Awesome para adicionar um ícone info-circle ao botão de informação e um ícone trash para o botão de deleção.

Observação: você pode usar os elementos i ou span para concluir este desafio.

```html
<div class="col-xs-4">
    <button class="btn btn-info btn-block">
        <i class="fas fa-info-circle">Info</i>
    </button>
</div>
<div class="col-xs-4">
    <button class="btn btn-danger btn-block">
        <i class="fas fa-trash">Delete</i>
    </button>
</div>
```

Testes:
- Você deve adicionar um `<i class="fas fa-info-circle"></i>` dentro do elemento de botão info.
- Você deve adicionar um `<i class="fas fa-trash"></i>` dentro do elemento de botão delete.
- Cada um dos elementos i deve ter uma tag de fechamento e `<i class="fas fa-thumbs-up"></i>` está no elemento de 
botão like.


### Criar botões de opção de estilo responsivo

Você pode usar as classes `col-xs-*` do Bootstrap nos elementos do form também! 
Dessa forma, nossos botões de opção vão estar simetricamente distribuídos pela página, 
independente da largura da resolução da tela.

Aninhe os botões de opção dentro de um elemento `<div class="row">`. 
Em seguida, aninhe cada um deles dentro de um elemento `<div class="col-xs-6">`.

Observação: como um lembrete, os botões de opção são elementos input do tipo radio.

```html
<div class="row">
    <div class="col-xs-6">
        <label><input type="radio" name="indoor-outdoor"> Indoor</label>
    </div>
    <div class="col-xs-6">
        <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
    </div>
</div>
```

Testes:
- Todos os botões de opção devem estar aninhados dentro de uma div com a classe `row`.
- Cada um dos botões de opção devem estar aninhados nas próprias div com a classe `col-xs-6`.
- Todos os elementos div devem ter tags de fechamento.


### Compreender caixas de seleção responsivas

Já que as classes `col-xs-*` do Bootstrap são aplicáveis a todos os elementos de form, 
você também pode usá-las nas caixas de seleções! 

Dessa forma, as caixas de seleções vão estar simetricamente distribuídas pela página, 
independente da largura da resolução da tela.

Aninhe as três caixas de seleção em um elemento `<div class="row">`. 
Então aninhe cada uma deles no elemento `<div class="col-xs-4">`.

```html
<div class="row">
    <div class="col-xs-4">
        <label><input type="checkbox" name="personality"> Loving</label>
    </div>
    <div class="col-xs-4">
        <label><input type="checkbox" name="personality"> Lazy</label>
    </div>
    <div class="col-xs-4">
        <label><input type="checkbox" name="personality"> Crazy</label>
    </div>
</div>
```

Testes:
- Todas as caixas de seleção devem estar aninhadas dentro de uma div com a classe row.
- Cada uma das caixas de seleção devem estar aninhadas dentro da própria div com a classe `col-xs-4`.
- Todos os elementos div devem ter tags de fechamento.


### Estilizar inputs de texto como controles de formulário

Você pode adicionar o ícone do Font Awesome `fa-paper-plane` incluindo `<i class="fa fa-paper-plane"></i>` 
dentro do elemento button de envio.

Dê ao campo de input de texto do formulário a classe `form-control`. 
Dê ao botão de envio do formulário as classes `btn btn-primary`. 
Também dê a esse botão o ícone do Font Awesome `fa-paper-plane`.

Todo texto dos elementos `<input>`, `<textarea>` e `<select>` com a classe `.form-control` possuem largura de 100%.


```html
<input type="text" placeholder="cat photo URL" class="form-control" required/>
<button type="submit" class="btn btn-primary">
    <i class="fa fa-paper-plane">Submit</i>
</button>
```

Testes:
- O botão de envio no seu formulário deve ter a classe `btn btn-primary`.
- Você deve adicionar uma `<i class="fa fa-paper-plane"></i>` dentro do elemento button de envio.
- O input de texto no formulário deve ter a classe `form-control`.
- Todos os seus elementos i devem ter uma tag de fechamento.


### Alinhar os elementos de formulário de maneira responsiva com o Bootstrap

Agora vamos colocar o input e o button de envio do formulário na mesma linha. 
Faremos isso da mesma forma que fizemos antes: 
usando um elemento div com a classe row e outros elementos div dentro do primeiro div usando a classe `col-xs-*`.

Aninhe o input de texto e o button de envio do formulário dentro de uma div com a classe `row`. 
Aninhe o texto do input do formulário dentro de uma div com a classe `col-xs-7`. 
Aninhe o button de envio do formulário em uma div com a classe `col-xs-5`.

Esse é o último desafio que faremos para nossa aplicação de fotos de gatos por agora. 
Esperamos que você tenha gostado de aprender Font Awesome, Bootstrap e design responsivo!

```html
<div class="row">
    <div class="col-xs-7">
        <input type="text" placeholder="cat photo URL" class="form-control" required/>
    </div>
    <div class="col-xs-5">
        <button type="submit" class="btn btn-primary">
            <i class="fa fa-paper-plane">Submit</i>
        </button>
    </div>
</div>
```

Testes:
- O botão de envio e o input de texto do formulário devem estar aninhados dentro de uma div com a classe `row`.
- O input de texto do formulário deve estar aninhado dentro de uma div com a classe `col-xs-7`.
- O botão de envio do formulário deve estar aninhado dentro de uma div com a classe `col-xs-5`.
- Todos os elementos div devem ter tags de fechamento.


### Criar um título com Bootstrap

Agora vamos construir algo do zero para praticar nossa habilidade em HTML, CSS e Bootstrap.

Vamos construir um playground jQuery, o qual vamos colocar em uso em breve nos desafios de jQuery.

Para começar, crie um elemento h3, com o texto jQuery Playground.

Dê ao elemento h3 uma cor com a classe text-primary, e centralize-o com a classe text-center do Bootstrap.

```html
<h3 class="text-primary text-center">jQuery Playground</h3>
```

Testes
- Você deve adicionar um elemento h3 à página.
- O elemento h3 deve ter uma tag de fechamento.
- O elemento h3 deve ser colorido ao aplicar a classe `text-primary`
- O elemento h3 deve ser centralizado ao aplicar a classe `text-center`
- O elemento h3 deve ter o texto jQuery Playground.

### Hospedar nossa página em um div de contêiner fluido do Bootstrap

Agora, vamos garantir que todo o conteúdo na sua página seja responsivo a dispositivo móveis.

Vamos aninhar nosso elemento h3 dentro de um elemento div com a classe `container-fluid`.

```html
<div class="container-fluid">
    <h3 class="text-primary text-center">jQuery Playground</h3>
</div>
```

Testes:
- O elemento div teve ter a classe container-fluid.
- Cada um de seus elementos div deve ter tags de fechamento.
- O elemento h3 deve estar aninhando dentro de um elemento div.


### Criar uma linha do Bootstrap

Agora vamos criar uma linha do Bootstrap para nossos elementos em linha.

Crie um elemento div abaixo da tag h3, com a classe `row`.

```html
```

Testes:
- Você deve adicionar o elemento div abaixo do elemento h3.
- O elemento div deve ter a classe row
- O row div deve estar aninhado dentro de container-fluid div
- O elemento div deve ter uma tag de fechamento.


### Dividir sua linha do Bootstrap

Agora que nós temos uma linha do Bootstrap, vamos dividi-la em duas colunas para hospedar nossos elementos.

Crie dois elementos div dentro da linha (row), ambos com a classe `col-xs-6`.

```html
<div class="row">
    <div class="col-xs-6"></div>
    <div class="col-xs-6"></div>
</div>
```

Testes:
- Dois elementos `div class="col-xs-6"` devem estar aninhados dentro do elemento `div class="row"`.
- Todos os elementos div devem ter tags de fechamento.


### Criar poços do Bootstrap

O Bootstrap tem uma classe chamada well que pode criar uma sensação visual de profundidade para suas colunas.

Aninhe um elemento div com a classe well dentro de cada um de seus elementos col-xs-6 div.

```html
    <div class="row">
    <div class="col-xs-6">
        <div class="well"></div>
    </div>
    <div class="col-xs-6">
        <div class="well"></div>
    </div>
</div>
```

Testes:
- Você deve adicionar um elemento div com a classe `well` dentro de cada um dos elementos `div com a classe col-xs-6`
- Ambos os elementos div com a classe `col-xs-6` devem estar aninhados dentro do elemento `div com a classe row`.
- Todos os elementos div devem ter tags de fechamento.


### Adicionar elementos aos poços no Bootstrap

Agora estamos na profundidade de diversos elementos div em cada coluna da nossa linha. 
Isso é tão profundo quanto precisamos ir. Agora podemos adicionar nossos elementos button.

Aninhe três elementos button dentro de cada um dos elementos div contendo o nome de classe well.

```html
<div class="col-xs-6">
    <div class="well">
        <button></button>
        <button></button>
        <button></button>
    </div>
</div>
<div class="col-xs-6">
    <div class="well">
        <button></button>
        <button></button>
        <button></button>
    </div>
</div>
```

Testes:
- Três elementos button devem ser aninhados dentro de cada um dos elementos div com a classe well.
- Você deve ter o total de 6 elementos button.
- Todos os elementos button devem ter tags de fechamento.


### Aplicar o estilo de botão padrão do Bootstrap

O Bootstrap tem outra classe de botão chamada btn-default.

Aplique ambas as classes btn e btn-default a cada um dos elementos button.

```html
 <div class="row">
    <div class="col-xs-6">
        <div class="well">
            <button class="btn btn-default"></button>
            <button class="btn btn-default"></button>
            <button class="btn btn-default"></button>
        </div>
    </div>
    <div class="col-xs-6">
        <div class="well">
            <button class="btn btn-default"></button>
            <button class="btn btn-default"></button>
            <button class="btn btn-default"></button>
        </div>
    </div>
</div>
```

Testes:
- Você deve aplicar a classe btn para cada um dos elementos button.
- Você deve aplicar a classe btn-default para cada um dos elementos button.


### Criar uma classe para selecionar com jQuery Selectors

Nem todas as classes precisam ter um CSS correspondente. 
Às vezes, criamos classes apenas com o propósito de selecionar esses elementos de forma mais fácil usando o jQuery.

Dê a cada um dos elementos button a classe target.

```html
<div class="row">
    <div class="col-xs-6">
        <div class="well">
            <button class="btn btn-default target"></button>
            <button class="btn btn-default target"></button>
            <button class="btn btn-default target"></button>
        </div>
    </div>
    <div class="col-xs-6">
        <div class="well">
            <button class="btn btn-default target"></button>
            <button class="btn btn-default target"></button>
            <button class="btn btn-default target"></button>
        </div>
    </div>
</div>
```

Testes
- Você deve aplicar a classe target para cada um dos elementos button.


## Adicionar atributos id aos elementos do Bootstrap

Lembre-se de que, além dos atributos de classe, você pode dar a cada um de seus elementos um atributo id.

Cada id precisa ser único para um elemento específico e utilizado apenas uma vez por página.

Vamos dar um id único para cada um de nossos elementos div com classe well.

Lembre-se de que você pode dar um id a um elemento dessa forma:

```html
<div class="well" id="center-well">
```

Dê ao poço à esquerda o id left-well. Dê ao poço à direita o id right-well.

```html
<div class="well" id="left-well"></div>
<div class="well" id="right-well"></div>
```

Testes:
- O well da esquerda deve ter o id left-well.
- O well da direita deve ter o id right-well.


### Dar um label aos poços do Bootstrap

Para deixar claro, vamos rotular nossos dois poços com seus ids.

Acima do poço da esquerda, dentro do elemento col-xs-6 div, adicione um elemento h4 com o texto #left-well.

Acima do poço da direita, dentro do elemento col-xs-6 div, adicione um elemento h4 com o texto #right-well.

```html
<h4>#left-well</h4>
<h4>#right-well</h4>
```

Testes:
- Você deve adicionar um elemento h4 para cada um dos elementos `<div class="col-xs-6">`.
- Um elemento h4 deve ter o texto #left-well.
- Um elemento h4 deve ter o texto #right-well.
- Todos os elementos h4 devem ter tags de fechamento.


### Dar a cada elemento um id único

Nós também queremos ser capazes de usar jQuery para selecionar cada botão a partir do seu id único.

Dê a cada um dos botões um id único, começando com target1 e terminando com target6.

Certifique-se de que target1 até target3 estão em #left-well, e target4 até target6 estão em #right-well.

```html
<div class="row">
    <div class="col-xs-6">
        <h4>#left-well</h4>
        <div class="well" id="left-well">
            <button class="btn btn-default target" id="target1"></button>
            <button class="btn btn-default target" id="target2"></button>
            <button class="btn btn-default target" id="target3"></button>
        </div>
    </div>
    <div class="col-xs-6">
        <h4>#right-well</h4>
        <div class="well" id="right-well">
            <button class="btn btn-default target" id="target4"></button>
            <button class="btn btn-default target" id="target5"></button>
            <button class="btn btn-default target" id="target6"></button>
        </div>
    </div>
</div>
```

Testes:
- Um elemento button teve ter o id target1.
- Um elemento button teve ter o id target2.
- Um elemento button teve ter o id target3.
- Um elemento button teve ter o id target4.
- Um elemento button teve ter o id target5.
- Um elemento button teve ter o id target6.


### Dar um label a botões do Bootstrap

Assim como fizemos com nossos poços, queremos também dar um label aos nossos botões.

Dê a cada um de seus elementos button o texto que corresponde ao seu seletor id.

```html
        <div class="row">
    <div class="col-xs-6">
        <h4>#left-well</h4>
        <div class="well" id="left-well">
            <button class="btn btn-default target" id="target1">#target1</button>
            <button class="btn btn-default target" id="target2">#target2</button>
            <button class="btn btn-default target" id="target3">#target3</button>
        </div>
    </div>
    <div class="col-xs-6">
        <h4>#right-well</h4>
        <div class="well" id="right-well">
            <button class="btn btn-default target" id="target4">#target4</button>
            <button class="btn btn-default target" id="target5">#target5</button>
            <button class="btn btn-default target" id="target6">#target6</button>
        </div>
    </div>
</div>
```

Testes:
- O elemento button com o id target1 deve ter o texto #target1.
- O elemento button com o id target2 deve ter o texto #target2.
- O elemento button com o id target3 deve ter o texto #target3.
- O elemento button com o id target4 deve ter o texto #target4.
- Seu elemento button com o id target5 deve ter o texto #target5.
- Seu elemento button com o id target6 deve ter o texto #target6.


### Usar comentários para deixar o código mais claro

Quando começarmos a usar jQuery, nós modificaremos os elementos do HTML sem a necessidade 
de realmente alterá-los no HTML.

Vamos ter certeza de que todo mundo sabe que eles não deveriam realmente modificar nenhum desse código diretamente.

Lembre-se de que você pode ` iniciar um comentário com <!-- e terminar um comentário com -->`

Adicione um comentário no topo do HTML, que diga Code below this line should not be changed

```html
<!--Code below this line should not be changed-->
```

Testes: 
- Você deve começar um `comentário com <!--` no topo do HTML.
- O comentário deve ter o texto Code below this line should not be changed.
- Você deve fechar o `comentário com -->`.
- Você deve ter o mesmo número de aberturas e fechamentos de comentários.


## Observações
Import bootstrap com a tag link;
Colocar todo o código do body dentro de uma div com a classe `container-fluid`;
Criar imagens responsivas com a classe `img-responsive`;
Criar button com classe `btn` seguido de outras classes para cor e bloco;
Criar div com classe row, e dentro delas colocar div com classes para definir as colunas cujo total deve ser 12.


## Referências
https://www.freecodecamp.org/portuguese/learn/front-end-development-libraries/