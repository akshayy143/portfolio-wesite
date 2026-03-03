# portfolio-wesite


<!DOCTYPE html>
<html lang="en">
<head>
    <base target="_self">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redoy Anul Haque | Portfolio</title>
    <meta name="description" content="Portfolio website of Redoy Anul Haque - Web Developer and Designer">
    <meta name="keywords" content="web developer, portfolio, designer, frontend, backend">
    <meta name="author" content="Redoy Anul Haque">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: "#2563eb",
                        secondary: "#1e40af",
                        accent: "#3b82f6",
                        dark: "#1f2937",
                        light: "#f9fafb"
                    },
                    fontFamily: {
                        'sans': ['Inter', 'system-ui', 'sans-serif'],
                        'mono': ['Fira Code', 'monospace']
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.5s ease-in-out',
                        'slide-up': 'slideUp 0.3s ease-out'
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' }
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(10px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' }
                        }
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500&display=swap');
        
        html {
            scroll-behavior: smooth;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .typewriter {
            overflow: hidden;
            border-right: .15em solid #3b82f6;
            white-space: nowrap;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #3b82f6 }
        }
    </style>
</head>
<body class="font-sans bg-light text-gray-800">
    <!-- Header & Navigation -->
    <header class="fixed w-full bg-white/90 backdrop-blur-sm shadow-sm z-50">
        <nav class="container mx-auto px-4 py-4">
            <div class="flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <div class="w-8 h-8 rounded-full gradient-bg"></div>
                    <a href="#home" class="text-xl font-bold text-dark hover:text-primary transition-colors">Redoy Anul Haque</a>
                </div>
                
                <ul id="nav-menu" class="hidden md:flex space-x-8"></ul>
                
                <div class="flex items-center space-x-4">
                    <button id="theme-toggle" class="p-2 rounded-full hover:bg-gray-100 transition-colors">
                        <i class="fas fa-moon text-gray-600"></i>
                    </button>
                    <button id="mobile-menu-btn" class="md:hidden p-2 rounded-lg hover:bg-gray-100 transition-colors">
                        <i class="fas fa-bars text-gray-700"></i>
                    </button>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="md:hidden mt-4 hidden">
                <ul id="mobile-nav-menu" class="space-y-2"></ul>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="pt-16">
        <!-- Hero Section -->
        <section id="home" class="min-h-screen flex items-center">
            <div class="container mx-auto px-4 py-12">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="animate-fade-in">
                        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-4">
                            Hi, I'm <span class="text-primary">Redoy Anul Haque</span>
                        </h1>
                        <div class="typewriter text-2xl md:text-3xl text-gray-600 mb-6">
                            Full Stack Web Developer
                        </div>
                        <p class="text-lg text-gray-600 mb-8 max-w-2xl">
                            I create beautiful, functional websites and web applications with modern technologies. 
                            Passionate about clean code, user experience, and solving complex problems.
                        </p>
                        <div class="flex flex-wrap gap-4">
                            <a href="#contact" class="px-6 py-3 bg-primary text-white rounded-lg hover:bg-secondary transition-colors font-medium">
                                Get In Touch
                            </a>
                            <a href="#projects" class="px-6 py-3 border-2 border-primary text-primary rounded-lg hover:bg-primary hover:text-white transition-colors font-medium">
                                View Projects
                            </a>
                        </div>
                    </div>
                    
                    <div class="relative">
                        <div class="relative w-64 h-64 md:w-80 md:h-80 lg:w-96 lg:h-96 mx-auto">
                            <div class="absolute inset-0 gradient-bg rounded-full animate-pulse opacity-20"></div>
                            <img src="https://picsum.photos/400?random=1" alt="Redoy Anul Haque - Web Developer" 
                                 class="relative w-full h-full rounded-full object-cover border-8 border-white shadow-2xl">
                        </div>
                        <div class="absolute -bottom-4 -right-4 w-24 h-24 bg-accent/10 rounded-full"></div>
                        <div class="absolute -top-4 -left-4 w-16 h-16 bg-primary/10 rounded-full"></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="py-20 bg-white">
            <div class="container mx-auto px-4">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">About Me</h2>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div>
                        <h3 class="text-2xl font-semibold mb-4">My Journey</h3>
                        <p class="text-gray-600 mb-6">
                            With over 5 years of experience in web development, I've worked on various projects 
                            ranging from small business websites to large-scale web applications. I specialize in 
                            creating responsive, accessible, and performant web solutions.
                        </p>
                        <p class="text-gray-600 mb-8">
                            My approach combines technical expertise with creative problem-solving to deliver 
                            exceptional digital experiences that meet both user needs and business goals.
                        </p>
                        
                        <div id="skills-container" class="grid grid-cols-2 md:grid-cols-3 gap-4"></div>
                    </div>
                    
                    <div class="space-y-6">
                        <div class="bg-gray-50 p-6 rounded-xl">
                            <h4 class="text-xl font-semibold mb-3">Education</h4>
                            <div class="space-y-4">
                                <div>
                                    <h5 class="font-medium text-primary">Bachelor of Science in Computer Science</h5>
                                    <p class="text-gray-600">University of Technology • 2015-2019</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="bg-gray-50 p-6 rounded-xl">
                            <h4 class="text-xl font-semibold mb-3">Certifications</h4>
                            <div id="certifications-container" class="space-y-2"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="py-20 bg-gray-50">
            <div class="container mx-auto px-4">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-4">Featured Projects</h2>
                <p class="text-gray-600 text-center mb-12 max-w-2xl mx-auto">
                    Here are some of my recent projects that showcase my skills and expertise.
                </p>
                
                <div id="projects-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"></div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-20 bg-white">
            <div class="container mx-auto px-4">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Get In Touch</h2>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                    <div>
                        <h3 class="text-2xl font-semibold mb-6">Let's Work Together</h3>
                        <p class="text-gray-600 mb-8">
                            Have a project in mind? I'd love to hear about it. Send me a message and let's discuss 
                            how we can work together to bring your ideas to life.
                        </p>
                        
                        <div id="contact-info" class="space-y-4"></div>
                    </div>
                    
                    <div class="bg-gray-50 p-8 rounded-xl">
                        <form id="contact-form" class="space-y-6">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-2">Name</label>
                                <input type="text" id="name" name="name" 
                                       class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition"
                                       required>
                            </div>
                            
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-2">Email</label>
                                <input type="email" id="email" name="email" 
                                       class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition"
                                       required>
                            </div>
                            
                            <div>
                                <label for="message" class="block text-sm font-medium text-gray-700 mb-2">Message</label>
                                <textarea id="message" name="message" rows="5"
                                          class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring-2 focus:ring-primary/20 outline-none transition"
                                          required></textarea>
                            </div>
                            
                            <button type="submit" 
                                    class="w-full px-6 py-3 bg-primary text-white rounded-lg hover:bg-secondary transition-colors font-medium">
                                Send Message
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-8 h-8 rounded-full gradient-bg"></div>
                        <span class="text-xl font-bold">Redoy Anul Haque</span>
                    </div>
                    <p class="text-gray-400">Building digital experiences that matter.</p>
                </div>
                
                <div class="mb-6 md:mb-0">
                    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
                    <ul id="footer-links" class="space-y-2"></ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">Connect With Me</h4>
                    <div id="social-links" class="flex space-x-4"></div>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; <span id="current-year"></span> Redoy Anul Haque. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Data Layer
        const navigationItems = [
            { "label": "Home", "href": "#home", "icon": "fas fa-home" },
            { "label": "About", "href": "#about", "icon": "fas fa-user" },
            { "label": "Projects", "href": "#projects", "icon": "fas fa-code" },
            { "label": "Contact", "href": "#contact", "icon": "fas fa-envelope" }
        ];

        const skills = [
            { "name": "HTML/CSS", "level": "95%" },
            { "name": "JavaScript", "level": "90%" },
            { "name": "React", "level": "85%" },
            { "name": "Node.js", "level": "80%" },
            { "name": "Python", "level": "75%" },
            { "name": "UI/UX Design", "level": "85%" }
        ];

        const certifications = [
            { "name": "AWS Certified Developer", "issuer": "Amazon Web Services" },
            { "name": "Google Cloud Professional", "issuer": "Google Cloud" },
            { "name": "React Advanced Certification", "issuer": "Meta" }
        ];

        const projects = [
            { 
                "title": "E-Commerce Platform", 
                "description": "A full-featured online shopping platform with payment integration and admin dashboard.",
                "image": "https://picsum.photos/400/300?random=2",
                "alt": "E-commerce platform dashboard",
                "technologies": ["React", "Node.js", "MongoDB", "Stripe"],
                "link": "#"
            },
            { 
                "title": "Task Management App", 
                "description": "Collaborative project management tool with real-time updates and team features.",
                "image": "https://picsum.photos/400/300?random=3",
                "alt": "Task management application interface",
                "technologies": ["Vue.js", "Firebase", "Tailwind CSS"],
                "link": "#"
            },
            { 
                "title": "Weather Dashboard", 
                "description": "Real-time weather application with location-based forecasts and interactive maps.",
                "image": "https://picsum.photos/400/300?random=4",
                "alt": "Weather dashboard with maps",
                "technologies": ["JavaScript", "API Integration", "Chart.js"],
                "link": "#"
            },
            { 
                "title": "Portfolio Website", 
                "description": "Responsive portfolio website with dark mode and animated transitions.",
                "image": "https://picsum.photos/400/300?random=5",
                "alt": "Portfolio website design",
                "technologies": ["HTML", "CSS", "JavaScript"],
                "link": "#"
            },
            { 
                "title": "Social Media Analytics", 
                "description": "Analytics dashboard for social media performance tracking and insights.",
                "image": "https://picsum.photos/400/300?random=6",
                "alt": "Social media analytics dashboard",
                "technologies": ["React", "D3.js", "Express"],
                "link": "#"
            },
            { 
                "title": "Fitness Tracking App", 
                "description": "Mobile-first fitness application with workout plans and progress tracking.",
                "image": "https://picsum.photos/400/300?random=7",
                "alt": "Fitness tracking mobile application",
                "technologies": ["React Native", "Redux", "Firebase"],
                "link": "#"
            }
        ];

        const contactInfo = [
            { "icon": "fas fa-envelope", "text": "hello@redoyanulhaque.me", "link": "mailto:hello@redoyanulhaque.me" },
            { "icon": "fas fa-phone", "text": "+1 (123) 456-7890", "link": "tel:+11234567890" },
            { "icon": "fas fa-map-marker-alt", "text": "Dhaka, Bangladesh", "link": "#" }
        ];

        const socialLinks = [
            { "icon": "fab fa-github", "label": "GitHub", "href": "https://github.com/redoyanulhaque" },
            { "icon": "fab fa-linkedin", "label": "LinkedIn", "href": "https://linkedin.com/in/redoyanulhaque" },
            { "icon": "fab fa-twitter", "label": "Twitter", "href": "https://twitter.com/redoyanulhaque" },
            { "icon": "fab fa-dribbble", "label": "Dribbble", "href": "https://dribbble.com/redoyanulhaque" }
        ];

        const footerLinks = [
            { "label": "Privacy Policy", "href": "#privacy" },
            { "label": "Terms of Service", "href": "#terms" },
            { "label": "Sitemap", "href": "#sitemap" }
        ];

        // Reusable Render Functions
        function renderNavigation(items, isMobile = false) {
            return items.map(item => {
                const icon = isMobile ? "<i class=\"" + item.icon + " mr-2\"></i>" : "";
                return "<li><a href=\"" + item.href + "\" class=\"" + 
                       (isMobile ? "block py-2 px-4 rounded-lg hover:bg-gray-100 transition-colors" : 
                       "text-gray-600 hover:text-primary transition-colors font-medium") + 
                       "\">" + icon + item.label + "</a></li>";
            }).join("");
        }

        function renderSkills(items) {
            return items.map(item => 
                "<div class=\"mb-4\"><div class=\"flex justify-between mb-1\"><span class=\"font-medium\">" + 
                item.name + "</span><span class=\"text-gray-500\">" + item.level + "</span></div>" +
                "<div class=\"w-full bg-gray-200 rounded-full h-2\"><div class=\"bg-primary h-2 rounded-full\" style=\"width: " + 
                item.level + "\"></div></div></div>"
            ).join("");
        }

        function renderCertifications(items) {
            return items.map(item => 
                "<div><h5 class=\"font-medium\">" + item.name + "</h5><p class=\"text-gray-600 text-sm\">" + 
                item.issuer + "</p></div>"
            ).join("");
        }

        function renderProjects(items) {
            return items.map((item, index) => 
                "<div class=\"card-hover bg-white rounded-xl overflow-hidden shadow-lg border border-gray-100\">" +
                "<img src=\"" + item.image + "\" alt=\"" + item.alt + "\" class=\"w-full h-48 object-cover\" loading=\"lazy\">" +
                "<div class=\"p-6\"><h3 class=\"text-xl font-semibold mb-2\">" + item.title + "</h3>" +
                "<p class=\"text-gray-600 mb-4\">" + item.description + "</p>" +
                "<div class=\"flex flex-wrap gap-2 mb-4\">" + 
                item.technologies.map(tech => "<span class=\"px-3 py-1 bg-primary/10 text-primary rounded-full text-sm\">" + 
                tech + "</span>").join("") + "</div>" +
                "<a href=\"" + item.link + "\" class=\"inline-flex items-center text-primary font-medium hover:text-secondary transition-colors\">" +
                "View Project <i class=\"fas fa-arrow-right ml-2\"></i></a></div></div>"
            ).join("");
        }

        function renderContactInfo(items) {
            return items.map(item => 
                "<div class=\"flex items-center space-x-3\"><div class=\"w-10 h-10 rounded-full bg-primary/10 flex items-center justify-center\">" +
                "<i class=\"" + item.icon + " text-primary\"></i></div><div><a href=\"" + item.link + "\" class=\"hover:text-primary transition-colors\">" +
                item.text + "</a></div></div>"
            ).join("");
        }

        function renderSocialLinks(items) {
            return items.map(item => 
                "<a href=\"" + item.href + "\" target=\"_blank\" rel=\"noopener noreferrer\" " +
                "class=\"w-10 h-10 rounded-full bg-gray-800 hover:bg-primary flex items-center justify-center transition-colors\" " +
                "aria-label=\"" + item.label + "\"><i class=\"" + item.icon + "\"></i></a>"
            ).join("");
        }

        function renderFooterLinks(items) {
            return items.map(item => 
                "<li><a href=\"" + item.href + "\" class=\"text-gray-400 hover:text-white transition-colors\">" + 
                item.label + "</a></li>"
            ).join("");
        }

        // Initialize Page Content
        document.addEventListener("DOMContentLoaded", function() {
            // Set current year
            document.getElementById("current-year").textContent = new Date().getFullYear();
            
            // Render navigation
            document.getElementById("nav-menu").innerHTML = renderNavigation(navigationItems);
            document.getElementById("mobile-nav-menu").innerHTML = renderNavigation(navigationItems, true);
            
            // Render skills
            document.getElementById("skills-container").innerHTML = renderSkills(skills);
            
            // Render certifications
            document.getElementById("certifications-container").innerHTML = renderCertifications(certifications);
            
            // Render projects
            document.getElementById("projects-grid").innerHTML = renderProjects(projects);
            
            // Render contact info
            document.getElementById("contact-info").innerHTML = renderContactInfo(contactInfo);
            
            // Render social links
            document.getElementById("social-links").innerHTML = renderSocialLinks(socialLinks);
            
            // Render footer links
            document.getElementById("footer-links").innerHTML = renderFooterLinks(footerLinks);
            
            // Mobile menu toggle
            const mobileMenuBtn = document.getElementById("mobile-menu-btn");
            const mobileMenu = document.getElementById("mobile-menu");
            
            mobileMenuBtn.addEventListener("click", function() {
                mobileMenu.classList.toggle("hidden");
                const icon = mobileMenuBtn.querySelector("i");
                if (mobileMenu.classList.contains("hidden")) {
                    icon.className = "fas fa-bars text-gray-700";
                } else {
                    icon.className = "fas fa-times text-gray-700";
                }
            });
            
            // Theme toggle
            const themeToggle = document.getElementById("theme-toggle");
            themeToggle.addEventListener("click", function() {
                const icon = themeToggle.querySelector("i");
                if (document.body.classList.contains("dark")) {
                    document.body.classList.remove("dark");
                    document.body.classList.add("light");
                    icon.className = "fas fa-moon text-gray-600";
                } else {
                    document.body.classList.remove("light");
                    document.body.classList.add("dark");
                    icon.className = "fas fa-sun text-yellow-500";
                }
            });
            
            // Contact form submission
            const contactForm = document.getElementById("contact-form");
            contactForm.addEventListener("submit", function(e) {
                e.preventDefault();
                
                const formData = new FormData(contactForm);
                const data = Object.fromEntries(formData);
                
                // In a real application, you would send this data to a server
                console.log("Form submitted:", data);
                
                // Show success message
                alert("Thank you for your message! I'll get back to you soon.");
                contactForm.reset();
            });
            
            // Smooth scrolling for anchor links
            document.addEventListener("click", function(event) {
                const link = event.target.closest("a[href^='#']");
                if (!link) return;
                
                const href = link.getAttribute("href");
                if (href === "#") return;
                
                event.preventDefault();
                const target = document.querySelector(href);
                if (target) {
                    // Close mobile menu if open
                    if (!mobileMenu.classList.contains("hidden")) {
                        mobileMenu.classList.add("hidden");
                        mobileMenuBtn.querySelector("i").className = "fas fa-bars text-gray-700";
                    }
                    
                    window.scrollTo({
                        top: target.offsetTop - 80,
                        behavior: "smooth"
                    });
                }
            });
            
            // Add scroll animation to sections
            const observerOptions = {
                threshold: 0.1,
                rootMargin: "0px 0px -50px 0px"
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("animate-slide-up");
                    }
                });
            }, observerOptions);
            
            // Observe all sections
            document.querySelectorAll("section").forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
