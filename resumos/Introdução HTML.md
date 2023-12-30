# Introdução HTML

Criado em: 16 de dezembro de 2023 21:56

ferramentas 

Vs code 

inspetor de elementos, modo desenvolvedor chrome f12  

# Estrutura Básica HTML

### tags

 <html> abrem a tag 

todo o conteúdo deve estar aqui dentro 

2 partes principais head e body 

   </html> fecha a tag 

### Tags html

<i> itálico 

<p> paragrafo 

<strong> negrito 

pesquisar no ggle mais tags 

### Atributos das Tags

id=”” identifica a tag 

style=””  coloca comando css direto no elemento 

### Textos tipografia html

<h1> Titulo </h1/>

h vem de header que é titulo vai de h1 ate h6 por ordem de tamanho e hierarquia 

<p> paragrafo </p>

<blockquoute> citação </blockquoute>

<u> underline 

<mark > marca texto

<sup> coloca no texto no superior da palavra tipo elevado

### Listas

<ol> lista ordenada (segue ordem numerica)

precisa de tags filhas <li > para colocar os itens da lista 

<ul> lista não ordenada (com bolinhas)

### Links

<a> ancor, ancora um link para algum lugar no texto

href= “exemplo-link” atributo  do a onde vc coloca o link

target=”blanl” abre o link em uma nova aba

target=”sef”  abre o link na mesma aba, comportamento padrao

title=”clique aqui e confira” faz um balazinho ao passar o mouse em cima

# Formulários HTML

## Tag Form

atributos da tag 

name  para identificar 

action=”exemplo-link” envia as informações do formulario para a pag fornecida no link

method=”POST”  encapsula as informações e envia no body de forma de confidencial

method=”GET” manda as informações no url do html. não é seguro pq da pra ler as informacoes no html 

autocomplete=”on” permite o navegador autocompletar os campos com info salvas

autocomplete=”off” não permite o navegador autocompletar os campos com info salvas

onsubmit=”” ativa um envento don JS quando clicar para enviar

### Tag imput

<imput> permite ao usuario fornercer informações 

atributos 

<label> coloca uns rotulos ou etiquetas nos imputs ou tags

type=”” vai dizer os tipo de input

text campo de texto comum, permite tudo

number apenas numeros

min=”0” define o numero minimo como 0

max=”100” define o numero maximo como 100

step=”5” sobe o contador de 5 em 5 

button cria um botão

range cria um campo scroll (barrinha de volume)

Color abre caixa de selecionar cor 

email campo de email (não deixa colocar endereço sem @)

Url campo para botar url

date campo para botar data 

week campo de escolher semana do ano (não funciona no firefox só chrome e edge)

checkbox caixa de seleção de check

radio seleção de um ou outro (ex: masculino ou feminino)

file campo de escolher arquivos 

multiple permite escolher vários arquivos

hidden input escondido no navegador mas é enviado junto do formulário

search campo de busca

### checkbox

no caso de uma lista para marcar mais de um valor (ex: opcional de uma pizzaria) o checkbox vai ficar substitindo os valores pelo ultimo na hora de mandar para o servidor 

para evitar isso use a tag name no input e coloque com colchetes como se fosse uma lista, tipo um array tipo:

name=”opcional[ ]” 

### radio button

as vezes ele buga e permite selecionar mais de um valor onde não deveria

para evitar isso no atributo name coloque o mesmo  nome em todas as opções 

disable torna a opção inacessivel 

### button

types=” “

button apenas um botão clicável n faz nada sem JS

reset limpa todos os campos do Form

submit envia as informações do form

ele ativa com botão enter tmb

onsubmit chama a função JS mt quando faz o submit muito usado pra validar se os dados estão corretos antes de mandar por exemplo

### Select box

tag <select>

faz uma lista de valores para o usuário selecionar

multiple muda pra conseguir selecionar vario elementos da lista  

### textarea

tag <textarea> 

campo de texto maior para o usuário utilizar 

atributos 

rows define o numero de linhas

cols numero de colunas na vertical

# Formatando textos

<p> paragrafo </p>

<strong> negrito, texto mais destacado </strong>

<i> itálico </i>

<b> bold, negrito </b> 

<u> underline </u>

<mark> marca texto </mark>

<sup> bota elevado em cima do texto </sup>

<sub> bota embaixo do text  </sub>

<blockquoute> da um espaçamento no texto,  faz uma citação </blockquoute>

## Tag font

<font color=”red” face=”arial”> </font>

precisa de atributos

color muda a cor

face muda a fonte ex arial

se separar por virgula e informar mais de uma fonte ele tenta como segunda opção caso não esteja disponivel a primeira na maquina do usuário

## Estruturando com Div e Span

Forma de pensar e estruturar em caixas 

Div é do tipo display block (ocupa o espaço horizontal inteiro por padrão)

tag span não é formato display block então da pra usar no meio do texto sem quebrar a linha

### Fieldset

segmenta em campos determinados por uma margem 

atributo legend

coloca uma legenda ou titulo nos campos

### Embeds

tag <embed src=”arquivo-de-video-exemolo”>

embedar um conteúdo, pegar um conteúdo externo e plugar no seu site pode ser um video, um flash, uma imagem.

era muito usado nos anos 90 (click jogos por exemlpo usando flash) hj em dia ainda é usado mas pode ser descontinuado pois existem tags melhores 

### iframes

Tag <iframe>

abre uma janela na página com conteúdo de outra página 

da pra botar paginas inteiras, google maps ou videos do youtube dentro do frame da sua página

ele conta a visita no site dentro frame 

pode ter problemas de segurança 

Resenha sobre cores 

navegadores modernos aceitam aproximadamente 140 nomes de cores

outras formas de escolher cores

RGB (red green blue)

HSL Hue (matiz) Saturation Lighten (iluminação) matiz tem valores onde 0 é vermelho 120 verde e 240 azul

RGBA mesmo que rgb mais o Alpha que é transparencia 

HSLA mesmo que HSL mas Alpha que é transparencia 

HEX vermelho verde e azul tambem mas descrito em hexadecimal 

no HEX é representado #RRGGBB onde tem dois valores hexadecimais para cada cor do rgb