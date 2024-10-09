# Entornos de Desarrollo: Comenzando con Git "Trabajando con Branchs

## Utilizo el git clone:

```CODE
pro@jpexposito-VirtualBox:~/Documentos$ git clone https://github.com/nexphernandez/ejercicio-git-branch
Clonando en 'ejercicio-git-branch'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Recibiendo objetos: 100% (3/3), listo.
```

## Creo una nueva rama:

```CODE
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout -b ejercicio1-branch
Cambiado a nueva rama 'ejercicio1-branch'
```

## Añado la clase .java:

```JAVA
     public class Ejercicio1 {
     public static void main(String[] args) {
         System.out.println("Ejercicio 1 realizado.");
     }
 }    
 ```

## Realizo el commit:

 ```Code
 pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git add .
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git commit -
m "Se incluye el Ejercici1.java"
[ejercicio1-branch ac2073f] Se incluye el Ejercici1.java
 2 files changed, 36 insertions(+), 1 deletion(-)
 create mode 100644 Ejercicio1.java
 rewrite README.md (100%)
 ```

## Subo los cambios a mi repositorio:

 ```Code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git push origin ejercicio1-branch
Enumerando objetos: 6, listo.
Contando objetos: 100% (6/6), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (4/4), listo.
Escribiendo objetos: 100% (4/4), 856 bytes | 856.00 KiB/s, listo.
Total 4 (delta 0), reusados 0 (delta 0), pack-reusados 0
remote: 
remote: Create a pull request for 'ejercicio1-branch' on GitHub by visiting:
remote:      https://github.com/nexphernandez/ejercicio-git-branch/pull/new/ejercicio1-branch
remote: 
To https://github.com/nexphernandez/ejercicio-git-branch
 * [new branch]      ejercicio1-branch -> ejercicio1-branch
```

## Fusiono la rama main:

```Code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout main                
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git merge ej
ercicio1-branch
Actualizando 9ff97a7..66f3f58
Fast-forward
 Ejercicio1.java |  5 ++++
 README.md       | 64 +++++++++++++++++++++++++++++++++++++++++++++++++-
 2 files changed, 68 insertions(+), 1 deletion(-)
 create mode 100644 Ejercicio1.java
 ```

## Creo una nueva rama:

```CODE
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git branch e
jercicio2-branch
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout
ejercicio2-branch
git: 'checkoutejercicio2-branch' no es un comando de git. Mira 'git --help'.
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout ejercicio2-branch
M       README.md
Cambiado a rama 'ejercicio2-branch'
```

## Añado la clase Ejercicio2:

```java
public class Ejercicio1 {
    public static void main(String[] args) {
        System.out.println("Ejercicio 2 realizado.");
    }
}    
```

## Realizo el commit:

```Code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git add .
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git commit -
m "Se incliye el Ejercicio2.java"
[ejercicio2-branch b6ccd2b] Se incliye el Ejercicio2.java
 2 files changed, 41 insertions(+)
 create mode 100644 Ejercicio2.java
```

## Subo los cambios a mi repositorio:

```CODE
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git push ori
gin ejercicio2-branch
Enumerando objetos: 9, listo.
Contando objetos: 100% (9/9), listo.
Compresión delta usando hasta 4 hipro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git push ori
gin ejercicio3-branch
Enumerando objetos: 6, listo.
Contando objetos: 100% (6/6), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (4/4), listo.
Escribiendo objetos: 100% (4/4), 579 bytes | 579.00 KiB/s, listo.
Total 4 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ejercicio3-branch' on GitHub by visiting:
remote:      https://github.com/nexphernandez/ejercicio-git-branch/pull/new/ejercicio3-branch
remote: 
To https://github.com/nexphernandez/ejercicio-git-branch
 * [new branch]      ejercicio3-branch -> ejercicio3-branch, listo.
Escribiendo objetos: 100% (7/7), 1.68 KiB | 1.68 MiB/s, listo.
Total 7 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'ejercicio2-branch' on GitHub by visiting:
remote:      https://github.com/nexphernandez/ejercicio-git-branch/pull/new/ejercicio2-branch
remote: 
To https://github.com/nexphernandez/ejercicio-git-branch
 * [new branch]      ejercicio2-branch -> ejercicio2-branch
```
## Fusiono la rama main:

```Code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout
 main
Cambiado a rama 'main'
Tu rama está adelantada a 'origin/main' por 2 commits.
  (usa "git push" para publicar tus commits locales)
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git merge ej
ercicio2-branch
Actualizando 66f3f58..13114af
Fast-forward
 Ejercicio2.java |  5 ++++
 README.md       | 70 ++++++++++++++++++++++++++++++++++++++++++++++++--
 2 files changed, 73 insertions(+), 2 deletions(-)
 create mode 100644 Ejercicio2.java
 ```
 
 ## Creo una nueva rama:

```Code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git branch e
jercicio3-branch
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git checkout ejercicio3-branch
M       README.md
Cambiado a rama 'ejercicio3-branch'
```
## Añado la clase Ejercicio2:

```Code
public class Ejercicio2 {
    public static void main(String[] args) {
        System.out.println("Ejercicio 3 realizado.");
    }
}    
```

## Realizo el commit:

```code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git add .
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git commit -
m "subo el ejercicio3"
[ejercicio3-branch 4aff737] subo el ejercicio3
 2 files changed, 30 insertions(+), 1 deletion(-)
 create mode 100644 Ejercicio3
```

## Subo los cambios a mi repositorio:

```code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-branch$ git push ori
gin ejercicio3-branch
Enumerando objetos: 6, listo.
Contando objetos: 100% (6/6), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (4/4), listo.
Escribiendo objetos: 100% (4/4), 579 bytes | 579.00 KiB/s, listo.
Total 4 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ejercicio3-branch' on GitHub by visiting:
remote:      https://github.com/nexphernandez/ejercicio-git-branch/pull/new/ejercicio3-branch
remote: 
To https://github.com/nexphernandez/ejercicio-git-branch
 * [new branch]      ejercicio3-branch -> ejercicio3-branch
```
