<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Bites | Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Simple custom CSS for the mobile menu */
        .mobile-menu {
            display: none;
        }
        .mobile-menu.active {
            display: block;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="bg-white shadow-sm">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold text-gray-800">Simple Bites</h1>
            <nav class="hidden md:block">
                <ul class="flex space-x-6">
                    <li><a href="#home" class="text-gray-800 hover:text-amber-600">Home</a></li>
                    <li><a href="#menu" class="text-gray-800 hover:text-amber-600">Menu</a></li>
                    <li><a href="#reservations" class="text-gray-800 hover:text-amber-600">Reservations</a></li>
                </ul>
            </nav>
            <button id="menu-toggle" class="md:hidden text-gray-800">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
            </button>
        </div>
        <!-- Mobile menu -->
        <div id="mobile-menu" class="mobile-menu md:hidden bg-white py-2 px-4 shadow-md">
            <ul class="space-y-2">
                <li><a href="#home" class="block py-2 text-gray-800 hover:text-amber-600">Home</a></li>
                <li><a href="#menu" class="block py-2 text-gray-800 hover:text-amber-600">Menu</a></li>
                <li><a href="#reservations" class="block py-2 text-gray-800 hover:text-amber-600">Reservations</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="bg-amber-50 py-16">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Welcome to Simple Bites</h2>
            <p class="text-gray-600 mb-8 max-w-2xl mx-auto">Fresh ingredients, simple recipes, great flavors.</p>
            <a href="#reservations" class="bg-amber-600 text-white px-6 py-3 rounded-md hover:bg-amber-700 transition">Book a Table</a>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">Our Menu</h2>
            
            <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Starters -->
                <div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-4 pb-2 border-b border-gray-200">Starters</h3>
                    <div class="space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-800">Bruschetta</h4>
                            <p class="text-gray-600 text-sm">Tomato, basil, garlic on toasted bread</p>
                            <p class="text-amber-600 font-medium mt-1">$8</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-800">Soup of the Day</h4>
                            <p class="text-gray-600 text-sm">Ask your server for today's selection</p>
                            <p class="text-amber-600 font-medium mt-1">$7</p>
                        </div>
                    </div>
                </div>
                
                <!-- Mains -->
                <div>
                    <h3 class="text-xl font-semibold text-gray-800 mb-4 pb-2 border-b border-gray-200">Main Courses</h3>
                    <div class="space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-800">Classic Burger</h4>
                            <p class="text-gray-600 text-sm">Beef patty, cheese, lettuce, special sauce</p>
                            <p class="text-amber-600 font-medium mt-1">$14</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-800">Pasta Carbonara</h4>
                            <p class="text-gray-600 text-sm">Spaghetti, eggs, pancetta, parmesan</p>
                            <p class="text-amber-600 font-medium mt-1">$16</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reservations Section -->
    <section id="reservations" class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-8">Make a Reservation</h2>
            
            <div class="max-w-md mx-auto bg-white p-6 rounded-lg shadow-sm">
                <form>
                    <div class="mb-4">
                        <label for="name" class="block text-gray-700 mb-2">Name</label>
                        <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
                    </div>
                    <div class="mb-4">
                        <label for="email" class="block text-gray-700 mb-2">Email</label>
                        <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
                    </div>
                    <div class="mb-4">
                        <label for="date" class="block text-gray-700 mb-2">Date</label>
                        <input type="date" id="date" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
                    </div>
                    
                    <div class="mb-4">
                        <label for="guests" class="block text-gray-700 mb-2">Number of Guests</label>
                        <select id="guests" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
                            <option value="1">1 person</option>
                            <option value="2">2 people</option>
                            <option value="3">3 people</option>
                            <option value="4">4 people</option>
                            <option value="5">5+ people</option>
                        </select>
                    </div>
                    <button type="submit" class="w-full bg-amber-600 text-white py-2 rounded-md hover:bg-amber-700 transition">Book Table</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-4">
            <div class="text-center">
                <h3 class="text-xl font-bold mb-4">Simple Bites</h3>
                <p class="text-gray-300 mb-4">Bienvenue Main Street<br>Puducherry</p>
                <p class="text-gray-300 mb-4">Phone: +91786543368<br>Email: @simplebites.com</p>
                <p class="text-gray-400 text-sm">&copy; 2025 Simple Bites. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple mobile menu toggle
        document.getElementById('menu-toggle').addEventListener('click', function() {
            document.getElementById('mobile-menu').classList.toggle('active');
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                // Close mobile menu if open
                document.getElementById('mobile-menu').classList.remove('active');
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
