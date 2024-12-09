# Ejemplos de lenguajes interpretados vs lenguajes compilados

### Python
Python es un lenguaje interpretado, lo cual significa que no es necesario generar un archivo binario para ejecutar su contenido. El código fuente de Python es procesado por un intérprete en tiempo de ejecución, lo que facilita la ejecución de scripts de manera rápida y flexible. Para ejecutar un archivo Python, utilizamos el siguiente comando:

`python programa1.py`

### Java
Java es un caso especial, ya que primero necesita ser compilado a bytecode y luego ejecutarse en su propia máquina virtual (JVM, Java Virtual Machine). Este enfoque permite que el código sea independiente de la plataforma, ya que la JVM se encarga de ejecutar el bytecode en diferentes sistemas operativos. Para compilar y ejecutar un archivo Java, se utilizan los siguientes comandos:

1. Compilar el archivo Java:
   
   `javac programa1.java`

2. Ejecutar el archivo compilado:

   `java programa1`

### C
C es un lenguaje compilado, lo que significa que el código fuente se transforma en un archivo binario antes de poder ejecutarse. Este proceso de compilación es específico para cada plataforma, por lo que el archivo ejecutable generado solo funcionará en el sistema operativo para el que fue compilado. Para compilar y ejecutar un archivo C, se utilizan los siguientes comandos:

1. Compilar el archivo C:

   `gcc programa1.c -o programa1`

2. Ejecutar el archivo compilado:

   `./programa1`

