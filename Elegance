<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elegance Studio | Creative Digital Agency</title>
    <style>
        /* ============ RESET & BASE ============ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6C63FF;
            --primary-dark: #5A52D5;
            --secondary: #FF6584;
            --dark: #1a1a2e;
            --darker: #16162a;
            --light: #f0f0f7;
            --text: #333;
            --text-light: #888;
            --white: #ffffff;
            --gradient: linear-gradient(135deg, #6C63FF, #FF6584);
            --shadow: 0 10px 40px rgba(108, 99, 255, 0.15);
            --shadow-hover: 0 20px 60px rgba(108, 99, 255, 0.25);
            --transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: var(--text);
            overflow-x: hidden;
            background: var(--white);
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        /* ============ PRELOADER ============ */
        .preloader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--dark);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            transition: opacity 0.5s, visibility 0.5s;
        }

        .preloader.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .preloader-spinner {
            width: 50px;
            height: 50px;
            border: 4px solid rgba(108, 99, 255, 0.2);
            border-top-color: var(--primary);
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* ============ CURSOR ============ */
        .custom-cursor {
            width: 20px;
            height: 20px;
            border: 2px solid var(--primary);
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            transition: transform 0.15s ease, background 0.15s ease;
            transform: translate(-50%, -50%);
        }

        .custom-cursor.hovering {
            transform: translate(-50%, -50%) scale(1.8);
            background: rgba(108, 99, 255, 0.1);
        }

        /* ============ NAVBAR ============ */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 60px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            z-index: 1000;
            transition: var(--transition);
            background: transparent;
        }

        .navbar.scrolled {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            padding: 15px 60px;
            box-shadow: 0 2px 30px rgba(0, 0, 0, 0.08);
        }

        .nav-logo {
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--white);
            transition: var(--transition);
            letter-spacing: -0.5px;
        }

        .navbar.scrolled .nav-logo {
            color: var(--dark);
        }

        .nav-logo span {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 35px;
            align-items: center;
        }

        .nav-links a {
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.95rem;
            font-weight: 500;
            position: relative;
            transition: var(--transition);
        }

        .navbar.scrolled .nav-links a {
            color: var(--text);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gradient);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-cta {
            padding: 10px 28px !important;
            background: var(--gradient) !important;
            color: var(--white) !important;
            border-radius: 50px;
            font-weight: 600 !important;
            transition: var(--transition);
            box-shadow: 0 4px 20px rgba(108, 99, 255, 0.3);
        }

        .nav-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(108, 99, 255, 0.4) !important;
        }

        .nav-cta::after {
            display: none !important;
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-toggle span {
            width: 28px;
            height: 3px;
            background: var(--white);
            border-radius: 3px;
            transition: var(--transition);
        }

        .navbar.scrolled .menu-toggle span {
            background: var(--dark);
        }

        .menu-toggle.active span:nth-child(1) {
            transform: rotate(45deg) translate(5px, 6px);
        }

        .menu-toggle.active span:nth-child(2) {
            opacity: 0;
        }

        .menu-toggle.active span:nth-child(3) {
            transform: rotate(-45deg) translate(5px, -6px);
        }

        /* ============ HERO ============ */
        .hero {
            min-height: 100vh;
            background: var(--dark);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            padding: 0 60px;
        }

        .hero-bg-shapes {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .hero-bg-shapes .shape {
            position: absolute;
            border-radius: 50%;
            opacity: 0.08;
        }

        .hero-bg-shapes .shape:nth-child(1) {
            width: 600px;
            height: 600px;
            background: var(--primary);
            top: -200px;
            right: -100px;
            animation: float1 8s ease-in-out infinite;
        }

        .hero-bg-shapes .shape:nth-child(2) {
            width: 400px;
            height: 400px;
            background: var(--secondary);
            bottom: -150px;
            left: -100px;
            animation: float2 10s ease-in-out infinite;
        }

        .hero-bg-shapes .shape:nth-child(3) {
            width: 200px;
            height: 200px;
            background: var(--primary);
            top: 50%;
            left: 50%;
            animation: float3 6s ease-in-out infinite;
        }

        @keyframes float1 {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(-40px, 40px) rotate(20deg); }
        }

        @keyframes float2 {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(40px, -30px) rotate(-15deg); }
        }

        @keyframes float3 {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(-30px, 30px) scale(1.2); }
        }

        .hero-particles {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: var(--primary);
            border-radius: 50%;
            opacity: 0.3;
            animation: particleFloat 15s linear infinite;
        }

        @keyframes particleFloat {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 0.3; }
            90% { opacity: 0.3; }
            100% { transform: translateY(-100vh) rotate(720deg); opacity: 0; }
        }

        .hero-content {
            text-align: center;
            position: relative;
            z-index: 2;
            max-width: 900px;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 8px 20px;
            background: rgba(108, 99, 255, 0.15);
            border: 1px solid rgba(108, 99, 255, 0.3);
            border-radius: 50px;
            color: var(--primary);
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 30px;
            animation: fadeInUp 0.8s ease;
        }

        .hero-badge .dot {
            width: 8px;
            height: 8px;
            background: #4CAF50;
            border-radius: 50%;
            animation: pulse 1.5s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.5; transform: scale(1.3); }
        }

        .hero h1 {
            font-size: 4.5rem;
            color: var(--white);
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 25px;
            animation: fadeInUp 0.8s ease 0.2s both;
            letter-spacing: -2px;
        }

        .hero h1 .highlight {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.6);
            max-width: 600px;
            margin: 0 auto 40px;
            line-height: 1.7;
            animation: fadeInUp 0.8s ease 0.4s both;
        }

        .hero-btns {
            display: flex;
            gap: 20px;
            justify-content: center;
            animation: fadeInUp 0.8s ease 0.6s both;
            flex-wrap: wrap;
        }

        .btn-primary {
            padding: 16px 40px;
            background: var(--gradient);
            color: var(--white);
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 20px rgba(108, 99, 255, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 40px rgba(108, 99, 255, 0.4);
        }

        .btn-secondary {
            padding: 16px 40px;
            background: transparent;
            color: var(--white);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-secondary:hover {
            border-color: var(--primary);
            color: var(--primary);
            transform: translateY(-3px);
        }

        .hero-stats {
            display: flex;
            gap: 60px;
            justify-content: center;
            margin-top: 80px;
            animation: fadeInUp 0.8s ease 0.8s both;
        }

        .hero-stat {
            text-align: center;
        }

        .hero-stat h3 {
            font-size: 2.5rem;
            color: var(--white);
            font-weight: 800;
        }

        .hero-stat h3 span {
            color: var(--primary);
        }

        .hero-stat p {
            font-size: 0.85rem;
            color: rgba(255, 255, 255, 0.4);
            margin: 5px auto 0;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* ============ MARQUEE ============ */
        .marquee-section {
            padding: 30px 0;
            background: var(--darker);
            overflow: hidden;
            border-top: 1px solid rgba(108, 99, 255, 0.1);
            border-bottom: 1px solid rgba(108, 99, 255, 0.1);
        }

        .marquee-track {
            display: flex;
            animation: marquee 20s linear infinite;
            width: max-content;
        }

        .marquee-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 0 40px;
            color: rgba(255, 255, 255, 0.3);
            font-size: 1.1rem;
            font-weight: 600;
            white-space: nowrap;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .marquee-item .separator {
            width: 8px;
            height: 8px;
            background: var(--primary);
            border-radius: 50%;
            opacity: 0.5;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* ============ SERVICES ============ */
        .services {
            padding: 120px 60px;
            background: var(--white);
        }

        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-tag {
            display: inline-block;
            padding: 6px 18px;
            background: rgba(108, 99, 255, 0.08);
            color: var(--primary);
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 15px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .section-header h2 {
            font-size: 3rem;
            color: var(--dark);
            font-weight: 800;
            letter-spacing: -1px;
            margin-bottom: 15px;
        }

        .section-header p {
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 550px;
            margin: 0 auto;
            line-height: 1.7;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: var(--white);
            border: 1px solid #eee;
            border-radius: 20px;
            padding: 45px 35px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--gradient);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.4s ease;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
            border-color: transparent;
        }

        .service-icon {
            width: 70px;
            height: 70px;
            background: rgba(108, 99, 255, 0.08);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin-bottom: 25px;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            background: var(--gradient);
            transform: rotate(-5deg) scale(1.05);
        }

        .service-card h3 {
            font-size: 1.3rem;
            color: var(--dark);
            font-weight: 700;
            margin-bottom: 12px;
        }

        .service-card p {
            color: var(--text-light);
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .service-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin-top: 20px;
            color: var(--primary);
            font-weight: 600;
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .service-link:hover {
            gap: 12px;
        }

        /* ============ PORTFOLIO ============ */
        .portfolio {
            padding: 120px 60px;
            background: var(--light);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .portfolio-card {
            border-radius: 20px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            aspect-ratio: 4/3;
            background: var(--dark);
            transition: var(--transition);
        }

        .portfolio-card:first-child {
            grid-column: span 2;
            grid-row: span 2;
            aspect-ratio: auto;
        }

        .portfolio-card-bg {
            width: 100%;
            height: 100%;
            position: absolute;
            transition: var(--transition);
        }

        .portfolio-card:nth-child(1) .portfolio-card-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .portfolio-card:nth-child(2) .portfolio-card-bg {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }

        .portfolio-card:nth-child(3) .portfolio-card-bg {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        .portfolio-card:nth-child(4) .portfolio-card-bg {
            background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
        }

        .portfolio-card:nth-child(5) .portfolio-card-bg {
            background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
        }

        .portfolio-card:hover .portfolio-card-bg {
            transform: scale(1.05);
        }

        /* NEW: Mockup inside portfolio cards */
        .portfolio-mockup {
            position: absolute;
            z-index: 2;
            transition: var(--transition);
        }

        .portfolio-card:hover .portfolio-mockup {
            transform: translateY(-10px) scale(1.02);
        }

        /* Browser Mockup */
        .browser-mockup {
            background: #1e1e2e;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            width: 85%;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }

        .portfolio-card:hover .browser-mockup {
            transform: translate(-50%, -50%) translateY(-10px) scale(1.02);
        }

        .browser-bar {
            background: #2d2d3f;
            padding: 10px 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .browser-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
        }

        .browser-dot.red { background: #ff5f57; }
        .browser-dot.yellow { background: #ffbd2e; }
        .browser-dot.green { background: #28c840; }

        .browser-url {
            background: #1e1e2e;
            border-radius: 5px;
            padding: 5px 12px;
            margin-left: 10px;
            flex: 1;
            font-size: 0.7rem;
            color: rgba(255,255,255,0.4);
            font-family: monospace;
        }

        .browser-content {
            padding: 0;
        }

        /* Website mockup layouts */
        .mockup-site {
            background: #ffffff;
        }

        .mockup-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 20px;
            border-bottom: 1px solid #eee;
        }

        .mockup-nav-logo {
            font-weight: 800;
            font-size: 0.85rem;
            color: #333;
        }

        .mockup-nav-links {
            display: flex;
            gap: 10px;
        }

        .mockup-nav-link {
            width: 35px;
            height: 6px;
            background: #e0e0e0;
            border-radius: 3px;
        }

        .mockup-hero-section {
            padding: 25px 20px;
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .mockup-hero-text {
            flex: 1;
        }

        .mockup-hero-text .line {
            height: 8px;
            background: #333;
            border-radius: 4px;
            margin-bottom: 6px;
        }

        .mockup-hero-text .line:nth-child(1) { width: 80%; }
        .mockup-hero-text .line:nth-child(2) { width: 60%; }
        .mockup-hero-text .line.subtitle {
            height: 5px;
            background: #ccc;
            margin-top: 10px;
            width: 90%;
        }

        .mockup-hero-text .line.subtitle:nth-child(4) { width: 70%; }

        .mockup-hero-btn {
            width: 70px;
            height: 22px;
            border-radius: 12px;
            margin-top: 12px;
        }

        .mockup-hero-img {
            width: 100px;
            height: 80px;
            border-radius: 10px;
            flex-shrink: 0;
        }

        .mockup-cards-row {
            display: flex;
            gap: 8px;
            padding: 0 20px 20px;
        }

        .mockup-card {
            flex: 1;
            border-radius: 8px;
            padding: 10px;
            border: 1px solid #eee;
        }

        .mockup-card-icon {
            width: 20px;
            height: 20px;
            border-radius: 6px;
            margin-bottom: 6px;
        }

        .mockup-card .line {
            height: 4px;
            border-radius: 2px;
            margin-bottom: 4px;
        }

        .mockup-card .line:nth-child(2) { width: 80%; }
        .mockup-card .line:nth-child(3) { width: 60%; background: #e0e0e0; }

        /* Phone Mockup */
        .phone-mockup {
            width: 140px;
            background: #1a1a2e;
            border-radius: 20px;
            padding: 8px;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }

        .portfolio-card:hover .phone-mockup {
            transform: translate(-50%, -50%) translateY(-10px) scale(1.02);
        }

        .phone-notch {
            width: 50px;
            height: 5px;
            background: #2d2d3f;
            border-radius: 3px;
            margin: 5px auto 8px;
        }

        .phone-screen {
            background: #fff;
            border-radius: 14px;
            overflow: hidden;
        }

        .phone-header {
            padding: 12px;
            color: white;
            text-align: center;
        }

        .phone-header-title {
            font-size: 0.7rem;
            font-weight: 700;
        }

        .phone-header-sub {
            font-size: 0.5rem;
            opacity: 0.7;
            margin-top: 2px;
        }

        .phone-items {
            padding: 8px;
        }

        .phone-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 6px 8px;
            border-radius: 8px;
            margin-bottom: 4px;
            background: #f8f8f8;
        }

        .phone-item-img {
            width: 24px;
            height: 24px;
            border-radius: 6px;
            flex-shrink: 0;
        }

        .phone-item-lines {
            flex: 1;
        }

        .phone-item-lines .line {
            height: 4px;
            border-radius: 2px;
            margin-bottom: 3px;
        }

        .phone-item-lines .line:first-child {
            width: 70%;
            background: #333;
        }

        .phone-item-lines .line:last-child {
            width: 50%;
            background: #ddd;
        }

        .phone-item-price {
            font-size: 0.55rem;
            font-weight: 700;
            white-space: nowrap;
        }

        .phone-bottom-nav {
            display: flex;
            justify-content: space-around;
            padding: 8px;
            border-top: 1px solid #eee;
        }

        .phone-bottom-icon {
            width: 16px;
            height: 16px;
            border-radius: 4px;
            background: #e0e0e0;
        }

        .phone-bottom-icon.active {
            background: var(--primary);
        }

        /* Dashboard Mockup */
        .dashboard-mockup {
            background: #1e1e2e;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            width: 85%;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }

        .portfolio-card:hover .dashboard-mockup {
            transform: translate(-50%, -50%) translateY(-10px) scale(1.02);
        }

        .dash-body {
            display: flex;
            background: #f5f5f5;
        }

        .dash-sidebar {
            width: 50px;
            background: #2d2d3f;
            padding: 10px 8px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        .dash-sidebar-icon {
            width: 24px;
            height: 24px;
            border-radius: 6px;
            background: rgba(255,255,255,0.1);
        }

        .dash-sidebar-icon.active {
            background: var(--primary);
        }

        .dash-main {
            flex: 1;
            padding: 12px;
        }

        .dash-top-cards {
            display: flex;
            gap: 6px;
            margin-bottom: 8px;
        }

        .dash-stat-card {
            flex: 1;
            background: white;
            border-radius: 8px;
            padding: 8px;
        }

        .dash-stat-label {
            height: 4px;
            width: 50%;
            background: #ddd;
            border-radius: 2px;
            margin-bottom: 6px;
        }

        .dash-stat-value {
            height: 8px;
            width: 40%;
            background: #333;
            border-radius: 4px;
        }

        .dash-chart {
            background: white;
            border-radius: 8px;
            padding: 10px;
            height: 70px;
            display: flex;
            align-items: flex-end;
            gap: 4px;
        }

        .dash-chart-bar {
            flex: 1;
            border-radius: 3px 3px 0 0;
            min-height: 8px;
        }

        .portfolio-card-content {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 35px;
            background: linear-gradient(transparent, rgba(0,0,0,0.8));
            transform: translateY(0);
            opacity: 1;
            transition: var(--transition);
            z-index: 5;
        }

        .portfolio-card:hover .portfolio-card-content {
            transform: translateY(0);
            opacity: 1;
        }

        .portfolio-card-content span {
            font-size: 0.75rem;
            color: var(--primary);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 2px;
            background: rgba(108, 99, 255, 0.15);
            padding: 4px 12px;
            border-radius: 50px;
        }

        .portfolio-card-content h3 {
            font-size: 1.3rem;
            color: var(--white);
            font-weight: 700;
            margin-top: 10px;
        }

        .portfolio-card-content p.portfolio-desc {
            font-size: 0.8rem;
            color: rgba(255,255,255,0.6);
            margin-top: 5px;
            line-height: 1.5;
        }

        .portfolio-tech-tags {
            display: flex;
            gap: 6px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .portfolio-tech-tags span {
            font-size: 0.65rem;
            background: rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.7);
            padding: 3px 10px;
            border-radius: 50px;
            letter-spacing: 0;
            text-transform: none;
        }

        /* ============ PROCESS ============ */
        .process {
            padding: 120px 60px;
            background: var(--dark);
        }

        .process .section-header h2 {
            color: var(--white);
        }

        .process .section-header p {
            color: rgba(255, 255, 255, 0.5);
        }

        .process-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .process-grid::before {
            content: '';
            position: absolute;
            top: 55px;
            left: 15%;
            right: 15%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
            opacity: 0.2;
        }

        .process-step {
            text-align: center;
            position: relative;
        }

        .process-number {
            width: 80px;
            height: 80px;
            background: rgba(108, 99, 255, 0.1);
            border: 2px solid rgba(108, 99, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            transition: var(--transition);
        }

        .process-step:hover .process-number {
            background: var(--gradient);
            border-color: transparent;
            color: var(--white);
            transform: scale(1.1);
            box-shadow: 0 10px 40px rgba(108, 99, 255, 0.3);
        }

        .process-step h3 {
            font-size: 1.2rem;
            color: var(--white);
            font-weight: 700;
            margin-bottom: 10px;
        }

        .process-step p {
            color: rgba(255, 255, 255, 0.4);
            font-size: 0.9rem;
            line-height: 1.6;
        }

        /* ============ TESTIMONIALS ============ */
        .testimonials {
            padding: 120px 60px;
            background: var(--white);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .testimonial-card {
            background: var(--white);
            border: 1px solid #eee;
            border-radius: 20px;
            padding: 40px 35px;
            transition: var(--transition);
            position: relative;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
            border-color: transparent;
        }

        .testimonial-stars {
            color: #FFD700;
            font-size: 1.1rem;
            margin-bottom: 20px;
            letter-spacing: 3px;
        }

        .testimonial-card blockquote {
            color: var(--text);
            font-size: 1rem;
            line-height: 1.8;
            font-style: italic;
            margin-bottom: 25px;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .testimonial-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: var(--white);
            font-size: 1.1rem;
        }

        .testimonial-card:nth-child(1) .testimonial-avatar {
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .testimonial-card:nth-child(2) .testimonial-avatar {
            background: linear-gradient(135deg, #f093fb, #f5576c);
        }

        .testimonial-card:nth-child(3) .testimonial-avatar {
            background: linear-gradient(135deg, #4facfe, #00f2fe);
        }

        .testimonial-info h4 {
            font-size: 1rem;
            color: var(--dark);
            font-weight: 700;
        }

        .testimonial-info span {
            font-size: 0.85rem;
            color: var(--text-light);
        }

        /* ============ PRICING ============ */
        .pricing {
            padding: 120px 60px;
            background: var(--light);
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1100px;
            margin: 0 auto;
            align-items: center;
        }

        .pricing-card {
            background: var(--white);
            border: 1px solid #eee;
            border-radius: 24px;
            padding: 45px 35px;
            text-align: center;
            transition: var(--transition);
            position: relative;
        }

        .pricing-card.featured {
            background: var(--dark);
            border-color: var(--primary);
            transform: scale(1.05);
            box-shadow: var(--shadow-hover);
        }

        .pricing-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
        }

        .pricing-card.featured:hover {
            transform: scale(1.05) translateY(-5px);
        }

        .pricing-badge {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            padding: 5px 20px;
            background: var(--gradient);
            color: var(--white);
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .pricing-card h3 {
            font-size: 1.2rem;
            color: var(--dark);
            font-weight: 700;
            margin-bottom: 15px;
        }

        .pricing-card.featured h3 {
            color: var(--white);
        }

        .pricing-price {
            font-size: 3.5rem;
            font-weight: 800;
            color: var(--dark);
            margin-bottom: 5px;
        }

        .pricing-card.featured .pricing-price {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .pricing-price span {
            font-size: 1rem;
            font-weight: 400;
            color: var(--text-light);
        }

        .pricing-card.featured .pricing-price span {
            -webkit-text-fill-color: rgba(255,255,255,0.5);
        }

        .pricing-desc {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-bottom: 30px;
        }

        .pricing-card.featured .pricing-desc {
            color: rgba(255,255,255,0.5);
        }

        .pricing-features {
            text-align: left;
            margin-bottom: 35px;
        }

        .pricing-features li {
            padding: 10px 0;
            color: var(--text);
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 1px solid #f0f0f0;
        }

        .pricing-card.featured .pricing-features li {
            color: rgba(255,255,255,0.7);
            border-color: rgba(255,255,255,0.08);
        }

        .pricing-features li .check {
            color: #4CAF50;
            font-weight: bold;
        }

        .pricing-btn {
            width: 100%;
            padding: 16px;
            border-radius: 50px;
            border: 2px solid #eee;
            background: transparent;
            color: var(--dark);
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .pricing-card.featured .pricing-btn {
            background: var(--gradient);
            border-color: transparent;
            color: var(--white);
            box-shadow: 0 4px 20px rgba(108, 99, 255, 0.3);
        }

        .pricing-btn:hover {
            border-color: var(--primary);
            color: var(--primary);
            transform: translateY(-2px);
        }

        .pricing-card.featured .pricing-btn:hover {
            box-shadow: 0 10px 40px rgba(108, 99, 255, 0.4);
        }

        /* ============ CTA SECTION ============ */
        .cta-section {
            padding: 120px 60px;
            background: var(--dark);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta-section::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: var(--primary);
            border-radius: 50%;
            top: -250px;
            right: -100px;
            opacity: 0.05;
        }

        .cta-section::after {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            background: var(--secondary);
            border-radius: 50%;
            bottom: -150px;
            left: -50px;
            opacity: 0.05;
        }

        .cta-section h2 {
            font-size: 3.5rem;
            color: var(--white);
            font-weight: 800;
            letter-spacing: -1px;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        .cta-section h2 .highlight {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .cta-section p {
            color: rgba(255,255,255,0.5);
            font-size: 1.1rem;
            max-width: 550px;
            margin: 0 auto 40px;
            line-height: 1.7;
            position: relative;
            z-index: 2;
        }

        .cta-section .btn-primary {
            position: relative;
            z-index: 2;
        }

        /* ============ FOOTER ============ */
        .footer {
            background: var(--darker);
            padding: 80px 60px 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 50px;
            max-width: 1200px;
            margin: 0 auto;
            padding-bottom: 50px;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .footer-brand .nav-logo {
            margin-bottom: 15px;
            display: block;
        }

        .footer-brand p {
            color: rgba(255,255,255,0.4);
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 25px;
        }

        .footer-social {
            display: flex;
            gap: 12px;
        }

        .footer-social a {
            width: 42px;
            height: 42px;
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: rgba(255,255,255,0.5);
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .footer-social a:hover {
            background: var(--primary);
            border-color: var(--primary);
            color: var(--white);
            transform: translateY(-3px);
        }

        .footer-col h4 {
            color: var(--white);
            font-size: 1rem;
            font-weight: 700;
            margin-bottom: 20px;
        }

        .footer-col ul li {
            margin-bottom: 12px;
        }

        .footer-col ul li a {
            color: rgba(255,255,255,0.4);
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .footer-col ul li a:hover {
            color: var(--primary);
            padding-left: 5px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            color: rgba(255,255,255,0.3);
            font-size: 0.85rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* ============ SCROLL ANIMATIONS ============ */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* ============ SCROLL TO TOP ============ */
        .scroll-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--gradient);
            border: none;
            border-radius: 50%;
            color: var(--white);
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            visibility: hidden;
            transform: translateY(20px);
            transition: var(--transition);
            box-shadow: 0 4px 20px rgba(108, 99, 255, 0.3);
            z-index: 999;
        }

        .scroll-top.visible {
            opacity: 1;
            visibility: visible;
            transform: translateY(0);
        }

        .scroll-top:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(108, 99, 255, 0.4);
        }

        /* ============ RESPONSIVE ============ */
        @media (max-width: 1024px) {
            .services-grid,
            .portfolio-grid,
            .testimonials-grid,
            .pricing-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .process-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 40px;
            }

            .process-grid::before {
                display: none;
            }

            .portfolio-card:first-child {
                grid-column: span 2;
                grid-row: span 1;
            }

            .hero h1 {
                font-size: 3.5rem;
            }

            .footer-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .pricing-card.featured {
                transform: scale(1);
            }

            .pricing-card.featured:hover {
                transform: translateY(-5px);
            }
        }

        @media (max-width: 768px) {
            .navbar {
                padding: 15px 25px;
            }

            .navbar.scrolled {
                padding: 12px 25px;
            }

            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: 280px;
                height: 100vh;
                background: var(--dark);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                gap: 25px;
                transition: right 0.4s ease;
            }

            .nav-links.open {
                right: 0;
            }

            .nav-links a {
                color: rgba(255,255,255,0.8) !important;
                font-size: 1.1rem;
            }

            .menu-toggle {
                display: flex;
            }

            .hero {
                padding: 0 25px;
            }

            .hero h1 {
                font-size: 2.5rem;
                letter-spacing: -1px;
            }

            .hero p {
                font-size: 1rem;
            }

            .hero-stats {
                gap: 30px;
                flex-wrap: wrap;
            }

            .hero-stat h3 {
                font-size: 2rem;
            }

            .services, .portfolio, .process,
            .testimonials, .pricing, .cta-section, .footer {
                padding: 80px 25px;
            }

            .services-grid,
            .portfolio-grid,
            .testimonials-grid,
            .pricing-grid,
            .process-grid {
                grid-template-columns: 1fr;
            }

            .portfolio-card:first-child {
                grid-column: span 1;
            }

            .section-header h2 {
                font-size: 2.2rem;
            }

            .cta-section h2 {
                font-size: 2.5rem;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .hero-btns {
                flex-direction: column;
                align-items: center;
            }

            .custom-cursor {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- Preloader -->
    <div class="preloader">
        <div class="preloader-spinner"></div>
    </div>

    <!-- Custom Cursor -->
    <div class="custom-cursor"></div>

    <!-- Scroll to Top -->
    <button class="scroll-top" id="scrollTop">↑</button>

    <!-- Navbar -->
    <nav class="navbar" id="navbar">
        <a href="#" class="nav-logo">Elegance<span>.</span></a>
        <ul class="nav-links" id="navLinks">
            <li><a href="#services">Services</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#process">Process</a></li>
            <li><a href="#testimonials">Reviews</a></li>
            <li><a href="#pricing">Pricing</a></li>
            <li><a href="#contact" class="nav-cta">Get Started</a></li>
        </ul>
        <div class="menu-toggle" id="menuToggle">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </nav>

    <!-- Hero -->
    <section class="hero" id="hero">
        <div class="hero-bg-shapes">
            <div class="shape"></div>
            <div class="shape"></div>
            <div class="shape"></div>
        </div>
        <div class="hero-particles" id="heroParticles"></div>
        <div class="hero-content">
            <div class="hero-badge">
                <span class="dot"></span>
                Available for new projects
            </div>
            <h1>We Build <span class="highlight">Digital Experiences</span> That Matter</h1>
            <p>A creative digital agency specializing in web design, development, and brand strategy that drives results and inspires users.</p>
            <div class="hero-btns">
                <a href="#portfolio" class="btn-primary">View Our Work →</a>
                <a href="#contact" class="btn-secondary">▶ Watch Showreel</a>
            </div>
            <div class="hero-stats">
                <div class="hero-stat">
                    <h3>150<span>+</span></h3>
                    <p>Projects Delivered</p>
                </div>
                <div class="hero-stat">
                    <h3>98<span>%</span></h3>
                    <p>Client Satisfaction</p>
                </div>
                <div class="hero-stat">
                    <h3>12<span>+</span></h3>
                    <p>Years Experience</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Marquee -->
    <div class="marquee-section">
        <div class="marquee-track">
            <div class="marquee-item">WEB DESIGN <span class="separator"></span></div>
            <div class="marquee-item">DEVELOPMENT <span class="separator"></span></div>
            <div class="marquee-item">BRANDING <span class="separator"></span></div>
            <div class="marquee-item">UI/UX <span class="separator"></span></div>
            <div class="marquee-item">E-COMMERCE <span class="separator"></span></div>
            <div class="marquee-item">SEO <span class="separator"></span></div>
            <div class="marquee-item">WORDPRESS <span class="separator"></span></div>
            <div class="marquee-item">REACT <span class="separator"></span></div>
            <div class="marquee-item">WEB DESIGN <span class="separator"></span></div>
            <div class="marquee-item">DEVELOPMENT <span class="separator"></span></div>
            <div class="marquee-item">BRANDING <span class="separator"></span></div>
            <div class="marquee-item">UI/UX <span class="separator"></span></div>
            <div class="marquee-item">E-COMMERCE <span class="separator"></span></div>
            <div class="marquee-item">SEO <span class="separator"></span></div>
            <div class="marquee-item">WORDPRESS <span class="separator"></span></div>
            <div class="marquee-item">REACT <span class="separator"></span></div>
        </div>
    </div>

    <!-- Services -->
    <section class="services" id="services">
        <div class="section-header reveal">
            <span class="section-tag">What We Do</span>
            <h2>Our Core Services</h2>
            <p>We deliver comprehensive digital solutions tailored to your business needs and goals.</p>
        </div>
        <div class="services-grid">
            <div class="service-card reveal">
                <div class="service-icon">🎨</div>
                <h3>Web Design</h3>
                <p>Stunning, user-centered designs that captivate your audience and reflect your brand's identity beautifully.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">⚡</div>
                <h3>Web Development</h3>
                <p>Clean, performant code built with modern technologies. Fast, secure, and scalable web applications.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">📱</div>
                <h3>Responsive Design</h3>
                <p>Pixel-perfect experiences across all devices. Your site will look amazing on mobile, tablet, and desktop.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🛒</div>
                <h3>E-Commerce</h3>
                <p>Powerful online stores that convert visitors into customers with seamless shopping experiences.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🔍</div>
                <h3>SEO Optimization</h3>
                <p>Data-driven SEO strategies that boost your visibility and drive organic traffic to your website.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🚀</div>
                <h3>Performance</h3>
                <p>Lightning-fast load times and optimized performance that keeps users engaged and improves rankings.</p>
                <a href="#" class="service-link">Learn More →</a>
            </div>
        </div>
    </section>

    <!-- Portfolio -->
    <section class="portfolio" id="portfolio">
        <div class="section-header reveal">
            <span class="section-tag">Our Work</span>
            <h2>Featured Projects</h2>
            <p>A showcase of our finest work across various industries and platforms.</p>
        </div>
        <div class="portfolio-grid">

            <!-- Project 1: SaaS Platform (Large Card with Browser Mockup) -->
            <div class="portfolio-card reveal">
                <div class="portfolio-card-bg"></div>
                <div class="portfolio-mockup browser-mockup">
                    <div class="browser-bar">
                        <div class="browser-dot red"></div>
                        <div class="browser-dot yellow"></div>
                        <div class="browser-dot green"></div>
                        <div class="browser-url">novatech.io/dashboard</div>
                    </div>
                    <div class="browser-content">
                        <div class="mockup-site">
                            <div class="mockup-nav">
                                <div class="mockup-nav-logo">NovaTech</div>
                                <div class="mockup-nav-links">
                                    <div class="mockup-nav-link"></div>
                                    <div class="mockup-nav-link"></div>
                                    <div class="mockup-nav-link"></div>
                                </div>
                            </div>
                            <div class="mockup-hero-section">
                                <div class="mockup-hero-text">
                                    <div class="line" style="background: #667eea;"></div>
                                    <div class="line" style="background: #764ba2;"></div>
                                    <div class="line subtitle"></div>
                                    <div class="line subtitle"></div>
                                    <div class="mockup-hero-btn" style="background: linear-gradient(135deg, #667eea, #764ba2);"></div>
                                </div>
                                <div class="mockup-hero-img" style="background: linear-gradient(135deg, #667eea, #764ba2);"></div>
                            </div>
                            <div class="mockup-cards-row">
                                <div class="mockup-card">
                                    <div class="mockup-card-icon" style="background: #667eea;"></div>
                                    <div class="line" style="background: #333; width: 80%;"></div>
                                    <div class="line" style="background: #e0e0e0; width: 60%;"></div>
                                </div>
                                <div class="mockup-card">
                                    <div class="mockup-card-icon" style="background: #764ba2;"></div>
                                    <div class="line" style="background: #333; width: 70%;"></div>
                                    <div class="line" style="background: #e0e0e0; width: 50%;"></div>
                                </div>
                                <div class="mockup-card">
                                    <div class="mockup-card-icon" style="background: #f093fb;"></div>
                                    <div class="line" style="background: #333; width: 75%;"></div>
                                    <div class="line" style="background: #e0e0e0; width: 55%;"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-card-content">
                    <span>Web Application</span>
                    <h3>NovaTech SaaS Platform</h3>
                    <p class="portfolio-desc">Full-stack SaaS platform with dashboard analytics and user management</p>
                    <div class="portfolio-tech-tags">
                        <span>React</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                    </div>
                </div>
            </div>

            <!-- Project 2: E-Commerce (Phone Mockup) -->
            <div class="portfolio-card reveal">
                <div class="portfolio-card-bg"></div>
                <div class="portfolio-mockup phone-mockup">
                    <div class="phone-notch"></div>
                    <div class="phone-screen">
                        <div class="phone-header" style="background: linear-gradient(135deg, #f093fb, #f5576c);">
                            <div class="phone-header-title">LUXE STORE</div>
                            <div class="phone-header-sub">Premium Fashion</div>
                        </div>
                        <div class="phone-items">
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #f093fb, #f5576c);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #f5576c;">$89</div>
                            </div>
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #fc5c7d, #6a82fb);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #f5576c;">$129</div>
                            </div>
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #f5af19, #f12711);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #f5576c;">$199</div>
                            </div>
                        </div>
                        <div class="phone-bottom-nav">
                            <div class="phone-bottom-icon active"></div>
                            <div class="phone-bottom-icon"></div>
                            <div class="phone-bottom-icon"></div>
                            <div class="phone-bottom-icon"></div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-card-content">
                    <span>E-Commerce</span>
                    <h3>Luxe Fashion Store</h3>
                    <p class="portfolio-desc">Mobile-first luxury fashion e-commerce</p>
                    <div class="portfolio-tech-tags">
                        <span>Shopify</span>
                        <span>Liquid</span>
                    </div>
                </div>
            </div>

            <!-- Project 3: Healthcare (Dashboard Mockup) -->
            <div class="portfolio-card reveal">
                <div class="portfolio-card-bg"></div>
                <div class="portfolio-mockup dashboard-mockup">
                    <div class="browser-bar">
                        <div class="browser-dot red"></div>
                        <div class="browser-dot yellow"></div>
                        <div class="browser-dot green"></div>
                        <div class="browser-url">medcare.health/admin</div>
                    </div>
                    <div class="dash-body">
                        <div class="dash-sidebar">
                            <div class="dash-sidebar-icon active"></div>
                            <div class="dash-sidebar-icon"></div>
                            <div class="dash-sidebar-icon"></div>
                            <div class="dash-sidebar-icon"></div>
                        </div>
                        <div class="dash-main">
                            <div class="dash-top-cards">
                                <div class="dash-stat-card">
                                    <div class="dash-stat-label"></div>
                                    <div class="dash-stat-value" style="background: #4facfe;"></div>
                                </div>
                                <div class="dash-stat-card">
                                    <div class="dash-stat-label"></div>
                                    <div class="dash-stat-value" style="background: #00f2fe;"></div>
                                </div>
                                <div class="dash-stat-card">
                                    <div class="dash-stat-label"></div>
                                    <div class="dash-stat-value" style="background: #43e97b;"></div>
                                </div>
                            </div>
                            <div class="dash-chart">
                                <div class="dash-chart-bar" style="height: 30%; background: #4facfe;"></div>
                                <div class="dash-chart-bar" style="height: 55%; background: #4facfe;"></div>
                                <div class="dash-chart-bar" style="height: 40%; background: #00f2fe;"></div>
                                <div class="dash-chart-bar" style="height: 75%; background: #4facfe;"></div>
                                <div class="dash-chart-bar" style="height: 60%; background: #00f2fe;"></div>
                                <div class="dash-chart-bar" style="height: 90%; background: #4facfe;"></div>
                                <div class="dash-chart-bar" style="height: 50%; background: #00f2fe;"></div>
                                <div class="dash-chart-bar" style="height: 70%; background: #4facfe;"></div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-card-content">
                    <span>Healthcare</span>
                    <h3>MedCare Portal</h3>
                    <p class="portfolio-desc">Patient management dashboard</p>
                    <div class="portfolio-tech-tags">
                        <span>Vue.js</span>
                        <span>Python</span>
                    </div>
                </div>
            </div>

            <!-- Project 4: Restaurant (Browser Mockup) -->
            <div class="portfolio-card reveal">
                <div class="portfolio-card-bg"></div>
                <div class="portfolio-mockup browser-mockup">
                    <div class="browser-bar">
                        <div class="browser-dot red"></div>
                        <div class="browser-dot yellow"></div>
                        <div class="browser-dot green"></div>
                        <div class="browser-url">saveur-dining.com</div>
                    </div>
                    <div class="browser-content">
                        <div class="mockup-site">
                            <div class="mockup-nav">
                                <div class="mockup-nav-logo">Saveur</div>
                                <div class="mockup-nav-links">
                                    <div class="mockup-nav-link"></div>
                                    <div class="mockup-nav-link"></div>
                                </div>
                            </div>
                            <div style="height: 60px; background: linear-gradient(135deg, #43e97b, #38f9d7); display: flex; align-items: center; justify-content: center;">
                                <div style="width: 60%; height: 8px; background: rgba(255,255,255,0.8); border-radius: 4px;"></div>
                            </div>
                            <div class="mockup-cards-row" style="padding-top: 10px;">
                                <div class="mockup-card">
                                    <div class="mockup-card-icon" style="background: #43e97b;"></div>
                                    <div class="line" style="background: #333; width: 70%;"></div>
                                    <div class="line" style="background: #e0e0e0; width: 50%;"></div>
                                </div>
                                <div class="mockup-card">
                                    <div class="mockup-card-icon" style="background: #38f9d7;"></div>
                                    <div class="line" style="background: #333; width: 65%;"></div>
                                    <div class="line" style="background: #e0e0e0; width: 45%;"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-card-content">
                    <span>Restaurant</span>
                    <h3>Saveur Fine Dining</h3>
                    <p class="portfolio-desc">Elegant restaurant with online reservations</p>
                    <div class="portfolio-tech-tags">
                        <span>WordPress</span>
                        <span>PHP</span>
                    </div>
                </div>
            </div>

            <!-- Project 5: Education (Phone Mockup) -->
            <div class="portfolio-card reveal">
                <div class="portfolio-card-bg"></div>
                <div class="portfolio-mockup phone-mockup">
                    <div class="phone-notch"></div>
                    <div class="phone-screen">
                        <div class="phone-header" style="background: linear-gradient(135deg, #fa709a, #fee140);">
                            <div class="phone-header-title">LearnHub</div>
                            <div class="phone-header-sub">Online Academy</div>
                        </div>
                        <div class="phone-items">
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #fa709a, #fee140);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #fa709a;">4.9★</div>
                            </div>
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #f7971e, #ffd200);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #fa709a;">4.8★</div>
                            </div>
                            <div class="phone-item">
                                <div class="phone-item-img" style="background: linear-gradient(135deg, #e44d26, #f16529);"></div>
                                <div class="phone-item-lines">
                                    <div class="line"></div>
                                    <div class="line"></div>
                                </div>
                                <div class="phone-item-price" style="color: #fa709a;">5.0★</div>
                            </div>
                        </div>
                        <div class="phone-bottom-nav">
                            <div class="phone-bottom-icon"></div>
                            <div class="phone-bottom-icon active" style="background: #fa709a;"></div>
                            <div class="phone-bottom-icon"></div>
                            <div class="phone-bottom-icon"></div>
                        </div>
                    </div>
                </div>
                <div class="portfolio-card-content">
                    <span>Education</span>
                    <h3>LearnHub Academy</h3>
                    <p class="portfolio-desc">Online learning platform with courses</p>
                    <div class="portfolio-tech-tags">
                        <span>Next.js</span>
                        <span>Stripe</span>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- Process -->
    <section class="process" id="process">
        <div class="section-header reveal">
            <span class="section-tag">How We Work</span>
            <h2>Our Proven Process</h2>
            <p>A streamlined approach that delivers exceptional results every time.</p>
        </div>
        <div class="process-grid">
            <div class="process-step reveal">
                <div class="process-number">01</div>
                <h3>Discovery</h3>
                <p>We dive deep into your business goals, target audience, and competitors to form a solid strategy.</p>
            </div>
            <div class="process-step reveal">
                <div class="process-number">02</div>
                <h3>Design</h3>
                <p>Our designers create stunning mockups and prototypes that bring your vision to life.</p>
            </div>
            <div class="process-step reveal">
                <div class="process-number">03</div>
                <h3>Develop</h3>
                <p>We build with clean, efficient code using the latest technologies for performance and security.</p>
            </div>
            <div class="process-step reveal">
                <div class="process-number">04</div>
                <h3>Launch</h3>
                <p>Rigorous testing, deployment, and ongoing support to ensure everything runs flawlessly.</p>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonials">
        <div class="section-header reveal">
            <span class="section-tag">Client Love</span>
            <h2>What They Say</h2>
            <p>Don't just take our word for it — hear from our happy clients.</p>
        </div>
        <div class="testimonials-grid">
            <div class="testimonial-card reveal">
                <div class="testimonial-stars">★★★★★</div>
                <blockquote>"Absolutely phenomenal work! They transformed our outdated website into a modern masterpiece. Our conversion rate increased by 240% within the first month."</blockquote>
                <div class="testimonial-author">
                    <div class="testimonial-avatar">S</div>
                    <div class="testimonial-info">
                        <h4>Sarah Mitchell</h4>
                        <span>CEO, NovaTech</span>
                    </div>
                </div>
            </div>
            <div class="testimonial-card reveal">
                <div class="testimonial-stars">★★★★★</div>
                <blockquote>"The team's attention to detail is remarkable. Every pixel was perfect, and the development was flawless. Best investment we've made for our brand."</blockquote>
                <div class="testimonial-author">
                    <div class="testimonial-avatar">J</div>
                    <div class="testimonial-info">
                        <h4>James Rodriguez</h4>
                        <span>Founder, Luxe Fashion</span>
                    </div>
                </div>
            </div>
            <div class="testimonial-card reveal">
                <div class="testimonial-stars">★★★★★</div>
                <blockquote>"Professional, creative, and incredibly responsive. They delivered our e-commerce platform ahead of schedule and it exceeded all expectations."</blockquote>
                <div class="testimonial-author">
                    <div class="testimonial-avatar">E</div>
                    <div class="testimonial-info">
                        <h4>Emily Chen</h4>
                        <span>Director, MedCare</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing -->
    <section class="pricing" id="pricing">
        <div class="section-header reveal">
            <span class="section-tag">Pricing</span>
            <h2>Simple & Transparent</h2>
            <p>Choose the plan that fits your needs. No hidden fees, ever.</p>
        </div>
        <div class="pricing-grid">
            <div class="pricing-card reveal">
                <h3>Starter</h3>
                <div class="pricing-price">$499 <span>/ project</span></div>
                <p class="pricing-desc">Perfect for small businesses</p>
                <ul class="pricing-features">
                    <li><span class="check">✓</span> Up to 5 Pages</li>
                    <li><span class="check">✓</span> Responsive Design</li>
                    <li><span class="check">✓</span> Basic SEO Setup</li>
                    <li><span class="check">✓</span> Contact Form</li>
                    <li><span class="check">✓</span> 1 Month Support</li>
                </ul>
                <button class="pricing-btn">Get Started</button>
            </div>
            <div class="pricing-card featured reveal">
                <div class="pricing-badge">Most Popular</div>
                <h3>Professional</h3>
                <div class="pricing-price">$999 <span>/ project</span></div>
                <p class="pricing-desc">For growing businesses</p>
                <ul class="pricing-features">
                    <li><span class="check">✓</span> Up to 15 Pages</li>
                    <li><span class="check">✓</span> Custom Design</li>
                    <li><span class="check">✓</span> Advanced SEO</li>
                    <li><span class="check">✓</span> CMS Integration</li>
                    <li><span class="check">✓</span> 3 Months Support</li>
                    <li><span class="check">✓</span> Performance Optimization</li>
                </ul>
                <button class="pricing-btn">Get Started</button>
            </div>
            <div class="pricing-card reveal">
                <h3>Enterprise</h3>
                <div class="pricing-price">$2499 <span>/ project</span></div>
                <p class="pricing-desc">For large-scale projects</p>
                <ul class="pricing-features">
                    <li><span class="check">✓</span> Unlimited Pages</li>
                    <li><span class="check">✓</span> Custom Everything</li>
                    <li><span class="check">✓</span> E-Commerce Ready</li>
                    <li><span class="check">✓</span> API Integrations</li>
                    <li><span class="check">✓</span> 12 Months Support</li>
                    <li><span class="check">✓</span> Priority Assistance</li>
                </ul>
                <button class="pricing-btn">Contact Us</button>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta-section" id="contact">
        <h2>Ready to Build Something <span class="highlight">Amazing?</span></h2>
        <p>Let's turn your vision into reality. Get in touch today and let's start creating your dream website.</p>
        <a href="mailto:hello@elegancestudio.com" class="btn-primary">Start Your Project →</a>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-grid">
            <div class="footer-brand">
                <a href="#" class="nav-logo">Elegance<span>.</span></a>
                <p>We craft beautiful, high-performing websites that help businesses grow and succeed in the digital world.</p>
                <div class="footer-social">
                    <a href="#">in</a>
                    <a href="#">tw</a>
                    <a href="#">ig</a>
                    <a href="#">fb</a>
                </div>
            </div>
            <div class="footer-col">
                <h4>Services</h4>
                <ul>
                    <li><a href="#">Web Design</a></li>
                    <li><a href="#">Development</a></li>
                    <li><a href="#">E-Commerce</a></li>
                    <li><a href="#">SEO</a></li>
                    <li><a href="#">Branding</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Company</h4>
                <ul>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Portfolio</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Contact</h4>
                <ul>
                    <li><a href="#">hello@elegance.com</a></li>
                    <li><a href="#">+1 (555) 123-4567</a></li>
                    <li><a href="#">New York, NY</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© 2024 Elegance Studio. All rights reserved. Crafted with ❤️</p>
        </div>
    </footer>

    <script>
        // Preloader
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.querySelector('.preloader').classList.add('hidden');
            }, 800);
        });

        // Custom Cursor
        const cursor = document.querySelector('.custom-cursor');
        document.addEventListener('mousemove', (e) => {
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
        });

        document.querySelectorAll('a, button, .portfolio-card, .service-card').forEach(el => {
            el.addEventListener('mouseenter', () => cursor.classList.add('hovering'));
            el.addEventListener('mouseleave', () => cursor.classList.remove('hovering'));
        });

        // Navbar Scroll
        const navbar = document.getElementById('navbar');
        const scrollTopBtn = document.getElementById('scrollTop');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 80) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }

            if (window.scrollY > 500) {
                scrollTopBtn.classList.add('visible');
            } else {
                scrollTopBtn.classList.remove('visible');
            }
        });

        scrollTopBtn.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // Mobile Menu
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');

        menuToggle.addEventListener('click', () => {
            menuToggle.classList.toggle('active');
            navLinks.classList.toggle('open');
        });

        navLinks.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                menuToggle.classList.remove('active');
                navLinks.classList.remove('open');
            });
        });

        // Hero Particles
        const particlesContainer = document.getElementById('heroParticles');
        for (let i = 0; i < 30; i++) {
            const particle = document.createElement('div');
            particle.classList.add('particle');
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 15 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
            particle.style.width = (Math.random() * 4 + 2) + 'px';
            particle.style.height = particle.style.width;
            particlesContainer.appendChild(particle);
        }

        // Scroll Reveal
        const revealElements = document.querySelectorAll('.reveal');

        const revealObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        });

        revealElements.forEach(el => revealObserver.observe(el));

        // Counter Animation
        const stats = document.querySelectorAll('.hero-stat h3');
        let counted = false;

        function animateCounters() {
            if (counted) return;
            counted = true;

            stats.forEach(stat => {
                const text = stat.textContent;
                const number = parseInt(text);
                const suffix = text.replace(/[0-9]/g, '');
                let current = 0;
                const increment = number / 60;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= number) {
                        current = number;
                        clearInterval(timer);
                    }
                    stat.innerHTML = Math.floor(current) + '<span>' + suffix + '</span>';
                }, 25);
            });
        }

        const heroObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateCounters();
                }
            });
        }, { threshold: 0.5 });

        document.querySelectorAll('.hero-stats').forEach(el => heroObserver.observe(el));

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });
    </script>
</body>
</html>
