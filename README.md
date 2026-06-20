# HALCONDORADO
HALCONDORADO
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Halcón Dorado — Lácteos & Delicias Premium</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:opsz,wght@9..40,400;9..40,500;9..40,600;9..40,700&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #C8960C;
            --gold-light: #E8B930;
            --gold-pale: #FDF6E3;
            --gold-dim: rgba(200,150,12,0.12);
            --navy: #1A1F3A;
            --navy-light: #2D3456;
            --navy-mid: #242952;
            --cream: #FFFCF5;
            --cream-dark: #F0E8D4;
            --cream-mid: #F7F0E0;
            --white: #FFFFFF;
            --text: #1E1E2E;
            --text-light: #6B6880;
            --red: #D64545;
            --green-wa: #25D366;
            --shadow-sm: 0 1px 3px rgba(26,31,58,0.06);
            --shadow-md: 0 4px 16px rgba(26,31,58,0.09);
            --shadow-lg: 0 12px 40px rgba(26,31,58,0.13);
            --shadow-gold: 0 4px 20px rgba(200,150,12,0.28);
            --radius: 18px;
            --radius-sm: 11px;
            --font-display: 'Playfair Display', Georgia, serif;
            --font-body: 'DM Sans', system-ui, sans-serif;
        }

        *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
        html { scroll-behavior: smooth; }
        body {
            font-family: var(--font-body);
            background: var(--cream);
            color: var(--text);
            line-height: 1.55;
            overflow-x: hidden;
            padding-bottom: 88px;
        }

        ::-webkit-scrollbar { width: 5px; }
        ::-webkit-scrollbar-track { background: var(--cream); }
        ::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 3px; }

        @keyframes fadeUp { from { opacity: 0; transform: translateY(22px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes pop { 0%,100% { transform: scale(1); } 50% { transform: scale(1.3); } }
        @keyframes shimmer { from { background-position: -200% 0; } to { background-position: 200% 0; } }
        .fade-up { animation: fadeUp 0.5s ease-out both; }

        /* ── HEADER ── */
        .site-header {
            position: sticky; top: 0; z-index: 100;
            background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
            box-shadow: 0 2px 24px rgba(0,0,0,0.18);
        }
        .header-inner {
            max-width: 1200px; margin: 0 auto;
            padding: 13px 20px;
            display: flex; justify-content: space-between; align-items: center;
        }
        .brand { display: flex; align-items: center; gap: 12px; text-decoration: none; }
        .brand-icon {
            width: 46px; height: 46px;
            background: linear-gradient(135deg, var(--gold) 0%, var(--gold-light) 100%);
            border-radius: 13px; display: flex; align-items: center; justify-content: center;
            font-size: 23px; box-shadow: var(--shadow-gold); flex-shrink: 0;
        }
        .brand-name { font-family: var(--font-display); font-weight: 900; font-size: 19px; color: var(--white); letter-spacing: -0.3px; line-height: 1.1; }
        .brand-tagline { font-size: 10.5px; color: var(--gold-light); font-weight: 600; letter-spacing: 1.6px; text-transform: uppercase; }
        .header-actions { display: flex; gap: 8px; align-items: center; }
        .header-btn {
            width: 42px; height: 42px; border-radius: 13px; border: none;
            background: rgba(255,255,255,0.09); color: white; font-size: 18px;
            cursor: pointer; transition: all 0.2s; display: flex; align-items: center; justify-content: center;
            position: relative;
        }
        .header-btn:hover { background: rgba(255,255,255,0.16); transform: translateY(-1px); }
        .cart-badge {
            position: absolute; top: -5px; right: -5px;
            background: var(--red); color: white; font-size: 10px; font-weight: 700;
            width: 19px; height: 19px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            border: 2.5px solid var(--navy);
        }
        .cart-badge.hidden { display: none; }
        .cart-badge.pop { animation: pop 0.3s ease-in-out; }

        /* ── HERO ── */
        .hero {
            background: linear-gradient(145deg, var(--navy) 0%, var(--navy-mid) 60%, #1F2650 100%);
            padding: 52px 20px 72px;
            position: relative; overflow: hidden;
        }
        .hero-glow-1 {
            position: absolute; top: -40%; right: -10%; width: 520px; height: 520px;
            background: radial-gradient(circle, rgba(200,150,12,0.18) 0%, transparent 65%);
            border-radius: 50%; pointer-events: none;
        }
        .hero-glow-2 {
            position: absolute; bottom: -20%; left: -5%; width: 350px; height: 350px;
            background: radial-gradient(circle, rgba(200,150,12,0.08) 0%, transparent 70%);
            border-radius: 50%; pointer-events: none;
        }
        .hero-wave {
            position: absolute; bottom: 0; left: 0; right: 0;
            height: 48px; background: var(--cream);
            clip-path: ellipse(55% 100% at 50% 100%);
        }
        .hero-inner { max-width: 1200px; margin: 0 auto; position: relative; z-index: 1; }
        .hero-eyebrow {
            display: inline-flex; align-items: center; gap: 6px;
            background: rgba(200,150,12,0.15); border: 1px solid rgba(200,150,12,0.3);
            padding: 5px 14px; border-radius: 100px; margin-bottom: 16px;
            font-size: 12px; font-weight: 600; color: var(--gold-light); letter-spacing: 0.5px;
        }
        .hero h1 {
            font-family: var(--font-display); font-size: clamp(30px, 6vw, 50px);
            color: var(--white); font-weight: 900; line-height: 1.12; margin-bottom: 14px;
        }
        .hero h1 em { color: var(--gold-light); font-style: italic; }
        .hero-sub { color: rgba(255,255,255,0.65); font-size: 15px; max-width: 460px; margin-bottom: 28px; line-height: 1.6; }
        .hero-badges { display: flex; gap: 10px; flex-wrap: wrap; }
        .hero-badge {
            background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.11);
            padding: 8px 16px; border-radius: 100px; color: rgba(255,255,255,0.85);
            font-size: 13px; font-weight: 500; backdrop-filter: blur(8px);
        }
        .hero-badge strong { color: var(--gold-light); }

        /* ── SEARCH & FILTERS ── */
        .controls { max-width: 1200px; margin: -22px auto 0; padding: 0 20px; position: relative; z-index: 10; }
        .search-bar {
            background: var(--white); border-radius: var(--radius); padding: 5px;
            box-shadow: var(--shadow-lg); display: flex; align-items: center; gap: 0;
            margin-bottom: 14px; border: 1.5px solid var(--cream-dark);
        }
        .search-icon { padding: 0 14px 0 18px; color: var(--text-light); font-size: 17px; flex-shrink: 0; }
        .search-bar input {
            flex: 1; border: none; outline: none; padding: 13px 0 13px 0;
            font-family: var(--font-body); font-size: 15px; background: transparent; color: var(--text);
        }
        .search-bar input::placeholder { color: var(--text-light); }
        .filter-row { display: flex; gap: 8px; overflow-x: auto; padding-bottom: 2px; }
        .filter-row::-webkit-scrollbar { display: none; }
        .filter-chip {
            padding: 8px 18px; border-radius: 100px; border: 1.5px solid var(--cream-dark);
            background: var(--white); font-size: 13px; font-weight: 600; color: var(--text-light);
            cursor: pointer; white-space: nowrap; transition: all 0.2s;
        }
        .filter-chip:hover { border-color: var(--gold); color: var(--gold); }
        .filter-chip.active {
            background: linear-gradient(135deg, var(--gold), var(--gold-light));
            color: var(--white); border-color: transparent; box-shadow: var(--shadow-gold);
        }

        /* ── SECTIONS ── */
        .section { max-width: 1200px; margin: 0 auto; padding: 44px 20px 0; }
        .section-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 22px; }
        .section-title { font-family: var(--font-display); font-size: 26px; font-weight: 900; color: var(--navy); }
        .section-title span { color: var(--gold); }

        /* ── COMBOS ── */
        .combos-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 16px; }
        .combo-card {
            background: linear-gradient(145deg, var(--navy) 0%, var(--navy-light) 100%);
            border-radius: var(--radius); padding: 26px; position: relative; overflow: hidden;
            cursor: pointer; transition: transform 0.22s, box-shadow 0.22s;
            border: 1px solid rgba(255,255,255,0.04);
        }
        .combo-card:hover { transform: translateY(-4px); box-shadow: 0 16px 48px rgba(26,31,58,0.22); }
        .combo-card::before {
            content: ''; position: absolute; top: -40%; right: -15%; width: 220px; height: 220px;
            background: radial-gradient(circle, rgba(200,150,12,0.22) 0%, transparent 68%);
            border-radius: 50%; pointer-events: none;
        }
        .combo-save-pill {
            display: inline-flex; align-items: center; gap: 5px;
            background: linear-gradient(135deg, var(--gold), var(--gold-light));
            color: var(--navy); font-size: 11px; font-weight: 800; padding: 4px 12px;
            border-radius: 100px; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 13px;
        }
        .combo-name { font-family: var(--font-display); font-size: 21px; font-weight: 700; color: var(--white); margin-bottom: 7px; line-height: 1.2; }
        .combo-desc { font-size: 13px; color: rgba(255,255,255,0.55); margin-bottom: 16px; line-height: 1.55; }
        .combo-items { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 18px; }
        .combo-item-tag {
            background: rgba(255,255,255,0.08); color: rgba(255,255,255,0.75);
            padding: 4px 10px; border-radius: 7px; font-size: 12px; font-weight: 500;
        }
        .combo-footer { display: flex; justify-content: space-between; align-items: center; }
        .combo-prices { display: flex; align-items: baseline; gap: 8px; }
        .combo-old { font-size: 14px; color: rgba(255,255,255,0.35); text-decoration: line-through; }
        .combo-new { font-size: 26px; font-weight: 800; color: var(--gold-light); font-family: var(--font-display); }
        .combo-add {
            width: 44px; height: 44px; border-radius: 13px; border: none;
            background: linear-gradient(135deg, var(--gold), var(--gold-light));
            color: var(--navy); font-size: 24px; font-weight: 700;
            cursor: pointer; transition: all 0.2s; display: flex; align-items: center; justify-content: center;
            box-shadow: var(--shadow-gold);
        }
        .combo-add:hover { transform: scale(1.08); }
        .combo-discount {
            position: absolute; top: 16px; right: 16px;
            background: rgba(255,255,255,0.1); border: 1px solid rgba(255,255,255,0.15);
            padding: 3px 9px; border-radius: 8px; font-size: 11px; font-weight: 700; color: var(--gold-light);
        }

        /* ── PRODUCTS ── */
        .products-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(162px, 1fr)); gap: 14px; }
        .product-card {
            background: var(--white); border-radius: var(--radius); padding: 18px 14px 14px;
            border: 1.5px solid var(--cream-dark); cursor: pointer;
            transition: all 0.25s; position: relative; overflow: hidden;
        }
        .product-card:hover { border-color: var(--gold); box-shadow: var(--shadow-md); transform: translateY(-3px); }
        .product-emoji {
            font-size: 42px; text-align: center; margin-bottom: 10px; display: block; line-height: 1;
        }
        .product-name { font-weight: 700; font-size: 14px; text-align: center; margin-bottom: 3px; color: var(--navy); line-height: 1.3; }
        .product-weight { font-size: 12px; color: var(--text-light); text-align: center; margin-bottom: 10px; }
        .product-price {
            font-size: 20px; font-weight: 800; color: var(--gold); text-align: center;
            font-family: var(--font-display); margin-bottom: 10px;
        }
        .product-add-btn {
            width: 100%; padding: 9px; border-radius: var(--radius-sm);
            border: 1.5px solid var(--gold); background: transparent; color: var(--gold);
            font-weight: 700; font-size: 13px; cursor: pointer; transition: all 0.2s;
            font-family: var(--font-body);
        }
        .product-add-btn:hover { background: var(--gold); color: var(--white); }
        .product-cat-tag {
            position: absolute; top: 9px; right: 9px;
            background: var(--cream-mid); padding: 2px 8px; border-radius: 6px;
            font-size: 10px; font-weight: 600; color: var(--text-light);
        }
        .admin-del-btn {
            position: absolute; top: 9px; left: 9px;
            background: var(--red); color: white; border: none; border-radius: 6px;
            width: 24px; height: 24px; font-size: 12px; cursor: pointer; display: none;
            align-items: center; justify-content: center;
        }

        /* ── CART ── */
        .cart-overlay {
            position: fixed; inset: 0; background: rgba(10,10,20,0.55);
            z-index: 200; opacity: 0; pointer-events: none; transition: opacity 0.3s;
            backdrop-filter: blur(3px);
        }
        .cart-overlay.open { opacity: 1; pointer-events: auto; }
        .cart-drawer {
            position: fixed; top: 0; right: 0; bottom: 0; width: min(400px, 92vw);
            background: var(--cream); z-index: 201;
            transform: translateX(100%); transition: transform 0.36s cubic-bezier(0.4,0,0.2,1);
            display: flex; flex-direction: column; box-shadow: -8px 0 40px rgba(0,0,0,0.15);
        }
        .cart-drawer.open { transform: translateX(0); }
        .cart-header {
            padding: 20px 22px; display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid var(--cream-dark);
            background: var(--white);
        }
        .cart-header h3 { font-family: var(--font-display); font-size: 22px; font-weight: 900; color: var(--navy); }
        .cart-close {
            width: 36px; height: 36px; border-radius: 10px; border: none;
            background: var(--cream-dark); cursor: pointer; font-size: 17px; transition: all 0.2s;
        }
        .cart-close:hover { background: #ddd0bb; }
        .cart-body { flex: 1; overflow-y: auto; padding: 14px 22px; }
        .cart-empty { text-align: center; padding: 64px 20px; color: var(--text-light); }
        .cart-empty-icon { font-size: 52px; margin-bottom: 14px; display: block; }
        .cart-empty p { font-size: 14px; line-height: 1.6; }
        .cart-item {
            display: flex; gap: 12px; align-items: center;
            padding: 14px 0; border-bottom: 1px solid var(--cream-dark);
        }
        .cart-item-emoji {
            font-size: 30px; width: 50px; height: 50px; background: var(--white);
            border-radius: 13px; display: flex; align-items: center; justify-content: center;
            flex-shrink: 0; border: 1px solid var(--cream-dark);
        }
        .cart-item-info { flex: 1; min-width: 0; }
        .cart-item-name { font-weight: 700; font-size: 14px; color: var(--navy); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
        .cart-item-price { font-size: 13px; color: var(--gold); font-weight: 600; margin-top: 2px; }
        .cart-qty { display: flex; align-items: center; gap: 8px; flex-shrink: 0; }
        .cart-qty button {
            width: 30px; height: 30px; border-radius: 9px; border: 1.5px solid var(--cream-dark);
            background: var(--white); cursor: pointer; font-size: 15px; font-weight: 700;
            display: flex; align-items: center; justify-content: center; transition: all 0.15s;
        }
        .cart-qty button:hover { border-color: var(--gold); color: var(--gold); }
        .cart-qty span { font-weight: 700; font-size: 14px; min-width: 22px; text-align: center; }
        .cart-footer { padding: 18px 22px; border-top: 1px solid var(--cream-dark); background: var(--white); }
        .cart-total { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 16px; }
        .cart-total-label { font-size: 13px; color: var(--text-light); font-weight: 500; }
        .cart-total-amount { font-family: var(--font-display); font-size: 30px; font-weight: 900; color: var(--navy); }
        .wa-btn {
            width: 100%; padding: 15px; border-radius: var(--radius-sm); border: none;
            background: #22C55E; color: white; font-size: 15px; font-weight: 700;
            cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 9px;
            font-family: var(--font-body); transition: all 0.2s; letter-spacing: 0.2px;
        }
        .wa-btn:hover { background: #16a34a; transform: translateY(-1px); box-shadow: 0 6px 20px rgba(34,197,94,0.3); }
        .wa-btn:disabled { opacity: 0.45; cursor: not-allowed; transform: none; box-shadow: none; }
        .clear-cart-btn {
            width: 100%; padding: 10px; margin-top: 8px; border-radius: var(--radius-sm);
            border: none; background: transparent; color: var(--red); font-size: 13px;
            font-weight: 600; cursor: pointer; font-family: var(--font-body); transition: background 0.2s;
        }
        .clear-cart-btn:hover { background: #fef2f2; border-radius: 8px; }

        /* ── MODALS ── */
        .modal-overlay {
            position: fixed; inset: 0; background: rgba(0,0,0,0.6);
            z-index: 300; display: none; align-items: center; justify-content: center; padding: 20px;
            backdrop-filter: blur(4px);
        }
        .modal-overlay.open { display: flex; }
        .modal-box {
            background: var(--white); border-radius: 22px; width: 100%; max-width: 440px;
            padding: 30px; max-height: 90vh; overflow-y: auto;
            animation: fadeUp 0.3s ease-out;
            box-shadow: 0 24px 64px rgba(0,0,0,0.2);
        }
        .modal-title { font-family: var(--font-display); font-size: 22px; font-weight: 900; color: var(--navy); margin-bottom: 22px; }
        .form-group { margin-bottom: 14px; }
        .form-group label { display: block; font-size: 11.5px; font-weight: 700; color: var(--text-light); margin-bottom: 5px; text-transform: uppercase; letter-spacing: 0.6px; }
        .form-input {
            width: 100%; padding: 11px 14px; border: 1.5px solid var(--cream-dark);
            border-radius: var(--radius-sm); font-family: var(--font-body); font-size: 14px;
            transition: border-color 0.2s; outline: none; background: var(--cream);
            color: var(--text);
        }
        .form-input:focus { border-color: var(--gold); background: var(--white); }
        .form-row { display: flex; gap: 10px; }
        .form-row > .form-group { flex: 1; }
        .modal-actions { display: flex; gap: 10px; margin-top: 22px; }
        .btn-cancel {
            flex: 1; padding: 13px; border-radius: var(--radius-sm); border: 1.5px solid var(--cream-dark);
            background: var(--white); font-weight: 700; font-size: 14px; cursor: pointer;
            font-family: var(--font-body); transition: all 0.2s; color: var(--text);
        }
        .btn-cancel:hover { background: var(--cream); }
        .btn-save {
            flex: 1; padding: 13px; border-radius: var(--radius-sm); border: none;
            background: linear-gradient(135deg, var(--gold), var(--gold-light));
            color: var(--white); font-weight: 700; font-size: 14px; cursor: pointer;
            font-family: var(--font-body); transition: all 0.2s; box-shadow: var(--shadow-gold);
        }
        .btn-save:hover { transform: translateY(-1px); box-shadow: 0 6px 24px rgba(200,150,12,0.35); }
        .btn-admin-add {
            padding: 8px 18px; border-radius: var(--radius-sm); border: none;
            background: var(--gold); color: var(--white); font-weight: 700; font-size: 13px;
            cursor: pointer; font-family: var(--font-body); transition: all 0.2s;
        }
        .btn-admin-add:hover { background: var(--gold-light); }

        /* ── CONTACT SECTION ── */
        .contact-section {
            max-width: 1200px; margin: 48px auto 0; padding: 0 20px;
        }
        .contact-card {
            background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
            border-radius: var(--radius); padding: 36px 32px;
            display: flex; align-items: center; justify-content: space-between; gap: 24px;
            flex-wrap: wrap; position: relative; overflow: hidden;
        }
        .contact-card::before {
            content: ''; position: absolute; top: -30%; right: -5%; width: 300px; height: 300px;
            background: radial-gradient(circle, rgba(200,150,12,0.15) 0%, transparent 70%);
            border-radius: 50%; pointer-events: none;
        }
        .contact-text { position: relative; z-index: 1; }
        .contact-text h3 { font-family: var(--font-display); font-size: 24px; font-weight: 900; color: var(--white); margin-bottom: 6px; }
        .contact-text p { color: rgba(255,255,255,0.6); font-size: 14px; }
        .wa-contact-btn {
            padding: 14px 28px; border-radius: var(--radius-sm); border: none;
            background: #22C55E; color: white; font-size: 15px; font-weight: 700;
            cursor: pointer; display: flex; align-items: center; gap: 9px;
            font-family: var(--font-body); transition: all 0.2s; white-space: nowrap;
            position: relative; z-index: 1;
        }
        .wa-contact-btn:hover { background: #16a34a; transform: translateY(-2px); box-shadow: 0 6px 20px rgba(34,197,94,0.3); }

        /* ── FOOTER ── */
        .site-footer {
            max-width: 1200px; margin: 52px auto 0; padding: 36px 20px 20px;
            border-top: 1px solid var(--cream-dark); text-align: center;
        }
        .footer-brand { font-family: var(--font-display); font-size: 20px; font-weight: 900; color: var(--navy); margin-bottom: 8px; }
        .footer-text { font-size: 13px; color: var(--text-light); line-height: 1.8; }

        /* ── MOBILE NAV ── */
        .mobile-nav {
            position: fixed; bottom: 0; left: 0; right: 0; z-index: 90;
            background: var(--white); border-top: 1px solid var(--cream-dark);
            display: none; padding: 6px 0 env(safe-area-inset-bottom, 8px);
            box-shadow: 0 -4px 24px rgba(0,0,0,0.07);
        }
        .mobile-nav-inner { display: flex; justify-content: space-around; align-items: center; }
        .mobile-nav-btn {
            display: flex; flex-direction: column; align-items: center; gap: 2px;
            background: none; border: none; padding: 6px 16px; cursor: pointer;
            color: var(--text-light); font-size: 10px; font-weight: 600;
            font-family: var(--font-body); transition: color 0.2s;
        }
        .mobile-nav-btn.active, .mobile-nav-btn:hover { color: var(--gold); }
        .mobile-nav-btn span:first-child { font-size: 21px; }

        /* ── TOAST ── */
        .toast {
            position: fixed; bottom: 96px; left: 50%; transform: translateX(-50%) translateY(20px);
            background: var(--navy); color: var(--white); padding: 12px 24px;
            border-radius: 100px; font-size: 14px; font-weight: 600; z-index: 500;
            opacity: 0; transition: all 0.3s; pointer-events: none;
            box-shadow: var(--shadow-lg); white-space: nowrap;
        }
        .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

        /* ── EMPTY STATE ── */
        .empty-state {
            grid-column: 1/-1; text-align: center; padding: 48px 20px;
            color: var(--text-light);
        }
        .empty-state-icon { font-size: 40px; margin-bottom: 12px; }

        /* ── ADMIN ── */
        .admin-only { display: none; }
        body.admin-mode .admin-only { display: flex; }
        body.admin-mode .admin-del-btn { display: flex; }

        /* ── RESPONSIVE ── */
        @media (max-width: 640px) {
            .products-grid { grid-template-columns: repeat(2, 1fr); gap: 10px; }
            .combos-grid { grid-template-columns: 1fr; }
            .hero { padding: 36px 20px 56px; }
            .mobile-nav { display: block; }
            .section { padding: 32px 16px 0; }
            .controls { padding: 0 16px; }
            .contact-card { padding: 28px 22px; }
            .contact-text h3 { font-size: 20px; }
        }
        @media (min-width: 641px) {
            .mobile-nav { display: none !important; }
        }
    </style>
</head>
<body>

<!-- HEADER -->
<header class="site-header">
    <div class="header-inner">
        <div class="brand">
            <div class="brand-icon">🦅</div>
            <div>
                <div class="brand-name">El Halcón Dorado</div>
                <div class="brand-tagline">Lácteos Premium</div>
            </div>
        </div>
        <div class="header-actions">
            <button class="header-btn admin-only" onclick="toggleAdmin()" title="Administración" aria-label="Admin">⚙️</button>
            <button class="header-btn" onclick="openCart()" title="Ver carrito" aria-label="Carrito">
                🛒
                <span id="cartBadge" class="cart-badge hidden" aria-live="polite">0</span>
            </button>
        </div>
    </div>
</header>

<!-- HERO -->
<section class="hero">
    <div class="hero-glow-1"></div>
    <div class="hero-glow-2"></div>
    <div class="hero-inner">
        <div class="hero-eyebrow fade-up">🦅 Calidad desde el campo hasta tu mesa</div>
        <h1 class="fade-up" style="animation-delay:0.08s">
            Sabor artesanal<br>en cada <em>producto</em>
        </h1>
        <p class="hero-sub fade-up" style="animation-delay:0.16s">
            Quesos, dulces y delicias artesanales. Calidad premium con delivery directo a tu puerta.
        </p>
        <div class="hero-badges fade-up" style="animation-delay:0.24s">
            <span class="hero-badge"><strong>🐄</strong> 100% Natural</span>
            <span class="hero-badge"><strong>🚚</strong> Delivery</span>
            <span class="hero-badge"><strong>📱</strong> Pedidos por WhatsApp</span>
            <span class="hero-badge"><strong>⭐</strong> Calidad Premium</span>
        </div>
    </div>
    <div class="hero-wave"></div>
</section>

<!-- SEARCH & FILTERS -->
<div class="controls">
    <div class="search-bar">
        <span class="search-icon">🔍</span>
        <input type="text" id="searchInput" placeholder="Buscar productos..." oninput="filtrar()" aria-label="Buscar">
    </div>
    <div class="filter-row" id="filterRow" role="group" aria-label="Filtrar categoría">
        <button class="filter-chip active" data-cat="Todos" onclick="setFilter(this)">Todos</button>
        <button class="filter-chip" data-cat="Frescos" onclick="setFilter(this)">🧀 Quesos</button>
        <button class="filter-chip" data-cat="Maduros" onclick="setFilter(this)">🏆 Madurados</button>
        <button class="filter-chip" data-cat="Dulces" onclick="setFilter(this)">🍯 Dulces</button>
        <button class="filter-chip" data-cat="Otros" onclick="setFilter(this)">🥨 Otros</button>
    </div>
</div>

<!-- COMBOS -->
<section class="section" id="sectionCombos">
    <div class="section-header">
        <h2 class="section-title">🔥 <span>Combos</span> Especiales</h2>
        <button class="btn-admin-add admin-only" onclick="abrirModalCombo()">+ Combo</button>
    </div>
    <div class="combos-grid" id="combosGrid"></div>
</section>

<!-- PRODUCTS -->
<section class="section" id="sectionCatalogo">
    <div class="section-header">
        <h2 class="section-title">🧀 Nuestro <span>Catálogo</span></h2>
        <button class="btn-admin-add admin-only" onclick="abrirModalProducto()">+ Producto</button>
    </div>
    <div class="products-grid" id="productsGrid"></div>
</section>

<!-- CONTACT -->
<div class="contact-section">
    <div class="contact-card">
        <div class="contact-text">
            <h3>¿Tienes alguna consulta?</h3>
            <p>Escríbenos por WhatsApp, respondemos rápido</p>
        </div>
        <button class="wa-contact-btn" onclick="contactarWA()">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.555 4.122 1.523 5.857L0 24l6.335-1.652A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.75c-1.875 0-3.63-.5-5.145-1.382l-.37-.219-3.756.98.998-3.648-.24-.38A9.69 9.69 0 012.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75z"/></svg>
            Hablar por WhatsApp
        </button>
    </div>
</div>

<!-- FOOTER -->
<footer class="site-footer">
    <div class="footer-brand">🦅 El Halcón Dorado</div>
    <p class="footer-text">
        Lácteos artesanales y delicias de calidad premium<br>
        Pedidos por WhatsApp · Delivery disponible<br>
        <span style="color:var(--gold);font-weight:600">📞 +51 956 750 818</span>
    </p>
</footer>

<!-- CART DRAWER -->
<div class="cart-overlay" id="cartOverlay" onclick="closeCart()" role="dialog" aria-modal="true" aria-label="Carrito de compras"></div>
<div class="cart-drawer" id="cartDrawer">
    <div class="cart-header">
        <h3>Tu Pedido 🛒</h3>
        <button class="cart-close" onclick="closeCart()" aria-label="Cerrar carrito">✕</button>
    </div>
    <div class="cart-body" id="cartBody"></div>
    <div class="cart-footer" id="cartFooter"></div>
</div>

<!-- MODAL PRODUCTO -->
<div class="modal-overlay" id="modalProducto" role="dialog" aria-modal="true">
    <div class="modal-box">
        <div class="modal-title" id="modalProdTitle">Nuevo Producto</div>
        <div id="formProducto">
            <input type="hidden" id="fProdId">
            <div class="form-group">
                <label>Nombre del producto</label>
                <input class="form-input" id="fProdNombre" placeholder="Ej: Queso Fresco Premium">
            </div>
            <div class="form-row">
                <div class="form-group">
                    <label>Peso / Cantidad</label>
                    <input class="form-input" id="fProdPeso" placeholder="Ej: 500g">
                </div>
                <div class="form-group">
                    <label>Precio (S/)</label>
                    <input class="form-input" type="number" step="0.50" min="0" id="fProdPrecio" placeholder="0.00">
                </div>
            </div>
            <div class="form-row">
                <div class="form-group">
                    <label>Categoría</label>
                    <select class="form-input" id="fProdCat">
                        <option value="Frescos">Quesos Frescos</option>
                        <option value="Maduros">Madurados & Especiales</option>
                        <option value="Dulces">Dulces & Manjar</option>
                        <option value="Otros">Rosquitas & Galletas</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Ícono</label>
                    <select class="form-input" id="fProdEmoji">
                        <option value="🧀">🧀 Queso</option>
                        <option value="🧈">🧈 Mantequilla</option>
                        <option value="🥛">🥛 Leche/Yogurt</option>
                        <option value="🍯">🍯 Manjar/Miel</option>
                        <option value="🥐">🥐 Rosca/Pan</option>
                        <option value="🍪">🍪 Galleta</option>
                        <option value="🥨">🥨 Rosquita</option>
                        <option value="🍰">🍰 King Kong</option>
                        <option value="🎂">🎂 Turrón</option>
                    </select>
                </div>
            </div>
            <div class="modal-actions">
                <button class="btn-cancel" onclick="cerrarModal('modalProducto')">Cancelar</button>
                <button class="btn-save" onclick="guardarProducto()">Guardar</button>
            </div>
        </div>
    </div>
</div>

<!-- MODAL COMBO -->
<div class="modal-overlay" id="modalCombo" role="dialog" aria-modal="true">
    <div class="modal-box">
        <div class="modal-title" id="modalComboTitle">Nuevo Combo</div>
        <div id="formCombo">
            <input type="hidden" id="fComboId">
            <div class="form-group">
                <label>Nombre del combo</label>
                <input class="form-input" id="fComboNombre" placeholder="Ej: Combo Familiar">
            </div>
            <div class="form-group">
                <label>Descripción</label>
                <input class="form-input" id="fComboDesc" placeholder="Qué incluye el combo">
            </div>
            <div class="form-group">
                <label>IDs de productos (separados por coma)</label>
                <input class="form-input" id="fComboItems" placeholder="Ej: p1,p2,p3">
            </div>
            <div class="form-row">
                <div class="form-group">
                    <label>Precio original (S/)</label>
                    <input class="form-input" type="number" step="0.50" id="fComboOrig" placeholder="0.00">
                </div>
                <div class="form-group">
                    <label>Precio combo (S/)</label>
                    <input class="form-input" type="number" step="0.50" id="fComboPrice" placeholder="0.00">
                </div>
            </div>
            <div class="modal-actions">
                <button class="btn-cancel" onclick="cerrarModal('modalCombo')">Cancelar</button>
                <button class="btn-save" onclick="guardarCombo()">Guardar</button>
            </div>
        </div>
    </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast" role="status" aria-live="polite"></div>

<!-- MOBILE NAV -->
<nav class="mobile-nav" aria-label="Navegación">
    <div class="mobile-nav-inner">
        <button class="mobile-nav-btn active" onclick="scrollTo({top:0,behavior:'smooth'})" aria-label="Inicio">
            <span>🏠</span>Inicio
        </button>
        <button class="mobile-nav-btn" onclick="document.getElementById('sectionCombos').scrollIntoView({behavior:'smooth'})" aria-label="Combos">
            <span>🔥</span>Combos
        </button>
        <button class="mobile-nav-btn" onclick="document.getElementById('sectionCatalogo').scrollIntoView({behavior:'smooth'})" aria-label="Catálogo">
            <span>🧀</span>Catálogo
        </button>
        <button class="mobile-nav-btn" onclick="openCart()" aria-label="Carrito">
            <span>🛒</span>Carrito
        </button>
    </div>
</nav>

<script>
const WHATSAPP = "51956750818";
let modoAdmin = false;
let filtroActivo = "Todos";

const defaultProductos = [
    { id:'p1', nombre:'Rosquitas Clásicas', peso:'Paquete', precio:10.00, categoria:'Otros', emoji:'🥨' },
    { id:'p2', nombre:'Queso Mantecoso', peso:'160g', precio:10.00, categoria:'Frescos', emoji:'🧀' },
    { id:'p3', nombre:'Manjar Blanco', peso:'450g', precio:10.00, categoria:'Dulces', emoji:'🍯' },
    { id:'p4', nombre:'Turrón de Doña Pepa', peso:'450g', precio:35.00, categoria:'Dulces', emoji:'🎂' },
    { id:'p5', nombre:'King Kong Sipán', peso:'900g', precio:35.00, categoria:'Dulces', emoji:'🍰' },
    { id:'p6', nombre:'Queso Suizo', peso:'500g', precio:30.00, categoria:'Maduros', emoji:'🧀' },
    { id:'p7', nombre:'Miel de Abeja Líquida', peso:'500g', precio:25.00, categoria:'Dulces', emoji:'🍯' },
    { id:'p8', nombre:'Roscas con Queso y Orégano', peso:'450g', precio:16.00, categoria:'Otros', emoji:'🥐' },
    { id:'p9', nombre:'Galletas de Leche', peso:'20u', precio:14.00, categoria:'Otros', emoji:'🍪' }
];

const defaultCombos = [
    {
        id:'c1',
        nombre:'Combo Fiestas Patrias',
        desc:'Turrón de Doña Pepa + King Kong Sipán 900g + Queso Suizo 500g',
        items:['p4','p5','p6'],
        precioOrig:100,
        precioCombo:85.00
    },
    {
        id:'c2',
        nombre:'Combo Compartir',
        desc:'Rosquitas Clásicas + Queso Mantecoso 160g + Manjar Blanco 450g',
        items:['p1','p2','p3'],
        precioOrig:30,
        precioCombo:25.00
    }
];

let dbProductos = JSON.parse(localStorage.getItem('halcon_productos') || 'null') || defaultProductos;
let dbCombos   = JSON.parse(localStorage.getItem('halcon_combos')   || 'null') || defaultCombos;
let carrito    = JSON.parse(localStorage.getItem('halcon_carrito')   || '[]');

function save(key, val) { try { localStorage.setItem(key, JSON.stringify(val)); } catch(e){} }
function saveAll() {
    save('halcon_productos', dbProductos);
    save('halcon_combos', dbCombos);
    save('halcon_carrito', carrito);
}

// ── CART ──
function agregarAlCarrito(id, tipo) {
    const key = tipo + '_' + id;
    const ex  = carrito.find(i => i.key === key);
    if (ex) {
        ex.qty++;
    } else {
        let item;
        if (tipo === 'producto') {
            const p = dbProductos.find(x => x.id === id);
            if (!p) return;
            item = { key, id, tipo, nombre:p.nombre, peso:p.peso, precio:p.precio, emoji:p.emoji, qty:1 };
        } else {
            const c = dbCombos.find(x => x.id === id);
            if (!c) return;
            item = { key, id, tipo, nombre:c.nombre, peso:'', precio:c.precioCombo, emoji:'🎁', qty:1 };
        }
        carrito.push(item);
    }
    save('halcon_carrito', carrito);
    actualizarBadge();
    renderCarrito();
    showToast('✓ Agregado al carrito');
    const badge = document.getElementById('cartBadge');
    badge.classList.remove('pop');
    void badge.offsetWidth;
    badge.classList.add('pop');
    setTimeout(() => badge.classList.remove('pop'), 350);
}

function cambiarCantidad(key, delta) {
    const item = carrito.find(i => i.key === key);
    if (!item) return;
    item.qty += delta;
    if (item.qty <= 0) carrito = carrito.filter(i => i.key !== key);
    save('halcon_carrito', carrito);
    actualizarBadge();
    renderCarrito();
}

function vaciarCarrito() {
    if (!confirm('¿Vaciar el carrito?')) return;
    carrito = [];
    save('halcon_carrito', carrito);
    actualizarBadge();
    renderCarrito();
}

function actualizarBadge() {
    const badge = document.getElementById('cartBadge');
    const total = carrito.reduce((s,i) => s + i.qty, 0);
    badge.textContent = total;
    badge.classList.toggle('hidden', total === 0);
}

function obtenerTotal() {
    return carrito.reduce((s,i) => s + (i.precio * i.qty), 0);
}

function openCart() {
    document.getElementById('cartOverlay').classList.add('open');
    document.getElementById('cartDrawer').classList.add('open');
    renderCarrito();
}

function closeCart() {
    document.getElementById('cartOverlay').classList.remove('open');
    document.getElementById('cartDrawer').classList.remove('open');
}

function renderCarrito() {
    const body   = document.getElementById('cartBody');
    const footer = document.getElementById('cartFooter');
    if (!carrito.length) {
        body.innerHTML = `
            <div class="cart-empty">
                <span class="cart-empty-icon">🛒</span>
                <p><strong>Tu carrito está vacío</strong><br>Agrega productos del catálogo</p>
            </div>`;
        footer.innerHTML = '';
        return;
    }
    body.innerHTML = carrito.map(item => `
        <div class="cart-item">
            <div class="cart-item-emoji">${item.emoji}</div>
            <div class="cart-item-info">
                <div class="cart-item-name">${item.nombre}</div>
                <div class="cart-item-price">S/ ${item.precio.toFixed(2)}${item.peso ? ' · '+item.peso : ''}</div>
            </div>
            <div class="cart-qty">
                <button onclick="cambiarCantidad('${item.key}',-1)" aria-label="Quitar">−</button>
                <span>${item.qty}</span>
                <button onclick="cambiarCantidad('${item.key}',1)" aria-label="Agregar">+</button>
            </div>
        </div>`).join('');
    const total = obtenerTotal();
    footer.innerHTML = `
        <div class="cart-total">
            <span class="cart-total-label">Total del pedido</span>
            <span class="cart-total-amount">S/ ${total.toFixed(2)}</span>
        </div>
        <button class="wa-btn" onclick="enviarWhatsApp()">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.555 4.122 1.523 5.857L0 24l6.335-1.652A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.75c-1.875 0-3.63-.5-5.145-1.382l-.37-.219-3.756.98.998-3.648-.24-.38A9.69 9.69 0 012.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75z"/></svg>
            Enviar Pedido por WhatsApp
        </button>
        <button class="clear-cart-btn" onclick="vaciarCarrito()">Vaciar carrito</button>`;
}

function enviarWhatsApp() {
    if (!carrito.length) return;
    let msg = '🦅 *Pedido — El Halcón Dorado*\n\n';
    carrito.forEach((item, i) => {
        msg += `${i+1}. ${item.nombre}${item.peso ? ' ('+item.peso+')' : ''} ×${item.qty} — S/ ${(item.precio*item.qty).toFixed(2)}\n`;
    });
    msg += `\n💰 *TOTAL: S/ ${obtenerTotal().toFixed(2)}*\n\n¡Hola! Me gustaría hacer este pedido. 😊`;
    window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent(msg)}`, '_blank');
}

function contactarWA() {
    window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent('¡Hola! Tengo una consulta sobre sus productos 😊')}`, '_blank');
}

// ── RENDER ──
function renderProductos() {
    const grid = document.getElementById('productsGrid');
    const q    = (document.getElementById('searchInput').value || '').toLowerCase().trim();
    const lista = dbProductos.filter(p => {
        const catOk = filtroActivo === 'Todos' || p.categoria === filtroActivo;
        const qOk   = !q || p.nombre.toLowerCase().includes(q) || p.categoria.toLowerCase().includes(q);
        return catOk && qOk;
    });
    if (!lista.length) {
        grid.innerHTML = `<div class="empty-state"><div class="empty-state-icon">🔍</div><p>No se encontraron productos</p></div>`;
        return;
    }
    grid.innerHTML = lista.map((p, i) => `
        <div class="product-card fade-up" style="animation-delay:${i*0.04}s">
            <button class="admin-del-btn" onclick="event.stopPropagation();eliminarProducto('${p.id}')" aria-label="Eliminar producto">✕</button>
            <span class="product-cat-tag">${p.categoria}</span>
            <span class="product-emoji">${p.emoji}</span>
            <div class="product-name">${p.nombre}</div>
            <div class="product-weight">${p.peso}</div>
            <div class="product-price">S/ ${parseFloat(p.precio).toFixed(2)}</div>
            <button class="product-add-btn" onclick="agregarAlCarrito('${p.id}','producto')">+ Agregar</button>
        </div>`).join('');
}

function renderCombos() {
    const grid = document.getElementById('combosGrid');
    if (!dbCombos.length) {
        grid.innerHTML = `<div class="empty-state"><div class="empty-state-icon">🎁</div><p>No hay combos disponibles</p></div>`;
        return;
    }
    grid.innerHTML = dbCombos.map((c, i) => {
        const itemNames = (c.items || []).map(pid => {
            const p = dbProductos.find(x => x.id === pid);
            return p ? `${p.nombre} ${p.peso}` : '';
        }).filter(Boolean);
        const pct = c.precioOrig > 0 ? Math.round((1 - c.precioCombo/c.precioOrig)*100) : 0;
        return `
        <div class="combo-card fade-up" style="animation-delay:${i*0.08}s">
            ${pct > 0 ? `<div class="combo-discount">−${pct}%</div>` : ''}
            <span class="combo-save-pill">⚡ Oferta especial</span>
            <div class="combo-name">${c.nombre}</div>
            <div class="combo-desc">${c.desc || ''}</div>
            ${itemNames.length ? `<div class="combo-items">${itemNames.map(n=>`<span class="combo-item-tag">${n}</span>`).join('')}</div>` : ''}
            <div class="combo-footer">
                <div class="combo-prices">
                    ${c.precioOrig > 0 ? `<span class="combo-old">S/ ${parseFloat(c.precioOrig).toFixed(2)}</span>` : ''}
                    <span class="combo-new">S/ ${parseFloat(c.precioCombo).toFixed(2)}</span>
                </div>
                <button class="combo-add" onclick="agregarAlCarrito('${c.id}','combo')" aria-label="Agregar combo">+</button>
            </div>
        </div>`;
    }).join('');
}

function renderAll() {
    renderProductos();
    renderCombos();
    actualizarBadge();
}

// ── FILTERS ──
function setFilter(btn) {
    document.querySelectorAll('.filter-chip').forEach(c => c.classList.remove('active'));
    btn.classList.add('active');
    filtroActivo = btn.dataset.cat;
    renderProductos();
}

function filtrar() { renderProductos(); }

// ── ADMIN ──
function toggleAdmin() {
    if (!modoAdmin) {
        const pwd = prompt('🔐 Clave de administrador:');
        if (pwd === null) return;
        if (pwd !== 'LAPARCA956') { showToast('❌ Clave incorrecta'); return; }
    }
    modoAdmin = !modoAdmin;
    document.body.classList.toggle('admin-mode', modoAdmin);
    showToast(modoAdmin ? '✅ Modo admin activado' : '🔒 Admin desactivado');
}

function abrirModalProducto() {
    document.getElementById('modalProdTitle').textContent = 'Nuevo Producto';
    ['fProdId','fProdNombre','fProdPeso','fProdPrecio'].forEach(id => document.getElementById(id).value = '');
    document.getElementById('fProdCat').value   = 'Frescos';
    document.getElementById('fProdEmoji').value = '🧀';
    document.getElementById('modalProducto').classList.add('open');
}

function abrirModalCombo() {
    document.getElementById('modalComboTitle').textContent = 'Nuevo Combo';
    ['fComboId','fComboNombre','fComboDesc','fComboItems','fComboOrig','fComboPrice'].forEach(id => document.getElementById(id).value = '');
    document.getElementById('modalCombo').classList.add('open');
}

function cerrarModal(id) { document.getElementById(id).classList.remove('open'); }

function guardarProducto() {
    const nombre = document.getElementById('fProdNombre').value.trim();
    const peso   = document.getElementById('fProdPeso').value.trim();
    const precio = parseFloat(document.getElementById('fProdPrecio').value);
    if (!nombre || !peso || isNaN(precio)) { showToast('⚠️ Completa todos los campos'); return; }
    const id   = document.getElementById('fProdId').value || 'p' + Date.now();
    const prod = { id, nombre, peso, precio, categoria: document.getElementById('fProdCat').value, emoji: document.getElementById('fProdEmoji').value };
    const idx  = dbProductos.findIndex(p => p.id === id);
    if (idx >= 0) dbProductos[idx] = prod; else dbProductos.push(prod);
    save('halcon_productos', dbProductos);
    cerrarModal('modalProducto');
    renderProductos();
    showToast('✓ Producto guardado');
}

function guardarCombo() {
    const nombre = document.getElementById('fComboNombre').value.trim();
    const precio = parseFloat(document.getElementById('fComboPrice').value);
    if (!nombre || isNaN(precio)) { showToast('⚠️ Completa los campos requeridos'); return; }
    const id    = document.getElementById('fComboId').value || 'c' + Date.now();
    const combo = {
        id, nombre,
        desc:      document.getElementById('fComboDesc').value.trim(),
        items:     document.getElementById('fComboItems').value.split(',').map(s=>s.trim()).filter(Boolean),
        precioOrig: parseFloat(document.getElementById('fComboOrig').value) || 0,
        precioCombo: precio
    };
    const idx = dbCombos.findIndex(c => c.id === id);
    if (idx >= 0) dbCombos[idx] = combo; else dbCombos.push(combo);
    save('halcon_combos', dbCombos);
    cerrarModal('modalCombo');
    renderCombos();
    showToast('✓ Combo guardado');
}

function eliminarProducto(id) {
    if (!confirm('¿Eliminar este producto?')) return;
    dbProductos = dbProductos.filter(p => p.id !== id);
    save('halcon_productos', dbProductos);
    renderProductos();
    showToast('Producto eliminado');
}

// ── TOAST ──
let toastTimer;
function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    clearTimeout(toastTimer);
    toastTimer = setTimeout(() => t.classList.remove('show'), 2300);
}

// Close modals on backdrop click
document.querySelectorAll('.modal-overlay').forEach(m => {
    m.addEventListener('click', e => { if (e.target === m) m.classList.remove('open'); });
});

// ESC closes cart & modals
document.addEventListener('keydown', e => {
    if (e.key === 'Escape') {
        closeCart();
        document.querySelectorAll('.modal-overlay.open').forEach(m => m.classList.remove('open'));
    }
});

renderAll();
</script>
</body>
</html>
