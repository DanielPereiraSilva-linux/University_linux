# **Introdução ao Shell e Comandos Básicos**

## O que é o Shell?

- O Shell é uma interface de linha de comando que permite interagir com
o sistema operacional GNU/Linux.
- No Linux, o **Bash (Bourne Again Shell)** é um dos Shells mais utilizados.

---

## Conceitos Básicos

1. **Terminal**: Interface para interagir com o Shell.
2. **Prompt**: O local onde você digita comandos. Exemplo de prompt padrão:
$(usuario sem privilegios) ou #(root ou usuario com privilegios)

---

## Comandos Básicos

### 1. Comando `pwd` (Print Working Directory)

Exibe o diretório atual em que você está trabalhando.

Exemplo:

```bash
pwd
```

Saída:

```bash
/home/user
```

---

### 2. Comando ls (List Directory)

Lista os arquivos e diretórios no diretório atual.

Opções comuns:

```bash
ls -l: Lista arquivos em formato detalhado.
ls -a: Mostra arquivos ocultos (começam com ".").
```

Exemplo:

```bash
ls -la
```

Saída:

```bash
drwx--x---+ 24 user user 4096 Jan 23 16:27 .
drwxr-xr-x. 3 root root  4096 Jan 17 06:12 ..
drwxr-xr-x  2 user user  4096 Jan 16 10:00 Documents
-rw-r--r--  1 user user    20 Jan 16 09:30 file.txt
```

Com podemos ver o comando apresenta os detalhes do que existe no diretório `-l`,
além de apresentar os arquivos ocultos `-a`.

---

### 3. Comando cd (Change Directory)

Navega entre diretórios.

Sintaxe:

```bash
cd [caminho-do-diretório]
```

Exemplo:

```bash
cd /home/user/Documents
```

Atalhos úteis:

`cd ..  : Volta para o diretório anterior.`

`cd ~   : Vai para o diretório home do usuário.`

`cd -   : Volta para o ultimo diretorio acessado`

---

### 4. Comando touch

Cria arquivos vazios.

Exemplo:

```bash
touch arquivo1.txt arquivo2.txt
```

Resultado:

Dois arquivos serão criados no diretório atual.

---

### 5. Comando mkdir (Make Directory)

Cria diretórios.

Exemplo:

```bash
mkdir projeto
```

Opção comum:

```bash
mkdir -p: Cria diretórios incluindo hierarquias.
```

Exemplo:

```bash
mkdir -p pasta1/pasta2
```

---

### 6. Comando rm (Remove Files and Directories)

Remove arquivos ou diretórios.

Sintaxe:

```bash
rm [arquivo]
```

Para remover diretórios:

```bash
rm -r [diretório]
```

- Cuidado: O rm apaga permanentemente sem enviar para a lixeira.

---

### 7. Comando cp (Copy Files and Directories)

Copia arquivos ou diretórios.

Sintaxe:

```bash
cp [arquivo_origem] [destino]
```

Para copiar diretórios:

```bash
cp -r [diretório_origem] [destino]
```

---

### 8. Comando mv (Move or Rename Files)

Move ou renomeia arquivos e diretórios.

**Exemplo:**

```bash
#Mover:
mv arquivo.txt /home/user/Documents
```

```bash
#Renomear:
mv arquivo.txt novo_nome.txt
```
=======
Observação: ao pressionar a tecla `tab` o terminal autocompleta, e em caso de
diretórios ele adicionará uma `/` ao final do caminho, mas em casos de
arquivos ele só autocompleta o nome do mesmo.

---

## Resumo Visual do 1 ao 8

|Comando | Função | Exemplo|
|---|---|---|
|pwd | Exibe o caminho do diretório | pwd |
|ls | Exibe os arquivos e diretórios do caminho atual | ls -l |
|cd| Acessa o diretório especificado | cd /bin |
|touch | Cria arquivos vazios | touch log.txt|
|mkdir | Cria diretório | mkdir Recursos|
|rm | Remove arquivos e diretórios | rm -r trabalho/|
|cp | Copia arquivos e diretórios | cp arquivo.txt /Documents|
|mv | Move ou renomeia arquivos e diretórios | mv antigo.txt novo.txt|

