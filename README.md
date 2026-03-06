<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>River North | Chicago's Creative Heart</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        :root { --chicago-blue: #007ac1; --river-gray: #f0f2f5; --dark-accent: #2d3748; }
        /* Navigation */
        nav { background: white; box-shadow: 0 2px 5px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 100; }
        .nav-container { max-width: 1200px; margin: 0 auto; padding: 1rem 2rem; display: flex; justify-content: space-between; align-items: center; }
        .logo { font-size: 1.5rem; font-weight: 700; color: var(--chicago-blue); }
        .nav-links a { margin-left: 1.5rem; text-decoration: none; color: dark-accent; transition: color 0.3s; }
        .nav-links a:hover { color: var(--chicago-blue); }
        .menu-toggle { display: none; font-size: 1.5rem; cursor: pointer; }
        /* Hero Carousel */
        .hero-carousel { position: relative; height: 80vh; overflow: hidden; }
        .carousel-slide { position: absolute; top: 0; left: 0; width: 100%; height: 100%; opacity: 0; transition: opacity 0.8s ease; }
        .carousel-slide.active { opacity: 1; }
        .carousel-slide img { width: 100%; height: 100%; object-fit: cover; }
        .slide-caption { position: absolute; bottom: 20%; left: 10%; color: white; text-shadow: 0 2px 4px rgba(0,0,0,0.8); }
        .slide-caption h1 { font-size: 3rem; margin-bottom: 1rem; }
        .slide-caption p { font-size: 1.2rem; margin-bottom: 1.5rem; }
        .btn { padding: 0.8rem 2rem; background: var(--chicago-blue); color: white; border: none; border-radius: 4px; text-decoration: none; font-weight: 600; transition: background 0.3s; }
        .btn:hover { background: #005f99; }
        /* Highlights Section */
        .highlights { max-width: 1200px; margin: 4rem auto; padding: 0 2rem; }
        .section-title { text-align: center; font-size: 2.2rem; color: var(--dark-accent); margin-bottom: 3rem; }
        .cards-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 2rem; }
        .card { background: white; border-radius: 8px; box-shadow: 0 3px 6px rgba(0,0,0,0.1); overflow: hidden; transition: transform 0.3s; }
        .card:hover { transform: translateY(-5px); }
        .card img { width: 100%; height: 200px; object-fit: cover; }
        .card-content { padding: 1.5rem; }
        .card-content h3 { color: var(--chicago-blue); margin-bottom: 0.8rem; }
        .card-content p { color: #6b7280; font-size: 0.95rem; }
       /* Events Snippet */
        .events { background: var(--river-gray); padding: 4rem 2rem; }
        .events-container { max-width: 1200px; margin: 0 auto; }
        .events-grid { display: flex; flex-wrap: wrap; gap: 2rem; justify-content: center; }
        .event-card { background: white; border-radius: 8px; padding: 1.5rem; width: 300px; box-shadow: 0 3px 6px rgba(0,0,0,0.1); }
        .event-date { color: var(--chicago-blue); font-weight: 700; margin-bottom: 0.5rem; }
         /* Footer */
        footer { background: var(--dark-accent); color: white; padding: 2rem; text-align: center; }
        .footer-links a { color: #e2e8f0; text-decoration: none; margin: 0 1rem; }
        .footer-links a:hover { color: var(--chicago-blue); }
        .copyright { margin-top: 1rem; font-size: 0.9rem; color: #94a3b8; }
          /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .nav-links { display: none; flex-direction: column; position: absolute; top: 100%; left: 0; width: 100%; background: white; padding: 1rem 2rem; gap: 1rem; }
            .nav-links.active { display: flex; }
            .menu-toggle { display: block; }
            .slide-caption h1 { font-size: 2rem; }
            .slide-caption p { font-size: 1rem; }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">RIVER NORTH CHI</div>
            <div class="menu-toggle" id="menuToggle">&#9776;</div>
            <div class="nav-links" id="navLinks">
                <a href="#home">Home</a>
                <a href="#highlights">Explore</a>
                <a href="#events">Events</a>
                <a href="#dining">Dining</a>
                <a href="#contact">Contact</a>
            </div>
        </div>
    </nav>

   <!-- Hero Carousel (Home Section) -->
   <section class="hero-carousel" id="home">
        <div class="carousel-slide active">
            <img src="https://images.unsplash.com/photo-1556703016-b8fe2e4b5b8b?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="River North Skyline at Dusk">
            <div class="slide-caption">
                <h1>Where Art Meets Urban Life</h1>
                <p>Discover Chicago's trendiest neighborhood – home to galleries, rooftop bars, and world-class dining.</p>
                <a href="#highlights" class="btn">Start Exploring</a>
            </div>
        </div>
        <div class="carousel-slide">
            <img src="https://images.unsplash.com/photo-1585060544812-6b45742d762f?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="River North Art Galleries">
            <div class="slide-caption">
                <h1>Chicago's Creative Hub</h1>
                <p>With over 100 art galleries, River North is a canvas for contemporary and classic works.</p>
                <a href="#dining" class="btn">Find Local Eats</a>
            </div>
        </div>
        <div class="carousel-slide">
            <img src="https://images.unsplash.com/photo-1568515045872-491a36120139?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="River North Rooftop Views">
            <div class="slide-caption">
                <h1>Sky-High Experiences</h1>
                <p>Take in panoramic city views from iconic rooftop lounges and terraces.</p>
                <a href="#events" class="btn">See Upcoming Events</a>
            </div>
        </div>
    </section>

   <!-- Highlights Section -->
   <section class="highlights" id="highlights">
        <h2 class="section-title">What Makes River North Special</h2>
        <div class="cards-grid">
            <div class="card">
                <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Art Galleries">
                <div class="card-content">
                    <h3>World-Class Art Scene</h3>
                    <p>Explore renowned galleries showcasing modern, contemporary, and street art from local and international artists.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Dining">
                <div class="card-content">
                    <h3>Culinary Destination</h3>
                    <p>From Michelin-starred restaurants to cozy cafes, River North offers flavors from around the globe.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1534430480872-3498386e7856?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Rooftops">
                <div class="card-content">
                    <h3>Iconic Rooftops</h3>
                    <p>Enjoy sunset views and craft cocktails at some of Chicago's most popular sky-high venues.</p>
                </div>
            </div>
            <div class="card">
                <img src="https://images.unsplash.com/photo-1588496274765-7a6212e10213?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Shopping">
                <div class="card-content">
                    <h3>Unique Shopping</h3>
                    <p>Discover boutique shops, designer stores, and vintage finds in the neighborhood's charming streets.</p>
                </div>
            </div>
        </div>
    </section>

   <!-- Events Snippet -->
   <section class="events" id="events">
        <div class="events-container">
            <h2 class="section-title">Upcoming in River North</h2>
            <div class="events-grid">
                <div class="event-card">
                    <div class="event-date">DEC 15 | 6-9 PM</div>
                    <h3>River North Gallery Walk</h3>
                    <p>Free self-guided tour of 20+ galleries featuring new exhibitions and artist talks.</p>
                </div>
                <div class="event-date">DEC 22 | 11 AM-4 PM</div>
                <div class="event-card">
                    <h3>Holiday Market at Wolf Point</h3>
                    <p>Local crafts, food trucks, and live music in the heart of the neighborhood.</p>
                </div>
                <div class="event-card">
                    <div class="event-date">JAN 6 | 8-11 PM</div>
                    <h3>Rooftop New Year's Bash</h3>
                    <p>Celebrate with cocktails, DJ sets, and skyline views at The J. Parker.</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 2rem;">
                <a href="#" class="btn">View All Events</a>
            </div>
        </div>
    </section>

   <!-- Footer -->
   <footer>
        <div class="footer-links">
            <a href="#home">Home</a>
            <a href="#highlights">Explore</a>
            <a href="#events">Events</a>
            <a href="#dining">Dining</a>
            <a href="#contact">Contact</a>
        </div>
        <div class="copyright">
            &copy; 2025 River North Chicago | All Rights Reserved
        </div>
    </footer>

   <!-- Carousel & Mobile Menu Script -->
   <script>
    // Mobile Menu Toggle
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        menuToggle.addEventListener('click', () => navLinks.classList.toggle('active'));

        // Auto-Rotating Carousel
        const slides = document.querySelectorAll('.carousel-slide');
        let currentSlide = 0;
        function nextSlide() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }
        setInterval(nextSlide, 5000); // Change slide every 5 seconds
    </script>
</body>
</html>
