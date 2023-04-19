# **Primeiros Passos**
## **Git Init**

O comando `git init` é utilizado para iniciar um repositório local. Esse comando irá criar um subdiretório chamado `.git` contendo um "esqueleto" para seu repositório. Além disso, uma *branch* inicial será criada sem nenhum *commit*. 

```bash
git init
```

Com uma *branch* inicial já é possível iniciar o monitoramento e versionamento do código. Veja os próximos comandos deste arquivo para entender como monitorar um arquivo e suas alterações.

|Opção|Funçao|
|:-----:|:-----:|
|`-q`|Mostra apenas mensagens de erros e avisos.|
|`-b`|Especifica o nome para a *branch* inicial.|

## **Git Add**

O comando `git add` inclui arquivos para serem rastreados pelo SCV. Para fazer isso o comando atualiza o *index* (índice) do git, uma estrutura utilizada para guardar uma *snapshot* do código versionado. A última *snapshot* armazenada no *index* será utilizada como o conteúdo do próximo *commit*.

Para entender melhor como o processo pense que ao preparar o seu commit suas alterações estarão sendo "escaneadas" pelo git a medida que você as adiciona ao *stage*. Caso queira visualizar os arquivos que você já adicionou na *stage* atente-se a observação abaixo.

> **Obs:** para obter um sumário de quais modificações estão sendo rastreadas utilize o comando `git status`.
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

|Opção|Função|
|:-----:|:-----:|
|`-v`|Mostra mensagens mais verbosas.|
|`-f`|Permite rastrear arquivos outrora ignorados.|
|`-u`|Permite a modificação e/ou remoção de arquivos que já se apresentam no *index*, mas não adiciona nenhum novo arquivo.|
|`--all`|Atualiza o *index* de forma completa, sem ignorar remoções de arquivos, por exemplo.|
|`--no-all`|Atualiza o *index* adicionando novos arquivos/modificações, mas ignora remoções de arquivos.|

## **Git Commit**

O comando `git commit` salva a *snapshot* do *index* em um novo "*commit*". Um *commit* pode ser entendido como o estado do seu projeto em um ponto específico da linha do tempo. Portanto, na linha do tempo de desenvolvimento de um projeto, diversos *commits* estão presentes, permitindo a visualização de todo o processo de criação da uma aplicação.

Seu *commit* também deve apresentar uma "descrição", uma mensagem de *log*, para facilitar a localização de uma alteração na linha do tempo.

Exemplo:
```bash
git commit
```

Ao executar o comando acima um editor de código de sua preferência será aberto para que você digite uma mensagem. Essa mensagem será o título do seu *commit*, ao mesmo tempo, você também pode adicionar ao *commit* uma descrição. Uma alternativa é utilizar a opção `-m` e escrever sua mensagem na mesma linha.

Exemplo
```bash
git commit -m "meu primeiro commit"
```

|Opção|Função|
|:-----:|:-----:|
|`-m <msg>`|Usa a mensagem (msg) recebida como a descrição do seu *commit*.|
|`-a`|Permite realizar um *commit* que irá, automaticamente, fazer rastreamento de todos os arquivos modificados e deletados, não incluindo novos arquivos.|
|`-v`|Mostra de forma explícita e verbosa o commit que será realizado.|
|`-q`|Sumariza a mensagem de *commit*.|
|`-F <file>`|Pega a mensagem de *commit* do arquivo especificado.|

## Referências

1. [Git Docs](https://git-scm.com/docs)
2. CHACON S. & STRAUB B. **Pro Git**. 2. ed. Apress: 2021. Disponível em: [Git Book](https://git-scm.com/book/en/v2) 