---

### 9. Comando cat (Concatenate and Display Files)

O que faz? Exibe o conteúdo de um arquivo diretamente no terminal.
Analogia: É como abrir um livro e ler as páginas diretamente.

Sintaxe

 ```bash
 cat [nome_do_arquivo]
 ```

Exemplo

```bash
cat texto.txt
```

Saída

```bash
Este é o conteúdo do arquivo texto.txt.
```

- Dica

Para exibir o conteúdo numerando as linhas:

```bash
cat -n texto.txt
```

---

### 10. Comando more (Paginação de Arquivos)

O que faz? Exibe o conteúdo de arquivos página por página,
ideal para arquivos grandes.

Analogia: É como folhear um livro grande, uma página por vez.

Sintaxe

```bash
more [nome_do_arquivo]
```

Exemplo

```bash
more log.txt
```

- Teclas úteis durante a visualização com more:
  - Pressione Enter para avançar linha por linha.
  - Pressione Espaço para avançar página por página.
  - Pressione q para sair.

---

### 11. Comando less (Leitura Avançada de Arquivos)

O que faz? Funciona como o more, mas permite navegar para frente e para
trás no conteúdo do arquivo.

Analogia: É como usar um aplicativo de leitura com rolagem.

Sintaxe

```bash
less [nome_do_arquivo]
```

Exemplo

```bash
less log.txt
```

- Teclas úteis durante a visualização com less:
  - Pressione Seta para cima/baixo para navegar.
  - Pressione / seguido de uma palavra para procurar algo no arquivo.
  - Pressione q para sair.

---

### 12. Comando head (Primeiras Linhas de Arquivo)

O que faz? Exibe as primeiras linhas de um arquivo.
Analogia: É como ler o começo de um livro para entender o contexto.

Sintaxe

```bash
head [nome_do_arquivo]
```

Exemplo

```bash
head texto.txt
```

- Dica

Para especificar o número de linhas exibidas, use o parâmetro -n:

```bash
head -n 5 texto.txt
```

---

### 13. Comando tail (Últimas Linhas de Arquivo)

O que faz? Exibe as últimas linhas de um arquivo.
Analogia: É como ir direto ao final de um livro para ver o desfecho.

Sintaxe

```bash
tail [nome_do_arquivo]
```

Exemplo

```bash
tail log.txt
```

- Dica

Para monitorar um arquivo em tempo real (como logs), use o parâmetro -f:

```bash
tail -f log.txt
```

---

### 14. Comando find (Buscar Arquivos e Diretórios)

O que faz? Busca por arquivos ou diretórios no sistema.
Analogia: É como usar uma lupa para encontrar algo em sua casa.

Sintaxe

```bash
find [caminho] -name [nome_do_arquivo]
```

Exemplo

```bash
find /home/user -name "documento.txt"
```

- Dica

Para buscar arquivos sem diferenciar maiúsculas e minúsculas, use -iname:

```bash
find /home/user -iname "documento.txt"
```

---

### 15. Comando wc (Word Count)

O que faz? Conta linhas, palavras e caracteres de um arquivo.
Analogia: É como ter um contador automático para verificar o tamanho de um texto.

Sintaxe

```bash
wc [arquivo]
```

Exemplo

```bash
wc texto.txt
```

Saída

```bash
10  50  500 texto.txt
```

`(10 linhas, 50 palavras, 500 caracteres no arquivo texto.txt).`

- Dica

    Para contar apenas as linhas, use wc -l.
    Para contar apenas palavras, use wc -w.
    Para contar apenas caracteres, use wc -c.

---

## Resumo Visual do 9 ao 15

|Comando | Função | Exemplo|
|---|---|---|
|cat | Exibe o conteúdo de arquivos | cat texto.txt|
|more| Exibe arquivos página por página | more log.txt|
|less | Exibe arquivos com navegação avançada | less log.txt|
|head | Exibe as primeiras linhas de um arquivo | head -n 5 texto.txt|
|tail | Exibe as últimas linhas de um arquivo | tail -f log.txt|
|find | Busca arquivos ou diretórios | find /home/user -name "arquivo.txt"|
|wc | Conta linhas, palavras e caracteres | wc texto.txt|

