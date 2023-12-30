# Fundamentos CSS

Criado em: 27 de dezembro de 2023 03:22

Cascading Style Sheets (CSS) 

adiciona estilos a documentos HTML

m

### O que pode ser criado com CSS

layouts e estilização web

animações e desenhos 

filtros 

contadores 

## Formas de declaração de CSS

### Propriedades e valores

**propriedade:** altura, largura, cor de fundo, espaçamento ,etc

**valor**: define o valor da propriedade que e como o navegador deve exibir o estilo do elemento

forma de declarar:  `propriedade: valor;`   exemplo `background: red;`

obs: ponto e q obrigatório no final sempre

## Como adicionar o CSS no html

### **CSS Inline:** usa o atributo style dentro das tags de html. elemento por elemento

desvantagem é que é muito ruim de dar manutenção e de aplicar pq é feito linha a linha 

possível vantagem é que a tag style tem prioridade sobre outros estilos aplicados então da pra reescrever aquele local mesmo sem acesso ao documento css

muito util pra testar novas ideias

### CSS interno: código CSS adicionado dentro da tag head na pagina HTLM. cria um style na head e joga todo o css ali

usa seletores para dizer em quais tags vão ser aplicados os estilos 

### CSS externo: criando um arquivo .css com todas as regras CSS e esse arquivo é referenciado dentro do HTML usando a tag <link>

vantagens css externo: carregamento mais rápido da pagina html, código mais organizado e pode usar o mesmo aquivo css em varias paginas. 

tag <link> link o seu arquivo html com arquivos externos 

atributo rel=”” indica a relação que esse outro arquivo tem com o  seu html no caso do css a relação é “stylesheet”

href=”exemplo link” onde vc coloca o caminho do arquivo que vai fazer o link

### Depurando o CSS

debug: identificar problemas no código fonte 

Dev Tools do chrome 

para abrir dev tools 

direito mouse e inspecionar 

CNTRL + SHIFT + i

CTRL + SHIFT + C

f12

# Seletores

Se**letor por tags ou tipos:** busca elementos por tag html especifica 

só colocar o nome da tag ex: div { }

