# Proyecto Simple con Maven

En este documento detallo cómo he creado y configurado un proyecto simple en Maven, cubriendo tres métodos diferentes: utilizando la línea de comandos, Visual Studio Code y otro IDE de mi elección.

## Configuración del Proyecto con Maven desde la Línea de Comandos

1. **Crear el Proyecto**:
   Desde la línea de comandos, ejecuté el siguiente comando para generar un proyecto basado en el arquetipo `maven-archetype-quickstart`:
   ```bash
   mvn archetype:generate -DgroupId=com.miempresa -DartifactId=mi-proyecto -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
   ```
   Esto generó la estructura básica del proyecto Maven:
   ```
   mi-proyecto/
   ├── pom.xml
   └── src/
       ├── main/
       │   └── java/
       │       └── com/miempresa/App.java
       └── test/
           └── java/
               └── com/miempresa/AppTest.java
   ```

2. **Verificar el Proyecto**:
   Para asegurarme de que el proyecto fue creado correctamente, ejecuté:
   ```bash
   mvn compile
   ```

3. **Ejecutar el Proyecto**:
   Para ejecutar la aplicación principal:
   ```bash
   mvn exec:java -Dexec.mainClass="com.miempresa.App"
   ```

## Configuración del Proyecto con Maven en Visual Studio Code

1. **Abrir el Proyecto en VSCode**:
   - Abrí la carpeta del proyecto `mi-proyecto` en Visual Studio Code.
   - Me aseguré de tener instaladas las extensiones necesarias, como **Maven for Java** y **Debugger for Java**.

2. **Compilar el Proyecto**:
   Utilicé la terminal integrada en VSCode para ejecutar:
   ```bash
   mvn compile
   ```

3. **Ejecutar la Aplicación**:
   - Configuré una tarea de depuración en VSCode para la clase principal `com.miempresa.App`.
   - Hice clic en **Run and Debug** y seleccioné la configuración.
   - La aplicación se ejecutó correctamente en el entorno de VSCode.

## Configuración del Proyecto con Maven en Apache NetBeans

1. **Importar el Proyecto**:
   - Abrí Apache NetBeans y seleccioné **Open Project** para cargar la carpeta del proyecto `mi-proyecto`.
   - NetBeans detectó automáticamente el archivo `pom.xml` y configuró el entorno del proyecto.

2. **Compilar el Proyecto**:
   - Desde la pestaña de proyectos, hice clic derecho sobre el nombre del proyecto y seleccioné **Build**.

3. **Ejecutar la Aplicación**:
   - Hice clic derecho sobre el proyecto y seleccioné **Run**.
   - La aplicación se ejecutó correctamente en la consola integrada de NetBeans.

---
