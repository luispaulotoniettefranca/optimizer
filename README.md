
###### Optimizer is a component of website optimization for search engines and social networks. Simplified and straight to the point it creates the necessary tags and links in your ***head*** for the best search and sharing result.

Optimizer é um componente de otimização de sites para motores de buscas e redes sociais. Simplificado e direto ao ponto ele cria as tags e links necessários em sua ***head*** para o melhor resultado de busca e compartilhamento.


### Highlights

- Simple composer for dynamic data (Compositor simples para dados dinâmicos)
- Author and publisher settings for Facebook (Configuração de autor e publicador para Facebook)
- Quickly configure TwitterCard data for sharing cards (Configure rapidamente os dados TwitterCard para cartões de compartilhamento)
- Quickly configure OpenGraph data for social sharing. (Configure rapidamente os dados OpenGraph para compartilhamento social.)
- Add FacebookAdmins or FacebookAppId and everything is ready (Adiciona FacebookAdmins ou FacebookAppId e tudo fica pronto)
- Composer ready and PSR-2 compliant (Pronto para o composer e compatível com PSR-2)

## Installation

Optimizer is available via Composer:

```bash
"toniette/optimizer": "2.0.*"
```

or run

```bash
composer require toniette/optimizer
```

## Documentation

###### For details on how to use the optimizer, see the sample folder with details in the component directory

Para mais detalhes sobre como usar o optimizer, veja a pasta de exemplo com detalhes no diretório do componente

#### @optimize

```php
<?php
require __DIR__ . "/../vendor/autoload.php";

$op = new \Toniette\Optimizer\Optimizer();

echo $op->optimize(
    "Optimizer Happy and @Toniette",
    "Is a compact and easy-to-use tag creator to optimize your site",
    "https://www.foo.bar.com/toniette/optimizer/example/",
    "https://www.foo.bar.br/uploads/images/2017/11/02-1511276983.jpg"
)->render();
```


#### @publisher

```php
<?php
require __DIR__ . "/../vendor/autoload.php";

$op = new \Toniette\Optimizer\Optimizer();

echo $op->publisher(
  "toniette",
  "luispaulo"
)->render();
```

##### Result @publisher

````html
<meta property="article:publisher" content="https://www.facebook.com/toniette"/>
<meta property="article:author" content="https://www.facebook.com/luispaulo"/>
````

#### @twitterCard

```php
<?php
require __DIR__ . "/../vendor/autoload.php";

$op = new \Toniette\Optimizer\Optimizer();

echo $op->twitterCard(
  "@toniette",
  "@luis",
  "foo.com.br",
  "summary_large_image"
)->render();
```

#### @openGraph

```php
<?php
require __DIR__ . "/../vendor/autoload.php";

$op = new \Toniette\Optimizer\Optimizer();

echo $op->openGraph(
  "toniette",
  "pt_BR",
  "article"
)->render();
```

##### Result @openGraph

````html
<meta property="og:type" content="article"/>
<meta property="og:site_name" content="toniette"/>
<meta property="og:locale" content="pt_BR"/>
````

## Contributing

Please see [CONTRIBUTING](https://github.com/robsonvleite/optimizer/blob/master/CONTRIBUTING.md) for details.