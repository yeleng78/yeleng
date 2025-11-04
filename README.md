<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TC客户端官网</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;600;700&family=Noto+Sans+SC:wght@300;400;500&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/vanta/0.5.24/vanta.birds.min.js"></script>
    <style>
        body {
            font-family: 'Noto Serif SC', serif;
            background: linear-gradient(135deg, #2c1810 0%, #1a0f0a 100%);
            min-height: 100vh;
        }
        
        .text-shadow {
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .grain-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            background-image: 
                radial-gradient(circle at 25% 25%, #ffffff 2px, transparent 0),
                radial-gradient(circle at 75% 75%, #ffffff 1px, transparent 0);
            background-size: 50px 50px;
            pointer-events: none;
            z-index: 1;
        }
        
        .content-layer {
            position: relative;
            z-index: 2;
        }
        
        .fade-in {
            animation: fadeIn 2s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .typewriter {
            overflow: hidden;
            border-right: 2px solid #d4af37;
            white-space: nowrap;
            animation: typing 3s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent; }
            50% { border-color: #d4af37; }
        }
        
        .parallax-bg {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
        
        .novel-text {
            line-height: 2;
            text-align: justify;
            hyphens: auto;
        }
        
        .interactive-element {
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .interactive-element:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(212, 175, 55, 0.2);
        }
        
        .chapter-marker {
            border-left: 3px solid #d4af37;
            padding-left: 1rem;
            margin: 2rem 0;
        }
    </style>
</head>
<body class="overflow-x-hidden">
    <div class="grain-overlay"></div>
    
    <!-- 导航栏 -->
    <nav class="content-layer fixed top-0 w-full bg-black bg-opacity-50 backdrop-blur-sm z-50">
        <div class="max-w-6xl mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <h1 class="text-2xl font-bold text-yellow-400 text-shadow">TC客户端官网</h1>
                <div class="flex space-x-6">
                    <a href="#story" class="text-gray-300 hover:text-yellow-400 transition-colors">功能</a>
                    <a href="#about" class="text-gray-300 hover:text-yellow-400 transition-colors">关于</a>
                    <a href="#contact" class="text-gray-300 hover:text-yellow-400 transition-colors">联系</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- 主要内容 -->
    <main class="content-layer pt-20">
        <!-- 英雄区域 -->
        <section class="relative min-h-screen flex items-center justify-center parallax-bg" 
                 style="background-image: url('rainy_street.png');">
            <div class="absolute inset-0 bg-black bg-opacity-60"></div>
            <div class="relative z-10 text-center max-w-4xl mx-auto px-6">
                <h1 class="text-6xl md:text-8xl font-bold text-yellow-400 mb-6 text-shadow fade-in">
                    开头
                </h1>
                <div class="text-xl md:text-2xl text-gray-300 mb-8 fade-in" style="animation-delay: 0.5s;">
                    <span class="typewriter">TC客户端</span>
                </div>
                <p class="text-lg text-gray-400 mb-12 max-w-2xl mx-auto fade-in" style="animation-delay: 1s;">
                    作者:夜冷大大又名甘于
                </p>
                <button onclick="scrollToStory()" 
                        class="bg-yellow-600 hover:bg-yellow-700 text-white px-8 py-4 rounded-lg text-lg font-semibold transition-all duration-300 transform hover:scale-105 fade-in interactive-element"
                        style="animation-delay: 1.5s;">
                    开始
                </button>
            </div>
        </section>

        <!-- 小说内容区域 -->
        <section id="story" class="py-20 bg-gradient-to-b from-gray-900 to-black">
            <div class="max-w-4xl mx-auto px-6">
                <!-- 章节标题 -->
                <div class="text-center mb-16 fade-in">
                    <h2 class="text-4xl font-bold text-yellow-400 mb-4 text-shadow">生存-PVP功能</h2>
                    <div class="w-24 h-1 bg-yellow-400 mx-auto"></div>
                </div>

                <!-- 小说正文 -->
                <div class="bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-lg p-8 md:p-12 shadow-2xl fade-in">
                    <div class="novel-text text-gray-200 leading-relaxed">
                        <p class="mb-6 text-lg">
                                『TipahxCokl Client』 
·PVP/生存功能介绍
·村民夸等级交易
·可开关矿透
·美丽光影
·防砍动画
·跑吃
·跑弓
·无受击抖动
·人物描边
·人物信息面板
·人物血条
·人物移动拖尾
·美丽音效
·冷白系UI
·打击变色
·适配市面上大部分模块
·绝对的防封
·等20+生存/PVP功能给你探索
                        </p>
                        
                        <div class="chapter-marker my-8">
                            <p class="text-yellow-400 font-semibold mb-2">·扩展功能</p>
                        </div>
                        
                        <p class="mb-6 text-lg">
                            
·保存账号→顾名思义
·注入账号→把保存的账号无需再次输入即可登录
·音乐播放器
                        </p>
                        
                        <div class="chapter-marker my-8">
                            <p class="text-yellow-400 font-semibold mb-2">最新更新时间</p>
                        </div>
                        
                        <p class="mb-6 text-lg">
                            2025年11月03日
                        </p>
                        
                        <div class="chapter-marker my-8">
                            <p class="text-yellow-400 font-semibold mb-2">官方最新售价</p>
                        </div>
                        
                        <p class="mb-6 text-lg">
                            普通用户:4.5人民币  普通代理:20  总代理45  代理售卖客户端的价格与作者的价格有些许不一致
                        </p>
                        
                        <p class="text-gray-400 italic text-center mt-12">
                        </p>
                    </div>
                </div>

                <!-- 互动元素 -->
                <div class="mt-16 grid md:grid-cols-2 gap-8 fade-in">
                    <div class="bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-lg p-6 interactive-element">
                        <img src="notebook.png" alt="尊贵的老板" class="w-full h-48 object-cover rounded-lg mb-4">
                        <h3 class="text-xl font-semibold text-yellow-400 mb-2"></h3>
                        <p class="text-gray-300"></p>
                    </div>
                    
                    <div class="bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-lg p-6 interactive-element">
                        <img src="rainy_street.png" alt="夜冷-甘于" class="w-full h-48 object-cover rounded-lg mb-4">
                        <h3 class="text-xl font-semibold text-yellow-400 mb-2"></h3>
                        <p class="text-gray-300"></p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 关于作者 -->
        <section id="about" class="py-20 bg-black bg-opacity-50">
            <div class="max-w-4xl mx-auto px-6 text-center">
                <h2 class="text-3xl font-bold text-yellow-400 mb-8 text-shadow fade-in"></h2>
                <div class="bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-lg p-8 fade-in">
                    <p class="text-gray-300 text-lg leading-relaxed mb-6">
                    </p>
                    <p class="text-gray-400">
                    </p>
                </div>
            </div>
        </section>

        <!-- 联系区域 -->
        <section id="contact" class="py-20 bg-gradient-to-b from-black to-gray-900">
            <div class="max-w-4xl mx-auto px-6 text-center">
                <h2 class="text-3xl font-bold text-yellow-400 mb-8 text-shadow fade-in"></h2>
                <div class="bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-lg p-8 fade-in">
                    <p class="text-gray-300 text-lg mb-8">
                    </p>
                    <div class="flex justify-center space-x-4">
                        <button class="bg-yellow-600 hover:bg-yellow-700 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 interactive-element">
                            想购买联系代理
                        </button>
                        <button class="border border-yellow-400 text-yellow-400 hover:bg-yellow-400 hover:text-black px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 interactive-element">
                            分享客户端官网
                        </button>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer class="bg-black bg-opacity-80 py-8">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <p class="text-gray-400">
                © 2025 TC客户端的价格-功能
            </p>
        </div>
    </footer>

    <script>
        // 平滑滚动到故事区域
        function scrollToStory() {
            document.getElementById('story').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // 滚动动画效果
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

        // 观察所有需要动画的元素
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // 视差滚动效果
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.parallax-bg');
            if (parallax) {
                const speed = scrolled * 0.5;
                parallax.style.transform = `translateY(${speed}px)`;
            }
        });

        // 打字机效果重置
        setInterval(() => {
            const typewriter = document.querySelector('.typewriter');
            if (typewriter) {
                typewriter.style.animation = 'none';
                setTimeout(() => {
                    typewriter.style.animation = 'typing 3s steps(40, end), blink-caret 0.75s step-end infinite';
                }, 100);
            }
        }, 8000);

        // 互动元素点击效果
        document.querySelectorAll('.interactive-element').forEach(element => {
            element.addEventListener('click', function(e) {
                // 创建波纹效果
                const ripple = document.createElement('span');
                const rect = this.getBoundingClientRect();
                const size = Math.max(rect.width, rect.height);
                const x = e.clientX - rect.left - size / 2;
                const y = e.clientY - rect.top - size / 2;
                
                ripple.style.cssText = `
                    position: absolute;
                    width: ${size}px;
                    height: ${size}px;
                    left: ${x}px;
                    top: ${y}px;
                    background: rgba(212, 175, 55, 0.3);
                    border-radius: 50%;
                    transform: scale(0);
                    animation: ripple 0.6s linear;
                    pointer-events: none;
                `;
                
                this.style.position = 'relative';
                this.style.overflow = 'hidden';
                this.appendChild(ripple);
                
                setTimeout(() => {
                    ripple.remove();
                }, 600);
            });
        });

        // 添加波纹动画样式
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
