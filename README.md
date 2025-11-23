<!DOCTYPE html>

<html dir="rtl" lang="fa">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>HamedBLAZE</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/lucide@latest/dist/umd/lucide.js"></script>
<link href="https://fonts.googleapis.com/css2?family=Vazir:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            'vazir': ['Vazir', 'system-ui', 'sans-serif'],
          },
          colors: {
            'gaming-red': '#ff0000',
            'gaming-dark': '#0a0a0a',
            'gaming-surface': '#1a1a1a',
            'gaming-accent': '#ff4444',
            'gaming-border': '#333333',
          },
          animation: {
            'fade-in': 'fadeIn 0.6s ease-out',
            'slide-up': 'slideUp 0.8s ease-out',
            'scale-in': 'scaleIn 0.5s ease-out',
            'glow': 'glow 2s ease-in-out infinite alternate',
          },
          keyframes: {
            fadeIn: {
              '0%': { opacity: '0' },
              '100%': { opacity: '1' },
            },
            slideUp: {
              '0%': { opacity: '0', transform: 'translateY(30px)' },
              '100%': { opacity: '1', transform: 'translateY(0)' },
            },
            scaleIn: {
              '0%': { opacity: '0', transform: 'scale(0.9)' },
              '100%': { opacity: '1', transform: 'scale(1)' },
            },
            glow: {
              '0%': { boxShadow: '0 0 20px rgba(255, 0, 0, 0.5)' },
              '100%': { boxShadow: '0 0 30px rgba(255, 0, 0, 0.8)' },
            },
          },
          backdropBlur: {
            'xs': '2px',
          }
        }
      }
    };
  </script>
