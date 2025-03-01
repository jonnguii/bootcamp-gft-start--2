🔀 Conflito de Merge

O que é Merge no Git?

Merge no Git é a operação de unir duas branches, ou seja, integrar as alterações feitas em uma branch secundária na branch principal do repositório. 
Fazemos isso com o objetivo principal de acoplar o trabalho feito nas versões distribuidas do projeto, no código principal, alinhando os caminhos.

🔹 Como o Merge funciona?

1. Antes de prosseguir, garantimos que estamos na branch que receberá as mudanças (exemplo: main) e usamos o comando git merge <branch-secundaria> para unir as alterações feitas na outra branch.
2. O Git identifica as diferenças entre as branches, combina as alterações automaticamente sempre que possível e, se necessário, solicita que o desenvolvedor resolva conflitos.
3. Após a fusão bem-sucedida, podemos confirmar as mudanças com git commit (se necessário) e enviá-las para o repositório remoto com git push.


📌 Exemplo de conflito

Tentamos enviar (push) mudanças para o repositório remoto, mas recebemos um erro:


```
$ git push origin master
To https://github.com/Perkles/livro-receitas.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/Perkles/livro-receitas.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.

```

Tentamos enviar mudanças ao nosso reposito remoto, mas o git percebeu que há novas alterações, ou seja, uma versão oficial não alinhada com a versão local.

```
$ git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 701 bytes | 50.00 KiB/s, done.
From https://github.com/Perkles/livro-receitas
 * branch            master     -> FETCH_HEAD
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```

Realizamos um "git pull", para "puxar" essa "versão oficial" do repositório remoto para o nosso local.
Ainda assim, percebemos um conflito: Ha um arquivo com 2 tipos de conteúdos.

⚠️ O que fazer quando há um conflito?

Quando realizamos um "git pull", automaticamente é feito um "git merge" pelo Git, mas, quando ele detecta um conflito onde ele não sabe quais dados manter, ele nos
da pistas e pede para resolvermos manualmente.


"Abrimos o arquivo "README.MD"":
```
<<<<<<< HEAD
(Nossa versão do código)
======= linha separadora
(Versão do código remoto)
>>>>>>> origin/master
```

Resolvemos o conflito, eliminando os dados errados e deixando o conteudo principal desejado, m
antendo apenas o conteúdo correto e removendo as marcas do Git (<<<<<<<, =======, >>>>>>>).

```
- Adicionamos o arquivo
git add README.md

- Descrevemos a alteração (commitamos)
git commit -m "Resolving README.md"

- Mandamos pro repositorio remoto
 git push origin main
```

Agora nosso código está atualizado, livre de conflitos e foi enviado ao repositório remoto com sucesso! 🚀


