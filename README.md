# Taller Alias  Git

1. Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
   utilizar el comando git log con algunas opciones específicas para obtener un resumen
   gráfico de los últimos 5 commits en todas las ramas.


   <u>*Comando:*</u>

   ```bash
   git config --global alias.five "log --oneline --graph --decorate --all -n 5"
   ```

   <u>*Explicación de comando:*</u>

-    git config: Es el comando utilizado para configurar opciones de Git. Puede utilizarse para establecer diferentes configuraciones, como el nombre de usuario, el correo electrónico, alias, etc.

- --global: Es una opción que indica que queremos aplicar la configuración a nivel global, es decir, para todos los repositorios de Git en el sistema. Si no utilizamos --global, la configuración se aplicará solo al repositorio actual.

- alias.graphlog: Es el nombre del alias que estamos creando. En este caso, el alias se llamará "graphlog".

- "log --oneline --graph --decorate --all -n 5": Esta es la cadena de comandos que queremos que el alias ejecute.

   - log: Indica que queremos ver el registro de los commits.
   --oneline: Muestra cada commit en una sola línea, con su hash y mensaje.
   --graph: Muestra una representación gráfica de la historia del commit.
   --decorate: Muestra los nombres de las ramas y las etiquetas junto a los commits correspondientes.
   --all: Muestra commits de todas las ramas, no solo de la rama actual.
   -n 5: Limita la salida a los últimos 5 commits.



2. Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y
   detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones
   específicas para personalizar el formato y presentación de la salida. La salida debe tener
   las siguientes especificaciones:

​	Muestra una representación gráfica del historial de commits

​	Muestra el hash corto del commit en color rojo

​	Muestra las referencias (ramas o tags) en las que está involucrado el commit en color
​	amarillo

​	Muestra el mensaje del commit.

​	Muestra la fecha relativa del commit en color verde.

​	Muestra el hash del commit como un identificador abreviado.

​	Muestra las fechas de los commits de forma relativa

   <u>*Comando:*</u>

   ```bash
git config --global alias.gg "log --graph --format='%C(red)%h%C(reset) %C(yellow)%d%C(reset) %s %C(green)(%ar)%C(reset) [%C(blue)%h%C(reset)]' --abbrev-commit --date=relative"

   ```

   <u>*Explicación de comando:*</u>

   - `--graph`: Muestra una representación gráfica del historial de commits.

- `--pretty=format`: Define el formato de salida personalizado para cada commit.
- `%C(red)%h%C(reset)`: Muestra el hash corto del commit en color rojo.
- `%C(yellow)%d%C(reset)`: Muestra las referencias (ramas o tags) en las que está involucrado el commit en color amarillo.
- `%s`: Muestra el mensaje del commit.
- `%C(green)(%ar)%C(reset)`: Muestra la fecha relativa del commit en color verde.
- `[%C(blue)%h%C(reset)]`: Muestra el hash del commit como un identificador abreviado entre corchetes en color azul.
- `--abbrev-commit`: Muestra los hash de los commits de forma abreviada.
- `--date=relative`: Muestra las fechas de los commits de forma relativa.



   

3. Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
   el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
   completo es un poco tedioso. Quieres simplificarlo creando un alias personalizado.

<u>*Comando:*</u>

```bash
git config --global alias.lt "log -1 HEAD"
```

<u>*Explicación de comando:*</u>

- `git config --global`: Este comando se utiliza para configurar opciones de Git a nivel global en tu sistema. La opción `--global` indica que los cambios se aplicarán a todos los repositorios en tu sistema y se almacenarán en el archivo de configuración global de Git.

- `alias.lt`: Aquí estoy creando un alias llamado "lt". 

- `'log -1 HEAD'`: Esta es la definición del comando que queremos asociar con el alias "last". Estamos utilizando el comando `git log` con las siguientes opciones:
   - `-1`: Muestra solo el último commit.
   - `HEAD`: Especifica que queremos ver el commit más reciente en la rama actual.



4. Imagina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea
   es utilizar el comando git config para crear un alias que te permita abrir fácilmente la
   configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias
   llamado ec que cumpla con la especificación dada.

<u>*Comando:*</u>

```bash
git config --global alias.ec 'config --global --edit'
```

<u>*Explicación de comando:*</u>

- `git config --global`: Este comando se utiliza para configurar opciones de Git a nivel global en tu sistema. La opción `--global` indica que los cambios se aplicarán a todos los repositorios en tu sistema y se almacenarán en el archivo de configuración global de Git.

- `alias.ec: Aquí estoy creando un alias llamado "ec". 

- `'config --global --edit'`: Esta es la definición del comando que queremos asociar con el alias "ec". Estamos utilizando el comando `git config` con las siguientes opciones:
   - `--global`: Indica que estamos editando la configuración global de Git.
   
   - `--edit`: Abre el archivo de configuración global en el editor de texto predeterminado del sistema.
   
     

   5.Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores
   y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar
   la salida del historial de commits y resaltar información clave.

<u>*Comando:*</u>

```bash
git config --global alias.f "log --graph --abbrev-commit --decorate --format=format:'%C(auto)%h %C(red)%d %C(white)%s%C(reset)-%C(dim blue)-[%an]%C(reset)'"
```

<u>*Explicación de comando:*</u>

- `git config --global`: Este comando se utiliza para configurar opciones de Git a nivel global en tu sistema. La opción `--global` indica que los cambios se aplicarán a todos los repositorios en tu sistema y se almacenarán en el archivo de configuración global de Git.

- `alias.lh`: Aquí estamos creando un alias llamado "lph". Los alias son atajos que te permiten definir comandos personalizados para Git.

  - `--graph`: Muestra una representación gráfica del historial de commits para visualizar las ramificaciones y fusiones.

  - `--abbrev-commit`: Muestra el hash abreviado del commit para una mejor legibilidad.

  - `--decorate`: Muestra las referencias (ramas y tags) asociadas con cada commit en la salida.

  - `--all`: Muestra todos los commits accesibles desde cualquier rama, no solo desde la rama actual.

  - `--format=format:"..."`: Define un formato personalizado para la salida del `git log`. En este caso,       estamos utilizando varias secuencias de formato para mostrar diferentes partes del commit:
    
    el %c(auto)%h = genera una abreviación del has
    el %C(white)%s%C(reset) le pone color blanco a los comentarios 
    el %C(dim blue)-%an%C(reset) pone en azul el nombre del usuario





