<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hảo SayGex - Trang Chủ</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: #fff;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            padding: 20px 0;
            background-color: rgba(0, 0, 0, 0.7);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 2.2rem;
            font-weight: bold;
            background: linear-gradient(to right, #fdbb2d, #b21f1f);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: #fdbb2d;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .hero {
            padding: 100px 0;
            text-align: center;
            background: rgba(0, 0, 0, 0.4);
            margin-bottom: 60px;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(to right, #fdbb2d, #b21f1f);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }
        
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, #fdbb2d, #b21f1f);
            margin: 15px auto;
            border-radius: 2px;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .feature-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            backdrop-filter: blur(10px);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .feature-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            color: #fdbb2d;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 60px;
        }
        
        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            height: 200px;
            position: relative;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
        }
        
        .gallery-item:hover {
            transform: scale(1.05);
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .testimonials {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 30px;
            backdrop-filter: blur(10px);
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
            background: linear-gradient(to right, #fdbb2d, #b21f1f);
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        footer {
            background-color: rgba(0, 0, 0, 0.8);
            padding: 50px 0 20px;
            margin-top: 60px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
            color: #fdbb2d;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: #fdbb2d;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Hảo SayGex</div>
                <nav>
                    <ul>
                        <li><a href="#">Trang Chủ</a></li>
                        <li><a href="#">Giới Thiệu</a></li>
                        <li><a href="#">Dịch Vụ</a></li>
                        <li><a href="#">Sản Phẩm</a></li>
                        <li><a href="#">Liên Hệ</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Chào Mừng Đến Với Hảo SayGex</h1>
            <p>Khám phá thế giới đầy màu sắc và sáng tạo với Hảo SayGex - nơi những ý tưởng độc đáo trở thành hiện thực</p>
            <a href="#" class="btn">Khám Phá Ngay</a>
        </div>
    </section>

    <div class="container">
        <section class="section">
            <h2 class="section-title">Tính Năng Nổi Bật</h2>
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">✨</div>
                    <h3>Sáng Tạo Đột Phá</h3>
                    <p>Những giải pháp sáng tạo và đột phá cho mọi nhu cầu của bạn với chất lượng hàng đầu.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚀</div>
                    <h3>Công Nghệ Hiện Đại</h3>
                    <p>Áp dụng những công nghệ tiên tiến nhất để mang lại trải nghiệm tốt nhất cho người dùng.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💎</div>
                    <h3>Chất Lượng Vượt Trội</h3>
                    <p>Cam kết mang đến sản phẩm và dịch vụ với chất lượng vượt trội và độ tin cậy cao.</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">Bộ Sưu Tập</h2>
            <div class="gallery">
                <div class="gallery-item" style="background: linear-gradient(45deg, #ff9a9e, #fad0c4);"></div>
                <div class="gallery-item" style="background: linear-gradient(45deg, #a1c4fd, #c2e9fb);"></div>
                <div class="gallery-item" style="background: linear-gradient(45deg, #ffecd2, #fcb69f);"></div>
                <div class="gallery-item" style="background: linear-gradient(45deg, #84fab0, #8fd3f4);"></div>
                <div class="gallery-item" style="background: linear-gradient(45deg, #d4fc79, #96e6a1);"></div>
                <div class="gallery-item" style="background: linear-gradient(45deg, #a6c0fe, #f68084);"></div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">Đánh Giá Từ Khách Hàng</h2>
            <div class="testimonials">
                <div class="testimonial">
                    <p class="testimonial-text">"Hảo SayGex đã mang đến cho tôi trải nghiệm tuyệt vời. Sản phẩm chất lượng và dịch vụ chuyên nghiệp!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">MN</div>
                        <div>
                            <h4>Minh Ngọc</h4>
                            <p>Nhà thiết kế</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">"Tôi rất ấn tượng với sự sáng tạo và chuyên nghiệp của đội ngũ Hảo SayGex. Đáng đồng tiền bát gạo!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">TH</div>
                        <div>
                            <h4>Trung Hiếu</h4>
                            <p>Doanh nhân</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">"Không thể tin được chất lượng dịch vụ tại đây. Từ nay tôi sẽ chỉ sử dụng Hảo SayGex cho mọi nhu cầu!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">LA</div>
                        <div>
                            <h4>Lan Anh</h4>
                            <p>Content Creator</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Hảo SayGex</h3>
                    <p>Nền tảng sáng tạo và đổi mới, mang đến những giải pháp độc đáo cho mọi khách hàng.</p>
                </div>
                <div class="footer-column">
                    <h3>Liên Kết Nhanh</h3>
                    <ul>
                        <li><a href="#">Trang Chủ</a></li>
                        <li><a href="#">Về Chúng Tôi</a></li>
                        <li><a href="#">Dịch Vụ</a></li>
                        <li><a href="#">Sản Phẩm</a></li>
                        <li><a href="#">Liên Hệ</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Dịch Vụ</h3>
                    <ul>
                        <li><a href="#">Thiết Kế Sáng Tạo</a></li>
                        <li><a href="#">Phát Triển Web</a></li>
                        <li><a href="#">Tư Vấn Chiến Lược</a></li>
                        <li><a href="#">Marketing Digital</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Liên Hệ</h3>
                    <ul>
                        <li>Địa chỉ: 123 Đường ABC, Quận 1, TP.HCM</li>
                        <li>Điện thoại: (0123) 456-7890</li>
                        <li>Email: info@haosaygex.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Hảo SayGex. Tất cả các quyền được bảo lưu.</p>
            </div>
        </div>
    </footer>
</body>
</html>
