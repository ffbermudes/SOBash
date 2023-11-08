# Sistemas operacionais AOP 2

## Capítulo 3: Organização do Linux

### Exercício de fixação 1 (p.40)

Desenhe a árvore do sistema de arquivos até o terceiro nível hierárquico. No terceiro nível,
basta listar no máximo três diretórios, se houver. Considerar o ponto de partida, o diretório
raiz, como o primeiro nível hierárquico.

| bin  | boot | dev   | etc    | home        | lib      |
|------|------|-------|--------|------------|----------|
| ls   | -    | ram1  | init.d | @meuusuario | apache2  |
| cp   | -    | ram2  | iscsi  | -          | apt      |
| zcat | -    | ram3  | kernel | -          | initcpio |


| mnt | opt      | proc        | root   | sbin | tmp               | usr      | var      |
|-----|---------|-------------|--------|------|-------------------|---------|---------|
| c   | -       | fs          | .local | mkfs | 0783d5391a045b54825c5be00 | bin     | backups |
| d   | -       | driver      | .ssh   | fsck | 0f8374064413b38c6c89fd200 | lib     | cache   |
| wsl | -       | bus         | .bashhistory | swapon | 2a56d29d2ea741c0c4eda9400 | include | opt     |

### Atividade 3.2 - Criando arquivos (p.61).
1. Posicione-se em seu diretório de trabalho e crie os arquivos “exemplo1” e “exemplo2” uti-
lizando comandos diferentes em cada caso. Ao criar um dos arquivos, entre com algumas

---

> resposta:

~~~bash
mkdir diretorioDeTrabalho
cd diretorioDeTrabalho
echo 'teste1' > exemplo1
touch exemplo2
~~~

Resultado dos códigos acima. Observa-se com o cat o exemplo1 com o conteúdo escrito __teste1__ e o exemplo2 está vazio.

![print do resultado do código](assets/3.2%20p.61%20N1.jpg)

2. Faça com que o arquivo vazio fique igual ao arquivo com conteúdo.

---

>resposta:

~~~bash
cat exemplo1 >> exemplo2
~~~

![print do resultado do código](assets/3.2%20p.61%20N2.jpg)

Dessa forma o arquivo exemplo2 agora possui os mesmos dados de exemplo1

### Atividade 3.3 - Criando diretórios e copiando arquivos.

3. Crie o diretório 'exemplos' em um subdiretório 'temp' no seu diretório 'home'. Utilize apenas um comando de criação para executar esta ação.

> resposta:

~~~bash
mkdir -p /home/temp/exemplos
~~~

![print do resultado do código](assets/3.3%20p.61%20N3.jpg)

4. Mova os arquivos “exemplo1” e “exemplo 2” para o diretório “exemplos”, deixando uma
cópia do segundo no diretório de origem.

> resposta:

~~~bash
sudo cp exemplo1 exemplo2 /home/temp/exemplos
~~~

![print do resultado do código](assets/3.3%20p.61%20N4.jpg)

### Atividade 3.4 - Empacotando e compactando arquivos

5. Entre no diretório temp/exemplos. Empacote e compacte os arquivos criados anteriormente num arquivo chamado “exemplos.tar.gz”. Use um único comando para efetuar esta operação.

>resposta:
~~~bash
cd /home/temp/
sudo tar -cvf exemplos.tar exemplos/
sudo gzip exemplos.tar
~~~

### Atividade 3.5 - Removendo arquivos e diretórios

1. Após o término das atividades, volte à situação original e remova todos os elementos criados

> resposta:

~~~bash
cd home/
rm -rf /temp
rm -rf /home/ambientedev/uvv/sistemasOperacionais/diretorioDeTrabalho/
~~~

todas as pastas removidas como solicitado segue as imagens da remoção

![print do resultado do código](assets/3.5%20N1.jpg)

![print do resultado do código](assets/3.5%20N1%20img2.jpg)

## Capítulo 4

### Exercício de fixação 1 - comando sort

1. Qual a utilidade do comando sort?
> resposta:

Ordenar o conteúdo de um arquivo de acordo com a necessidade. A ordenação pode ser numérica crescente ou decrescente ou alfabética.

2. Através da página de manual do comando, encontre a opção que organiza o arquivo com
base nas colunas.

> resposta:
Utilizando o sort também podemos ordenar em colunas basta utilizarmos o parâmetro __-k__ seguido da quantidade de colunas um número inteiro segue abaixo o exemplo:

~~~bash
sort -k 2 arquivo.txt
~~~

3. Pesquise três opções do comando sort.

	* `sort -b ` ignora espaços em branco no inicio e no final das linhas.
	
	![sort -b imagem](assets/4%20p.68%20N3.jpg)

	* `sort -f ` ignora a diferença entre letras maiusculas e minusculas

	![sort -b imagem](assets/4%20p.68%20N3%20img2.jpg)

	* `sort -i` espaços em branco quebra de linhas tabulações e outros são ignorados na hora de imprimir na tela os dados.

	![sort -b imagem](assets/arquivo%20com%20tabulações%20e%20espaços.jpg)

	sem ordenação arquivo
	
	![sort -b imagem](assets/arquivo%20com%20tabulações%20e%20espaços.jpg)

	Ordenado, pode-se ver que foi ignorado as tabulações e espaços.