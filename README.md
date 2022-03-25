# Pequeno "manual" de utilização comandos <i>git</i> utilizando o git-bash

## Software necessário
<i>Terminal <u>git bash</u> - onde irão ser executados os comandos</i>
Website oficial:
> https://git-scm.com/

## Comandos importantes
### Configurar os dados do utilizador que vão ficar registados no github associados ao commit
<i>Este passo é importante realizar, pois o github associa os commits a um user, daí ser necessário registar um username/nome e o email da conta no github.</i>
#### Username
> git config --global user.name "dgraca"
#### Email
> git config --global user.email github@danielgraca.com

#### Verificar se as configurações préviamente introduzidas estão corretas
> git config --list

 ### Clonar um repositório localmente no <i>nosso</i> computador
 <i>Note-se que com <b>nosso</b> não quero parecer comunista. Apenas utilizo uma linguagem que faça um macaco entender o processo.</i>
> git clone https://github.com/dgraca/comandos_git

<i>Note-se que <b>https://github.com/dgraca/comandos_git</b> utiliza-se como exemplo de um repositório existente. Deve-se trocar com o repositório que se quer clonar</i>

### Adicionar ficheiros para fazer commit
<i>Este passo é importante, porque para enviar documentos adicionados/editados/removidos, é preciso "dizer" ao git que existem alterações que devem ser enviadas</i>
> git add .

<i>O ponto <b>.</b> faz adicionar toda a diretoria selecionada e todos os seus ficheiros e diretorias, recursivamente</i>
<i>Caso seja preciso adicionar um ficheiro em particular, consultar https://git-scm.com/docs/git-add</i>


### Criar o commit
<i>Após se ter dito ao git os ficheiros alterados que queremos enviar para o repositório, criamos um commit</i>
> git commit -m "descricao do commit"

### Enviar o commit
<i>Não queremos dizer ao git que temos algo pra enviar e depois nunca mais enviamos, certo? Imagem-se dizer aos vossos namorad@s que lhes vão dar uma prenda de aniversário e depois deixam-n@s pendurad@s. <b>Not cool.</b></i>

> git remote -v

<i><b>git remote</b> - de forma simplística - cria uma conexão com o repositório</i>

> git push -u origin master

<i>Acima o <b>master</b> representa a branch para qual queremos dar commit. O commit adotou <b>main</b> como nome default da branch principal, devido aquelas <b>pirolisses</b> de que <b>master</b> remete para slave labor e coisas do género. Eit.</i>


### sincronizar repositório git com repositório local
<i>Imagine-se que <b>macaco A</b> está a trabalhar com <b>macaco B</b>. Se o <b>macaco A</b> enviar dados para o repositório e o  <b>macaco B</b> não as puxar, o que é que acontece quando o <b>macaco B</b> enviar as suas coisas para o servidor? Yup. <b>Dá barracada</b>. Por isso, executa a porcaria do comando e sincroniza as tuas branches. Não custa nada.</i>
> git pull

## Comandos honorários
### Verificar o estados da <i>branch</i>
<i>Antes de enviar um commit tenho o hábito de verificar o que raio é que vai ser enviado. Este comando é útil porque permite listar os ficheiros adicionados/editados/removidos na branch selecionada</i>
> git status

### Trocar de <i>branch</i>
<i>Say what!? Podemos ter mais que uma branch? Sim, e é util conseguir trocar de branch quando se trabalha em equipa ou têm-se um projeto dividido por tarefas/fases. E não só, mas de forma simplista, é isto.</i>
> git checkout branch_name

<i><b>NOTA IMPORTANTE:</b> Brincadeiras à parte, é preciso ter cuidado com este comando. Se tivermos ficheiros alterados e não fizermos nada com eles, ao trocar de branch eles vêm connosco agarrados e pode haver confusão. Deve-se sempre dar <b>stash</b> aos ficheiros antes de trocar de branch.</i>

### Dar <i>stash</i> aos ficheiros
<i>É basicamente metê-los no baú enquanto não precisamos deles, mas não os queremos perder. Tipo o que se faz aos diamantes no minecraft. Não preciso deles por agora mas estão lá para quando precisar.</i>
> git stash
 
<i>Okay, os meus diamantes estão no baú. E agora? Quero os meus diamantes de volta e não sei ir buscá-los. O que faço? Bem... a verdade é que pode-se fazer algumas coisas diferentes, mas o mais básico é fazer <b>pop</b> ao último <b>stash</b> feito. Isto significa que vamos pegar no último <b>stash</b> e "cancelá-lo" - ou seja - voltar a ter os ficheiros de volta. Estes comandos têm uma série de flags e opções que podem ser usadas. Se valer a pena, consultem https://www.atlassian.com/git/tutorials/saving-changes/git-stash e vejam por vocês mesmos.</i>
> git stash pop

## Conclusões
<i>Os comandos git conseguem ser simples e complexos, dependendo da forma como são usados. Se precisarem, podem consultar a net. Mas neste documento encontram-se os mais importantes - diria eu - de forma simples para poderem começar a usa-los em contexto académico e familiarizarem-se com eles para no futuro ser bem mais simples e intuitivo. Qualquer coisa também podem perguntar. <br />Cheers,</i>

> https://github.com/dgraca
