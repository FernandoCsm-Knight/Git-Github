# **Clone & Log**
## **Clone**
O comando `git clone` clona um repositório git, local ou remoto, pré-existente. Cada versão de cada arquivo no histórico do projeto é obtida por padrão quando você executa esse comando.

Exemplo:
```bash
git clone <repository-path>
```
## **Log**
O comando `git log` mostra o histórico das alterações realizadas no repositório, como ciração de novas brenchs, commits e merges. Neste comando a alteração mais recente aparece primeiro.

Exemplo:
```bash
git log 
```

### **Argumentos**

Alguns dos argumentos mais importantes para o comando `git log` são o `-p` e o `-<number>`.

O comando `git log -p` mostra a alteração realizada nos commits.

```bash
git log -p
```
O comando `git log -<x>` mostra as últimas x alerações realizadas no repositório.

```bash
git log -10
```

#### **--stat & --pretty**

O argumento `--stat` é muito útil caso você queira receber algumas estatísticas acerca dos seus commits digite o comando. 

```bash
git log --stat
```

O argumento `--pretty` modifica os registros retornados para
formar outro formato diferente do padrão. Algumas opções para o comando já estão pré-definidos e remetem aos seguintes formatos: 

- `oneline`: retorna os registros em uma unica linha.
- `short`: retorna os registros com menos informações.
- `full`: retorna os registros com todas as informações necessárias.
- `fuller`: retorna os registros com todas as informações possíveis.

```bash
git log --pretty=oneline
git log --pretty=short
git log --pretty=full
git log --pretty=fuller
```

A opção `format` permite que você especifique um formato personalizado para a mensagem de retorno. Para utilizar essa opção você pode especificar máscaras para refletir o formato desejado da mensagem. As máscaras disponíveis estão presentes na tabela abaixo:

| Máscara | Saída | 
| :-------: | :----- |
| `%H` | Hash do commit |
| `%h` | Hash do commit abreviado |
| `%T` | Hash da árvore |
| `%t` | Hash da árvore abreviado |
| `%P` | Hashes dos pais |
| `%p` | Hashes dos pais abreviado |
| `%an` | Nome do Autor |
| `%ae` | Email do Autor |
| `%ad` | Data do Autor (o formato segue a opção --date=option) |
| `%ar` | Data do Autor, relativa |
| `%cn` | Nome do Committer |
| `%ce` | Email do Committer |
| `%cd` | Data do Committer |
| `%cr` | Data do Committer, relativa |
| `%s` | Comentário |

Exemplo:

```bash
git log --pretty=format:"%h - %an, %ar : %s"
```

#### **Tabela com mais opções:**

| Opção | Função |
| :---: | ----: |
| `-p` | Mostra o patch introduzido com cada commit.
| `--stat` | Mostra estatísticas de arquivos modificados em cada commit.
| `--shortstat` | Exibe apenas a linha informando a alteração, inserção e exclusão do comando --stat.
| `--name-only` | Mostra a lista de arquivos modificados após as informações de commit.
| `--name-status` | Mostra também a lista de arquivos que sofreram modificação com informações adicionadas / modificadas / excluídas.
| `--abbrev-commit` | Mostra apenas os primeiros caracteres da soma de verificação SHA-1 em vez de todos os 40.
| `--relative-date` | Exibe a data em um formato relativo (por exemplo, ‘` 2 semanas atrás '’) em vez de usar o formato de data completo.
| `--graph` | Exibe um gráfico ASCII do histórico de branches e merges ao lado da saída do log.
| `--pretty` | Mostra os commits em um formato alternativo. As opções incluem oneline, short, full, fuller e format (onde você especifica seu próprio formato).

## **Referências**

1. [Git Docs](https://git-scm.com/docs)
2. CHACON S. & STRAUB B. **Pro Git**. 2. ed. Apress: 2021. Disponível em: [Git Book](https://git-scm.com/book/en/v2) 