<style>
    .glass-effect {
      backdrop-filter: blur(10px);
      background: rgba(26, 26, 26, 0.8);
      border: 1px solid rgba(255, 255, 255, 0.1);
    }
    
    .text-gradient {
      background: linear-gradient(135deg, #ff0000 0%, #ff4444 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .hover-lift {
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .hover-lift:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }
    
    .content-card {
      background: linear-gradient(145deg, #1a1a1a 0%, #0f0f0f 100%);
      border: 1px solid #333;
    }
    
    /* Persian/RTL optimizations */
    .persian-text {
      font-feature-settings: "kern" 1;
      text-rendering: optimizeLegibility;
    }
  </style>
</head>
<body class="font-vazir bg-gaming-dark text-white min-h-screen">
<!-- Navigation Header -->
<!-- @COMPONENT: Header [navigation, logo, admin toggle] -->
<header class="sticky top-0 z-50 glass-effect border-b border-gaming-border">
<div class="container mx-auto px-4 py-4">
<div class="flex items-center justify-between">
<!-- Logo -->
<div class="flex items-center space-x-reverse space-x-4">
<h1 class="text-3xl font-bold text-gradient animate-glow">HamedBLAZE</h1>
<span class="text-gaming-accent text-sm font-medium bg-gaming-accent/20 px-2 py-1 rounded-full">LIVE</span>
</div>
 
<!-- Navigation -->
<nav class="hidden md:flex items-center space-x-reverse space-x-8">

<a class="text-white hover:text-gaming-accent transition-colors duration-300 font-medium relative group" href="#about">
            درباره من
            <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-gaming-accent transition-all duration-300 group-hover:w-full"></span>
</a>
<button class="bg-gaming-red hover:bg-gaming-accent px-4 py-2 rounded-lg font-medium transition-colors duration-300" data-event="click:toggleAdmin">
            پنل مدیریت
          </button>
</nav>

<!-- Mobile Menu Toggle -->
<button class="md:hidden text-white" data-event="click:toggleMobileMenu">
<i class="w-6 h-6" data-lucide="menu"></i>
</button>
</div>
<!-- Mobile Navigation -->
<!-- @STATE: mobileMenuOpen:boolean = false -->
<div class="md:hidden mt-4 pb-4 border-t border-gaming-border hidden" id="mobile-menu">
<nav class="flex flex-col space-y-4 mt-4">

<a class="text-white hover:text-gaming-accent transition-colors duration-300" href="#about">درباره من</a>
<button class="bg-gaming-red hover:bg-gaming-accent px-4 py-2 rounded-lg font-medium transition-colors duration-300 w-full">
            پنل مدیریت
          </button>
</nav>
</div>
</div>
</header>
<!-- @END_COMPONENT: Header -->
<!-- Hero Section -->
<!-- @COMPONENT: HeroSection [title, background, cta] -->
<section class="relative h-screen flex items-center justify-center overflow-hidden">
<!-- Background with gaming imagery -->
<!-- A dramatic gaming setup with RGB lighting, multiple monitors, and futuristic ambiance -->
<div class="absolute inset-0 bg-center bg-cover bg-no-repeat opacity-70" style="background-image: url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=1920&amp;h=1080')"></div>
<div class="absolute inset-0 bg-gradient-to-b from-gaming-dark/50 to-gaming-dark/90"></div>
<!-- Hero Content -->
<div class="relative z-10 text-center px-4 max-w-4xl mx-auto animate-fade-in">
<h2 class="text-5xl md:text-7xl font-bold mb-6 persian-text">
        به دنیای 
        <span class="text-gradient animate-glow">HamedBLAZE</span>
<br/>خوش اومدی 🔥
      </h2>
<p class="text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed persian-text">
        بهترین محتوای گیمینگ، چالش‌های هیجان‌انگیز، و داستان‌های ترسناک
      </p>
<div class="flex flex-col sm:flex-row gap-4 justify-center">

</div>
<!-- Stats -->
<div class="flex justify-center gap-8 mt-12 text-center">
<div class="animate-scale-in">
<div class="text-3xl font-bold text-gaming-accent" data-bind="stats.subscribers">127K</div>
<div class="text-sm text-gray-400">دنبال‌کننده</div>
</div>
<div class="animate-scale-in" style="animation-delay: 0.2s">
<div class="text-3xl font-bold text-gaming-accent" data-bind="stats.videos">850</div>
<div class="text-sm text-gray-400">ویدیو</div>
</div>
<div class="animate-scale-in" style="animation-delay: 0.4s">
<div class="text-3xl font-bold text-gaming-accent" data-bind="stats.views">2.5M</div>
<div class="text-sm text-gray-400">بازدید</div>
</div>
</div>
</div>
</section>
<!-- @END_COMPONENT: HeroSection -->
<!-- Featured Content Section -->
<!-- @COMPONENT: FeaturedContent [latest video, trending content] -->
<section class="py-16 px-4">
<div class="container mx-auto max-w-6xl">
<div class="text-center mb-12">
<h2 class="text-4xl font-bold mb-4 persian-text">🌟 محتوای ویژه</h2>
<p class="text-gray-400 text-lg">آخرین و بهترین محتواهای HamedBLAZE</p>
</div>
<div class="grid md:grid-cols-2 gap-8 items-center">
<!-- Latest Video -->
<div class="content-card rounded-2xl p-6 hover-lift animate-slide-up">
<div class="aspect-video bg-gaming-surface rounded-lg mb-4 relative overflow-hidden group">
<!-- A gaming scene with intense action, colorful special effects, and dramatic lighting -->
<img alt="Latest gaming video thumbnail" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" src="https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=800&amp;h=450"/>
<div class="absolute inset-0 bg-black/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
<button class="bg-gaming-red text-white p-4 rounded-full hover:bg-gaming-accent transition-colors">
<i class="w-8 h-8" data-lucide="play"></i>
</button>
</div>
<!-- Play button overlay -->
<div class="absolute top-4 right-4 bg-gaming-red text-white px-3 py-1 rounded-full text-sm font-bold">
              جدید
            </div>
</div>
<h3 class="text-2xl font-bold mb-2 persian-text" data-bind="latestVideo.title">چالش ترسناک نیمه‌شب در بازی هورور جدید!</h3>
<p class="text-gray-400 mb-4" data-bind="latestVideo.description">تو این ویدیو قراره یه چالش فوق‌العاده ترسناک رو انجام بدم که باعث شده قلبم از کار بیفته!</p>
<div class="flex items-center justify-between text-sm text-gray-500">
<span data-bind="latestVideo.views">45K بازدید</span>
<span data-bind="latestVideo.date">2 روز پیش</span>
</div>
</div>
<!-- Stats & Info -->
<div class="space-y-6">
<div class="content-card rounded-2xl p-6 hover-lift animate-slide-up" style="animation-delay: 0.2s">
<h3 class="text-2xl font-bold mb-4 text-gaming-accent">🏆 دستاوردهای اخیر</h3>
<div class="space-y-4">
<div class="flex items-center justify-between">
<span>بهترین گیمر ماه</span>
<span class="text-gaming-accent font-bold">🥇 طلایی</span>
</div>
<div class="flex items-center justify-between">
<span>100K دنبال‌کننده</span>
<span class="text-gaming-accent font-bold">✅ تکمیل</span>
</div>
<div class="flex items-center justify-between">
<span>ویدیوی میلیونی</span>
<span class="text-gaming-accent font-bold">🔥 فعال</span>
</div>
</div>
</div>
<div class="content-card rounded-2xl p-6 hover-lift animate-slide-up" style="animation-delay: 0.4s">
<h3 class="text-2xl font-bold mb-4 text-gaming-accent">📊 آمار هفته</h3>
<div class="grid grid-cols-2 gap-4">
<div class="text-center">
<div class="text-2xl font-bold text-gaming-red" data-bind="weeklyStats.newSubs">+2.5K</div>
<div class="text-sm text-gray-400">دنبال‌کننده جدید</div>
</div>
<div class="text-center">
<div class="text-2xl font-bold text-gaming-red" data-bind="weeklyStats.totalViews">180K</div>
<div class="text-sm text-gray-400">بازدید کل</div>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- @END_COMPONENT: FeaturedContent -->
<!-- Videos Section -->
<!-- @COMPONENT: VideosSection [video grid, filters, load more] -->
<section class="py-16 px-4 bg-gaming-surface/30" id="videos">
<div class="container mx-auto max-w-6xl">
<div class="flex items-center justify-between mb-12">
<div>
<h2 class="text-4xl font-bold mb-4 persian-text">🎮 آخرین ویدیوها</h2>
<p class="text-gray-400 text-lg">بهترین محتواهای گیمینگ و سرگرمی</p>
</div>
<!-- Filter Buttons -->
<div class="hidden md:flex gap-2">
<button class="bg-gaming-red text-white px-4 py-2 rounded-lg font-medium transition-colors">همه</button>
<button class="bg-gaming-surface text-gray-300 hover:bg-gaming-border px-4 py-2 rounded-lg font-medium transition-colors">گیمینگ</button>
<button class="bg-gaming-surface text-gray-300 hover:bg-gaming-border px-4 py-2 rounded-lg font-medium transition-colors">چالش</button>
<button class="bg-gaming-surface text-gray-300 hover:bg-gaming-border px-4 py-2 rounded-lg font-medium transition-colors">ترسناک</button>
</div>
</div>
<!-- Video Grid -->
<!-- @MAP: videos.map(video => ( -->
<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
<div class="content-card rounded-xl overflow-hidden hover-lift animate-slide-up" data-mock="true">
<div class="aspect-video relative group overflow-hidden">
<!-- A first-person shooter game scene with intense action and vibrant colors -->
<img alt="Gaming video thumbnail" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" src="https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=600&amp;h=338"/>
<div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
<button class="bg-gaming-red text-white p-3 rounded-full hover:bg-gaming-accent transition-colors">
<i class="w-6 h-6" data-lucide="play"></i>
</button>
</div>
<div class="absolute bottom-2 right-2 bg-black/80 text-white px-2 py-1 rounded text-sm" data-bind="video.duration">15:42</div>
</div>
<div class="p-4">
<h3 class="font-bold text-lg mb-2 line-clamp-2" data-bind="video.title">بازی جدید اکشن: مبارزه نهایی با باس!</h3>
<p class="text-gray-400 text-sm mb-3 line-clamp-2" data-bind="video.description">در این ویدیو قراره با قدرتمندترین باس بازی مبارزه کنیم و...</p>
<div class="flex items-center justify-between text-sm text-gray-500">
<span data-bind="video.views">23K بازدید</span>
<span data-bind="video.date">3 روز پیش</span>
</div>
</div>
</div>
<div class="content-card rounded-xl overflow-hidden hover-lift animate-slide-up" data-mock="true" style="animation-delay: 0.1s">
<div class="aspect-video relative group overflow-hidden">
<!-- A horror game scene with dark atmosphere and scary elements -->
<img alt="Horror gaming video thumbnail" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=600&amp;h=338"/>
<div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
<button class="bg-gaming-red text-white p-3 rounded-full hover:bg-gaming-accent transition-colors">
<i class="w-6 h-6" data-lucide="play"></i>
</button>
</div>
<div class="absolute bottom-2 right-2 bg-black/80 text-white px-2 py-1 rounded text-sm">22:18</div>
</div>
<div class="p-4">
<h3 class="font-bold text-lg mb-2 line-clamp-2">چالش ترسناک: بازی هورور در تاریکی!</h3>
<p class="text-gray-400 text-sm mb-3 line-clamp-2">امشب قراره بدون هیچ چراغی این بازی ترسناک رو تمام کنم...</p>
<div class="flex items-center justify-between text-sm text-gray-500">
<span>67K بازدید</span>
<span>1 هفته پیش</span>
</div>
</div>
</div>
<div class="content-card rounded-xl overflow-hidden hover-lift animate-slide-up" data-mock="true" style="animation-delay: 0.2s">
<div class="aspect-video relative group overflow-hidden">
<!-- A racing game scene with fast cars and motion blur effects -->
<img alt="Racing game video thumbnail" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" src="https://images.unsplash.com/photo-1493238792000-8113da705763?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=600&amp;h=338"/>
<div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
<button class="bg-gaming-red text-white p-3 rounded-full hover:bg-gaming-accent transition-colors">
<i class="w-6 h-6" data-lucide="play"></i>
</button>
</div>
<div class="absolute bottom-2 right-2 bg-black/80 text-white px-2 py-1 rounded text-sm">18:35</div>
</div>
<div class="p-4">
<h3 class="font-bold text-lg mb-2 line-clamp-2">مسابقه دیوانه‌وار: سریع‌ترین راننده!</h3>
<p class="text-gray-400 text-sm mb-3 line-clamp-2">بیایید ببینیم تو این مسابقه فوق‌العاده چه اتفاقی می‌افته...</p>
<div class="flex items-center justify-between text-sm text-gray-500">
<span>34K بازدید</span>
<span>5 روز پیش</span>
</div>
</div>
</div>
</div>
<!-- @END_MAP )) -->
<div class="text-center">
<button class="bg-gaming-red hover:bg-gaming-accent px-8 py-3 rounded-lg font-bold transition-colors duration-300" data-event="click:loadMoreVideos">
          مشاهده بیشتر
        </button>
</div>
</div>
</section>
<!-- @END_COMPONENT: VideosSection -->
<!-- Blog Section -->
<!-- @COMPONENT: BlogSection [article grid, categories, read more] -->
<!-- @END_COMPONENT: BlogSection -->
<!-- About Section -->
<!-- @COMPONENT: AboutSection [bio, achievements, social links] -->
<section class="py-16 px-4 bg-gaming-surface/30" id="about">
<div class="container mx-auto max-w-4xl">
<div class="text-center mb-12">
<h2 class="text-4xl font-bold mb-4 persian-text">🔥 درباره HamedBLAZE</h2>
</div>
<div class="grid md:grid-cols-2 gap-12 items-center">
<!-- Profile Image -->
<div class="text-center">
<!-- A professional gaming portrait with dramatic lighting and gaming setup in background -->
<a href="https://aparat.com/hamedblaze">

<img alt="HamedBLAZE profile picture" class="w-80 h-80 rounded-full mx-auto border-4 border-gaming-red shadow-lg hover-lift" src="https://static.cdn.asset.aparat.com/profile-photo/19906500-243039-m.jpg"/>
<!-- Social Links -->
<div class="flex justify-center gap-4 mt-8">
<a href=https://youtube.com/@hamedblaze
<a class="bg-gaming-surface hover:bg-gaming-red p-3 rounded-full transition-colors duration-300" href="#">
<i class="w-6 h-6" data-lucide="youtube"></i>
</a>
<a href=https://Instagram.com/hamed_blaze92/
	
<a class="bg-gaming-surface hover:bg-gaming-red p-3 rounded-full transition-colors duration-300" href="#">
<i class="w-6 h-6" data-lucide="instagram"></i>
</a>
<a href=minecraft://?addExternalServer=hamedxward84|hamedxward84.aternos.me:53943
	
<a class="bg-gaming-surface hover:bg-gaming-red p-3 rounded-full transition-colors duration-300" href="#">
<i class="w-6 h-6" data-lucide="add external server"></i>
</a>
</div>
</div>
<!-- Bio Content -->
<div class="space-y-6">
<div class="animate-slide-up">
<h3 class="text-2xl font-bold text-gaming-accent mb-4">سلام، من حامدم! 👋</h3>
<p class="text-gray-300 leading-relaxed persian-text" data-bind="bio.description">
              من حامد هستم، معروف به HamedBLAZE! از سال 2018 شروع به ساخت محتوای گیمینگ کردم و الان بیش از 127 هزار نفر 
              منو دنبال می‌کنند. تو کانال من پیدا می‌کنید: ویدیوهای گیمینگ مختلف، چالش‌های هیجان‌انگیز، 
              اداستان‌های ترسناک، ریویو بازی‌ها، و کلی محتوای باحال دیگه!
            </p>
</div>
<!-- Specialties -->
<div class="animate-slide-up" style="animation-delay: 0.2s">
<h4 class="text-xl font-bold mb-3 text-gaming-accent">🎯 تخصص‌ها</h4>
<div class="flex flex-wrap gap-2">
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">اکشن</span>
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">هورور</span>
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">مهیج</span>
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">ماجراجویی</span>
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">چالش</span>
<span class="bg-gaming-red px-3 py-1 rounded-full text-sm">استریم</span>
</div>
</div>
<!-- Gaming Setup -->
<div class="animate-slide-up" style="animation-delay: 0.4s">
<h4 class="text-xl font-bold mb-3 text-gaming-accent">⚡ تجهیزات من</h4>
<div class="space-y-2 text-gray-300">
<div class="flex justify-between">
<span>کارت گرافیک:</span>
<span class="text-gaming-accent font-medium" data-bind="setup.gpu">RTX 4080</span>
</div>
<div class="flex justify-between">
<span>پردازنده:</span>
<span class="text-gaming-accent font-medium" data-bind="setup.cpu">Intel i7-13700K</span>
</div>
<div class="flex justify-between">
<span>رم:</span>
<span class="text-gaming-accent font-medium" data-bind="setup.ram">32GB DDR5</span>
</div>
<div class="flex justify-between">
<span>میکروفون:</span>
<span class="text-gaming-accent font-medium" data-bind="setup.mic">Blue Yeti Pro</span>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- @END_COMPONENT: AboutSection -->
<!-- Admin Panel Modal (Hidden by default) -->
<!-- @COMPONENT: AdminPanel [content management, upload forms, settings] -->
<!-- @STATE: adminPanelOpen:boolean = false -->
<div class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden" id="admin-panel">
<div class="min-h-screen flex items-center justify-center p-4">
<div class="bg-gaming-surface border border-gaming-border rounded-2xl max-w-4xl w-full max-h-[90vh] overflow-y-auto">
<!-- Panel Header -->
<div class="flex items-center justify-between p-6 border-b border-gaming-border">
<h2 class="text-2xl font-bold text-gaming-accent">پنل مدیریت محتوا</h2>
<button class="text-gray-400 hover:text-white transition-colors" data-event="click:closeAdmin">
<i class="w-6 h-6" data-lucide="x"></i>
</button>
</div>
<!-- Panel Tabs -->
<div class="flex border-b border-gaming-border">

<button class="px-6 py-3 text-gray-400 hover:text-white transition-colors">مقالات</button>
<button class="px-6 py-3 text-gray-400 hover:text-white transition-colors">تنظیمات</button>
</div>
<!-- Panel Content -->
<div class="p-6">
<!-- Add New Video Form -->
<div class="grid md:grid-cols-2 gap-6">
<div>
<h3 class="text-xl font-bold mb-4 text-gaming-accent">افزودن ویدیو جدید</h3>
<form class="space-y-4" data-implementation="Handle video upload and metadata" onsubmit="return validateAntiSpam(event, this)">

    <!-- Anti-spam hidden fields: honeypot and timestamp -->
    <input type="text" name="website" value="" tabindex="-1" autocomplete="off" style="position:absolute;left:-9999px;top:auto;opacity:0;" />
    <input type="hidden" name="form_ts" value="" />
<div>
<label class="block text-sm font-medium mb-2">عنوان ویدیو</label>
<input class="w-full bg-gaming-dark border border-gaming-border rounded-lg px-4 py-2 text-white focus:border-gaming-red focus:outline-none" placeholder="عنوان ویدیو را وارد کنید..." type="text"/>
</div>
<div>
<label class="block text-sm font-medium mb-2">توضیحات</label>
<textarea class="w-full bg-gaming-dark border border-gaming-border rounded-lg px-4 py-2 text-white focus:border-gaming-red focus:outline-none h-24" placeholder="توضیحات ویدیو..."></textarea>
</div>
<div>
<label class="block text-sm font-medium mb-2">تصویر شاخص</label>
<div class="border-2 border-dashed border-gaming-border rounded-lg p-6 text-center hover:border-gaming-red transition-colors cursor-pointer" data-implementation="Use FileUpload component here" data-mock-image="true">
<i class="w-8 h-8 mx-auto text-gray-400 mb-2" data-lucide="upload"></i>
<p class="text-gray-400">تصویر را اینجا بکشید یا کلیک کنید</p>
</div>
</div>
<div>
<label class="block text-sm font-medium mb-2">دسته‌بندی</label>
<select class="w-full bg-gaming-dark border border-gaming-border rounded-lg px-4 py-2 text-white focus:border-gaming-red focus:outline-none">
<option>گیمینگ</option>
<option>چالش</option>
<option>ترسناک</option>
<option>مسابقه</option>
</select>
</div>

</form>
</div>
<!-- Recent Videos Management -->
<div>
<h3 class="text-xl font-bold mb-4 text-gaming-accent">مدیریت ویدیوها</h3>
<div class="space-y-3">
<!-- @MAP: adminVideos.map(video => ( -->
<div class="bg-gaming-dark rounded-lg p-4 flex items-center gap-4" data-mock="true">
<div class="w-16 h-12 bg-gaming-border rounded overflow-hidden">
<!-- Gaming video thumbnail for admin panel -->
<img alt="Video thumbnail" class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=100&amp;h=75"/>
</div>
<div class="flex-1">
<h4 class="font-medium" data-bind="video.title">بازی اکشن جدید</h4>
<p class="text-sm text-gray-400" data-bind="video.stats">23K بازدید • 3 روز پیش</p>
</div>
<div class="flex gap-2">
<button class="text-gaming-accent hover:text-gaming-red">
<i class="w-4 h-4" data-lucide="edit"></i>
</button>
<button class="text-red-500 hover:text-red-400">
<i class="w-4 h-4" data-lucide="trash-2"></i>
</button>
</div>
</div>
<!-- @END_MAP )) -->
<div class="bg-gaming-dark rounded-lg p-4 flex items-center gap-4" data-mock="true">
<div class="w-16 h-12 bg-gaming-border rounded overflow-hidden">
<img alt="Video thumbnail" class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3&amp;auto=format&amp;fit=crop&amp;w=100&amp;h=75"/>
</div>
<div class="flex-1">
<h4 class="font-medium">چالش ترسناک</h4>
<p class="text-sm text-gray-400">67K بازدید • 1 هفته پیش</p>
</div>
<div class="flex gap-2">
<button class="text-gaming-accent hover:text-gaming-red">
<i class="w-4 h-4" data-lucide="edit"></i>
</button>
<button class="text-red-500 hover:text-red-400">
<i class="w-4 h-4" data-lucide="trash-2"></i>
</button>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- @END_COMPONENT: AdminPanel -->
<!-- Newsletter Section -->

<!-- Footer -->
<!-- @COMPONENT: Footer [links, social media, copyright] -->
<footer class="bg-gaming-surface border-t border-gaming-border py-12">
<div class="container mx-auto px-4">
<div class="grid md:grid-cols-4 gap-8 mb-8">
<!-- Brand Column -->
<div>
<h3 class="text-2xl font-bold text-gradient mb-4">HamedBLAZE</h3>
<p class="text-gray-400 persian-text leading-relaxed">
            بهترین محتوای گیمینگ، چالش‌های هیجان‌انگیز، و داستان‌های ترسناک رو اینجا پیدا می‌کنی!
          </p>
</div>
<!-- Quick Links -->
<div>
<h4 class="text-lg font-bold mb-4 text-gaming-accent">لینک‌های مفید</h4>
<ul class="space-y-2">
<li></li>
<li><a class="text-gray-400 hover:text-gaming-accent transition-colors" href="#about">درباره من</a></li>
</ul>
</div>
<!-- Categories -->
<div>
<h4 class="text-lg font-bold mb-4 text-gaming-accent">دسته‌بندی‌ها</h4>
<ul class="space-y-2">
<li><a class="text-gray-400 hover:text-gaming-accent transition-colors" href="#">گیمینگ</a></li>
<li><a class="text-gray-400 hover:text-gaming-accent transition-colors" href="#">چالش</a></li>
<li><a class="text-gray-400 hover:text-gaming-accent transition-colors" href="#">ترسناک</a></li>
<li><a class="text-gray-400 hover:text-gaming-accent transition-colors" href="#">ریویو</a></li>
</ul>
</div>
<!-- Social & Contact -->
<div>
<h4 class="text-lg font-bold mb-4 text-gaming-accent">دنبال کن</h4>
<div class="flex gap-3 mb-4">
<a href=https://youtube.com/@hamedblaze</a>
	
<a class="bg-gaming-dark hover:bg-gaming-red p-3 rounded-lg transition-colors" href="#">
<i class="w-5 h-5" data-lucide="youtube"></i>
</a>
<a href=https://Instagram.com/hamed_blaze92/</a>
	
<a class="bg-gaming-dark hover:bg-gaming-red p-3 rounded-lg transition-colors" href="#">
<i class="w-5 h-5" data-lucide="instagram"></i>
</a>
</div>
<div class="text-gray-400 text-sm">
<p>🎮 همه روزه آنلاین</p>
<p><a href="mailto:hamedblazeofficial@gmail.com">hamedblazeofficial@gmail.com</a></p>
</div>
</div>
</div>
<!-- Copyright -->
<div class="border-t border-gaming-border pt-8 text-center">

<g>
                                <path class="st0" d="M639.1,236.3c9.3-9.3,9.3-24.4,0-33.8L443.6,7c-9.3-9.3-24.4-9.3-33.8,0l-69.9,69.9c-9.3,9.3-24.4,9.3-33.8,0
		L236.2,7c-9.3-9.3-24.4-9.3-33.8,0L7,202.5c-9.3,9.3-9.3,24.4,0,33.8l69.9,69.9c9.3,9.3,9.3,24.4,0,33.8L7,409.9
		c-9.3,9.3-9.3,24.4,0,33.8l195.5,195.5c9.3,9.3,24.4,9.3,33.8,0l69.9-69.9c9.3-9.3,24.4-9.3,33.8,0l69.9,69.9
		c9.3,9.3,24.4,9.3,33.8,0l195.5-195.5c9.3-9.3,9.3-24.4,0-33.8L569.3,340c-9.3-9.3-9.3-24.4,0-33.8L639.1,236.3z M497.9,361.3
		c0,75-61.4,136.4-136.4,136.4h-76.7c-75,0-136.4-61.4-136.4-136.4v-76.7c0-75,61.4-136.4,136.4-136.4h76.7
		c75,0,136.4,61.4,136.4,136.4V361.3z"></path>
<a href="https://exaroton.com">
<img src=https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT8jaCY7J7VQVeLDVssS9feaksMGqZjm51AsA&s
                <div class="header-exaroton-link-right">
                    <div class="header-exaroton-link-text-main">
                        برای بازی کردن، فقط پرداخت کنید.                    </div>
                    <div class="header-exaroton-link-text-sub">
                        با سرور های قدرتمند و پر تقاضای ما.                    </div>
                </div>
            </div>
        </a>
    </div>
    </div>
</div>
</div>
<div class="border-t border-gaming-border pt-8 text-center">
<p class="text-gray-400 persian-text">
          © 2025 HamedBLAZE - تمامی حقوق محفوظ است | ساخته شده با ❤️ برای گیمرها
        </p>                         https://exaroton.com
</footer>
<!-- @END_COMPONENT: Footer -->
<script>
    // Initialize Lucide icons
    (function() {
      if (typeof lucide !== 'undefined') {
        lucide.createIcons();
      }
    })();

    // Scroll animations
    (function() {
      const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
      };

      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
          }
        });
      }, observerOptions);

      // Observe all elements with slide-up animation
      document.querySelectorAll('.animate-slide-up').forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(30px)';
        el.style.transition = 'opacity 0.8s ease-out, transform 0.8s ease-out';
        observer.observe(el);
      });
    })();

    // Mobile menu toggle
    (function() {
      const mobileMenuButton = document.querySelector('[data-event="click:toggleMobileMenu"]');
      const mobileMenu = document.getElementById('mobile-menu');
      
      if (mobileMenuButton && mobileMenu) {
        mobileMenuButton.addEventListener('click', function() {
          mobileMenu.classList.toggle('hidden');
          // TODO: Implement proper mobile menu state management
        });
      }
    })();

    // Admin panel toggle
    (function() {
      const adminButtons = document.querySelectorAll('[data-event="click:toggleAdmin"]');
      const adminPanel = document.getElementById('admin-panel');
      const closeButton = document.querySelector('[data-event="click:closeAdmin"]');
      
      adminButtons.forEach(button => {
        button.addEventListener('click', function() {
          if (adminPanel) {
            adminPanel.classList.remove('hidden');
            document.body.style.overflow = 'hidden';
            // TODO: Implement authentication check before showing admin panel
          }
        });
      });
      
      if (closeButton && adminPanel) {
        closeButton.addEventListener('click', function() {
          adminPanel.classList.add('hidden');
          document.body.style.overflow = 'auto';
        });
      }
      
      // Close admin panel on backdrop click
      if (adminPanel) {
        adminPanel.addEventListener('click', function(e) {
          if (e.target === adminPanel) {
            adminPanel.classList.add('hidden');
            document.body.style.overflow = 'auto';
          }
        });
      }
    })();

    // Smooth scrolling for anchor links
    (function() {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          e.preventDefault();
          const target = document.querySelector(this.getAttribute('href'));
          if (target) {
            target.scrollIntoView({
              behavior: 'smooth',
              block: 'start'
            });
          }
        });
      });
    })();

    // TODO: Implement the following functionality:
    // - Video upload and management system
    // - Blog post creation and editing
    // - User authentication and authorization
    // - Content filtering and search
    // - Real-time statistics updates
    // - Newsletter subscription handling
    // - Social media integration
    // - Comment system for videos and blog posts
    // - Like/dislike functionality
    // - Share functionality
    // - Push notifications for new content
  </script>

