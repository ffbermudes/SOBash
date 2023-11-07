# Sistemas operacionais

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

### Atividade 3.2 (p.61)
1. Posicione-se em seu diretório de trabalho e crie os arquivos “exemplo1” e “exemplo2” uti-
lizando comandos diferentes em cada caso. Ao criar um dos arquivos, entre com algumas

linhas de dados pelo teclado.

2. Faça com que o arquivo vazio fique igual ao arquivo com conteúdo.



	1. 

~~~bash
	mkdir diretorioDeTrabalho
	cd diretorioDeTrabalho
	echo 'teste1' > exemplo1
	touch exemplo2
~~~

![print do resultado do código](assets/3.2%20p.61%20N1.jpg)
