# Como compilar en java

## Directorios
```
projecte/
├── build/               
├── com/                  
│   └── dennis/           
│       └── edd/          
│           ├── Calculadora.java   
│           └── Main.java   

```

## Codigo
He creado esta calculadora en java la cual utiliza 2 archivos. Uno para el main y otra guarda las funciones (sumar, restar, multiplcar y dividir.)
### Calculadora.java
```
package com.dennis.edd;

public class Calculadora {
    public static int suma(int a, int b) {
        return a + b;
    }

    public static int resta(int a, int b) {
        return a - b;
    }

    public static int multiplica(int a, int b) {
        return a * b;
    }

    public static int divideix(int a, int b) {
        if (b == 0) {
            System.err.println("Error: no es pot dividir entre zero.");
            return 0;
        }
        return a / b;
    }
}
```
### Main.java
```
package com.dennis.edd;
public class main {
    public class Main {
        public static void main(String[] args) {
            int a = 20;
            int b = 5;
    
            System.out.println("Suma: " +Calculadora.suma(a, b));
            System.out.println("Resta: " + Calculadora.resta(a, b));
            System.out.println("Multiplicació: " + Calculadora.multiplica(a, b));
            System.out.println("Divisió: " + Calculadora.divideix(a, b));
    
            // Exemple de divisió entre zero
            System.out.println("Divisió entre zero: " + Calculadora.divideix(a, 0));
        }
    }
}

```
## Compilar y ejecutar
Para compilar el archivo utilizamos el siguiente comando

```
javac -d projecte/build/ projecte/com/dennis/edd/*.java
``` 
Y para ejecutar el archivo utilizamos el comando
```
java -cp build com.dennis.edd.Main

```
# Java ANT

Para compilar con ant editamos la estructura de directorios para que se vea así.
```
projecte/
├── build/                
├── src/                  
│   └── com/
│       └── usuari/
│           └── edd/
│               ├── Calculadora.java
│               └── Main.java
├── build.xml               
```
En la carpeta projecte a parte de tener las carpetas build y src agregamos el archivo build.xml con el siguiente contenido. Este le indica a ant que debe hacer con cada uno de sus comandos
```
<project name="Calculadora" default="run" basedir=".">
    <!-- Directorios -->
    <property name="src" value="src"/>
    <property name="build" value="build"/>

    <!-- Limpieza -->
    <target name="clean">
        <delete dir="build"/>
    </target>

    <!-- Compilación -->
    <target name="compile">
        <mkdir dir="build"/>
        <javac srcdir="src.dir" destdir="build.dir" includeantruntime="false"/>
    </target>

    <!-- Ejecución -->
    <target name="run" depends="compile">
        <java classname="com.usuari.edd.Main" fork="true">
            <classpath>
                <pathelement path="build"/>
            </classpath>
        </java>
    </target>
</project>

```
## Comandos de ANT

Para compilar usamos 
```
ant compile
```
Para ejecutar usamos
```
ant run
```
Para limpiar los archivos compilados (.class)
```
ant clean
```
