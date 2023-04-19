# Interagindo com o repositório

## Git Push

É o comando utilizado para atualizar seu repositório remoto a partir das alterações salvas em seu repositório local. Esse comando é utilizado quando você está com seus *commits* (veja [Init, Add e Commit](../Init%2C%20Add%20e%20Commit/README.md)) prontos e deseja salvalos em um repositório remoto, geralmente compartilhado.

Exemplo:
```bash
git push origin dev
```

Observe que o comando `push` apresenta como opções: o repositório remoto que deve ser atualizado e a *branch* que o desenvolvedor deseja atualizar. Portanto o comando pode ser visto da seguinte forma: `git push <repository> <branch>`.

> **Obs:** Caso você queira digitar apenas `git push` para atualizar um repositório padrão você pode utilizar o comando abaixo para configurar um repositório remoto de sua escolha.
>
> ```bash
> git push --set-upstream origin dev
> ```
>
> ou
>
> ```bash
> git push -u origin dev 
> ```

| Opção | Função |
| :-------: | :----- |
| `--all` | Atualiza todas as branchs de uma única vez. |
| `-d` | Todas as referencias citadas são deletadas do repositório remoto. |
| `-q` | Reprime todos os logs enviados duarnte a execução do comando. |
| `-v` | Expande os logs durante a execução do comando. |
| `-4` | Usa apenas endereços IPv4, ignorando endereços IPv6 |
| `-6` | Usa apenas endereços IPv6, ignorando endereços IPv4 |
## Git Pull



## Git Fetch



