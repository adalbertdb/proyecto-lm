# Proyecto Simple de Calculadora con Ant

En este documento explico cómo he creado un proyecto simple de una calculadora usando Apache Ant. El proyecto incluye las operaciones básicas de suma, resta, multiplicación y división.

## Estructura del Proyecto

Creé la siguiente estructura de carpetas y archivos:

```
calculadora/
├── src/
│   └── Calculadora.java
├── build/
├── dist/
├── build.xml
```

- **`src/`**: Contiene el código fuente.
- **`build/`**: Almacena los archivos `.class` después de compilar.
- **`dist/`**: Contiene el archivo JAR o ejecutable si se requiere empaquetar.
- **`build.xml`**: Archivo de configuración de Ant.

## Código Fuente de la Calculadora

Creé el archivo `src/Calculadora.java` con el siguiente contenido:

```java
package calculadora;

import java.util.Scanner;

public class Calculadora {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenido a la Calculadora");
        System.out.println("Elige una operación: ");
        System.out.println("1. Sumar");
        System.out.println("2. Restar");
        System.out.println("3. Multiplicar");
        System.out.println("4. Dividir");

        int opcion = scanner.nextInt();
        System.out.println("Ingresa el primer número:");
        double num1 = scanner.nextDouble();
        System.out.println("Ingresa el segundo número:");
        double num2 = scanner.nextDouble();

        double resultado = 0;

        switch (opcion) {
            case 1:
                resultado = num1 + num2;
                break;
            case 2:
                resultado = num1 - num2;
                break;
            case 3:
                resultado = num1 * num2;
                break;
            case 4:
                if (num2 != 0) {
                    resultado = num1 / num2;
                } else {
                    System.out.println("Error: División por cero.");
                    return;
                }
                break;
            default:
                System.out.println("Opción no válida.");
                return;
        }

        System.out.println("El resultado es: " + resultado);
    }
}
```

## Archivo `build.xml`

Creé el archivo `build.xml` en la raíz del proyecto con el siguiente contenido:

```xml
<project name="Calculadora" default="run" basedir=".">
    <!-- Variables de directorio -->
    <property name="src.dir" value="src" />
    <property name="build.dir" value="build" />
    <property name="dist.dir" value="dist" />
    <property name="main.class" value="calculadora.Calculadora" />

    <!-- Target: limpiar -->
    <target name="clean">
        <delete dir="${build.dir}" />
        <delete dir="${dist.dir}" />
    </target>

    <!-- Target: compilar -->
    <target name="compile" depends="clean">
        <mkdir dir="${build.dir}" />
        <javac srcdir="${src.dir}" destdir="${build.dir}" includeantruntime="false" />
    </target>

    <!-- Target: ejecutar -->
    <target name="run" depends="compile">
        <java classname="${main.class}" fork="true">
            <classpath>
                <pathelement path="${build.dir}" />
            </classpath>
        </java>
    </target>
</project>
```

## Pasos para Ejecutar el Proyecto

1. **Preparar el Proyecto**:
   - Creé las carpetas y archivos según la estructura.
   - Me aseguré de que el código fuente y el archivo `build.xml` estuvieran en las ubicaciones correctas.

2. **Limpiar el Proyecto**:
   Ejecuté el siguiente comando para eliminar archivos generados previamente:
   ```bash
   ant clean
   ```

3. **Compilar el Código**:
   Compilé el proyecto ejecutando:
   ```bash
   ant compile
   ```
   Esto generó los archivos `.class` en la carpeta `build/`.

4. **Ejecutar la Calculadora**:
   Para ejecutar la calculadora, utilicé:
   ```bash
   ant run
   ```

   Esto inició la aplicación en la terminal.

---
