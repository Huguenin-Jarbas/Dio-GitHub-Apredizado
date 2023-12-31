# Versionamento Git e GitHub

Criado em: 31 de outubro de 2023 01:50

### O que é versionamento de código?

O versionamento de código é um sistema que controla as versões de um arquivo ao longo do tempo. Ele registra o histórico de atualizações, gerenciando as alterações feitas, a data, o autor, entre outros dados. O versionamento de código é utilizado para organizar, controlar e garantir a segurança dos arquivos de um projeto. Ele permite que diferentes pessoas trabalhem em um mesmo projeto sem conflitos, além de facilitar o acompanhamento das alterações e a reversão para versões anteriores quando necessário.

### VCS centralizados (CVCS)

**Vantagens do VCS Centralizado:**

- Fácil de usar e entender, especialmente para iniciantes.
- Acesso centralizado a todos os arquivos e históricos.
- Controle estrito sobre as permissões de acesso.
- Facilidade na colaboração em equipe, pois todos trabalham no mesmo repositório central.
- Maior segurança e consistência dos dados.
- Melhor controle sobre conflitos de mesclagem.

**Desvantagens do VCS Centralizado:**

- Dependência de um servidor centralizado, o que pode resultar em problemas se o servidor estiver inacessível.
- Limitações na capacidade de trabalho offline.
- Dificuldade em lidar com projetos de grande escala.
- Dificuldade em lidar com conflitos de mesclagem complexos.
- Menor flexibilidade e liberdade para cada membro da equipe trabalhar em diferentes ramos simultaneamente.

### VCS Distribuídos (DVCS)

**Vantagens do VCS Distribuído:**

- Maior flexibilidade e liberdade para cada membro da equipe trabalhar em diferentes ramos simultaneamente.
- Trabalho offline facilitado, pois cada cópia local do repositório contém todo o histórico.
- Melhor desempenho em operações locais, já que não há necessidade de comunicação com um servidor central.
- Maior escalabilidade para projetos de grande escala.
- Possibilidade de criar repositórios remotos em diferentes servidores, garantindo redundância e segurança.

**Desvantagens do VCS Distribuído:**

- Curva de aprendizado mais íngreme, especialmente para iniciantes.
- Complexidade adicional devido à necessidade de sincronização entre repositórios distribuídos.
- Possibilidade de conflitos de mesclagem mais frequentes e complexos.
- Menor controle centralizado sobre permissões de acesso, exigindo a implementação de medidas adicionais de segurança.
- Necessidade de gerenciar e garantir a integridade de múltiplas cópias do repositório.

## Git e GitHub

Git é um sistema de controle de versão distribuído usado para rastrear as alterações em arquivos de código-fonte durante o desenvolvimento de software. Ele permite que várias pessoas trabalhem juntas em um projeto, mantendo um histórico completo das alterações feitas. 

O GitHub é uma plataforma de hospedagem de código-fonte baseada em nuvem que utiliza o Git. Ele fornece recursos adicionais, como controle de acesso e rastreamento de problemas, facilitando a colaboração em equipe e o gerenciamento de projetos de software.

Aqui estão alguns dos principais comandos do Git e suas funções:

- `git init`: Inicializa um repositório Git em um diretório.
- `git clone`: Clona um repositório Git existente para a máquina local.
- `git add`: Adiciona arquivos ao índice do Git para serem commitados.
- `git commit`: Grava as alterações feitas nos arquivos adicionados ao repositório.
- `git push`: Envia as alterações commitadas para um repositório remoto.
- `git pull`: Atualiza o repositório local com as alterações mais recentes do repositório remoto.
- `git branch`: Lista, cria ou exclui branches (ramificações) no repositório.
- `git checkout`: Muda para um branch especificado ou restaura arquivos a partir de um commit específico.
- `git merge`: Combina as alterações de um branch com outro.
- `git status`: Mostra o estado atual do repositório, incluindo arquivos modificados, adicionados ou excluídos.
- `git log`: Mostra o histórico de commits do repositório, incluindo informações como autor, data e mensagem do commit.

Esses são apenas alguns dos comandos mais utilizados no Git. Existem muitos outros comandos e opções disponíveis para auxiliar no controle de versão do seu projeto.

## criando e clonando  repositórios

existem duas formas de obter um repositório git na sua maquina 

### 1. Transformando um diretório local não controlado por versão em um repositório Git

Na pasta local, utilize o comando `git init` no terminal para transformá-la em um repositório.

Para conectar a um repositório remoto, utilize o comando `git remote add origin URL`

(substitua "URL" pela URL do repositório no GitHub)

### 2. Clonando um repositório existente

Utilize o comando `git clone URL` no terminal para clonar um repositório remoto para a sua máquina.

Se você adicionar um nome no final do comando, a pasta do repositório será renomeada com o novo nome que você especificar.

Exemplo: `git clone URL novo-nome`

