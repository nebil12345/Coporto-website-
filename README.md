# coporto website
Factories website development 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coporto - Professional Website Development Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #7c3aed;
            --accent: #06b6d4;
            --light: #f8fafc;
            --dark: #1e293b;
            --gray: #64748b;
            --success: #10b981;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: #ffffff;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.1rem;
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
            text-align: center;
            box-shadow: 0 4px 6px rgba(37, 99, 235, 0.2);
        }

        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(37, 99, 235, 0.3);
        }

        .btn-secondary {
            background: var(--secondary);
            box-shadow: 0 4px 6px rgba(124, 58, 237, 0.2);
        }

        .btn-secondary:hover {
            background: #6d28d9;
            box-shadow: 0 6px 12px rgba(124, 58, 237, 0.3);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            box-shadow: none;
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
            position: fixed;
            width: 100%;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 1.2rem;
            margin-right: 10px;
        }

        .logo-text {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--dark);
        }

        .logo-text span {
            color: var(--primary);
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
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            bottom: -5px;
            left: 0;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--dark);
        }

        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.1) 0%, rgba(124, 58, 237, 0.1) 100%);
            top: -250px;
            right: -150px;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(6, 182, 212, 0.1) 0%, rgba(37, 99, 235, 0.1) 100%);
            bottom: -150px;
            left: -100px;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: relative;
            z-index: 1;
        }

        .hero-text {
            flex: 1;
            max-width: 600px;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .hero-text h1 span {
            color: var(--primary);
            position: relative;
        }

        .hero-text h1 span::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 8px;
            background: rgba(37, 99, 235, 0.2);
            bottom: 5px;
            left: 0;
            z-index: -1;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--gray);
            margin-bottom: 30px;
            max-width: 500px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        .hero-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            transform: perspective(1000px) rotateY(-5deg) rotateX(5deg);
            transition: transform 0.5s ease;
        }

        .hero-image img:hover {
            transform: perspective(1000px) rotateY(0) rotateX(0);
        }

        /* Services Section */
        .services {
            background-color: var(--light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: white;
            border-radius: 12px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            color: white;
            font-size: 1.8rem;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .service-card p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .service-link {
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            transition: all 0.3s ease;
        }

        .service-link i {
            margin-left: 5px;
            transition: transform 0.3s ease;
        }

        .service-link:hover i {
            transform: translateX(5px);
        }

        /* Process Section */
        .process-steps {
            display: flex;
            justify-content: space-between;
            position: relative;
            margin-top: 50px;
        }

        .process-steps::before {
            content: '';
            position: absolute;
            top: 40px;
            left: 0;
            width: 100%;
            height: 2px;
            background: #e2e8f0;
            z-index: 1;
        }

        .process-step {
            text-align: center;
            position: relative;
            z-index: 2;
            flex: 1;
        }

        .step-number {
            width: 80px;
            height: 80px;
            background: white;
            border: 2px solid #e2e8f0;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            position: relative;
            transition: all 0.3s ease;
        }

        .process-step.active .step-number {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .step-content h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .step-content p {
            color: var(--gray);
            max-width: 250px;
            margin: 0 auto;
        }

        /* Portfolio Section */
        .portfolio {
            background-color: var(--light);
        }

        .portfolio-filters {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 40px;
        }

        .filter-btn {
            padding: 8px 20px;
            background: white;
            border: 1px solid #e2e8f0;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            background: white;
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .portfolio-image {
            height: 250px;
            overflow: hidden;
        }

        .portfolio-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .portfolio-item:hover .portfolio-image img {
            transform: scale(1.05);
        }

        .portfolio-content {
            padding: 20px;
        }

        .portfolio-content h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .portfolio-content p {
            color: var(--gray);
            margin-bottom: 15px;
        }

        .portfolio-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .portfolio-tag {
            background: #f1f5f9;
            color: var(--gray);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
        }

        /* Testimonials Section */
        .testimonials {
            position: relative;
        }

        .testimonials::before {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.05) 0%, rgba(124, 58, 237, 0.05) 100%);
            top: -150px;
            right: -150px;
            z-index: -1;
        }

        .testimonials-container {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }

        .testimonial-card {
            background: white;
            border-radius: 12px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            margin: 20px;
            position: relative;
        }

        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 30px;
            font-size: 5rem;
            color: #e2e8f0;
            line-height: 1;
            font-family: Georgia, serif;
        }

        .testimonial-content {
            position: relative;
            z-index: 1;
        }

        .testimonial-text {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 25px;
            font-style: italic;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
        }

        .author-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }

        .author-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .author-info h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
            color: var(--dark);
        }

        .author-info p {
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Pricing Section */
        .pricing {
            background-color: var(--light);
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .pricing-card {
            background: white;
            border-radius: 12px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 0, 0, 0.05);
            position: relative;
        }

        .pricing-card.featured {
            border: 2px solid var(--primary);
            transform: scale(1.05);
        }

        .pricing-card.featured::before {
            content: 'Most Popular';
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            color: white;
            padding: 5px 20px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .pricing-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .pricing-card.featured:hover {
            transform: scale(1.05) translateY(-10px);
        }

        .pricing-header {
            margin-bottom: 30px;
        }

        .pricing-name {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .pricing-price {
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .pricing-period {
            color: var(--gray);
        }

        .pricing-features {
            list-style: none;
            margin-bottom: 30px;
            text-align: left;
        }

        .pricing-features li {
            padding: 10px 0;
            border-bottom: 1px solid #f1f5f9;
            display: flex;
            align-items: center;
        }

        .pricing-features li i {
            color: var(--success);
            margin-right: 10px;
            font-size: 0.9rem;
        }

        /* Contact Section */
        .contact-container {
            display: flex;
            gap: 50px;
        }

        .contact-info {
            flex: 1;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .contact-info p {
            color: var(--gray);
            margin-bottom: 30px;
        }

        .contact-details {
            margin: 30px 0;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: var(--primary);
            font-size: 1.2rem;
        }

        .contact-text h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .contact-form {
            flex: 1;
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #e2e8f0;
            border-radius: 6px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            text-align: center;
            padding: 80px 0;
        }

        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .cta p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
        }

        .cta .btn {
            background: white;
            color: var(--primary);
        }

        .cta .btn:hover {
            background: rgba(255, 255, 255, 0.9);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 80px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: white;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 3px;
            background: var(--primary);
            bottom: 0;
            left: 0;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #cbd5e1;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: white;
        }

        .footer-about p {
            color: #cbd5e1;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #94a3b8;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                margin-bottom: 50px;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .contact-container {
                flex-direction: column;
            }
            
            .pricing-card.featured {
                transform: scale(1);
            }
            
            .pricing-card.featured:hover {
                transform: translateY(-10px);
            }
        }

        @media (max-width: 768px) {
            .navbar {
                padding: 15px 0;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                flex-direction: column;
                background: white;
                text-align: center;
                transition: 0.3s;
                box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
                padding: 20px 0;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero-text h1 {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .process-steps {
                flex-direction: column;
                gap: 40px;
            }
            
            .process-steps::before {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">
                    <div class="logo-icon">C</div>
                    <div class="logo-text">Coporto<span>.</span></div>
                </a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#process">Process</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>We Create <span>Digital Experiences</span> That Drive Growth</h1>
                    <p>Coporto is a premier web development agency specializing in creating stunning, high-performance websites and applications that help businesses thrive in the digital world.</p>
                    <div class="hero-buttons">
                        <a href="#portfolio" class="btn">View Our Work</a>
                        <a href="#contact" class="btn btn-outline">Get In Touch</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80" alt="Web Development">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>We offer a comprehensive range of web development services to help your business succeed online</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>Custom Web Development</h3>
                    <p>Tailored websites and web applications built with the latest technologies to meet your specific business needs.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3>E-Commerce Solutions</h3>
                    <p>Complete online stores with secure payment processing, inventory management, and marketing tools.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Responsive Design</h3>
                    <p>Websites that look and function perfectly on all devices, from desktops to smartphones.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-search"></i>
                    </div>
                    <h3>SEO Optimization</h3>
                    <p>Improve your search engine rankings and drive more organic traffic to your website.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tachometer-alt"></i>
                    </div>
                    <h3>Website Maintenance</h3>
                    <p>Ongoing support, updates, and security monitoring to keep your website running smoothly.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>Web Hosting</h3>
                    <p>Fast, secure, and reliable hosting solutions with 99.9% uptime guarantee.</p>
                    <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>Our Portfolio</h2>
                <p>Take a look at some of our recent projects that showcase our expertise and creativity</p>
            </div>
            <div class="portfolio-filters">
                <button class="filter-btn active">All</button>
                <button class="filter-btn">E-Commerce</button>
                <button class="filter-btn">Corporate</button>
                <button class="filter-btn">Web Apps</button>
                <button class="filter-btn">Landing Pages</button>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="E-Commerce Website">
                    </div>
                    <div class="portfolio-content">
                        <h3>Modern Fashion Store</h3>
                        <p>A fully responsive e-commerce website with integrated payment processing and inventory management.</p>
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">E-Commerce</span>
                            <span class="portfolio-tag">WordPress</span>
                            <span class="portfolio-tag">WooCommerce</span>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1115&q=80" alt="Corporate Website">
                    </div>
                    <div class="portfolio-content">
                        <h3>Tech Solutions Inc.</h3>
                        <p>A corporate website with custom CMS, lead generation forms, and integration with CRM systems.</p>
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">Corporate</span>
                            <span class="portfolio-tag">React</span>
                            <span class="portfolio-tag">Node.js</span>
                        </div>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Web Application">
                    </div>
                    <div class="portfolio-content">
                        <h3>Project Management Tool</h3>
                        <p>A custom web application for project tracking with real-time collaboration features.</p>
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">Web App</span>
                            <span class="portfolio-tag">Vue.js</span>
                            <span class="portfolio-tag">Firebase</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section class="process" id="process">
        <div class="container">
            <div class="section-title">
                <h2>Our Process</h2>
                <p>We follow a structured approach to ensure every project is delivered on time and exceeds expectations</p>
            </div>
            <div class="process-steps">
                <div class="process-step active">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3>Discovery & Planning</h3>
                        <p>We begin by understanding your business goals, target audience, and project requirements.</p>
                    </div>
                </div>
                <div class="process-step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3>Design & Prototyping</h3>
                        <p>We create wireframes and design mockups to visualize the final product before development.</p>
                    </div>
                </div>
                <div class="process-step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3>Development</h3>
                        <p>Our developers bring the designs to life using the latest technologies and best practices.</p>
                    </div>
                </div>
                <div class="process-step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3>Testing & Launch</h3>
                        <p>We thoroughly test the website and deploy it to a live environment once everything is perfect.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Client Testimonials</h2>
                <p>See what our clients have to say about working with us</p>
            </div>
            <div class="testimonials-container">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <div class="testimonial-text">
                            "Working with Coporto was a game-changer for our business. They delivered a website that not only looks amazing but has significantly increased our online conversions. Their team was professional, responsive, and truly understood our vision."
                        </div>
                        <div class="testimonial-author">
                            <div class="author-avatar">
                                <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah Johnson">
                            </div>
                            <div class="author-info">
                                <h4>Sarah Johnson</h4>
                                <p>Marketing Director, TechGrowth Inc.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="pricing" id="pricing">
        <div class="container">
            <div class="section-title">
                <h2>Pricing Plans</h2>
                <p>Choose the plan that works best for your business needs and budget</p>
            </div>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3 class="pricing-name">Starter</h3>
                        <div class="pricing-price">$1,499</div>
                        <div class="pricing-period">one-time fee</div>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> 5 Page Website</li>
                        <li><i class="fas fa-check"></i> Responsive Design</li>
                        <li><i class="fas fa-check"></i> Basic SEO Setup</li>
                        <li><i class="fas fa-check"></i> Contact Form</li>
                        <li><i class="fas fa-times"></i> E-Commerce Functionality</li>
                        <li><i class="fas fa-times"></i> Custom CMS</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Get Started</a>
                </div>
                <div class="pricing-card featured">
                    <div class="pricing-header">
                        <h3 class="pricing-name">Business</h3>
                        <div class="pricing-price">$3,999</div>
                        <div class="pricing-period">one-time fee</div>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Up to 15 Pages</li>
                        <li><i class="fas fa-check"></i> Responsive Design</li>
                        <li><i class="fas fa-check"></i> Advanced SEO</li>
                        <li><i class="fas fa-check"></i> Custom Design</li>
                        <li><i class="fas fa-check"></i> Basic E-Commerce</li>
                        <li><i class="fas fa-check"></i> Custom CMS</li>
                    </ul>
                    <a href="#contact" class="btn">Get Started</a>
                </div>
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3 class="pricing-name">Enterprise</h3>
                        <div class="pricing-price">$7,999</div>
                        <div class="pricing-period">one-time fee</div>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Unlimited Pages</li>
                        <li><i class="fas fa-check"></i> Fully Custom Design</li>
                        <li><i class="fas fa-check"></i> Comprehensive SEO</li>
                        <li><i class="fas fa-check"></i> Advanced E-Commerce</li>
                        <li><i class="fas fa-check"></i> Custom Web Application</li>
                        <li><i class="fas fa-check"></i> Ongoing Support</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Get Started</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Ready to start your project? Get in touch with us today for a free consultation</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Let's Talk About Your Project</h3>
                    <p>We're excited to learn about your business and discuss how we can help you achieve your goals with a custom web solution.</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Our Office</h4>
                                <p>123 Business Avenue, Suite 100<br>New York, NY 10001</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Phone</h4>
                                <p>+1 (555) 123-4567</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Email</h4>
                                <p>hello@coporto.com</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <label for="company">Company</label>
                            <input type="text" id="company" class="form-control" placeholder="Your Company">
                        </div>
                        <div class="form-group">
                            <label for="budget">Project Budget</label>
                            <select id="budget" class="form-control">
                                <option value="">Select Budget Range</option>
                                <option value="1k-5k">$1,000 - $5,000</option>
                                <option value="5k-10k">$5,000 - $10,000</option>
                                <option value="10k-25k">$10,000 - $25,000</option>
                                <option value="25k+">$25,000+</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">Project Details</label>
                            <textarea id="message" class="form-control" placeholder="Tell us about your project..." required></textarea>
                        </div>
                        <button type="submit" class="btn" style="width: 100%;">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="container">
            <h2>Ready to Transform Your Online Presence?</h2>
            <p>Let's work together to create a website that not only looks great but also drives results for your business.</p>
            <a href="#contact" class="btn">Start Your Project Today</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Coporto</h3>
                    <div class="footer-about">
                        <p>We are a passionate team of web developers and designers dedicated to creating exceptional digital experiences that help businesses grow.</p>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#portfolio">Portfolio</a></li>
                        <li><a href="#process">Our Process</a></li>
                        <li><a href="#pricing">Pricing</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Custom Web Development</a></li>
                        <li><a href="#">E-Commerce Solutions</a></li>
                        <li><a href="#">Responsive Design</a></li>
                        <li><a href="#">SEO Optimization</a></li>
                        <li><a href="#">Website Maintenance</a></li>
                        <li><a href="#">Web Hosting</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i> 123 Business Avenue, Suite 100</li>
                        <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                        <li><i class="fas fa-envelope"></i> hello@coporto.com</li>
                        <li><i class="fas fa-clock"></i> Mon-Fri: 9am-6pm</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Coporto Web Development. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Header background change on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if(window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.backgroundColor = 'white';
                header.style.backdropFilter = 'none';
            }
        });

        // Portfolio filtering
        const filterButtons = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');

        filterButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons
                filterButtons.forEach(btn => btn.classList.remove('active'));
                // Add active class to clicked button
                button.classList.add('active');
                
                const filterValue = button.textContent;
                
                portfolioItems.forEach(item => {
                    if(filterValue === 'All' || item.querySelector('.portfolio-tags').textContent.includes(filterValue)) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });

        // Process steps animation on scroll
        const processSteps = document.querySelectorAll('.process-step');
        
        const observerOptions = {
            threshold: 0.5
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);
        
        processSteps.forEach(step => {
            observer.observe(step);
        });

        // Form submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // In a real application, you would send the form data to a server here
            alert('Thank you for your message! We will get back to you soon.');
            contactForm.reset();
        });
    </script>
</body>
</html>
