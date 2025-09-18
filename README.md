<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>VIRUS - Portfolio</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1s ease-out, transform 1s ease-out;
    }
    .fade-in.show {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body class="bg-gray-900 text-white font-sans">
  <!-- Navbar -->
  <nav class="bg-gray-800 fixed w-full z-10 top-0 shadow-lg">
    <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
      <div class="text-2xl font-bold text-green-400">VIRUS</div>
      <div class="space-x-6">
        <a href="#home" class="hover:text-green-400">Home</a>
        <a href="#about" class="hover:text-green-400">About Us</a>
        <a href="#contact" class="hover:text-green-400">Contact</a>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <section id="home" class="h-screen flex flex-col justify-center items-center text-center px-6">
    <img src="logo.png" alt="VIRUS Logo" class="w-32 h-32 mb-6 animate-bounce">
    <h1 class="text-4xl md:text-6xl font-bold mb-4">Securing the Future</h1>
    <p class="text-xl text-gray-300 mb-6">One Line of Code at a Time</p>
    <a href="#contact" class="bg-green-500 px-6 py-3 rounded-full font-semibold hover:bg-green-600 transition">
      Get in Touch
    </a>
  </section>

  <!-- About -->
  <section id="about" class="py-20 px-6 fade-in">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-6 text-green-400">About Us</h2>
      <p class="text-gray-300 leading-relaxed">
        We are <span class="text-green-400 font-bold">VIRUS</span>, a passionate team of developers and security researchers.
        Our mission is to <span class="text-green-400">build secure web and desktop applications</span> while providing
        <span class="text-green-400">penetration testing services</span> to ensure that businesses stay safe in the digital era.
      </p>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="py-20 px-6 bg-gray-800 fade-in">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-10 text-green-400">What We Offer</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="p-6 bg-gray-700 rounded-lg shadow hover:scale-105 transition">
          <h3 class="text-xl font-semibold mb-3">Fullstack Development</h3>
          <p class="text-gray-300">Modern web & desktop applications with secure design.</p>
        </div>
        <div class="p-6 bg-gray-700 rounded-lg shadow hover:scale-105 transition">
          <h3 class="text-xl font-semibold mb-3">Penetration Testing</h3>
          <p class="text-gray-300">Comprehensive security audits with detailed reports.</p>
        </div>
        <div class="p-6 bg-gray-700 rounded-lg shadow hover:scale-105 transition">
          <h3 class="text-xl font-semibold mb-3">Consulting</h3>
          <p class="text-gray-300">Helping startups and companies build secure solutions.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 fade-in">
    <div class="max-w-3xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-6 text-green-400">Contact Us</h2>
      <p class="text-gray-300 mb-4">Have a project in mind? Let's talk.</p>
      <p class="text-xl text-green-400 font-semibold">info@virus-team.com</p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 py-6 text-center text-gray-400">
    <div class="space-x-6 mb-3">
      <a href="#home" class="hover:text-green-400">Home</a>
      <a href="#about" class="hover:text-green-400">About Us</a>
      <a href="#contact" class="hover:text-green-400">Contact</a>
    </div>
    <p>&copy; 2025 VIRUS. All Rights Reserved.</p>
  </footer>

  <!-- Animation JS -->
  <script>
    const faders = document.querySelectorAll('.fade-in');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('show');
        }
      });
    });
    faders.forEach(fade => observer.observe(fade));
  </script>
</body>
</html>