(substitua "URL" pela URL do repositório no GitHub)

### Salvando alterações no repositório remoto

git status mostra o status da arvore de trabalho e o estado dos arquivos 

untracked files são arquivos não rastreados (não presentes em commits anteriores do git) 

diretórios vazios são ignorados pelo git.  para ser reconhecido tem que ter pelo menos um arquivo 

comando touch no git bash cria arquivo 

comando `.gitignore` cria um arquivo dentro da pasta que faz com que o git ignore a pasta ou arquivo para que não apareça no commit 

criar um arquivo .gitkeep dentro de uma pasta vazia geralmente é pra que o commit inclua a pasta vazia 

`git add “nome do arquivo”` prepara para commit 

se vc quiser adicionar tds os arquivos de uma vez use git add .  

[README.md](http://README.md) 

um sobre o seu projeto que vai junto do git 

md significa mark down é tipo html só que mais simples 

[readme.so](http://readme.so) site brabo pra facilitar criar readme 

## Desfazendo alterações git

remover versionamento de uma pasta caso tenha dado git init errado ou etc

basta excluir o diretório .git 

use os comandos: `rm -rf .git` 

`git restore “nome do arquivo”`   restaura pro ultimo commit 

pode te salvar caso tenha apagado tudo errado sem querer 

mas cuidado pq se tiver alterções que queira mantes elas vão ser perdidas já que vai restaurar pra antes delas

## Alterar a mensagem dos commits

`git log` mostra o histórico de commits 

`git commit --amend -m”nova mensagem”` altera a msg do commit anterior 

`git commit --amend` abre o editor de codigo (vs code) para faça alterações lá 

### Desfazer commits

Usamos o comando git reset que tem 3 opções soft, mixed e hard.  

você tem que copiar o numero de identificação do commit que vc quer retornar 

`git reset --soft 12345`

pega os arquivos posteriores ao commit selecionado e manda pra area de preparação (aquela mesma do git add)

`git reset --mixed 12345`

padrão do comando pega os arquivos posteriores e adiciona na arvore de terabalho como untracked files 

`git reset --hard 123245` 

restauro pro commit indicado e ignora completamente os arquivos dos commits que vem depois, apaga eles   

*substituir o 12345 pelo id do commit 

da pra remover arquivos da area de preparação usando o git reset e o nome do arquivo

## Enviado para o repositório remoto

crie um novo repositório no GitHub e siga as instruções que tem lá 

que vão ser mais ou menos:

`git remote add origin link-do-repo-remoto-aq
git branch -M main`  (esse muda o nome da branch pra main caso seja outra, no seu caso já é então esse comando n precisa )
`git push -u origin main`

depois disso já vai ter feito seu commit para o repo remoto no github

### editores online

lá vc pode editar os arquivos dentro do prórpio github e commitar as mudanças ou  na pagina do repositório clicar em ponto no teclado ele abre um vscode virtual pra editar as paradas

### Comando `git pull`

puxa as alterações do repósitorio remoto para o repósitorio local 

as mudanças feitas no remoto agora aparecem da sua maquina 

## Trabalhando com Branches

branch é uma ramificação do projeto 

é um ponteiro móvel para um commit no histórico do repositório tipo uma linha do tempo paralela

Se vc cria uma nova branch dentro de uma já existente ela passa a apontar para o mesmo commit da anterior 

`git checkout -b nome-nova-branch-aq`  cria uma nova branch apontando para o commit atual 

`git checkout nome-da-branch` troca de branch

`git branch` lista todas as branches 

`git branch -v` lista os ultimos commits de cada branch

`git branch -d nome-da-branch` deleta a branch selecionada 

`git merge nome-da-branch` mescla a branch selecionada a branch atual. junta as informações

### Conflitos de merge

Se duas alterações na mesma linha de codigo são feitas em branches diferentes vai gerar um conflito na hora do merge o git vai te dar a opção de escolher qual alteração vc quer manter

o comando `git pull` é a junção de `git fetch` + `git merge` 

o fetch baixa as alterações 

o merge mescla elas

 `git diff nome das branches`  ele mostra a diferença entre  as branches

Para clonar apenas uma branch quando for usar o git clone faça: `git clone link-do-repo-remoto --branch nome-branch --single branch` 

caso não especifique ele pega o repo todo 

`git stash` arquiva modificações (n entendi real)

## Materiais de apoio

- [GIT. Documentation](https://git-scm.com/doc)
- [GITHUB. Documentation](https://docs.github.com/)

[https://github.com/elidianaandrade/dio-curso-git-github](https://github.com/elidianaandrade/dio-curso-git-github) sobre o curso todos as info

[Versionamento de Código com Git e GitHub.pdf](Versionamento%20Git%20e%20GitHub%2022a77d2d358144fb89be5f7102056e81/Versionamento_de_Cdigo_com_Git_e_GitHub.pdf)

/