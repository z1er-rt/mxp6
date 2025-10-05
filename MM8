<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر النخبة - تسوق بذكاء</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --success-color: #2ecc71;
            --danger-color: #ff4757;
            --warning-color: #ffa502;
            --dark: #2c3e50;
            --light: #ecf0f1;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            position: relative;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><rect width="100" height="100" fill="none"/><circle cx="50" cy="50" r="1" fill="white" opacity="0.1"/></svg>');
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Styles */
        header {
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(20px);
            padding: 20px 0;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid transparent;
            border-image: var(--primary-gradient) 1;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 30px;
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo {
            font-size: 32px;
            font-weight: 900;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -1px;
        }

        .logo-subtitle {
            font-size: 12px;
            color: #666;
            font-weight: 500;
        }

        nav {
            display: flex;
            gap: 40px;
        }

        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: all 0.3s;
            position: relative;
            padding: 5px 10px;
            font-size: 16px;
        }

        nav a:hover {
            color: #667eea;
            transform: translateY(-2px);
        }

        nav a.active {
            color: #667eea;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 10px;
            right: 10px;
            height: 3px;
            background: var(--primary-gradient);
            transform: scaleX(0);
            transition: transform 0.3s;
            border-radius: 2px;
        }

        nav a:hover::after,
        nav a.active::after {
            transform: scaleX(1);
        }

        .header-actions {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        .search-box {
            position: relative;
        }

        .search-box input {
            padding: 10px 40px 10px 20px;
            border: 2px solid #eee;
            border-radius: 25px;
            width: 250px;
            transition: all 0.3s;
            font-size: 14px;
        }

        .search-box input:focus {
            outline: none;
            border-color: #667eea;
            width: 300px;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .search-box::after {
            content: '🔍';
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 16px;
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
            font-size: 28px;
            transition: all 0.3s;
            padding: 10px;
            border-radius: 50%;
        }

        .cart-icon:hover {
            background: rgba(102, 126, 234, 0.1);
            transform: scale(1.1);
        }

        .cart-count {
            position: absolute;
            top: 0;
            left: 0;
            background: var(--danger-color);
            color: white;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            font-weight: bold;
            animation: pulse 2s infinite;
            box-shadow: 0 2px 8px rgba(255, 71, 87, 0.4);
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Hero Section */
        .hero {
            background: white;
            border-radius: 30px;
            padding: 80px;
            margin: 30px 0;
            text-align: center;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            animation: fadeInUp 0.8s;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.05) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 56px;
            color: var(--dark);
            margin-bottom: 20px;
            font-weight: 900;
            line-height: 1.2;
        }

        .hero h1 .highlight {
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 22px;
            color: #666;
            margin-bottom: 40px;
            line-height: 1.6;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 60px;
            margin-top: 40px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 36px;
            font-weight: bold;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            font-size: 14px;
            color: #666;
            margin-top: 5px;
        }

        .btn {
            background: var(--primary-gradient);
            color: white;
            border: none;
            padding: 18px 50px;
            border-radius: 50px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.4s;
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            transition: left 0.5s;
        }

        .btn:hover::before {
            left: 100%;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(102, 126, 234, 0.6);
        }

        .btn:active {
            transform: translateY(-1px);
        }

        /* Category Filter */
        .category-filter {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .category-btn {
            padding: 12px 30px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            background: rgba(255, 255, 255, 0.9);
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            color: var(--dark);
            backdrop-filter: blur(10px);
        }

        .category-btn:hover,
        .category-btn.active {
            background: white;
            border-color: #667eea;
            color: #667eea;
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        /* Products Grid */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin: 30px 0;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.4s;
            animation: fadeInUp 0.6s;
            position: relative;
            overflow: hidden;
        }

        .product-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: var(--primary-gradient);
            transform: scaleX(0);
            transition: transform 0.4s;
        }

        .product-card:hover::before {
            transform: scaleX(1);
        }

        .product-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.2);
        }

        .product-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: var(--danger-color);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
            z-index: 10;
        }

        .product-badge.new {
            background: var(--success-color);
        }

        .product-badge.sale {
            background: var(--warning-color);
        }

        .product-image {
            width: 100%;
            height: 220px;
            background: var(--secondary-gradient);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 70px;
            margin-bottom: 20px;
            transition: all 0.3s;
            cursor: pointer;
        }

        .product-card:hover .product-image {
            transform: scale(1.05);
        }

        .product-title {
            font-size: 22px;
            font-weight: bold;
            color: var(--dark);
            margin-bottom: 12px;
        }

        .product-description {
            color: #666;
            font-size: 15px;
            margin-bottom: 20px;
            line-height: 1.6;
            min-height: 48px;
        }

        .product-rating {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }

        .stars {
            color: #ffa502;
            font-size: 18px;
        }

        .rating-count {
            color: #999;
            font-size: 14px;
        }

        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
        }

        .product-price {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .price-current {
            font-size: 28px;
            font-weight: bold;
            color: #667eea;
        }

        .price-old {
            font-size: 16px;
            color: #999;
            text-decoration: line-through;
        }

        .add-to-cart {
            background: var(--primary-gradient);
            color: white;
            border: none;
            padding: 14px 28px;
            border-radius: 12px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 15px;
        }

        .add-to-cart:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.4);
        }

        /* Cart Page */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        .cart-items {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin: 30px 0;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eee;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 25px;
            margin-bottom: 15px;
            background: #f8f9ff;
            border-radius: 15px;
            animation: slideIn 0.3s;
            transition: all 0.3s;
        }

        .cart-item:hover {
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transform: translateX(-5px);
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .item-info {
            display: flex;
            gap: 25px;
            align-items: center;
            flex: 1;
        }

        .item-image {
            width: 100px;
            height: 100px;
            background: var(--secondary-gradient);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }

        .item-details h3 {
            font-size: 20px;
            margin-bottom: 8px;
            color: var(--dark);
        }

        .item-details p {
            color: #666;
            font-size: 14px;
        }

        .quantity-controls {
            display: flex;
            gap: 15px;
            align-items: center;
            background: white;
            padding: 8px 15px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        .quantity-btn {
            background: #667eea;
            color: white;
            border: none;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            font-size: 18px;
        }

        .quantity-btn:hover {
            background: #764ba2;
            transform: scale(1.15);
        }

        .quantity-display {
            font-weight: bold;
            font-size: 18px;
            min-width: 30px;
            text-align: center;
        }

        .item-price {
            font-size: 24px;
            font-weight: bold;
            color: #667eea;
            min-width: 120px;
            text-align: center;
        }

        .remove-btn {
            background: var(--danger-color);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
        }

        .remove-btn:hover {
            background: #ee5a6f;
            transform: scale(1.05);
        }

        .cart-summary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            border-radius: 20px;
            margin-top: 30px;
        }

        .summary-row {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .summary-row:last-child {
            border-bottom: none;
            padding-top: 25px;
            margin-top: 10px;
            border-top: 2px solid rgba(255, 255, 255, 0.3);
        }

        .summary-label {
            font-size: 18px;
            font-weight: 500;
        }

        .summary-value {
            font-size: 18px;
            font-weight: bold;
        }

        .total-price {
            font-size: 36px !important;
            font-weight: 900 !important;
        }

        .promo-code {
            display: flex;
            gap: 10px;
            margin: 20px 0;
        }

        .promo-code input {
            flex: 1;
            padding: 15px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            border-radius: 12px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 16px;
        }

        .promo-code input::placeholder {
            color: rgba(255, 255, 255, 0.6);
        }

        .promo-code input:focus {
            outline: none;
            border-color: white;
            background: rgba(255, 255, 255, 0.2);
        }

        .promo-code button {
            padding: 15px 30px;
            background: white;
            color: #667eea;
            border: none;
            border-radius: 12px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        .promo-code button:hover {
            transform: scale(1.05);
        }

        /* Checkout Form */
        .checkout-form {
            background: white;
            border-radius: 20px;
            padding: 50px;
            margin: 30px 0;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        }

        .checkout-form h2 {
            font-size: 32px;
            margin-bottom: 40px;
            color: var(--dark);
            text-align: center;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .form-group {
            margin-bottom: 30px;
        }

        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: var(--dark);
            font-size: 15px;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 16px 20px;
            border: 2px solid #eee;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s;
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 4px rgba(102, 126, 234, 0.1);
        }

        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .payment-method {
            padding: 25px;
            border: 3px solid #eee;
            border-radius: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            background: white;
        }

        .payment-method:hover {
            border-color: #667eea;
            background: #f8f9ff;
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .payment-method.selected {
            border-color: #667eea;
            background: var(--primary-gradient);
            color: white;
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .payment-icon {
            font-size: 40px;
            margin-bottom: 12px;
        }

        .payment-name {
            font-weight: 600;
            font-size: 15px;
        }

        /* Contact Page */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1.5fr;
            gap: 40px;
            margin: 30px 0;
        }

        .contact-info {
            background: white;
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        }

        .contact-info h2 {
            font-size: 28px;
            margin-bottom: 35px;
            color: var(--dark);
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 30px;
            padding: 25px;
            background: #f8f9ff;
            border-radius: 15px;
            transition: all 0.3s;
        }

        .contact-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        .contact-icon {
            font-size: 35px;
            min-width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--primary-gradient);
            border-radius: 12px;
        }

        .contact-details strong {
            display: block;
            margin-bottom: 8px;
            color: var(--dark);
            font-size: 18px;
        }

        .contact-details p {
            color: #666;
            line-height: 1.6;
            font-size: 15px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            background: var(--primary-gradient);
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.4);
        }

        /* Empty Cart */
        .empty-cart {
            text-align: center;
            padding: 80px 20px;
            color: #666;
        }

        .empty-cart-icon {
            font-size: 100px;
            margin-bottom: 25px;
            opacity: 0.4;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .empty-cart h2 {
            font-size: 32px;
            margin-bottom: 15px;
            color: var(--dark);
        }

        /* Success Message */
        .success-message {
            background: linear-gradient(135deg, var(--success-color) 0%, #27ae60 100%);
            color: white;
            padding: 25px 30px;
            border-radius: 15px;
            text-align: center;
            margin: 25px 0;
            display: none;
            animation: slideDown 0.5s;
            box-shadow: 0 10px 30px rgba(46, 204, 113, 0.3);
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .success-message.show {
            display: block;
        }

        /* Loading Animation */
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }

            nav {
                flex-wrap: wrap;
                justify-content: center;
                gap: 20px;
            }

            .search-box input {
                width: 200px;
            }

            .search-box input:focus {
                width: 220px;
            }

            .hero {
                padding: 50px 30px;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }

            .hero-stats {
                flex-direction: column;
                gap: 30px;
            }

            .products-grid {
                grid-template-columns: 1fr;
            }

            .cart-item {
                flex-direction: column;
                gap: 20px;
            }

            .item-info {
                flex-direction: column;
                text-align: center;
            }

            .checkout-form,
            .contact-info {
                padding: 30px 20px;
            }

            .payment-methods {
                grid-template-columns: 1fr;
            }
        }

        /* Notification Toast */
        .toast {
            position: fixed;
            top: 100px;
            left: 50%;
            transform: translateX(-50%);
            background: white;
            color: var(--dark);
            padding: 20px 40px;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
            z-index: 10000;
            animation: slideDown 0.5s;
            display: flex;
            align-items: center;
            gap: 15px;
            font-weight: 600;
        }

        .toast-icon {
            font-size: 28px;
        }

        /* Wishlist Badge */
        .wishlist-btn {
            position: absolute;
            top: 20px;
            left: 20px;
            background: white;
            border: none;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            z-index: 10;
        }

        .wishlist-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }

        .wishlist-btn.active {
            color: #ff4757;
        }

        /* Quick View Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 10000;
            align-items: center;
            justify-content: center;
            animation: fadeIn 0.3s;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            border-radius: 25px;
            padding: 50px;
            max-width: 600px;
            width: 90%;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            animation: scaleIn 0.3s;
        }

        @keyframes scaleIn {
            from {
                transform: scale(0.9);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        .modal-close {
            position: absolute;
            top: 20px;
            left: 20px;
            background: #ff4757;
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            font-size: 24px;
            cursor: pointer;
            transition: all 0.3s;
        }

        .modal-close:hover {
            transform: rotate(90deg);
            background: #ee5a6f;
        }

        .discount-banner {
            background: linear-gradient(135deg, #ffa502 0%, #ff6348 100%);
            color: white;
            text-align: center;
            padding: 15px;
            font-weight: bold;
            animation: slideDown 0.5s;
        }
    </style>
</head>
<body>
    <!-- Discount Banner -->
    <div class="discount-banner" id="discountBanner">
        🎉 عرض خاص: خصم 20% على جميع المنتجات! استخدم كود: SAVE20
    </div>

    <header>
        <div class="header-content">
            <div class="logo-container">
                <div>
                    <div class="logo">🛍️ متجر النخبة</div>
                    <div class="logo-subtitle">تسوق بذكاء واحترافية</div>
                </div>
            </div>
            <nav>
                <a href="#" class="nav-link active" data-page="home">🏠 الرئيسية</a>
                <a href="#" class="nav-link" data-page="products">📦 المنتجات</a>
                <a href="#" class="nav-link" data-page="cart">🛒 السلة</a>
                <a href="#" class="nav-link" data-page="contact">📞 التواصل</a>
            </nav>
            <div class="header-actions">
                <div class="search-box">
                    <input type="text" id="searchInput" placeholder="ابحث عن منتج..." onkeyup="searchProducts()">
                </div>
                <div class="cart-icon" onclick="showPage('cart')">
                    🛒
                    <span class="cart-count" id="cartCount">0</span>
                </div>
            </div>
        </div>
    </header>

    <div class="container">
        <!-- الصفحة الرئيسية -->
        <div class="page active" id="home">
            <div class="hero">
                <div class="hero-content">
                    <h1>اكتشف عالماً من <span class="highlight">التميز</span></h1>
                    <p>منتجات عالية الجودة بأسعار تنافسية وخدمة توصيل سريعة</p>
                    <button class="btn" onclick="showPage('products')">ابدأ التسوق الآن 🚀</button>
                    <div class="hero-stats">
                        <div class="stat-item">
                            <div class="stat-number">500+</div>
                            <div class="stat-label">منتج متوفر</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">10K+</div>
                            <div class="stat-label">عميل سعيد</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">24/7</div>
                            <div class="stat-label">دعم فني</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحة المنتجات -->
        <div class="page" id="products">
            <div class="hero" style="padding: 40px;">
                <h1>تصفح <span class="highlight">منتجاتنا</span></h1>
                <p>اختر من بين مجموعة واسعة من المنتجات المميزة</p>
            </div>
            
            <div class="category-filter">
                <button class="category-btn active" onclick="filterCategory('all')">الكل</button>
                <button class="category-btn" onclick="filterCategory('electronics')">إلكترونيات</button>
                <button class="category-btn" onclick="filterCategory('fashion')">أزياء</button>
                <button class="category-btn" onclick="filterCategory('home')">منزل</button>
                <button class="category-btn" onclick="filterCategory('sports')">رياضة</button>
            </div>

            <div class="products-grid" id="productsGrid"></div>
        </div>

        <!-- صفحة السلة -->
        <div class="page" id="cart">
            <div class="hero" style="padding: 40px;">
                <h1>سلة <span class="highlight">التسوق</span></h1>
                <p>راجع مشترياتك قبل إتمام الطلب</p>
            </div>
            <div class="cart-items" id="cartItems"></div>
            
            <div class="checkout-form" id="checkoutForm" style="display: none;">
                <h2>🎁 إتمام الطلب</h2>
                <div id="successMessage" class="success-message"></div>
                <form onsubmit="submitOrder(event)">
                    <div class="form-row">
                        <div class="form-group">
                            <label>الاسم الأول *</label>
                            <input type="text" required placeholder="محمد">
                        </div>
                        <div class="form-group">
                            <label>الاسم الأخير *</label>
                            <input type="text" required placeholder="أحمد">
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label>رقم الهاتف *</label>
                            <input type="tel" required placeholder="05xxxxxxxx" pattern="[0-9]{10}">
                        </div>
                        <div class="form-group">
                            <label>البريد الإلكتروني *</label>
                            <input type="email" required placeholder="example@email.com">
                        </div>
                    </div>

                    <div class="form-group">
                        <label>المدينة *</label>
                        <select required>
                            <option value="">اختر المدينة</option>
                            <option>الرياض</option>
                            <option>جدة</option>
                            <option>الدمام</option>
                            <option>مكة المكرمة</option>
                            <option>المدينة المنورة</option>
                            <option>الخبر</option>
                            <option>الطائف</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label>العنوان بالتفصيل *</label>
                        <textarea required rows="3" placeholder="الحي، الشارع، رقم المبنى"></textarea>
                    </div>

                    <div class="form-group">
                        <label>طريقة الدفع *</label>
                        <div class="payment-methods">
                            <div class="payment-method" onclick="selectPayment(this, 'cod')">
                                <div class="payment-icon">💵</div>
                                <div class="payment-name">الدفع عند الاستلام</div>
                            </div>
                            <div class="payment-method" onclick="selectPayment(this, 'card')">
                                <div class="payment-icon">💳</div>
                                <div class="payment-name">بطاقة ائتمان</div>
                            </div>
                            <div class="payment-method" onclick="selectPayment(this, 'mada')">
                                <div class="payment-icon">💰</div>
                                <div class="payment-name">مدى</div>
                            </div>
                            <div class="payment-method" onclick="selectPayment(this, 'stc')">
                                <div class="payment-icon">📱</div>
                                <div class="payment-name">STC Pay</div>
                            </div>
                            <div class="payment-method" onclick="selectPayment(this, 'transfer')">
                                <div class="payment-icon">🏦</div>
                                <div class="payment-name">تحويل بنكي</div>
                            </div>
                            <div class="payment-method" onclick="selectPayment(this, 'apple')">
                                <div class="payment-icon">🍎</div>
                                <div class="payment-name">Apple Pay</div>
                            </div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label>ملاحظات إضافية</label>
                        <textarea rows="3" placeholder="أي ملاحظات أو طلبات خاصة"></textarea>
                    </div>

                    <button type="submit" class="btn" style="width: 100%; padding: 20px; font-size: 20px;">
                        تأكيد الطلب وإرساله 🎉
                    </button>
                </form>
            </div>
        </div>

        <!-- صفحة التواصل -->
        <div class="page" id="contact">
            <div class="hero" style="padding: 40px;">
                <h1>تواصل <span class="highlight">معنا</span></h1>
                <p>نحن هنا لمساعدتك في أي وقت</p>
            </div>
            <div class="contact-grid">
                <div class="contact-info">
                    <h2>📍 معلومات التواصل</h2>
                    
                    <div class="contact-item">
                        <div class="contact-icon">📞</div>
                        <div class="contact-details">
                            <strong>الهاتف</strong>
                            <p>+966 50 123 4567<br>متاح 24/7</p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div class="contact-details">
                            <strong>البريد الإلكتروني</strong>
                            <p>support@elitestore.com<br>نرد خلال 24 ساعة</p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div class="contact-details">
                            <strong>العنوان</strong>
                            <p>شارع الملك فهد، الرياض<br>المملكة العربية السعودية</p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">⏰</div>
                        <div class="contact-details">
                            <strong>ساعات العمل</strong>
                            <p>السبت - الخميس: 9 صباحاً - 10 مساءً<br>الجمعة: 2 ظهراً - 10 مساءً</p>
                        </div>
                    </div>

                    <h3 style="margin: 30px 0 20px;">تابعنا على</h3>
                    <div class="social-links">
                        <a href="#" class="social-link">📘</a>
                        <a href="#" class="social-link">📷</a>
                        <a href="#" class="social-link">🐦</a>
                        <a href="#" class="social-link">💼</a>
                        <a href="#" class="social-link">📱</a>
                    </div>
                </div>

                <div class="checkout-form">
                    <h2>✉️ أرسل رسالة</h2>
                    <div id="contactSuccess" class="success-message"></div>
                    <form onsubmit="submitContact(event)">
                        <div class="form-row">
                            <div class="form-group">
                                <label>الاسم *</label>
                                <input type="text" required placeholder="اسمك الكامل">
                            </div>
                            <div class="form-group">
                                <label>رقم الهاتف</label>
                                <input type="tel" placeholder="05xxxxxxxx">
                            </div>
                        </div>

                        <div class="form-group">
                            <label>البريد الإلكتروني *</label>
                            <input type="email" required placeholder="example@email.com">
                        </div>

                        <div class="form-group">
                            <label>الموضوع *</label>
                            <select required>
                                <option value="">اختر الموضوع</option>
                                <option>استفسار عن منتج</option>
                                <option>شكوى أو مشكلة</option>
                                <option>استفسار عن الطلب</option>
                                <option>اقتراح</option>
                                <option>أخرى</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label>الرسالة *</label>
                            <textarea required rows="6" placeholder="اكتب رسالتك هنا بالتفصيل..."></textarea>
                        </div>

                        <button type="submit" class="btn" style="width: 100%;">
                            إرسال الرسالة 📨
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Quick View Modal -->
    <div class="modal" id="quickViewModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">✕</button>
            <div id="modalContent"></div>
        </div>
    </div>

    <script>
        // المنتجات مع تفاصيل أكثر
        const products = [
            { 
                id: 1, 
                name: 'آيفون 15 برو ماكس', 
                price: 5499, 
                oldPrice: 6299,
                description: 'أحدث إصدار من آيفون بشريحة A17 Pro وكاميرا 48 ميجابكسل', 
                emoji: '📱',
                category: 'electronics',
                rating: 5,
                reviews: 234,
                badge: 'جديد'
            },
            { 
                id: 2, 
                name: 'ساعة أبل الترا 2', 
                price: 3299, 
                oldPrice: 3799,
                description: 'ساعة ذكية متطورة مع GPS وشاشة Retina دائمة', 
                emoji: '⌚',
                category: 'electronics',
                rating: 5,
                reviews: 189,
                badge: 'خصم'
            },
            { 
                id: 3, 
                name: 'إيربودز برو 2', 
                price: 999, 
                oldPrice: 1199,
                description: 'سماعات لاسلكية مع إلغاء ضوضاء نشط', 
                emoji: '🎧',
                category: 'electronics',
                rating: 5,
                reviews: 456,
                badge: 'خصم'
            },
            { 
                id: 4, 
                name: 'ماك بوك برو 16', 
                price: 10999, 
                oldPrice: 12499,
                description: 'لابتوب احترافي بمعالج M3 Max وذاكرة 64GB', 
                emoji: '💻',
                category: 'electronics',
                rating: 5,
                reviews: 123,
                badge: null
            },
            { 
                id: 5, 
                name: 'كاميرا سوني A7R V', 
                price: 15999, 
                oldPrice: 17999,
                description: 'كاميرا ميرورليس احترافية بدقة 61 ميجابكسل', 
                emoji: '📷',
                category: 'electronics',
                rating: 5,
                reviews: 87,
                badge: null
            },
            { 
                id: 6, 
                name: 'آيباد برو 12.9', 
                price: 4799, 
                oldPrice: 5299,
                description: 'تابلت قوي بشريحة M2 وشاشة Liquid Retina XDR', 
                emoji: '📱',
                category: 'electronics',
                rating: 5,
                reviews: 298,
                badge: 'خصم'
            },
            { 
                id: 7, 
                name: 'تلفزيون سامسونج 65"', 
                price: 6499, 
                oldPrice: 7999,
                description: 'شاشة ذكية QLED 4K مع تقنية HDR10+', 
                emoji: '📺',
                category: 'electronics',
                rating: 4,
                reviews: 176,
                badge: 'خصم'
            },
            { 
                id: 8, 
                name: 'كيبورد ميكانيكي RGB', 
                price: 549, 
                oldPrice: 699,
                description: 'لوحة مفاتيح ميكانيكية للألعاب مع إضاءة RGB', 
                emoji: '⌨️',
                category: 'electronics',
                rating: 4,
                reviews: 342,
                badge: null
            },
            { 
                id: 9, 
                name: 'ساعة رولكس', 
                price: 45000, 
                oldPrice: null,
                description: 'ساعة فاخرة أصلية بتصميم كلاسيكي', 
                emoji: '⌚',
                category: 'fashion',
                rating: 5,
                reviews: 45,
                badge: 'جديد'
            },
            { 
                id: 10, 
                name: 'حذاء نايكي اير', 
                price: 599, 
                oldPrice: 799,
                description: 'حذاء رياضي مريح بتقنية Air Zoom', 
                emoji: '👟',
                category: 'sports',
                rating: 4,
                reviews: 567,
                badge: 'خصم'
            },
            { 
                id: 11, 
                name: 'نظارة راي بان', 
                price: 899, 
                oldPrice: 1099,
                description: 'نظارة شمسية أنيقة مع حماية UV', 
                emoji: '🕶️',
                category: 'fashion',
                rating: 4,
                reviews: 234,
                badge: null
            },
            { 
                id: 12, 
                name: 'روبوت مكنسة ذكية', 
                price: 1899, 
                oldPrice: 2299,
                description: 'مكنسة روبوت ذكية مع تقنية AI للتنظيف الذاتي', 
                emoji: '🤖',
                category: 'home',
                rating: 5,
                reviews: 432,
                badge: 'خصم'
            }
        ];

        // السلة
        let cart = [];
        let selectedPayment = '';
        let currentCategory = 'all';

        // عرض المنتجات
        function displayProducts(filter = 'all') {
            const grid = document.getElementById('productsGrid');
            let filteredProducts = products;
            
            if (filter !== 'all') {
                filteredProducts = products.filter(p => p.category === filter);
            }
            
            grid.innerHTML = filteredProducts.map(product => {
                const stars = '⭐'.repeat(product.rating);
                const badgeHTML = product.badge ? 
                    `<div class="product-badge ${product.badge === 'جديد' ? 'new' : 'sale'}">${product.badge}</div>` : '';
                const oldPriceHTML = product.oldPrice ? 
                    `<div class="price-old">${product.oldPrice} ريال</div>` : '';
                
                return `
                <div class="product-card" data-category="${product.category}">
                    <button class="wishlist-btn" onclick="toggleWishlist(this, ${product.id})">🤍</button>
                    ${badgeHTML}
                    <div class="product-image" onclick="quickView(${product.id})">${product.emoji}</div>
                    <div class="product-title">${product.name}</div>
                    <div class="product-rating">
                        <span class="stars">${stars}</span>
                        <span class="rating-count">(${product.reviews} تقييم)</span>
                    </div>
                    <div class="product-description">${product.description}</div>
                    <div class="product-footer">
                        <div class="product-price">
                            <div class="price-current">${product.price} ريال</div>
                            ${oldPriceHTML}
                        </div>
                        <button class="add-to-cart" onclick="addToCart(${product.id})">
                            أضف 🛒
                        </button>
                    </div>
                </div>
            `}).join('');
        }

        // تصفية حسب الفئة
        function filterCategory(category) {
            currentCategory = category;
            displayProducts(category);
            
            document.querySelectorAll('.category-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
        }

        // البحث عن المنتجات
        function searchProducts() {
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            const grid = document.getElementById('productsGrid');
            
            let filteredProducts = products.filter(p => 
                p.name.toLowerCase().includes(searchTerm) || 
                p.description.toLowerCase().includes(searchTerm)
            );
            
            if (currentCategory !== 'all') {
                filteredProducts = filteredProducts.filter(p => p.category === currentCategory);
            }
            
            grid.innerHTML = filteredProducts.map(product => {
                const stars = '⭐'.repeat(product.rating);
                const badgeHTML = product.badge ? 
                    `<div class="product-badge ${product.badge === 'جديد' ? 'new' : 'sale'}">${product.badge}</div>` : '';
                const oldPriceHTML = product.oldPrice ? 
                    `<div class="price-old">${product.oldPrice} ريال</div>` : '';
                
                return `
                <div class="product-card">
                    <button class="wishlist-btn" onclick="toggleWishlist(this, ${product.id})">🤍</button>
                    ${badgeHTML}
                    <div class="product-image" onclick="quickView(${product.id})">${product.emoji}</div>
                    <div class="product-title">${product.name}</div>
                    <div class="product-rating">
                        <span class="stars">${stars}</span>
                        <span class="rating-count">(${product.reviews} تقييم)</span>
                    </div>
                    <div class="product-description">${product.description}</div>
                    <div class="product-footer">
                        <div class="product-price">
                            <div class="price-current">${product.price} ريال</div>
                            ${oldPriceHTML}
                        </div>
                        <button class="add-to-cart" onclick="addToCart(${product.id})">
                            أضف 🛒
                        </button>
                    </div>
                </div>
            `}).join('');
        }

        // إضافة للسلة
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);
            
            if (existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({ ...product, quantity: 1 });
            }
            
            updateCart();
            showToast('✅ تم إضافة المنتج للسلة بنجاح');
        }

        // تحديث السلة
        function updateCart() {
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            document.getElementById('cartCount').textContent = totalItems;
            displayCart();
        }

        // عرض السلة
        function displayCart() {
            const container = document.getElementById('cartItems');
            const checkoutForm = document.getElementById('checkoutForm');
            
            if (cart.length === 0) {
                container.innerHTML = `
                    <div class="empty-cart">
                        <div class="empty-cart-icon">🛒</div>
                        <h2>سلة التسوق فارغة</h2>
                        <p>ابدأ بإضافة منتجات رائعة إلى سلتك الآن</p>
                        <button class="btn" onclick="showPage('products')" style="margin-top: 25px;">
                            تصفح المنتجات 🚀
                        </button>
                    </div>
                `;
                checkoutForm.style.display = 'none';
                return;
            }

            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const shipping = subtotal > 200 ? 0 : 30;
            const discount = 0; // يمكن تطبيق الكوبون لاحقاً
            const total = subtotal + shipping - discount;
            
            container.innerHTML = `
                <div class="cart-header">
                    <h2 style="font-size: 28px;">🛍️ المنتجات (${cart.length})</h2>
                    <button class="remove-btn" onclick="clearCart()">مسح السلة</button>
                </div>
                ${cart.map(item => `
                    <div class="cart-item">
                        <div class="item-info">
                            <div class="item-image">${item.emoji}</div>
                            <div class="item-details">
                                <h3>${item.name}</h3>
                                <p>${item.description}</p>
                            </div>
                        </div>
                        <div style="display: flex; gap: 25px; align-items: center;">
                            <div class="quantity-controls">
                                <button class="quantity-btn" onclick="decreaseQuantity(${item.id})">−</button>
                                <span class="quantity-display">${item.quantity}</span>
                                <button class="quantity-btn" onclick="increaseQuantity(${item.id})">+</button>
                            </div>
                            <div class="item-price">${item.price * item.quantity} ريال</div>
                            <button class="remove-btn" onclick="removeFromCart(${item.id})">🗑️</button>
                        </div>
                    </div>
                `).join('')}
                
                <div class="cart-summary">
                    <div class="promo-code">
                        <input type="text" placeholder="أدخل كود الخصم (SAVE20)" id="promoInput">
                        <button onclick="applyPromo()">تطبيق</button>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">المجموع الفرعي:</span>
                        <span class="summary-value">${subtotal} ريال</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">الشحن:</span>
                        <span class="summary-value">${shipping === 0 ? 'مجاني 🎉' : shipping + ' ريال'}</span>
                    </div>
                    ${discount > 0 ? `
                    <div class="summary-row">
                        <span class="summary-label">الخصم:</span>
                        <span class="summary-value" style="color: #2ecc71;">- ${discount} ريال</span>
                    </div>
                    ` : ''}
                    <div class="summary-row">
                        <span class="summary-label">المجموع الكلي:</span>
                        <span class="summary-value total-price">${total} ريال</span>
                    </div>
                    ${subtotal < 200 ? '<p style="text-align: center; margin-top: 15px; opacity: 0.9;">💡 أضف 
