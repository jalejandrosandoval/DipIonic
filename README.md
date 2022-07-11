# Dip_Ionic

Diplomado de Desarrollo de Aplicaciones híbridas utilizando Ionic y Angular. 

## Estructura de Archivos del Proyecto

```bash
└─IonicAPP
    ├─.angular
    ├─e2e
    ├─node_modules 
    └─src 
        ├─app
        │   ├─Components  
        │   │   └─...
        │   ├─Guards
        │   │   └─...
        │   ├─Interceptors
        │   │   └─...
        │   ├─Interfaces
        │   │   └─...
        │   ├─Pages
        │   │   └─...
        │   ├─Pipes
        │   │   └─...
        │   └─Services
        │      └─...
        ├─assets
        ├─enviroments
        └─theme
```

## Requisitos Previos Para Instalar IONIC y Angular

### Instalar NodeJs

* Descargar el instalador de [NodeJS](https://nodejs.org/es/).
* Ejecutar el instalador.

### Instalar Ionic

Una vez instalado NodeJS, se procede a abrir la consola de NodeJS <b>(Node.js command prompt)</b>, esto es con el fin de ejecutar los comandos para instalar Ionic y sus dependencias.

* Instalar Ionic en su ultima versión junto con sus dependencias:
```bash
npm i -g @ionic/cli native-run cordova-res
```

### Instalar Angular
Una vez instalado NodeJS, se procede a abrir la consola de NodeJS <b>(Node.js command prompt)</b>, esto es con el fin de ejecutar los comandos para instalar angular y sus dependencias.

* Instalar Angular en su ultima versión:
```bash
npm i -g @angular/cli
```

* Si se desea, instalar angular en una versión especifica se debe utilizar el siguiente comando:
```bash
npm i -g @angular/cli@'N°. Version'
```

* Para verificar la versión de angular instalada:

```bash
ng --version 
```
or
```bash
ng version 
```

### NodeModules

* Para instalar los nodemodules de proyecto se debe utilizar el siguiente comando:

```bash
npm i
```

### Instalar Otras Dependencias

Si se desea realizar desde 0 con la instalación del proyecto desde 0, se deben instalar uno a uno cada uno de los modules a utilizar; en este caso, se utilizará boostrap y algunos otros paquetes; Sin embargo, hay que tener en cuenta que al instalar cada dependencia se debe hacer su respectiva importación y/o llamado en el Archivo "Angular.JSON".

* #### Instalación de FireBase -> BD NSQL
Para instalar firebase solamente se debe ejecutar el siguiente comando:

```bash
npm i @angular/fire --save
```

* #### Instalación de Boostrap -> Estilos
Para instalar boostrap se requieren las dependencias de JQUERY y de PopperJS:

```bash
npm i boostrap jquery @popperjs/core --save
```

* #### Instalación de FontAwesome -> Iconos
Para instalar fontawesome basta con la siguiente linea de comando:

```bash
npm install --save @fortawesome/fontawesome-free --save
```

```bash
npm install @fortawesome/angular-fontawesome --save 
```

* #### Instalación de NGX-TOASTR -> Notificaciones
Para instalar Toastr, se requiere de la siguiente linea de comando:

```bash
npm install ngx-toastr --save
```
Junto con la instalación del siguiente paquete, el cual ayuda a la funcionalidad del TOASTR.

```bash
npm i @angular/animations --save
```

* #### Instalación de Datatables -> Visualizar en tablas info

```bash
npm install datatables.net --save
npm install datatables.net-dt --save
npm install angular-datatables --save
npm install @types/jquery --save-dev
npm install @types/datatables.net --save-dev
```

### Llamar o Vincular las dependencias instaladas en el proyecto

Para hacer el llamado, la vinculación o la importanción de las depencias instaladas se debe modificar el archivo <b> angular.json </b>, más exactamente se deben agregar estas lineas:

```bash
"styles": [
    "src/styles.css",
    "node_modules/datatables.net-dt/css/jquery.dataTables.css"              
    ],
"scripts": [
    "node_modules/jquery/dist/jquery.min.js",
    "node_modules/@popperjs/core/dist/umd/popper.min.js",
    "node_modules/bootstrap/dist/js/bootstrap.min.js",
    "node_modules/datatables.net/js/jquery.dataTables.js"
    ]
```

## Generación de Pages o Componentes

1. Ubicado en `...\IonicAPP\src\app>`.
2. Ejecute `ionic generate page name`. En este caso name corresponde al nombre de la página a crear.

```bash
..\IonicAPP\src\app> ionic generate page name
```

3. Ejecute `ionic generate component name`. En este caso name corresponde al nombre del componente a crear.

```bash
..\IonicAPP\src\app> ionic generate component name
```