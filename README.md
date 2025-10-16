<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Krempai Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
        }

        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .logo {
            font-size: 28px;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            gap: 25px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .user-actions {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .user-actions a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .user-actions a:hover {
            color: var(--secondary);
        }

        .welcome-text {
            color: var(--light);
            font-weight: 500;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.9)), url('https://images.unsplash.com/photo-1607082350899-7e105aa886ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
        }

        .btn-danger {
            background-color: var(--accent);
        }

        .btn-danger:hover {
            background-color: #c0392b;
        }

        /* Categories Section */
        .categories {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 32px;
            color: var(--dark);
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .category-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-10px);
        }

        .category-img {
            height: 200px;
            background-color: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: var(--primary);
        }

        .category-info {
            padding: 20px;
            text-align: center;
        }

        .category-info h3 {
            margin-bottom: 10px;
            color: var(--dark);
        }

        /* Features Section */
        .features {
            padding: 80px 0;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            text-align: center;
            padding: 30px;
        }

        .feature-icon {
            font-size: 50px;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 20px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: white;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bdc3c7;
            font-size: 14px;
        }

        /* Content Sections */
        .content-section {
            display: none;
            padding: 80px 0;
        }

        .content-section.active {
            display: block;
        }

        .currency-grid, .services-grid, .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .currency-item, .service-item, .review-item {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .currency-item:hover, .service-item:hover, .review-item:hover {
            transform: translateY(-5px);
        }

        .currency-amount {
            font-size: 24px;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 10px;
        }

        .currency-price {
            font-size: 20px;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .service-title {
            font-size: 22px;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 15px;
        }

        .service-description {
            margin-bottom: 20px;
            color: #666;
        }

        .service-price {
            font-size: 20px;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .review-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .review-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-right: 15px;
        }

        .review-author {
            font-weight: 700;
            color: var(--dark);
        }

        .review-text {
            color: #666;
            line-height: 1.6;
        }

        .support-content {
            background-color: white;
            border-radius: 10px;
            padding: 40px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .support-icon {
            font-size: 60px;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .support-text {
            margin-bottom: 30px;
            color: #666;
            line-height: 1.6;
        }

        .telegram-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background-color: #0088cc;
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }

        .telegram-btn:hover {
            background-color: #0077b3;
            transform: translateY(-3px);
        }

        /* Payment Modal */
        .payment-modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .payment-content {
            background-color: white;
            margin: 5% auto;
            padding: 30px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
        }

        .close {
            position: absolute;
            right: 15px;
            top: 15px;
            font-size: 24px;
            cursor: pointer;
            color: var(--gray);
        }

        .close:hover {
            color: var(--dark);
        }

        .payment-title {
            margin-bottom: 20px;
            color: var(--dark);
            text-align: center;
        }

        .card-info {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
            text-align: center;
        }

        .card-number {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .copy-btn {
            background: var(--secondary);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 500;
            transition: background 0.3s;
        }

        .copy-btn:hover {
            background: #2980b9;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }

        .form-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }

        .payment-instructions {
            background: #e8f4fd;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            font-size: 14px;
            color: #2c3e50;
        }

        /* Notification */
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 25px;
            background-color: #2ecc71;
            color: white;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            z-index: 1001;
            display: none;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .top-bar {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-links {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .user-actions {
                flex-direction: column;
                gap: 10px;
            }
            
            .currency-grid, .services-grid, .reviews-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Notification -->
    <div class="notification" id="notification"></div>

    <!-- Payment Modal -->
    <div class="payment-modal" id="paymentModal">
        <div class="payment-content">
            <span class="close" onclick="closePaymentModal()">&times;</span>
            <h2 class="payment-title">Оплата заказа</h2>
            
            <div class="card-info">
                <p>Переведите сумму на карту:</p>
                <div class="card-number" id="cardNumber">4441 1110 3888 4767</div>
                <button class="copy-btn" onclick="copyCardNumber()">Скопировать номер карты</button>
            </div>
            
            <div class="form-group">
                <label for="userNickname">Ваш игровой никнейм *</label>
                <input type="text" id="userNickname" placeholder="Введите ваш никнейм" required>
            </div>
            
            <div class="form-group">
                <label for="promoCode">Промокод (не обязательно)</label>
                <input type="text" id="promoCode" placeholder="Введите промокод, если есть">
            </div>
            
            <button class="btn" onclick="confirmPayment()" style="width: 100%;">Подтвердить оплату</button>
            
            <div class="payment-instructions">
                <p><strong>Инструкция:</strong></p>
                <p>1. Скопируйте номер карты и переведите точную сумму заказа и напишите в комментарии ваш ник</p>
                <p>2. Заполните ваш игровой никнейм</p>
                <p>3. Нажмите "Подтвердить оплату"</p>
                <p>4. После проверки платежа товар будет доставлен в течение 15 минут</p>
            </div>
        </div>
    </div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="top-bar">
                <a href="#" class="logo">KREMP<span>AI</span> STORE</a>
                <div class="nav-links">
                    <a href="#" onclick="showSection('currency')"><i class="fas fa-dollar-sign"></i> Валюта</a>
                    <a href="#" onclick="showSection('services')"><i class="fas fa-concierge-bell"></i> Услуги</a>
                    <a href="#" onclick="showSection('reviews')"><i class="fas fa-comments"></i> Отзывы</a>
                    <a href="#" onclick="showSection('support')"><i class="fas fa-headset"></i> Тех поддержка</a>
                </div>
                <div class="user-actions">
                    <a href="#" onclick="login()"><i class="fas fa-sign-in-alt"></i> Вход</a>
                    <a href="#" onclick="register()"><i class="fas fa-user-plus"></i> Регистрация</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main>
        <!-- Hero Section -->
        <section class="hero" id="main">
            <div class="container">
                <h1>Добро пожаловать в Krempai Store</h1>
                <p>Лучший магазин для покупки игровой валюты, услуг и многого другого. Безопасные сделки, быстрая доставка и круглосуточная поддержка.</p>
                <button class="btn" onclick="showSection('currency')">Начать покупки</button>
            </div>
        </section>

        <!-- Currency Section -->
        <section class="content-section" id="currency">
            <div class="container">
                <h2 class="section-title">Игровая Валюта</h2>
                <div class="currency-grid">
                    <div class="currency-item">
                        <div class="currency-amount">100кк</div>
                        <div class="currency-price">50 грн</div>
                        <button class="btn" onclick="buyCurrency('100кк', 50)">Купить</button>
                    </div>
                    <div class="currency-item">
                        <div class="currency-amount">50кк</div>
                        <div class="currency-price">25 грн</div>
                        <button class="btn" onclick="buyCurrency('50кк', 25)">Купить</button>
                    </div>
                    <div class="currency-item">
                        <div class="currency-amount">150кк</div>
                        <div class="currency-price">75 грн</div>
                        <button class="btn" onclick="buyCurrency('150кк', 75)">Купить</button>
                    </div>
                    <div class="currency-item">
                        <div class="currency-amount">200кк</div>
                        <div class="currency-price">100 грн</div>
                        <button class="btn" onclick="buyCurrency('200кк', 100)">Купить</button>
                    </div>
                    <div class="currency-item">
                        <div class="currency-amount">250кк</div>
                        <div class="currency-price">125 грн</div>
                        <button class="btn" onclick="buyCurrency('250кк', 125)">Купить</button>
                    </div>
                    <div class="currency-item">
                        <div class="currency-amount">300кк</div>
                        <div class="currency-price">150 грн</div>
                        <button class="btn" onclick="buyCurrency('300кк', 150)">Купить</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section class="content-section" id="services">
            <div class="container">
                <h2 class="section-title">Услуги</h2>
                <div class="services-grid">
                    <div class="service-item">
                        <h3 class="service-title">Постройка фармилки криперов</h3>
                        <p class="service-description">Строительство эффективной фармилки криперов для получения большого количества порока.</p>
                        <div class="service-price">100 грн</div>
                        <button class="btn" onclick="buyService('Постройка фармилки криперов', 100)">Купить</button>
                    </div>
                    <div class="service-item">
                        <h3 class="service-title">Постройка фармилки криперов 50/50</h3>
                        <p class="service-description">Улучшенная версия фармилки с увеличенной эффективностью и надежностью.</p>
                        <div class="service-price">200 грн</div>
                        <button class="btn" onclick="buyService('Постройка фармилки криперов 50/50', 200)">Купить</button>
                    </div>
                    <div class="service-item">
                        <h3 class="service-title">Постройка зельеварки</h3>
                        <p class="service-description">Создание автоматизированной зельеварки для приготовления различных зелий.</p>
                        <div class="service-price">150 грн</div>
                        <button class="btn" onclick="buyService('Постройка зельеварки', 150)">Купить</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Reviews Section -->
        <section class="content-section" id="reviews">
            <div class="container">
                <h2 class="section-title">Отзывы</h2>
                <div class="reviews-grid">
                    <div class="review-item">
                        <div class="review-header">
                            <div class="review-avatar">B</div>
                            <div class="review-author">Bro9i</div>
                        </div>
                        <p class="review-text">Отличный магазин! Купил 100кк валюты, все пришло мгновенно. Очень доволен обслуживанием и скоростью доставки. Рекомендую!</p>
                    </div>
                    <div class="review-item">
                        <div class="review-header">
                            <div class="review-avatar">F</div>
                            <div class="review-author">Fluger</div>
                        </div>
                        <p class="review-text">Заказывал постройку фармилки криперов. Сделали все качественно и быстро. Теперь у меня много пороха для крафта! Спасибо Krempai Store!</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Support Section -->
        <section class="content-section" id="support">
            <div class="container">
                <h2 class="section-title">Техническая Поддержка</h2>
                <div class="support-content">
                    <div class="support-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <p class="support-text">Если у вас возникли вопросы или проблемы, наши специалисты всегда готовы помочь. Напишите нам в Telegram, и мы оперативно решим ваш вопрос.</p>
                    <a href="https://t.me/krempai_support" class="telegram-btn" target="_blank">
                        <i class="fab fa-telegram"></i> Написать в Telegram
                    </a>
                </div>
            </div>
        </section>

        <!-- Categories Section -->
        <section class="categories">
            <div class="container">
                <h2 class="section-title">Категории товаров</h2>
                <div class="category-grid">
                    <div class="category-card" onclick="showSection('currency')">
                        <div class="category-img">
                            <i class="fas fa-coins"></i>
                        </div>
                        <div class="category-info">
                            <h3>Игровая валюта</h3>
                            <p>Золото, кредиты, рубины и другие игровые деньги</p>
                        </div>
                    </div>
                    <div class="category-card" onclick="showSection('services')">
                        <div class="category-img">
                            <i class="fas fa-tools"></i>
                        </div>
                        <div class="category-info">
                            <h3>Услуги</h3>
                            <p>Буст, прокачка, обучение и другие услуги</p>
                        </div>
                    </div>
                    <div class="category-card" onclick="showSection('reviews')">
                        <div class="category-img">
                            <i class="fas fa-comments"></i>
                        </div>
                        <div class="category-info">
                            <h3>Отзывы</h3>
                            <p>Что говорят наши клиенты о нас</p>
                        </div>
                    </div>
                    <div class="category-card" onclick="showSection('support')">
                        <div class="category-img">
                            <i class="fas fa-headset"></i>
                        </div>
                        <div class="category-info">
                            <h3>Поддержка</h3>
                            <p>Помощь и консультации по любым вопросам</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section class="features">
            <div class="container">
                <h2 class="section-title">Почему выбирают нас</h2>
                <div class="feature-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-shipping-fast"></i>
                        </div>
                        <h3>Быстрая доставка</h3>
                        <p>Доставляем заказы в течение 15 минут после оплаты</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Безопасные сделки</h3>
                        <p>Все транзакции защищены и гарантированы</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-headset"></i>
                        </div>
                        <h3>Поддержка 24/7</h3>
                        <p>Наша служба поддержки всегда готова помочь вам</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Krempai Store</h3>
                    <p>Лучший магазин игровых товаров и услуг с гарантией качества и быстрой доставкой.</p>
                </div>
                <div class="footer-column">
                    <h3>Категории</h3>
                    <ul>
                        <li><a href="#" onclick="showSection('currency')">Игровая валюта</a></li>
                        <li><a href="#" onclick="showSection('services')">Услуги</a></li>
                        <li><a href="#" onclick="showSection('reviews')">Отзывы</a></li>
                        <li><a href="#" onclick="showSection('support')">Поддержка</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Помощь</h3>
                    <ul>
                        <li><a href="#" onclick="showSection('support')">Доставка</a></li>
                        <li><a href="#" onclick="showSection('support')">Гарантии</a></li>
                        <li><a href="#" onclick="showSection('support')">Оплата</a></li>
                        <li><a href="#" onclick="showSection('support')">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-envelope"></i> support@krempai.store</li>
                        <li><i class="fab fa-discord"></i> Discord: Krempaiii</li>
                        <li><i class="fab fa-telegram"></i> Telegram: @krempaiiiMZ</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Krempai Store. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script>
        // Переменные для хранения текущего заказа
        let currentOrder = {
            type: '',
            name: '',
            price: 0
        };

        // Показать определенную секцию
        function showSection(sectionId) {
            // Скрыть все секции
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Скрыть главную секцию
            document.getElementById('main').style.display = 'none';
            
            // Показать выбранную секцию
            document.getElementById(sectionId).classList.add('active');
            
            // Прокрутить к выбранной секции
            document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
        }

        // Вернуться на главную
        function showMain() {
            // Скрыть все секции
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Показать главную секцию
            document.getElementById('main').style.display = 'block';
            
            // Прокрутить к главной секции
            document.getElementById('main').scrollIntoView({ behavior: 'smooth' });
        }

        // Функции покупки
        function buyCurrency(amount, price) {
            currentOrder = {
                type: 'currency',
                name: amount,
                price: price
            };
            showPaymentModal();
        }

        function buyService(service, price) {
            currentOrder = {
                type: 'service',
                name: service,
                price: price
            };
            showPaymentModal();
        }

        // Показать модальное окно оплаты
        function showPaymentModal() {
            document.getElementById('paymentModal').style.display = 'block';
        }

        // Закрыть модальное окно оплаты
        function closePaymentModal() {
            document.getElementById('paymentModal').style.display = 'none';
            // Очистить поля формы
            document.getElementById('userNickname').value = '';
            document.getElementById('promoCode').value = '';
        }

        // Скопировать номер карты
        function copyCardNumber() {
            const cardNumber = document.getElementById('cardNumber').textContent;
            navigator.clipboard.writeText(cardNumber).then(() => {
                showNotification('Номер карты скопирован в буфер обмена');
            });
        }

        // Подтвердить оплату
        function confirmPayment() {
            const nickname = document.getElementById('userNickname').value;
            const promoCode = document.getElementById('promoCode').value;
            
            if (!nickname) {
                showNotification('Пожалуйста, введите ваш игровой никнейм');
                return;
            }
            
            let message = `Заказ "${currentOrder.name}" на сумму ${currentOrder.price} грн оформлен! `;
            message += `Ваш никнейм: ${nickname}. `;
            
            if (promoCode) {
                message += `Промокод: ${promoCode}. `;
            }
            
            message += 'После проверки платежа товар будет доставлен в течение 15 минут.';
            
            showNotification(message);
            closePaymentModal();
        }

        function login() {
            showNotification('Форма входа будет открыта в ближайшее время');
        }

        function register() {
            showNotification('Форма регистрации будет открыта в ближайшее время');
        }

        // Утилиты
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.style.display = 'block';
            
            setTimeout(() => {
                notification.style.display = 'none';
            }, 5000);
        }

        // Обработка клика по логотипу для возврата на главную
        document.querySelector('.logo').addEventListener('click', function(e) {
            e.preventDefault();
            showMain();
        });

        // Закрытие модального окна при клике вне его
        window.onclick = function(event) {
            const modal = document.getElementById('paymentModal');
            if (event.target == modal) {
                closePaymentModal();
            }
        }
    </script>
    <!-- Admin Panel -->
    <div class="admin-panel" id="adminPanel" style="display: none;">
        <div class="admin-content">
            <span class="close" onclick="closeAdminPanel()">&times;</span>
            <h2 class="admin-title">Админ-панель</h2>
            
            <div class="admin-tabs">
                <div class="admin-tab active" onclick="showAdminTab('orders')">Заказы</div>
                <div class="admin-tab" onclick="showAdminTab('users')">Пользователи</div>
                <div class="admin-tab" onclick="showAdminTab('stats')">Статистика</div>
            </div>
            
            <div class="admin-tab-content active" id="ordersTab">
                <h3>Последние заказы</h3>
                <div class="orders-list" id="ordersList">
                    <!-- Заказы будут загружаться здесь -->
                </div>
            </div>
            
            <div class="admin-tab-content" id="usersTab">
                <h3>Пользователи</h3>
                <div class="users-list" id="usersList">
                    <!-- Пользователи будут загружаться здесь -->
                </div>
            </div>
            
            <div class="admin-tab-content" id="statsTab">
                <h3>Статистика</h3>
                <div class="stats-info" id="statsInfo">
                    <!-- Статистика будет загружаться здесь -->
                </div>
            </div>
        </div>
    </div>
</body>
</html>
        /* Admin Panel Styles */
        .admin-panel {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .admin-content {
            background-color: white;
            margin: 2% auto;
            padding: 30px;
            border-radius: 10px;
            width: 90%;
            max-width: 900px;
            max-height: 80vh;
            overflow-y: auto;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
        }

        .admin-title {
            margin-bottom: 20px;
            color: var(--dark);
            text-align: center;
        }

        .admin-tabs {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid #eee;
        }

        .admin-tab {
            flex: 1;
            text-align: center;
            padding: 10px;
            cursor: pointer;
            border-bottom: 2px solid transparent;
            font-weight: 500;
        }

        .admin-tab.active {
            border-bottom: 2px solid var(--secondary);
            color: var(--secondary);
            font-weight: 600;
        }

        .admin-tab-content {
            display: none;
        }

        .admin-tab-content.active {
            display: block;
        }

        .orders-list, .users-list, .stats-info {
            margin-top: 20px;
        }

        .order-item, .user-item {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            border-left: 4px solid var(--secondary);
        }

        .order-status {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 600;
            margin-left: 10px;
        }

        .status-pending {
            background: #f39c12;
            color: white;
        }

        .status-completed {
            background: #2ecc71;
            color: white;
        }

        .status-cancelled {
            background: #e74c3c;
            color: white;
        }

        .admin-btn {
            background: var(--secondary);
            color: white;
            border: none;
            padding: 6px 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 12px;
            margin-left: 5px;
        }

        .admin-btn-danger {
            background: var(--accent);
        }

        .secret-admin-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--dark);
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 999;
            opacity: 0.3;
            transition: opacity 0.3s;
        }

        .secret-admin-btn:hover {
            opacity: 1;
        }
        // Админ-панель
        function showAdminPanel() {
            document.getElementById('adminPanel').style.display = 'block';
            loadAdminData();
        }

        function closeAdminPanel() {
            document.getElementById('adminPanel').style.display = 'none';
        }

        function showAdminTab(tabName) {
            // Скрыть все вкладки
            document.querySelectorAll('.admin-tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Убрать активный класс со всех вкладок
            document.querySelectorAll('.admin-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Показать выбранную вкладку
            document.getElementById(tabName + 'Tab').classList.add('active');
            
            // Сделать вкладку активной
            event.target.classList.add('active');
        }

        function loadAdminData() {
            // Загрузка заказов
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const ordersList = document.getElementById('ordersList');
            ordersList.innerHTML = '';
            
            if (orders.length === 0) {
                ordersList.innerHTML = '<p>Заказов пока нет</p>';
            } else {
                orders.forEach((order, index) => {
                    const orderItem = document.createElement('div');
                    orderItem.className = 'order-item';
                    orderItem.innerHTML = `
                        <strong>Заказ #${index + 1}</strong>
                        <span class="order-status status-${order.status || 'pending'}">${getStatusText(order.status)}</span>
                        <p>Товар: ${order.name}</p>
                        <p>Цена: ${order.price} грн</p>
                        <p>Никнейм: ${order.nickname}</p>
                        <p>Комментарий: ${order.comment || 'Не указан'}</p>
                        <p>Время: ${order.timestamp || 'Неизвестно'}</p>
                        <button class="admin-btn" onclick="updateOrderStatus(${index}, 'completed')">Выполнено</button>
                        <button class="admin-btn admin-btn-danger" onclick="updateOrderStatus(${index}, 'cancelled')">Отменить</button>
                    `;
                    ordersList.appendChild(orderItem);
                });
            }
            
            // Загрузка статистики
            const statsInfo = document.getElementById('statsInfo');
            const totalOrders = orders.length;
            const completedOrders = orders.filter(order => order.status === 'completed').length;
            const totalRevenue = orders.filter(order => order.status === 'completed')
                                     .reduce((sum, order) => sum + order.price, 0);
            
            statsInfo.innerHTML = `
                <div class="order-item">
                    <p><strong>Всего заказов:</strong> ${totalOrders}</p>
                    <p><strong>Выполнено заказов:</strong> ${completedOrders}</p>
                    <p><strong>Общая выручка:</strong> ${totalRevenue} грн</p>
                    <p><strong>Процент выполнения:</strong> ${totalOrders > 0 ? Math.round((completedOrders / totalOrders) * 100) : 0}%</p>
                </div>
            `;
        }

        function getStatusText(status) {
            const statusMap = {
                'pending': 'Ожидание',
                'completed': 'Выполнено',
                'cancelled': 'Отменено'
            };
            return statusMap[status] || 'Ожидание';
        }

        function updateOrderStatus(orderIndex, status) {
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            if (orders[orderIndex]) {
                orders[orderIndex].status = status;
                localStorage.setItem('orders', JSON.stringify(orders));
                loadAdminData();
                showNotification(`Статус заказа #${orderIndex + 1} обновлен на "${getStatusText(status)}"`);
            }
        }

        // Секретная кнопка админки (трижды кликнуть на логотип)
        let adminClickCount = 0;
        let adminClickTimer;

        document.querySelector('.logo').addEventListener('click', function(e) {
            e.preventDefault();
            adminClickCount++;
            
            clearTimeout(adminClickTimer);
            adminClickTimer = setTimeout(() => {
                adminClickCount = 0;
            }, 1000);
            
            if (adminClickCount === 3) {
                showAdminPanel();
                adminClickCount = 0;
            }
        });

        // Обновите функцию confirmPayment для сохранения заказов
        function confirmPayment() {
            const nickname = document.getElementById('userNickname').value;
            const comment = document.getElementById('paymentComment').value;
            const promoCode = document.getElementById('promoCode').value;
            
            if (!nickname) {
                showNotification('Пожалуйста, введите ваш игровой никнейм');
                return;
            }
            
            if (!comment) {
                showNotification('Пожалуйста, укажите комментарий для перевода');
                return;
            }
            
            // Сохраняем заказ в localStorage
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const newOrder = {
                type: currentOrder.type,
                name: currentOrder.name,
                price: currentOrder.price,
                nickname: nickname,
                comment: comment,
                promoCode: promoCode,
                status: 'pending',
                timestamp: new Date().toLocaleString('ru-RU')
            };
            
            orders.push(newOrder);
            localStorage.setItem('orders', JSON.stringify(orders));
            
            let message = `Заказ "${currentOrder.name}" на сумму ${currentOrder.price} грн оформлен! `;
            message += `Ваш никнейм: ${nickname}. `;
            message += `Комментарий для перевода: ${comment}. `;
            
            if (promoCode) {
                message += `Промокод: ${promoCode}. `;
            }
            
            message += 'После проверки платежа товар будет доставлен в течение 15 минут.';
            
            showNotification(message);
            closePaymentModal();
        }
        function performLogin() {
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            // Секретный вход для админа
            if (email === 'admin@krempai.store' && password === 'admin123') {
                showNotification('Добро пожаловать в админ-панель!');
                document.getElementById('welcomeText').textContent = 'Администратор';
                closeAuthModal();
                showAdminPanel();
                return;
            }
            
            // Обычная логика входа...
            if (!email || !password) {
                showNotification('Пожалуйста, заполните все поля');
                return;
            }
            
            showNotification('Вход выполнен успешно!');
            document.getElementById('welcomeText').textContent = email;
            closeAuthModal();
        }
