# Rocketseat - Guia Estelar de Github

Neste curso iremos aprender a usar o Github que é um site onde podemos salvar nossos projetos em modo privado para somente a equipe visualizar ou publico para outros devs usarem ou como um portfolio nosso e quem vai nos ensinar será o _**Mayk Brito**_ da Rocketseat

>Seu código precisa ficar seguro e disponível, por isso, aprender o Github irá te dar opção para salvar seu código na nuvem e deixá-lo disponível para outros devs.

# Modulo 01 - Introdução

## Aula 01 - Para quem é o curso
O Git é o gerenciador do nosso projeto onde vamos usar ele para criar o historio do nosso projeto
O Github serve como repositório online e existe diversos site com esta mesma funcionalidade

## Aula 02 - Requisitos para o curso e revisão de Git
Antes de aprender sobre o Github devemos saber como o Git funciona

Iremos agora revisar os comandos que mais iremos utilizar
  * Cria o repositório: `git init`
  * Seleciona todos os arquivos: `git add .`
  * Cria um commit dos arquivos selecionados: `git commit -m "Descrição aqui"`
  * Para verificar a pendencia dos arquivos: `git status`
  * Para ver todos os commits: `git log`
  * Cria conexão com o repositório online: `git remote add nome link`
  * Exclui conexão com o repositório online: `git remote remove nome link`
  * Lista as conexão existente: `git remote`
  * Enviar os arquivos para o repositório online: `git push`
  * Receber os arquivos do repositório online: `git pull`

`Vim` é o editor de texto padrão do Git e para fechar devemos aperta `:wq`

# Modulo 02 - Primeiros passos

## Aula 03 - Criando uma conta
Primeiro de tudo temos que criar uma conta informando o nome, email e uma senha
Existe desde a versão gratuita e paga

## Aula 04 - Configurando perfil público
No perfil público podemos adicionar uma foto, email, descrição, local que mora, se está a busca de emprego ou até relacionar a empresa que trabalha

## Aula 05 - Conhecendo a página do usuário
Vimos que na página temos os atalhos para ir na página inicial, pull request que é o envio dos arquivo para a linha principal depois de uma confirmação, issues que serve para solicitar a correção de um bug, marketplace e explores, mais tudo isso iremos ver futuramente

# Modulo 03 - Criando repositórios

## Aula 06 - Criando repositório online
Temos que ir na página inicial e clicar em `new`

O primeiro repositório será um readme para o nosso perfil onde para isso temos que
  1. Colocar nosso login como nome do repositório
  2. Deixar ele como público
  3. Selecionar a opção `add a readme file`
  4. E por último clicar em `create repository`

## Aula 07 - Conhecendo a página do repositório
Agora aprendemos sobre oque existe dentro de uma página de repositório

Onde temos uma guia principal como as opções de code, issues, pull requests, actions, projects, wiki, security, insights e settings, tudo isso é baseado no repositório aberto

Nela também conseguimos ver uma observação e seus commits criado e seus detalhes

## Aula 08 - Atualizando o repositório
Vimos que para acessar um repositório já criado temos que ir na página inicial e depois buscar ele no lado esquerdo da tela, para atualizar um arquivo no Github basta clicarmos em editar e para salvar temos que ir no final da pagina onde teremos que adicionar um título falando oque fizemos e aqui da para adicionar uma descrição do que foi feito

## Aula 09 - Copiando ideia de readme do pessoal
O readme também aceita HTML e para criar o nosso podemos nos basear em alguns existente

## Aula 10 - Colaborando em outros repositórios
Podemos editar a qualquer momento repositórios públicos de outros usuários

Onde quando clicamos em editar criamos um `fork` onde ele será uma copia do repositório original que ficaram salvo na nossa conta, depois que eu realizar todas as alterações e salva um `pull resquest` será criado avisando o dono do repositório original que alguém sugeriu algum tipo de mudança

## Aula 11 - Conhecendo o restante da página pessoal
Conseguimos personalizar quais repositório deve aparecer como destaque, também temos uma tabela que mostra quantos commits foram realizados por dia de repositórios aberto

# Modulo 04 - Trabalhando com repositórios

## Aula 12 - Criando chave SSH
Esta chave é um tipo de conexão onde com ela o Github sabe que a maquina que está tentando se conectar a ele é um equipamento autorizado

Para criar a chave precisamos digitar este comando no `Bash do Git`, ele vai realizar algumas perguntas mais basta darmos um enter e não preencher nada
```bash
ssh-keygen -t rsa -b 4096 -C "emailDaContaDoGithub@email.com.br"
```

Para acessar a chave devemos utilizar este comando
```bash
cat ~/.ssh/id_rsa.pub
```

Ai depois na nossa conta devemos acessar settings, SSH and GPG keys, New SSH key, agora informamos um titulo como o nome do equipamento e embaixo a chave

## Aula 13 - Adicionando chaves ao gerenciador local SSH Agent
Agora temos que vincular nosso equipamento com o SSH criado, para isso temos este [site](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) que mostra os comandos necessário para cada tipo de sistema operacional
```bash
eval `ssh-agent -s`
ssh-add ~/.ssh/id_rsa
```

## Aula 14 - Linkando um repositório remoto com local
Para criar o link basta utilizamos o endereço SSH do nosso repositório
```bash
git remote add origin git@github.com:login/NomeRepositório.git
```

## Aula 15 - Modificando arquivos local e enviando para repositório remoto
Na aula foi realizado algumas alterações no arquivo enviado para mostrar que alguns comandos são executados somente uma vez como adicionar um link remoto e que o `git push` vai enviar as alterações para o link preferencial

## Aula 16 - Modificando arquivos remotos e puxando para repositório local
Para fazer o download de um arquivo devemos usar outro comando pois o `push` envia alterações
```bash
git pull
```

## Aula 17 - Entendendo o histórico remoto
No site temos um opção de histório onde ele mostra todos os commits e seu id, ele é completo e muito mais fácil de usar do que usar um `git log` no terminal

## Aula 18 - Corrigindo conflitos de merge
Um conflito de merge é quando o arquivo local está diferente do online, assim teremos que analisar qual alteração vamos querer manter, depois de decidir deveremos criar um novo commit e executar o comando anterior que identificou o merge
