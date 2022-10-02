# **Primeiros Passos**
## **Git Init**

O comando `git init` é o primeiro comando necessário para iniciar um repositório local git em um diretório de sua escolha. Esse comando irá criar no diretório atual um novo diretório chamado `.git`. Imediatamente após executar esse comando seu repositório já apresenta um esqueleto, entretanto nada do seu projeto está sendo monitorado. Para que você consiga realizar o versionamento do seu código primeiro será necessário informar ao git quais arquivos ele deve monitorar com o comando `git add`. 

```bash
git init
```

## **Git Add**

O comando `git add` inclui arquivos para serem rastreados pelo SCV. Desse modo você pode escolher quais arquivos serão rastreados pelo git. 

> **Obs:** para monitorar quais arquivos estão ou não sendo rastreados pelo SCV utilize o comando `git status`.
> 
> Exemplo:
> ```bash
> git status
> ```
> 

Exemplos

```bash
git add *.c
git add HelloWorld.js
```

## **Git Rm**

Caso você queira remover arquivos do rastreamento pelo CSV, o comando `git rm` pode ser útil. Ele irá remover o arquivo do seu diretório de trabalho e fará com que no próximo commit esse arquivo seja removido do seu repositório. Se o arquivo tiver sido alterado ou se já estiver sendo rastreado, você terá que forçar a remoção com a opção `-f`.

```bash
git rm -f HelloWorld.js
```


## **Git Commit**

O comando `git commit` salva as alterações dos arquivos que estão sendo rastreados pelo SCV. Esse comando só salvará as alterações das versões do projeto que estão sendo rastreadas pelo git, ou seja, ao dar um commit você irá salvar uma *snapshot* das versões dos arquivos adicionados pelo comando `git add`. Desse modo sempre que alterar os arquivos do seu projeto lembre-se de adicionar os arquivos alterados novamente antes de realizar o commit.

Exemplo:
```bash
git commit
```

Ao executar o comando acima um editor de código de sua preferência será aberto para que você digite sua mensagem de commit. Uma alternativa para evitar a abertura do editor de código você pode utilizar a opção `-m` e escrever sua mensagem na mesma linha.

Exemplo
```bash
git commit -m "meu primeiro commit"
```

## Referências

1. [Git Docs](https://git-scm.com/docs)
2. CHACON S. & STRAUB B. **Pro Git**. 2. ed. Apress: 2021. Disponível em: [Git Book](https://git-scm.com/book/en/v2) 
