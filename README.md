# <Imitación de la página web del Soumaya usando Html y Css con Bootstrap>

Enlace de la página: https://davidlem548-jpg.github.io/DesarrolloWeb-BootstrapSoumaya/

# -- Proceso de creación del sitio hasta llevarlo a la rama main:

1. Inicializar el repositorio local
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya
$ git init
Initialized empty Git repository in C:/Users/david/OneDrive/Escritorio/tarea-bootstrap/tareaSoumaya/.git/

2. Crear la rama que no sea main
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (master)
$ git switch -c ramaInicial
Switched to a new branch 'ramaInicial'

3. Agregar el origen remoto del repo de github "davidlem548-jpg/sitioWebSoumaya"
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git remote add origin https://github.com/davidlem548-jpg/sitioWebSoumaya

4. Añadir los archivos index.html y la hoja de estilado styles.css
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git add index.html
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git add styles.css

5. Hacer commit de los cambios y push
david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git commit -m "Sitio web del Soumaya"
[ramaInicial (root-commit) e824787] Sitio web del Soumaya
 2 files changed, 436 insertions(+)
 create mode 100644 index.html
 create mode 100644 styles.css

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git push -u origin ramaInicial
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 5.13 KiB | 2.56 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/davidlem548-jpg/sitioWebSoumaya
 * [new branch]      ramaInicial -> ramaInicial
branch 'ramaInicial' set up to track 'origin/ramaInicial'.

6. Crear una rama main vacía

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git switch --orphan main
Switched to a new branch 'main'

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (main)
$ git commit --allow-empty -m "Inicializar main vacía"
[main (root-commit) 2557734] Inicializar main vacía

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (main)
$ git push -u origin main
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Writing objects: 100% (2/2), 181 bytes | 181.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya/pull/new/main
remote:
To https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

7. hacer que 'ramaInicial' nazca desde main:

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (main)
$ git fetch origin --prune

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (main)
$ git switch ramaInicial
Switched to branch 'ramaInicial'
Your branch is up to date with 'origin/ramaInicial'.

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git rebase --rebase-merges --onto origin/main --root
Successfully rebased and updated refs/heads/ramaInicial.

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git push -f
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 5.12 KiB | 2.56 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya
 + 6732805...d916f31 ramaInicial -> ramaInicial (forced update)

8. Aquí se hizo el siguiente pull request para mergear ramaInicial con main:
https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya/pull/1

- Ya quedó en main el proyecto completo

# Carga de los archivos de video

 8. Agregar y hacer push de los archivos de evidencia de video

 david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git status
On branch ramaInicial
Your branch is up to date with 'origin/ramaInicial'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        SamsungGalaxy.mp4
        ipadMini.mp4
        ipadPro.mp4

nothing added to commit but untracked files present (use "git add" to track)

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git add SamsungGalaxy.mp4

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git add ipadMini.mp4

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git add ipadPro.mp4

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git commit -m "Evidencias de video"
[ramaInicial 23b342d] Evidencias de video
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 SamsungGalaxy.mp4
 create mode 100644 ipadMini.mp4
 create mode 100644 ipadPro.mp4

david@David MINGW64 /c/users/david/onedrive/escritorio/tarea-bootstrap/tareaSoumaya (ramaInicial)
$ git push -u origin ramaInicial
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 51.25 MiB | 6.41 MiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya
   d916f31..23b342d  ramaInicial -> ramaInicial
branch 'ramaInicial' set up to track 'origin/ramaInicial'.

9. Aquí se hizo un pull request de ramaInicial a main, para cargar ahí las evidencias de video
https://github.com/davidlem548-jpg/DesarrolloWeb-BootstrapSoumaya/pull/2