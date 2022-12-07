# Mario Gil Salazar

## ITT_2021_2022

Ingeniaritza Telematikoko Teknologia irakasgairako proba

~~~sh
https://www.hostinger.es/tutoriales/comandos-de-git
~~~

1. Poned en marcha la máquina virtual Ubuntu 20.04 que se encuentra en el Virtual Box.
   >Lo hago desde windows
2. Cread una cuenta GitHub

i. Cread un repositorio

ii. Buscad el siguiente repositorio "NekaneBilbao/ITT_2021_2022" y haced una
copia de él en vuestra cuenta

> Lo clono para coger los ficheros que contenga.

~~~sh
$ git clone https://github.com/NekaneBilbao/ITT_2021_2022.git
Cloning into 'ITT_2021_2022'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
~~~

> Cogemos los ficheros y los subimos a nuestro repo personal.

iii. Visualizad los repositorios que tenéis ahora

 >✅

3. Instalad Git

>✅

i. Visualizad y analizad las opciones que tiene Git. Mirad si coinciden con lo
explicado en teoría y cómo se utilizan

>✅

4. El repositorio que habéis creado en remoto copiadlo en local

~~~sh
$ git clone https://github.com/muriatx/ITT_2021_2022.git
Cloning into 'ITT_2021_2022'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
~~~

5. En la carpeta del repositorio local cread un fichero utilizando el editor vi

>$ git config --global core.editor "vi"

>$ git config --global core.editor "nano"

i. Escribid vuestro nombre en el fichero

~~~sh  
$ vi fich1.txt

$ cat fich1.txt
Mario Gil
~~~

ii. Mirad en qué estado se encuentra el fichero

> Está en estado "untraked":

~~~sh  
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fich1.txt

nothing added to commit but untracked files present (use "git add" to track)
~~~

iii. Poned el fichero de modo que pueda ser gestiona con el control de versiones,
es decir, incluidlo en el staging area

~~~sh  
$ git add fich1.txt
warning: in the working copy of 'fich1.txt', LF will be replaced by CRLF the next time Git touches it
~~~

iv. Volved a mirar en qué estado se encuentra el fichero

~~~sh  
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   fich1.txt
~~~

v. Guardad el fichero en el repositorio local

~~~sh  
$ git commit
[main 8e960f9] Apartado 5.V.
 1 file changed, 1 insertion(+)
 create mode 100644 fich1.txt
~~~

vi. Volved a mirar en qué estado se encuentra el fichero

~~~sh  
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working tree clean
~~~

vii. Añadid en el fichero el nombre de algún compañero de clase

~~~sh  
$ vi fich1.txt

$ cat fich1.txt
Mario Gil
Paula Rodriguez
~~~

viii. Volved a mirar en qué estado se encuentra el fichero

> Está en estado "modified":

~~~sh  
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fich1.txt
~~~

ix. Guardad el cambio realizado en el fichero en el repositorio local

~~~sh  
$ git add fich1.txt
warning: in the working copy of 'fich1.txt', LF will be replaced by CRLF the next time Git touches it

$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   fich1.txt

$ git commit
[main 5bdd715] Commit 5.IX.
 1 file changed, 1 insertion(+)
~~~

x. Mirad el histórico de cambios realizados en el repositorio local

~~~sh  
$ git log
commit 5bdd71518ef0c6fab00e29970970e4c390a0081b (HEAD -> main)
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:34:55 2022 +0100

    Commit 5.IX.

commit 8e960f9722b8c6bdb06e4f0dae2a09d7f788469f
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:28:05 2022 +0100

    Apartado 5.V.

commit 3de2c16e3eb8274d13c35e2cefcd861c34d639a3 (origin/main, origin/HEAD)
Author: Mario <60343471+muriatx@users.noreply.github.com>
Date:   Wed Dec 7 22:12:54 2022 +0100

    Add files via upload
~~~

6. Cread una nueva Branch (variante)

~~~sh  
$ git branch "rama1"

$ git branch
* main
  rama1
~~~

i. Moveros a la nueva branch y en el fichero añadid el nombre de otro compañero
de clase

~~~sh  
$ git checkout rama1
Switched to branch 'rama1'
M       README.md

$ git branch
  main
* rama1

$ vi fich1.txt

$ cat fich1.txt
Mario Gil
Paula Rodriguez
Yeray Rodri
~~~

ii. Mirad en qué estado se encuentra el fichero

~~~sh  
$ git status
On branch rama1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fich1.txt

$ git add fich1.txt

$ git status
On branch rama1
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   fich1.txt
~~~

iii. Guardad el cambio realizado en el fichero en el repositorio local

~~~sh  
$ git commit
[rama1 26c2632] Commit 6.III
 1 file changed, 1 insertion(+)
~~~

7. Visualizad el fichero de la branch de inicio y comprobad que no aparece el último
nombre introducido

~~~sh  
$ git branch
  main
* rama1

$ git checkout main
Switched to branch 'main'
M       README.md
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

$ git branch
* main
  rama1

$ cat fich1.txt
Mario Gil
Paula Rodriguez
~~~

8. Mirad el histórico de cambios realizados en el repositorio local

~~~sh  
$ git log
commit 5bdd71518ef0c6fab00e29970970e4c390a0081b (HEAD -> main)
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:34:55 2022 +0100

    Commit 5.IX.

commit 8e960f9722b8c6bdb06e4f0dae2a09d7f788469f
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:28:05 2022 +0100

    Apartado 5.V.

commit 3de2c16e3eb8274d13c35e2cefcd861c34d639a3 (origin/main, origin/HEAD)
Author: Mario <60343471+muriatx@users.noreply.github.com>
Date:   Wed Dec 7 22:12:54 2022 +0100

    Add files via upload

$ git checkout rama1
Switched to branch 'rama1'
M       README.md

$ git log
commit 26c263266f8a54d7eacd2139b4807243076688d9 (HEAD -> rama1)
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:42:08 2022 +0100

    Commit 6.III

commit 5bdd71518ef0c6fab00e29970970e4c390a0081b (main)
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:34:55 2022 +0100

    Commit 5.IX.

commit 8e960f9722b8c6bdb06e4f0dae2a09d7f788469f
Author: muriatx <mgil047@ikasle.ehu.eus>
Date:   Wed Dec 7 22:28:05 2022 +0100

    Apartado 5.V.

commit 3de2c16e3eb8274d13c35e2cefcd861c34d639a3 (origin/main, origin/HEAD)
Author: Mario <60343471+muriatx@users.noreply.github.com>
Date:   Wed Dec 7 22:12:54 2022 +0100

    Add files via upload
~~~  

9.  Volcad los cambios realizados al repositorio remoto

~~~sh  
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 564 bytes | 141.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/muriatx/ITT_2021_2022.git
   3de2c16..5bdd715  main -> main

~~~


