---
layout: null
title: Vn-Elliott | Chuyên trang Sóng Elliott & Trading
description: Hướng dẫn giao dịch Forex, Chứng khoán chuyên sâu với lý thuyết Sóng Elliott.
---
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>
    <meta name="description" content="{{ page.description }}">
    
    <!-- Link đến file CSS đã tạo -->
    <link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">
    
    <!-- Google Fonts (Optional) -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- HEADER -->
    <header>
        <div class="container">
            <a href="/" class="logo">VN-ELLIOTT</a>
            <nav>
                <ul>
                    <li><a href="/">Trang chủ</a></li>
                    <li><a href="/about">Giới thiệu</a></li>
                    <li><a href="/blog">Kiến thức</a></li>
                    <li><a href="/contact">Liên hệ</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <!-- HERO SECTION -->
    <section class="hero">
        <div class="container">
            <h1>Chinh Phục Thị Trường Với Nguyên Lý Sóng Elliott</h1>
            <p>Phương pháp phân tích kỹ thuật chuyên sâu giúp bạn xác định xu hướng và tìm kiếm cơ hội giao dịch Forex, Chứng khoán hiệu quả.</p>
            <a href="#latest-posts" class="btn-primary">Bắt đầu học ngay</a>
        </div>
    </section>
    <!-- GIỚI THIỆU / LỢI ÍCH -->
    <section class="section bg-light">
        <div class="container">
            <div class="section-title">
                <h2>Tại Sao Chọn Vn-Elliott?</h2>
                <span></span>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <h3>🔍 Phân Tích Chuyên Sâu</h3>
                    <p>Các bài nhận định thị trường dựa trên cấu trúc sóng chi tiết, không chỉ là dự đoán giá đơn thuần.</p>
                </div>
                <div class="feature-card">
                    <h3>📚 Kiến Thức Thực Chiến</h3>
                    <p>Chia sẻ kinh nghiệm giao dịch thực tế, quản lý vốn và tâm lý giao dịch trong thị trường tài chính.</p>
                </div>
                <div class="feature-card">
                    <h3>📈 Đa Dạng Thị Trường</h3>
                    <p>Áp dụng nguyên lý sóng cho cả Forex, Chứng khoán Việt Nam (VNI), Vàng và Tiền điện tử.</p>
                </div>
            </div>
        </div>
    </section>
    <!-- BÀI VIẾT MỚI NHẤT (Sử dụng Liquid của Jekyll) -->
    <section class="section" id="latest-posts">
        <div class="container">
            <div class="section-title">
                <h2>Bài Viết Mới Nhất</h2>
                <span></span>
            </div>
            <div class="post-grid">
                {% for post in site.posts limit:3 %}
                <article class="post-card">
                    <div class="post-content">
                        <div class="post-meta">
                            {{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | first }}
                        </div>
                        <a href="{{ post.url | relative_url }}" class="post-title">
                            {{ post.title }}
                        </a>
                        <p>
                            {{ post.excerpt | strip_html | truncatewords: 20 }}
                        </p>
                    </div>
                </article>
                {% endfor %}
            </div>
            <div style="text-align: center; margin-top: 30px;">
                <a href="/blog" style="color: var(--primary-color); font-weight: bold; text-decoration: underline;">Xem tất cả bài viết &rarr;</a>
            </div>
        </div>
    </section>
    <!-- FOOTER -->
    <footer>
        <div class="container">
            <h3>VN-ELLIOTT</h3>
            <p>Chia sẻ đam mê - Kết nối cộng đồng Trader Việt Nam</p>
            <div style="margin: 20px 0;">
                <!-- Social links ví dụ -->
                <a href="#">Facebook</a> | <a href="#">Telegram</a> | <a href="#">Youtube</a>
            </div>
            <p>&copy; {{ site.time | date: '%Y' }} Vn-Elliott.com. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>