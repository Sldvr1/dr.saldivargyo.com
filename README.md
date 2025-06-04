<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dra. Laura Méndez - Ginecología y Obstetricia</title>
    <style>
        /* Estilos CSS */
        :root {
            --color-primario: #8e44ad;
            --color-secundario: #9b59b6;
            --color-blanco: #ffffff;
            --color-gris-claro: #f8f9fa;
            --color-texto: #333333;
            --color-texto-claro: #666666;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', Arial, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--color-texto);
            background-color: var(--color-blanco);
        }
        
        header {
            background: linear-gradient(135deg, var(--color-primario), var(--color-secundario));
            color: var(--color-blanco);
            padding: 30px 0;
            text-align: center;
            position: relative;
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }
        
        .logo img {
            height: 80px;
            margin-right: 15px;
        }
        
        .logo-text h1 {
            font-size: 2.2rem;
            margin-bottom: 5px;
        }
        
        .logo-text p {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        nav {
            background-color: var(--color-blanco);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--color-texto);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--color-primario);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--color-primario);
            cursor: pointer;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1579684385127-1ef15d508118?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(142, 68, 173, 0.7);
        }
        
        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 1;
            color: var(--color-blanco);
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            max-width: 600px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--color-blanco);
            color: var(--color-primario);
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            border: 2px solid var(--color-blanco);
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--color-blanco);
        }
        
        .btn-primary {
            background-color: var(--color-primario);
            color: var(--color-blanco);
            border-color: var(--color-primario);
        }
        
        .btn-primary:hover {
            background-color: transparent;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 20px;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--color-primario);
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--color-texto-claro);
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--color-blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .service-img {
            height: 200px;
            overflow: hidden;
        }
        
        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .service-card:hover .service-img img {
            transform: scale(1.1);
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--color-primario);
        }
        
        .service-content p {
            color: var(--color-texto-claro);
            margin-bottom: 20px;
        }
        
        .about-container {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-content {
            flex: 1;
        }
        
        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--color-primario);
        }
        
        .about-content p {
            margin-bottom: 15px;
            color: var(--color-texto-claro);
        }
        
        .specialties {
            margin-top: 30px;
        }
        
        .specialties h4 {
            margin-bottom: 15px;
            color: var(--color-primario);
        }
        
        .specialties ul {
            list-style-position: inside;
            columns: 2;
        }
        
        .specialties li {
            margin-bottom: 10px;
            color: var(--color-texto-claro);
        }
        
        .contact-info {
            background-color: var(--color-gris-claro);
            padding: 80px 0;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .contact-card {
            background-color: var(--color-blanco);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
        }
        
        .contact-icon {
            font-size: 2.5rem;
            color: var(--color-primario);
            margin-bottom: 20px;
        }
        
        .contact-card h3 {
            margin-bottom: 15px;
            color: var(--color-primario);
        }
        
        .contact-card p, .contact-card a {
            color: var(--color-texto-claro);
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
        }
        
        .contact-card a:hover {
            color: var(--color-primario);
        }
        
        .appointment-form {
            background-color: var(--color-blanco);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--color-texto);
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--color-primario);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        footer {
            background-color: #222;
            color: var(--color-blanco);
            padding: 50px 0 20px;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .footer-col h3 {
            color: var(--color-blanco);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        
        .footer-col p, .footer-col a {
            color: #aaa;
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-col a:hover {
            color: var(--color-blanco);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--color-primario);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive design */
        @media (max-width: 992px) {
            .about-container {
                flex-direction: column;
            }
            
            .specialties ul {
                columns: 1;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
        
        @media (max-width: 576px) {
            .logo {
                flex-direction: column;
                text-align: center;
            }
            
            .logo img {
                margin-right: 0;
                margin-bottom: 10px;
            }
            
            .btn {
                padding: 10px 20px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo">
                <img src="https://via.placeholder.com/80x80?text=Logo" alt="Logo Dra. Laura Méndez">
                <div class="logo-text">
                    <h1>Dra. Laura Méndez</h1>
                    <p>Ginecología y Obstetricia</p>
                </div>
            </div>
        </div>
    </header>
    
    <nav>
        <div class="nav-container">
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li><a href="#citas">Citas en Línea</a></li>
            </ul>
        </div>
    </nav>
    
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h2>Cuidado integral para la salud femenina</h2>
            <p>Ofrecemos atención personalizada y compasiva en todas las etapas de la vida de la mujer, desde la adolescencia hasta la menopausia.</p>
            <a href="#citas" class="btn btn-primary">Solicitar Cita</a>
        </div>
    </section>
    
    <section class="container" id="servicios">
        <div class="section-title">
            <h2>Nuestros Servicios</h2>
            <p>Ofrecemos una amplia gama de servicios ginecológicos y obstétricos para satisfacer todas las necesidades de salud de la mujer.</p>
        </div>
        
        <div class="services-grid">
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1579684453423-f84349ef60b0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Control Prenatal">
                </div>
                <div class="service-content">
                    <h3>Control Prenatal</h3>
                    <p>Acompañamiento profesional durante todo el embarazo para garantizar la salud de la madre y el bebé.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1576091160550-2173dba999ef?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ecografías">
                </div>
                <div class="service-content">
                    <h3>Ecografías</h3>
                    <p>Tecnología de imagen avanzada para el diagnóstico y seguimiento del embarazo y condiciones ginecológicas.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1505751172876-fa1923c5c528?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Planificación Familiar">
                </div>
                <div class="service-content">
                    <h3>Planificación Familiar</h3>
                    <p>Orientación y métodos anticonceptivos adaptados a tus necesidades y estilo de vida.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Menopausia">
                </div>
                <div class="service-content">
                    <h3>Manejo de la Menopausia</h3>
                    <p>Tratamientos y consejos para una transición saludable y cómoda durante esta etapa.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1581056771107-24ca5f033842?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Cirugía Ginecológica">
                </div>
                <div class="service-content">
                    <h3>Cirugía Ginecológica</h3>
                    <p>Procedimientos mínimamente invasivos para diversas condiciones ginecológicas.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-img">
                    <img src="https://images.unsplash.com/photo-1579684385127-1ef15d508118?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Salud Sexual">
                </div>
                <div class="service-content">
                    <h3>Salud Sexual</h3>
                    <p>Evaluación, diagnóstico y tratamiento de condiciones relacionadas con la salud sexual femenina.</p>
                    <a href="#citas" class="btn">Más información</a>
                </div>
            </div>
        </div>
    </section>
    
    <section class="container" id="sobre-mi">
        <div class="section-title">
            <h2>Sobre Mí</h2>
            <p>Conoce a tu especialista en ginecología y obstetricia</p>
        </div>
        
        <div class="about-container">
            <div class="about-img">
                <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Dra. Laura Méndez">
            </div>
            <div class="about-content">
                <h3>Dra. Laura Méndez</h3>
                <p>Médico especialista en Ginecología y Obstetricia con más de 15 años de experiencia en el cuidado de la salud femenina. Me gradué de la Universidad Nacional Autónoma de México y realicé mi especialidad en el Hospital ABC.</p>
                <p>Mi enfoque es brindar atención médica de alta calidad con calidez humana, respetando siempre la individualidad y necesidades de cada paciente. Creo en la medicina preventiva y en empoderar a mis pacientes con conocimiento sobre su salud.</p>
                
                <div class="specialties">
                    <h4>Especialidades:</h4>
                    <ul>
                        <li>Ginecología general</li>
                        <li>Obstetricia y control prenatal</li>
                        <li>Ecografía ginecológica y obstétrica</li>
                        <li>Cirugía ginecológica mínimamente invasiva</li>
                        <li>Endocrinología ginecológica</li>
                        <li>Climaterio y menopausia</li>
                        <li>Planificación familiar</li>
                        <li>Salud sexual femenina</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact-info" id="contacto">
        <div class="container">
            <div class="section-title">
                <h2>Contacto</h2>
                <p>Estamos aquí para responder tus preguntas y brindarte la atención que necesitas</p>
            </div>
            
            <div class="contact-container">
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <h3>Dirección</h3>
                    <p>Calle Flores #123, Colonia Jardines</p>
                    <p>Ciudad de México, CDMX 03810</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <h3>Teléfonos</h3>
                    <p><a href="tel:+525555555555">55-5555-5555</a></p>
                    <p><a href="tel:+525555555556">55-5555-5556</a></p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <h3>Correo Electrónico</h3>
                    <p><a href="mailto:contacto@dralauramendez.com">contacto@dralauramendez.com</a></p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>Horario de Atención</h3>
                    <p>Lunes a Viernes: 9:00 - 18:00 hrs</p>
                    <p>Sábados: 9:00 - 13:00 hrs</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="container" id="citas">
        <div class="section-title">
            <h2>Solicita una Cita</h2>
            <p>Completa el siguiente formulario y nos pondremos en contacto contigo para confirmar tu cita</p>
        </div>
        
        <div class="appointment-form">
            <form id="citaForm">
                <div class="form-group">
                    <label for="nombre">Nombre completo</label>
                    <input type="text" id="nombre" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Correo electrónico</label>
                    <input type="email" id="email" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="telefono">Teléfono</label>
                    <input type="tel" id="telefono" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="servicio">Servicio de interés</label>
                    <select id="servicio" class="form-control" required>
                        <option value="">Selecciona un servicio</option>
                        <option value="control-prenatal">Control prenatal</option>
                        <option value="ecografia">Ecografía</option>
                        <option value="planificacion-familiar">Planificación familiar</option>
                        <option value="menopausia">Manejo de menopausia</option>
                        <option value="cirugia">Cirugía ginecológica</option>
                        <option value="salud-sexual">Salud sexual</option>
                        <option value="consulta-general">Consulta general</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="fecha">Fecha preferida</label>
                    <input type="date" id="fecha" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="mensaje">Mensaje adicional</label>
                    <textarea id="mensaje" class="form-control"></textarea>
                </div>
                
                <button type="submit" class="btn btn-primary">Solicitar Cita</button>
            </form>
        </div>
    </section>
    
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h3>Dra. Laura Méndez</h3>
                <p>Especialista en Ginecología y Obstetricia comprometida con la salud y bienestar integral de la mujer.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
            
            <div class="footer-col">
                <h3>Enlaces Rápidos</h3>
                <a href="#inicio">Inicio</a>
                <a href="#servicios">Servicios</a>
                <a href="#sobre-mi">Sobre Mí</a>
                <a href="#contacto">Contacto</a>
                <a href="#citas">Citas en Línea</a>
            </div>
            
            <div class="footer-col">
                <h3>Servicios</h3>
                <a href="#">Control Prenatal</a>
                <a href="#">Ecografías</a>
                <a href="#">Planificación Familiar</a>
                <a href="#">Manejo de Menopausia</a>
                <a href="#">Cirugía Ginecológica</a>
            </div>
            
            <div class="footer-col">
                <h3>Contacto</h3>
                <p><i class="fas fa-map-marker-alt"></i> Calle Flores #123, CDMX</p>
                <p><i class="fas fa-phone-alt"></i> 55-5555-5555</p>
                <p><i class="fas fa-envelope"></i> contacto@dralauramendez.com</p>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 Dra. Laura Méndez - Ginecología y Obstetricia. Todos los derechos reservados.</p>
        </div>
    </footer>
    
    <script>
        // JavaScript para el formulario de citas
        document.getElementById('citaForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Obtener valores del formulario
            const nombre = document.getElementById('nombre').value;
            const servicio = document.getElementById('servicio').value;
            
            // Mostrar mensaje de confirmación
            alert(`Gracias ${nombre}, hemos recibido tu solicitud de cita para ${servicio}. Nos pondremos en contacto contigo para confirmar.`);
            
            // Resetear formulario
            this.reset();
        });
        
        // Menú móvil
        const menuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        menuBtn.addEventListener('click', function() {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Cerrar menú al hacer clic en un enlace
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', function() {
                if (window.innerWidth <= 768) {
                    navLinks.style.display = 'none';
                }
            });
        });
        
        // Actualizar año del copyright
        document.querySelector('.copyright p').innerHTML = `&copy; ${new Date().getFullYear()} Dra. Laura Méndez - Ginecología y Obstetricia. Todos los derechos reservados.`;
    </script>
</body>
</html>