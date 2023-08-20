<h1>Infraestrutura como Código: Script para Criação de Usuários, Diretórios e Permissões. </h1>
<p> Sejam bem-vindos ao projeto de LAB <strong>Infraestrutura como Código</strong> oferecido pela plataforma de cursos online <a href="https://dio.me/"><strong> Digital Innovation One</strong></a>.<br>

<h2>🎯 Objetivo do Projeto</h2>
<p>Criar um script que automatiza a criação de diretórios, grupos de usuários, criação de usuários e configuração de permissões em um ambiente Linux que está sendo usado como teste. Note que o uso de senhas criptografadas diretamente no script não é recomendado em um ambiente de produção. Em um ambiente real, você deve usar métodos mais seguros para gerenciar senhas de usuário.</p>

<h2>
🛑 Pré-requistos
</h2>

- [x] Básico de Linux

- [x] Máquinas Virtuais

<h2> 🚦 Guia </h2>

<ol>
    <li> Apresentação do Projeto Base </li>
    <li> Download e Instalação do Ubuntu no VirtualBox</li>
    <li> Configurações da máquina virtual</em></li>
    <li> Acesso remoto via Putty</li>
    <li> Criação de Scripts </li>
</ol>

<h2>🛠 Tecnologias Utilizadas</h2>

<ul>
    <li>Ubuntu Server 22.04.3</li>
    <li>VirtualBox</li>
    <li>Putty</li>
</ul>


<h2><a href="[https://strn.com.br/artigos/2018/12/11/todas-as-anota%C3%A7%C3%B5es-do-jpa-anota%C3%A7%C3%B5es-de-mapeamento/](https://www.redhat.com/pt-br/topics/virtualization/what-is-virtualization)">
Comandos Utilizados</a></h2>

<h3>Este é um script em shell (Bash) que realiza várias operações relacionadas à criação de diretórios, grupos de usuários, criação de usuários e atribuição de permissões em um sistema Linux.</h3>

<strong>`mkdir /publico`</strong>
Este comando cria um diretório chamado "publico" na raiz do sistema de arquivos.

<strong>`mkdir /adm`</strong>
Este comando cria um diretório chamado "adm" na raiz do sistema de arquivos.

<strong>`mkdir /ven`</strong>
Este comando cria um diretório chamado "ven" na raiz do sistema de arquivos.

<strong>`mkdir /sec`</strong>
Este comando cria um diretório chamado "sec" na raiz do sistema de arquivos.

<strong>`groupadd GRP_ADM`</strong>
Cria um grupo de usuários chamado "GRP_ADM".

<strong>`groupadd GRP_VEN`</strong>
Cria um grupo de usuários chamado "GRP_VEN".

<strong>`groupadd GRP_SEC`</strong>
Cria um grupo de usuários chamado "GRP_SEC".

<h3>Os próximos comandos useradd criam usuários com as seguintes configurações:</h3>

<strong>`useradd username -m -s /bin/bash -p $(openssl passwd -crypt Senha123) -G GRP_ADM`</strong>
Cria o usuário "vitor" com um diretório home (-m), o shell padrão "/bin/bash" (-s), uma senha criptografada com o algoritmo DES usando o OpenSSL e adiciona o usuário ao grupo "GRP_ADM".

<h3>Os comandos chown são usados para alterar o proprietário e o grupo dos diretórios criados anteriormente:</h3>

<strong>`chown root:GRP_ADM /adm`</strong>
Define o proprietário como "root" e o grupo como "GRP_ADM" para o diretório "/adm".

<strong>`chown root:GRP_VEN /ven`</strong>
 Define o proprietário como "root" e o grupo como "GRP_VEN" para o diretório "/ven".

 <strong>`chown root:GRP_SEC /sec`</strong>
 Define o proprietário como "root" e o grupo como "GRP_SEC" para o diretório "/sec".

 <h3>Os comandos chmod são usados para definir permissões nos diretórios:</h3>

<strong>`chmod 770 /adm`, `chmod 770 /ven` e `chmod 770 /sec`</strong>
Define permissões de leitura, escrita e execução (rwx) para o proprietário (root), sem permissões para o grupo e sem permissões para outros usuários.

<strong>`chmod 777 /publico`</strong>
Define permissões de leitura, escrita e execução (rwx) para todos os usuários (proprietário, grupo e outros) no diretório "/publico".


<h2>🔗 Links Úteis</h2>
<ul>
    <li><a href="https://www.redhat.com/pt-br/topics/linux/what-is-linux">O que é Linux?</a></li>
    <li><a href="https://www.redhat.com/pt-br/topics/virtualization/what-is-virtualization">O que é Virtualização?</a></li>
    <li><a href="https://aws.amazon.com/pt/what-is-cloud-computing/">Computação em Nuvem</a></li>
</ul>

------------


### Instruções para criação do repositório via linha de comando do Git:

Passo 1: `git init`

Passo 2: `git add .`

Passo 3: `git commit -m "Início da Atividade"`

Passo 4: `curl -H "Authorization: token TOKEN_AQUI" https://api.github.com/user/repos -d '{"name":"REST-Spring"}'`

Passo 5: `git branch -M main`

Passo 6: `git remote add origin https://github.com/vitorramon/REST-Spring.git`

Passo 7: `git push -u origin main`

### Instruções para puxar as atualizações do repositório remoto para o repositório local via linha de comando do Git:

Passo 1: `git fetch`

Passo 2: `git merge`

ou

Passo 3: `git pull` = `git fetch` + `git merge`  

>[!NOTE]
>
>Verifique se está na branch correta, caso contrário utilize o comando: `git checkout NOME_DA_BRANCH``.
