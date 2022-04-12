### Curso Git 🔥
# Sistema de controle de versao:
	>Os sistemas de controle de versao sao 
	softwares com a finalidade de fazer o gerenciamento de
	versoes de um documento qualquer.
>Tais como: Controle de Histórico, Rastreabilidade e Trabalho em Equipe.

# Centro de versao centralizado:
	Area de trabalho: commita para o Repositório Central e Re-
	positório Central atualiza para a área de trabalho;
	Blame; Branch; Merge; Revert; Log para Repositório Central;
	GIT NAO É CENTRALIZADO!.

# Centro de versao distribuído:
	>Área de trabalho tem um repositório local e da push ou pull para o repositório remoto ou do repositório.
>Exemplo: No repositório remoto possui-se o arquivo 1. Eu baixei a versao um e minha amiga também. Caso eu atualize para uma versao mais recente e de um push para o repositório remoto, devo informar que é um arquivo 2, pois foi atualizado. Caso minha amiga também de pull no arquivo 1 e faça alteraçoes, ela nao poderá dar um push com o nome arquivo 2, pois apresentará incompatibilidade. Deverá ser arquivo 3 ou assim em diante.

# Para git:
# Plataformas de hospedagem:
	>Armazenam repositórios Git servindo como bacup de todos os arquivos e alteraçoes.
	>Permitem o trabalho colaborativo em projetos open source ou privados.
	>As plataformas mais comuns sao: Github; Bitbucket; Gitlab.
	>Bitbucket: Soluçao em nuvem para armazenar repositórios do Git.

### COMANDOS GIT NO BIT BUCKET:
		>git --system: aplica as configuraçoes para todo repositorio dos usuarios do PC.
		>git --global: aplica para todo repositório do usuário corrente.
		>git --local: aplica para o repositório corrente.
		>As configuraçoes serao aplicadas na ordem: 
			1- Caso tenha local, prevalece local.
			2- Caso tenha global, prevalece global.
			3- Se nao, prevalece a do sistema.

		### $ git config --global user.name "<nome>-global" = Nome global para o usuário
		### $ git config --local user.name "<nome>" = Nome local para o usuário
		### $ git config user.name = Checar usuário
		### % git config --local user.mail "<email>"
		Aliases:
		  >O termo alias é sinonimo de atalho; 
		  >Os aliases sao usados para criar comandos menores que correspondem a comandos maiores;
		  >Eles viabilizam fluxos de trabalho mais eficientes por que exigem menos teclas para a exec do comando;
		  >Definimos um aliasa da seguinte forma: git config --local ou --global ou --system alias.<curto-comando><longo-comando>;
		  >No curso usarei um comando chamado hist que será um log personalizado e utilizarei ao longo do curso.


		  >$git config --global alias.hist 'log --pretty=format:"%h%ad | %s%ad [%an]"" --graph --date=short'
		  >%h == Hash abreviada do commit;
		  >%ad == Data do commit;
		  >%s == Comentários do commit;
		  >%d == Referencias do commit;
		  >%an == Nome do autor;
		  >--graph == Arvore de commits no formato ASCII
		  >--date=short == Mantem o formato de data pequeno.

# Pedindo Ajuda:
	Para acessar o manual de ajuda do Git, usa-se o seguinte comando:
		$git<verb> --help

# Primeiro Commit:
	>Usamos o comando echo, por exemplo:
		>$ echo "hello world" > hello.txt
		>Criamos um txt com a frase hello world!
		>Para realizarmos um commit, a princípio
		usaremos o comando $git add nomedoarquivo
		>E depois $git commit -m "teste"
		>-m == Descriçao do arquivo
		>OBS: Se usarmos $git add .
			adicionaremos todos os arquivos
			para a área de staging.

### Repositório:
	O repositório possui tres áreas, tais como:
	Area de trabalho: área que contém os arquivos e diretórios físicos,
	onde se altera os dados.
	Para realizarmos um commit nos arquivos desejados, devemos adicionar
	os arquivos para a área de staging, com um simples comando
	>$git add nomedosarquivos
	Após isso, basta executar um git commit, para fazer a exportaçao
	para os repositórios.

# Git show:
	Rever as alteraçoes envolvidas no commit.
	$git show == Irá exibir as alteraçoes do último commit. 
	Caso eu tenha feito muitos commits, posso mostrar as alteraçoes
	de um conjunto de commits utiliza-se:
	$git show commitN...commitM
	
