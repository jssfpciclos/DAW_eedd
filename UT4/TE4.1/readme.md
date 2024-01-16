## TAREA EVALUABLE 4.1. TRABAJJO CON GIT (Comandos)

### Objetivos

- Conocer los comandos de git más importantes para trabajar con repositorios locales y remotos.
- Conocer el entorno de VS Code para trabajar con git.
- Conocer el lenguaje de marcado Markdown y su utilización en el desarrollo de documentación.


### Entrega

El documento justificativo de la realización de la tarea se realizará en formato `Markdown`, el nombre del fichero será `readme.md` y estará dentro de la carpeta `UT4\TE4.1` dentro del repositorio oficial del alumno para la asignatura.

El fichero `readme.md` debe contener los siguientes apartados:
  - Cada uno de los puntos de la tarea.
  - Explicación de los pasos realizados y una imagen/gif justificativo del paso. (las imagenes se guardarán en la carpeta `UT4\TE4.1\img`).
  

### 1. Crear repositorio local y subir a GITHUB

1. Crea una carpeta llamada `UT4.1.a`.
2. Inicializa un repositorio local en la carpeta `UT4.1.a`. ¿Qué comando/s utilizas?
3. Revisa qué rama se ha creado por defecto. ¿Qué comando/s utilizas?
4. Renombrar la rama por defecto a `main` en caso de que tenga otro nombre. ¿Qué comando/s utilizas?
5. Agrega un fichero `README.md`.
   
   ```markdown
    # UT4.1.a
    Repositorio de prueba para la tarea 4.1.a
   ```
6. Agrega el fichero `README.md` al stage area. ¿Qué comando/s utilizas?
7. Realiza un commit con el mensaje "Add README". ¿Qué comando/s utilizas?
8. Agrega otro fichero `01.xml` con siguiente texto.

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <libreria>
       <libro>
           <titulo>El Quijote</titulo>
           <autor>Miguel de Cervantes</autor>
           <editorial>Editorial Castalia</editorial>
           <fecha>1605</fecha>
           <genero>Novela</genero>
           <precio>20</precio>
       </libro>
   </libreria>
   ```
9. Agrega el fichero `01.xml` al stage area y realiza el commit "Add file 01.xml" ¿Qué comando/s utilizas?
10. Agrega una nueva rama llamada y posicionate directamente en ella con el mismo comando `fea/wac01`. ¿Qué comando/s utilizas? (busca en internet si no lo recuerdas)
11. En qué rama estas ahora mismo? ¿Qué comando/s utilizas?
12. Estando en la rama `fea/wac01` agrega un fichero `02.xml, y agrega al área de stage y realiza commit "Add file 02".

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>
    ```
13. Muestra el log utilizando solo una línea por commit con opciones gráficas. ¿Qué comando/s utilizas?
14. Posicionate de nuevo en la rama `main`, y crea otra rama `fea/wac02`, posicionandote direcamente en ella. Agrega un fichero `03.xml`, agrega al área de stage y realiza commit "Add file 03".

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```

15. Posicionate en la rama `main` y muestra los ficheros que hay en el directorio. ¿Qué comando/s utilizas?
16. Realizar un merge de la rama `fea/wac01` en la rama `main`. (Indica los comandos utilizados y explica cada uno de ellos).
17. Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen/gif visualizando los comandos)
18. Elimina la rama `fea/wac01` sin posibilidad de recuperación. ¿Qué comando/s utilizas?
19. Realiza un merge de la rama `fea/wac02` en la rama `main`. 
20. Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen)
21. Vuelve a la rama `fea/wac02` y modifica el fichero `03.xml` añadiendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```
    Agrega al área de stage y realiza commit "Update 03 file. Add book El Silmarillion".

22. Posicionate en la rama `main`, muestra el estado y muestra el contenido del fichero `cat 03.xml`. (Imagen visualizando comandos)

23. Realiza un merge de la rama `fea/wac02` en la rama `main`.
24. Muestra el estado del repositorio, y muestra el contenido del fichero `03.xml`. (Imagen visualizando comandos)
25. Ahora, en la rama `main` modifica el fichero `03.xml` incluyendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>    
    ```
    Agrega al área de stage y realiza commit "Update 03 file. Add book El Hobbit".

26. Agrega un nuevo fichero `04.xml` sobre libros ciencia-ficcion, en la rama `main`.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El fin de la eternidad</titulo>
            <autor>Isaac Asimov</autor>
            <editorial>Edhasa</editorial>
            <fecha>1955</fecha>
            <genero>Ciencia ficción</genero>
            <precio>20</precio>
        </libro>
    </liberia>
    ```

    Agrega al área de stage y realiza commit "Add 04 file. Add cienca-ficcion books".

27. Muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos)
28. Vuelve un commit atrás, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos)
29. Vuelve al commit anterior, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos)
30. Posicionate de nuevo en el último commit, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos)

### 2. Crear repositorio remoto y subir a GITHUB

1. Crea un repositorio remoto en GITHUB llamado `EEDD_{NombreApellido}_TE4.1` público, vacio, sin nada.
2. Agrega el repositorio remoto a tu repositorio local. ¿Qué comando/s utilizas?
3. Muestra los repositorios remotos que tienes configurados. ¿Qué comando/s utilizas?
4. Sube la rama `main` al repositorio remoto. ¿Qué comando/s utilizas?
5. Muestra el log de la rama `main` con opciones gráficas. ¿Qué comando/s utilizas?
6. Posicionate en la rama `fea/wac02` y sube la rama `fea/wac02` al repositorio remoto. ¿Qué comando/s utilizas?

7. Ahora desde GITHUB en la rama `fea\wac02`, modifica el fichero `04.xml` añadiendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El fin de la eternidad</titulo>
            <autor>Isaac Asimov</autor>
            <editorial>Edhasa</editorial>
            <fecha>1955</fecha>
            <genero>Ciencia ficción</genero>
            <precio>20</precio>
        </libro>
        <libro>
            <titulo>El hombre bicentenario</titulo>
            <autor>Isaac Asimov</autor>
            <editorial>Edhasa</editorial>
            <fecha>1976</fecha>
            <genero>Ciencia ficción</genero>
            <precio>20</precio>
        </libro>
    </libreria>
    ```
    Realiza un commit con el mensaje "Update 04 file. Add book El hombre bicentenario".
    (Muestra pantallazo de GITHUB con el commit realizado)

8. Ahora obten los cambios sin acualizar el repositorio local (`git fetch origin`).
9. Muestra un log del repositorio local con opciones gráficas. (Incluye imagen)
10. Ahora actualiza el repositorio local con los cambios del repositorio remoto (`git pull origin main`).
11. Muestra un log del repositorio local con opciones gráficas. (Incluye imagen)
12. Haz un merge de la rama `fea/wac02` en la rama `main`. Muestra estado, log, y el contenido fichero `04.xml` (Incluye imagen)
13. Elimina la rama local `fea/wac02` sin posibilidad de recuperación. ¿Qué comando/s utilizas?
14. Elimina la rama remota `fea/wac02` sin posibilidad de recuperación (git push origin --delete fea/wac02).
15. Muestra desde GITHUB las ramas que tienes el en repositorio remoto. (Incluye imagen)
16. Para finalizar, muestra el log del repositorio local con opciones gráficas. (Incluye imagen)


### 3. Enlace repositorio remoto

1. Incluye el enlace al repositorio remoto en este punto para que el profesor pueda acceder a él.
