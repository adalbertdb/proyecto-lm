# Ejercicio de ant

## Instalación de ant en Windows

# Instalación de Apache Ant en Windows

Apache Ant es una herramienta de automatización de construcción basada en Java. A continuación, se describe el proceso para instalar Apache Ant en un sistema Windows.

## Requisitos previos
1. **Java Development Kit (JDK)**: Apache Ant requiere que Java esté instalado y configurado en el sistema. Puedes descargarlo desde el sitio oficial de Oracle o utilizar una distribución de código abierto como OpenJDK.
   
   - [Descargar JDK](https://www.oracle.com/java/technologies/javase-downloads.html)

## Pasos de instalación

### 1. Descargar Apache Ant
1. Ve al sitio web oficial de Apache Ant: [https://ant.apache.org/](https://ant.apache.org/).
2. Dirígete a la sección de descargas ("Download") y selecciona la versión binaria más reciente.
3. Descarga el archivo comprimido (ZIP).

### 2. Extraer el archivo descargado
1. Extrae el contenido del archivo ZIP en un directorio de tu elección, por ejemplo:
   ```
   C:\Apache\ant
   ```

### 3. Configurar las variables de entorno

1. **Configurar `ANT_HOME`**:
   - Abre el Panel de Control > Sistema > Configuración avanzada del sistema > Variables de entorno.
   - En "Variables del sistema", haz clic en "Nuevo" y añade:
     - Nombre de la variable: `ANT_HOME`
     - Valor de la variable: Ruta del directorio donde se extrajo Apache Ant (por ejemplo, `C:\Apache\ant`).

2. **Agregar Ant al PATH**:
   - En la misma sección de "Variables del sistema", selecciona la variable `Path` y haz clic en "Editar".
   - Añade el siguiente valor al final de la lista:
     ```
     %ANT_HOME%\bin
     ```

3. **Configurar `JAVA_HOME` (si no está configurado)**:
   - Añade una nueva variable con:
     - Nombre de la variable: `JAVA_HOME`
     - Valor de la variable: Ruta de instalación del JDK (por ejemplo, `C:\Program Files\Java\jdk-XX.X.X`).

### 4. Verificar la instalación
1. Abre una terminal (símbolo del sistema o PowerShell).
2. Escribe el siguiente comando y presiona Enter:
   ```
   ant -version
   ```
3. Deberías ver la versión de Apache Ant instalada.

