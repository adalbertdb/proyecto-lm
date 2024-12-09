# Instalación de Apache Maven en Windows

Maven es una herramienta para gestionar dependencias y automatizar la construcción de proyectos. Es mucho más extenso que ant.

## Paso 1: Descargar Apache Maven
1. Ve a la página oficial de Apache Maven: [https://maven.apache.org/](https://maven.apache.org/).
2. Haz clic en la sección "Download".
3. Descarga el archivo ZIP de la última versión estable.

## Paso 2: Extraer el archivo
Descomprime el archivo descargado en una carpeta de tu elección. Yo lo puse en:
```
C:\Herramientas\maven
```

## Paso 3: Configurar las variables de entorno

### Configurar `MAVEN_HOME`
1. Abre el Panel de Control > Sistema > Configuración avanzada del sistema > Variables de entorno.
2. En "Variables del sistema", haz clic en "Nueva" y añade:
   - **Nombre de la variable**: `MAVEN_HOME`
   - **Valor de la variable**: La ruta donde descomprimiste Maven, en mi caso:
     ```
     C:\Herramientas\maven
     ```

### Agregar Maven al `Path`
1. Busca la variable `Path` en "Variables del sistema" y haz clic en "Editar".
2. Añade esta línea al final:
   ```
   %MAVEN_HOME%\bin
   ```

### Configurar `JAVA_HOME` (si no lo has hecho antes)
1. Añade una nueva variable con:
   - **Nombre de la variable**: `JAVA_HOME`
   - **Valor de la variable**: La ruta de instalación de tu JDK (por ejemplo, `C:\Program Files\Java\jdk-XX.X.X`).

## Paso 4: Verificar la instalación
1. Abre una terminal (yo uso PowerShell, pero puedes usar CMD si prefieres).
2. Escribe el siguiente comando:
   ```bash
   mvn -version
   ```
3. Si todo está bien, deberías ver la versión de Maven, la de Java y la configuración del entorno.
