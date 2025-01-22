# **Aula 1: Introdução ao Shell e Comandos Básicos**

## O que é o Shell?

- O Shell é uma interface de linha de comando que permite interagir com
o sistema operacional.
- No Linux, o **Bash (Bourne Again Shell)** é um dos Shells mais utilizados.

---

## Conceitos Básicos

1. **Terminal**: Interface para interagir com o Shell.
2. **Prompt**: O local onde você digita comandos. Exemplo de prompt padrão:

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
drwxr-xr-x  2 user user 4096 Jan 16 10:00 Documents
-rw-r--r--  1 user user   20 Jan 16 09:30 file.txt
```

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

Cuidado: O rm apaga permanentemente sem enviar para a lixeira.

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
