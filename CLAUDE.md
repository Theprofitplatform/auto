# Website Page Creation Template

## Objective

To create new pages for the website using the provided HTML template.

## Instructions

1. Copy the HTML template below.
2. Create a new HTML file (e.g., `new-page.html`).
3. Paste the code and modify the content (titles, text, images, links).
4. Save the new file.

## HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Marketing Agency Sydney | Get 3x More Leads - The Profit Platform</title>
    <meta name="description" content="Sydney's results-driven digital marketing agency. Get more customers with proven SEO, Google Ads & web design. No lock-ins. Free strategy call.">
    
    <!-- Preconnect to external domains -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">     
    <style>
        /* ========================= 
           CSS RESET & VARIABLES 
           ========================= */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --pp-primary: #2c86f9;
            --pp-primary-dark: #1e6ee8;
            --pp-black: #0f172a;
            --pp-white: #ffffff;
            --pp-gray-50: #f8fafc;
            --pp-gray-100: #f1f5f9;
            --pp-gray-200: #e2e8f0;
            --pp-gray-300: #cbd5e1;
            --pp-gray-400: #94a3b8;
            --pp-gray-500: #64748b;
            --pp-gray-600: #475569;
            --pp-gray-700: #334155;
            --pp-gray-800: #1e293b;
            --pp-gray-900: #0f172a;
            --pp-success: #10b981;
            --pp-warning: #f59e0b;
            --pp-danger: #ef4444;
            --pp-radius: 16px;
            --pp-radius-sm: 8px;
            --pp-radius-lg: 24px;
            --pp-shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
            --pp-shadow: 0 4px 20px rgba(15, 23, 42, .08);
            --pp-shadow-lg: 0 20px 40px rgba(15, 23, 42, .12);
            --pp-shadow-xl: 0 25px 50px -12px rgba(0, 0, 0, .25);
            --pp-transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --pp-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --pp-gradient-light: linear-gradient(135deg, #a7c0f2 0%, #d6b3e8 100%);
            --pp-gradient-dark: linear-gradient(135deg, #1e6ee8 0%, #0f4bb2 100%);
            --pp-gradient-success: linear-gradient(135deg, #10b981 0%, #059669 100%);
            --pp-gradient-warning: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
            --pp-gradient-danger: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);    
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            color: var(--pp-gray-800);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            background: var(--pp-gray-50);
            font-size: 16px;
            scroll-behavior: smooth;
            position: relative;
        }

        /* ========================= 
           TYPOGRAPHY 
           ========================= */
        h1, h2, h3, h4, h5, h6 {
            font-weight: 700;
            line-height: 1.2;
            color: var(--pp-black);
        }

        h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 800;
            letter-spacing: -0.02em;
        }
        
        h2 {
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 700;
            letter-spacing: -0.01em;
        }
        
        h3 {
            font-size: clamp(1.5rem, 3vw, 2rem);
            font-weight: 600;
        }

        p {
            font-size: clamp(1rem, 1.5vw, 1.125rem);
            line-height: 1.7;
            color: var(--pp-gray-600);
        }

        /* ========================= 
           LAYOUT COMPONENTS 
           ========================= */
        .container {
            max-width: 1280px;
            margin: 0 auto !important;
            padding: 0 20px !important;
            box-sizing: border-box;
            width: 100%;
        }

        .section {
            padding: 80px 0;
            position: relative;
        }

        @media (max-width: 768px) {
            .section {
                padding: 60px 0;
            }
        }

        /* ========================= 
           SCROLL PROGRESS INDICATOR 
           ========================= */
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            z-index: 9999;
            background: rgba(44, 134, 249, 0.1);
        }

        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, var(--pp-primary), var(--pp-primary-dark));
            width: 0%;
            transition: width 0.1s ease;
        }

        /* ========================= 
           ENHANCED HEADER & NAVIGATION 
           ========================= */
        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.93);
            backdrop-filter: blur(20px) saturate(180%);
            -webkit-backdrop-filter: blur(20px) saturate(180%);
            z-index: 1000;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            border-bottom: 1px solid rgba(44, 134, 249, 0.1);
            box-shadow: 0 1px 20px rgba(0, 0, 0, 0.03);
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 100%;
            background: linear-gradient(90deg, 
                rgba(44, 134, 249, 0.02) 0%,
                rgba(44, 134, 249, 0.01) 50%,
                rgba(44, 134, 249, 0.02) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        header.scrolled {
            background: rgba(255, 255, 255, 0.96);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
            border-bottom-color: rgba(44, 134, 249, 0.2);
            transform: translateY(0);
        }

        header.scrolled::before {
            opacity: 1;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0 !important;
            width: 100%;
            gap: 30px !important;
            transition: padding 0.3s ease;
            margin: 0 !important;
            box-sizing: border-box;
        }

        header.scrolled nav {
            padding: 16px 0 !important;
        }

        .nav-links {
            display: flex;
            gap: 8px !important;
            list-style: none;
            margin: 0 !important;
            padding: 0 !important;
            align-items: center;
            flex: 1;
            justify-content: center;
            box-sizing: border-box;
        }

        .nav-links li {
            position: relative;
            margin: 0 !important;
            padding: 0 !important;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--pp-gray-700);
            font-weight: 600;
            font-size: 0.95rem;
            padding: 14px 20px !important;
            border-radius: var(--pp-radius-sm);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            display: inline-block;
            margin: 0 2px !important;
            box-sizing: border-box;
            white-space: nowrap;
        }

        .nav-links a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.08), rgba(44, 134, 249, 0.04));
            border-radius: var(--pp-radius-sm);
            opacity: 0;
            transform: scale(0.85);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: -1;
        }

        .nav-links a:hover::before {
            opacity: 1;
            transform: scale(1);
        }

        .nav-links a:hover {
            color: var(--pp-primary);
            transform: translateY(-1px);
        }

        .nav-links a.active {
            color: var(--pp-primary);
            font-weight: 700;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.08), rgba(44, 134, 249, 0.04));
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 8px;
            width: 4px;
            height: 4px;
            background: var(--pp-primary);
            border-radius: 50%;
            transform: translateX(-50%) scale(0);
            transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            transform: translateX(-50%) scale(1);
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            flex-shrink: 0;
            position: relative;
            padding: 10px 15px !important;
            border-radius: var(--pp-radius);
            overflow: hidden;
            margin: 0 !important;
            box-sizing: border-box;
        }

        .logo::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(44, 134, 249, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .logo:hover::before {
            left: 100%;
        }

        .logo-img {
            height: 64px;
            width: auto;
            max-width: 220px;
            object-fit: contain;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            filter: drop-shadow(0 3px 6px rgba(0, 0, 0, 0.06));
            position: relative;
            z-index: 1;
        }

        .logo:hover .logo-img {
            transform: scale(1.03) translateY(-1px);
            filter: drop-shadow(0 6px 12px rgba(44, 134, 249, 0.15));
        }

        header.scrolled .logo-img {
            height: 56px;
            transform: scale(0.98);
        }

        .nav-cta {
            display: flex;
            align-items: center;
            gap: 20px !important;
            flex-shrink: 0;
            margin: 0 !important;
            padding: 0 !important;
            box-sizing: border-box;
        }

        .phone-number {
            font-weight: 700;
            color: var(--pp-primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1rem;
            white-space: nowrap;
            padding: 12px 18px !important;
            border-radius: 25px;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.08), rgba(44, 134, 249, 0.04));
            border: 2px solid rgba(44, 134, 249, 0.2);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            margin: 0 !important;
            box-sizing: border-box;
        }

        .phone-number::before {
            content: "📞";
            font-size: 1.1rem;
            animation: phone-ring 2s ease-in-out infinite;
        }

        @keyframes phone-ring {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(-10deg); }
            20% { transform: rotate(10deg); }
        }

        .phone-number:hover {
            color: white;
            background: linear-gradient(135deg, var(--pp-primary), var(--pp-primary-dark));
            border-color: var(--pp-primary);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(44, 134, 249, 0.3);
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            padding: 10px;
            border-radius: var(--pp-radius-sm);
            transition: var(--pp-transition);
            z-index: 1001;
            position: relative;
            background: none;
            border: none;
        }

        .menu-toggle:hover {
            background: var(--pp-gray-50);
        }

        .menu-toggle span {
            width: 28px;
            height: 3px;
            background: var(--pp-black);
            transition: var(--pp-transition);
            border-radius: 2px;
            transform-origin: center;
        }

        .menu-toggle.active span:nth-child(1) {
            transform: rotate(45deg) translate(7px, 7px);
        }

        .menu-toggle.active span:nth-child(2) {
            opacity: 0;
        }

        .menu-toggle.active span:nth-child(3) {
            transform: rotate(-45deg) translate(7px, -7px);
        }

        /* Enhanced Mobile Navigation Overlay */
        .mobile-nav-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            background: linear-gradient(45deg, rgba(0, 0, 0, 0.7), rgba(44, 134, 249, 0.1));
            backdrop-filter: blur(10px);
            z-index: 998;
            opacity: 0;
            visibility: hidden;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .mobile-nav-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        /* Enhanced Mobile Navigation Menu */
        .mobile-nav {
            position: fixed;
            top: 0;
            right: -100%;
            width: 380px;
            max-width: 92vw;
            height: 100vh;
            background: linear-gradient(135deg, #fff 0%, #fafbfc 100%);
            z-index: 999;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: -10px 0 40px rgba(0, 0, 0, 0.2);
            overflow-y: auto;
            border-left: 3px solid var(--pp-primary);
        }

        .mobile-nav.active {
            right: 0;
        }

        .mobile-nav-header {
            padding: 25px 25px 20px !important;
            border-bottom: 1px solid var(--pp-gray-200);
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 0 !important;
            box-sizing: border-box;
        }

        .mobile-nav-close {
            background: none;
            border: none;
            font-size: 28px;
            cursor: pointer;
            color: var(--pp-gray-600);
            transition: color 0.3s ease;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }

        .mobile-nav-close:hover {
            color: var(--pp-primary);
            background: var(--pp-gray-50);
        }

        .mobile-nav-links {
            padding: 30px 0 !important;
            margin: 0 !important;
            box-sizing: border-box;
        }

        .mobile-nav-links a {
            display: block;
            padding: 20px 25px !important;
            color: var(--pp-black);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            border-bottom: 1px solid rgba(44, 134, 249, 0.08);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            transform: translateX(20px);
            opacity: 0;
            animation: slideInMobile 0.5s ease-out forwards;
            margin: 0 !important;
            box-sizing: border-box;
        }

        .mobile-nav-links a:nth-child(1) { animation-delay: 0.1s; }
        .mobile-nav-links a:nth-child(2) { animation-delay: 0.15s; }
        .mobile-nav-links a:nth-child(3) { animation-delay: 0.2s; }
        .mobile-nav-links a:nth-child(4) { animation-delay: 0.25s; }
        .mobile-nav-links a:nth-child(5) { animation-delay: 0.3s; }
        .mobile-nav-links a:nth-child(6) { animation-delay: 0.35s; }
        .mobile-nav-links a:nth-child(7) { animation-delay: 0.4s; }

        @keyframes slideInMobile {
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .mobile-nav-links a::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 4px;
            background: var(--pp-primary);
            transform: scaleY(0);
            transition: transform 0.3s ease;
        }

        .mobile-nav-links a:hover::before {
            transform: scaleY(1);
        }

        .mobile-nav-links a:hover {
            color: var(--pp-primary);
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.1), rgba(44, 134, 249, 0.05));
            padding-left: 35px;
            transform: translateX(5px);
        }

        .mobile-nav-links a:last-child {
            border-bottom: none;
        }

        .mobile-nav-cta {
            padding: 25px !important;
            border-top: 2px solid var(--pp-gray-200);
            background: var(--pp-gray-50);
            margin: 0 !important;
            box-sizing: border-box;
        }

        .mobile-nav-cta .phone-number {
            display: block;
            margin-bottom: 20px;
            padding: 15px 0;
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--pp-primary);
            text-align: center;
            background: white;
            border-radius: var(--pp-radius);
            box-shadow: var(--pp-shadow-sm);
        }

        .mobile-nav-cta .phone-number::before {
            content: "📞 ";
        }

        .mobile-nav-cta .btn {
            width: 100%;
            text-align: center;
            justify-content: center;
            font-size: 1.1rem;
            padding: 16px 24px;
        }

        /* ========================= 
           ENHANCED BUTTONS 
           ========================= */
        .btn {
            display: inline-block;
            padding: 14px 32px;
            border-radius: var(--pp-radius-sm);
            font-weight: 600;
            text-decoration: none;
            transition: var(--pp-transition);
            cursor: pointer;
            border: none;
            font-size: 1rem;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--pp-primary), var(--pp-primary-dark));
            color: white;
            box-shadow: 0 4px 14px rgba(44, 134, 249, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(44, 134, 249, 0.4);
        }

        .btn-outline {
            background: transparent;
            color: var(--pp-primary);
            border: 2px solid var(--pp-primary);
        }

        .btn-outline:hover {
            background: var(--pp-primary);
            color: white;
            transform: translateY(-2px);
        }

        /* Button ripple effect */
        .btn::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .btn:hover::after {
            width: 300px;
            height: 300px;
        }

        /* ========================= 
           FLOATING CTA 



    

        

       

        @keyframes pulse-glow {
            0%, 100% { box-shadow: 0 8px 25px rgba(44, 134, 249, 0.4); }
            50% { box-shadow: 0 8px 35px rgba(44, 134, 249, 0.6); }
        }

        /* ========================= 
           HERO SECTION 
           ========================= */
        .hero {
            padding: 160px 0 100px;
            background: linear-gradient(135deg, #f8fafc 0%, #fff 50%, #f0f9ff 100%);
            position: relative;
            overflow: hidden;
            min-height: 90vh;
            display: flex;
            align-items: center;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(44, 134, 249, 0.05) 0%, transparent 70%);
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(-30px, -30px) rotate(180deg); }
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 80px;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .hero-text h1 {
            margin-bottom: 20px;
            animation: fadeInUp 0.8s ease-out;
        }

        .hero-text .subtitle {
            font-size: 1.35rem;
            color: var(--pp-gray-600);
            margin-bottom: 40px;
            line-height: 1.6;
            animation: fadeInUp 0.8s ease-out 0.4s both;
        }

        .hero-bullets {
            list-style: none;
            margin: 30px 0;
            animation: fadeInUp 0.8s ease-out 0.4s both;
        }

        .hero-bullets li {
            padding: 10px 0;
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 500;
            color: var(--pp-gray-700);
            transition: color 0.3s ease, transform 0.3s ease;
        }

        .hero-bullets li::before {
            content: "✔";
            font-size: 1.2rem;
            color: var(--pp-primary);
            flex-shrink: 0;
            transition: color 0.3s ease;
        }

        .hero-bullets li:hover {
            color: var(--pp-primary);
            transform: translateX(5px);
            transition: var(--pp-transition);
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            margin-bottom: 25px;
            flex-wrap: wrap;
        }

        .hero-image {
            position: relative;
            animation: fadeInRight 1s ease-out;
        }

        .hero-image img {
            width: 100%;
            height: auto;
            border-radius: var(--pp-radius-lg);
            box-shadow: var(--pp-shadow-xl);
        }

        .hero-stats {
            position: absolute;
            bottom: 30px;
            left: 30px;
            background: white;
            padding: 20px;
            border-radius: var(--pp-radius);
            box-shadow: var(--pp-shadow-lg);
            animation: slideInLeft 1s ease-out 0.5s both;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin: 10px 0;
        }

        .stat-number {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--pp-primary);
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--pp-gray-600);
        }

        /* ========================= 
           ENHANCED HERO ELEMENTS 
           ========================= */

        /* Floating background elements */
        .hero-background-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .floating-shape {
            position: absolute;
            border-radius: 50%;
            filter: blur(1px);
            animation: float-shapes 20s ease-in-out infinite;
        }

        .shape-1 {
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(116, 75, 162, 0.1));
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .shape-2 {
            width: 150px;
            height: 150px;
            background: linear-gradient(135deg, rgba(244, 114, 182, 0.08), rgba(168, 85, 247, 0.08));
            top: 60%;
            right: 15%;
            animation-delay: -5s;
        }

        .shape-3 {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.05), rgba(147, 51, 234, 0.05));
            top: 10%;
            right: 30%;
            animation-delay: -10s;
        }

        @keyframes float-shapes {
            0%, 100% { transform: translate(0, 0) rotate(0deg) scale(1); }
            25% { transform: translate(30px, -30px) rotate(90deg) scale(1.1); }
            50% { transform: translate(-20px, -50px) rotate(180deg) scale(0.9); }
            75% { transform: translate(-40px, 20px) rotate(270deg) scale(1.05); }
        }

        /* Hero Badge */
        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1), rgba(37, 99, 235, 0.1));
            border: 1px solid rgba(59, 130, 246, 0.2);
            padding: 12px 24px;
            border-radius: 50px;
            margin-bottom: 30px;
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--pp-primary);
            animation: fadeInUp 0.8s ease-out;
        }

        .hero-badge i {
            color: #f59e0b;
        }

        /* Enhanced Hero Title */
        .hero-title {
            font-size: clamp(2.5rem, 5.5vw, 4.2rem);
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 30px;
            position: relative;
            animation: fadeInUp 0.8s ease-out 0.2s both;
        }

        .highlight-text {
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
        }

        .location-text {
            color: #059669;
            position: relative;
        }

        .title-underline {
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60%;
            height: 4px;
            background: linear-gradient(90deg, var(--pp-primary), transparent);
            border-radius: 2px;
            animation: expandLine 1.5s ease-out 1s both;
        }

        @keyframes expandLine {
            from { width: 0; }
            to { width: 60%; }
        }

        /* Value Proposition Items */
        .value-proposition {
            margin: 40px 0;
            animation: fadeInUp 0.8s ease-out 0.6s both;
        }

        .value-item {
            display: flex;
            align-items: center;
            gap: 16px;
            margin: 20px 0;
            padding: 16px 20px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: var(--pp-radius);
            border-left: 4px solid var(--pp-primary);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .value-item:hover {
            background: rgba(59, 130, 246, 0.05);
            transform: translateX(10px);
            box-shadow: 0 8px 25px rgba(59, 130, 246, 0.1);
        }

        .value-item i {
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--pp-primary);
            font-size: 1.2rem;
        }

        .value-item span {
            font-weight: 500;
            color: var(--pp-gray-700);
            font-size: 1.05rem;
        }

        /* Enhanced Hero CTA Section */
        .hero-cta-section {
            margin-top: 50px;
            animation: fadeInUp 0.8s ease-out 0.8s both;
        }

        .hero-primary-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 20px 32px;
            border-radius: var(--pp-radius);
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            gap: 4px;
            position: relative;
            overflow: hidden;
            min-width: 280px;
            transition: all 0.4s ease;
        }

        .hero-primary-btn:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
        }

        .btn-text {
            font-size: 1.1rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .btn-subtext {
            font-size: 0.85rem;
            opacity: 0.9;
            font-weight: 500;
        }

        .btn-arrow {
            position: absolute;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            transition: transform 0.3s ease;
        }

        .hero-primary-btn:hover .btn-arrow {
            transform: translateY(-50%) translateX(5px);
        }

        .hero-call-btn {
            background: transparent;
            color: var(--pp-primary);
            border: 2px solid var(--pp-primary);
            padding: 20px 32px;
            border-radius: var(--pp-radius);
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 700;
            transition: all 0.3s ease;
        }

        .hero-call-btn:hover {
            background: var(--pp-primary);
            color: white;
            transform: translateY(-2px);
        }

        .hero-guarantee {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--pp-gray-500);
            font-size: 0.9rem;
            justify-content: center;
            margin-top: 25px;
        }

        .hero-guarantee i {
            color: #10b981;
        }

        /* Enhanced Hero Visual */
        .hero-visual {
            position: relative;
            animation: fadeInRight 1s ease-out 0.5s both;
        }

        .hero-image-container {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hero-main-image {
            width: 100%;
            max-width: 500px;
            height: auto;
            border-radius: var(--pp-radius-lg);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
            position: relative;
            z-index: 1;
        }

        /* Floating Stats Cards */
        .floating-stats {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .stat-card {
            position: absolute;
            background: white;
            padding: 20px;
            border-radius: var(--pp-radius);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            gap: 15px;
            min-width: 180px;
            animation: float-cards 6s ease-in-out infinite;
            border: 1px solid rgba(255, 255, 255, 0.8);
        }

        .stat-1 {
            top: 20%;
            left: -60px;
            animation-delay: 0s;
        }

        .stat-2 {
            bottom: 30%;
            right: -80px;
            animation-delay: 2s;
        }

        .stat-3 {
            top: 10%;
            right: -40px;
            animation-delay: 4s;
        }

        @keyframes float-cards {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .stat-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }

        .stat-1 .stat-icon { background: linear-gradient(135deg, #667eea, #764ba2); }
        .stat-2 .stat-icon { background: linear-gradient(135deg, #f093fb, #f5576c); }
        .stat-3 .stat-icon { background: linear-gradient(135deg, #4facfe, #00f2fe); }

        .stat-content {
            display: flex;
            flex-direction: column;
        }

        .floating-stats .stat-number {
            font-size: 2rem;
            font-weight: 800;
            color: var(--pp-black);
            line-height: 1;
        }

        .floating-stats .stat-label {
            font-size: 0.9rem;
            color: var(--pp-gray-500);
            font-weight: 500;
        }

        /* Success Notification */
        .success-notification {
            position: absolute;
            bottom: -20px;
            left: 20px;
            background: white;
            padding: 16px 20px;
            border-radius: var(--pp-radius);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border-left: 4px solid #10b981;
            animation: slideInBottom 1s ease-out 2s both, pulse-notification 3s ease-in-out 3s infinite;
        }

        @keyframes slideInBottom {
            from { transform: translateY(100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        @keyframes pulse-notification {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .notification-content {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .notification-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .notification-text {
            display: flex;
            flex-direction: column;
        }

        .notification-text strong {
            color: var(--pp-black);
            font-size: 0.95rem;
        }

        .notification-time {
            color: var(--pp-gray-500);
            font-size: 0.8rem;
        }

        /* ========================= 
           TRUST BAR WITH BADGES
           ========================= */
        .trust-bar {
            padding: 40px 0;
            background: white;
            border-top: 1px solid var(--pp-gray-200);
            border-bottom: 1px solid var(--pp-gray-200);
        }

        .trust-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .trust-item {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 20px;
            background: var(--pp-gray-50);
            border-radius: var(--pp-radius-sm);
            transition: var(--pp-transition);
        }

        .trust-item:hover {
            transform: translateY(-2px);
            background: var(--pp-gray-100);
        }

        .trust-item strong {
            color: var(--pp-black);
            font-size: 1.2rem;
        }

        .trust-badges {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        .badge {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 16px;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.1), rgba(44, 134, 249, 0.2));
            border-radius: var(--pp-radius-sm);
            color: var(--pp-primary);
            font-weight: 600;
            font-size: 0.9rem;
            border: 1px solid rgba(44, 134, 249, 0.2);
        }

        /* ========================= 
           ENHANCED RESULTS SECTION 
           ========================= */
        .results {
            padding: 100px 0;
            background: linear-gradient(135deg, #fafbfc 0%, white 50%, #f0f9ff 100%);
            position: relative;
            overflow: hidden;
        }

        .section-header {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 60px;
        }

        .section-header h2 {
            margin-bottom: 20px;
        }

        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        @media (min-width: 769px) {
            .results-grid {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        @media (min-width: 1200px) {
            .results-grid {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        .result-card {
            background: white;
            border-radius: var(--pp-radius);
            padding: 40px 30px;
            text-align: center;
            box-shadow: var(--pp-shadow);
            transition: var(--pp-transition);
            position: relative;
            overflow: hidden;
            border: 2px solid transparent;
            cursor: pointer;
        }

        .result-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--pp-primary), var(--pp-primary-dark));
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .result-card:hover {
            transform: translateY(-8px) rotateX(5deg);
            box-shadow: var(--pp-shadow-xl);
            border-color: var(--pp-primary);
        }

        .result-card:hover::before {
            transform: scaleX(1);
        }

        .result-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.1), rgba(44, 134, 249, 0.2));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: var(--pp-primary);
            transition: transform 0.3s ease;
        }

        .result-card:hover .result-icon {
            transform: scale(1.2) rotate(10deg);
        }

        .result-number {
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--pp-primary), var(--pp-primary-dark));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            font-family: 'Inter', sans-serif;
        }

        .result-label {
            font-size: 1.25rem;
            color: var(--pp-black);
            font-weight: 600;
            margin-bottom: 10px;
        }

        .result-description {
            font-size: 1rem;
            color: var(--pp-gray-500);
            margin-bottom: 20px;
        }

        .result-timeline {
            display: inline-block;
            background: var(--pp-primary);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        /* ========================= 
           ENHANCED RESULTS ELEMENTS 
           ========================= */

        .results-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .results-pattern {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="results-grid" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="1" fill="rgba(44,134,249,0.05)"/></pattern></defs><rect width="100%" height="100%" fill="url(%23results-grid)"/></svg>');
            opacity: 0.6;
        }

        .section-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.1), rgba(5, 150, 105, 0.1));
            border: 1px solid rgba(16, 185, 129, 0.2);
            padding: 10px 20px;
            border-radius: 50px;
            margin-bottom: 25px;
            font-size: 0.9rem;
            font-weight: 600;
            color: #059669;
        }

        .section-badge i {
            color: #10b981;
        }

        /* Enhanced Result Cards */
        .result-card {
            background: linear-gradient(135deg, white 0%, #fafbfc 100%) !important;
            border-radius: var(--pp-radius-lg) !important;
            padding: 0 !important;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08) !important;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important;
            border: 1px solid rgba(255, 255, 255, 0.8) !important;
            display: flex !important;
            flex-direction: column !important;
        }

        .result-card::before {
            height: 4px !important;
            transform: scaleX(0) !important;
            transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important;
        }

        .case-study-1::before { background: linear-gradient(90deg, #667eea, #764ba2) !important; }
        .case-study-2::before { background: linear-gradient(90deg, #f093fb, #f5576c) !important; }
        .case-study-3::before { background: linear-gradient(90deg, #4facfe, #00f2fe) !important; }
        .case-study-4::before { background: linear-gradient(90deg, #43e97b, #38f9d7) !important; }

        .result-card:hover {
            transform: translateY(-15px) scale(1.02) !important;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15) !important;
        }

        /* Result Card Header */
        .result-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            padding: 30px 30px 0;
            position: relative;
        }

        .result-icon {
            width: 70px !important;
            height: 70px !important;
            margin: 0 !important;
            border-radius: 50% !important;
            color: white !important;
            font-size: 2rem !important;
            transition: all 0.4s ease !important;
        }

        .case-study-1 .result-icon { background: linear-gradient(135deg, #667eea, #764ba2) !important; }
        .case-study-2 .result-icon { background: linear-gradient(135deg, #f093fb, #f5576c) !important; }
        .case-study-3 .result-icon { background: linear-gradient(135deg, #4facfe, #00f2fe) !important; }
        .case-study-4 .result-icon { background: linear-gradient(135deg, #43e97b, #38f9d7) !important; }

        .icon-glow {
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border-radius: 50%;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .case-study-1 .icon-glow { background: linear-gradient(135deg, #667eea, #764ba2); }
        .case-study-2 .icon-glow { background: linear-gradient(135deg, #f093fb, #f5576c); }
        .case-study-3 .icon-glow { background: linear-gradient(135deg, #4facfe, #00f2fe); }
        .case-study-4 .icon-glow { background: linear-gradient(135deg, #43e97b, #38f9d7); }

        .result-card:hover .result-icon {
            transform: scale(1.1) rotateY(10deg) !important;
        }

        .result-card:hover .icon-glow {
            opacity: 0.3;
            animation: pulse-glow 2s ease-in-out infinite;
        }

        @keyframes pulse-glow {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Result Badges */
        .result-badge {
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            color: white;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .result-badge.success { background: linear-gradient(135deg, #10b981, #059669); }
        .result-badge.growth { background: linear-gradient(135deg, #f59e0b, #d97706); }
        .result-badge.savings { background: linear-gradient(135deg, #3b82f6, #1d4ed8); }
        .result-badge.ranking { background: linear-gradient(135deg, #8b5cf6, #7c3aed); }

        /* Result Metrics */
        .result-metrics {
            padding: 20px 30px;
            text-align: center;
        }

        .before-after {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin-bottom: 25px;
            padding: 15px;
            background: rgba(249, 250, 251, 0.8);
            border-radius: var(--pp-radius);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .before, .after {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }

        .before .label, .after .label {
            font-size: 0.8rem;
            color: var(--pp-gray-500);
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .before .value {
            font-size: 1.1rem;
            font-weight: 700;
            color: #ef4444;
        }

        .after .value {
            font-size: 1.1rem;
            font-weight: 700;
            color: #10b981;
        }

        .arrow {
            color: var(--pp-primary);
            font-size: 1.2rem;
        }

        .result-number {
            font-size: 3.5rem !important;
            font-weight: 900 !important;
            margin-bottom: 10px !important;
            line-height: 1 !important;
        }

        .case-study-1 .result-number {
            background: linear-gradient(135deg, #667eea, #764ba2) !important;
            -webkit-background-clip: text !important;
            -webkit-text-fill-color: transparent !important;
        }
        .case-study-2 .result-number {
            background: linear-gradient(135deg, #f093fb, #f5576c) !important;
            -webkit-background-clip: text !important;
            -webkit-text-fill-color: transparent !important;
        }
        .case-study-3 .result-number {
            background: linear-gradient(135deg, #4facfe, #00f2fe) !important;
            -webkit-background-clip: text !important;
            -webkit-text-fill-color: transparent !important;
        }
        .case-study-4 .result-number {
            background: linear-gradient(135deg, #43e97b, #38f9d7) !important;
            -webkit-background-clip: text !important;
            -webkit-text-fill-color: transparent !important;
        }

        .result-label {
            font-size: 1.3rem !important;
            font-weight: 700 !important;
            margin-bottom: 15px !important;
        }

        /* Result Details */
        .result-details {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 30px;
            border-top: 1px solid rgba(0, 0, 0, 0.05);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        .client-info {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .client-avatar {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .case-study-1 .client-avatar { background: linear-gradient(135deg, #667eea, #764ba2); }
        .case-study-2 .client-avatar { background: linear-gradient(135deg, #f093fb, #f5576c); }
        .case-study-3 .client-avatar { background: linear-gradient(135deg, #4facfe, #00f2fe); }
        .case-study-4 .client-avatar { background: linear-gradient(135deg, #43e97b, #38f9d7); }

        .client-details {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .client-details strong {
            color: var(--pp-black);
            font-size: 1rem;
            font-weight: 600;
        }

        .client-details span {
            color: var(--pp-gray-500);
            font-size: 0.85rem;
        }

        .result-timeline {
            display: flex !important;
            align-items: center !important;
            gap: 6px !important;
            color: var(--pp-gray-500) !important;
            font-size: 0.9rem !important;
            font-weight: 500 !important;
            background: none !important;
            padding: 0 !important;
            border-radius: 0 !important;
        }

        .result-timeline i {
            color: var(--pp-primary);
        }

        /* Result Testimonial */
        .result-testimonial {
            padding: 20px 30px;
            background: rgba(249, 250, 251, 0.5);
            flex-grow: 1;
            display: flex;
            align-items: center;
        }

        .result-testimonial p {
            font-style: italic;
            color: var(--pp-gray-600);
            font-size: 0.95rem;
            line-height: 1.5;
            margin: 0;
            position: relative;
        }

        .result-testimonial p::before {
            content: '"';
            font-size: 2rem;
            color: var(--pp-primary);
            opacity: 0.3;
            position: absolute;
            left: -15px;
            top: -5px;
            font-family: Georgia, serif;
        }

        /* Results CTA */
        .results-cta {
            text-align: center;
            margin-top: 60px;
            padding: 50px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.05), rgba(116, 75, 162, 0.05));
            border-radius: var(--pp-radius-lg);
            border: 1px solid rgba(102, 126, 234, 0.1);
        }

        .results-cta h3 {
            font-size: 2rem;
            margin-bottom: 15px;
            color: var(--pp-black);
        }

        .results-cta p {
            font-size: 1.2rem;
            color: var(--pp-gray-600);
            margin-bottom: 30px;
        }

        .results-btn {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            padding: 18px 32px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            border-radius: var(--pp-radius);
            font-size: 1.1rem;
            font-weight: 700;
            transition: all 0.3s ease;
        }

        .results-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.4);
        }

        .results-btn i {
            transition: transform 0.3s ease;
        }

        .results-btn:hover i {
            transform: translateX(5px);
        }

        /* ========================= 
           INTERACTIVE PROCESS TIMELINE 
           ========================= */
        .process {
            padding: 100px 0;
            background: linear-gradient(135deg, #fafbfc 0%, white 30%, #f0f9ff 70%, #fafbfc 100%);
            position: relative;
            overflow: visible;
        }

        .process-timeline {
            position: relative;
            max-width: 1200px;
            margin: 60px auto 0;
            padding: 0 20px;
        }

        .timeline-line {
            position: absolute;
            top: 50%;
            left: 8%;
            right: 8%;
            height: 4px;
            background: var(--pp-gray-200);
            border-radius: 2px;
            transform: translateY(-50%);
        }

        .timeline-progress {
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
            background: linear-gradient(90deg, var(--pp-primary), var(--pp-primary-dark));
            border-radius: 2px;
            width: 0%;
            transition: width 1s ease;
        }


        .process-step {
            text-align: center;
            position: relative;
            padding: 0;
            transition: var(--pp-transition);
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .process-step.active {
            transform: translateY(-10px);
        }

        .step-circle {
            width: 100px;
            height: 100px;
            margin: 0 auto 20px;
            border-radius: 50%;
            background: white;
            border: 4px solid var(--pp-gray-200);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--pp-gray-400);
            transition: var(--pp-transition);
            position: relative;
            box-shadow: var(--pp-shadow);
        }

        .process-step.active .step-circle,
        .process-step.completed .step-circle {
            border-color: var(--pp-primary);
            background: var(--pp-primary);
            color: white;
            transform: scale(1.1);
        }

        .pulse-ring {
            position: absolute;
            top: -8px;
            left: -8px;
            right: -8px;
            bottom: -8px;
            border: 2px solid var(--pp-primary);
            border-radius: 50%;
            opacity: 0;
            animation: pulse-ring 2s ease-out infinite;
        }

        .process-step.active .pulse-ring {
            opacity: 1;
        }

        @keyframes pulse-ring {
            0% { transform: scale(0.8); opacity: 1; }
            100% { transform: scale(1.2); opacity: 0; }
        }

        .step-content {
            background: white;
            padding: 25px 20px;
            border-radius: var(--pp-radius);
            box-shadow: var(--pp-shadow);
            margin-top: 20px;
            border: 2px solid transparent;
            transition: var(--pp-transition);
            width: 100%;
            min-height: 300px;
            display: flex;
            flex-direction: column;
        }

        .process-step.active .step-content {
            border-color: var(--pp-primary);
            box-shadow: var(--pp-shadow-xl);
        }

        .step-title {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--pp-black);
        }

        .step-description {
            color: var(--pp-gray-600);
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .step-deliverables {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            justify-content: center;
        }

        .tag {
            background: var(--pp-gray-100);
            color: var(--pp-gray-700);
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 4px;
        }

        .process-step.active .tag {
            background: rgba(44, 134, 249, 0.1);
            color: var(--pp-primary);
        }

        .step-week {
            position: absolute;
            top: -45px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--pp-primary);
            color: white;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            white-space: nowrap;
        }

        /* Optimize step content for desktop */
        .step-header {
            margin-bottom: 15px;
        }

        .step-timeline-info {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }

        .step-duration {
            font-size: 0.8rem;
            color: var(--pp-gray-500);
            background: var(--pp-gray-100);
            padding: 2px 8px;
            border-radius: 10px;
        }

        .step-title {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: var(--pp-black);
        }

        .step-description {
            font-size: 0.9rem;
            color: var(--pp-gray-600);
            line-height: 1.5;
            margin-bottom: 15px;
        }

        /* Hide complex content on desktop, show only on hover or active */
        .step-process,
        .step-outcome,
        .client-example {
            display: none;
        }

        .process-step.active .step-process,
        .process-step:hover .step-process {
            display: block;
            margin-top: 15px;
        }

        .process-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 8px 0;
            font-size: 0.85rem;
            color: var(--pp-gray-700);
        }

        .process-item i {
            color: var(--pp-primary);
            font-size: 0.8rem;
            width: 16px;
        }

        .step-badge {
            display: inline-block;
            background: var(--pp-primary);
            color: white;
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .step-badge.discovery { background: var(--pp-success); }
        .step-badge.building { background: var(--pp-warning); }
        .step-badge.launch { background: var(--pp-primary); }
        .step-badge.optimize { background: #8b5cf6; }

        /* Desktop optimizations */
        @media (min-width: 1024px) {
            .process-steps {
                max-width: 1600px;
                gap: 50px;
            }

            .process-step {
                padding: 0 15px;
            }
            
            .step-content {
                padding: 30px 25px;
            }

            .step-content {
                padding: 30px 25px !important;
                min-height: 280px !important;
                margin-top: 20px !important;
                text-align: center !important;
            }

            .step-circle {
                width: 100px !important;
                height: 100px !important;
                margin: 0 auto 20px !important;
            }
            .step-icon {
                font-size: 1.8rem !important;
            }

            .step-number {
                width: 30px !important;
                height: 30px !important;
                font-size: 0.9rem !important;
                bottom: -3px !important;
                right: -3px !important;
            }

            .step-week {
                position: absolute !important;
                top: -35px !important;
                left: 50% !important;
                transform: translateX(-50%) !important;
                padding: 5px 12px !important;
                font-size: 0.8rem !important;
                margin-bottom: 0 !important;
            }

            .timeline-line {
                left: 6%;
                right: 6%;
                display: block;
            }
        }

        @media (min-width: 769px) and (max-width: 1023px) {
            .process-steps {
                grid-template-columns: repeat(2, 1fr);
                gap: 30px;
                max-width: 900px;
            }

            .timeline-line {
                display: none;
            }

            .process-step {
                margin-bottom: 40px;
            }

            /* Show some content on tablet */
            .step-process {
                display: block !important;
            }
        }

        /* ========================= 
           ENHANCED PROCESS ELEMENTS 
           ========================= */

        .process-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .process-pattern {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 60"><defs><pattern id="process-dots" width="30" height="30" patternUnits="userSpaceOnUse"><circle cx="15" cy="15" r="2" fill="rgba(102,126,234,0.04)"/></pattern></defs><rect width="100%" height="100%" fill="url(%23process-dots)"/></svg>');
            opacity: 0.7;
        }

        .floating-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .floating-element {
            position: absolute;
            border-radius: 50%;
            filter: blur(1px);
            animation: float-process 25s ease-in-out infinite;
        }

        .element-1 {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.08), rgba(116, 75, 162, 0.08));
            top: 15%;
            left: 5%;
            animation-delay: 0s;
        }

        .element-2 {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, rgba(244, 114, 182, 0.06), rgba(168, 85, 247, 0.06));
            top: 60%;
            right: 10%;
            animation-delay: -8s;
        }

        .element-3 {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.05), rgba(147, 51, 234, 0.05));
            top: 30%;
            right: 25%;
            animation-delay: -15s;
        }

        @keyframes float-process {
            0%, 100% { transform: translate(0, 0) rotate(0deg) scale(1); }
            25% { transform: translate(20px, -20px) rotate(90deg) scale(1.1); }
            50% { transform: translate(-15px, -30px) rotate(180deg) scale(0.9); }
            75% { transform: translate(-25px, 15px) rotate(270deg) scale(1.05); }
        }

        /* Process Overview Stats */
        .process-overview {
            margin: 60px 0;
            text-align: center;
        }

        .process-stats {
            display: flex;
            justify-content: center;
            gap: 60px;
            flex-wrap: wrap;
        }

        .process-stats .stat-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
        }

        .process-stats .stat-number {
            font-size: 3rem;
            font-weight: 900;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1;
        }

        .process-stats .stat-label {
            color: var(--pp-gray-600);
            font-weight: 500;
            font-size: 1rem;
        }

        /* Enhanced Process Steps - Desktop Grid Layout */
        .process-steps {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            position: relative;
            z-index: 2;
            max-width: 1400px;
            margin: 0 auto;
            align-items: start;
        }

        .process-step {
            text-align: center;
            position: relative;
            padding: 0 !important;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important;
            cursor: pointer !important;
        }

        .process-step.active {
            transform: translateY(-10px) !important;
        }

        /* Step Headers */
        .step-header {
            margin-bottom: 30px;
        }

        .step-timeline-info {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }

        .step-week {
            position: static !important;
            transform: none !important;
            background: var(--pp-primary) !important;
            color: white !important;
            padding: 8px 20px !important;
            border-radius: 25px !important;
            font-size: 0.9rem !important;
            font-weight: 700 !important;
            margin-bottom: 5px !important;
        }

        .step-duration {
            font-size: 0.8rem;
            color: var(--pp-gray-500);
            font-weight: 500;
        }

        /* Enhanced Step Circles */
        .step-circle {
            width: 120px !important;
            height: 120px !important;
            margin: 0 auto 30px !important;
            border-radius: 50% !important;
            background: white !important;
            border: 4px solid var(--pp-gray-200) !important;
            display: flex !important;
            align-items: center !important;
            justify-content: center !important;
            position: relative !important;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1) !important;
        }

        .step-icon {
            font-size: 2.5rem;
            color: var(--pp-gray-400);
            transition: all 0.3s ease;
            position: relative;
            z-index: 3;
        }

        .step-number {
            position: absolute !important;
            bottom: -5px !important;
            right: -5px !important;
            width: 35px !important;
            height: 35px !important;
            background: var(--pp-primary) !important;
            color: white !important;
            border-radius: 50% !important;
            display: flex !important;
            align-items: center !important;
            justify-content: center !important;
            font-size: 1rem !important;
            font-weight: 700 !important;
            border: 3px solid white !important;
            z-index: 4 !important;
        }

        .process-step.active .step-circle,
        .process-step.completed .step-circle {
            border-color: var(--pp-primary) !important;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(116, 75, 162, 0.1)) !important;
            transform: scale(1.1) !important;
        }

        .process-step.active .step-icon,
        .process-step.completed .step-icon {
            color: var(--pp-primary) !important;
            transform: scale(1.1) !important;
        }

        /* Step Content */
        .step-content {
            background: white !important;
            padding: 40px 30px !important;
            border-radius: var(--pp-radius-lg) !important;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08) !important;
            border: 2px solid transparent !important;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1) !important;
            text-align: left !important;
            margin-top: 0 !important;
        }

        .process-step.active .step-content {
            border-color: var(--pp-primary) !important;
            box-shadow: 0 25px 50px rgba(102, 126, 234, 0.15) !important;
            transform: translateY(-5px) !important;
        }

        .step-badge {
            display: inline-block;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 15px;
            color: white;
        }

        .step-badge.discovery { background: linear-gradient(135deg, #3b82f6, #1d4ed8); }
        .step-badge.building { background: linear-gradient(135deg, #f59e0b, #d97706); }
        .step-badge.launching { background: linear-gradient(135deg, #10b981, #059669); }
        .step-badge.scaling { background: linear-gradient(135deg, #8b5cf6, #7c3aed); }

        .step-title {
            font-size: 1.5rem !important;
            font-weight: 700 !important;
            margin-bottom: 15px !important;
            color: var(--pp-black) !important;
        }

        .step-description {
            color: var(--pp-gray-600) !important;
            margin-bottom: 25px !important;
            line-height: 1.6 !important;
            font-size: 1rem !important;
        }

        /* Step Process Items */
        .step-process {
            margin: 25px 0;
            padding: 20px;
            background: rgba(249, 250, 251, 0.8);
            border-radius: var(--pp-radius);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .process-item {
            display: flex;
            align-items: center;
            gap: 12px;
            margin: 12px 0;
            color: var(--pp-gray-700);
            font-size: 0.95rem;
        }

        .process-item i {
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--pp-primary);
            flex-shrink: 0;
        }

        /* Step Outcomes */
        .step-outcome {
            margin: 25px 0;
            padding: 20px;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.05), rgba(5, 150, 105, 0.05));
            border-radius: var(--pp-radius);
            border: 1px solid rgba(16, 185, 129, 0.1);
        }

        .outcome-header {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
            color: #059669;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .outcome-header i {
            color: #10b981;
        }

        .deliverables {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .deliverable-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--pp-gray-700);
            font-size: 0.9rem;
        }

        .deliverable-item i {
            width: 16px;
            height: 16px;
            color: #10b981;
            flex-shrink: 0;
        }

        /* Client Examples */
        .client-example {
            margin-top: 20px;
            padding: 15px;
            background: rgba(102, 126, 234, 0.05);
            border-radius: var(--pp-radius);
            border-left: 4px solid var(--pp-primary);
        }

        .example-text {
            font-style: italic;
            color: var(--pp-gray-600);
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .example-text strong {
            color: var(--pp-primary);
            font-weight: 600;
        }

        /* Process Guarantee */
        .process-guarantee {
            margin-top: 80px;
            padding: 50px;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.05), rgba(5, 150, 105, 0.05));
            border-radius: var(--pp-radius-lg);
            border: 1px solid rgba(16, 185, 129, 0.2);
        }

        .guarantee-content {
            display: flex;
            align-items: center;
            gap: 30px;
            text-align: left;
        }

        .guarantee-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #10b981, #059669);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            flex-shrink: 0;
        }

        .guarantee-text {
            flex: 1;
        }

        .guarantee-text h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--pp-black);
        }

        .guarantee-text p {
            color: var(--pp-gray-600);
            font-size: 1rem;
            line-height: 1.6;
            margin: 0;
        }

        .guarantee-cta .btn {
            padding: 15px 30px;
            font-size: 1.1rem;
            font-weight: 600;
        }

        /* Responsive Process */
        @media (max-width: 768px) {
            .process {
                padding: 80px 0;
            }

            .process-stats {
                gap: 30px;
            }

            .process-stats .stat-number {
                font-size: 2.5rem;
            }

            .process-steps {
                flex-direction: column !important;
                gap: 40px !important;
            }

            .timeline-line {
                display: none !important;
            }

            .step-header {
                margin-bottom: 20px;
            }

            .step-circle {
                width: 100px !important;
                height: 100px !important;
            }

            .step-icon {
                font-size: 2rem;
            }

            .step-content {
                padding: 30px 25px !important;
            }

            .guarantee-content {
                flex-direction: column;
                text-align: center;
                gap: 20px;
            }

            .guarantee-icon {
                width: 60px;
                height: 60px;
                font-size: 1.5rem;
            }
        }

        /* ========================= 
           SERVICES SECTION 
           ========================= */
        .services {
            background: var(--pp-gray-50);
            padding: 80px 0;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .service-card {
            background: linear-gradient(135deg, #fff 0%, #fafbfc 100%);
            border-radius: var(--pp-radius);
            padding: 40px 30px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.08);
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            height: 100%;
            transform: translateY(0);
        }

        .service-card::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.8), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .service-card:hover::after {
            opacity: 1;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            transform: scaleX(0);
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: 1;
        }

        .service-card:nth-child(1)::before {
            background: linear-gradient(90deg, #667eea, #764ba2);
        }

        .service-card:nth-child(2)::before {
            background: linear-gradient(90deg, #f093fb, #f5576c);
        }

        .service-card:nth-child(3)::before {
            background: linear-gradient(90deg, #4facfe, #00f2fe);
        }

        .service-card:hover {
            transform: translateY(-12px) rotateX(2deg);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            border-radius: var(--pp-radius);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            margin-bottom: 25px;
            position: relative;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
        }

        /* Individual service icon themes */
        .service-icon.web-design {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .service-icon.seo-search {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
        }

        .service-icon.google-ads {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
        }

        /* Background pattern for icons */
        .icon-bg-pattern {
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="30" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="1"/><circle cx="50" cy="50" r="15" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23grain)"/></svg>') center/cover;
            opacity: 0;
            transition: opacity 0.3s ease, transform 0.3s ease;
            pointer-events: none;
        }

        .service-card:hover .service-icon {
            transform: translateY(-8px) scale(1.1);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }

        .service-card:hover .icon-bg-pattern {
            opacity: 1;
            transform: rotate(45deg);
        }

        .service-icon i {
            position: relative;
            z-index: 2;
            transition: transform 0.3s ease;
        }

        .service-card:hover .service-icon i {
            transform: scale(1.1) rotateY(10deg);
        }

        /* Add pulse animation for featured service */
        .service-card.featured .service-icon.seo-search {
            animation: subtle-pulse 3s ease-in-out infinite;
        }

        @keyframes subtle-pulse {
            0%, 100% { 
                box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1); 
            }
            50% { 
                box-shadow: 0 8px 35px rgba(245, 87, 108, 0.3); 
            }
        }

        .service-card h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
            color: var(--pp-black);
            font-weight: 700;
        }

        .service-card p {
            margin-bottom: 20px;
            color: var(--pp-gray-600);
            font-size: 1rem;
            line-height: 1.6;
        }

        .service-features {
            list-style: none;
            margin: 20px 0;
            padding: 0;
            flex-grow: 1;
        }

        .service-features li {
            padding: 8px 0;
            color: var(--pp-gray-600);
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.9rem;
        }

        .service-features li::before {
            content: "✔";
            color: var(--pp-primary);
            font-weight: bold;
            flex-shrink: 0;
        }

        .service-price {
            display: flex;
            align-items: baseline;
            gap: 8px;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid var(--pp-gray-200);
            position: relative;
            z-index: 2;
        }

        .service-price .from {
            font-size: 0.9rem;
            color: var(--pp-gray-500);
            font-weight: 500;
        }

        .service-price .amount {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--pp-primary);
        }

        .service-price .period {
            color: var(--pp-gray-500);
            font-size: 0.9rem;
            font-weight: 500;
        }


        /* ========================= 
           TESTIMONIALS SECTION 
           ========================= */
        .testimonials {
            background: var(--pp-gray-50);
            padding: 80px 0;
        }

        .testimonials-slider {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: var(--pp-radius);
            box-shadow: var(--pp-shadow);
            position: relative;
            transition: var(--pp-transition);
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--pp-shadow-xl);
        }

        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 30px;
            font-size: 4rem;
            color: var(--pp-primary);
            opacity: 0.1;
            font-family: Georgia, serif;
        }

        .testimonial-text {
            font-size: 1.1rem;
            line-height: 1.7;
            color: var(--pp-gray-700);
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
            padding-top: 20px;
            border-top: 1px solid var(--pp-gray-200);
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--pp-primary), var(--pp-primary-dark));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.2rem;
        }

        .author-info {
            flex: 1;
        }

        .author-name {
            font-weight: 600;
            color: var(--pp-black);
            margin-bottom: 2px;
        }

        .author-title {
            font-size: 0.9rem;
            color: var(--pp-gray-500);
        }

        .testimonial-rating {
            color: var(--pp-warning);
            font-size: 1.2rem;
            margin-bottom: 15px;
        }

        /* ========================= 
           ENHANCED PRICING SECTION 
           ========================= */
        .pricing {
            background: linear-gradient(135deg, var(--pp-gray-50) 0%, #f8fafc 100%);
            padding: 100px 0;
            position: relative;
        }

        .pricing::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="pricing-pattern" width="50" height="50" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="20" fill="none" stroke="rgba(44,134,249,0.03)" stroke-width="1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23pricing-pattern)"/></svg>');
            pointer-events: none;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            margin-top: 80px;
            align-items: stretch;
        }

        .pricing-card {
            background: linear-gradient(135deg, #fff 0%, #fafbfc 100%);
            border-radius: var(--pp-radius-lg);
            padding: 50px 40px;
            position: relative;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            border: 2px solid rgba(255, 255, 255, 0.8);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        /* Pricing tier themes */
        .pricing-card.starter-tier {
            background: linear-gradient(135deg, #fff 0%, #f0f9ff 100%);
        }

        .pricing-card.growth-tier {
            background: linear-gradient(135deg, #fff 0%, #f0f4ff 100%);
            border-color: #667eea;
            transform: scale(1.08) translateY(-10px);
        }

        .pricing-card.seo-tier {
            background: linear-gradient(135deg, #fff 0%, #f0fdf4 100%);
        }

        .pricing-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .pricing-card.growth-tier:hover {
            transform: scale(1.1) translateY(-20px);
            box-shadow: 0 40px 80px rgba(102, 126, 234, 0.3);
        }

        /* Pricing card icons */
        .pricing-icon {
            width: 70px;
            height: 70px;
            margin: 0 auto 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            position: relative;
            transition: transform 0.3s ease;
        }

        .starter-tier .pricing-icon {
            background: linear-gradient(135deg, #3b82f6, #1d4ed8);
            color: white;
        }

        .growth-tier .pricing-icon {
            background: linear-gradient(135deg, #f59e0b, #d97706);
            color: white;
        }

        .seo-tier .pricing-icon {
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
        }

        .pricing-card:hover .pricing-icon {
            transform: scale(1.15) rotate(10deg);
        }

        .pricing-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .pricing-title {
            font-size: 1.75rem;
            margin-bottom: 15px;
            color: var(--pp-black);
            font-weight: 700;
        }

        .pricing-price {
            display: flex;
            align-items: baseline;
            justify-content: center;
            gap: 8px;
            margin: 25px 0;
        }

        .pricing-currency {
            font-size: 1.5rem;
            color: var(--pp-gray-500);
            font-weight: 600;
        }

        .pricing-amount {
            font-size: 3.5rem;
            font-weight: 900;
            color: var(--pp-primary);
            line-height: 1;
        }

        .growth-tier .pricing-amount {
            color: #667eea;
        }

        .pricing-period {
            color: var(--pp-gray-500);
            font-size: 1.1rem;
            font-weight: 500;
        }

        .pricing-description {
            color: var(--pp-gray-600);
            font-size: 1.1rem;
            margin-top: 15px;
            line-height: 1.5;
        }

        /* Savings info */
        .savings-info {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin: 15px 0;
        }

        .original-price {
            color: var(--pp-gray-400);
            text-decoration: line-through;
            font-size: 1rem;
        }

        .savings {
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        .pricing-features {
            list-style: none;
            padding: 0;
            margin: 30px 0;
            flex-grow: 1;
        }

        .pricing-features li {
            padding: 15px 0;
            display: flex;
            align-items: center;
            gap: 15px;
            color: var(--pp-gray-700);
            font-size: 1rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }

        .pricing-features li:last-child {
            border-bottom: none;
        }

        .pricing-features li:hover {
            color: var(--pp-primary);
            transform: translateX(5px);
        }

        .pricing-features li i {
            width: 20px;
            height: 20px;
            flex-shrink: 0;
            transition: transform 0.3s ease;
        }

        .starter-tier .pricing-features li i {
            color: #3b82f6;
        }

        .growth-tier .pricing-features li i {
            color: #f59e0b;
        }

        .seo-tier .pricing-features li i {
            color: #10b981;
        }

        .pricing-features li:hover i {
            transform: scale(1.2);
        }

        /* CTA Section */
        .pricing-cta {
            text-align: center;
            margin-top: 40px;
        }

        .pricing-btn {
            width: 100%;
            padding: 18px 32px;
            font-size: 1.1rem;
            font-weight: 700;
            border-radius: var(--pp-radius);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .featured-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            border: none;
            color: white;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .featured-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.5);
        }

        .pricing-note {
            margin-top: 15px;
            color: var(--pp-gray-500);
            font-size: 0.9rem;
            font-style: italic;
        }

        /* Badges */
        .value-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(16, 185, 129, 0.3);
        }

        /* Responsive pricing */
        @media (max-width: 768px) {
            .pricing-grid {
                grid-template-columns: 1fr;
                gap: 30px;
                margin-top: 60px;
            }

            .pricing-card.growth-tier {
                transform: none;
            }

            .pricing-card:hover {
                transform: translateY(-10px);
            }

            .pricing-card.growth-tier:hover {
                transform: translateY(-10px);
            }
        }

        /* ========================= 
           ENHANCED FAQ SECTION 
           ========================= */
        .faq {
            padding: 80px 0;
            background: var(--pp-gray-50);
        }

        /* FAQ Search */
        .faq-search {
            margin: 40px 0 30px;
        }

        .search-container {
            max-width: 600px;
            margin: 0 auto;
            position: relative;
        }

        .search-container input {
            width: 100%;
            padding: 16px 24px;
            border: 2px solid var(--pp-gray-200);
            border-radius: var(--pp-radius);
            font-size: 1.1rem;
            transition: var(--pp-transition);
            background: white;
        }

        .search-container input:focus {
            outline: none;
            border-color: var(--pp-primary);
            box-shadow: 0 0 0 3px rgba(44, 134, 249, 0.1);
        }

        .search-results-count {
            position: absolute;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--pp-gray-500);
            font-size: 0.9rem;
            font-weight: 600;
        }

        /* FAQ Categories */
        .faq-categories {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0 50px;
            flex-wrap: wrap;
        }

        .faq-filter {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            border: 2px solid var(--pp-gray-200);
            background: white;
            border-radius: 50px;
            cursor: pointer;
            transition: var(--pp-transition);
            font-weight: 600;
            color: var(--pp-gray-600);
        }

        .faq-filter:hover {
            border-color: var(--pp-primary);
            color: var(--pp-primary);
            transform: translateY(-2px);
        }

        .faq-filter.active {
            background: var(--pp-primary);
            border-color: var(--pp-primary);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(44, 134, 249, 0.3);
        }

        .faq-filter i {
            font-size: 1rem;
        }

        /* FAQ Grid */
        .faq-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .faq-item {
            background: white;
            border-radius: var(--pp-radius);
            padding: 0;
            box-shadow: var(--pp-shadow);
            overflow: hidden;
            transition: var(--pp-transition);
            border: 2px solid transparent;
            opacity: 1;
            transform: translateY(0);
        }

        .faq-item.hidden {
            display: none;
        }

        .faq-item:hover {
            transform: translateY(-3px);
            box-shadow: var(--pp-shadow-lg);
            border-color: rgba(44, 134, 249, 0.2);
        }

        .faq-question {
            padding: 25px 30px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            font-weight: 600;
            color: var(--pp-black);
            transition: var(--pp-transition);
            border: none;
            background: none;
            width: 100%;
            text-align: left;
            font-size: 1rem;
            gap: 15px;
        }

        .faq-question:hover {
            background: var(--pp-gray-50);
        }

        .faq-question.active {
            background: var(--pp-gray-50);
            color: var(--pp-primary);
        }

        .faq-category-icon {
            margin-right: 12px;
            color: var(--pp-primary);
            font-size: 1.1rem;
            flex-shrink: 0;
            margin-top: 2px;
        }

        .faq-icon {
            font-size: 1.5rem;
            transition: transform 0.3s ease;
            flex-shrink: 0;
            margin-top: 2px;
        }

        .faq-question.active .faq-icon {
            transform: rotate(45deg);
        }

        .faq-answer {
            padding: 0 30px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease, padding 0.4s ease;
        }

        .faq-answer.active {
            padding: 0 30px 30px;
            max-height: 2000px;
        }

        .faq-answer p {
            margin-bottom: 15px;
            line-height: 1.7;
        }

        .faq-answer ul {
            margin: 15px 0;
            padding-left: 20px;
        }

        .faq-answer li {
            margin-bottom: 8px;
            line-height: 1.6;
        }

        .faq-answer strong {
            color: var(--pp-black);
        }

        .faq-answer em {
            color: var(--pp-primary);
            font-style: normal;
            font-weight: 600;
        }

        /* Enhanced FAQ Content Styles */
        .service-areas {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .area-group {
            background: var(--pp-gray-50);
            padding: 15px;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-primary);
        }

        .industry-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .industry-item {
            background: var(--pp-gray-50);
            padding: 12px;
            border-radius: var(--pp-radius-sm);
            font-size: 0.95rem;
        }

        .results-timeline {
            margin: 20px 0;
        }

        .timeline-item {
            margin: 20px 0;
            padding: 20px;
            border-radius: var(--pp-radius);
            border-left: 4px solid var(--pp-primary);
        }

        .timeline-item.immediate {
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.1), rgba(16, 185, 129, 0.05));
            border-left-color: var(--pp-success);
        }

        .timeline-item.short {
            background: linear-gradient(135deg, rgba(245, 158, 11, 0.1), rgba(245, 158, 11, 0.05));
            border-left-color: var(--pp-warning);
        }

        .timeline-item.medium {
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.1), rgba(44, 134, 249, 0.05));
            border-left-color: var(--pp-primary);
        }

        .timeline-item.long {
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(139, 92, 246, 0.05));
            border-left-color: #8b5cf6;
        }

        .result-examples {
            margin: 20px 0;
        }

        .result-item {
            background: var(--pp-gray-50);
            padding: 12px 16px;
            margin: 10px 0;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-success);
        }

        .support-channels {
            margin: 20px 0;
        }

        .support-item {
            background: var(--pp-gray-50);
            padding: 15px;
            margin: 10px 0;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-primary);
        }


        }

        .step-number {
            width: 40px;
            height: 40px;
            background: var(--pp-primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            flex-shrink: 0;
        }

        .step-content {
            flex: 1;
        }

        .step-content strong {
            display: block;
            margin-bottom: 8px;
            color: var(--pp-primary);
        }

        .reporting-types {
            margin: 20px 0;
        }

        .report-type {
            background: var(--pp-gray-50);
            padding: 12px 16px;
            margin: 10px 0;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-primary);
        }

        .security-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .security-item {
            background: var(--pp-gray-50);
            padding: 15px;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-success);
        }

        .differentiators {
            margin: 20px 0;
        }

        .diff-item {
            background: var(--pp-gray-50);
            padding: 15px;
            margin: 15px 0;
            border-radius: var(--pp-radius-sm);
            border-left: 4px solid var(--pp-primary);
        }

        /* Show More Button */
        .faq-show-more {
            text-align: center;
            margin: 50px 0 30px;
        }

        .faq-show-more .btn {
            background: white;
            border: 2px solid var(--pp-primary);
            color: var(--pp-primary);
            padding: 15px 30px;
            border-radius: 50px;
        }

        .faq-show-more .btn:hover {
            background: var(--pp-primary);
            color: white;
            transform: translateY(-2px);
        }

        /* FAQ CTA */
        .faq-cta {
            text-align: center;
            background: white;
            padding: 40px 30px;
            border-radius: var(--pp-radius-lg);
            box-shadow: var(--pp-shadow-lg);
            margin: 40px auto 0;
            max-width: 600px;
        }

        .faq-cta h3 {
            color: var(--pp-black);
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        .faq-cta p {
            color: var(--pp-gray-600);
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        .faq-cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .faq-cta-buttons .btn {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 14px 24px;
            border-radius: var(--pp-radius);
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .faq-categories {
                gap: 10px;
            }

            .faq-filter {
                padding: 10px 16px;
                font-size: 0.9rem;
            }

            .faq-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .faq-question {
                padding: 20px 20px;
            }

            .faq-answer.active {
                padding: 0 20px 25px;
            }

            .service-areas,
            .industry-grid,
            .security-features {
                grid-template-columns: 1fr;
            }

            .process-step {
                flex-direction: column;
                gap: 15px;
            }

            .faq-cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .faq-cta-buttons .btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
        }

        /* ========================= 
           CONTACT SECTION 
           ========================= */
        .contact {
            padding: 80px 0;
            background: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 60px;
            margin-top: 60px;
            align-items: start;
        }

        .contact-info h3 {
            color: var(--pp-black);
            margin-bottom: 30px;
            font-size: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 30px;
            padding: 20px;
            background: var(--pp-gray-50);
            border-radius: var(--pp-radius);
            transition: var(--pp-transition);
        }

        .contact-item:hover {
            background: var(--pp-gray-100);
            transform: translateX(5px);
        }

        .contact-item i {
            width: 24px;
            height: 24px;
            background: var(--pp-primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9rem;
            flex-shrink: 0;
            margin-top: 2px;
        }

        .contact-item div {
            flex: 1;
        }

        .contact-item strong {
            display: block;
            color: var(--pp-black);
            margin-bottom: 5px;
            font-weight: 600;
        }

        .contact-item a {
            color: var(--pp-primary);
            text-decoration: none;
            font-weight: 600;
            transition: var(--pp-transition);
        }

        .contact-item a:hover {
            color: var(--pp-primary-dark);
        }

        .contact-item span {
            color: var(--pp-gray-600);
        }

        /* Contact Form */
        .contact-form-container {
            background: var(--pp-gray-50);
            padding: 40px;
            border-radius: var(--pp-radius-lg);
            box-shadow: var(--pp-shadow);
        }

        .contact-form h3 {
            color: var(--pp-black);
            margin-bottom: 30px;
            font-size: 1.5rem;
            text-align: center;
        }

        .form-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--pp-black);
            font-weight: 600;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid var(--pp-gray-200);
            border-radius: var(--pp-radius-sm);
            font-size: 1rem;
            transition: var(--pp-transition);
            background: white;
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--pp-primary);
            box-shadow: 0 0 0 3px rgba(44, 134, 249, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .contact-form .btn {
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            font-size: 1.1rem;
            padding: 18px 24px;
            margin-top: 20px;
        }

        .form-note {
            text-align: center;
            color: var(--pp-gray-500);
            font-size: 0.9rem;
            margin-top: 15px;
            font-style: italic;
        }

        /* Contact Section Mobile */
        @media (max-width: 768px) {
            .contact-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .contact-form-container {
                padding: 30px 20px;
            }

            .form-grid {
                grid-template-columns: 1fr;
                gap: 15px;
            }

            .contact-item {
                padding: 15px;
            }
        }

        /* ========================= 
           ENHANCED CTA SECTION 
           ========================= */
        .cta {
            background: linear-gradient(135deg, var(--pp-primary) 0%, var(--pp-primary-dark) 50%, #0f4bb2 100%);
            padding: 100px 0;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .cta::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
            animation: ctaFloat 20s ease-in-out infinite;
        }

        .cta::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="cta-pattern" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="8" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23cta-pattern)"/></svg>');
            opacity: 0.3;
            animation: ctaPattern 30s linear infinite;
        }

        @keyframes ctaFloat {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            33% { transform: translate(-30px, -30px) rotate(120deg); }
            66% { transform: translate(30px, -20px) rotate(240deg); }
        }

        @keyframes ctaPattern {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(-20px) translateY(-20px); }
        }

        .cta-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }

        .cta-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 8px 20px;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 25px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            animation: ctaBadgeGlow 3s ease-in-out infinite;
        }

        @keyframes ctaBadgeGlow {
            0%, 100% { box-shadow: 0 0 20px rgba(255, 255, 255, 0.3); }
            50% { box-shadow: 0 0 30px rgba(255, 255, 255, 0.5); }
        }

        .cta h2 {
            color: white;
            margin-bottom: 25px;
            font-size: clamp(2.2rem, 4vw, 3.5rem);
            font-weight: 800;
            line-height: 1.1;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .cta p {
            color: rgba(255, 255, 255, 0.95);
            font-size: 1.3rem;
            margin-bottom: 45px;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.6;
            text-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
        }

        .cta-buttons {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 50px;
        }

        .cta .btn {
            background: white;
            color: var(--pp-primary);
            font-weight: 700;
            font-size: 1.1rem;
            padding: 18px 35px;
            border-radius: 50px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            border: 2px solid white;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            min-width: 200px;
        }

        .cta .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            transition: left 0.5s ease;
        }

        .cta .btn:hover::before {
            left: 100%;
        }

        .cta .btn:hover {
            background: rgba(255, 255, 255, 0.95);
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
            color: var(--pp-primary-dark);
        }

        .cta .btn-outline {
            background: transparent;
            color: white;
            border: 2px solid rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
        }

        .cta .btn-outline:hover {
            background: white;
            color: var(--pp-primary);
            border-color: white;
            transform: translateY(-3px) scale(1.02);
        }

        .cta-stats {
            display: flex;
            justify-content: center;
            gap: 50px;
            margin-top: 60px;
            flex-wrap: wrap;
        }

        .cta-stat {
            text-align: center;
            color: white;
        }

        .cta-stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            display: block;
            margin-bottom: 8px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .cta-stat-label {
            font-size: 1rem;
            opacity: 0.9;
            font-weight: 500;
        }

        /* ========================= 
           ENHANCED FOOTER 
           ========================= */
        footer {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
            color: white;
            padding: 80px 0 0;
            position: relative;
            overflow: hidden;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="footer-pattern" width="40" height="40" patternUnits="userSpaceOnUse"><circle cx="20" cy="20" r="1" fill="rgba(44,134,249,0.1)"/></pattern></defs><rect width="100%" height="100%" fill="url(%23footer-pattern)"/></svg>');
            opacity: 0.6;
        }

        footer::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--pp-primary), transparent);
        }

        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 50px;
            margin-bottom: 50px;
            position: relative;
            z-index: 1;
        }

        .footer-column {
            animation: footerFadeIn 0.8s ease-out;
        }

        .footer-column:nth-child(1) { animation-delay: 0.1s; }
        .footer-column:nth-child(2) { animation-delay: 0.2s; }
        .footer-column:nth-child(3) { animation-delay: 0.3s; }
        .footer-column:nth-child(4) { animation-delay: 0.4s; }

        @keyframes footerFadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .footer-column h4 {
            color: white;
            margin-bottom: 25px;
            font-size: 1.2rem;
            font-weight: 700;
            position: relative;
            padding-bottom: 10px;
        }
        .footer-column h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 30px;
            height: 3px;
            background: linear-gradient(90deg, var(--pp-primary), transparent);
            border-radius: 2px;
        }

        .footer-about {
            max-width: 350px;
        }

        .footer-about p {
            color: rgba(255, 255, 255, 0.8);
            margin: 25px 0;
            line-height: 1.7;
            font-size: 1.05rem;
        }

        .footer-links {
            list-style: none;
            padding: 0;
        }

        .footer-links li {
            margin-bottom: 15px;
            transition: transform 0.3s ease;
        }

        .footer-links li:hover {
            transform: translateX(5px);
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.75);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1rem;
            position: relative;
            display: inline-block;
            padding: 5px 0;
        }

        .footer-links a::before {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 0;
            height: 2px;
            background: var(--pp-primary);
            transition: width 0.3s ease;
        }

        .footer-links a:hover::before {
            width: 100%;
        }

        .footer-links a:hover {
            color: var(--pp-primary);
        }

        .footer-social {
            display: flex;
            gap: 20px;
            margin-top: 30px;
        }

        .social-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, rgba(44, 134, 249, 0.2), rgba(44, 134, 249, 0.1));
            border: 2px solid rgba(44, 134, 249, 0.3);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: rgba(255, 255, 255, 0.8);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            text-decoration: none;
            font-size: 1.2rem;
            position: relative;
            overflow: hidden;
        }

        .social-icon::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, var(--pp-primary), var(--pp-primary-dark));
            opacity: 0;
            transition: opacity 0.3s ease;
            border-radius: 50%;
        }

        .social-icon:hover::before {
            opacity: 1;
        }

        .social-icon:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 10px 25px rgba(44, 134, 249, 0.4);
            color: white;
            border-color: var(--pp-primary);
        }

        .social-icon i,
        .social-icon span {
            position: relative;
            z-index: 1;
        }

        .footer-contact-info {
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 15px;
            color: rgba(255, 255, 255, 0.8);
            font-size: 1rem;
        }

        .contact-item i {
            color: var(--pp-primary);
            width: 20px;
            text-align: center;
        }

        .footer-bottom {
            padding: 40px 0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            color: rgba(255, 255, 255, 0.6);
            position: relative;
            z-index: 1;
            background: rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
        }

        .footer-bottom-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .footer-legal-links {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        .footer-legal-links a {
            color: rgba(255, 255, 255, 0.6);
            text-decoration: none;
            transition: color 0.3s ease;
            font-size: 0.9rem;
        }

        .footer-legal-links a:hover {
            color: var(--pp-primary);
        }

        /* ========================= 
           ANIMATIONS 
           ========================= */
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

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease-out;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* ========================= 
           RESPONSIVE DESIGN 
           ========================= */
        @media (min-width: 769px) {
            .trust-content {
                flex-direction: row !important;
                justify-content: space-between !important;
                align-items: center !important;
            }
            .results-grid {
                grid-template-columns: repeat(4, 1fr) !important;
            }
        }

        @media (max-width: 1024px) and (min-width: 769px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-image {
                margin-top: 40px;
            }

            .hero-stats {
                position: static;
                margin-top: 30px;
            }

            .trust-content {
                justify-content: center;
                flex-wrap: wrap;
            }

            .results-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .process-steps {
                flex-direction: column;
                gap: 40px;
            }

            .timeline-line {
                display: none;
            }
        }

        @media (max-width: 768px) {
            /* Header Mobile */
            .nav-links {
                display: none !important;
            }

            .nav-cta .phone-number,
            .nav-cta .btn {
                display: none !important;
            }

            .menu-toggle {
                display: flex !important;
            }

            nav {
                padding: 15px 0 !important;
                gap: 15px !important;
            }

            .logo {
                padding: 8px 10px !important;
            }

            .logo-img {
                height: 50px !important;
            }

            /* Enhanced CTA Section Mobile */
            .cta {
                padding: 80px 0;
            }

            .cta h2 {
                font-size: 2.2rem;
                margin-bottom: 20px;
            }

            .cta p {
                font-size: 1.1rem;
                margin-bottom: 35px;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
                gap: 20px;
                margin-top: 40px;
            }

            .cta .btn {
                width: 100%;
                max-width: 300px;
                font-size: 1rem;
                padding: 16px 30px;
            }

            .cta-stats {
                gap: 30px;
                margin-top: 50px;
            }

            .cta-stat-number {
                font-size: 2rem;
            }

            .cta-stat-label {
                font-size: 0.9rem;
            }

            /* Enhanced Footer Mobile */
            .footer-content {
                grid-template-columns: 1fr !important;
                gap: 40px;
                text-align: center;
            }

            .footer-about {
                max-width: 100%;
            }

            .footer-about p {
                font-size: 1rem;
                margin: 20px 0;
            }

            .footer-social {
                justify-content: center;
                gap: 15px;
            }

            .social-icon {
                width: 45px;
                height: 45px;
                font-size: 1.1rem;
            }

            .footer-contact-info {
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }

            .contact-item {
                justify-content: center;
                font-size: 0.95rem;
            }

            .footer-bottom-content {
                flex-direction: column;
                text-align: center;
                gap: 15px;
            }

            .footer-legal-links {
                justify-content: center;
                gap: 20px;
            }

            /* Hero Section Mobile */
            .hero-content {
                grid-template-columns: 1fr !important;
                text-align: center;
                gap: 30px;
            }

            .hero-image {
                margin-top: 20px;
                order: 2;
            }

            .hero-text {
                order: 1;
            }

            .hero-stats {
                position: static;
                margin-top: 20px;
                display: flex;
                justify-content: center;
                gap: 20px;
            }

            /* Process Steps Mobile */
            .process {
                padding: 80px 0;
            }
            
            .process-timeline {
                padding: 0 15px;
            }
            
            .process-steps {
                display: flex !important;
                flex-direction: column;
                gap: 30px;
                align-items: center;
                grid-template-columns: none !important;
            }

            .process-step {
                max-width: 100%;
                width: 100%;
                padding: 0;
            }

            .timeline-line {
                display: none;
            }

            .step-content {
                min-height: auto;
            }

            /* Show all content on mobile */
            .step-process,
            .step-outcome,
            .client-example {
                display: block !important;
            }

            .step-header {
                text-align: center;
            }

            .step-timeline-info {
                flex-direction: row;
                justify-content: center;
                gap: 15px;
            }

            .step-week {
                position: static;
                transform: none;
                display: inline-block;
                margin-bottom: 10px;
            }

            /* Footer Mobile Fix */

            .footer-column footer-about {
                max-width: 100%;
                align-items: center;
            }
            
            .footer-content {
                grid-template-columns: 1fr !important;
                gap: 30px;
                align-items: center;
                text-align: center;

            }
        }

            .hero-buttons {
                flex-direction: column;
                width: 100%;
            }

            .btn {
                width: 100%;
                text-align: center;
            }

            .results-grid {
                grid-template-columns: 1fr;
            }

            .trust-content {
                flex-direction: column;
                align-items: center;
                text-align: center;
                gap: 20px;
            }

            .floating-cta {
                bottom: 20px;
                right: 20px;
            }

            .trust-badges {
                flex-wrap: wrap;
                justify-content: center;
            }

            h1 {
                font-size: 2rem;
            }

            h2 {
                font-size: 1.75rem;
            }

            .section {
                padding: 60px 0;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 15px !important;
                margin: 0 auto !important;
            }

            nav {
                padding: 12px 0 !important;
                gap: 10px !important;
            }

            .logo {
                padding: 6px 8px !important;
            }

            .logo-img {
                height: 45px !important;
            }

            .menu-toggle {
                padding: 8px !important;
            }

            .floating-cta-btn {
                padding: 12px 20px;
                font-size: 0.9rem;
            }

            /* Hero Section Mobile */
            .hero h1 {
                font-size: 1.75rem;
            }
            
            .hero-stats {
                flex-direction: column;
                gap: 10px;
            }

            /* Footer Mobile Fix */

            .footer-column footer-about {
                max-width: 100%;
                align-items: center;
            }
            
            .footer-content {
                grid-template-columns: 1fr !important;
                text-align: center;
            }

            .footer-column {
                margin-bottom: 20px;
            }

            .footer-about {
                max-width: 100%;
            }

            .footer-links {
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .footer-bottom {
                font-size: 0.85rem;
                padding: 20px 0;
                text-align: center;
            }
        }

        /* ========================= 
           UTILITY CLASSES 
           ========================= */
        .text-center { text-align: center; }
        .hidden { display: none; }
    </style>
</head>
<body>
    <!-- Scroll Progress Indicator -->
    <div class="scroll-progress">
        <div class="progress-bar" id="progressBar"></div>
    </div>

    <!-- Header -->
    <header id="header">
        <nav class="container">
            <a href="/" class="logo">
                <img src="https://theprofitplatform.com.au/wp-content/uploads/2025/08/cropped-The-Profit-Platform-Logo-1.png" alt="The Profit Platform Logo" class="logo-img">
            </a>

            <ul class="nav-links">
                <li><a href="#services">Services</a></li>
                <li><a href="#results">Results</a></li>
                <li><a href="#process">How It Works</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#pricing">Pricing</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            
            <div class="nav-cta">
              
                <a href="#contact" class="btn btn-primary">Get Free Audit</a>
            </div>

            <div class="menu-toggle" id="menuToggle">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <!-- Mobile Navigation Overlay -->
    <div class="mobile-nav-overlay" id="mobileNavOverlay"></div>

    <!-- Mobile Navigation Menu -->
    <div class="mobile-nav" id="mobileNav">
        <div class="mobile-nav-header">
            <div class="logo">
                <img src="https://theprofitplatform.com.au/wp-content/uploads/2025/08/cropped-The-Profit-Platform-Logo-1.png" alt="The Profit Platform Logo" class="logo-img" style="height: 40px;">
            </div>
            <button class="mobile-nav-close" id="mobileNavClose">&times;</button>
        </div>
        <div class="mobile-nav-links">
            <a href="#services">🎯 Services</a>
            <a href="#results">📈 Results</a>
            <a href="#process">⚙️ How It Works</a>
            <a href="#testimonials">⭐ Testimonials</a>
            <a href="#pricing">💰 Pricing</a>
            <a href="#faq">❓ FAQ</a>
            <a href="#contact">📞 Contact</a>
        </div>
        <div class="mobile-nav-cta">
            <a href="tel:0487286451" class="phone-number">0487 286 451</a>
            <a href="#contact" class="btn btn-primary">Get Free Audit</a>
        </div>
    </div>

    <!-- Enhanced Hero Section -->
    <section class="hero">
        <div class="hero-background-elements">
            <div class="floating-shape shape-1"></div>
            <div class="floating-shape shape-2"></div>
            <div class="floating-shape shape-3"></div>
        </div>
        
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    
                    
                    <h1 id="heroHeading" class="hero-title">
                        Get <span class="highlight-text">3x More</span> Local Customers in 
                        <span class="location-text">Sydney</span>
                        <div class="title-underline"></div>
                    </h1>
                    
                    <p class="subtitle">Stop losing customers to competitors. We help Sydney businesses dominate Google and get more enquiries with proven digital marketing strategies that actually work.</p>
                    
                    <div class="value-proposition">
                        <div class="value-item">
                            <i class="fas fa-rocket"></i>
                            <span>Get found on Google Maps & search results</span>
                        </div>
                        <div class="value-item">
                            <i class="fas fa-chart-line"></i>
                            <span>Convert more visitors into paying customers</span>
                        </div>
                        <div class="value-item">
                            <i class="fas fa-handshake"></i>
                            <span>No lock-in contracts - cancel anytime</span>
                        </div>
                    </div>

                    <div class="hero-cta-section">
                        <div class="hero-buttons">
                            <a href="#contact" class="btn btn-primary hero-primary-btn">
                                <span class="btn-text">Get Your Free $500 Marketing Audit</span>
                                <span class="btn-subtext">Usually $500 - Free for 48 hours</span>
                                <i class="fas fa-arrow-right btn-arrow"></i>
                            </a>
                            <a href="tel:0487286451" class="btn btn-secondary hero-call-btn">
                                <i class="fas fa-phone"></i>
                                <span>Call Now: 0487 286 451</span>
                            </a>
                        </div>
                        
                        <div class="hero-guarantee">
                            <i class="fas fa-shield-alt"></i>
                            <span>100% Risk-Free • No Setup Fees • Cancel Anytime</span>
                        </div>
                    </div>
                </div>

                <div class="hero-visual">
                    <div class="hero-image-container">
                        <img src="https://theprofitplatform.com.au/wp-content/uploads/2025/08/ChatGPT-Image-Aug-17-2025-11_30_04-PM.png" alt="Local SEO in Sydney" class="hero-main-image">
                        
                        <div class="floating-stats">
                            <div class="stat-card stat-1">
                                <div class="stat-icon">
                                    <i class="fas fa-users"></i>
                                </div>
                                <div class="stat-content">
                                    <span class="stat-number" data-target="247">0+</span>
                                    <span class="stat-label">Happy Clients</span>
                                </div>
                            </div>
                            
                            <div class="stat-card stat-2">
                                <div class="stat-icon">
                                    <i class="fas fa-chart-bar"></i>
                                </div>
                                <div class="stat-content">
                                    <span class="stat-number" data-target="3.2">0x</span>
                                    <span class="stat-label">Avg. ROI</span>
                                </div>
                            </div>
                            
                            <div class="stat-card stat-3">
                                <div class="stat-icon">
                                    <i class="fas fa-star"></i>
                                </div>
                                <div class="stat-content">
                                    <span class="stat-number" data-target="4.9">0</span>
                                    <span class="stat-label">Rating</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="success-notification">
                            <div class="notification-content">
                                <div class="notification-avatar">JM</div>
                                <div class="notification-text">
                                    <strong>John M.</strong> just got 12 new leads!
                                    <span class="notification-time">2 minutes ago</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Trust Bar -->
    <section class="trust-bar">
        <div class="container">
            <div class="trust-content">
                <div class="trust-item">
                    <strong>⭐⭐⭐⭐⭐</strong>
                    <span>4.9/5 from 150+ reviews</span>
                </div>
                <div class="trust-item">
                    <strong>Sydney-based</strong>
                    <span>Local team, local results</span>
                </div>
                <div class="trust-item">
                    <strong>No Lock-ins</strong>
                    <span>Month-to-month contracts</span>
                
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Results Section -->
    <section class="results section" id="results">
        <div class="results-background">
            <div class="results-pattern"></div>
        </div>
        
        <div class="container">
            <div class="section-header animate-on-scroll">
                <div class="section-badge">
                    <i class="fas fa-chart-line"></i>
                    <span>Proven Track Record</span>
                </div>
                <h2>Real Results for Sydney Businesses</h2>
                <p>We measure success in leads, sales, and ROI - not vanity metrics. Here are actual results from our recent clients.</p>
            </div>
            
            <div class="results-grid">
                <div class="result-card animate-on-scroll case-study-1" data-result="74">
                    <div class="result-header">
                        <div class="result-icon">
                            <i class="fas fa-phone-volume"></i>
                            <div class="icon-glow"></div>
                        </div>
                        <div class="result-badge success">Success Story</div>
                    </div>
                    
                    <div class="result-metrics">
                        <div class="before-after">
                            <div class="before">
                                <span class="label">Before</span>
                                <span class="value">12/week</span>
                            </div>
                            <div class="arrow">
                                <i class="fas fa-arrow-right"></i>
                            </div>
                            <div class="after">
                                <span class="label">After</span>
                                <span class="value">21/week</span>
                            </div>
                        </div>
                        
                        <div class="result-number" data-target="74">+0%</div>
                        <div class="result-label">More Phone Calls</div>
                    </div>
                    
                    <div class="result-details">
                        <div class="client-info">
                            <div class="client-avatar">MW</div>
                            <div class="client-details">
                                <strong>Mike's Plumbing</strong>
                                <span>Parramatta, NSW</span>
                            </div>
                        </div>
                        
                        <div class="result-timeline">
                            <i class="fas fa-clock"></i>
                            <span>60 days</span>
                        </div>
                    </div>
                    
                    <div class="result-testimonial">
                        <p>"The phone doesn't stop ringing now. Best investment I've made."</p>
                    </div>
                </div>
                
                <div class="result-card animate-on-scroll case-study-2" data-result="3.2">
                    <div class="result-header">
                        <div class="result-icon">
                            <i class="fas fa-calendar-check"></i>
                            <div class="icon-glow"></div>
                        </div>
                        <div class="result-badge growth">Growth</div>
                    </div>
                    
                    <div class="result-metrics">
                        <div class="before-after">
                            <div class="before">
                                <span class="label">Before</span>
                                <span class="value">8/week</span>
                            </div>
                            <div class="arrow">
                                <i class="fas fa-arrow-right"></i>
                            </div>
                            <div class="after">
                                <span class="label">After</span>
                                <span class="value">26/week</span>
                            </div>
                        </div>
                        
                        <div class="result-number" data-target="3.2">0x</div>
                        <div class="result-label">Booking Increase</div>
                    </div>
                    
                    <div class="result-details">
                        <div class="client-info">
                            <div class="client-avatar">SC</div>
                            <div class="client-details">
                                <strong>Sydney Physio Care</strong>
                                <span>North Shore, NSW</span>
                            </div>
                        </div>
                        
                        <div class="result-timeline">
                            <i class="fas fa-clock"></i>
                            <span>90 days</span>
                        </div>
                    </div>
                    
                    <div class="result-testimonial">
                        <p>"Our calendar is completely booked out. Amazing results!"</p>
                    </div>
                </div>
                
                <div class="result-card animate-on-scroll case-study-3" data-result="41">
                    <div class="result-header">
                        <div class="result-icon">
                            <i class="fas fa-dollar-sign"></i>
                            <div class="icon-glow"></div>
                        </div>
                        <div class="result-badge savings">Cost Savings</div>
                    </div>
                    
                    <div class="result-metrics">
                        <div class="before-after">
                            <div class="before">
                                <span class="label">Before</span>
                                <span class="value">$85</span>
                            </div>
                            <div class="arrow">
                                <i class="fas fa-arrow-right"></i>
                            </div>
                            <div class="after">
                                <span class="label">After</span>
                                <span class="value">$50</span>
                            </div>
                        </div>
                        
                        <div class="result-number" data-target="41">-0%</div>
                        <div class="result-label">Cost Per Lead</div>
                    </div>
                    
                    <div class="result-details">
                        <div class="client-info">
                            <div class="client-avatar">DE</div>
                            <div class="client-details">
                                <strong>Dan's Electrical</strong>
                                <span>Western Sydney, NSW</span>
                            </div>
                        </div>
                        
                        <div class="result-timeline">
                            <i class="fas fa-clock"></i>
                            <span>30 days</span>
                        </div>
                    </div>
                    
                    <div class="result-testimonial">
                        <p>"Cut my advertising costs in half while getting more leads."</p>
                    </div>
                </div>
                
                <div class="result-card animate-on-scroll case-study-4">
                    <div class="result-header">
                        <div class="result-icon">
                            <i class="fas fa-trophy"></i>
                            <div class="icon-glow"></div>
                        </div>
                        <div class="result-badge ranking">SEO Victory</div>
                    </div>
                    
                    <div class="result-metrics">
                        <div class="before-after">
                            <div class="before">
                                <span class="label">Before</span>
                                <span class="value">Page 3</span>
                            </div>
                            <div class="arrow">
                                <i class="fas fa-arrow-right"></i>
                            </div>
                            <div class="after">
                                <span class="label">After</span>
                                <span class="value">#1</span>
                            </div>
                        </div>
                        
                        <div class="result-number">#1</div>
                        <div class="result-label">Google Ranking</div>
                    </div>
                    
                    <div class="result-details">
                        <div class="client-info">
                            <div class="client-avatar">AE</div>
                            <div class="client-details">
                                <strong>Aussie Electric Pro</strong>
                                <span>Inner West, NSW</span>
                            </div>
                        </div>
                        
                        <div class="result-timeline">
                            <i class="fas fa-clock"></i>
                            <span>4 months</span>
                        </div>
                    </div>
                    
                    <div class="result-testimonial">
                        <p>"Finally ranking #1 for 'electrician sydney'. Game changer!"</p>
                    </div>
                </div>
            </div>
            
            <div class="results-cta animate-on-scroll">
                <h3>Ready to Be Our Next Success Story?</h3>
                <p>Join 247+ Sydney businesses already growing with our proven marketing strategies.</p>
                <a href="#contact" class="btn btn-primary results-btn">
                    <span>Get Your Results Plan</span>
                    <i class="fas fa-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Enhanced Services Section -->
    <section class="services section" id="services">
        <div class="container">
            <div class="section-header animate-on-scroll">
                <h2>Services That Drive Real Enquiries</h2>
                <p>Choose the perfect solution for your business growth. All services include monthly reporting and dedicated support.</p>
            </div>

            <div class="services-grid">
                <div class="service-card animate-on-scroll">
                    <div class="service-icon web-design">
                        <i class="fas fa-laptop-code"></i>
                        <div class="icon-bg-pattern"></div>
                    </div>
                    <h3>Web Design & Development</h3>
                    <p>Fast, mobile-first websites that convert visitors into customers. Built on WordPress with full ownership.</p>
                    <ul class="service-features">
                        <li>5-page responsive website</li>
                        <li>Contact forms & CRM integration</li>
                        <li>Google Analytics & tracking setup</li>
                        <li>2-second load time guarantee</li>
                    </ul>
                    <div class="service-price">
                        <span class="from">From</span>
                        <span class="amount">$1,790</span>
                        <span class="period">one-time</span>
                    </div>
                </div>

                <div class="service-card animate-on-scroll featured">
                        <div class="service-icon seo-search">
                        <i class="fas fa-search-location"></i>
                        <div class="icon-bg-pattern"></div>
                    </div>
                    <h3>SEO & Local Search</h3>
                    <p>Dominate Google search results and map pack. Get found by customers actively looking for your services.</p>
                    <ul class="service-features">
                        <li>Google My Business optimization</li>
                        <li>On-page & technical SEO</li>
                        <li>Monthly content creation</li>
                        <li>Competitor analysis & tracking</li>
                    </ul>
                    <div class="service-price">
                        <span class="from">From</span>
                        <span class="amount">$990</span>
                        <span class="period">/month</span>
                    </div>
                </div>

                <div class="service-card animate-on-scroll">
                    <div class="service-icon google-ads">
                        <i class="fas fa-bullhorn"></i>
                        <div class="icon-bg-pattern"></div>
                    </div>
                    <h3>Google & Meta Ads</h3>
                    <p>Instant visibility with targeted ads. We manage everything from setup to weekly optimization.</p>
                    <ul class="service-features">
                        <li>Campaign setup & management</li>
                        <li>Landing page optimization</li>
                        <li>A/B testing & refinement</li>
                        <li>Weekly performance reports</li>
                    </ul>
                    <div class="service-price">
                        <span class="from">From</span>
                        <span class="amount">$490</span>
                        <span class="period">/month + ad spend</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Testimonials Section -->
    <section class="testimonials section">
        <div class="container">
            <div class="section-header animate-on-scroll">
                <h2>Loved by Sydney Small Businesses</h2>
                <p>Don't just take our word for it - hear from our happy clients.</p>
            </div>

            <div class="testimonials-slider">
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-rating">⭐⭐⭐⭐⭐</div>
                    <blockquote class="testimonial-text">So impressed with the service, you helped my small business grow, and I'm really thankful. Super professional, super affordable, and just an all-round great experience.</blockquote>
                    <div class="testimonial-author">
                        <div class="author-avatar">TC</div>
                        <div class="author-info">
                            <div class="author-name">Tina Chen</div>
                            <div class="author-title">Owner, Sydney Dental Care</div>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-rating">⭐⭐⭐⭐⭐</div>
                    <blockquote class="testimonial-text">We started getting calls within a week. Clear advice and no fluff. The team knows what they're doing and delivers results.</blockquote>
                    <div class="testimonial-author">
                        <div class="author-avatar">JM</div>
                        <div class="author-info">
                            <div class="author-name">John Mitchell</div>
                            <div class="author-title">Local Electrician, South-West Sydney</div>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-rating">⭐⭐⭐⭐⭐</div>
                    <blockquote class="testimonial-text">Bookings doubled after the site refresh. Reporting is easy to understand and they're always available when I need them.</blockquote>
                    <div class="testimonial-author">
                        <div class="author-avatar">SK</div>
                        <div class="author-info">
                            <div class="author-name">Sarah Kim</div>
                            <div class="author-title">Physio Clinic, North Shore</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Interactive Process Timeline -->
    <section class="process section" id="process">
        <div class="process-background">
            <div class="process-pattern"></div>
            <div class="floating-elements">
                <div class="floating-element element-1"></div>
                <div class="floating-element element-2"></div>
                <div class="floating-element element-3"></div>
            </div>
        </div>
        
        <div class="container">
            <div class="section-header animate-on-scroll">
                <div class="section-badge">
                    <i class="fas fa-route"></i>
                    <span>Our Proven Process</span>
                </div>
                <h2>How We Transform Your Business</h2>
                <p>From struggling to get leads to becoming the go-to choice in your area. Here's exactly how we make it happen.</p>
            </div>

            <div class="process-overview animate-on-scroll">
                <div class="process-stats">
                    <div class="stat-item">
                        <div class="stat-number">30</div>
                        <div class="stat-label">Days to Results</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">247+</div>
                        <div class="stat-label">Success Stories</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">3.2x</div>
                        <div class="stat-label">Average Growth</div>
                    </div>
                </div>
            </div>

            <div class="process-timeline">
                <div class="timeline-line">
                    <div class="timeline-progress" id="timelineProgress"></div>
                </div>
                
                <div class="process-steps">
                    <div class="process-step active" data-step="1">
                        <div class="step-header">
                            <div class="step-timeline-info">
                                <div class="step-week">Week 1</div>
                                <div class="step-duration">2-3 Days</div>
                            </div>
                        </div>
                        
                        <div class="step-circle">
                            <div class="step-icon">
                                <i class="fas fa-search-dollar"></i>
                            </div>
                            <div class="pulse-ring"></div>
                            <div class="step-number">1</div>
                        </div>
                        
                        <div class="step-content">
                            <div class="step-badge discovery">Discovery</div>
                            <h3 class="step-title">Free Strategy Audit</h3>
                            <p class="step-description">We dive deep into your business, analyze your competition, and identify exactly why you're not getting more customers.</p>
                            
                            <div class="step-process">
                                <div class="process-item">
                                    <i class="fas fa-chart-line"></i>
                                    <span>Current performance analysis</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-users"></i>
                                    <span>Competitor research & gaps</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-bullseye"></i>
                                    <span>Target audience mapping</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-map-marked-alt"></i>
                                    <span>Local market opportunities</span>
                                </div>
                            </div>
                            
                            <div class="step-outcome">
                                <div class="outcome-header">
                                    <i class="fas fa-gift"></i>
                                    <span>You Get (Worth $500)</span>
                                </div>
                                <div class="deliverables">
                                    <div class="deliverable-item">
                                        <i class="fas fa-file-chart"></i>
                                        <span>Complete audit report</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-road"></i>
                                        <span>Custom growth roadmap</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-calculator"></i>
                                        <span>ROI projection</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="client-example">
                                <div class="example-text">
                                    <strong>Real Example:</strong> "We found Mike's Plumbing was missing 73% of local searches"
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="process-step" data-step="2">
                        <div class="step-header">
                            <div class="step-timeline-info">
                                <div class="step-week">Weeks 2-3</div>
                                <div class="step-duration">10-14 Days</div>
                            </div>
                        </div>
                        
                        <div class="step-circle">
                            <div class="step-icon">
                                <i class="fas fa-tools"></i>
                            </div>
                            <div class="pulse-ring"></div>
                            <div class="step-number">2</div>
                        </div>
                        
                        <div class="step-content">
                            <div class="step-badge building">Building</div>
                            <h3 class="step-title">Foundation & Assets</h3>
                            <p class="step-description">We build everything you need to dominate your local market - from optimized landing pages to professional ad campaigns.</p>
                            
                            <div class="step-process">
                                <div class="process-item">
                                    <i class="fas fa-code"></i>
                                    <span>Landing page creation</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-ad"></i>
                                    <span>Ad campaign setup</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-chart-bar"></i>
                                    <span>Analytics & tracking</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-search"></i>
                                    <span>SEO optimization</span>
                                </div>
                            </div>
                            
                            <div class="step-outcome">
                                <div class="outcome-header">
                                    <i class="fas fa-check-circle"></i>
                                    <span>What We Build</span>
                                </div>
                                <div class="deliverables">
                                    <div class="deliverable-item">
                                        <i class="fas fa-laptop"></i>
                                        <span>Conversion-optimized pages</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-bullhorn"></i>
                                        <span>Google & Facebook campaigns</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-phone"></i>
                                        <span>Call tracking system</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="client-example">
                                <div class="example-text">
                                    <strong>Behind the Scenes:</strong> "Every landing page is tested for 2-second load times"
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="process-step" data-step="3">
                        <div class="step-header">
                            <div class="step-timeline-info">
                                <div class="step-week">Week 4</div>
                                <div class="step-duration">7 Days</div>
                            </div>
                        </div>
                        
                        <div class="step-circle">
                            <div class="step-icon">
                                <i class="fas fa-rocket"></i>
                            </div>
                            <div class="pulse-ring"></div>
                            <div class="step-number">3</div>
                        </div>
                        
                        <div class="step-content">
                            <div class="step-badge launching">Launch</div>
                            <h3 class="step-title">Go Live & Optimize</h3>
                            <p class="step-description">Everything goes live and we immediately start testing and optimizing to find what works best for your specific market.</p>
                            
                            <div class="step-process">
                                <div class="process-item">
                                    <i class="fas fa-play-circle"></i>
                                    <span>Campaign activation</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-vial"></i>
                                    <span>A/B testing setup</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-eye"></i>
                                    <span>Performance monitoring</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-sliders-h"></i>
                                    <span>Real-time adjustments</span>
                                </div>
                            </div>
                            
                            <div class="step-outcome">
                                <div class="outcome-header">
                                    <i class="fas fa-chart-line"></i>
                                    <span>First Results</span>
                                </div>
                                <div class="deliverables">
                                    <div class="deliverable-item">
                                        <i class="fas fa-phone-volume"></i>
                                        <span>First leads within 48 hours</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-chart-pie"></i>
                                        <span>Daily performance reports</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-comments"></i>
                                        <span>Direct communication channel</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="client-example">
                                <div class="example-text">
                                    <strong>Typical Results:</strong> "Most clients see their first leads within 24-48 hours"
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="process-step" data-step="4">
                        <div class="step-header">
                            <div class="step-timeline-info">
                                <div class="step-week">Month 2+</div>
                                <div class="step-duration">Ongoing</div>
                            </div>
                        </div>
                        
                        <div class="step-circle">
                            <div class="step-icon">
                                <i class="fas fa-chart-area"></i>
                            </div>
                            <div class="pulse-ring"></div>
                            <div class="step-number">4</div>
                        </div>
                        
                        <div class="step-content">
                            <div class="step-badge scaling">Scaling</div>
                            <h3 class="step-title">Scale & Dominate</h3>
                            <p class="step-description">Once we find what works, we double down and scale it up. Weekly optimizations ensure you stay ahead of competitors.</p>
                            
                            <div class="step-process">
                                <div class="process-item">
                                    <i class="fas fa-expand-arrows-alt"></i>
                                    <span>Scale winning campaigns</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-wrench"></i>
                                    <span>Weekly optimizations</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-trophy"></i>
                                    <span>Competitor monitoring</span>
                                </div>
                                <div class="process-item">
                                    <i class="fas fa-handshake"></i>
                                    <span>Monthly strategy calls</span>
                                </div>
                            </div>
                            
                            <div class="step-outcome">
                                <div class="outcome-header">
                                    <i class="fas fa-star"></i>
                                    <span>Long-term Growth</span>
                                </div>
                                <div class="deliverables">
                                    <div class="deliverable-item">
                                        <i class="fas fa-file-alt"></i>
                                        <span>Detailed monthly reports</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-phone"></i>
                                        <span>Monthly strategy sessions</span>
                                    </div>
                                    <div class="deliverable-item">
                                        <i class="fas fa-bullseye"></i>
                                        <span>Continuous improvement</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="client-example">
                                <div class="example-text">
                                    <strong>Long-term Success:</strong> "After 6 months, most clients become the #1 choice in their area"
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="process-guarantee animate-on-scroll">
                <div class="guarantee-content">
                    <div class="guarantee-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div class="guarantee-text">
                        <h3>Our 30-Day Guarantee</h3>
                        <p>If you don't see measurable results within 30 days, we'll refund your first month and help you find a solution that works.</p>
                    </div>
                    <div class="guarantee-cta">
                        <a href="#contact" class="btn btn-primary">Start Your Transformation</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Pricing Section -->
    <section class="pricing section" id="pricing">
        <div class="container">
            <div class="section-header animate-on-scroll">
                <h2>Transparent Pricing, No Surprises</h2>
                <p>Choose your growth package. No lock-in contracts, cancel anytime.</p>
            </div>

            <div class="pricing-grid">
                <div class="pricing-card animate-on-scroll starter-tier">
                    <div class="pricing-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <div class="pricing-header">
                        <h3 class="pricing-title">Starter Website</h3>
                        <div class="pricing-price">
                            <span class="pricing-currency">$</span>
                            <span class="pricing-amount">1,790</span>
                            <span class="pricing-period">one-time</span>
                        </div>
                        <p class="pricing-description">Perfect for small businesses needing online presence</p>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check-circle"></i>5-page responsive website</li>
                        <li><i class="fas fa-check-circle"></i>Mobile optimized design</li>
                        <li><i class="fas fa-check-circle"></i>Contact forms & maps</li>
                        <li><i class="fas fa-check-circle"></i>Basic SEO setup</li>
                        <li><i class="fas fa-check-circle"></i>Google Analytics</li>
                        <li><i class="fas fa-check-circle"></i>2 rounds of revisions</li>
                        <li><i class="fas fa-check-circle"></i>1 month support</li>
                    </ul>
                    <div class="pricing-cta">
                        <a href="#contact" class="btn btn-outline pricing-btn">Get Started</a>
                        <p class="pricing-note">One-time setup fee</p>
                    </div>
                </div>

                <div class="pricing-card featured animate-on-scroll growth-tier">
                    <div class="value-badge">Best Value</div>
                    <div class="pricing-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <div class="pricing-header">
                        <h3 class="pricing-title">Growth Package</h3>
                        <div class="pricing-price">
                            <span class="pricing-currency">$</span>
                            <span class="pricing-amount">1,490</span>
                            <span class="pricing-period">/month</span>
                        </div>
                        <div class="savings-info">
                            <span class="original-price">Usually $2,200</span>
                            <span class="savings">Save 32%</span>
                        </div>
                        <p class="pricing-description">Complete digital marketing solution</p>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-star"></i>Everything in SEO package</li>
                        <li><i class="fas fa-star"></i>Google Ads management</li>
                        <li><i class="fas fa-star"></i>Facebook/Instagram ads</li>
                        <li><i class="fas fa-star"></i>Landing page creation</li>
                        <li><i class="fas fa-star"></i>Weekly optimization</li>
                        <li><i class="fas fa-star"></i>Call tracking & recording</li>
                        <li><i class="fas fa-star"></i>Monthly strategy calls</li>
                    </ul>
                    <div class="pricing-cta">
                        <a href="#contact" class="btn btn-primary pricing-btn featured-btn">Start Growing Now</a>
                        <p class="pricing-note">Complete marketing solution</p>
                    </div>
                </div>

                <div class="pricing-card animate-on-scroll seo-tier">
                    <div class="pricing-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="pricing-header">
                        <h3 class="pricing-title">SEO Package</h3>
                        <div class="pricing-price">
                            <span class="pricing-currency">$</span>
                            <span class="pricing-amount">990</span>
                            <span class="pricing-period">/month</span>
                        </div>
                        <p class="pricing-description">Dominate local search results</p>
                    </div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check-circle"></i>Local SEO optimization</li>
                        <li><i class="fas fa-check-circle"></i>Google My Business</li>
                        <li><i class="fas fa-check-circle"></i>On-page optimization</li>
                        <li><i class="fas fa-check-circle"></i>Monthly content (4 posts)</li>
                        <li><i class="fas fa-check-circle"></i>Link building</li>
                        <li><i class="fas fa-check-circle"></i>Competitor tracking</li>
                        <li><i class="fas fa-check-circle"></i>Monthly reports</li>
                    </ul>
                    <div class="pricing-cta">
                        <a href="#contact" class="btn btn-outline pricing-btn">Get Started</a>
                        <p class="pricing-note">Great for local businesses</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced FAQ Section -->
    <section class="faq section" id="faq">
        <div class="container">
            <div class="section-header animate-on-scroll">
                <h2>Frequently Asked Questions</h2>
                <p>Got questions? We've got comprehensive answers to help you make the right decision.</p>
            </div>

            <!-- FAQ Search -->
            <div class="faq-search animate-on-scroll">
                <div class="search-container">
                    <input type="text" id="faqSearch" placeholder="🔍 Search frequently asked questions..." />
                    <div class="search-results-count" id="searchCount"></div>
                </div>
            </div>

            <!-- FAQ Categories -->
            <div class="faq-categories animate-on-scroll">
                <button class="faq-filter active" data-category="all">
                    <i class="fas fa-th-large"></i> All Questions
                </button>
                <button class="faq-filter" data-category="services">
                    <i class="fas fa-cogs"></i> Services & Pricing
                </button>
                <button class="faq-filter" data-category="results">
                    <i class="fas fa-chart-line"></i> Results & Timeline
                </button>
                <button class="faq-filter" data-category="support">
                    <i class="fas fa-headset"></i> Support & Process
                </button>
                <button class="faq-filter" data-category="technical">
                    <i class="fas fa-code"></i> Technical & Ownership
                </button>
            </div>

            <div class="faq-grid" id="faqGrid">
                <!-- Services & Pricing -->
                <div class="faq-item animate-on-scroll" data-category="services">
                    <button class="faq-question" type="button">
                        <i class="fas fa-dollar-sign faq-category-icon"></i>
                        How is your pricing structured?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Transparent, no-surprise pricing:</strong></p>
                        <ul>
                            <li><strong>Website Design:</strong> One-time fee from $1,790 (includes 5 pages, mobile optimization, contact forms)</li>
                            <li><strong>SEO Services:</strong> Monthly packages from $990 (includes local SEO, content creation, technical optimization)</li>
                            <li><strong>Google Ads:</strong> Management fee from $490/month + your ad spend budget (you pay Google directly)</li>
                            <li><strong>Meta Ads:</strong> Same structure - management fee + ad spend</li>
                        </ul>
                        <p><em>No setup fees, no hidden costs, no long-term contracts required.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="services">
                    <button class="faq-question" type="button">
                        <i class="fas fa-handshake faq-category-icon"></i>
                        Are there any lock-in contracts?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>No lock-in contracts, ever.</strong> All our services are month-to-month because we believe in earning your business through results, not legal agreements.</p>
                        <p><strong>Cancellation terms:</strong></p>
                        <ul>
                            <li>30 days written notice for ongoing services</li>
                            <li>Pause services anytime (great for seasonal businesses)</li>
                            <li>Resume services whenever you're ready</li>
                            <li>Keep everything we've built - websites, ads accounts, analytics</li>
                        </ul>
                        <p><em>We're confident you'll want to stay because of the results we deliver.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="services">
                    <button class="faq-question" type="button">
                        <i class="fas fa-map-marker-alt faq-category-icon"></i>
                        What areas of Sydney do you service?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>We serve all of Greater Sydney:</strong></p>
                        <div class="service-areas">
                            <div class="area-group">
                                <strong>Inner Sydney:</strong> CBD, Surry Hills, Darlinghurst, Potts Point, Redfern
                            </div>
                            <div class="area-group">
                                <strong>North Shore:</strong> Chatswood, North Sydney, Neutral Bay, Mosman, Hornsby
                            </div>
                            <div class="area-group">
                                <strong>Eastern Suburbs:</strong> Bondi, Randwick, Double Bay, Woollahra, Maroubra
                            </div>
                            <div class="area-group">
                                <strong>Inner West:</strong> Newtown, Leichhardt, Balmain, Glebe, Marrickville
                            </div>
                            <div class="area-group">
                                <strong>Western Sydney:</strong> Parramatta, Penrith, Blacktown, Liverpool, Campbelltown
                            </div>
                            <div class="area-group">
                                <strong>Southern Sydney:</strong> Sutherland Shire, St George, Hurstville, Bankstown
                            </div>
                        </div>
                        <p><strong>Virtual consultations</strong> available for all NSW businesses. <strong>On-site meetings</strong> available within 50km of Sydney CBD.</p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="services">
                    <button class="faq-question" type="button">
                        <i class="fas fa-industry faq-category-icon"></i>
                        What industries do you work with?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>We specialize in local Sydney businesses across all industries:</strong></p>
                        <div class="industry-grid">
                            <div class="industry-item">🏠 <strong>Home Services:</strong> Plumbers, electricians, landscapers, cleaners</div>
                            <div class="industry-item">🏥 <strong>Health & Wellness:</strong> Dentists, physios, gyms, beauty salons</div>
                            <div class="industry-item">⚖️ <strong>Professional Services:</strong> Lawyers, accountants, consultants</div>
                            <div class="industry-item">🏪 <strong>Retail & E-commerce:</strong> Online stores, local retailers</div>
                            <div class="industry-item">🍴 <strong>Hospitality:</strong> Restaurants, cafes, catering</div>
                            <div class="industry-item">🚗 <strong>Automotive:</strong> Mechanics, car dealers, auto services</div>
                        </div>
                        <p><em>Every industry has unique challenges - we tailor our approach accordingly.</em></p>
                    </div>
                </div>

                <!-- Results & Timeline -->
                <div class="faq-item animate-on-scroll" data-category="results">
                    <button class="faq-question" type="button">
                        <i class="fas fa-rocket faq-category-icon"></i>
                        How quickly will I see results?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Results timeline by service:</strong></p>
                        <div class="results-timeline">
                            <div class="timeline-item immediate">
                                <strong>🚀 Immediate (24-48 hours):</strong>
                                <ul>
                                    <li>Google Ads campaigns go live</li>
                                    <li>Website improvements visible</li>
                                    <li>Analytics tracking active</li>
                                </ul>
                            </div>
                            <div class="timeline-item short">
                                <strong>📈 Short-term (1-4 weeks):</strong>
                                <ul>
                                    <li>First Google Ads leads and calls</li>
                                    <li>Google My Business improvements</li>
                                    <li>Website conversion rate improvements</li>
                                </ul>
                            </div>
                            <div class="timeline-item medium">
                                <strong>📊 Medium-term (1-3 months):</strong>
                                <ul>
                                    <li>Local SEO ranking improvements</li>
                                    <li>Increased organic website traffic</li>
                                    <li>More consistent lead flow</li>
                                </ul>
                            </div>
                            <div class="timeline-item long">
                                <strong>🎯 Long-term (3-6 months):</strong>
                                <ul>
                                    <li>Significant SEO results</li>
                                    <li>Established market presence</li>
                                    <li>Predictable ROI and growth</li>
                                </ul>
                            </div>
                        </div>
                        <p><em>We track and report on progress every step of the way.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="results">
                    <button class="faq-question" type="button">
                        <i class="fas fa-chart-bar faq-category-icon"></i>
                        What kind of results can I expect?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Real results from recent Sydney clients:</strong></p>
                        <div class="result-examples">
                            <div class="result-item">📞 <strong>Plumber (Inner West):</strong> +74% phone calls in 60 days</div>
                            <div class="result-item">💪 <strong>Gym (North Shore):</strong> +120% membership enquiries in 90 days</div>
                            <div class="result-item">🦷 <strong>Dental Practice (CBD):</strong> +45% new patient bookings in 45 days</div>
                            <div class="result-item">⚖️ <strong>Law Firm (Eastern Suburbs):</strong> +89% consultation requests in 4 months</div>
                            <div class="result-item">🔧 <strong>Auto Repair (Western Sydney):</strong> -35% cost per lead with Google Ads</div>
                        </div>
                        <p><strong>Typical improvements within 90 days:</strong></p>
                        <ul>
                            <li>2-5x increase in website enquiries</li>
                            <li>30-80% more phone calls</li>
                            <li>First page Google rankings for target keywords</li>
                            <li>ROI of 3:1 to 8:1 on advertising spend</li>
                        </ul>
                        <p><em>Results vary by industry and competition, but we guarantee you'll see measurable improvement.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="results">
                    <button class="faq-question" type="button">
                        <i class="fas fa-target faq-category-icon"></i>
                        Do you guarantee results?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Our guarantee:</strong> If you don't see measurable improvement in your key metrics within 90 days, we'll work for free until you do.</p>
                        <p><strong>What we guarantee:</strong></p>
                        <ul>
                            <li>✅ Increased website traffic and engagement</li>
                            <li>✅ Improved Google search visibility</li>
                            <li>✅ More enquiries through your website</li>
                            <li>✅ Better conversion rates</li>
                            <li>✅ Transparent monthly reporting</li>
                        </ul>
                        <p><strong>What we don't guarantee:</strong> Specific ranking positions or exact lead numbers (too many variables outside our control).</p>
                        <p><em>We're so confident in our process that we're willing to put our money where our mouth is.</em></p>
                    </div>
                </div>

                <!-- Support & Process -->
                <div class="faq-item animate-on-scroll" data-category="support">
                    <button class="faq-question" type="button">
                        <i class="fas fa-headset faq-category-icon"></i>
                        What kind of support do you provide?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Comprehensive support included:</strong></p>
                        <div class="support-channels">
                            <div class="support-item">
                                <strong>📞 Phone Support:</strong> Direct line to your account manager (not a call center)
                            </div>
                            <div class="support-item">
                                <strong>📧 Email Support:</strong> Response within 4 business hours
                            </div>
                            <div class="support-item">
                                <strong>💬 WhatsApp:</strong> Quick questions and urgent issues
                            </div>
                            <div class="support-item">
                                <strong>🖥️ Screen Share:</strong> We'll show you exactly what we're doing
                            </div>
                            <div class="support-item">
                                <strong>📊 Monthly Calls:</strong> Strategy review and planning sessions
                            </div>
                        </div>
                        <p><strong>Support hours:</strong> Monday-Friday 9am-6pm AEST. Emergency support available for critical issues.</p>
                        <p><em>You'll always talk to the same team members who know your business.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="support">
                    <button class="faq-question" type="button">
                        <i class="fas fa-clipboard-list faq-category-icon"></i>
                        How does the onboarding process work?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Simple 4-step process:</strong></p>
                        <div class="process-steps">
                            <div class="process-step">
                                <div class="step-number">1</div>
                                <div class="step-content">
                                    <strong>Discovery Call (Week 1):</strong>
                                    <p>45-minute strategy session to understand your business, goals, and challenges. We'll audit your current marketing and create a custom action plan.</p>
                                </div>
                            </div>
                            <div class="process-step">
                                <div class="step-number">2</div>
                                <div class="step-content">
                                    <strong>Setup & Build (Weeks 2-3):</strong>
                                    <p>We create your assets, set up tracking systems, and configure campaigns. You'll receive login details and training materials.</p>
                                </div>
                            </div>
                            <div class="process-step">
                                <div class="step-number">3</div>
                                <div class="step-content">
                                    <strong>Launch (Week 4):</strong>
                                    <p>Everything goes live with careful monitoring. We start with small budgets and scale what works best.</p>
                                </div>
                            </div>
                            <div class="process-step">
                                <div class="step-number">4</div>
                                <div class="step-content">
                                    <strong>Optimize & Scale (Ongoing):</strong>
                                    <p>Weekly optimizations, monthly strategy calls, and quarterly business reviews to ensure continuous growth.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="support">
                    <button class="faq-question" type="button">
                        <i class="fas fa-chart-pie faq-category-icon"></i>
                        How do you report on progress?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Transparent reporting you'll actually understand:</strong></p>
                        <div class="reporting-types">
                            <div class="report-type">
                                <strong>📊 Monthly Dashboard:</strong> Live access to all your key metrics 24/7
                            </div>
                            <div class="report-type">
                                <strong>📈 Monthly Reports:</strong> Detailed analysis of what's working and what's not
                            </div>
                            <div class="report-type">
                                <strong>📞 Monthly Calls:</strong> 30-minute review of results and next steps
                            </div>
                            <div class="report-type">
                                <strong>🚨 Weekly Alerts:</strong> Immediate notification of significant changes
                            </div>
                        </div>
                        <p><strong>We track metrics that matter to your business:</strong></p>
                        <ul>
                            <li>Phone calls and form submissions</li>
                            <li>Website traffic and user behavior</li>
                            <li>Google rankings and visibility</li>
                            <li>Conversion rates and cost per lead</li>
                            <li>ROI and revenue attribution</li>
                        </ul>
                        <p><em>No confusing jargon - just clear insights you can act on.</em></p>
                    </div>
                </div>

                <!-- Technical & Ownership -->
                <div class="faq-item animate-on-scroll" data-category="technical">
                    <button class="faq-question" type="button">
                        <i class="fas fa-user-check faq-category-icon"></i>
                        Do I own the website and assets you create?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Yes, you own everything - 100%!</strong></p>
                        <p><strong>What you own:</strong></p>
                        <ul>
                            <li>✅ Website files and database</li>
                            <li>✅ Domain name registration</li>
                            <li>✅ All content and images we create</li>
                            <li>✅ Google Ads account (admin access)</li>
                            <li>✅ Google Analytics account</li>
                            <li>✅ Google My Business listing</li>
                            <li>✅ Social media business accounts</li>
                            <li>✅ All login credentials and passwords</li>
                        </ul>
                        <p><strong>If you leave:</strong> Everything transfers to you immediately. We'll even help you transition to a new provider if needed.</p>
                        <p><em>No hostage situations - your business assets belong to you, always.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="technical">
                    <button class="faq-question" type="button">
                        <i class="fas fa-mobile-alt faq-category-icon"></i>
                        Will my website work on mobile phones?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Absolutely! Mobile-first design is standard.</strong></p>
                        <p><strong>What we include:</strong></p>
                        <ul>
                            <li>📱 Responsive design that works on all devices</li>
                            <li>⚡ Page load speeds under 3 seconds</li>
                            <li>👆 Touch-friendly buttons and navigation</li>
                            <li>📞 Click-to-call phone numbers</li>
                            <li>🗺️ Easy-to-find contact forms</li>
                            <li>🔍 Google mobile-friendly optimization</li>
                        </ul>
                        <p><strong>Why it matters:</strong> 70%+ of your customers will view your website on mobile. Google also uses mobile performance for search rankings.</p>
                        <p><em>Every website is tested on multiple devices before launch.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="technical">
                    <button class="faq-question" type="button">
                        <i class="fas fa-shield-alt faq-category-icon"></i>
                        How secure and reliable will my website be?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>Enterprise-level security and reliability:</strong></p>
                        <div class="security-features">
                            <div class="security-item">
                                <strong>🔒 SSL Certificate:</strong> All data encrypted in transit
                            </div>
                            <div class="security-item">
                                <strong>🛡️ Security Monitoring:</strong> 24/7 malware and hack detection
                            </div>
                            <div class="security-item">
                                <strong>💾 Daily Backups:</strong> Automatic backups stored securely
                            </div>
                            <div class="security-item">
                                <strong>⚡ 99.9% Uptime:</strong> Reliable hosting with redundancy
                            </div>
                            <div class="security-item">
                                <strong>🔧 Auto Updates:</strong> Security patches applied automatically
                            </div>
                            <div class="security-item">
                                <strong>🚨 Monitoring:</strong> Immediate alerts if anything goes wrong
                            </div>
                        </div>
                        <p><strong>Hosting location:</strong> Australian servers for faster loading speeds for Sydney visitors.</p>
                        <p><em>Your website will be more secure and reliable than 95% of small business websites.</em></p>
                    </div>
                </div>

                <div class="faq-item animate-on-scroll" data-category="support">
                    <button class="faq-question" type="button">
                        <i class="fas fa-star-half-alt faq-category-icon"></i>
                        What makes you different from other agencies?
                        <span class="faq-icon">+</span>
                    </button>
                    <div class="faq-answer">
                        <p><strong>We're local Sydney business owners who understand your challenges:</strong></p>
                        <div class="differentiators">
                            <div class="diff-item">
                                <strong>🏠 Local Focus:</strong> We live and work in Sydney - we understand the local market, competition, and customer behavior.
                            </div>
                            <div class="diff-item">
                                <strong>📊 Results Over Vanity:</strong> We measure success by your revenue growth, not meaningless metrics like "impressions."
                            </div>
                            <div class="diff-item">
                                <strong>📞 We Answer Our Phones:</strong> Direct access to decision makers - no account managers who don't know your business.
                            </div>
                            <div class="diff-item">
                                <strong>🤝 Partnership Approach:</strong> We become part of your team, not just another vendor. Your success is our success.
                            </div>
                            <div class="diff-item">
                                <strong>🔓 No Lock-ins:</strong> Month-to-month service because we earn your business every single month.
                            </div>
                            <div class="diff-item">
                                <strong>📈 Proven Track Record:</strong> 8+ years helping Sydney businesses grow, with 200+ happy clients and documented case studies.
                            </div>
                        </div>
                        <p><em>Most agencies promise the world but deliver reports. We deliver results.</em></p>
                    </div>
                </div>
            </div>

            <!-- Show More Button -->
            <div class="faq-show-more animate-on-scroll">
                <button id="showMoreFaqs" class="btn btn-outline">
                    <i class="fas fa-chevron-down"></i> Show More Questions
                </button>
            </div>

            <!-- Contact CTA -->
            <div class="faq-cta animate-on-scroll">
                <h3>Still have questions?</h3>
                <p>Get personalized answers in a free 15-minute consultation call.</p>
                <div class="faq-cta-buttons">
                    <a href="#contact" class="btn btn-primary">
                        <i class="fas fa-calendar"></i> Book Free Call
                    </a>
                    <a href="tel:0487286451" class="btn btn-outline">
                        <i class="fas fa-phone"></i> Call Now: 0487 286 451
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact section" id="contact">
        <div class="container">
            <div class="section-header animate-on-scroll">
                <h2>Ready to Get Started?</h2>
                <p>Get your free digital marketing audit and growth plan. No obligations, just valuable insights.</p>
            </div>

            <div class="contact-content">
                <div class="contact-info animate-on-scroll">
                    <h3>Get In Touch</h3>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <strong>Phone</strong>
                            <a href="tel:0487286451">0487 286 451</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <strong>Email</strong>
                            <a href="mailto:avi@profitplatform.com.au">avi@profitplatform.com.au</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <strong>Location</strong>
                            <span>Sydney, NSW Australia</span>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <strong>Hours</strong>
                            <span>Mon-Fri: 9am-6pm AEST</span>
                        </div>
                    </div>
                </div>

                <div class="contact-form-container animate-on-scroll">
                    <form class="contact-form">
                        <h3>Get Your Free Growth Audit</h3>
                        <div class="form-grid">
                            <div class="form-group">
                                <label for="name">Full Name *</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            <div class="form-group">
                                <label for="phone">Phone Number *</label>
                                <input type="tel" id="phone" name="phone" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Email Address *</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            <div class="form-group">
                                <label for="company">Company Name</label>
                                <input type="text" id="company" name="company">
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="website">Current Website (if any)</label>
                            <input type="url" id="website" name="website" placeholder="https://">
                        </div>
                        <div class="form-group">
                            <label for="budget">Monthly Marketing Budget</label>
                            <select id="budget" name="budget">
                                <option value="">Select budget range</option>
                                <option value="1000-2500">$1,000 - $2,500</option>
                                <option value="2500-5000">$2,500 - $5,000</option>
                                <option value="5000-10000">$5,000 - $10,000</option>
                                <option value="10000+">$10,000+</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">Tell us about your business goals</label>
                            <textarea id="message" name="message" rows="4" placeholder="What are your main challenges? What would you like to achieve?"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">
                            <i class="fas fa-rocket"></i> Get My Free Audit
                        </button>
                        <p class="form-note">We'll get back to you within 4 hours with your personalized growth plan.</p>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced CTA Section -->
    <section class="cta" id="contact">
        <div class="container">
            <div class="cta-content">
                <div class="cta-badge">🚀 No Lock-In Contracts</div>
                <h2>Ready to Dominate Your Market?</h2>
                <p>Join 247+ successful Sydney businesses. Get your free growth audit and discover exactly how to triple your leads in 90 days.</p>
                <div class="cta-buttons">
                    <a href="#contact" class="btn">Get Your Free Audit</a>
                    <a href="tel:0487286451" class="btn btn-outline">📞 Call Now</a>
                </div>
                <div class="cta-stats">
                    <div class="cta-stat">
                        <span class="cta-stat-number">247+</span>
                        <span class="cta-stat-label">Happy Clients</span>
                    </div>
                    <div class="cta-stat">
                        <span class="cta-stat-number">3.2x</span>
                        <span class="cta-stat-label">Average ROI</span>
                    </div>
                    <div class="cta-stat">
                        <span class="cta-stat-number">90 Days</span>
                        <span class="cta-stat-label">Average Results</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column footer-about">
                    <h4>The Profit Platform</h4>
                    <p>Australia's fastest-growing digital marketing agency. We've helped 247+ Sydney businesses triple their leads and dominate their competition with proven marketing strategies.</p>
                    <div class="footer-social">
                        <a href="https://facebook.com/theprofitplatform" class="social-icon" aria-label="Facebook" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://linkedin.com/company/theprofitplatform" class="social-icon" aria-label="LinkedIn" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://instagram.com/theprofitplatform" class="social-icon" aria-label="Instagram" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="https://youtube.com/theprofitplatform" class="social-icon" aria-label="YouTube" target="_blank">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </div>
                </div>

                <div class="footer-column">
                    <h4>🎯 Services</h4>
                    <ul class="footer-links">
                        <li><a href="#services">Website Design & Development</a></li>
                        <li><a href="#services">Local SEO & Google Ranking</a></li>
                        <li><a href="#services">Google & Meta Ads</a></li>
                        <li><a href="#services">Conversion Optimization</a></li>
                        <li><a href="#services">Marketing Automation</a></li>
                    </ul>
                </div>

                <div class="footer-column">
                    <h4>🏢 Company</h4>
                    <ul class="footer-links">
                        <li><a href="#results">Success Stories</a></li>
                        <li><a href="#testimonials">Client Reviews</a></li>
                        <li><a href="#pricing">Transparent Pricing</a></li>
                        <li><a href="#faq">Frequently Asked Questions</a></li>
                        <li><a href="#process">How We Work</a></li>
                    </ul>
                </div>

                <div class="footer-column">
                    <h4>📞 Contact Us</h4>
                    <div class="footer-contact-info">
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Sydney, NSW Australia</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <a href="tel:0487286451">0487 286 451</a>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <a href="mailto:avi@theprofitplatform.com.au">avi@theprofitplatform.com.au</a>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <span>Mon-Fri: 9am-8pm AEST</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="footer-bottom">
                <div class="container">
                    <div class="footer-bottom-content">
                        <p>&copy; 2024 The Profit Platform. All rights reserved.</p>
                        <div class="footer-legal-links">
                            <a href="#privacy">Privacy Policy</a>
                            <a href="#terms">Terms of Service</a>
                            <a href="#cookies">Cookie Policy</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <!-- Floating CTA -->
    
    <script>
        // Scroll Progress Bar
        function updateScrollProgress() {
            const scrollTop = window.scrollY;
            const docHeight = document.documentElement.scrollHeight - window.innerHeight;
            const scrollPercent = (scrollTop / docHeight) * 100;
            document.getElementById('progressBar').style.width = scrollPercent + '%';
        }

        window.addEventListener('scroll', updateScrollProgress);

        // Floating CTA visibility
        window.addEventListener('scroll', () => {
            const floatingCta = document.getElementById('floatingCta');
            if (window.scrollY > 500) {
                floatingCta.classList.add('visible');
            } else {
                floatingCta.classList.remove('visible');
            }
        });

        // Animated Counters
        function animateCounter(element, target, suffix = '') {
            let current = 0;
            const increment = target / 100;
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    current = target;
                    clearInterval(timer);
                }
                
                if (suffix === 'x') {
                    element.textContent = current.toFixed(1) + suffix;
                } else if (suffix === '%') {
                    element.textContent = (suffix === '-' ? '-' : '+') + Math.floor(current) + '%';
                } else {
                    element.textContent = (suffix === '-' ? '-' : '+') + Math.floor(current) + '%';
                }
            }, 20);
        }

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.3,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    
                    // Animate counters
                    if (entry.target.classList.contains('result-card')) {
                        const numberEl = entry.target.querySelector('.result-number');
                        const target = parseFloat(entry.target.dataset.result);
                        
                        if (target === 74) {
                            animateCounter(numberEl, target, '%');
                        } else if (target === 3.2) {
                            animateCounter(numberEl, target, 'x');
                        } else if (target === 41) {
                            animateCounter(numberEl, target, '-%');
                        }
                    }
                }
            });
        }, observerOptions);

        // Observe all animated elements
        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            observer.observe(el);
        });

        // Interactive Process Timeline
        const processSteps = document.querySelectorAll('.process-step');
        const timelineProgress = document.getElementById('timelineProgress');

        processSteps.forEach((step, index) => {
            step.addEventListener('click', () => {
                // Remove active class from all steps
                processSteps.forEach(s => s.classList.remove('active', 'completed'));
                
                // Add active class to clicked step
                step.classList.add('active');
                
                // Add completed class to previous steps
                for (let i = 0; i < index; i++) {
                    processSteps[i].classList.add('completed');
                }
                
                // Update timeline progress
                const progressPercent = ((index + 1) / processSteps.length) * 100;
                timelineProgress.style.width = progressPercent + '%';
            });
        });

        // Auto-advance timeline every 3 seconds
        let currentStep = 0;
        setInterval(() => {
            if (currentStep < processSteps.length - 1) {
                currentStep++;
            } else {
                currentStep = 0;
            }
            
            processSteps.forEach(s => s.classList.remove('active', 'completed'));
            processSteps[currentStep].classList.add('active');
            
            for (let i = 0; i < currentStep; i++) {
                processSteps[i].classList.add('completed');
            }
            
            const progressPercent = ((currentStep + 1) / processSteps.length) * 100;
            timelineProgress.style.width = progressPercent + '%';
        }, 3000);

        // Enhanced FAQ functionality
        let visibleFaqs = 6; // Show only first 6 FAQs initially
        let allFaqs = [];
        let filteredFaqs = [];

        function initializeFAQs() {
            allFaqs = Array.from(document.querySelectorAll('.faq-item'));
            filteredFaqs = [...allFaqs];
            
            // Hide FAQs beyond the initial visible count
            updateFAQVisibility();
            updateSearchCount();
        }

        function updateFAQVisibility() {
            allFaqs.forEach((faq, index) => {
                const shouldShow = filteredFaqs.includes(faq) && index < visibleFaqs;
                faq.style.display = shouldShow ? 'block' : 'none';
                
                if (!shouldShow) {
                    // Close expanded FAQs when hiding
                    const question = faq.querySelector('.faq-question');
                    const answer = faq.querySelector('.faq-answer');
                    question.classList.remove('active');
                    answer.classList.remove('active');
                }
            });

            // Update "Show More" button
            const showMoreBtn = document.getElementById('showMoreFaqs');
            const hiddenCount = filteredFaqs.length - Math.min(visibleFaqs, filteredFaqs.length);
            
            if (hiddenCount > 0) {
                showMoreBtn.style.display = 'block';
                showMoreBtn.innerHTML = `<i class="fas fa-chevron-down"></i> Show ${hiddenCount} More Questions`;
            } else {
                showMoreBtn.style.display = 'none';
            }
        }

        function updateSearchCount() {
            const countEl = document.getElementById('searchCount');
            const visibleCount = Math.min(visibleFaqs, filteredFaqs.length);
            const totalCount = allFaqs.length;
            
            if (filteredFaqs.length < totalCount) {
                countEl.textContent = `${filteredFaqs.length} of ${totalCount} questions`;
            } else {
                countEl.textContent = `${totalCount} questions`;
            }
        }

        // FAQ Search functionality
        function initializeSearch() {
            const searchInput = document.getElementById('faqSearch');
            
            searchInput.addEventListener('input', function() {
                const searchTerm = this.value.toLowerCase().trim();
                
                if (searchTerm === '') {
                    filteredFaqs = [...allFaqs];
                } else {
                    filteredFaqs = allFaqs.filter(faq => {
                        const question = faq.querySelector('.faq-question').textContent.toLowerCase();
                        const answer = faq.querySelector('.faq-answer').textContent.toLowerCase();
                        return question.includes(searchTerm) || answer.includes(searchTerm);
                    });
                }
                
                // Reset visible count when searching
                visibleFaqs = searchTerm === '' ? 6 : Math.max(6, filteredFaqs.length);
                updateFAQVisibility();
                updateSearchCount();
            });
        }

        // FAQ Category filtering
        function initializeFilters() {
            const filterButtons = document.querySelectorAll('.faq-filter');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Update active filter
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    this.classList.add('active');
                    
                    const category = this.dataset.category;
                    
                    if (category === 'all') {
                        filteredFaqs = [...allFaqs];
                    } else {
                        filteredFaqs = allFaqs.filter(faq => 
                            faq.dataset.category === category
                        );
                    }
                    
                    // Reset search
                    document.getElementById('faqSearch').value = '';
                    
                    // Show more FAQs when filtering to specific category
                    visibleFaqs = category === 'all' ? 6 : Math.max(6, filteredFaqs.length);
                    updateFAQVisibility();
                    updateSearchCount();
                });
            });
        }

        // FAQ accordion functionality
        function initializeAccordion() {
            document.querySelectorAll('.faq-question').forEach(question => {
                question.addEventListener('click', function() {
                    const answer = this.nextElementSibling;
                    const icon = this.querySelector('.faq-icon');
                    
                    // Toggle current item
                    const isActive = this.classList.contains('active');
                    
                    // Close other items first
                    document.querySelectorAll('.faq-question').forEach(otherQuestion => {
                        if (otherQuestion !== this) {
                            otherQuestion.classList.remove('active');
                            otherQuestion.nextElementSibling.classList.remove('active');
                        }
                    });
                    
                    // Toggle current item
                    if (isActive) {
                        this.classList.remove('active');
                        answer.classList.remove('active');
                    } else {
                        this.classList.add('active');
                        answer.classList.add('active');
                        
                        // Smooth scroll to question
                        setTimeout(() => {
                            this.scrollIntoView({
                                behavior: 'smooth',
                                block: 'nearest'
                            });
                        }, 300);
                    }
                });
            });
        }

        // Show More functionality
        function initializeShowMore() {
            const showMoreBtn = document.getElementById('showMoreFaqs');
            
            showMoreBtn.addEventListener('click', function() {
                const remainingFaqs = filteredFaqs.length - visibleFaqs;
                visibleFaqs += Math.min(6, remainingFaqs); // Show 6 more or all remaining
                
                updateFAQVisibility();
                
                // Smooth scroll to first newly visible FAQ
                const firstNewFaq = filteredFaqs[visibleFaqs - Math.min(6, remainingFaqs)];
                if (firstNewFaq) {
                    setTimeout(() => {
                        firstNewFaq.scrollIntoView({
                            behavior: 'smooth',
                            block: 'center'
                        });
                    }, 100);
                }
            });
        }

        // Initialize all FAQ functionality
        function initializeEnhancedFAQ() {
            initializeFAQs();
            initializeSearch();
            initializeFilters();
            initializeAccordion();
            initializeShowMore();
        }

        // Header functionality
        function initializeHeader() {
            const header = document.getElementById('header');
            const menuToggle = document.getElementById('menuToggle');
            const mobileNav = document.getElementById('mobileNav');
            const mobileNavOverlay = document.getElementById('mobileNavOverlay');
            const mobileNavClose = document.getElementById('mobileNavClose');

            // Enhanced header scroll effect with active navigation
            window.addEventListener('scroll', () => {
                const header = document.getElementById('header');
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }

                // Update active navigation links based on scroll position
                updateActiveNavLink();
            });

            // Smooth scrolling for navigation links
            function setupSmoothScrolling() {
                document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                    anchor.addEventListener('click', function (e) {
                        e.preventDefault();
                        const target = document.querySelector(this.getAttribute('href'));
                        if (target) {
                            const headerHeight = document.getElementById('header').offsetHeight;
                            const targetPosition = target.offsetTop - headerHeight - 20;
                            
                            window.scrollTo({
                                top: targetPosition,
                                behavior: 'smooth'
                            });
                            
                            // Close mobile nav if open
                            closeMobileNav();
                        }
                    });
                });
            }

            // Update active navigation link
            function updateActiveNavLink() {
                const sections = document.querySelectorAll('section[id]');
                const navLinks = document.querySelectorAll('.nav-links a, .mobile-nav-links a');
                const headerHeight = document.getElementById('header').offsetHeight;
                
                let activeSection = '';
                
                sections.forEach(section => {
                    const sectionTop = section.offsetTop - headerHeight - 100;
                    const sectionBottom = sectionTop + section.offsetHeight;
                    
                    if (window.scrollY >= sectionTop && window.scrollY < sectionBottom) {
                        activeSection = section.getAttribute('id');
                    }
                });
                
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === `#${activeSection}`) {
                        link.classList.add('active');
                    }
                });
            }

            // Mobile menu functions
            function openMobileNav() {
                menuToggle.classList.add('active');
                mobileNav.classList.add('active');
                mobileNavOverlay.classList.add('active');
                document.body.style.overflow = 'hidden';
            }

            function closeMobileNav() {
                menuToggle.classList.remove('active');
                mobileNav.classList.remove('active');
                mobileNavOverlay.classList.remove('active');
                document.body.style.overflow = '';
            }

            // Event listeners
            if (menuToggle) {
                menuToggle.addEventListener('click', openMobileNav);
            }

            if (mobileNavClose) {
                mobileNavClose.addEventListener('click', closeMobileNav);
            }

            if (mobileNavOverlay) {
                mobileNavOverlay.addEventListener('click', closeMobileNav);
            }

            // Close mobile nav when clicking on links
            document.querySelectorAll('.mobile-nav-links a').forEach(link => {
                link.addEventListener('click', closeMobileNav);
            });

            // Close mobile nav on escape key
            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape' && mobileNav.classList.contains('active')) {
                    closeMobileNav();
                }
            });

            // Prevent body scroll when mobile nav is open
            window.addEventListener('resize', () => {
                if (window.innerWidth > 768 && mobileNav.classList.contains('active')) {
                    closeMobileNav();
                }
            });

            // Initialize enhanced navigation features
            document.addEventListener('DOMContentLoaded', () => {
                setupSmoothScrolling();
                updateActiveNavLink();
                initCTAAnimations();
                initFooterAnimations();
            });

            // Enhanced CTA Section Animations
            function initCTAAnimations() {
                const ctaStats = document.querySelectorAll('.cta-stat-number');
                
                // Animate stats when CTA section comes into view
                const ctaObserver = new IntersectionObserver((entries) => {
                    entries.forEach(entry => {
                        if (entry.isIntersecting) {
                            ctaStats.forEach((stat, index) => {
                                setTimeout(() => {
                                    stat.style.animation = 'ctaCountUp 1s ease-out forwards';
                                    stat.style.transform = 'scale(1.1)';
                                    setTimeout(() => {
                                        stat.style.transform = 'scale(1)';
                                    }, 200);
                                }, index * 200);
                            });
                        }
                    });
                }, { threshold: 0.5 });

                const ctaSection = document.querySelector('.cta');
                if (ctaSection) {
                    ctaObserver.observe(ctaSection);
                }

                // Add hover effects to CTA buttons
                document.querySelectorAll('.cta .btn').forEach(btn => {
                    btn.addEventListener('mouseenter', function() {
                        this.style.transform = 'translateY(-3px) scale(1.02)';
                    });
                    
                    btn.addEventListener('mouseleave', function() {
                        this.style.transform = 'translateY(0) scale(1)';
                    });
                });
            }

            // Enhanced Footer Animations
            function initFooterAnimations() {
                // Animate footer columns on scroll
                const footerColumns = document.querySelectorAll('.footer-column');
                
                const footerObserver = new IntersectionObserver((entries) => {
                    entries.forEach(entry => {
                        if (entry.isIntersecting) {
                            entry.target.style.animation = 'footerFadeIn 0.8s ease-out forwards';
                        }
                    });
                }, { threshold: 0.3 });

                footerColumns.forEach(column => {
                    footerObserver.observe(column);
                });

                // Add pulse effect to social icons
                document.querySelectorAll('.social-icon').forEach(icon => {
                    icon.addEventListener('mouseenter', function() {
                        this.style.animation = 'socialPulse 0.5s ease-out';
                    });
                    
                    icon.addEventListener('animationend', function() {
                        this.style.animation = '';
                    });
                });
            }

            // Add new keyframes for animations
            const ctaStyles = `
                @keyframes ctaCountUp {
                    from { opacity: 0.5; transform: translateY(20px); }
                    to { opacity: 1; transform: translateY(0); }
                }
                
                @keyframes socialPulse {
                    0% { transform: scale(1); }
                    50% { transform: scale(1.15); }
                    100% { transform: scale(1); }
                }
            `;
            
            const styleSheet = document.createElement('style');
            styleSheet.textContent = ctaStyles;
            document.head.appendChild(styleSheet);

            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        const headerHeight = header.offsetHeight;
                        const targetPosition = target.offsetTop - headerHeight - 20;
                        
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        }

        // Call initialization after DOM is loaded
        document.addEventListener('DOMContentLoaded', function() {
            initializeHeader();
            initializeEnhancedFAQ();
        });

    </script>
</body>
</html>
- Rember that I am using Wordpress with Kaedence Theme and plugins like Rank Math. Yes start with Phase 1 .