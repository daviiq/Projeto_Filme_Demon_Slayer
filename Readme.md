# Demon Slayer: Castelo Infinito

Este projeto é um site feito em **HTML e CSS** que apresenta informações sobre o filme *Demon Slayer: Kimetsu no Yaiba – Castelo Infinito*.  
O objetivo é mostrar o uso de elementos de estrutura, semântica, estilos e responsividade na construção de páginas web.

------------------------------------------------------------------------------------

## Estrutura do Projeto

O site é dividido em três páginas principais:

1. **index.html** → Página inicial com a sinopse do filme.  
2. **elenco.html** → Mostra o elenco, personagens e equipe de produção.  
3. **extras.html** → Contém curiosidades, trilha sonora e batalhas marcantes.

Além disso, há o arquivo **style.css**, responsável por todo o design e formatação visual.

------------------------------------------------------------------------------------

## Organização

Foram usadas várias Formas de organização para deixar o código mais organizado e acessível:

<header> → Cabeçalho com o título e a imagem principal.

<nav> → Menu de navegação entre as páginas. (Uma estrutura que descobri que com a função de navegação mesmo, ficando mais fácil para criar aquele "header" )

<main> → Conteúdo principal de cada página. (Vai até o footer)

<section> → Divide o conteúdo em partes temáticas, para ficar mais semântico (Diferente da div que também foi utilizada, mas apenas para agrupar, e não para organizar)

<article> → Usado para blocos de conteúdo individual, como sinopse e curiosidades.

<footer> → Rodapé com informações de estúdio, direitos e links.

------------------------------------------------------------------------------------

## Links para navegar

O menu principal usa uma lista de links:

<nav class="main-nav">
    <ul>
        <li><a href="index.html">Sinopse</a></li>
        <li><a href="elenco.html">Elenco & Equipe</a></li>
        <li><a href="extras.html">Batalhas & Extras</a></li>
    </ul>
</nav>

Assim, é possível navegar entre as páginas do site de forma clara

------------------------------------------------------------------------------------

## Imagens

As imagens foram adicionadas com a tag <img> e formatadas via CSS:

<img src="./imagens/demon-slayer-castelo-infinito-capa3.jpg" 
     alt="Capa do filme 3" 
     style="width: 100%;">

Exemplo do Css:

.cast-member img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid #3ab79a;
    margin-bottom: 10px;
}

(Aqui foi utilizado para fazer o círculo em volta das fotos dos atores do elenco, podemos ver por conta das caracteristicas e também da cor utilizada,)

Além disso, é possível ver em <a href="./elenco.html">Elenco</a> a utilização de "<.figure>". Foi utilizado por conta que figure é mais comum para códigos com legendas, o que foi o meu caso.

------------------------------------------------------------------------------------

## Listas

Foram usadas listas em vários momentos:

<ul> (lista não ordenada) para elenco e curiosidades.

<dl> (lista de descrição) para mostrar as batalhas com título e explicação.

Exemplo das Listas usadas no código:

<article class="extras-item ficha-tecnica">
                <h3>Trilha Sonora e Curiosidades </h3>
                <ul class="crew-list">
                    <li><strong>Música:</strong> Aimer & LiSA, cantadas por Yuki Kajiura & Go Shiina </li>
                    <li><strong> Críticas:</strong> <a href="https://www.adorocinema.com/filmes/filme-1000006302/criticas/espectadores/"> clique aqui </a> para acessar as Críticas e Comentários </li>
                    <li><strong>Fenômeno de bilheteria:</strong> "Castelo Infinito" se tornou o filme de anime de maior sucesso na história da América Latina e do Brasil, quebrando recordes de bilheteria.</li>
                    <li><strong>Classificação polêmica:</strong> A classificação indicativa de não recomendado para menores de 18 anos no Brasil devido à violência gráfica. Isso gerou surpresa e confusão, já que o país é o único a adotar essa restrição </li>
                </ul>
            </article>

 <article class="extras-item batalhas">
                <h3>Confrontos Épicos (Spoilers!)</h3>
                <dl class="curiosity-list">
                    <dt>Zenitsu vs. Kaigaku (Lua Superior Seis)</dt>
                    <dd>Um duelo intenso entre antigos discípulos da Respiração do Trovão, focado na superação e no peso da traição.</dd>
                    <dt>Shinobu vs. Doma (Lua Superior Dois)</dt>
                    <dd>A aguardada e trágica batalha de vingança da Hashira do Inseto, um dos momentos mais impactantes do filme.</dd>
                    <dt>Tanjiro e Tomioka vs Akaza (Lua Superior três)</dt>
                    <dd>O confronto mais aguardado de todos ! Será que tanjiro e Tomioka vão conseguir superar a lua que deu o fim em Rengoku?</dd>
                </dl>
                
Exemplo de CSS: 

.curiosity-list {
    margin-top: 15px;
}
.curiosity-list dt {
    font-weight: 800;
    color: #3ab79a;
    margin-top: 10px;
    font-size: 1.1em;
}
.curiosity-list dd {
    margin-left: 20px;
    font-style: italic;
    color: #ccc;
}

------------------------------------------------------------------------------------

## Tema visual

Foi criada uma classe principal chamada .demon-slayer-theme que define o estilo escuro usado em todas as páginas:

body.demon-slayer-theme {
    background-color: #0f0a0a;
    color: #e8e8e8;
    font-family: 'Jost', sans-serif;
}

Assim, fica um tom mais escuro em todas as páginas, e para aplicar apenas puxei no body

<body class="demon-slayer-theme">

------------------------------------------------------------------------------------

## Layout e espaçamento

Usado margin, padding e border-radius para dar espaço e arredondar caixas, deixando o visual mais bonito.
Alguns elementos têm text-align: center; para centralizar textos e imagens.

Exemplo do rodapé:
.main-footer {
    background-color: #000000;
    color: #888;
    padding: 20px 0;
    text-align: center;
    border-top: 5px solid #a00000;
    font-size: 0.9em;
}

------------------------------------------------------------------------------------

## Responsividade

Como já havia feito algumas atividades usando a responsividade, ficou bem mais prático para fazer aqui também.

"<.meta name="viewport" content="width=device-width, initial-scale=1.0">"

Assim ele se adapta de acordo com a tela utilizada, mas também dentro de style.css no final, possui mais detalhes sobre o que foi feito

## Correções feitas pelo Validador W3C
1. As porcentagens (width="100%") foram substituídas por style="width: 100%;".</il> 
2. O tema escuro foi aplicado em todas as páginas com class="demon-slayer-theme".</il> 
3. As imagens e ícones estão organizados na pasta /imagens.</il> 
4. Além disso, tinha algumas divs que estavam criadas sem serem abertas. Isso aconteceu bastante nos tamanhos das imagens, pois acreditva que deveria ficar assim: width:100%> "<./div>" Mas corrigi também.</il> 


------------------------------------------------------------------------------------

## Recursos de HTML Utilizados

## Estrutura básica
Em todos os arquivos há a estrutura padrão do HTML:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>...</title>
    <link rel="stylesheet" href="style.css">
</head>
<body> ... </body>
</html>

------------------------------------------------------------------------------------