<!-- reCAPTCHA v2 (checkbox) - add your site key below. Replace 'YOUR_RECAPTCHA_SITE_KEY' with your real key. -->
<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<!-- Place this where you want the checkbox inside each form (example inserted by JS if .recaptcha-placeholder found): -->
<!-- <div class="g-recaptcha recaptcha-placeholder" data-sitekey="YOUR_RECAPTCHA_SITE_KEY"></div> -->

<script>
// Anti-spam client-side helpers
(function(){
  function nowSecs(){ return Math.floor(Date.now()/1000); }

  // On DOM ready, set form timestamps and insert recaptcha placeholders where class present
  document.addEventListener('DOMContentLoaded', function(){
    var forms = document.getElementsByTagName('form');
    for(var i=0;i<forms.length;i++){
      var f = forms[i];
      var ts = f.querySelector('input[name="form_ts"]');
      if(ts) ts.value = nowSecs();
      // If form contains an element with class recaptcha-placeholder, ensure it will render the widget server-side by having data-sitekey set.
      var ph = f.querySelector('.recaptcha-placeholder');
      if(ph && !ph.getAttribute('data-sitekey')){
        // Insert a visible hint for developer to replace site key
        ph.innerHTML = '<p style="color:#c00">[Replace data-sitekey with your reCAPTCHA site key]</p>';
      }
    }
  });

  // Validation function called onsubmit: returns true to proceed, false to prevent submit
  window.validateAntiSpam = function(e, form){
    try{
      // 1) Honeypot must be empty
      var hp = form.querySelector('input[name="website"]');
      if(hp && hp.value.trim() !== ''){
        // likely bot
        if(e && e.preventDefault) e.preventDefault();
        return false;
      }
      // 2) Minimum time check (at least 3 seconds since page load)
      var ts = form.querySelector('input[name="form_ts"]');
      if(ts){
        var then = parseInt(ts.value) || 0;
        var diff = Math.floor(Date.now()/1000) - then;
        if(diff < 3){
          // too fast - possible bot
          if(e && e.preventDefault) e.preventDefault();
          return false;
        }
      }
      // 3) If form has a reCAPTCHA widget, ensure user completed it
      // For reCAPTCHA v2, grecaptcha.getResponse(widgetId) returns empty string if not completed.
      if(window.grecaptcha){
        // try to find any .g-recaptcha in the form
        var rec = form.querySelector('.g-recaptcha');
        if(rec){
          // attempt to read the response
          try{
            var response = grecaptcha.getResponse();
            if(!response || response.length === 0){
              if(e && e.preventDefault) e.preventDefault();
              alert('لطفاً کپچا را تکمیل کنید.');
              return false;
            }
            // optionally, append response to form as hidden input so server can verify
            var existing = form.querySelector('input[name="g-recaptcha-response"]');
            if(!existing){
              var inp = document.createElement('input');
              inp.type = 'hidden';
              inp.name = 'g-recaptcha-response';
              inp.value = response;
              form.appendChild(inp);
            }
          }catch(err){
            // ignore grecaptcha errors (server-side should still verify)
          }
        }
      }
      // Passed basic checks
      return true;
    }catch(err){
      // On error, be permissive to avoid locking out real users; server-side should be authoritative.
      console.error('Anti-spam validation error:', err);
      return true;
    }
  };
})();
</script>


