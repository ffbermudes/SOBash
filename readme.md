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