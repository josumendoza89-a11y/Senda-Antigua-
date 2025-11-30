<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Palabras de Vida | Volviendo a la Senda Antigua</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Fuentes: Merriweather (Solemne) y Inter (Legible) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400&display=swap" rel="stylesheet">
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fdfbf7; /* Color papiro suave */
            color: #1a202c;
        }
        h1, h2, h3, h4, .serif-font {
            font-family: 'Merriweather', serif;
        }
        .bible-verse {
            border-left: 4px solid #b45309; /* Amber-700 */
            padding-left: 1rem;
            font-style: italic;
            color: #431407;
            background-color: #fffbeb;
            padding: 1rem;
            border-radius: 0 0.5rem 0.5rem 0;
            margin: 1.5rem 0;
        }
        .hero-bg {
            background-image: linear-gradient(rgba(20, 20, 25, 0.85), rgba(20, 20, 25, 0.9)), url('https://images.unsplash.com/photo-1504052434569-70ad5836ab65?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        /* Scroll suave y ocultar barra en modales */
        .smooth-scroll { scroll-behavior: smooth; }
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        .hide-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>
<body class="smooth-scroll flex flex-col min-h-screen">

    <!-- Navegación -->
    <nav class="bg-white shadow-sm fixed w-full z-40 border-b border-amber-100" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-24 items-center">
                <div class="flex items-center cursor-pointer group" onclick="window.scrollTo(0,0)">
                    <div class="bg-amber-900 text-amber-50 p-2 rounded mr-3 group-hover:bg-amber-800 transition">
                        <i data-lucide="book-open" class="h-6 w-6"></i>
                    </div>
                    <div class="flex flex-col">
                        <span class="font-bold text-lg md:text-xl tracking-tight text-slate-900 serif-font leading-tight">Palabras de Vida</span>
                        <span class="text-xs md:text-sm text-slate-600 italic">Volviendo a la Senda Antigua</span>
                        <span class="text-[10px] text-amber-700 uppercase tracking-wider mt-1 font-bold">Pr. Julio César Mendoza</span>
                    </div>
                </div>
                
                <!-- Menú Desktop -->
                <div class="hidden lg:flex items-center space-x-8">
                    <a href="#inicio" class="text-slate-600 hover:text-amber-800 font-medium transition text-sm uppercase tracking-wide">Inicio</a>
                    <a href="#biblia" class="text-slate-600 hover:text-amber-800 font-medium transition text-sm uppercase tracking-wide">Lectura</a>
                    <a href="#contenido" class="text-slate-600 hover:text-amber-800 font-medium transition text-sm uppercase tracking-wide">Biblioteca</a>
                    <a href="#cursos" class="text-slate-600 hover:text-amber-800 font-medium transition text-sm uppercase tracking-wide">Cursos</a>
                    
                    <!-- Botón WhatsApp Donación -->
                    <button onclick="contactDonation()" class="bg-green-600 hover:bg-green-700 text-white px-5 py-2 rounded-full font-bold transition flex items-center shadow-sm hover:shadow-md transform hover:-translate-y-0.5">
                        <i data-lucide="message-circle" class="w-4 h-4 mr-2"></i> Ofrendar
                    </button>
                </div>

                <!-- Botón Menú Móvil -->
                <div class="flex items-center lg:hidden">
                    <button id="mobile-menu-btn" class="text-slate-600 hover:text-slate-900 focus:outline-none p-2">
                        <i data-lucide="menu" class="h-8 w-8"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Menú Móvil -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white border-t border-slate-100 shadow-lg absolute w-full">
            <div class="px-4 pt-2 pb-4 space-y-2">
                <a href="#inicio" class="block py-3 text-base font-medium text-slate-700 border-b border-slate-50">Inicio</a>
                <a href="#biblia" class="block py-3 text-base font-medium text-slate-700 border-b border-slate-50">Lectura Diaria</a>
                <a href="#contenido" class="block py-3 text-base font-medium text-slate-700 border-b border-slate-50">Biblioteca (Devocionales)</a>
                <a href="#cursos" class="block py-3 text-base font-medium text-slate-700 border-b border-slate-50">Cursos Bíblicos</a>
                <button onclick="contactDonation()" class="w-full mt-4 bg-green-600 text-white py-3 rounded-lg font-bold flex justify-center items-center">
                    <i data-lucide="message-circle" class="w-5 h-5 mr-2"></i> Contactar para Ofrendar
                </button>
            </div>
        </div>
    </nav>

    <!-- Sección Hero -->
    <section id="inicio" class="hero-bg min-h-screen flex items-center justify-center text-center px-4 relative pt-20">
        <div class="max-w-4xl mx-auto text-white z-10">
            <div class="mb-6 animate-fade-in-up">
                <i data-lucide="anchor" class="w-12 h-12 mx-auto text-amber-500 mb-4 opacity-80"></i>
                <span class="uppercase tracking-[0.3em] text-xs font-bold text-amber-200">Ministerio del Pr. Julio César Mendoza</span>
            </div>
            <h1 class="text-4xl md:text-6xl font-bold mb-6 drop-shadow-xl leading-tight serif-font">Volviendo a la<br/><span class="text-amber-500">Senda Antigua</span></h1>
            <div class="max-w-2xl mx-auto bg-black/30 p-6 rounded-lg backdrop-blur-sm border-l-4 border-amber-500">
                <p class="text-xl md:text-2xl font-serif italic text-slate-100">"Así dijo Jehová: Paraos en los caminos, y mirad, y preguntad por las sendas antiguas, cuál sea el buen camino, y andad por él, y hallaréis descanso para vuestra alma."</p>
                <p class="text-right text-sm mt-2 text-amber-400 font-bold">— Jeremías 6:16</p>
            </div>
            <div class="mt-10 flex flex-col sm:flex-row justify-center gap-4">
                <a href="#contenido" class="bg-amber-700 hover:bg-amber-600 text-white px-8 py-3 rounded text-lg transition shadow-lg font-serif">
                    Explorar la Palabra
                </a>
            </div>
        </div>
    </section>

    <!-- Sección Lectura Bíblica -->
    <section id="biblia" class="py-20 bg-amber-50/50">
        <div class="max-w-5xl mx-auto px-4">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-slate-900 serif-font">Lectura de las Escrituras</h2>
                <p class="text-slate-600 mt-2">La base de nuestra fe es la Biblia, no la opinión humana.</p>
            </div>
            
            <div class="bg-white rounded-xl shadow-xl border border-amber-100 overflow-hidden">
                <div class="bg-slate-900 text-amber-50 p-4 flex justify-between items-center">
                    <div class="flex items-center gap-2">
                        <i data-lucide="sun" class="w-5 h-5 text-amber-400"></i>
                        <span class="font-bold tracking-wide" id="current-date">Fecha</span>
                    </div>
                    <select id="bible-selector" class="bg-slate-800 border-none text-sm rounded px-3 py-1 focus:ring-1 focus:ring-amber-500">
                        <option value="salmos">Salmos 19:7-11</option>
                        <option value="timoteo">2 Timoteo 3:14-17</option>
                        <option value="hebreos">Hebreos 4:12-13</option>
                    </select>
                </div>
                <div class="p-8 md:p-12">
                    <h3 class="text-2xl font-bold text-amber-900 mb-6 serif-font text-center" id="bible-title">La Ley de Jehová es Perfecta</h3>
                    <div class="prose prose-lg max-w-none font-serif text-slate-700 leading-relaxed" id="bible-text">
                        <!-- Texto inyectado -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Biblioteca de Contenido (Escalable a 1000 archivos) -->
    <section id="contenido" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-end mb-8 border-b border-slate-200 pb-4">
                <div>
                    <span class="text-amber-700 font-bold uppercase tracking-wider text-xs">Biblioteca Digital</span>
                    <h2 class="text-3xl font-bold text-slate-900 serif-font mt-1">Devocionales y Enseñanzas</h2>
                </div>
                
                <!-- Buscador -->
                <div class="mt-4 md:mt-0 w-full md:w-auto relative">
                    <input type="text" id="search-input" placeholder="Buscar por tema o versículo..." class="w-full md:w-64 pl-10 pr-4 py-2 border border-slate-300 rounded-full text-sm focus:outline-none focus:border-amber-600 focus:ring-1 focus:ring-amber-600">
                    <i data-lucide="search" class="w-4 h-4 text-slate-400 absolute left-3 top-3"></i>
                </div>
            </div>

            <!-- Grid de Contenido -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="content-grid">
                <!-- Los artículos se generan dinámicamente con JS -->
            </div>

            <div class="mt-12 text-center">
                <button id="load-more-btn" class="text-slate-500 hover:text-amber-700 font-medium text-sm flex items-center justify-center mx-auto border border-slate-300 rounded-full px-6 py-2 transition hover:bg-amber-50">
                    Cargar más contenido antiguo <i data-lucide="refresh-cw" class="w-4 h-4 ml-2"></i>
                </button>
                <p class="text-xs text-slate-400 mt-2">Mostrando contenido de la base de datos del ministerio.</p>
            </div>
        </div>
    </section>

    <!-- Sección Cursos -->
    <section id="cursos" class="py-20 bg-slate-50 border-t border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-slate-900 serif-font">Cursos de Formación Bíblica</h2>
                <p class="text-slate-600 mt-2 max-w-2xl mx-auto">Profundiza en la teología sistemática y la historia. "Mi pueblo fue destruido, porque le faltó conocimiento" (Oseas 4:6).</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Curso 1 -->
                <div class="bg-white p-6 rounded shadow hover:shadow-lg transition border-t-4 border-amber-600">
                    <h3 class="font-bold text-lg text-slate-900 mb-2">Teología Sistemática I</h3>
                    <p class="text-sm text-slate-600 mb-4">Un estudio de la doctrina de Dios, las Escrituras y el Hombre basado en la Teología Reformada.</p>
                    <button onclick="registerCourse('Teología Sistemática')" class="text-amber-700 font-bold text-sm hover:underline">Solicitar Inscripción &rarr;</button>
                </div>
                <!-- Curso 2 -->
                <div class="bg-white p-6 rounded shadow hover:shadow-lg transition border-t-4 border-slate-700">
                    <h3 class="font-bold text-lg text-slate-900 mb-2">Historia de la Iglesia</h3>
                    <p class="text-sm text-slate-600 mb-4">Desde Pentecostés hasta la Reforma. Conoce a los mártires y padres de la fe.</p>
                    <button onclick="registerCourse('Historia de la Iglesia')" class="text-amber-700 font-bold text-sm hover:underline">Solicitar Inscripción &rarr;</button>
                </div>
                <!-- Curso 3 -->
                <div class="bg-white p-6 rounded shadow hover:shadow-lg transition border-t-4 border-slate-700">
                    <h3 class="font-bold text-lg text-slate-900 mb-2">Exégesis Bíblica</h3>
                    <p class="text-sm text-slate-600 mb-4">Aprende a interpretar la Biblia correctamente respetando su contexto histórico y gramatical.</p>
                    <button onclick="registerCourse('Exégesis')" class="text-amber-700 font-bold text-sm hover:underline">Solicitar Inscripción &rarr;</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-900 text-slate-400 py-12">
        <div class="max-w-7xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
            <div class="mb-6 md:mb-0 text-center md:text-left">
                <span class="text-slate-100 font-bold serif-font text-lg">Palabras de Vida</span>
                <p class="text-sm mt-2">Pr. Julio César Mendoza</p>
                <p class="text-xs mt-1">"La hierba se seca, y la flor se marchita,<br>mas la palabra del Dios nuestro permanece para siempre." (Isaías 40:8)</p>
            </div>
            <div class="flex flex-col items-center md:items-end">
                <button onclick="contactDonation()" class="flex items-center text-green-400 hover:text-green-300 transition mb-2">
                    <i data-lucide="heart" class="w-4 h-4 mr-2"></i> Apoyar el Ministerio
                </button>
                <p class="text-xs text-slate-600">Diseñado para la gloria de Dios.</p>
            </div>
        </div>
    </footer>

    <!-- MODAL DE LECTURA -->
    <div id="reading-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center bg-slate-900/90 p-4 opacity-0 transition-opacity duration-300">
        <div class="bg-white rounded-lg shadow-2xl w-full max-w-3xl max-h-[90vh] overflow-y-auto transform scale-95 transition-transform duration-300" id="reading-modal-panel">
            <div class="sticky top-0 bg-white/95 backdrop-blur border-b border-amber-100 px-6 py-4 flex justify-between items-center z-10">
                <span class="text-xs font-bold text-amber-600 uppercase" id="modal-tag">DOCTRINA</span>
                <button onclick="closeModal()" class="text-slate-400 hover:text-slate-800"><i data-lucide="x" class="w-6 h-6"></i></button>
            </div>
            <div class="p-8 md:p-12">
                <h2 class="text-3xl font-bold text-slate-900 serif-font mb-4" id="modal-title">Título</h2>
                <div class="flex items-center text-slate-500 text-xs mb-8 space-x-4">
                    <span class="flex items-center"><i data-lucide="book" class="w-3 h-3 mr-1"></i> Pr. Julio C. Mendoza</span>
                    <span id="modal-verse-ref" class="bg-slate-100 px-2 py-1 rounded text-slate-600 font-mono">Ref. Bíblica</span>
                </div>
                <div class="prose prose-lg prose-slate max-w-none font-serif text-slate-800 leading-relaxed" id="modal-body">
                    <!-- Contenido -->
                </div>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT: LÓGICA Y BASE DE DATOS -->
    <script>
        // 1. CONFIGURACIÓN DE DONACIONES (WHATSAPP)
        function contactDonation() {
            // Número proporcionado por el usuario
            const phoneNumber = "59176949692"; 
            const message = "Hola hermano, bendiciones. Visité la página web Palabras de Vida y deseo realizar una ofrenda voluntaria al ministerio. ¿Podría indicarme los métodos disponibles?";
            
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        function registerCourse(courseName) {
            const phoneNumber = "59176949692"; 
            const message = `Hola, me interesa inscribirme al curso: ${courseName}. Quedo atento a la información.`;
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        // 2. BASE DE DATOS DE CONTENIDO (ARQUITECTURA PARA 1000 ARCHIVOS)
        /* INSTRUCCIONES PARA AGREGAR MÁS CONTENIDO:
           Copia un bloque dentro de 'articles', pégalo al final y cambia los datos.
           Usa etiquetas HTML como <p> para párrafos y <blockquote> para citas.
        */
        const articles = [
            {
                id: 1,
                title: "La Autoridad Final de las Escrituras",
                tag: "Sola Scriptura",
                verse: "2 Timoteo 3:16",
                preview: "En tiempos de relativismo, debemos volver a la única fuente de verdad inerrante.",
                content: `
                    <p>La doctrina de la autoridad bíblica no es un tema secundario; es el cimiento sobre el cual se construye toda la fe cristiana. Como dijo Agustín de Hipona: <em>"Lo que la Escritura dice, Dios lo dice"</em>.</p>
                    <div class="bible-verse">"Toda la Escritura es inspirada por Dios, y útil para enseñar, para redargüir, para corregir, para instruir en justicia." (2 Timoteo 3:16)</div>
                    <p>Hoy en día, la "senda antigua" está cubierta de maleza porque hemos permitido que la cultura interprete la Biblia, en lugar de que la Biblia interprete la cultura. El Pr. Julio César nos llama a someter nuestra razón, nuestras emociones y nuestras tradiciones al escrutinio de la Palabra de Dios.</p>
                    <p>Referencia recomendada: <em>La Inspiración y Autoridad de la Biblia</em> de B.B. Warfield.</p>
                `
            },
            {
                id: 2,
                title: "El Temor de Dios: El Tesoro Perdido",
                tag: "Santidad",
                verse: "Proverbios 1:7",
                preview: "Hemos domesticado a Dios en nuestros púlpitos, olvidando que Él es fuego consumidor.",
                content: `
                    <p>A.W. Tozer escribió acertadamente en <em>El Conocimiento del Santo</em>: "La iglesia ha entregado su concepto de Dios y lo ha sustituido por uno tan bajo, tan innoble, que no es digno de hombres pensantes".</p>
                    <p>Volver a la senda antigua implica recuperar el asombro reverente ante la Majestad Divina. No nos acercamos a Dios como a un "amigo casual", sino como al Soberano del Universo que, en su misericordia, nos ha adoptado.</p>
                    <div class="bible-verse">"El principio de la sabiduría es el temor de Jehová; Los insensatos desprecian la sabiduría y la enseñanza." (Proverbios 1:7)</div>
                    <p>Sin un entendimiento correcto de la santidad de Dios, nuestra comprensión del pecado será superficial y, por ende, nuestra apreciación de la gracia será insignificante.</p>
                `
            },
            {
                id: 3,
                title: "La Cruz Céntrica",
                tag: "Evangelio",
                verse: "1 Corintios 2:2",
                preview: "No hay cristianismo sin cruz. La predicación moderna a menudo evita el sufrimiento.",
                content: `
                    <p>El apóstol Pablo fue claro: <em>"Pues me propuse no saber entre vosotros cosa alguna sino a Jesucristo, y a éste crucificado"</em>.</p>
                    <p>La senda antigua es una s
