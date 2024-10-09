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
        System.out.println("Ejercicio 1 realizado.");
    }
}    
```

