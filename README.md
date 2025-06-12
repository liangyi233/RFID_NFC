RDID_NFC
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>智能卡</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome -->
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <!-- Chart.js -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.8/dist/chart.umd.min.js"></script>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  
  <!-- Tailwind Configuration -->
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            primary: '#165DFF',
            secondary: '#36D399',
            accent: '#FF9F1C',
            dark: {
              bg: '#0F172A',
              card: '#1E293B',
              text: '#E2E8F0'
            }
          },
          fontFamily: {
            inter: ['Inter', 'sans-serif'],
          },
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .text-shadow {
        text-shadow: 0 2px 4px rgba(0,0,0,0.1);
      }
      .card-hover {
        transition: all 0.3s ease;
      }
      .card-hover:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
      }
      .animate-float {
        animation: float 6s ease-in-out infinite;
      }
      @keyframes float {
        0% { transform: translateY(0px); }
        50% { transform: translateY(-10px); }
        100% { transform: translateY(0px); }
      }
      .bg-gradient {
        background: linear-gradient(135deg, #165DFF 0%, #36D399 100%);
      }
    }
  </style>
</head>
<body class="font-inter bg-gray-50 text-gray-800 dark:bg-dark-bg dark:text-dark-text min-h-screen">
  <!-- Navigation -->
  <header id="navbar" class="fixed w-full top-0 z-50 transition-all duration-300 bg-white/80 dark:bg-dark-bg/80 backdrop-blur-md">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <div class="flex items-center">
          <a href="#" class="text-xl font-bold text-primary dark:text-primary">
            <i class="fa fa-github mr-2"></i>Your Profile
          </a>
        </div>
        
        <!-- Desktop Navigation -->
        <nav class="hidden md:flex space-x-8">
          <a href="#about" class="text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">About</a>
          <a href="#projects" class="text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Projects</a>
          <a href="#skills" class="text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Skills</a>
          <a href="#blog" class="text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Blog</a>
          <a href="#contact" class="text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Contact</a>
        </nav>
        
        <div class="flex items-center space-x-4">
          <!-- Dark Mode Toggle -->
          <button id="darkModeToggle" class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-dark-card transition-colors">
            <i class="fa fa-moon-o dark:hidden"></i>
            <i class="fa fa-sun-o hidden dark:inline-block"></i>
          </button>
          
          <!-- Mobile Menu Button -->
          <button id="mobileMenuButton" class="md:hidden p-2 rounded-md hover:bg-gray-100 dark:hover:bg-dark-card transition-colors">
            <i class="fa fa-bars"></i>
          </button>
        </div>
      </div>
    </div>
    
    <!-- Mobile Navigation -->
    <div id="mobileMenu" class="md:hidden hidden bg-white dark:bg-dark-card shadow-lg rounded-b-lg mx-4">
      <div class="px-4 py-3 space-y-3">
        <a href="#about" class="block py-2 text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">About</a>
        <a href="#projects" class="block py-2 text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Projects</a>
        <a href="#skills" class="block py-2 text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Skills</a>
        <a href="#blog" class="block py-2 text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Blog</a>
        <a href="#contact" class="block py-2 text-gray-700 hover:text-primary dark:text-gray-300 dark:hover:text-primary transition-colors">Contact</a>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="hero" class="pt-28 pb-16 md:pt-40 md:pb-24">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row items-center">
        <div class="md:w-1/2 mb-10 md:mb-0">
          <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold leading-tight text-shadow">
            第六组物联网 <span class="text-primary">RFID好评智能卡</span>
          </h1>
          <p class="mt-4 text-lg md:text-xl text-gray-600 dark:text-gray-400 max-w-xl">
            专注于为商家提供美观、易用的好评智能卡
          </p>
          <div class="mt-8 flex flex-wrap gap-4">
            <a href="#projects" class="px-6 py-3 bg-primary hover:bg-primary/90 text-white rounded-lg shadow-lg hover:shadow-xl transition-all duration-300">
              <i class="fa fa-code mr-2"></i>跳转页面
            </a>
            <a href="#contact" class="px-6 py-3 bg-white dark:bg-dark-card hover:bg-gray-100 dark:hover:bg-dark-card/80 text-gray-800 dark:text-gray-200 rounded-lg shadow-lg hover:shadow-xl transition-all duration-300">
              <i class="fa fa-envelope mr-2"></i>联系我们
            </a>
          </div>
          <div class="mt-10 flex space-x-6">
            <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
              <i class="fa fa-github text-2xl"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
              <i class="fa fa-twitter text-2xl"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
              <i class="fa fa-linkedin text-2xl"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
              <i class="fa fa-dev text-2xl"></i>
            </a>
          </div>
        </div>
        <div class="md:w-1/2 flex justify-center">
          <div class="relative">
            <div class="w-64 h-64 md:w-80 md:h-80 rounded-full bg-gradient animate-float">
              <img src="https://picsum.photos/id/160/400/400" alt="NFC card" class="absolute inset-0 w-full h-full rounded-full object-cover p-2">
            </div>
            <div class="absolute -bottom-4 -right-4 bg-white dark:bg-dark-card p-3 rounded-lg shadow-lg">
              <div class="flex items-center">
                <div class="w-3 h-3 bg-green-500 rounded-full animate-pulse mr-2"></div>
                <span class="font-medium">好评智能卡</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16 bg-gray-100 dark:bg-dark-card/30">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-[clamp(1.8rem,4vw,2.5rem)] font-bold">About Me</h2>
        <div class="w-20 h-1 bg-primary mx-auto mt-4 rounded-full"></div>
      </div>
      
      <div class="max-w-3xl mx-auto">
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg p-8 md:p-12">
          <p class="text-lg leading-relaxed mb-6 text-gray-700 dark:text-gray-300">
            I'm a passionate software developer with experience in building web applications, mobile apps, and desktop software. My journey in tech started [mention how you got into tech, e.g., "when I built my first website at 15"] and since then, I've been constantly learning and growing.
          </p>
          <p class="text-lg leading-relaxed mb-6 text-gray-700 dark:text-gray-300">
            I specialize in [mention your tech stack, e.g., "JavaScript, React, Node.js, and Python"] and I'm always eager to explore new technologies and frameworks. My goal is to create efficient, scalable, and user-friendly solutions that solve real-world problems.
          </p>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mt-10">
            <div>
              <h3 class="text-xl font-semibold mb-4 text-primary">Education</h3>
              <div class="space-y-4">
                <div class="p-4 bg-gray-50 dark:bg-dark-bg rounded-lg">
                  <h4 class="font-medium">University of Technology</h4>
                  <p class="text-gray-600 dark:text-gray-400">Computer Science, B.S.</p>
                  <p class="text-sm text-gray-500 dark:text-gray-500">2018 - 2022</p>
                </div>
              </div>
            </div>
            <div>
              <h3 class="text-xl font-semibold mb-4 text-primary">Experience</h3>
              <div class="space-y-4">
                <div class="p-4 bg-gray-50 dark:bg-dark-bg rounded-lg">
                  <h4 class="font-medium">Senior Developer</h4>
                  <p class="text-gray-600 dark:text-gray-400">Tech Company Inc.</p>
                  <p class="text-sm text-gray-500 dark:text-gray-500">2022 - Present</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="py-16">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-[clamp(1.8rem,4vw,2.5rem)] font-bold">My Projects</h2>
        <div class="w-20 h-1 bg-primary mx-auto mt-4 rounded-full"></div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Project Card 1 -->
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg overflow-hidden card-hover">
          <div class="h-48 overflow-hidden">
            <img src="https://picsum.photos/id/1/600/400" alt="Project image" class="w-full h-full object-cover">
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-3">
              <h3 class="text-xl font-bold">Project Name 1</h3>
              <span class="px-2 py-1 bg-blue-100 dark:bg-blue-900/30 text-blue-800 dark:text-blue-300 text-xs rounded-full">React</span>
            </div>
            <p class="text-gray-600 dark:text-gray-400 mb-4">
              A modern web application that solves [problem] using [technology]. This project showcases my skills in [specific skills].
            </p>
            <div class="flex justify-between items-center">
              <span class="text-sm text-gray-500 dark:text-gray-500">
                <i class="fa fa-star mr-1"></i> 243
              </span>
              <div class="flex space-x-2">
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-github"></i>
                </a>
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-external-link"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Project Card 2 -->
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg overflow-hidden card-hover">
          <div class="h-48 overflow-hidden">
            <img src="https://picsum.photos/id/2/600/400" alt="Project image" class="w-full h-full object-cover">
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-3">
              <h3 class="text-xl font-bold">Project Name 2</h3>
              <span class="px-2 py-1 bg-green-100 dark:bg-green-900/30 text-green-800 dark:text-green-300 text-xs rounded-full">Node.js</span>
            </div>
            <p class="text-gray-600 dark:text-gray-400 mb-4">
              A backend service that handles [specific task] with high performance and scalability. Built with [technologies].
            </p>
            <div class="flex justify-between items-center">
              <span class="text-sm text-gray-500 dark:text-gray-500">
                <i class="fa fa-star mr-1"></i> 187
              </span>
              <div class="flex space-x-2">
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-github"></i>
                </a>
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-external-link"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Project Card 3 -->
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg overflow-hidden card-hover">
          <div class="h-48 overflow-hidden">
            <img src="https://picsum.photos/id/3/600/400" alt="Project image" class="w-full h-full object-cover">
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-3">
              <h3 class="text-xl font-bold">Project Name 3</h3>
              <span class="px-2 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-800 dark:text-purple-300 text-xs rounded-full">Python</span>
            </div>
            <p class="text-gray-600 dark:text-gray-400 mb-4">
              A data analysis tool that processes [type of data] and generates insights using [techniques]. Features [key features].
            </p>
            <div class="flex justify-between items-center">
              <span class="text-sm text-gray-500 dark:text-gray-500">
                <i class="fa fa-star mr-1"></i> 156
              </span>
              <div class="flex space-x-2">
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-github"></i>
                </a>
                <a href="#" class="text-gray-600 hover:text-primary dark:text-gray-400 dark:hover:text-primary transition-colors">
                  <i class="fa fa-external-link"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <div class="text-center mt-12">
        <a href="#" class="inline-flex items-center px-6 py-3 bg-white dark:bg-dark-card hover:bg-gray-100 dark:hover:bg-dark-card/80 text-gray-800 dark:text-gray-200 rounded-lg shadow-lg hover:shadow-xl transition-all duration-300">
          <i class="fa fa-github mr-2"></i> View All Projects
        </a>
      </div>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills" class="py-16 bg-gray-100 dark:bg-dark-card/30">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-[clamp(1.8rem,4vw,2.5rem)] font-bold">My Skills</h2>
        <div class="w-20 h-1 bg-primary mx-auto mt-4 rounded-full"></div>
      </div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
        <div>
          <h3 class="text-xl font-semibold mb-6 text-primary">Technical Skills</h3>
          <div class="space-y-6">
            <!-- Skill 1 -->
            <div>
              <div class="flex justify-between mb-2">
                <span class="font-medium">JavaScript</span>
                <span class="text-gray-500 dark:text-gray-500">95%</span>
              </div>
              <div class="h-2 bg-gray-200 dark:bg-dark-bg rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 95%"></div>
              </div>
            </div>
            
            <!-- Skill 2 -->
            <div>
              <div class="flex justify-between mb-2">
                <span class="font-medium">React</span>
                <span class="text-gray-500 dark:text-gray-500">90%</span>
              </div>
              <div class="h-2 bg-gray-200 dark:bg-dark-bg rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 90%"></div>
              </div>
            </div>
            
            <!-- Skill 3 -->
            <div>
              <div class="flex justify-between mb-2">
                <span class="font-medium">Node.js</span>
                <span class="text-gray-500 dark:text-gray-500">85%</span>
              </div>
              <div class="h-2 bg-gray-200 dark:bg-dark-bg rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 85%"></div>
              </div>
            </div>
            
            <!-- Skill 4 -->
            <div>
              <div class="flex justify-between mb-2">
                <span class="font-medium">Python</span>
                <span class="text-gray-500 dark:text-gray-500">80%</span>
              </div>
              <div class="h-2 bg-gray-200 dark:bg-dark-bg rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 80%"></div>
              </div>
            </div>
            
            <!-- Skill 5 -->
            <div>
              <div class="flex justify-between mb-2">
                <span class="font-medium">HTML/CSS</span>
                <span class="text-gray-500 dark:text-gray-500">95%</span>
              </div>
              <div class="h-2 bg-gray-200 dark:bg-dark-bg rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 95%"></div>
              </div>
            </div>
          </div>
        </div>
        
        <div>
          <h3 class="text-xl font-semibold mb-6 text-primary">Tools & Technologies</h3>
          <div class="grid grid-cols-2 sm:grid-cols-3 gap-4">
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-github text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>Git</span>
            </div>
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-database text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>SQL</span>
            </div>
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-terminal text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>CLI</span>
            </div>
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-cloud text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>AWS</span>
            </div>
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-code-fork text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>Docker</span>
            </div>
            <div class="bg-white dark:bg-dark-card p-4 rounded-lg shadow-md flex items-center justify-center">
              <i class="fa fa-server text-2xl mr-3 text-gray-600 dark:text-gray-400"></i>
              <span>Linux</span>
            </div>
          </div>
          
          <h3 class="text-xl font-semibold mt-12 mb-6 text-primary">Coding Activity</h3>
          <div class="bg-white dark:bg-dark-card p-6 rounded-xl shadow-lg">
            <canvas id="codingActivityChart" height="200"></canvas>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Blog Section -->
  <section id="blog" class="py-16">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-[clamp(1.8rem,4vw,2.5rem)] font-bold">Latest Blog Posts</h2>
        <div class="w-20 h-1 bg-primary mx-auto mt-4 rounded-full"></div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Blog Post 1 -->
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg overflow-hidden card-hover">
          <div class="h-48 overflow-hidden">
            <img src="https://picsum.photos/id/4/600/400" alt="Blog post image" class="w-full h-full object-cover">
          </div>
          <div class="p-6">
            <div class="flex items-center mb-3">
              <span class="text-sm text-gray-500 dark:text-gray-500">May 15, 2023</span>
              <span class="mx-2">•</span>
              <span class="text-sm text-gray-500 dark:text-gray-500">5 min read</span>
            </div>
            <h3 class="text-xl font-bold mb-3">How I Built My First Full-Stack Application</h3>
            <p class="text-gray-600 dark:text-gray-400 mb-4">
              In this post, I share my experience building a full-stack application from scratch, including the challenges I faced and the lessons I learned.
            </p>
            <a href="#" class="inline-flex items-center text-primary hover:text-primary/80 transition-colors">
              Read more <i class="fa fa-arrow-right ml-2"></i>
            </a>
          </div>
        </div>
        
        <!-- Blog Post 2 -->
        <div class="bg-white dark:bg-dark-card rounded-xl shadow-lg overflow-hidden card-hover">
          <div class="h-48 overflow-hidden">
            <img src="https://picsum.photos/id/5/600/400" alt="Blog post image" class="w-full h-full object-cover">
          </div>
          <div class="p-6">
            <div class="flex items-center mb-3">
              <span class="text-sm text-gray-500 dark:text-gray-500">April 22, 2023</span>
              
