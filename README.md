# Taller Alias  Git

1. Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
   utilizar el comando git log con algunas opciones específicas para obtener un resumen
   gráfico de los últimos 5 commits en todas las ramas.

   <u>*Comando:*</u>

   ```bash
   git config --global alias.lg 'log --graph --pretty=format:"%C(red)%h%Creset%C(yellow)%d%Creset %s %C(green)(%ar)%Creset" --abbrev-commit'
   ```

   <u>*Explicación de comando:*</u>

   - `git config --global`: Este comando se utiliza para configurar opciones de Git a nivel global en tu sistema. La opción `--global` indica que los cambios se aplicarán a todos los repositorios en tu sistema y se almacenarán en el archivo de configuración global de Git.

   - `git log`: Este es el comando principal que estamos utilizando. `git log` muestra el historial de commits de un repositorio Git.

   - `--graph`: Esta opción de `git log` muestra una representación gráfica del historial de commits. La representación gráfica es útil para visualizar la estructura de ramificación y fusión en el repositorio.

   - `--pretty=format:'...'`: Esta opción nos permite personalizar el formato de salida del `git log`. En este caso, estamos definiendo un formato personalizado para cómo se muestran los commits en la salida.

   - `%C(red)`, `%C(yellow)`, `%C(green)`, `%Creset`: Estas secuencias de escape son utilizadas para cambiar el color del texto en la salida del `git log`. Por ejemplo, `%C(red)` establece el color rojo, `%C(yellow)` establece el color amarillo, `%C(green)` establece el color verde, y `%Creset` reinicia el color.

   - `%h`: Muestra el hash corto del commit.

   - `%d`: Muestra las referencias (ramas o tags) en las que está involucrado el commit.

   - `%s`: Muestra el mensaje del commit.

   - `%ar`: Muestra la fecha relativa del commit. Por ejemplo, "hace 3 días".

   - `--abbrev-commit`: Esta opción de `git log` muestra los hashes de commit como identificadores abreviados.

   

2. Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
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

   

3. Imagina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea
   es utilizar el comando git config para crear un alias que te permita abrir fácilmente la
   configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias
   llamado ec que cumpla con la especificación dada.

   <u>*Comando:*</u>

   ```bash
   git config --global alias.t 'config --global --edit'
   ```

   <u>*Explicación de comando:*</u>

   - `git config --global`: Este comando se utiliza para configurar opciones de Git a nivel global en tu sistema. La opción `--global` indica que los cambios se aplicarán a todos los repositorios en tu sistema y se almacenarán en el archivo de configuración global de Git.

   - `alias.t: Aquí estoy creando un alias llamado "t". 

   - `'config --global --edit'`: Esta es la definición del comando que queremos asociar con el alias "ec". Estamos utilizando el comando `git config` con las siguientes opciones:
      - `--global`: Indica que estamos editando la configuración global de Git.
      - `--edit`: Abre el archivo de configuración global en el editor de texto predeterminado del sistema.

   

4. Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores
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

     - `--format=format:"..."`: Define un formato personalizado para la salida del `git log`. En este caso, estamos utilizando varias secuencias de formato para mostrar diferentes partes del commit:
       
       
       el %c(auto)%h = genera una abreviación del has
       
       el %C(white)%s%C(reset) le pone color blanco a los comentarios 
       el %C(dim blue)-%an%C(reset) pone en azul el nombre del usuario

   