**seletor por ID (#):** busca elementos através do atributo ID 

usa a # pra indicar a id no css. ex: #id-escolhido{ } 

o id só pode ser usado 1 em cada elentento, tem que ser unico

 

**seletor de Classes (.):**  busca o elemento através do atributo class.

a classe diferente do id pode ser usado em mais de um elemento e identifica aquele grupo todo. cria uma classe né dah

usa . (ponto) para indicar a classe no css ex:  .class-name{ }

o mesmo elemento pode ter mais de uma classe. basta dar um espaço e adicionar mais uma no atributo class

**seletor universal (*):** seleciona tudo na página htlm. aplica para todos os elementos independente da tag

bom pra padronizar as paradas 

e pra fazer reset css ?

usa simplesmente um asterisco *{ }

**seletor de atributo [ ]:** seleciona todos os elementos que possuem o atributo e aplica o estilo a eles 

sempre que falamos de atributo em css fica entre colchetes 

ex: [atributo]

se passar o valor do atributo também ele vai selecionar elementos com aquele exato atributo e valor especifico somente 

ex: `[atributo=valor] { }`

da pra procurar por um atributo que tenha uma palavra no valor também usando:

ex: `[atributo~=valor]{ }` assim ele pega qualquer atributo que tenha aquela palavra no valor mesmo se tiver outras palavra junto 

ex: `[atributo~=streaming]` pegaria tanto as tags com o 

streaming netflix e streaming prime

ex: `[atributo^=sulfixo-valor] {}` vai procurar os atributos que tenham como sulfixo o valor indicado 

ex: `[atributo$=prefixo-valor] {}` vai procurar os atributos que tenham como prefixo o valor indicado 

ex: `[atributo*=valor] {}` vai procurar os atributos que tenham o valor indicado em qualquer posição 

### Agrupamento de seletores

pode declarar vários seletores juntos separando eles por virgula dai o bloco de código vale para todos.

ex: `h1, p, div, .texto, #botão {` 

   `color: red;  }`

# Combinadores

qual o tipo de relação entre os seletores

estrutura para usar o combinador

`[seletor] [combinador] [seletor]`

### Combinador descendente (espaço)

ex no style: 

`li li {color: red;}`  ele vai buscar o li dentro do li e vai aplicar nele o estilo 

no HTML:

<li>

<li>

</li>

</li>

Pode ser também entre diferentes tipos de seletores sem problemas

ex:

`#lista-01 li {}` vai procurar dentro da tag com id= lista-01 a tag li

### combinador filho (>)

vai selecionar todos os elementos filhos diretos do seletor à esquerda

ex style: 

`div > p {color: red; }`  vai buscar as tags p filhas da tag div mas vai ignorar as tags netas por exemplo o p dentro do spam

html ex:

<div>

<p>  </p>

<p>  </p>

<spam>   

<p>  </p>

</spam>  

 </div>

### combinador irmão adjacente (+)

aplica o estilo na tag p irmã que venha logo depois da indicada

*tag irmã é que tem o mesmo nível de indentação*  

ex style: 

`div + p {color: red; }`  vai aplicar no p que vem logo depois da div e apenas nele

html ex:

<p>  </p>

<div>

<spam>   

<p>  </p>

</spam>  

 </div>

<p>  </p> 

<p>  </p>

### combinador irmão geral (~)

aplica o estilo em todas as tags irmãs da selecionada 

ex style: 

`div ~ p {color: red; }`  vai aplicar em todos os p irmãos da div

html ex:

<p>  </p>

<div>

<spam>   

<p>  </p>

</spam>  

 </div>

<p>  </p> 

<p>  </p>

# Propriedades de dimensionamento e espaçamento

### Largura e altura

width = largura 

height = altura 

ex:

`div {`

`width: 200px;`

`height: 200px;`

`}`

vai aplicar uma largura e altura de 200px na div 

palavras importantes para declarar propriedaes 

auto = faz com que o valor seja preenchido automaticamente

initial = vai pegar o valor padrão da propriedade 

inherit = herda a o valor da propriedade do elemento pai

### Altura e Largura máxima e mínima

`max-width:`  `min-width:`   define a largura maxima e minima 

`max-height`  `min-height`   define a altura maxima e minima 

# Margin

margem cria um espaçamento em volta dos elementos 

é criado por fora das bordas do elemento

pode ser definido de forma individual para cada lado do elemento 

ex: `: 100px;`  cria um espaçamento de 100px em cima do elemento

então para definir um valor individual temos 

`margin-top`   cima

`margin-botton`  baixo 

`margin-left`   esquerda 

`margin-right`   direita 

Porém o mais utilizado é a propriedade margin pura que varia o comportamento de acordo com numero de valores passados 

`margin: 10px`                                 **Um valor:** aplica nos 4 lados 

`margin: 10px 15px`                         **Dois valores:** em cima , em baixo    

`margin: 10px 15px 20px`                **Três valores:** em cima, ambos os lados, embaixo    

`margin: 10px 15px 20px 8 px;`      **Quatro valores:** cima, direita, baixo, esquerda    

                                                         (com *4 segue o sentido horário começando de cima)* 

também temos as opções

 `inherit` que herda do pai

`margin: auto;`  calcula as distancias disponíveis e automaticamente  centraliza o elemento na tela de forma horizontal 

Da pra usar margem negativa também declara um -30px por exemplo

### Padding

enquanto a margem cria a distancia da borda para fora do elemento o padding cria a distancia interna

![Untitled](Fundamentos%20CSS%2027af5203ec274a67a1d86be025a633c2/Untitled.png)

segue as mesmas regras de declaração do margin

### Box sizing

width acaba sendo somado junto com a borda e o padding então pode acabar com o tamanho maior que o declarado 

mexemos na propriedade box-sizing 

width = largura + borda + padding

`box-sizing: content-box;` é o padrão onde ele soma tudo no que foi declarado e deixa passar pra ajustar

`box-sizing: border-box;`  redimenciona automaticamente não permitindo que passe do declarado e ajusta diminuindo pra caber