<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>AURA PERFUMES | Compra con Propósito</title>

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: #faf7f5;
            color: #333;
        }

        header {
            background-color: #241b1f;
            color: white;
            padding: 20px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #e8b4b8;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: bold;
        }

        nav a:hover {
            color: #e8b4b8;
        }

        .carrito {
            background-color: #b76e79;
            padding: 10px 15px;
            border-radius: 8px;
        }

        .inicio {
            min-height: 600px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 40px;

            background:
                linear-gradient(
                    rgba(36,27,31,0.75),
                    rgba(36,27,31,0.75)
                ),
                url("https://images.unsplash.com/photo-1541643600914-78b084683601")
                center/cover;
        }

        .inicio h1 {
            font-size: 65px;
            color: #f1c5c9;
            margin-bottom: 15px;
        }

        .inicio h2 {
            color: white;
            font-size: 28px;
            margin-bottom: 20px;
        }

        .inicio p {
            max-width: 750px;
            color: #eeeeee;
            font-size: 18px;
            line-height: 1.7;
        }

        .boton {
            display: inline-block;
            margin-top: 30px;
            padding: 14px 30px;
            background-color: #b76e79;
            color: white;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
        }

        .boton:hover {
            background-color: #d38b95;
        }

        section {
            padding: 70px 8%;
        }

        section h2 {
            text-align: center;
            color: #9b5360;
            font-size: 36px;
            margin-bottom: 40px;
        }

        .productos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
        }

        .producto {
            background-color: white;
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            transition: 0.3s;
        }

        .producto:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .imagen {
            height: 180px;
            background-color: #f3e8e9;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            margin-bottom: 15px;
        }

        .producto h3 {
            color: #4b3036;
            margin-bottom: 10px;
        }

        .producto p {
            color: #777;
            min-height: 40px;
        }

        .precio {
            display: block;
            color: #a45261;
            font-size: 21px;
            font-weight: bold;
            margin: 15px 0;
        }

        .producto button {
            border: none;
            background-color: #b76e79;
            color: white;
            padding: 10px 18px;
            border-radius: 7px;
            cursor: pointer;
            font-weight: bold;
        }

        .producto button:hover {
            background-color: #963f4d;
        }

        .proposito {
            background-color: #241b1f;
            color: white;
            text-align: center;
        }

        .proposito h2 {
            color: #f1c5c9;
        }

        .proposito-contenido {
            max-width: 850px;
            margin: auto;
        }

        .proposito p {
            font-size: 18px;
            line-height: 1.8;
            color: #eeeeee;
        }

        .donacion {
            margin: 35px auto;
            max-width: 450px;
            padding: 30px;
            background-color: #38272d;
            border-radius: 15px;
        }

        .donacion h3 {
            font-size: 35px;
            color: #f1c5c9;
            margin-bottom: 10px;
        }

        .tarjetas {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 35px;
        }

        .tarjeta {
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .tarjeta h3 {
            color: #9b5360;
            margin-bottom: 15px;
        }

        .nosotros {
            text-align: center;
        }

        .nosotros > p {
            max-width: 850px;
            margin: auto;
            color: #666;
            font-size: 18px;
            line-height: 1.8;
        }

        .formulario {
            max-width: 600px;
            margin: auto;
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .formulario label {
            display: block;
            margin-top: 15px;
            margin-bottom: 7px;
            font-weight: bold;
        }

        .formulario input,
        .formulario textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 7px;
        }

        .formulario textarea {
            height: 120px;
            resize: none;
        }

        .formulario button {
            margin-top: 20px;
            width: 100%;
            padding: 13px;
            border: none;
            border-radius: 7px;
            background-color: #b76e79;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }

        #carrito {
            background-color: #f1e7e8;
        }

        #listaCarrito {
            max-width: 800px;
            margin: auto;
        }

        .item-carrito {
            background-color: white;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .item-carrito button {
            background-color: #963f4d;
            color: white;
            border: none;
            padding: 7px 10px;
            border-radius: 5px;
            cursor: pointer;
        }

        .total {
            max-width: 800px;
            margin: 20px auto;
            text-align: right;
            font-size: 25px;
            color: #9b5360;
            font-weight: bold;
        }

        .donacion-carrito {
            max-width: 800px;
            margin: 10px auto;
            text-align: right;
            color: #9b5360;
            font-weight: bold;
        }

        footer {
            background-color: #241b1f;
            color: #ccc;
            text-align: center;
            padding: 35px;
        }

        footer strong {
            color: #e8b4b8;
        }

        @media(max-width: 700px) {

            header {
                flex-direction: column;
                gap: 15px;
                padding: 20px;
            }

            nav {
                text-align: center;
            }

            nav a {
                display: inline-block;
                margin: 5px;
                font-size: 14px;
            }

            .inicio h1 {
                font-size: 42px;
            }

            .inicio h2 {
                font-size: 21px;
            }

        }

    </style>
</head>


<body>


<header>

    <div class="logo">
        AURA PERFUMES
    </div>

    <nav>

        <a href="#inicio">Inicio</a>

        <a href="#productos">Perfumes</a>

        <a href="#proposito">Compra con Propósito</a>

        <a href="#nosotros">Nosotros</a>

        <a href="#contacto">Contacto</a>

        <a href="#carrito" class="carrito">
            🛒 Carrito <span id="contador">0</span>
        </a>

    </nav>

</header>



<main>


<!-- INICIO -->

<section class="inicio" id="inicio">

    <h1>AURA PERFUMES</h1>

    <h2>
        “Una fragancia que deja huella.”
    </h2>

    <p>
        Descubre nuestra colección de perfumes para hombre y mujer.
        En AURA PERFUMES creemos que una compra puede hacer la diferencia,
        por eso el 5% de cada compra será destinado a apoyar a niños
        con cáncer.
    </p>

    <a href="#productos" class="boton">
        VER PERFUMES
    </a>

</section>



<!-- PRODUCTOS -->

<section id="productos">

    <h2>Nuestros Perfumes</h2>

    <div class="productos">


        <article class="producto">

            <div class="imagen">🌹</div>

            <h3>Aura Rose</h3>

            <p>Fragancia floral y elegante.</p>

            <span class="precio">$899 MXN</span>

            <button onclick="agregar('Aura Rose',899)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌸</div>

            <h3>Pink Essence</h3>

            <p>Aroma dulce con notas florales.</p>

            <span class="precio">$799 MXN</span>

            <button onclick="agregar('Pink Essence',799)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌺</div>

            <h3>Bloom</h3>

            <p>Perfume floral para mujer.</p>

            <span class="precio">$950 MXN</span>

            <button onclick="agregar('Bloom',950)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">✨</div>

            <h3>Golden Aura</h3>

            <p>Fragancia elegante y sofisticada.</p>

            <span class="precio">$1,199 MXN</span>

            <button onclick="agregar('Golden Aura',1199)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌹</div>

            <h3>Velvet Rose</h3>

            <p>Aroma intenso de rosas.</p>

            <span class="precio">$999 MXN</span>

            <button onclick="agregar('Velvet Rose',999)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🍓</div>

            <h3>Sweet Berry</h3>

            <p>Fragancia dulce y juvenil.</p>

            <span class="precio">$699 MXN</span>

            <button onclick="agregar('Sweet Berry',699)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌙</div>

            <h3>Midnight</h3>

            <p>Perfume para ocasiones especiales.</p>

            <span class="precio">$1,099 MXN</span>

            <button onclick="agregar('Midnight',1099)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">💐</div>

            <h3>Floral Dream</h3>

            <p>Mezcla de flores y frutas.</p>

            <span class="precio">$849 MXN</span>

            <button onclick="agregar('Floral Dream',849)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌷</div>

            <h3>Elegant Lady</h3>

            <p>Fragancia femenina elegante.</p>

            <span class="precio">$1,049 MXN</span>

            <button onclick="agregar('Elegant Lady',1049)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🍊</div>

            <h3>Citrus Fresh</h3>

            <p>Aroma fresco con notas cítricas.</p>

            <span class="precio">$749 MXN</span>

            <button onclick="agregar('Citrus Fresh',749)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌿</div>

            <h3>Green Nature</h3>

            <p>Fragancia fresca y natural.</p>

            <span class="precio">$799 MXN</span>

            <button onclick="agregar('Green Nature',799)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🖤</div>

            <h3>Black Night</h3>

            <p>Aroma profundo y elegante.</p>

            <span class="precio">$1,099 MXN</span>

            <button onclick="agregar('Black Night',1099)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🔥</div>

            <h3>Intense</h3>

            <p>Fragancia intensa y duradera.</p>

            <span class="precio">$1,299 MXN</span>

            <button onclick="agregar('Intense',1299)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌊</div>

            <h3>Ocean Blue</h3>

            <p>Aroma fresco inspirado en el océano.</p>

            <span class="precio">$899 MXN</span>

            <button onclick="agregar('Ocean Blue',899)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌲</div>

            <h3>Forest</h3>

            <p>Notas de madera y naturaleza.</p>

            <span class="precio">$949 MXN</span>

            <button onclick="agregar('Forest',949)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">👑</div>

            <h3>Royal</h3>

            <p>Perfume elegante de alta gama.</p>

            <span class="precio">$1,499 MXN</span>

            <button onclick="agregar('Royal',1499)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">💎</div>

            <h3>Diamond</h3>

            <p>Fragancia sofisticada y moderna.</p>

            <span class="precio">$1,399 MXN</span>

            <button onclick="agregar('Diamond',1399)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🍋</div>

            <h3>Lemon Fresh</h3>

            <p>Aroma cítrico y refrescante.</p>

            <span class="precio">$699 MXN</span>

            <button onclick="agregar('Lemon Fresh',699)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌼</div>

            <h3>Sun Flower</h3>

            <p>Fragancia floral y luminosa.</p>

            <span class="precio">$849 MXN</span>

            <button onclick="agregar('Sun Flower',849)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🍯</div>

            <h3>Honey Touch</h3>

            <p>Aroma dulce y cálido.</p>

            <span class="precio">$899 MXN</span>

            <button onclick="agregar('Honey Touch',899)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌌</div>

            <h3>Galaxy</h3>

            <p>Fragancia moderna y misteriosa.</p>

            <span class="precio">$1,199 MXN</span>

            <button onclick="agregar('Galaxy',1199)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🍒</div>

            <h3>Cherry Love</h3>

            <p>Aroma frutal y dulce.</p>

            <span class="precio">$799 MXN</span>

            <button onclick="agregar('Cherry Love',799)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌹</div>

            <h3>Red Passion</h3>

            <p>Fragancia intensa y romántica.</p>

            <span class="precio">$999 MXN</span>

            <button onclick="agregar('Red Passion',999)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">🌙</div>

            <h3>Night Bloom</h3>

            <p>Perfume floral para la noche.</p>

            <span class="precio">$1,099 MXN</span>

            <button onclick="agregar('Night Bloom',1099)">
                Agregar al carrito
            </button>

        </article>


        <article class="producto">

            <div class="imagen">⭐</div>

            <h3>Star Essence</h3>

            <p>Fragancia exclusiva de AURA.</p>

            <span class="precio">$1,299 MXN</span>

            <button onclick="agregar('Star Essence',1299)">
                Agregar al carrito
            </button>

        </article>


    </div>

</section>



<!-- COMPRA CON PROPOSITO -->

<section class="proposito" id="proposito">

    <h2>💗 Compra con Propósito</h2>

    <div class="proposito-contenido">

        <p>
            En AURA PERFUMES creemos que una compra puede convertirse
            en una oportunidad para ayudar. Por eso, destinaremos el
            <strong>5% del valor de cada compra</strong> a apoyar a
            niños con cáncer.
        </p>


        <div class="donacion">

            <h3>5%</h3>

            <p>
                de cada compra será destinado a nuestro programa
                de apoyo.
            </p>

        </div>


        <div class="tarjetas">

            <div class="tarjeta">

                <h3>💗 Nuestro propósito</h3>

                <p>
                    Contribuir al apoyo de niños con cáncer mediante
                    una parte de las ganancias generadas por nuestras ventas.
                </p>

            </div>


            <div class="tarjeta">

                <h3>🎗️ Nuestro compromiso</h3>

                <p>
                    Buscamos que nuestros clientes puedan disfrutar
                    de sus perfumes mientras participan en una iniciativa
                    de apoyo social.
                </p>

            </div>


            <div class="tarjeta">

                <h3>🤝 Compra con Propósito</h3>

                <p>
                    Cada compra representa una oportunidad para contribuir
                    a nuestro programa de apoyo.
                </p>

            </div>

        </div>

    </div>

</section>



<!-- NOSOTROS -->

<section class="nosotros" id="nosotros">

    <h2>Sobre AURA PERFUMES</h2>

    <p>

        AURA PERFUMES es una tienda dedicada a la venta de perfumes
        y fragancias para diferentes gustos y ocasiones. Nuestro
        objetivo es combinar la venta de productos de calidad con
        una iniciativa de responsabilidad social.

    </p>


    <div class="tarjetas">

        <div class="tarjeta">

            <h3>Misión</h3>

            <p>
                Ofrecer perfumes de calidad y brindar una experiencia
                de compra agradable, incorporando acciones que contribuyan
                al apoyo de niños con cáncer.
            </p>

        </div>


        <div class="tarjeta">

            <h3>Objetivo</h3>

            <p>
                Crear una tienda de perfumes reconocida por su variedad,
                atención al cliente y compromiso con nuestra iniciativa
                Compra con Propósito.
            </p>

        </div>


        <div class="tarjeta">

            <h3>Valores</h3>

            <p>
                Solidaridad, responsabilidad, respeto, honestidad
                y compromiso.
            </p>

        </div>

    </div>

</section>



<!-- CONTACTO -->

<section id="contacto">

    <h2>Contacto</h2>

    <form class="formulario">

        <label>
            Nombre completo
        </label>

        <input
            type="text"
            placeholder="Escribe tu nombre"
            required
        >


        <label>
            Correo electrónico
        </label>

        <input
            type="email"
            placeholder="correo@ejemplo.com"
            required
        >


        <label>
            Teléfono
        </label>

        <input
            type="tel"
            placeholder="55 1234 5678"
        >


        <label>
            Mensaje
        </label>

        <textarea
            placeholder="Escribe tu mensaje"
        ></textarea>


        <button type="submit">
            ENVIAR MENSAJE
        </button>

    </form>

</section>



<!-- CARRITO -->

<section id="carrito">

    <h2>🛒 Carrito de Compras</h2>

    <div id="listaCarrito">

        <p style="text-align:center;">
            Tu carrito está vacío.
        </p>

    </div>


    <div class="total">

        Total:
        $<span id="total">0</span> MXN

    </div>


    <div class="donacion-carrito">

        Donación del 5%:
        $<span id="donacion">0</span> MXN

    </div>


    <div style="text-align:center;">

        <a href="#contacto" class="boton">
            CONTINUAR CON LA COMPRA
        </a>

    </div>

</section>


</main>



<footer>

    <p>
        © 2026 <strong>AURA PERFUMES</strong>
    </p>

    <p>
        “Una fragancia que deja huella.”
    </p>

    <br>

    <p>
        Proyecto realizado por:
    </p>

    <p>
        <strong>ESCRIBE AQUÍ LOS NOMBRES COMPLETOS</strong>
    </p>

</footer>



<script>

    let carrito = [];

    let total = 0;


    function agregar(nombre, precio) {

        carrito.push({
            nombre: nombre,
            precio: precio
        });

        total = total + precio;

        actualizarCarrito();

    }


    function eliminar(indice) {

        total = total - carrito[indice].precio;

        carrito.splice(indice, 1);

        actualizarCarrito();

    }


    function actualizarCarrito() {

        let lista = document.getElementById("listaCarrito");

        let contador = document.getElementById("contador");

        let totalElemento = document.getElementById("total");

        let donacionElemento = document.getElementById("donacion");


        contador.textContent = carrito.length;


        totalElemento.textContent =
            total.toLocaleString("es-MX");


        let donacion = total * 0.05;


        donacionElemento.textContent =
            donacion.toLocaleString("es-MX");


        if (carrito.length === 0) {

            lista.innerHTML =
                '<p style="text-align:center;">Tu carrito está vacío.</p>';

            return;

        }


        lista.innerHTML = "";


        carrito.forEach(function(producto, indice) {

            let elemento = document.createElement("div");

            elemento.className = "item-carrito";


            elemento.innerHTML = `

                <span>
                    ${producto.nombre}
                    - $${producto.precio.toLocaleString("es-MX")}
                </span>

                <button onclick="eliminar(${indice})">
                    Eliminar
                </button>

            `;


            lista.appendChild(elemento);

        });

    }

</script>


</body>
</html>