<!-- Admin panel password protection (client-side) -->
<style>
/* Admin lock modal styles */
#adminLockModal { position: fixed; inset: 0; display: flex; align-items: center; justify-content: center; background: rgba(0,0,0,0.6); z-index: 99999; }
#adminLockModal .card { background: white; padding: 20px; border-radius: 8px; width: 320px; max-width: 90%; box-shadow: 0 10px 30px rgba(0,0,0,0.2); text-align: center; }
#adminLockModal input { width: 100%; padding: 10px; margin-top: 8px; margin-bottom: 12px; }
#adminLockModal button { padding: 10px 14px; border-radius: 6px; cursor: pointer; }
#adminLoginBtn { position: fixed; top: 12px; right: 12px; z-index: 99998; background:#111; color:#fff; padding:8px 10px; border-radius:6px; cursor:pointer; font-size:14px; }
.admin-locked-overlay { position: absolute; inset: 0; background: rgba(255,255,255,0.95); display:flex; align-items:center; justify-content:center; z-index:99990; }
.lock-message { font-size:14px; color:#333; }
.lock-desc { font-size:13px; color:#666; margin-top:8px; }
.small-muted { font-size:12px; color:#999; margin-top:6px; }
</style>

<!-- Admin Login Button (visible always to open login modal) -->
<!-- Modal (inserted/hidden via JS) -->
<div id="adminLockModal" style="display:none;" aria-hidden="true">
  <div class="card" role="dialog" aria-modal="true" aria-labelledby="adminLockTitle">
    <h3 id="adminLockTitle">ورود به پنل مدیریت</h3>
    <p class="small-muted">برای دسترسی به پنل مدیریت، رمز عبور را وارد کنید.</p>
    <input id="adminPasswordInput" type="password" placeholder="رمز عبور" autocomplete="current-password" />
    <div style="display:flex;gap:8px;justify-content:center;">
      <button id="adminUnlockBtn">ورود</button>
      <button id="adminCancelBtn">انصراف</button>
    </div>
    <p class="small-muted" id="adminLockInfo" style="margin-top:10px;"></p>
  </div>
</div>

<script>
/*
  Client-side admin protection (convenience layer).
  IMPORTANT: Client-side protection is not a substitute for server-side authentication.
  This script:
   - Finds likely admin panel elements (id/class/text containing "admin" or "پنل مدیریت") and overlays them until unlocked.
   - Provides a modal to enter the admin password. Password check is done by comparing SHA-256 hashes (so the plain password is not embedded).
   - Implements local lockout after 3 failed attempts for 1 hour (stored in localStorage).
   - Stores a session token in localStorage when authenticated (expires after 1 hour).
  
  How to set password (recommended):
   - Replace storedHash variable with the SHA-256 hex of your desired password.
   - Or call setAdminPassword() in the console to set it interactively (it will store hash in localStorage).
   
  To set hash from a password in JS console (once):
    window.setAdminPassword('your-desired-password');
  To clear stored password hash (console):
    localStorage.removeItem('admin_password_hash');
  To logout:
    localStorage.removeItem('admin_auth');
*/

// Utilities: SHA-256 hashing using SubtleCrypto
async function sha256Hex(str) {
  const enc = new TextEncoder();
  const buf = await crypto.subtle.digest('SHA-256', enc.encode(str));
  const hex = Array.from(new Uint8Array(buf)).map(b => b.toString(16).padStart(2,'0')).join('');
  return hex;
}

// Config: You may optionally hardcode a hash here (hex string).
let storedHash = localStorage.getItem('admin_password_hash') || ''; // if empty, user can set via console

// Lockout config
const MAX_FAILED = 3;
const LOCK_DURATION_SEC = 60*60; // 1 hour

// Find candidate admin elements to protect
function findAdminElements() {
  const candidates = new Set();
  // by id/class containing 'admin'
  document.querySelectorAll('[id], [class]').forEach(el => {
    const id = (el.id || '').toLowerCase();
    const cls = (el.className || '').toLowerCase();
    if (id.includes('admin') || cls.includes('admin') ) candidates.add(el);
  });
  // by headings/text that contain 'پنل مدیریت' or 'مدیریت' (fuzzy)
  const textEls = Array.from(document.querySelectorAll('h1,h2,h3,section,div,p,nav,aside,header')).filter(el => {
    const t = (el.textContent || '').toLowerCase();
    return t.includes('پنل مدیریت') || t.includes('پنل') && t.includes('مدیریت');
  });
  textEls.forEach(el => {
    // climb up to a likely container
    let container = el.closest('section,div,main') || el.parentElement;
    if(container) candidates.add(container);
  });
  return Array.from(candidates);
}

// Overlay a locked layer over an element
function overlayElement(el) {
  if(!el) return null;
  // ensure position relative
  const computed = window.getComputedStyle(el);
  if(computed.position === 'static') el.style.position = 'relative';
  const ov = document.createElement('div');
  ov.className = 'admin-locked-overlay';
  ov.innerHTML = '<div><div class="lock-message">دسترسی به این بخش نیازمند ورود است.</div><div class="lock-desc">برای دسترسی، لطفاً وارد پنل شوید.</div></div>';
  ov.setAttribute('data-admin-locked','true');
  el.insertBefore(ov, el.firstChild);
  return ov;
}

// Remove overlays
function removeOverlays() {
  document.querySelectorAll('.admin-locked-overlay').forEach(o => o.remove());
}

// Check lockout state
function isLockedOut() {
  const info = JSON.parse(localStorage.getItem('admin_lock_info') || '{}');
  if(info.lockUntil && Date.now() < info.lockUntil) return {locked:true, until: info.lockUntil};
  return {locked:false};
}

// Register failed attempt
function registerFailedAttempt() {
  const info = JSON.parse(localStorage.getItem('admin_lock_info') || '{}');
  info.failed = (info.failed || 0) + 1;
  if(info.failed >= MAX_FAILED) {
    info.lockUntil = Date.now() + LOCK_DURATION_SEC*1000;
    info.failed = 0; // reset counter after lock
  }
  localStorage.setItem('admin_lock_info', JSON.stringify(info));
}

// Reset failed attempts
function resetFailedAttempts() {
  localStorage.removeItem('admin_lock_info');
}

// Session handling
function setAuthSession() {
  const sess = { token: Math.random().toString(36).slice(2), expires: Date.now() + 60*60*1000 }; // 1 hour
  localStorage.setItem('admin_auth', JSON.stringify(sess));
}
function isAuthenticated() {
  try {
    const sess = JSON.parse(localStorage.getItem('admin_auth') || '{}');
    return sess.token && Date.now() < sess.expires;
  } catch(e) { return false; }
}
function clearAuth() { localStorage.removeItem('admin_auth'); }

// Expose helper to set password (stores hash in localStorage)
window.setAdminPassword = async function(password) {
  const h = await sha256Hex(password);
  localStorage.setItem('admin_password_hash', h);
  storedHash = h;
  console.info('Admin password hash set. Keep your password safe.');
  return h;
};

// Main: apply overlays to admin elements
function protectAdminAreas() {
  if(isAuthenticated()) {
    removeOverlays();
    return;
  }
  const els = findAdminElements();
  if(els.length === 0) {
    // nothing obvious to protect; do not block whole site automatically.
    // leave the explicit Admin Login button for manual use.
    return;
  }
  // add overlays
  els.forEach(el => {
    if(!el.querySelector('.admin-locked-overlay')) overlayElement(el);
  });
}

// Show modal
function showAdminModal(msg) {
  const modal = document.getElementById('adminLockModal');
  const info = document.getElementById('adminLockInfo');
  if(msg) info.textContent = msg; else info.textContent = '';
  modal.style.display = 'flex';
  modal.setAttribute('aria-hidden','false');
  document.getElementById('adminPasswordInput').focus();
}

// Hide modal
function hideAdminModal() {
  const modal = document.getElementById('adminLockModal');
  modal.style.display = 'none';
  modal.setAttribute('aria-hidden','true');
  document.getElementById('adminPasswordInput').value = '';
}

// Attempt unlock with password
async function attemptUnlock(password) {
  // check lockout
  const lock = isLockedOut();
  if(lock.locked) {
    const rem = Math.ceil((lock.until - Date.now())/1000);
    showAdminModal('حساب قفل شده. لطفاً بعد از ' + rem + ' ثانیه تلاش کنید.');
    return false;
  }
  if(!password || password.length === 0) {
    showAdminModal('لطفاً رمز را وارد کنید.');
    return false;
  }
  // if storedHash is empty, allow setting password interactively (first-run)
  if(!storedHash) {
    // set password
    const h = await sha256Hex(password);
    localStorage.setItem('admin_password_hash', h);
    storedHash = h;
    setAuthSession();
    removeOverlays();
    hideAdminModal();
    alert('رمز در همین مرورگر ذخیره شد. برای امنیت، توصیه می‌شود از احراز هویت سمت سرور استفاده کنید.');
    return true;
  }
  const ph = await sha256Hex(password);
  if(ph === storedHash) {
    // success
    setAuthSession();
    resetFailedAttempts();
    removeOverlays();
    hideAdminModal();
    return true;
  } else {
    registerFailedAttempt();
    const info = isLockedOut();
    if(info.locked) {
      showAdminModal('تعداد تلاش‌های ناموفق زیاد شد — حساب برای 1 ساعت قفل شده است.');
    } else {
      showAdminModal('رمز اشتباه است. دوباره تلاش کنید.');
    }
    return false;
  }
}

// Wire up modal buttons
document.addEventListener('DOMContentLoaded', function(){
  // Protect areas on load
  protectAdminAreas();

  // If already authenticated, nothing to do
  if(isAuthenticated()) return;

  const loginBtn = document.getElementById('adminLoginBtn');
  loginBtn.addEventListener('click', function(){ showAdminModal(); });

  const unlockBtn = document.getElementById('adminUnlockBtn');
  unlockBtn.addEventListener('click', function(){
    const pw = document.getElementById('adminPasswordInput').value || '';
    attemptUnlock(pw);
  });

  const cancelBtn = document.getElementById('adminCancelBtn');
  cancelBtn.addEventListener('click', function(){ hideAdminModal(); });

  // allow Enter key
  document.getElementById('adminPasswordInput').addEventListener('keydown', function(e){
    if(e.key === 'Enter') {
      e.preventDefault();
      attemptUnlock(e.target.value || '');
    }
  });

  // If admin areas exist, auto-show modal to prompt for login
  const adminEls = findAdminElements();
  if(adminEls.length > 0) showAdminModal();
});
</script>
<!-- End admin protection snippet -->

</body>
</html>
