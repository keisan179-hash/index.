<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Patitas Felices | Veterinaria & Estética Canina en San Gil</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;600;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <!-- Estilos CSS -->
    <style>
        :root {
            --verde-esmeralda: #1a7a4a;
            --blanco: #FFFFFF;
            --naranja-calido: #FF6B2B;
            --naranja-hover: #e65a1d;
            --crema-suave: #F5F5F0;
            --gris-oscuro: #2C2C2C;
            --gris-texto: #555555;
            --sombra: 0 4px 15px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        /* Reset y General */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Nunito', sans-serif;
            color: var(--gris-oscuro);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        ul {
            list-style: none;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 700;
            text-align: center;
            transition: var(--transition);
            cursor: pointer;
            border: none;
        }

        .btn-naranja {
            background-color: var(--naranja-calido);
            color: var(--blanco);
        }

        .btn-naranja:hover {
            background-color: var(--naranja-hover);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 107, 43, 0.3);
        }

        .btn-verde {
            background-color: var(--verde-esmeralda);
            color: var(--blanco);
        }

        .btn-verde:hover {
            background-color: #145e39;
            transform: translateY(-2px);
        }

        /* --- HEADER & NAVBAR --- */
        header {
            background-color: var(--blanco);
            height: 80px;
            display: flex;
            align-items: center;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: var(--sombra);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: var(--verde-esmeralda);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            align-items: center;
        }

        .nav-links a:hover {
            color: var(--verde-esmeralda);
        }

        .menu-toggle {
            display: none;
            font-size: 1.8rem;
            cursor: pointer;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
                        url('https://images.unsplash.com/photo-1516734212186-a967f81ad0d7?q=80&w=2071&auto=format&fit=crop') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--blanco);
            padding-top: 80px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* --- SECCIONES GENERALES --- */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--verde-esmeralda);
            margin-bottom: 10px;
        }

        .section-title p {
            color: var(--gris-texto);
            font-size: 1.1rem;
        }

        /* --- SOBRE NOSOTROS --- */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-img img {
            width: 100%;
            border-radius: 20px;
            box-shadow: var(--sombra);
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--gris-texto);
        }

        .stats {
            display: flex;
            gap: 30px;
            margin-top: 30px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-item span {
            display: block;
            font-size: 2rem;
            font-weight: 700;
            color: var(--naranja-calido);
        }

        /* --- SERVICIOS --- */
        .services {
            background-color: var(--crema-suave);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--blanco);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            transition: var(--transition);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--sombra);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            display: inline-block;
        }

        .service-card h3 {
            margin-bottom: 15px;
            color: var(--verde-esmeralda);
        }

        /* --- GALERÍA --- */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }

        .gallery-item {
            height: 250px;
            overflow: hidden;
            border-radius: 15px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* --- TESTIMONIOS --- */
        .testimonials {
            background-color: var(--verde-esmeralda);
            color: var(--blanco);
        }

        .testimonials .section-title h2 {
            color: var(--blanco);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .client-info {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-top: 20px;
        }

        .client-info img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
        }

        .stars {
            color: #FFD700;
            margin-bottom: 10px;
        }

        /* --- CONTACTO --- */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info-card {
            background: var(--crema-suave);
            padding: 40px;
            border-radius: 20px;
        }

        .info-item {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }

        .info-item span:first-child {
            font-size: 1.5rem;
        }

        .map-container {
            width: 100%;
            height: 100%;
            min-height: 300px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--sombra);
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--gris-oscuro);
            color: var(--blanco);
            padding: 60px 0 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            transition: var(--transition);
            font-size: 1.2rem;
        }

        .social-icon:hover {
            background: var(--naranja-calido);
            transform: scale(1.1);
        }

        .footer-links h4 {
            margin-bottom: 20px;
            color: var(--naranja-calido);
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #aaa;
        }

        /* --- WHATSAPP FLOTANTE --- */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            box-shadow: 2px 2px 10px rgba(0,0,0,0.2);
            z-index: 999;
            transition: var(--transition);
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            background-color: #128c7e;
        }

        /* --- ANIMACIONES --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 992px) {
            .about-grid, .contact-grid {
                grid-template-columns: 1fr;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 80px;
                left: 0;
                width: 100%;
                background: var(--blanco);
                padding: 20px;
                box-shadow: var(--sombra);
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Botón de WhatsApp Flotante -->
    <a href="https://wa.me/573003435190" class="whatsapp-float" target="_blank">
        <svg width="35" height="35" fill="currentColor" viewBox="0 0 16 16">
            <path d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93a7.898 7.898 0 0 0-2.326-5.607zM7.994 14.52a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"/>
        </svg>
    </a>

    <!-- NAVBAR -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">
                    <span>🐾</span> Patitas Felices
                </a>
                <div class="menu-toggle" id="mobile-menu">☰</div>
                <ul class="nav-links">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#galeria">Galería</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                    <li><a href="https://wa.me/573003435190" target="_blank" class="btn btn-verde">Agendar Cita</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="inicio">
        <div class="hero-content container">
            <h1>Expertos en el cuidado de tu mejor amigo</h1>
            <p>5 años brindando amor, salud y belleza a las mascotas de San Gil. Porque para nosotros, son familia.</p>
            <a href="https://wa.me/573003435190" target="_blank" class="btn btn-naranja">¡Agenda tu cita por WhatsApp!</a>
        </div>
    </section>

    <!-- SOBRE NOSOTROS -->
    <section id="nosotros">
        <div class="container">
            <div class="about-grid">
                <div class="about-img reveal">
                    <img src="https://images.unsplash.com/photo-1581888227599-779811939961?q=80&w=1974&auto=format&fit=crop" alt="Valentina con mascota">
                </div>
                <div class="about-text reveal">
                    <h3>Pasión por las mascotas</h3>
                    <p>En <strong>Patitas Felices</strong>, liderado por Valentina Torres, entendemos que tu mascota es parte fundamental de tu vida. Ubicados en el corazón de Villa Olímpica, llevamos media década transformando la experiencia veterinaria en San Gil.</p>
                    <p>Nuestra filosofía se basa en tres pilares: amor incondicional, confianza absoluta y un profesionalismo que garantiza la salud integral de tu compañero.</p>
                    <div class="stats">
                        <div class="stat-item">
                            <span>5+</span>
                            <small>Años de Experiencia</small>
                        </div>
                        <div class="stat-item">
                            <span>1500+</span>
                            <small>Mascotas Felices</small>
                        </div>
                        <div class="stat-item">
                            <span>100%</span>
                            <small>Dedicación</small>
                        </div>
                    </div>
                    <br>
                    <a href="#contacto" class="btn btn-verde">Conoce nuestra ubicación</a>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICIOS -->
    <section class="services" id="servicios">
        <div class="container">
            <div class="section-title reveal">
                <h2>Nuestros Servicios</h2>
                <p>Cuidado integral para que siempre muevan la colita</p>
            </div>
            <div class="services-grid">
                <!-- Servicio 1 -->
                <div class="service-card reveal">
                    <span class="service-icon">🐾</span>
                    <h3>Peluquería Canina y Felina</h3>
                    <p>Baños relajantes, cortes de raza y tratamiento de pelaje con productos de alta calidad para que luzcan radiantes.</p>
                    <a href="https://wa.me/573003435190" target="_blank" class="btn btn-verde">Ver más</a>
                </div>
                <!-- Servicio 2 -->
                <div class="service-card reveal">
                    <span class="service-icon">✂️</span>
                    <h3>Arreglo Estético</h3>
                    <p>Corte de uñas, limpieza de oídos y arreglo de almohadillas. Detalles que marcan la diferencia en su comodidad.</p>
                    <a href="https://wa.me/573003435190" target="_blank" class="btn btn-verde">Ver más</a>
                </div>
                <!-- Servicio 3 -->
                <div class="service-card reveal">
                    <span class="service-icon">🩺</span>
                    <h3>Consulta Veterinaria</h3>
                    <p>Atención médica profesional, diagnósticos precisos y seguimiento preventivo para una vida larga y saludable.</p>
                    <a href="https://wa.me/573003435190" target="_blank" class="btn btn-verde">Ver más</a>
                </div>
            </div>
        </div>
    </section>

    <!-- GALERÍA -->
    <section id="galeria">
        <div class="container">
            <div class="section-title reveal">
                <h2>Clientes Felices</h2>
                <p>Momentos capturados en nuestra veterinaria</p>
            </div>
            <div class="gallery-grid reveal">
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1516734212186-a967f81ad0d7?q=80&w=500&auto=format&fit=crop" alt="Perro feliz"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1514888286974-6c03e2ca1dba?q=80&w=500&auto=format&fit=crop" alt="Gato curioso"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1537151608828-ea2b11777ee8?q=80&w=500&auto=format&fit=crop" alt="Golden retriever"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1583511655857-d19b40a7a54e?q=80&w=500&auto=format&fit=crop" alt="Perro en baño"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1592194996308-7b43878e84a6?q=80&w=500&auto=format&fit=crop" alt="Gato en consulta"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1544191341-a675f9227f2f?q=80&w=500&auto=format&fit=crop" alt="Peluquería canina"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1548191265-cc70d3d45ba1?q=80&w=500&auto=format&fit=crop" alt="Perros jugando"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1527362950785-f487a7c1fe48?q=80&w=500&auto=format&fit=crop" alt="Mascota pequeña"></div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIOS -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title reveal">
                <h2>Lo que dicen nuestros clientes</h2>
                <p>Nuestra mayor recompensa es su satisfacción</p>
            </div>
            <div class="testimonials-grid">
                <!-- Testimonio 1 -->
                <div class="testimonial-card reveal">
                    <div class="stars">★★★★★</div>
                    <p>"Llevo a mi perrita Luna desde que abrieron. El trato de Valentina es excepcional, siempre sale hermosa y muy tranquila. ¡Súper recomendados!"</p>
                    <div class="client-info">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Cliente">
                        <div>
                            <strong>María Fernanda R.</strong>
                            <small>San Gil</small>
                        </div>
                    </div>
                </div>
                <!-- Testimonio 2 -->
                <div class="testimonial-card reveal">
                    <div class="stars">★★★★★</div>
                    <p>"Excelente servicio veterinario. Mi gato tenía un problema de piel y en Patitas Felices le dieron el tratamiento perfecto. Son muy profesionales."</p>
                    <div class="client-info">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Cliente">
                        <div>
                            <strong>Juan Carlos D.</strong>
                            <small>Barrio Villa Olímpica</small>
                        </div>
                    </div>
                </div>
                <!-- Testimonio 3 -->
                <div class="testimonial-card reveal">
                    <div class="stars">★★★★★</div>
                    <p>"La mejor peluquería de San Gil. El corte de mi Poodle quedó impecable. Se nota que aman a los animales por cómo los cuidan."</p>
                    <div class="client-info">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Cliente">
                        <div>
                            <strong>Sofía Moreno</strong>
                            <small>San Gil</small>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACTO Y UBICACIÓN -->
    <section id="contacto">
        <div class="container">
            <div class="section-title reveal">
                <h2>Contáctanos</h2>
                <p>Estamos listos para recibir a tu mascota</p>
            </div>
            <div class="contact-grid">
                <div class="contact-info-card reveal">
                    <h3>¡Agenda hoy mismo!</h3>
                    <p style="margin-bottom: 30px;">Tu mascota merece lo mejor — ¡contáctanos y reserva su espacio!</p>
                    
                    <div class="info-item">
                        <span>📞</span>
                        <div>
                            <strong>WhatsApp</strong>
                            <p><a href="https://wa.me/573003435190">300 343 5190</a></p>
                        </div>
                    </div>
                    <div class="info-item">
                        <span>⏰</span>
                        <div>
                            <strong>Horario de Atención</strong>
                            <p>Lunes a Sábado: 8:00 a.m. – 6:00 p.m.</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <span>📍</span>
                        <div>
                            <strong>Ubicación</strong>
                            <p>Barrio Villa Olímpica, San Gil, Santander</p>
                        </div>
                    </div>
                    <a href="https://wa.me/573003435190" target="_blank" class="btn btn-naranja" style="width: 100%;">Escríbenos por WhatsApp</a>
                </div>
                <div class="map-container reveal">
                    <!-- Mapa de Google Maps (San Gil, Villa Olímpica) -->
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15878.506547630712!2d-73.1368943!3d6.5516909!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e69c6934c767f47%3A0xc48c037f5d475c87!2sSan%20Gil%2C%20Santander!5e0!3m2!1ses!2sco!4v1714578000000!5m2!1ses!2sco" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-links">
                    <div class="footer-logo">🐾 Patitas Felices</div>
                    <p>Cuidando las mascotas de San Gil con amor y dedicación desde hace 5 años.</p>
                    <div class="social-links">
                        <a href="#" class="social-icon">f</a>
                        <a href="#" class="social-icon">i</a>
                        <a href="https://wa.me/573003435190" class="social-icon">w</a>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Links Rápidos</h4>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#galeria">Galería</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Servicios</h4>
                    <ul>
                        <li>Peluquería Canina</li>
                        <li>Estética Felina</li>
                        <li>Consulta Médica</li>
                        <li>Corte de Uñas</li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Legal</h4>
                    <ul>
                        <li>Privacidad</li>
                        <li>Términos y condiciones</li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Patitas Felices Veterinaria & Estética Canina. San Gil, Santander. Atendido por Valentina Torres.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript para Animaciones y Navegación -->
    <script>
        // Navegación Responsive
        const menuToggle = document.getElementById('mobile-menu');
        const navLinks = document.querySelector('.nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Cerrar menú al hacer click en un link (en móvil)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // Animación Reveal al hacer Scroll
        function reveal() {
            var reveals = document.querySelectorAll(".reveal");
            for (var i = 0; i < reveals.length; i++) {
                var windowHeight = window.innerHeight;
                var elementTop = reveals[i].getBoundingClientRect().top;
                var elementVisible = 150;
                if (elementTop < windowHeight - elementVisible) {
                    reveals[i].classList.add("active");
                }
            }
        }

        window.addEventListener("scroll", reveal);
        // Llamar una vez al cargar por si hay elementos visibles
        window.onload = reveal;

        // Header pegajoso efecto
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.padding = "5px 0";
            } else {
                header.style.padding = "0";
            }
        });
    </script>
</body>
</html>
