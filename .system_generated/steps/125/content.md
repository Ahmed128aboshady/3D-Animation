Title: Live Content

Description: Fetched live

Source: https://raw.githubusercontent.com/Ahmed128aboshady/five-hills/main/portfolio.html

---

<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <link rel="canonical" href="https://fivehills.ae/portfolio.html" />
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Property Portfolio & Operations | 5 Hills Dubai</title>
    <meta name="description" content="Five Hills Real Estate L.L.C is a premier property management and leasing agency in Dubai Marina. Specialized in A-to-Z property operations, yield optimization, and renovations.">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    

    <!-- Main stylesheet -->
    <link rel="stylesheet" href="style.css?v=1.25">

    <style>
        /* ---- Custom Utility Classes replacing Tailwind ---- */
        .relative { position: relative; }
        .absolute { position: absolute; }
        .fixed { position: fixed; }
        .sticky { position: sticky; }
        .top-0 { top: 0; }
        .left-0 { left: 0; }
        .right-0 { right: 0; }
        .bottom-0 { bottom: 0; }
        .inset-0 { top: 0; right: 0; bottom: 0; left: 0; }
        .flex { display: flex; }
        .items-center { align-items: center; }
        .justify-center { justify-content: center; }
        .h-screen { height: 100vh; }
        .w-full { width: 100%; }
        .h-full { height: 100%; }
        .overflow-hidden { overflow: hidden; }
        .object-cover { object-fit: cover; }
        .mx-auto { margin-left: auto; margin-right: auto; }
        .max-w-700 { max-width: 700px; }
        .px-6 { padding-left: 1.5rem; padding-right: 1.5rem; }
        .text-center { text-align: center; }

        /* ---- Soft Visual Design Agency Custom Rules (tasteskill) ---- */
        :root {
            --color-bg-obsidian: #03070c;
            --color-card-obsidian: rgba(10, 16, 26, 0.85);
            --color-accent-green: #1b8243;
            --color-gold-agency: #cfa15c;
            --color-border-hairline: rgba(207, 161, 92, 0.15);
            --color-text-bright: #FFFFFF;
            --color-text-muted: #cbd5e1;
            --color-bg-deep-alt: #050a11;
            --color-outer-bezel-bg: rgba(255, 255, 255, 0.02);
            --color-outer-bezel-border: rgba(255, 255, 255, 0.04);
            --transition-spring: all 0.6s cubic-bezier(0.16, 1, 0.3, 1);
            --color-hero-overlay: rgba(3, 7, 12, 0.30);
        }

        body.light-theme {
            --color-bg-obsidian: #f3f5f8;
            --color-card-obsidian: rgba(255, 255, 255, 0.85);
            --color-border-hairline: rgba(12, 60, 102, 0.15);
            --color-text-bright: #050b11;
            --color-text-muted: #334155;
            --color-bg-deep-alt: #e9ecf0;
            --color-outer-bezel-bg: rgba(0, 0, 0, 0.02);
            --color-outer-bezel-border: rgba(0, 0, 0, 0.04);
            --color-hero-overlay: rgba(243, 245, 248, 0.45);
        }

        body {
            background-color: var(--color-bg-obsidian) !important;
            color: var(--color-text-bright) !important;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            transition: background-color 0.4s ease, color 0.4s ease;
        }

        /* Subtle film grain effect to elevate layout visual feel */
        .film-grain {
            position: fixed;
            inset: 0;
            width: 100vw;
            height: 100vh;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
            opacity: 0.015;
            pointer-events: none;
            z-index: 9999;
        }

        /* Custom Magnetic Cursor using translate3d for GPU acceleration */
        .custom-cursor {
            width: 8px;
            height: 8px;
            background: var(--color-gold-agency);
            border-radius: 50%;
            position: fixed;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 10000;
            transition: width 0.3s, height 0.3s, background-color 0.3s;
            will-change: transform;
        }

        .custom-cursor-follower {
            width: 32px;
            height: 32px;
            border: 1px solid rgba(207, 161, 92, 0.3);
            border-radius: 50%;
            position: fixed;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 9999;
            transition: transform 0.15s cubic-bezier(0.25, 1, 0.5, 1), width 0.3s, height 0.3s, border-color 0.3s;
            will-change: transform;
        }

        @media (max-width: 1024px) {
            .custom-cursor, .custom-cursor-follower { display: none; }
        }

        /* ---- Double-Bezel Concentric Card Architecture (Doppelrand) ---- */
        .double-bezel-outer {
            background: var(--color-outer-bezel-bg);
            border: 1px solid var(--color-outer-bezel-border);
            padding: 12px;
            border-radius: 24px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
            transition: var(--transition-spring);
        }

        .double-bezel-inner {
            background: var(--color-card-obsidian);
            border: 1px solid var(--color-border-hairline);
            border-radius: calc(24px - 12px);
            padding: 30px;
            height: 100%;
            box-shadow: inset 0 1px 1px rgba(255,255,255,0.08);
            transition: var(--transition-spring);
        }

        /* ---- Agency Bento Box Masonry Grid ---- */
        .bento-grid {
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .bento-item-3 { grid-column: span 3; }
        .bento-item-4 { grid-column: span 4; }
        .bento-item-5 { grid-column: span 5; }
        .bento-item-6 { grid-column: span 6; }
        .bento-item-7 { grid-column: span 7; }
        .bento-item-8 { grid-column: span 8; }
        .bento-item-12 { grid-column: span 12; }

        @media (max-width: 900px) {
            .bento-item-3, .bento-item-4, .bento-item-5, .bento-item-6, .bento-item-7, .bento-item-8 { grid-column: span 12; }
            .bento-grid { gap: 20px; }
        }

        /* ---- High-End Layout Typography & Spacing ---- */
        .agency-section {
            padding: 140px 0;
            position: relative;
        }

        @media (max-width: 768px) {
            .agency-section { padding: 80px 0; }
        }

        .agency-tagline {
            font-size: 0.8rem;
            color: var(--color-gold-agency);
            letter-spacing: 0.25em;
            text-transform: uppercase;
            font-weight: 600;
            display: block;
            margin-bottom: 20px;
        }

        .agency-title {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            line-height: 1.15;
            color: var(--color-text-bright) !important;
            font-weight: 500;
        }

        .agency-desc {
            font-size: 1.05rem;
            color: var(--color-text-muted);
            line-height: 1.75;
            margin-top: 25px;
            max-width: 680px;
        }

        @media (max-width: 768px) {
            .agency-title { font-size: 2.3rem; }
            .agency-desc {
                font-size: 0.95rem;
                color: var(--color-text-bright) !important;
                font-weight: 500;
            }
        }

        /* ---- Interactive Reveal-on-Scroll Staggered Slide Classes ---- */
        .reveal-element {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 1.2s cubic-bezier(0.16, 1, 0.3, 1), transform 1.2s cubic-bezier(0.16, 1, 0.3, 1);
            will-change: transform, opacity;
        }

        .reveal-left {
            opacity: 0;
            transform: translateX(-80px) translateY(15px);
            transition: opacity 1.3s cubic-bezier(0.16, 1, 0.3, 1), transform 1.3s cubic-bezier(0.16, 1, 0.3, 1);
            will-change: transform, opacity;
        }

        .reveal-right {
            opacity: 0;
            transform: translateX(80px) translateY(15px);
            transition: opacity 1.3s cubic-bezier(0.16, 1, 0.3, 1), transform 1.3s cubic-bezier(0.16, 1, 0.3, 1);
            will-change: transform, opacity;
        }

        .reveal-element.active,
        .reveal-left.active,
        .reveal-right.active {
            opacity: 1;
            transform: translate3d(0, 0, 0);
        }

        /* ---- Concentric 3D Card Hover Effects ---- */
        .hover-card-3d {
            perspective: 1000px;
            cursor: pointer;
        }

        .hover-card-3d:hover .double-bezel-outer {
            transform: translateY(-8px) scale(1.01);
            border-color: rgba(207, 161, 92, 0.3);
            box-shadow: 0 20px 45px rgba(27,130,67,0.15);
        }

        .hover-card-3d:hover .double-bezel-inner {
            border-color: rgba(207, 161, 92, 0.3);
        }

        /* ---- Image Containment double bezel ---- */
        .agency-media-wrap {
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--color-border-hairline);
            position: relative;
            height: 230px;
            margin-bottom: 20px;
        }

        .agency-media-wrap img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.7s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .hover-card-3d:hover .agency-media-wrap img {
            transform: scale(1.08);
        }

        /* ---- Premium Filter Buttons ---- */
        .filter-agency-container {
            display: flex;
            gap: 15px;
            margin-bottom: 50px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .filter-agency-btn {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid var(--color-border-hairline);
            color: var(--color-text-muted);
            padding: 10px 24px;
            font-size: 0.85rem;
            border-radius: 50px;
            cursor: pointer;
            transition: var(--transition-spring);
        }

        .filter-agency-btn.active, .filter-agency-btn:hover {
            background: var(--color-accent-green);
            border-color: var(--color-accent-green);
            color: #FFFFFF;
            box-shadow: 0 5px 15px rgba(27, 130, 67, 0.3);
        }

        /* Exploding text animation styling (Asymmetric Entry Directions) */
        .explode-text {
            transition: opacity 0.35s cubic-bezier(0.16, 1, 0.3, 1), transform 0.35s cubic-bezier(0.16, 1, 0.3, 1);
            position: absolute;
            width: 100%;
            opacity: 0;
            pointer-events: none;
            will-change: transform, opacity;
        }

        .explode-text.active {
            opacity: 1;
            transform: translate3d(0, 0, 0) scale(1) !important;
            pointer-events: auto;
        }

        .explode-text p {
            font-size: 1.05rem;
            line-height: 1.6;
            color: var(--color-text-muted) !important;
            font-weight: 400;
        }

        /* 3D Scroll Panel Distinct Entry Vectors */
        #explode-text-1 {
            transform: translate3d(140px, -140px, 0); /* Top-Right */
        }
        #explode-text-2 {
            transform: translate3d(140px, 140px, 0); /* Bottom-Right */
        }
        #explode-text-3 {
            transform: translate3d(-140px, -140px, 0); /* Top-Left */
        }
        #explode-text-4 {
            transform: translate3d(-140px, 140px, 0); /* Bottom-Left */
        }
        #explode-text-5 {
            transform: scale(0.5); /* Zoom in from center */
        }
        #explode-text-6 {
            transform: translate3d(0, -180px, 0); /* Top-Center drop */
        }

        @media (max-width: 768px) {
            .explode-text p {
                font-size: 0.95rem;
                color: var(--color-text-bright) !important;
                font-weight: 500;
            }
            .double-bezel-inner p {
                color: var(--color-text-bright) !important;
                font-weight: 500;
            }
            /* Reset horizontal transformations on mobile for screen alignment safety */
            .reveal-left, .reveal-right {
                transform: translateY(40px) !important;
            }

            /* ── MOBILE: Replace sticky 3D scroll with simple stacked cards ── */

            /* 1. Collapse the tall sticky scroll section to auto height */
            #exploding-scroll {
                height: auto !important;
                padding: 60px 0 !important;
            }

            /* 2. Un-sticky the inner wrapper - make it a normal block */
            #exploding-scroll > div:first-child {
                position: static !important;
                height: auto !important;
                display: block !important;
                overflow: visible !important;
            }

            /* 3. Hide the 3D canvas and vignette overlays */
            #explode-canvas,
            #exploding-scroll .vignette-radial,
            #exploding-scroll .fade-top,
            #exploding-scroll .fade-bottom {
                display: none !important;
            }

            /* 4. Hide the glow background blob */
            #exploding-scroll > div:first-child > div:first-child {
                display: none !important;
            }

            /* 5. Make the panels container a normal vertical stack */
            #exploding-scroll .relative.z-10.mx-auto {
                position: static !important;
                display: flex !important;
                flex-direction: column !important;
                gap: 24px !important;
                padding: 0 16px !important;
                max-width: 100% !important;
                box-sizing: border-box !important;
                width: 100% !important;
            }

            /* 6. All panels visible as stacked cards on mobile - no JS needed */
            .explode-text {
                position: static !important;
                width: 100% !important;
                opacity: 1 !important;
                transform: none !important;
                transition: none !important;
                pointer-events: auto !important;
            }

            /* 7. Panel sizing on mobile */
            .double-bezel-inner {
                padding: 22px !important;
            }
            .explode-text h2.agency-title,
            #exploding-scroll h2.agency-title {
                font-size: 1.5rem !important;
            }
        }


        /* Vignettes using variable color paths */
        .vignette-radial {
            position: absolute;
            inset: 0;
            background: radial-gradient(ellipse 70% 55% at center, transparent 25%, var(--color-bg-obsidian) 75%);
            z-index: 2;
            pointer-events: none;
        }
        .fade-top {
            position: absolute;
            inset-x: 0;
            top: 0;
            height: 12rem;
            background: linear-gradient(to bottom, var(--color-bg-obsidian), transparent);
            z-index: 2;
            pointer-events: none;
        }
        .fade-bottom {
            position: absolute;
            inset-x: 0;
            bottom: 0;
            height: 12rem;
            background: linear-gradient(to top, var(--color-bg-obsidian), transparent);
            z-index: 2;
            pointer-events: none;
        }

        /* ---- Floating WhatsApp Widget Styling ---- */
        .whatsapp-widget {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25d366;
            color: #FFFFFF;
            padding: 12px 20px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            z-index: 999;
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.3);
            transition: var(--transition-spring);
        }
        .whatsapp-widget:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(37, 211, 102, 0.45);
        }
        .whatsapp-widget svg {
            width: 20px;
            height: 20px;
            fill: currentColor;
        }

        /* ---- Asset Detail Modal Styling ---- */
        .asset-modal {
            position: fixed;
            inset: 0;
            background: rgba(3, 7, 12, 0.92);
            backdrop-filter: blur(20px);
            z-index: 99999;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px 15px;
            opacity: 0;
            pointer-events: none;
            transition: var(--transition-spring);
        }
        .asset-modal.active {
            opacity: 1;
            pointer-events: auto;
        }
        .asset-modal-window {
            background: rgba(10, 16, 26, 0.97);
            border: 1px solid var(--color-border-hairline);
            border-radius: 24px;
            padding: 25px 25px 25px 25px;
            max-width: 540px;
            width: 100%;
            max-height: calc(90vh - 30px);
            overflow-y: auto;
            position: relative;
            transform: scale(0.9) translateY(20px);
            transition: var(--transition-spring);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.9);
            box-sizing: border-box;
            overscroll-behavior: contain;
        }
        .asset-modal-window::-webkit-scrollbar {
            width: 6px;
        }
        .asset-modal-window::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 8px;
        }
        .asset-modal-window::-webkit-scrollbar-thumb {
            background: rgba(255, 255, 255, 0.2);
            border-radius: 8px;
        }
        .asset-modal-window::-webkit-scrollbar-thumb:hover {
            background: var(--color-gold-agency);
        }
        .asset-modal.active .asset-modal-window {
            transform: scale(1) translateY(0);
        }
        .asset-modal-close {
            position: sticky;
            top: 0;
            float: right;
            z-index: 100;
            background: rgba(255, 255, 255, 0.12);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: #FFFFFF;
            font-size: 1.5rem;
            width: 34px;
            height: 34px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            line-height: 1;
            cursor: pointer;
            opacity: 0.9;
            transition: all 0.2s ease;
            margin-bottom: 5px;
        }
        .asset-modal-close:hover {
            opacity: 1;
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.08);
        }
        .asset-modal-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 2.5vw, 1.6rem);
            margin-bottom: 15px;
            padding-right: 40px;
            line-height: 1.3;
        }
        .asset-modal-desc {
            font-size: 0.88rem;
            color: var(--color-text-muted);
            line-height: 1.6;
            margin-bottom: 20px;
        }
        .asset-modal-meta {
            display: flex;
            flex-direction: column;
            gap: 10px;
            font-size: 0.88rem;
            margin-bottom: 25px;
            border-top: 1px solid rgba(255,255,255,0.06);
            padding-top: 15px;
        }
        .asset-modal-gallery {
            margin-bottom: 15px;
        }
        .asset-modal-main-img {
            width: 100%;
            height: clamp(160px, 22vh, 220px);
            object-fit: cover;
            border-radius: 14px;
            border: 1px solid var(--color-border-hairline);
            margin-bottom: 10px;
        }
        .asset-modal-thumbs {
            display: flex;
            gap: 8px;
            overflow-x: auto;
            padding-bottom: 4px;
 

