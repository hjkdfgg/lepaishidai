<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>智能手表X | 未来科技，触手可及</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* 全局样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        :root {
            --primary-color: #2563eb;
            --secondary-color: #1e40af;
            --accent-color: #3b82f6;
            --text-color: #333;
            --light-color: #f8fafc;
            --dark-color: #1e293b;
            --gray-color: #64748b;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            line-height: 1.6;
            color: var(--text-color);
            background-color: #fff;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 80px 0;
        }
        
        h1, h2, h3, h4 {
            color: var(--dark-color);
            line-height: 1.2;
            margin-bottom: 15px;
        }
        
        h1 {
            font-size: 3rem;
        }
        
        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary-color);
            border-radius: 2px;
        }
        
        p {
            margin-bottom: 15px;
            color: var(--gray-color);
        }
        
        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 12px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .btn:hover {
            background: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }
        
        .btn-secondary {
            background: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }
        
        .btn-secondary:hover {
            background: var(--primary-color);
            color: white;
        }
        
        /* 导航栏 */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 15px 0;
            transition: var(--transition);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }
        
        .logo span {
            color: var(--dark-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 600;
            transition: var(--transition);
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            background: none;
            border: none;
            color: var(--dark-color);
            cursor: pointer;
        }
        
        /* 英雄区域 */
        .hero {
            padding-top: 150px;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            overflow: hidden;
        }
        
        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        
        .hero-text h1 {
            margin-bottom: 20px;
        }
        
        .hero-text p {
            font-size: 1.1rem;
            margin-bottom: 30px;
        }
        
        .btn-group {
            display: flex;
            gap: 15px;
        }
        
        .hero-image {
            text-align: center;
            position: relative;
        }
        
        .hero-image img {
            max-width: 100%;
            filter: drop-shadow(0 15px 30px rgba(0, 0, 0, 0.2));
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        /* 特性区域 */
        .features {
            background-color: var(--light-color);
        }
        
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        
        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
        }
        
        /* 产品详情 */
        .product-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        
        .details-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }
        
        .spec-list {
            list-style: none;
            margin-top: 20px;
        }
        
        .spec-list li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
        }
        
        .spec-list li:last-child {
            border-bottom: none;
        }
        
        .spec-name {
            font-weight: 600;
        }
        
        .spec-value {
            color: var(--gray-color);
        }
        
        /* 评价区域 */
        .testimonials {
            background-color: var(--light-color);
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
            background-color: #e0f2fe;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .author-info h4 {
            margin-bottom: 5px;
        }
        
        .rating {
            color: #fbbf24;
        }
        
        /* 定价区域 */
        .pricing-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            text-align: center;
            transition: var(--transition);
        }
        
        .pricing-card:hover {
            transform: translateY(-10px);
        }
        
        .pricing-header {
            background: var(--primary-color);
            color: white;
            padding: 30px;
        }
        
        .pricing-header h3 {
            color: white;
        }
        
        .price {
            font-size: 3rem;
            font-weight: 700;
            margin: 20px 0;
        }
        
        .price span {
            font-size: 1rem;
            font-weight: normal;
        }
        
        .pricing-features {
            padding: 30px;
            list-style: none;
        }
        
        .pricing-features li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        
        .pricing-features li:last-child {
            border-bottom: none;
        }
        
        .pricing-card .btn {
            margin: 0 30px 30px;
            width: calc(100% - 60px);
        }
        
        /* 联系表单 */
        .contact-form {
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: var(--shadow);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }
        
        /* 页脚 */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            color: white;
            margin-bottom: 25px;
            font-size: 1.3rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #cbd5e1;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--primary-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #cbd5e1;
            font-size: 0.9rem;
        }
        
        /* 响应式设计 */
        @media (max-width: 992px) {
            .hero-content,
            .product-details {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .feature-grid,
            .testimonial-grid,
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
                transform: translateY(-100%);
                opacity: 0;
                transition: var(--transition);
                z-index: 999;
            }
            
            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .feature-grid,
            .testimonial-grid,
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .btn-group {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .btn-group .btn {
                width: 100%;
                text-align: center;
            }
        }
        
        @media (max-width: 576px) {
            section {
                padding: 60px 0;
            }
            
            .hero {
                padding-top: 120px;
            }
            
            .contact-form {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">Smart<span>Watch</span>X</a>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">首页</a></li>
                <li><a href="#features">特性</a></li>
                <li><a href="#details">产品详情</a></li>
                <li><a href="#testimonials">用户评价</a></li>
                <li><a href="#pricing">定价</a></li>
                <li><a href="#contact">联系我们</a></li>
            </ul>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>智能手表X：未来科技，触手可及</h1>
                    <p>智能手表X重新定义了可穿戴设备的边界。集健康监测、智能通知、运动追踪于一体，让您的生活更加便捷、健康、高效。</p>
                    <div class="btn-group">
                        <a href="#pricing" class="btn">立即购买</a>
                        <a href="#features" class="btn btn-secondary">了解更多</a>
                    </div>
                </div>
                <div class="hero-image">
                    <!-- 这里可以使用真实图片替换 -->
                    <img src="https://images.unsplash.com/photo-1551816230-ef5deaed4a26?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="智能手表X">
                </div>
            </div>
        </div>
    </section>

    <!-- 特性区域 -->
    <section class="features" id="features">
        <div class="container">
            <h2>产品特性</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <h3>健康监测</h3>
                    <p>24小时心率监测、血氧检测、睡眠质量分析，全面守护您的健康。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-battery-full"></i>
                    </div>
                    <h3>超长续航</h3>
                    <p>14天超长续航，支持快速充电，充电15分钟可使用一整天。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-swimming-pool"></i>
                    </div>
                    <h3>50米防水</h3>
                    <p>支持游泳级防水，洗手、淋浴、游泳均可佩戴，无惧水渍。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 产品详情 -->
    <section class="details" id="details">
        <div class="container">
            <h2>产品详情</h2>
            <div class="product-details">
                <div class="details-image">
                    <img src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="智能手表X细节图">
                </div>
                <div class="details-text">
                    <h3>创新设计，卓越性能</h3>
                    <p>智能手表X采用航空级铝合金材质，1.5英寸AMOLED全彩显示屏，显示效果细腻清晰。内置高性能处理器，运行流畅不卡顿。</p>
                    <ul class="spec-list">
                        <li>
                            <span class="spec-name">显示屏</span>
                            <span class="spec-value">1.5英寸AMOLED</span>
                        </li>
                        <li>
                            <span class="spec-name">处理器</span>
                            <span class="spec-value">双核1.2GHz</span>
                        </li>
                        <li>
                            <span class="spec-name">内存</span>
                            <span class="spec-value">8GB存储 + 1GB RAM</span>
                        </li>
                        <li>
                            <span class="spec-name">传感器</span>
                            <span class="spec-value">心率、血氧、加速度等</span>
                        </li>
                        <li>
                            <span class="spec-name">防水等级</span>
                            <span class="spec-value">5ATM（50米）</span>
                        </li>
                        <li>
                            <span class="spec-name">电池容量</span>
                            <span class="spec-value">450mAh</span>
                        </li>
                    </ul>
                    <a href="#contact" class="btn">获取详细规格</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 用户评价 -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2>用户评价</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "智能手表X改变了我的生活方式。健康监测功能非常准确，电池续航也很出色。强烈推荐！"
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">张</div>
                        <div class="author-info">
                            <h4>张明</h4>
                            <div class="rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "作为运动爱好者，这款手表完全满足我的需求。GPS定位精准，运动数据记录详细。"
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">李</div>
                        <div class="author-info">
                            <h4>李娜</h4>
                            <div class="rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "设计时尚，佩戴舒适。通知提醒功能让我不错过任何重要信息。物超所值！"
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">王</div>
                        <div class="author-info">
                            <h4>王伟</h4>
                            <div class="rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 定价区域 -->
    <section class="pricing" id="pricing">
        <div class="container">
            <h2>选择适合您的方案</h2>
            <div class="feature-grid">
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>标准版</h3>
                        <div class="price">¥999<span>/台</span></div>
                    </div>
                    <ul class="pricing-features">
                        <li>基础健康监测</li>
                        <li>7天续航</li>
                        <li>10种运动模式</li>
                        <li>智能通知</li>
                        <li>1年质保</li>
                    </ul>
                    <a href="#contact" class="btn">立即购买</a>
                </div>
                <div class="pricing-card" style="transform: scale(1.05); box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);">
                    <div class="pricing-header" style="background: var(--secondary-color);">
                        <h3>专业版</h3>
                        <div class="price">¥1299<span>/台</span></div>
                        <p style="color: rgba(255,255,255,0.9); font-size: 0.9rem;">最受欢迎</p>
                    </div>
                    <ul class="pricing-features">
                        <li>全面健康监测（含血氧）</li>
                        <li>14天超长续航</li>
                        <li>50种运动模式</li>
                        <li>GPS定位</li>
                        <li>2年质保 + 免费表带</li>
                    </ul>
                    <a href="#contact" class="btn">立即购买</a>
                </div>
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>尊享版</h3>
                        <div class="price">¥1699<span>/台</span></div>
                    </div>
                    <ul class="pricing-features">
                        <li>全面健康监测 + ECG</li>
                        <li>21天续航 + 无线充电</li>
                        <li>100+运动模式</li>
                        <li>双频GPS + 音乐存储</li>
                        <li>3年质保 + 专属客服</li>
                    </ul>
                    <a href="#contact" class="btn">立即购买</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系表单 -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>联系我们</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">姓名</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">邮箱</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">电话</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                    <div class="form-group">
                        <label for="message">留言</label>
                        <textarea id="message" name="message" rows="5" placeholder="请留下您的疑问或需求..."></textarea>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">提交查询</button>
                </form>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h3>SmartWatchX</h3>
                    <p>我们致力于通过创新科技，为用户带来更智能、更健康的生活方式。</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-weibo"></i></a>
                        <a href="#"><i class="fab fa-weixin"></i></a>
                        <a href="#"><i class="fab fa-qq"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>快速链接</h3>
                    <ul class="footer-links">
                        <li><a href="#home">首页</a></li>
                        <li><a href="#features">产品特性</a></li>
                        <li><a href="#details">产品详情</a></li>
                        <li><a href="#testimonials">用户评价</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>支持</h3>
                    <ul class="footer-links">
                        <li><a href="#">使用帮助</a></li>
                        <li><a href="#">常见问题</a></li>
                        <li><a href="#">保修政策</a></li>
                        <li><a href="#">售后服务</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>联系我们</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i> 北京市海淀区科技园</li>
                        <li><i class="fas fa-phone"></i> 400-123-4567</li>
                        <li><i class="fas fa-envelope"></i> info@smartwatchx.com</li>
                        <li><i class="fas fa-clock"></i> 周一至周五 9:00-18:00</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 SmartWatchX. 保留所有权利。</p>
            </div>
        </div>
    </footer>

    <script>
        // 移动端菜单切换
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // 点击导航链接后关闭移动菜单
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.style.padding = '10px 0';
                header.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.padding = '15px 0';
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });
        
        // 表单提交处理
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // 这里可以添加表单验证和提交逻辑
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            
            // 简单的成功提示
            alert(`感谢 ${name} 的留言！我们会尽快通过 ${email} 与您联系。`);
            
            // 重置表单
            this.reset();
        });
    </script>
</body>
</html>
