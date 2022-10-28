<!doctype html>
<!--
    Programado por Luis Cabrera Benito 

  ____          _____               _ _           _       
 |  _ \        |  __ \             (_) |         | |      
 | |_) |_   _  | |__) |_ _ _ __ _____| |__  _   _| |_ ___ 
 |  _ <| | | | |  ___/ _` | '__|_  / | '_ \| | | | __/ _ \
 | |_) | |_| | | |  | (_| | |   / /| | |_) | |_| | ||  __/
 |____/ \__, | |_|   \__,_|_|  /___|_|_.__/ \__, |\__\___|
         __/ |                               __/ |        
        |___/                               |___/         
    
    
    Blog:       https://parzibyte.me/blog
    Ayuda:      https://parzibyte.me/blog/contrataciones-ayuda/
    Contacto:   https://parzibyte.me/blog/contacto/
-->
<html lang="es">
    <head>
        <meta charset="utf-8">
        <meta
            name="viewport"
            content="width=device-width, initial-scale=1,shrink-to-fit=no">
        <meta name="description" content="Jugar memorama en línea">
        <title>Gp seguros</title>
        <link href="./css/bootstrap.min.css" rel="stylesheet">
        <link href="./css/style.css" rel="stylesheet">
    </head>
    <body>
        <main role="main" class="container-fluid" id="app">
            <div class="row">
                <div class="col-12">
                    <h1 class="text-center">Gp seguros</h1>
                    <p>
                        <span class="h5">Intentos: </span>
                        {{intentos}}/{{MAXIMOS_INTENTOS}}&nbsp;<span class="h5">Aciertos:
                        </span> {{aciertos}}
                        <br><a @click="mostrarCreditos" href="#"></a>
                    </p>
                </div>
            </div>
            <div v-for="(fila, indiceFila) in memorama" :key="indiceFila"
                class="row">
                <div :key="indiceFila+''+indiceImagen" class="col-3"
                    v-for="(imagen, indiceImagen) in fila">
                    <div class="mb-3">
                        <img @click="voltear(indiceFila, indiceImagen)"
                            :class="{'girar': imagen.mostrar}"
                            :src="(imagen.mostrar ? imagen.ruta :
                            NOMBRE_IMAGEN_OCULTA)" class="card-img-top img-fluid
                            img-thumbnail">
                    </div>
                </div>
            </div>
        </main>
        <footer class="px-2 py-2 fixed-bottom bg-success text-white">
            <span>
                <a class="text-white" href="https://www.disenowebdiseno.com/"></a>
            </span>
        </footer>
        <script src="./js/sweetalert2.all.min.js"></script>
        <script src="./js/vue.min.js"></script>
        <script src="./js/script.js"></script>
    </body>

</html>
