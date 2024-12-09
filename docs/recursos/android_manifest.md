


```
<manifest xmlns:android="http://schemas.android.com/apk/res/android" package="com.example.myapp">
<!--  Permisos necessaris per a l'aplicació  -->
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
<!--  Configuració de l'aplicació  -->
<application android:allowBackup="true" android:icon="@mipmap/ic_launcher" android:label="@string/app_name" android:roundIcon="@mipmap/ic_launcher_round" android:supportsRtl="true" android:theme="@style/AppTheme">
<!--  Activitat principal  -->
<activity android:name=".MainActivity">
<intent-filter>
<action android:name="android.intent.action.MAIN"/>
<category android:name="android.intent.category.LAUNCHER"/>
</intent-filter>
</activity>
</application>
</manifest>

```

# Explicación

El archivo `AndroidManifest.xml` es esencial en cualquier aplicación Android, ya que define información clave sobre la aplicación para el sistema operativo. Este archivo especifica los permisos que necesita la app, sus componentes (como actividades), y varios aspectos de su configuración.

Este archivo define los siguientes elementos clave para la aplicación:
- **Espacios de nombres y paquete**: El espacio de nombres `xmlns:android` define el esquema para los atributos, y el paquete (`com.example.myapp`) es la identificación única de la aplicación. Los ***espacios de nombre*** son una forma de evitar conflictos entre etiquetas y atributos que pueden tener el mismo nombre pero diferentes significados o usos.

- **Permisos**: 

(`<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>`) 

Estas líneas de código XML sirven para declarar dos permisos, uno para acceder a Internet y otro para comprobar el estado de la red.

- **Configuración de la aplicación**:

(`<application android:allowBackup="true" android:icon="@mipmap/ic_launcher" android:label="@string/app_name" android:roundIcon="@mipmap/ic_launcher_round" android:supportsRtl="true" android:theme="@style/AppTheme">`) 

Se configuran los atributos generales, como los iconos y el nombre de la app, 

- **Actividad principal**: Se define la actividad principal (`MainActivity`) que será mostrada al iniciar la aplicación.





