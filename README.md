<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>زوود کوک | فروشگاه آنلاین غذاهای ایرانی و فست فود</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#FF6B6B',
                        secondary: '#4ECDC4',
                        accent: '#FFE66D',
                        dark: '#292F36',
                        light: '#F7FFF7',
                    },
                    fontFamily: {
                        sans: ['Vazirmatn', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@100;200;300;400;500;600;700;800;900&display=swap');
        
        body {
            font-family: 'Vazirmatn', sans-serif;
            background-color: #F7FFF7;
        }
        
        .iranian-pattern {
            background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23FF6B6B' fill-opacity='0.1'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }
        
        .food-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .nav-link::after {
            content: '';
            display: block;
            width: 0;
            height: 2px;
            background: #FF6B6B;
            transition: width .3s;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .cart-badge {
            position: absolute;
            top: -5px;
            right: -5px;
            width: 20px;
            height: 20px;
            background: #FF6B6B;
            color: white;
            border-radius: 50%;
            font-size: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    </style>
</head>
<body class="iranian-pattern">
    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2 space-x-reverse">
                <div class="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
                    <i class="fas fa-utensils text-white text-xl"></i>
                </div>
                <h1 class="text-2xl font-bold text-dark">زوود کوک</h1>
            </div>
            
            <nav class="hidden md:flex space-x-8 space-x-reverse">
                <a href="#home" class="nav-link text-dark font-medium hover:text-primary transition">صفحه اصلی</a>
                <a href="#menu" class="nav-link text-dark font-medium hover:text-primary transition">منو غذاها</a>
                <a href="#about" class="nav-link text-dark font-medium hover:text-primary transition">درباره ما</a>
                <a href="#contact" class="nav-link text-dark font-medium hover:text-primary transition">تماس با ما</a>
            </nav>
            
            <div class="flex items-center space-x-4 space-x-reverse">
                <div class="relative">
                    <button id="cart-btn" class="text-dark hover:text-primary transition">
                        <i class="fas fa-shopping-cart text-xl"></i>
                        <span class="cart-badge hidden">0</span>
                    </button>
                </div>
                <button id="login-btn" class="bg-primary text-white px-4 py-2 rounded-full hover:bg-opacity-90 transition">
                    ورود به پنل مدیریت
                </button>
                <button id="mobile-menu-btn" class="md:hidden text-dark">
                    <i class="fas fa-bars text-xl"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white py-2 px-4 shadow-lg">
            <a href="#home" class="block py-2 text-dark hover:text-primary transition">صفحه اصلی</a>
            <a href="#menu" class="block py-2 text-dark hover:text-primary transition">منو غذاها</a>
            <a href="#about" class="block py-2 text-dark hover:text-primary transition">درباره ما</a>
            <a href="#contact" class="block py-2 text-dark hover:text-primary transition">تماس با ما</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="py-16">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-10 md:mb-0">
                <h2 class="text-4xl md:text-5xl font-bold text-dark mb-4">غذای خوشمزه، تحویل سریع</h2>
                <p class="text-lg text-gray-600 mb-6">با زوود کوک، بهترین غذاهای ایرانی و فست فود را درب منزل تحویل بگیرید. ما کیفیت و طعم واقعی را به شما هدیه می دهیم.</p>
                <div class="flex space-x-4 space-x-reverse">
                    <a href="#menu" class="bg-primary text-white px-6 py-3 rounded-full hover:bg-opacity-90 transition">مشاهده منو</a>
                    <a href="#about" class="border-2 border-primary text-primary px-6 py-3 rounded-full hover:bg-primary hover:text-white transition">درباره ما</a>
                </div>
            </div>
            <div class="md:w-1/2 relative">
                <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80" alt="غذای ایرانی" class="w-full rounded-2xl shadow-xl">
                <div class="absolute -bottom-5 -right-5 bg-accent p-4 rounded-2xl shadow-lg">
                    <p class="font-bold text-dark">از ۵۰٪ تخفیف ویژه اولین خرید بهره مند شوید!</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Categories -->
    <section class="py-12 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-dark mb-12">دسته بندی غذاها</h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <div class="bg-light rounded-2xl p-6 text-center hover:shadow-md transition cursor-pointer">
                    <div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-hamburger text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-bold text-dark mb-2">فست فود</h3>
                    <p class="text-gray-600 text-sm">برگر، پیتزا، ساندویچ و ...</p>
                </div>
                <div class="bg-light rounded-2xl p-6 text-center hover:shadow-md transition cursor-pointer">
                    <div class="w-16 h-16 bg-secondary bg-opacity-10 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-home text-secondary text-2xl"></i>
                    </div>
                    <h3 class="font-bold text-dark mb-2">غذای خانگی</h3>
                    <p class="text-gray-600 text-sm">غذاهای گرم و تازه خانگی</p>
                </div>
                <div class="bg-light rounded-2xl p-6 text-center hover:shadow-md transition cursor-pointer">
                    <div class="w-16 h-16 bg-accent bg-opacity-10 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-utensils text-accent text-2xl"></i>
                    </div>
                    <h3 class="font-bold text-dark mb-2">غذای ایرانی</h3>
                    <p class="text-gray-600 text-sm">چلوکباب، قورمه سبزی و ...</p>
                </div>
                <div class="bg-light rounded-2xl p-6 text-center hover:shadow-md transition cursor-pointer">
                    <div class="w-16 h-16 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-blender text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-bold text-dark mb-2">نیمه آماده</h3>
                    <p class="text-gray-600 text-sm">آماده پخت در منزل</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu -->
    <section id="menu" class="py-12 bg-light">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-dark mb-6">منوی غذاها</h2>
            <p class="text-center text-gray-600 mb-12">غذاهای محبوب ما را امتحان کنید</p>
            
            <div class="flex justify-center mb-8">
                <div class="inline-flex rounded-full bg-white p-1 shadow">
                    <button class="category-btn active px-4 py-2 rounded-full bg-primary text-white" data-category="all">همه</button>
                    <button class="category-btn px-4 py-2 rounded-full hover:bg-gray-100 transition" data-category="fastfood">فست فود</button>
                    <button class="category-btn px-4 py-2 rounded-full hover:bg-gray-100 transition" data-category="homemade">خانگی</button>
                    <button class="category-btn px-4 py-2 rounded-full hover:bg-gray-100 transition" data-category="iranian">ایرانی</button>
                    <button class="category-btn px-4 py-2 rounded-full hover:bg-gray-100 transition" data-category="semi">نیمه آماده</button>
                </div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="food-items-container">
                <!-- Food items will be added here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-10">
                    <h2 class="text-3xl font-bold text-dark mb-6">درباره زوود کوک</h2>
                    <p class="text-gray-600 mb-4">زوود کوک در سال ۱۴۰۰ با هدف ارائه غذاهای باکیفیت و خوشمزه به مشتریان عزیز تأسیس شد. ما معتقدیم که غذای خوب می‌تواند روز هر کسی را بهتر کند.</p>
                    <p class="text-gray-600 mb-6">تیم ما متشکل از سرآشپزهای حرفه‌ای و با تجربه است که با عشق و دقت غذاهای ما را آماده می‌کنند. ما از بهترین مواد اولیه استفاده می‌کنیم تا رضایت شما را جلب نماییم.</p>
                    <div class="flex space-x-4 space-x-reverse">
                        <div class="bg-primary bg-opacity-10 p-4 rounded-lg">
                            <h3 class="font-bold text-primary">۱۰۰+</h3>
                            <p class="text-gray-600">انواع غذا</p>
                        </div>
                        <div class="bg-secondary bg-opacity-10 p-4 rounded-lg">
                            <h3 class="font-bold text-secondary">۵۰۰۰+</h3>
                            <p class="text-gray-600">مشتری راضی</p>
                        </div>
                        <div class="bg-accent bg-opacity-10 p-4 rounded-lg">
                            <h3 class="font-bold text-accent">۳۰+</h3>
                            <p class="text-gray-600">شعبه فعال</p>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2 relative">
                    <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="آشپزهای زوود کوک" class="w-full rounded-2xl shadow-xl">
                    <div class="absolute -bottom-5 -left-5 bg-white p-4 rounded-2xl shadow-lg border border-gray-100">
                        <div class="flex items-center space-x-3 space-x-reverse">
                            <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center">
                                <i class="fas fa-award text-white text-xl"></i>
                            </div>
                            <div>
                                <p class="font-bold text-dark">بهترین رستوران آنلاین ۱۴۰۱</p>
                                <p class="text-sm text-gray-600">از دید مشتریان</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="py-16 bg-light">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-dark mb-6">نظرات مشتریان</h2>
            <p class="text-center text-gray-600 mb-12">آنچه مشتریان ما می‌گویند</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 rounded-2xl shadow-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-gray-200 overflow-hidden">
                            <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="مشتری" class="w-full h-full object-cover">
                        </div>
                        <div class="mr-3">
                            <h4 class="font-bold text-dark">نازنین محمدی</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">غذاهای زوود کوک واقعاً عالی هستند. همیشه تازه و داغ به دستم می‌رسند. مخصوصاً چلوکبابشان فوق‌العاده است!</p>
                </div>
                <div class="bg-white p-6 rounded-2xl shadow-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-gray-200 overflow-hidden">
                            <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="مشتری" class="w-full h-full object-cover">
                        </div>
                        <div class="mr-3">
                            <h4 class="font-bold text-dark">امیر حسینی</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">سرعت تحویل غذاها واقعاً قابل تقدیره. چند بار که سفارش دادم همیشه زودتر از موعد مقرر رسید.</p>
                </div>
                <div class="bg-white p-6 rounded-2xl shadow-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-gray-200 overflow-hidden">
                            <img src="https://randomuser.me/api/portraits/women/63.jpg" alt="مشتری" class="w-full h-full object-cover">
                        </div>
                        <div class="mr-3">
                            <h4 class="font-bold text-dark">سارا نوروزی</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">غذاهای نیمه آماده‌شان عالی هستند. کیفیت مواد اولیه خیلی خوبه و طعم واقعی غذاهای ایرانی رو دارن.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-dark mb-6">تماس با ما</h2>
            <p class="text-center text-gray-600 mb-12">سوال یا پیشنهادی دارید؟ با ما در میان بگذارید</p>
            
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-10">
                    <form class="space-y-6">
                        <div>
                            <label for="name" class="block text-gray-700 mb-2">نام شما</label>
                            <input type="text" id="name" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="نام خود را وارد کنید">
                        </div>
                        <div>
                            <label for="email" class="block text-gray-700 mb-2">ایمیل</label>
                            <input type="email" id="email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="ایمیل خود را وارد کنید">
                        </div>
                        <div>
                            <label for="message" class="block text-gray-700 mb-2">پیام شما</label>
                            <textarea id="message" rows="5" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="پیام خود را بنویسید..."></textarea>
                        </div>
                        <button type="submit" class="bg-primary text-white px-6 py-3 rounded-lg hover:bg-opacity-90 transition w-full">ارسال پیام</button>
                    </form>
                </div>
                <div class="md:w-1/2">
                    <div class="bg-light p-8 rounded-2xl h-full">
                        <h3 class="text-xl font-bold text-dark mb-6">اطلاعات تماس</h3>
                        <div class="space-y-6">
                            <div class="flex items-start space-x-4 space-x-reverse">
                                <div class="w-10 h-10 bg-primary bg-opacity-10 rounded-full flex items-center justify-center mt-1">
                                    <i class="fas fa-map-marker-alt text-primary"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-dark mb-1">آدرس</h4>
                                    <p class="text-gray-600">تهران، خیابان ولیعصر، کوچه فلان، پلاک ۱۲</p>
                                </div>
                            </div>
                            <div class="flex items-start space-x-4 space-x-reverse">
                                <div class="w-10 h-10 bg-secondary bg-opacity-10 rounded-full flex items-center justify-center mt-1">
                                    <i class="fas fa-phone-alt text-secondary"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-dark mb-1">تلفن</h4>
                                    <p class="text-gray-600">۰۲۱-۱۲۳۴۵۶۷۸</p>
                                    <p class="text-gray-600">۰۹۱۲۳۴۵۶۷۸۹</p>
                                </div>
                            </div>
                            <div class="flex items-start space-x-4 space-x-reverse">
                                <div class="w-10 h-10 bg-accent bg-opacity-10 rounded-full flex items-center justify-center mt-1">
                                    <i class="fas fa-envelope text-accent"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-dark mb-1">ایمیل</h4>
                                    <p class="text-gray-600">info@zooodcook.ir</p>
                                    <p class="text-gray-600">support@zooodcook.ir</p>
                                </div>
                            </div>
                        </div>
                        <div class="mt-8">
                            <h4 class="font-bold text-dark mb-4">ما را در شبکه‌های اجتماعی دنبال کنید</h4>
                            <div class="flex space-x-4 space-x-reverse">
                                <a href="#" class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center text-gray-600 hover:bg-primary hover:text-white transition">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center text-gray-600 hover:bg-primary hover:text-white transition">
                                    <i class="fab fa-telegram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center text-gray-600 hover:bg-primary hover:text-white transition">
                                    <i class="fab fa-whatsapp"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center text-gray-600 hover:bg-primary hover:text-white transition">
                                    <i class="fab fa-twitter"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center space-x-2 space-x-reverse mb-4">
                        <div class="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
                            <i class="fas fa-utensils text-white text-xl"></i>
                        </div>
                        <h3 class="text-xl font-bold">زوود کوک</h3>
                    </div>
                    <p class="text-gray-300 mb-4">ارائه دهنده بهترین غذاهای ایرانی و فست فود با کیفیت عالی و طعم بی‌نظیر</p>
                    <div class="flex space-x-4 space-x-reverse">
                        <a href="#" class="text-gray-300 hover:text-white transition"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-300 hover:text-white transition"><i class="fab fa-telegram"></i></a>
                        <a href="#" class="text-gray-300 hover:text-white transition"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">لینک‌های مفید</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white transition">صفحه اصلی</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">منو غذاها</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">درباره ما</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">تماس با ما</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">وبلاگ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">خدمات مشتریان</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white transition">سوالات متداول</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">شرایط و ضوابط</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">حریم خصوصی</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">روش‌های پرداخت</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition">پیگیری سفارش</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">خبرنامه</h4>
                    <p class="text-gray-300 mb-4">برای دریافت جدیدترین تخفیف‌ها و پیشنهادهای ویژه در خبرنامه ما عضو شوید</p>
                    <form class="flex">
                        <input type="email" placeholder="ایمیل شما" class="px-4 py-2 rounded-r-lg focus:outline-none text-dark w-full">
                        <button type="submit" class="bg-primary px-4 py-2 rounded-l-lg hover:bg-opacity-90 transition">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </form>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
                <p>© ۱۴۰۲ تمام حقوق برای زوود کوک محفوظ است.</p>
            </div>
        </div>
    </footer>

    <!-- Shopping Cart Sidebar -->
    <div id="cart-sidebar" class="fixed top-0 right-0 h-full w-full md:w-96 bg-white shadow-xl z-50 transform translate-x-full transition-transform duration-300 overflow-y-auto">
        <div class="p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-dark">سبد خرید</h3>
                <button id="close-cart" class="text-gray-500 hover:text-dark">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <div id="cart-items" class="space-y-4 mb-6">
                <!-- Cart items will be added here by JavaScript -->
                <div class="text-center py-8 text-gray-500" id="empty-cart-message">
                    <i class="fas fa-shopping-cart text-4xl mb-4"></i>
                    <p>سبد خرید شما خالی است</p>
                </div>
            </div>
            
            <div class="border-t border-gray-200 pt-4 mb-6">
                <div class="flex justify-between mb-2">
                    <span class="text-gray-600">جمع کل:</span>
                    <span class="font-bold" id="cart-total">۰ تومان</span>
                </div>
                <div class="flex justify-between mb-2">
                    <span class="text-gray-600">تخفیف:</span>
                    <span class="font-bold text-primary" id="cart-discount">۰ تومان</span>
                </div>
                <div class="flex justify-between text-lg font-bold mt-4">
                    <span>مبلغ قابل پرداخت:</span>
                    <span id="cart-final-total">۰ تومان</span>
                </div>
            </div>
            
            <button id="checkout-btn" class="bg-primary text-white w-full py-3 rounded-lg hover:bg-opacity-90 transition disabled:opacity-50 disabled:cursor-not-allowed" disabled>
                پرداخت و تکمیل سفارش
            </button>
        </div>
    </div>
    <div id="cart-overlay" class="fixed inset-0 bg-black bg-opacity-50 z-40 hidden"></div>

    <!-- Admin Login Modal -->
    <div id="admin-modal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white rounded-2xl shadow-xl w-full max-w-md mx-4">
            <div class="p-6">
                <div class="flex justify-between items-center mb-6">
                    <h3 class="text-xl font-bold text-dark">ورود به پنل مدیریت</h3>
                    <button id="close-admin-modal" class="text-gray-500 hover:text-dark">
                        <i class="fas fa-times text-xl"></i>
                    </button>
                </div>
                
                <div id="login-step">
                    <div class="mb-4">
                        <label for="admin-email" class="block text-gray-700 mb-2">ایمیل مدیریت</label>
                        <input type="email" id="admin-email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="ایمیل خود را وارد کنید">
                    </div>
                    <button id="send-code-btn" class="bg-primary text-white w-full py-3 rounded-lg hover:bg-opacity-90 transition">
                        ارسال کد تأیید
                    </button>
                </div>
                
                <div id="verification-step" class="hidden">
                    <p class="text-gray-600 mb-4">کد تأیید به ایمیل <span id="admin-email-display"></span> ارسال شد. لطفاً کد را وارد کنید.</p>
                    <div class="mb-4">
                        <label for="verification-code" class="block text-gray-700 mb-2">کد تأیید</label>
                        <input type="text" id="verification-code" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="کد ۶ رقمی">
                    </div>
                    <button id="verify-code-btn" class="bg-primary text-white w-full py-3 rounded-lg hover:bg-opacity-90 transition">
                        تأیید و ورود
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Admin Panel -->
    <div id="admin-panel" class="fixed inset-0 bg-gray-100 z-50 hidden overflow-y-auto">
        <div class="min-h-screen">
            <!-- Admin Header -->
            <header class="bg-dark text-white shadow-md">
                <div class="container mx-auto px-4 py-3 flex justify-between items-center">
                    <div class="flex items-center space-x-2 space-x-reverse">
                        <div class="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
                            <i class="fas fa-user-shield text-white text-xl"></i>
                        </div>
                        <h1 class="text-xl font-bold">پنل مدیریت زوود کوک</h1>
                    </div>
                    
                    <div class="flex items-center space-x-4 space-x-reverse">
                        <button id="admin-logout" class="text-white hover:text-accent transition">
                            <i class="fas fa-sign-out-alt text-xl"></i>
                        </button>
                    </div>
                </div>
            </header>
            
            <!-- Admin Content -->
            <div class="container mx-auto px-4 py-8">
                <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
                    <div class="bg-white rounded-2xl shadow p-6">
                        <div class="flex items-center justify-between">
                            <div>
                                <p class="text-gray-500">تعداد سفارشات</p>
                                <h3 class="text-2xl font-bold">۱۲۴</h3>
                            </div>
                            <div class="w-12 h-12 bg-primary bg-opacity-10 rounded-full flex items-center justify-center">
                                <i class="fas fa-shopping-cart text-primary text-xl"></i>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white rounded-2xl shadow p-6">
                        <div class="flex items-center justify-between">
                            <div>
                                <p class="text-gray-500">درآمد امروز</p>
                                <h3 class="text-2xl font-bold">۳,۴۵۰,۰۰۰ تومان</h3>
                            </div>
                            <div class="w-12 h-12 bg-secondary bg-opacity-10 rounded-full flex items-center justify-center">
                                <i class="fas fa-wallet text-secondary text-xl"></i>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white rounded-2xl shadow p-6">
                        <div class="flex items-center justify-between">
                            <div>
                                <p class="text-gray-500">تعداد کاربران</p>
                                <h3 class="text-2xl font-bold">۵۶۸</h3>
                            </div>
                            <div class="w-12 h-12 bg-accent bg-opacity-10 rounded-full flex items-center justify-center">
                                <i class="fas fa-users text-accent text-xl"></i>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white rounded-2xl shadow p-6">
                        <div class="flex items-center justify-between">
                            <div>
                                <p class="text-gray-500">محصولات فعال</p>
                                <h3 class="text-2xl font-bold">۸۷</h3>
                            </div>
                            <div class="w-12 h-12 bg-primary bg-opacity-10 rounded-full flex items-center justify-center">
                                <i class="fas fa-utensils text-primary text-xl"></i>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white rounded-2xl shadow overflow-hidden mb-8">
                    <div class="border-b border-gray-200 p-4 flex justify-between items-center">
                        <h3 class="font-bold text-lg">مدیریت محصولات</h3>
                        <button id="add-product-btn" class="bg-primary text-white px-4 py-2 rounded-lg hover:bg-opacity-90 transition">
                            <i class="fas fa-plus ml-2"></i> افزودن محصول جدید
                        </button>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="min-w-full divide-y divide-gray-200">
                            <thead class="bg-gray-50">
                                <tr>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">تصویر</th>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">نام محصول</th>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">دسته بندی</th>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">قیمت</th>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">وضعیت</th>
                                    <th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">عملیات</th>
                                </tr>
                            </thead>
                            <tbody class="bg-white divide-y divide-gray-200" id="admin-products-table">
                                <!-- Products will be added here by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div class="bg-white rounded-2xl shadow overflow-hidden">
                        <div class="border-b border-gray-200 p-4">
                            <h3 class="font-bold text-lg">آخرین سفارشات</h3>
                        </div>
                        <div class="divide-y divide-gray-200">
                            <!-- Orders will be added here by JavaScript -->
                            <div class="p-4 flex items-center justify-between">
                                <div class="flex items-center space-x-3 space-x-reverse">
                                    <div class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center">
                                        <i class="fas fa-shopping-bag text-gray-500"></i>
                                    </div>
                                    <div>
                                        <p class="font-medium">سفارش #۱۲۵۴</p>
                                        <p class="text-sm text-gray-500">۲ ساعت پیش</p>
                                    </div>
                                </div>
                                <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm">تحویل شده</span>
                            </div>
                            <div class="p-4 flex items-center justify-between">
                                <div class="flex items-center space-x-3 space-x-reverse">
                                    <div class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center">
                                        <i class="fas fa-shopping-bag text-gray-500"></i>
                                    </div>
                                    <div>
                                        <p class="font-medium">سفارش #۱۲۵۳</p>
                                        <p class="text-sm text-gray-500">۵ ساعت پیش</p>
                                    </div>
                                </div>
                                <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-sm">در حال آماده‌سازی</span>
                            </div>
                            <div class="p-4 flex items-center justify-between">
                                <div class="flex items-center space-x-3 space-x-reverse">
                                    <div class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center">
                                        <i class="fas fa-shopping-bag text-gray-500"></i>
                                    </div>
                                    <div>
                                        <p class="font-medium">سفارش #۱۲۵۲</p>
                                        <p class="text-sm text-gray-500">۱ روز پیش</p>
                                    </div>
                                </div>
                                <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm">در راه</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-white rounded-2xl shadow overflow-hidden">
                        <div class="border-b border-gray-200 p-4">
                            <h3 class="font-bold text-lg">نظرات جدید</h3>
                        </div>
                        <div class="divide-y divide-gray-200">
                            <!-- Reviews will be added here by JavaScript -->
                            <div class="p-4">
                                <div class="flex items-center space-x-3 space-x-reverse mb-2">
                                    <div class="w-10 h-10 rounded-full bg-gray-200 overflow-hidden">
                                        <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="کاربر" class="w-full h-full object-cover">
                                    </div>
                                    <div>
                                        <p class="font-medium">نازنین محمدی</p>
                                        <div class="flex text-yellow-400 text-sm">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                        </div>
                                    </div>
                                </div>
                                <p class="text-gray-600 text-sm">غذاهای زوود کوک واقعاً عالی هستند. همیشه تازه و داغ به دستم می‌رسند.</p>
                            </div>
                            <div class="p-4">
                                <div class="flex items-center space-x-3 space-x-reverse mb-2">
                                    <div class="w-10 h-10 rounded-full bg-gray-200 overflow-hidden">
                                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="کاربر" class="w-full h-full object-cover">
                                    </div>
                                    <div>
                                        <p class="font-medium">امیر حسینی</p>
                                        <div class="flex text-yellow-400 text-sm">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star-half-alt"></i>
                                        </div>
                                    </div>
                                </div>
                                <p class="text-gray-600 text-sm">سرعت تحویل غذاها واقعاً قابل تقدیره. چند بار که سفارش دادم همیشه زودتر از موعد مقرر رسید.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Add/Edit Product Modal -->
    <div id="product-modal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white rounded-2xl shadow-xl w-full max-w-2xl mx-4">
            <div class="p-6">
                <div class="flex justify-between items-center mb-6">
                    <h3 class="text-xl font-bold text-dark" id="product-modal-title">افزودن محصول جدید</h3>
                    <button id="close-product-modal" class="text-gray-500 hover:text-dark">
                        <i class="fas fa-times text-xl"></i>
                    </button>
                </div>
                
                <form id="product-form">
                    <input type="hidden" id="product-id">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <label for="product-name" class="block text-gray-700 mb-2">نام محصول</label>
                            <input type="text" id="product-name" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" required>
                        </div>
                        <div>
                            <label for="product-category" class="block text-gray-700 mb-2">دسته بندی</label>
                            <select id="product-category" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" required>
                                <option value="fastfood">فست فود</option>
                                <option value="homemade">خانگی</option>
                                <option value="iranian">ایرانی</option>
                                <option value="semi">نیمه آماده</option>
                            </select>
                        </div>
                        <div>
                            <label for="product-price" class="block text-gray-700 mb-2">قیمت (تومان)</label>
                            <input type="number" id="product-price" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" required>
                        </div>
                        <div>
                            <label for="product-status" class="block text-gray-700 mb-2">وضعیت</label>
                            <select id="product-status" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" required>
                                <option value="active">فعال</option>
                                <option value="inactive">غیرفعال</option>
                            </select>
                        </div>
                        <div class="md:col-span-2">
                            <label for="product-description" class="block text-gray-700 mb-2">توضیحات</label>
                            <textarea id="product-description" rows="3" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"></textarea>
                        </div>
                        <div class="md:col-span-2">
                            <label for="product-image" class="block text-gray-700 mb-2">تصویر محصول</label>
                            <div class="flex items-center space-x-4 space-x-reverse">
                                <div class="w-24 h-24 bg-gray-100 rounded-lg overflow-hidden flex items-center justify-center" id="product-image-preview">
                                    <i class="fas fa-image text-gray-400 text-2xl"></i>
                                </div>
                                <div class="flex-1">
                                    <input type="file" id="product-image" class="hidden" accept="image/*">
                                    <button type="button" id="upload-image-btn" class="bg-gray-100 text-gray-700 px-4 py-2 rounded-lg hover:bg-gray-200 transition">
                                        انتخاب تصویر
                                    </button>
                                    <p class="text-sm text-gray-500 mt-2">فرمت‌های مجاز: JPG, PNG, GIF. حداکثر حجم: 2MB</p>
                                </div>
                            </div>
                        </div>
                        <div class="md:col-span-2">
                            <label for="product-payment-link" class="block text-gray-700 mb-2">لینک پرداخت</label>
                            <input type="url" id="product-payment-link" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent" placeholder="https://">
                        </div>
                    </div>
                    
                    <div class="mt-8 flex justify-end space-x-4 space-x-reverse">
                        <button type="button" id="cancel-product-btn" class="border-2 border-primary text-primary px-6 py-2 rounded-lg hover:bg-primary hover:text-white transition">
                            انصراف
                        </button>
                        <button type="submit" id="save-product-btn" class="bg-primary text-white px-6 py-2 rounded-lg hover:bg-opacity-90 transition">
                            ذخیره محصول
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Success Notification -->
    <div id="success-notification" class="fixed bottom-4 right-4 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg flex items-center space-x-3 space-x-reverse transform translate-x-full transition-transform duration-300 z-50">
        <i class="fas fa-check-circle"></i>
        <span id="success-message">عملیات با موفقیت انجام شد</span>
    </div>

    <script>
        // Sample data for food items
        const foodItems = [
            {
                id: 1,
                name: "چلوکباب برگ",
                category: "iranian",
                price: 120000,
                description: "چلوکباب برگ با گوشت گوسفندی تازه و برنج ایرانی مرغوب",
                image: "https://images.unsplash.com/photo-1601050690597-df0568f70950?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                paymentLink: "https://example.com/payment/1"
            },
            {
                id: 2,
                name: "قورمه سبزی",
                category: "iranian",
                price: 85000,
                description: "قورمه سبزی با گوشت گوساله و سبزی تازه",
                image: "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                paymentLink: "https://example.com/payment/2"
            },
            {
                id: 3,
                name: "برگر ویژه",
                category: "fastfood",
                price: 65000,
                description: "برگر با گوشت ۱۰۰% گوساله، پنیر چدار و سس مخصوص",
                image: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=999&q=80",
                paymentLink: "https://example.com/payment/3"
            },
            {
                id: 4,
                name: "پیتزا مخصوص",
                category: "fastfood",
                price: 95000,
                description: "پیتزا با سوسیس، قارچ، زیتون و پنیر موزارلا",
                image: "https://images.unsplash.com/photo-1513104890138-7c749659a591?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                paymentLink: "https://example.com/payment/4"
            },
            {
                id: 5,
                name: "خوراک مرغ",
                category: "homemade",
                price: 75000,
                description: "خوراک مرغ با سبزیجات تازه و سس مخصوص",
                image: "https://images.unsplash.com/photo-1547592180-85f173990554?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                paymentLink: "https://example.com/payment/5"
            },
            {
                id: 6,
                name: "خوراک سبزیجات",
                category: "homemade",
                price: 60000,
                description: "خوراک سبزیجات فصل با سس مخصوص گیاهی",
                image: "https://images.unsplash.com/photo-1546069901-d5bfd2cbfb1f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                paymentLink: "https://example.com/payment/6"
            },
            {
                id: 7,
                name: "کوفته نیمه آماده",
                category: "semi",
                price: 45000,
                description: "کوفته آماده برای پخت، همراه با دستور پخت",
                image: "https://images.unsplash.com/photo-1601050690647-8b6d2470a8c1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                paymentLink: "https://example.com/payment/7"
            },
            {
                id: 8,
                name: "لازانیا نیمه آماده",
                category: "semi",
                price: 55000,
                description: "لازانیا آماده برای پخت در فر، همراه با دستور پخت",
                image: "https://images.unsplash.com/photo-1574894709920-11b28e7367e3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                paymentLink: "https://example.com/payment/8"
            }
        ];

        // Shopping cart
        let cart = [];

        // DOM Elements
        const foodItemsContainer = document.getElementById('food-items-container');
        const cartBtn = document.getElementById('cart-btn');
        const cartSidebar = document.getElementById('cart-sidebar');
        const closeCartBtn = document.getElementById('close-cart');
        const cartItems = document.getElementById('cart-items');
        const emptyCartMessage = document.getElementById('empty-cart-message');
        const cartTotal = document.getElementById('cart-total');
        const cartDiscount = document.getElementById('cart-discount');
        const cartFinalTotal = document.getElementById('cart-final-total');
        const checkoutBtn = document.getElementById('checkout-btn');
        const cartOverlay = document.getElementById('cart-overlay');
        const cartBadge = document.querySelector('.cart-badge');
        const categoryBtns = document.querySelectorAll('.category-btn');
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const loginBtn = document.getElementById('login-btn');
        const adminModal = document.getElementById('admin-modal');
        const closeAdminModal = document.getElementById('close-admin-modal');
        const sendCodeBtn = document.getElementById('send-code-btn');
        const verifyCodeBtn = document.getElementById('verify-code-btn');
        const verificationStep = document.getElementById('verification-step');
        const loginStep = document.getElementById('login-step');
        const adminEmailDisplay = document.getElementById('admin-email-display');
        const adminPanel = document.getElementById('admin-panel');
        const adminLogout = document.getElementById('admin-logout');
        const addProductBtn = document.getElementById('add-product-btn');
        const productModal = document.getElementById('product-modal');
        const closeProductModal = document.getElementById('close-product-modal');
        const productForm = document.getElementById('product-form');
        const productModalTitle = document.getElementById('product-modal-title');
        const cancelProductBtn = document.getElementById('cancel-product-btn');
        const saveProductBtn = document.getElementById('save-product-btn');
        const uploadImageBtn = document.getElementById('upload-image-btn');
        const productImagePreview = document.getElementById('product-image-preview');
        const successNotification = document.getElementById('success-notification');
        const adminProductsTable = document.getElementById('admin-products-table');

        // Initialize the app
        function init() {
            renderFoodItems();
            setupEventListeners();
        }

        // Render food items
        function renderFoodItems(category = 'all') {
            foodItemsContainer.innerHTML = '';
            
            const filteredItems = category === 'all' 
                ? foodItems 
                : foodItems.filter(item => item.category === category);
            
            if (filteredItems.length === 0) {
                foodItemsContainer.innerHTML = `
                    <div class="col-span-3 text-center py-12 text-gray-500">
                        <i class="fas fa-utensils text-4xl mb-4"></i>
                        <p>هیچ محصولی در این دسته بندی وجود ندارد</p>
                    </div>
                `;
                return;
            }
            
            filteredItems.forEach(item => {
                const foodItem = document.createElement('div');
                foodItem.className = 'bg-white rounded-2xl shadow-md overflow-hidden food-card transition duration-300';
                foodItem.innerHTML = `
                    <div class="relative">
                        <img src="${item.image}" alt="${item.name}" class="w-full h-48 object-cover">
                        <div class="absolute top-4 left-4 bg-primary text-white px-3 py-1 rounded-full text-sm">${getCategoryName(item.category)}</div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-lg mb-2">${item.name}</h3>
                        <p class="text-gray-600 text-sm mb-4">${item.description}</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold">${item.price.toLocaleString()} تومان</span>
                            <button class="add-to-cart bg-primary text-white px-4 py-2 rounded-lg hover:bg-opacity-90 transition" data-id="${item.id}">
                                <i class="fas fa-plus ml-1"></i> افزودن
                            </button>
                        </div>
                    </div>
                `;
                foodItemsContainer.appendChild(foodItem);
            });
            
            // Add event listeners to add to cart buttons
            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', function() {
                    const id = parseInt(this.getAttribute('data-id'));
                    addToCart(id);
                });
            });
        }

        // Get category name in Persian
        function getCategoryName(category) {
            switch(category) {
                case 'fastfood': return 'فست فود';
                case 'homemade': return 'خانگی';
                case 'iranian': return 'ایرانی';
                case 'semi': return 'نیمه آماده';
                default: return '';
            }
        }

        // Add to cart
        function addToCart(id) {
            const item = foodItems.find(item => item.id === id);
            if (!item) return;
            
            const existingItem = cart.find(cartItem => cartItem.id === id);
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    ...item,
                    quantity: 1
                });
            }
            
            updateCart();
            showSuccessNotification('محصول به سبد خرید اضافه شد');
        }

        // Update cart
        function updateCart() {
            // Update cart items
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                emptyCartMessage.classList.remove('hidden');
                checkoutBtn.disabled = true;
            } else {
                emptyCartMessage.classList.add('hidden');
                checkoutBtn.disabled = false;
                
                cart.forEach(item => {
                    const cartItem = document.createElement('div');
                    cartItem.className = 'flex items-center justify-between bg-gray-50 p-4 rounded-lg';
                    cartItem.innerHTML = `
                        <div class="flex items-center space-x-4 space-x-reverse">
                            <div class="w-16 h-16 bg-gray-200 rounded-lg overflow-hidden">
                                <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover">
                            </div>
                            <div>
                                <h4 class="font-bold">${item.name}</h4>
                                <p class="text-sm text-gray-600">${item.price.toLocaleString()} تومان</p>
                            </div>
                        </div>
                        <div class="flex items-center space-x-3 space-x-reverse">
                            <button class="decrease-quantity text-gray-500 hover:text-primary transition" data-id="${item.id}">
                                <i class="fas fa-minus"></i>
                            </button>
                            <span class="quantity">${item.quantity}</span>
                            <button class="increase-quantity text-gray-500 hover:text-primary transition" data-id="${item.id}">
                                <i class="fas fa-plus"></i>
                            </button>
                            <button class="remove-item text-red-500 hover:text-red-700 transition" data-id="${item.id}">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    `;
                    cartItems.appendChild(cartItem);
                });
                
                // Add event listeners to quantity buttons
                document.querySelectorAll('.increase-quantity').forEach(btn => {
                    btn.addEventListener('click', function() {
                        const id = parseInt(this.getAttribute('data-id'));
                        changeQuantity(id, 1);
                    });
                });
                
                document.querySelectorAll('.decrease-quantity').forEach(btn => {
                    btn.addEventListener('click', function() {
                        const id = parseInt(this.getAttribute('data-id'));
                        changeQuantity(id, -1);
                    });
                });
                
                document.querySelectorAll('.remove-item').forEach(btn => {
                    btn.addEventListener('click', function() {
                        const id = parseInt(this.getAttribute('data-id'));
                        removeFromCart(id);
                    });
                });
            }
            
            // Update cart totals
            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const discount = subtotal > 200000 ? subtotal * 0.1 : 0;
            const total = subtotal - discount;
            
            cartTotal.textContent = subtotal.toLocaleString() + ' تومان';
            cartDiscount.textContent = discount.toLocaleString() + ' تومان';
            cartFinalTotal.textContent = total.toLocaleString() + ' تومان';
            
            // Update cart badge
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            if (totalItems > 0) {
                cartBadge.textContent = totalItems;
                cartBadge.classList.remove('hidden');
            } else {
                cartBadge.classList.add('hidden');
            }
        }

        // Change quantity
        function changeQuantity(id, change) {
            const item = cart.find(item => item.id === id);
            if (!item) return;
            
            item.quantity += change;
            
            if (item.quantity <= 0) {
                removeFromCart(id);
            } else {
                updateCart();
            }
        }

        // Remove from cart
        function removeFromCart(id) {
            cart = cart.filter(item => item.id !== id);
            updateCart();
            showSuccessNotification('محصول از سبد خرید حذف شد');
        }

        // Show success notification
        function showSuccessNotification(message) {
            const notification = successNotification;
            const messageElement = document.getElementById('success-message');
            
            messageElement.textContent = message;
            notification.classList.remove('translate-x-full');
            notification.classList.add('translate-x-0');
            
            setTimeout(() => {
                notification.classList.remove('translate-x-0');
                notification.classList.add('translate-x-full');
            }, 3000);
        }

        // Setup event listeners
        function setupEventListeners() {
            // Cart toggle
            cartBtn.addEventListener('click', () => {
                cartSidebar.classList.remove('translate-x-full');
                cartOverlay.classList.remove('hidden');
                document.body.style.overflow = 'hidden';
            });
            
            closeCartBtn.addEventListener('click', () => {
                cartSidebar.classList.add('translate-x-full');
                cartOverlay.classList.add('hidden');
                document.body.style.overflow = '';
            });
            
            cartOverlay.addEventListener('click', () => {
                cartSidebar.classList.add('translate-x-full');
                cartOverlay.classList.add('hidden');
                document.body.style.overflow = '';
            });
            
            // Checkout
            checkoutBtn.addEventListener('click', () => {
                alert('در حال انتقال به درگاه پرداخت...');
                cart = [];
                updateCart();
                cartSidebar.classList.add('translate-x-full');
                cartOverlay.classList.add('hidden');
                document.body.style.overflow = '';
                showSuccessNotification('سفارش شما با موفقیت ثبت شد');
            });
            
            // Category filter
            categoryBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    categoryBtns.forEach(b => b.classList.remove('active', 'bg-primary', 'text-white'));
                    this.classList.add('active', 'bg-primary', 'text-white');
                    const category = this.getAttribute('data-category');
                    renderFoodItems(category);
                });
            });
            
            // Mobile menu toggle
            mobileMenuBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Admin login
            loginBtn.addEventListener('click', () => {
                adminModal.classList.remove('hidden');
                document.body.style.overflow = 'hidden';
            });
            
            closeAdminModal.addEventListener('click', () => {
                adminModal.classList.add('hidden');
                document.body.style.overflow = '';
            });
            
            sendCodeBtn.addEventListener('click', () => {
                const email = document.getElementById('admin-email').value;
                if (!email) {
                    alert('لطفاً ایمیل خود را وارد کنید');
                    return;
                }
                
                // Simulate sending verification code
                adminEmailDisplay.textContent = email;
                loginStep.classList.add('hidden');
                verificationStep.classList.remove('hidden');
            });
            
            verifyCodeBtn.addEventListener('click', () => {
                const code = document.getElementById('verification-code').value;
                if (!code || code.length !== 6) {
                    alert('لطفاً کد تأیید ۶ رقمی را وارد کنید');
                    return;
                }
                
                // Simulate verification
                adminModal.classList.add('hidden');
                adminPanel.classList.remove('hidden');
                document.body.style.overflow = 'hidden';
                showSuccessNotification('ورود با موفقیت انجام شد');
            });
            
            // Admin logout
            adminLogout.addEventListener('click', () => {
                adminPanel.classList.add('hidden');
                document.body.style.overflow = '';
                showSuccessNotification('خروج با موفقیت انجام شد');
            });
            
            // Product management
            addProductBtn.addEventListener('click', () => {
                productModalTitle.textContent = 'افزودن محصول جدید';
                productForm.reset();
                productImagePreview.innerHTML = '<i class="fas fa-image text-gray-400 text-2xl"></i>';
                productModal.classList.remove('hidden');
            });
            
            closeProductModal.addEventListener('click', () => {
                productModal.classList.add('hidden');
            });
            
            cancelProductBtn.addEventListener('click', () => {
                productModal.classList.add('hidden');
            });
            
            uploadImageBtn.addEventListener('click', () => {
                document.getElementById('product-image').click();
            });
            
            document.getElementById('product-image').addEventListener('change', function(e) {
                const file = e.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = function(event) {
                        productImagePreview.innerHTML = `<img src="${event.target.result}" class="w-full h-full object-cover">`;
                    };
                    reader.readAsDataURL(file);
                }
            });
            
            productForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // In a real app, you would save the product to a database
                // Here we just simulate it
                productModal.classList.add('hidden');
                showSuccessNotification('محصول با موفقیت ذخیره شد');
                
                // Update admin products table
                renderAdminProductsTable();
            });
        }

        // Render admin products table
        function renderAdminProductsTable() {
            adminProductsTable.innerHTML = '';
            
            foodItems.forEach(item => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="px-6 py-4 whitespace-nowrap">
                        <div class="w-10 h-10 rounded-lg overflow-hidden">
                            <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover">
                        </div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">
                        <div class="text-sm font-medium text-gray-900">${item.name}</div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">
                        <div class="text-sm text-gray-500">${getCategoryName(item.category)}</div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">

</html>
