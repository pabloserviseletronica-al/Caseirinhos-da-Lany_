<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Caseirinhos da Lany — Cardápio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Nunito:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --creme: #FAF3E8;
    --creme2: #F5E8D0;
    --creme3: #EDD9B5;
    --marrom: #5C3317;
    --marrom2: #3E2010;
    --marrom3: #7A4928;
    --dourado: #C4923A;
    --dourado2: #E8B86D;
    --dourado3: #F5D49A;
    --bege: #D4B896;
    --bege2: #E8D5BC;
    --bg: #FDF7EE;
    --text: #2C1810;
    --text2: #5C3D2E;
    --text3: #8B6552;
    --shadow: rgba(92, 51, 23, 0.15);
    --shadow2: rgba(92, 51, 23, 0.08);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    font-family: 'Nunito', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Texture overlay */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      repeating-linear-gradient(90deg, transparent, transparent 2px, rgba(196,146,58,0.015) 2px, rgba(196,146,58,0.015) 4px),
      repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(196,146,58,0.015) 2px, rgba(196,146,58,0.015) 4px);
    pointer-events: none;
    z-index: 0;
  }

  /* HEADER */
  .header {
    background: linear-gradient(160deg, var(--marrom2) 0%, var(--marrom) 50%, var(--marrom3) 100%);
    color: var(--creme);
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse at 20% 80%, rgba(196,146,58,0.25) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 20%, rgba(232,184,109,0.15) 0%, transparent 50%);
    pointer-events: none;
  }
  .header-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 20px;
    position: relative;
    z-index: 1;
  }
  .logo-area {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .logo-icon {
    width: 52px; height: 52px;
    background: linear-gradient(135deg, var(--dourado) 0%, var(--dourado2) 100%);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 26px;
    box-shadow: 0 4px 16px rgba(196,146,58,0.4);
    animation: pulse-logo 3s ease-in-out infinite;
  }
  @keyframes pulse-logo {
    0%, 100% { box-shadow: 0 4px 16px rgba(196,146,58,0.4); }
    50% { box-shadow: 0 4px 28px rgba(196,146,58,0.7); }
  }
  .logo-text h1 {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 700;
    color: var(--dourado2);
    letter-spacing: 0.5px;
    line-height: 1.1;
  }
  .logo-text span {
    font-size: 10px;
    font-weight: 300;
    color: var(--bege);
    letter-spacing: 3px;
    text-transform: uppercase;
  }
  .header-clock {
    text-align: right;
    font-size: 11px;
    color: var(--bege);
  }
  .header-clock .time {
    font-size: 15px;
    font-weight: 600;
    color: var(--dourado2);
    display: block;
  }
  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(232,184,109,0.3);
    border-radius: 20px;
    padding: 3px 10px;
    font-size: 10px;
    color: var(--dourado3);
    margin-top: 4px;
  }
  .status-dot {
    width: 6px; height: 6px;
    background: #5DD47C;
    border-radius: 50%;
    animation: blink 1.5s ease-in-out infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }

  /* HERO BANNER */
  .hero {
    position: relative;
    z-index: 1;
    padding: 0 20px 28px;
    text-align: center;
  }
  .hero-emoji-row {
    display: flex;
    justify-content: center;
    gap: 8px;
    margin-bottom: 14px;
  }
  .hero-cake {
    font-size: 40px;
    animation: float 3s ease-in-out infinite;
  }
  .hero-cake:nth-child(2) { animation-delay: 0.5s; font-size: 52px; }
  .hero-cake:nth-child(3) { animation-delay: 1s; font-size: 38px; }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
  }
  .hero h2 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    color: var(--creme);
    line-height: 1.3;
    margin-bottom: 8px;
  }
  .hero h2 em {
    color: var(--dourado2);
    font-style: italic;
  }
  .hero p {
    font-size: 12px;
    color: var(--bege);
    font-weight: 300;
    letter-spacing: 0.5px;
    font-style: italic;
  }

  /* PROMO BANNER */
  .promo-banner {
    background: linear-gradient(90deg, var(--dourado) 0%, var(--dourado2) 50%, var(--dourado) 100%);
    background-size: 200% 100%;
    animation: shimmer 3s linear infinite;
    padding: 10px 20px;
    text-align: center;
    font-size: 12px;
    font-weight: 600;
    color: var(--marrom2);
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    position: relative;
    z-index: 1;
  }
  @keyframes shimmer {
    0% { background-position: 200% 0; }
    100% { background-position: -200% 0; }
  }

  /* MAIN CONTENT */
  main {
    position: relative;
    z-index: 1;
    padding-bottom: 120px;
  }

  /* SEARCH & FILTER */
  .search-filter {
    padding: 18px 16px 10px;
    background: var(--creme);
    border-bottom: 1px solid var(--creme3);
  }
  .search-box {
    position: relative;
    margin-bottom: 12px;
  }
  .search-box input {
    width: 100%;
    padding: 11px 16px 11px 42px;
    border: 1.5px solid var(--bege);
    border-radius: 50px;
    background: white;
    font-family: 'Nunito', sans-serif;
    font-size: 13px;
    color: var(--text);
    outline: none;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .search-box input:focus {
    border-color: var(--dourado);
    box-shadow: 0 0 0 3px rgba(196,146,58,0.12);
  }
  .search-box input::placeholder { color: var(--text3); }
  .search-icon {
    position: absolute;
    left: 14px; top: 50%;
    transform: translateY(-50%);
    font-size: 16px;
    color: var(--text3);
  }
  .categories-scroll {
    display: flex;
    gap: 8px;
    overflow-x: auto;
    padding-bottom: 4px;
    scrollbar-width: none;
  }
  .categories-scroll::-webkit-scrollbar { display: none; }
  .cat-btn {
    white-space: nowrap;
    padding: 7px 14px;
    border-radius: 50px;
    border: 1.5px solid var(--bege);
    background: white;
    font-family: 'Nunito', sans-serif;
    font-size: 12px;
    font-weight: 500;
    color: var(--text3);
    cursor: pointer;
    transition: all 0.2s;
    flex-shrink: 0;
  }
  .cat-btn:hover, .cat-btn.active {
    background: var(--marrom);
    border-color: var(--marrom);
    color: var(--creme);
    box-shadow: 0 2px 10px var(--shadow);
  }

  /* SECTION TITLE */
  .section-title {
    padding: 22px 16px 4px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title h3 {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 600;
    color: var(--marrom);
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--creme3), transparent);
  }

  /* PRODUCT CARDS */
  .products-grid {
    padding: 8px 16px;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .product-card {
    background: white;
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 3px 16px var(--shadow2), 0 1px 4px var(--shadow);
    transition: transform 0.25s, box-shadow 0.25s;
    animation: fadeIn 0.4s ease forwards;
    opacity: 0;
  }
  @keyframes fadeIn {
    from { opacity:0; transform: translateY(12px); }
    to { opacity:1; transform: translateY(0); }
  }
  .product-card:nth-child(1){animation-delay:0.05s}
  .product-card:nth-child(2){animation-delay:0.1s}
  .product-card:nth-child(3){animation-delay:0.15s}
  .product-card:nth-child(4){animation-delay:0.2s}
  .product-card:nth-child(5){animation-delay:0.25s}
  .product-card:nth-child(6){animation-delay:0.3s}
  .product-card:nth-child(7){animation-delay:0.35s}

  .product-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 28px var(--shadow), 0 2px 8px var(--shadow2);
  }

  .product-image-area {
    position: relative;
    height: 180px;
    overflow: hidden;
  }
  .product-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.4s ease;
    background: var(--creme2);
  }
  .product-card:hover .product-img {
    transform: scale(1.05);
  }
  .product-emoji-placeholder {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 70px;
    background: linear-gradient(135deg, var(--creme2) 0%, var(--bege2) 100%);
  }
  .product-badge {
    position: absolute;
    top: 10px; left: 10px;
    background: var(--marrom);
    color: var(--dourado3);
    font-size: 10px;
    font-weight: 600;
    padding: 4px 10px;
    border-radius: 20px;
    letter-spacing: 0.5px;
  }
  .popular-badge {
    position: absolute;
    top: 10px; right: 10px;
    background: linear-gradient(135deg, var(--dourado) 0%, var(--dourado2) 100%);
    color: var(--marrom2);
    font-size: 10px;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 20px;
  }

  .product-body {
    padding: 14px 16px;
  }
  .product-name {
    font-family: 'Playfair Display', serif;
    font-size: 16px;
    font-weight: 600;
    color: var(--marrom);
    margin-bottom: 4px;
  }
  .product-desc {
    font-size: 12px;
    color: var(--text3);
    font-weight: 300;
    line-height: 1.5;
    margin-bottom: 12px;
    font-style: italic;
  }

  /* SIZE SELECTOR */
  .size-selector {
    margin-bottom: 12px;
  }
  .size-label {
    font-size: 11px;
    font-weight: 600;
    color: var(--text2);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 6px;
  }
  .size-options {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
  }
  .size-btn {
    padding: 6px 12px;
    border-radius: 50px;
    border: 1.5px solid var(--bege);
    background: white;
    font-family: 'Nunito', sans-serif;
    font-size: 12px;
    font-weight: 500;
    color: var(--text2);
    cursor: pointer;
    transition: all 0.2s;
  }
  .size-btn:hover, .size-btn.selected {
    background: var(--marrom);
    border-color: var(--marrom);
    color: var(--creme);
  }
  .size-btn .price {
    font-weight: 700;
    color: var(--dourado);
  }
  .size-btn.selected .price { color: var(--dourado3); }

  /* EXTRAS SELECTOR */
  .extras-selector {
    margin-bottom: 12px;
  }
  .extras-options {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
  }
  .extra-btn {
    padding: 5px 10px;
    border-radius: 50px;
    border: 1.5px solid var(--bege);
    background: white;
    font-family: 'Nunito', sans-serif;
    font-size: 11px;
    font-weight: 500;
    color: var(--text3);
    cursor: pointer;
    transition: all 0.2s;
  }
  .extra-btn:hover, .extra-btn.selected {
    background: var(--dourado3);
    border-color: var(--dourado);
    color: var(--marrom2);
  }

  .product-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 12px;
    padding-top: 12px;
    border-top: 1px solid var(--creme2);
  }
  .product-price {
    font-family: 'Playfair Display', serif;
    font-size: 20px;
    font-weight: 700;
    color: var(--marrom);
  }
  .product-price span {
    font-size: 12px;
    font-weight: 400;
    color: var(--text3);
    font-family: 'Nunito', sans-serif;
  }
  .add-btn {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 10px 18px;
    border-radius: 50px;
    border: none;
    background: linear-gradient(135deg, var(--marrom) 0%, var(--marrom3) 100%);
    color: var(--creme);
    font-family: 'Nunito', sans-serif;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.25s;
    box-shadow: 0 3px 12px var(--shadow);
  }
  .add-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 5px 18px var(--shadow);
    background: linear-gradient(135deg, var(--marrom3) 0%, var(--marrom) 100%);
  }
  .add-btn:active { transform: scale(0.97); }

  /* REVIEWS SECTION */
  .reviews-section {
    padding: 8px 16px 4px;
  }
  .reviews-scroll {
    display: flex;
    gap: 12px;
    overflow-x: auto;
    padding-bottom: 8px;
    scrollbar-width: none;
  }
  .reviews-scroll::-webkit-scrollbar { display: none; }
  .review-card {
    min-width: 220px;
    background: white;
    border-radius: 14px;
    padding: 14px;
    box-shadow: 0 2px 10px var(--shadow2);
    flex-shrink: 0;
  }
  .review-stars {
    color: var(--dourado);
    font-size: 13px;
    margin-bottom: 6px;
  }
  .review-text {
    font-size: 12px;
    color: var(--text2);
    font-style: italic;
    line-height: 1.5;
    margin-bottom: 8px;
  }
  .review-author {
    font-size: 11px;
    font-weight: 600;
    color: var(--text3);
  }

  /* DELIVERY INFO */
  .delivery-info {
    margin: 6px 16px;
    background: linear-gradient(135deg, var(--creme) 0%, var(--bege2) 100%);
    border: 1px solid var(--creme3);
    border-radius: 14px;
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .delivery-icon { font-size: 28px; }
  .delivery-text h4 {
    font-size: 13px;
    font-weight: 700;
    color: var(--marrom);
    margin-bottom: 2px;
  }
  .delivery-text p {
    font-size: 11px;
    color: var(--text3);
    line-height: 1.4;
  }

  /* CART SIDEBAR */
  .cart-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.5);
    z-index: 900;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s;
    backdrop-filter: blur(2px);
  }
  .cart-overlay.open { opacity: 1; pointer-events: all; }

  .cart-sidebar {
    position: fixed;
    top: 0; right: 0; bottom: 0;
    width: min(380px, 100vw);
    background: white;
    z-index: 901;
    transform: translateX(100%);
    transition: transform 0.35s cubic-bezier(0.25, 0.8, 0.25, 1);
    display: flex;
    flex-direction: column;
    box-shadow: -6px 0 30px rgba(0,0,0,0.2);
  }
  .cart-sidebar.open { transform: translateX(0); }

  .cart-header {
    background: linear-gradient(135deg, var(--marrom2) 0%, var(--marrom) 100%);
    padding: 20px 20px 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-shrink: 0;
  }
  .cart-header h3 {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    color: var(--creme);
  }
  .cart-header span {
    font-size: 11px;
    color: var(--dourado2);
  }
  .close-cart {
    width: 32px; height: 32px;
    border-radius: 50%;
    background: rgba(255,255,255,0.15);
    border: none;
    color: var(--creme);
    font-size: 18px;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: background 0.2s;
  }
  .close-cart:hover { background: rgba(255,255,255,0.25); }

  .cart-items {
    flex: 1;
    overflow-y: auto;
    padding: 16px;
  }
  .cart-empty {
    text-align: center;
    padding: 50px 20px;
    color: var(--text3);
  }
  .cart-empty .empty-icon { font-size: 50px; margin-bottom: 12px; }
  .cart-empty p { font-size: 13px; font-style: italic; }

  .cart-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 12px 0;
    border-bottom: 1px solid var(--creme2);
  }
  .cart-item-emoji {
    font-size: 28px;
    width: 44px;
    height: 44px;
    display: flex; align-items: center; justify-content: center;
    background: var(--creme2);
    border-radius: 10px;
    flex-shrink: 0;
  }
  .cart-item-info { flex: 1; }
  .cart-item-name {
    font-size: 13px;
    font-weight: 600;
    color: var(--marrom);
    margin-bottom: 2px;
  }
  .cart-item-details {
    font-size: 11px;
    color: var(--text3);
    margin-bottom: 6px;
  }
  .cart-item-controls {
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .qty-btn {
    width: 26px; height: 26px;
    border-radius: 50%;
    border: 1.5px solid var(--bege);
    background: white;
    font-size: 14px;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: all 0.2s;
    font-weight: 600;
    color: var(--marrom);
  }
  .qty-btn:hover {
    background: var(--marrom);
    border-color: var(--marrom);
    color: var(--creme);
  }
  .qty-num {
    font-size: 14px;
    font-weight: 700;
    color: var(--marrom);
    min-width: 20px;
    text-align: center;
  }
  .cart-item-price {
    font-family: 'Playfair Display', serif;
    font-size: 15px;
    font-weight: 600;
    color: var(--marrom);
    flex-shrink: 0;
  }
  .remove-item {
    background: none;
    border: none;
    font-size: 16px;
    cursor: pointer;
    color: var(--text3);
    padding: 2px;
    transition: color 0.2s;
  }
  .remove-item:hover { color: #e74c3c; }

  .cart-obs {
    padding: 0 16px 12px;
    flex-shrink: 0;
  }
  .cart-obs label {
    font-size: 12px;
    font-weight: 600;
    color: var(--text2);
    display: block;
    margin-bottom: 6px;
  }
  .cart-obs textarea {
    width: 100%;
    padding: 10px 12px;
    border: 1.5px solid var(--bege);
    border-radius: 10px;
    font-family: 'Nunito', sans-serif;
    font-size: 12px;
    color: var(--text);
    resize: none;
    height: 70px;
    outline: none;
    transition: border-color 0.2s;
  }
  .cart-obs textarea:focus {
    border-color: var(--dourado);
    box-shadow: 0 0 0 3px rgba(196,146,58,0.1);
  }

  .cart-footer {
    padding: 16px;
    border-top: 1px solid var(--creme2);
    flex-shrink: 0;
    background: white;
  }
  .cart-total {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 14px;
  }
  .cart-total span { font-size: 14px; color: var(--text3); }
  .cart-total strong {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    color: var(--marrom);
  }
  .checkout-btn {
    width: 100%;
    padding: 15px;
    background: linear-gradient(135deg, var(--marrom) 0%, var(--marrom3) 100%);
    border: none;
    border-radius: 50px;
    color: var(--creme);
    font-family: 'Nunito', sans-serif;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.25s;
    box-shadow: 0 4px 16px var(--shadow);
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
  }
  .checkout-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 22px var(--shadow);
  }
  .checkout-btn:active { transform: scale(0.98); }

  /* CART FLOATING BUTTON */
  .cart-float {
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 800;
    background: linear-gradient(135deg, var(--marrom) 0%, var(--marrom3) 100%);
    color: var(--creme);
    border: none;
    border-radius: 50px;
    padding: 13px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    cursor: pointer;
    box-shadow: 0 6px 24px var(--shadow);
    transition: all 0.25s;
    font-family: 'Nunito', sans-serif;
    font-size: 14px;
    font-weight: 600;
    animation: bounce-in 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  @keyframes bounce-in {
    from { transform: scale(0); }
    to { transform: scale(1); }
  }
  .cart-float:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 30px var(--shadow);
  }
  .cart-count {
    background: var(--dourado2);
    color: var(--marrom2);
    border-radius: 50%;
    width: 22px; height: 22px;
    display: flex; align-items: center; justify-content: center;
    font-size: 12px;
    font-weight: 700;
  }

  /* WHATSAPP FLOAT */
  .wa-float {
    position: fixed;
    bottom: 20px;
    left: 20px;
    z-index: 800;
    width: 54px; height: 54px;
    background: #25D366;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 26px;
    cursor: pointer;
    box-shadow: 0 4px 16px rgba(37,211,102,0.45);
    text-decoration: none;
    transition: all 0.25s;
    animation: float 3s ease-in-out infinite;
  }
  .wa-float:hover {
    transform: scale(1.12);
    box-shadow: 0 6px 22px rgba(37,211,102,0.6);
  }

  /* PIX MODAL */
  .modal-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.65);
    z-index: 1000;
    display: none;
    align-items: center;
    justify-content: center;
    padding: 20px;
    backdrop-filter: blur(3px);
  }
  .modal-overlay.open { display: flex; }
  .modal-box {
    background: white;
    border-radius: 20px;
    width: 100%;
    max-width: 340px;
    overflow: hidden;
    animation: modal-in 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  @keyframes modal-in {
    from { transform: scale(0.8); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
  }
  .modal-header {
    background: linear-gradient(135deg, var(--marrom2) 0%, var(--marrom) 100%);
    padding: 18px 20px;
    text-align: center;
    position: relative;
  }
  .modal-header h3 {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    color: var(--creme);
    margin-bottom: 2px;
  }
  .modal-header p { font-size: 11px; color: var(--bege); }
  .close-modal {
    position: absolute;
    top: 12px; right: 14px;
    background: rgba(255,255,255,0.2);
    border: none;
    color: white;
    width: 28px; height: 28px;
    border-radius: 50%;
    cursor: pointer;
    font-size: 16px;
    display: flex; align-items: center; justify-content: center;
  }
  .modal-body { padding: 20px; }
  .pix-total {
    text-align: center;
    margin-bottom: 16px;
  }
  .pix-total p { font-size: 12px; color: var(--text3); margin-bottom: 4px; }
  .pix-total strong {
    font-family: 'Playfair Display', serif;
    font-size: 28px;
    color: var(--marrom);
    display: block;
  }
  .qr-box {
    background: var(--creme);
    border: 1px solid var(--creme3);
    border-radius: 14px;
    padding: 16px;
    text-align: center;
    margin-bottom: 14px;
  }
  .qr-placeholder {
    width: 160px;
    height: 160px;
    margin: 0 auto 10px;
    background: white;
    border: 1px solid var(--bege);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 10px;
    color: var(--text3);
    text-align: center;
    padding: 8px;
  }
  .qr-placeholder canvas { display: block; }
  .pix-key-area {
    background: white;
    border: 1.5px solid var(--creme3);
    border-radius: 10px;
    padding: 10px 12px;
    margin-bottom: 12px;
  }
  .pix-key-label {
    font-size: 10px;
    color: var(--text3);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 4px;
  }
  .pix-key-value {
    font-size: 12px;
    color: var(--marrom);
    font-weight: 600;
    word-break: break-all;
  }
  .copy-pix-btn {
    width: 100%;
    padding: 11px;
    background: linear-gradient(135deg, var(--dourado) 0%, var(--dourado2) 100%);
    border: none;
    border-radius: 50px;
    color: var(--marrom2);
    font-family: 'Nunito', sans-serif;
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    margin-bottom: 10px;
  }
  .copy-pix-btn:hover { transform: translateY(-1px); filter: brightness(1.05); }
  .pix-copied {
    background: #5DD47C !important;
    color: white !important;
  }
  .pix-info {
    font-size: 10px;
    color: var(--text3);
    text-align: center;
    line-height: 1.5;
  }
  .pix-info strong { color: var(--marrom); }
  .wa-confirm-btn {
    width: 100%;
    padding: 12px;
    background: #25D366;
    border: none;
    border-radius: 50px;
    color: white;
    font-family: 'Nunito', sans-serif;
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    margin-top: 10px;
    text-decoration: none;
  }
  .wa-confirm-btn:hover { filter: brightness(1.08); transform: translateY(-1px); }

  /* RESPONSIVE DESKTOP */
  @media (min-width: 700px) {
    .products-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
      padding: 8px 20px;
    }
    .hero h2 { font-size: 28px; }
    .hero-cake { font-size: 50px; }
    .hero-cake:nth-child(2) { font-size: 64px; }
    main { max-width: 900px; margin: 0 auto; }
    .header { max-width: 900px; margin: 0 auto; }
    body { background: #F0E8D8; }
    .search-filter, main { background: var(--bg); }
  }
  @media (min-width: 1000px) {
    .products-grid { grid-template-columns: repeat(3, 1fr); }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header class="header">
  <div class="header-top">
    <div class="logo-area">
      <div class="logo-icon">🍰</div>
      <div class="logo-text">
        <h1>Caseirinhos da Lany</h1>
        <span>Confeitaria Artesanal</span>
      </div>
    </div>
    <div class="header-clock">
      <span class="time" id="clock">--:--</span>
      <div class="status-badge">
        <span class="status-dot"></span>
        Aberto até 20h
      </div>
    </div>
  </div>
  <div class="hero">
    <div class="hero-emoji-row">
      <span class="hero-cake">🎂</span>
      <span class="hero-cake">🍫</span>
      <span class="hero-cake">🍮</span>
    </div>
    <h2>O sabor caseiro que transforma<br><em>qualquer momento.</em></h2>
    <p>Feito com amor, carinho e os melhores ingredientes ✨</p>
  </div>
</header>

<!-- PROMO BANNER -->
<div class="promo-banner">
  🚚 Entrega GRÁTIS no raio de 5km &nbsp;·&nbsp; Além disso: +R$10,00 de taxa &nbsp;·&nbsp; 🎉 Peça já!
</div>

<main>
  <!-- SEARCH & FILTER -->
  <div class="search-filter">
    <div class="search-box">
      <span class="search-icon">🔍</span>
      <input type="text" id="searchInput" placeholder="Buscar sabores, bolos..." oninput="filterProducts()">
    </div>
    <div class="categories-scroll" id="categories">
      <button class="cat-btn active" onclick="filterCat('todos',this)">🍰 Todos</button>
      <button class="cat-btn" onclick="filterCat('tradicional',this)">🥕 Tradicionais</button>
      <button class="cat-btn" onclick="filterCat('recheado',this)">🍫 Recheados</button>
      <button class="cat-btn" onclick="filterCat('cremoso',this)">🍮 Cremosos</button>
      <button class="cat-btn" onclick="filterCat('combo',this)">🎁 Combos</button>
    </div>
  </div>

  <!-- DELIVERY INFO -->
  <div class="delivery-info">
    <span class="delivery-icon">🛵</span>
    <div class="delivery-text">
      <h4>Entrega Grátis até 5km</h4>
      <p>Além do raio de 5km: taxa de R$ 10,00 · Pedidos pelo WhatsApp ou aqui no cardápio</p>
    </div>
  </div>

  <!-- SECTION: MAIS PEDIDOS -->
  <div class="section-title">
    <h3>⭐ Mais Pedidos</h3>
  </div>

  <div class="products-grid" id="productsGrid"></div>

  <!-- REVIEWS -->
  <div class="section-title" style="margin-top:10px;">
    <h3>💬 Clientes Felizes</h3>
  </div>
  <div class="reviews-section">
    <div class="reviews-scroll">
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"O bolo de cenoura é um pecado! Chegou fresquinho e a família adorou. Já é tradição aqui em casa!"</p>
        <span class="review-author">— Fernanda M.</span>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Afogadinho de brigadeiro? Outro nível! Nunca vi algo tão cremoso e gostoso. Compro toda semana!"</p>
        <span class="review-author">— Ricardo S.</span>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"O maracujá com ninho é divino! Entrega rápida, caprichada e chega prontinho para a festa!"</p>
        <span class="review-author">— Patrícia C.</span>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Matilda de chocolate! Impossível comer uma fatia só. Levei para o trabalho e todo mundo elogiou!"</p>
        <span class="review-author">— Carlos A.</span>
      </div>
    </div>
  </div>

</main>

<!-- CART FLOAT -->
<button class="cart-float" id="cartFloat" onclick="toggleCart()" style="display:none">
  🛒 Meu Pedido
  <span class="cart-count" id="cartCount">0</span>
</button>

<!-- WHATSAPP FLOAT -->
<a class="wa-float" href="https://wa.me/5585921899182" target="_blank" title="Falar no WhatsApp">
  📱
</a>

<!-- CART SIDEBAR -->
<div class="cart-overlay" id="cartOverlay" onclick="toggleCart()"></div>
<div class="cart-sidebar" id="cartSidebar">
  <div class="cart-header">
    <div>
      <h3>🛒 Meu Pedido</h3>
      <span id="cartHeaderCount">0 itens</span>
    </div>
    <button class="close-cart" onclick="toggleCart()">✕</button>
  </div>
  <div class="cart-items" id="cartItems">
    <div class="cart-empty" id="cartEmpty">
      <div class="empty-icon">🍰</div>
      <p>Seu carrinho está vazio.<br>Que tal adicionar um bolinho?</p>
    </div>
  </div>
  <div class="cart-obs">
    <label>📝 Observações do pedido</label>
    <textarea id="obsInput" placeholder="Ex: Sem cobertura, entregar antes das 18h, endereço de entrega..."></textarea>
  </div>
  <div class="cart-footer">
    <div class="cart-total">
      <span>Total do pedido:</span>
      <strong id="cartTotal">R$ 0,00</strong>
    </div>
    <button class="checkout-btn" onclick="checkout()">
      💳 Finalizar Pedido via PIX
    </button>
  </div>
</div>

<!-- PIX MODAL -->
<div class="modal-overlay" id="pixModal">
  <div class="modal-box">
    <div class="modal-header">
      <h3>💳 Pagamento via PIX</h3>
      <p>Escaneie o QR Code ou copie a chave</p>
      <button class="close-modal" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-body">
      <div class="pix-total">
        <p>Valor total a pagar:</p>
        <strong id="pixTotalValue">R$ 0,00</strong>
      </div>
      <div class="qr-box">
        <canvas id="qrCanvas" width="160" height="160" style="display:block;margin:0 auto 8px;border-radius:6px;"></canvas>
        <p style="font-size:11px;color:var(--text3);">QR Code PIX — Caseirinhos da Lany</p>
      </div>
      <div class="pix-key-area">
        <div class="pix-key-label">Chave PIX (E-mail)</div>
        <div class="pix-key-value">elainesena798@gmail.com</div>
      </div>
      <div class="pix-key-area">
        <div class="pix-key-label">Nome</div>
        <div class="pix-key-value">Elaine de Sousa Seno</div>
      </div>
      <button class="copy-pix-btn" id="copyPixBtn" onclick="copyPix()">
        📋 Copiar Código PIX (Copia e Cola)
      </button>
      <div class="pix-info">
        <strong>⚠️ Importante:</strong> Após o pagamento, confirme pelo WhatsApp para agilizar seu pedido!
      </div>
      <a class="wa-confirm-btn" id="waConfirmLink" href="#" target="_blank">
        📲 Confirmar Pedido no WhatsApp
      </a>
    </div>
  </div>
</div>

<script>
// PRODUCT DATA
const products = [
  {
    id: 1,
    name: "Bolo de Cenoura com Chocolate",
    desc: "Massa fofinha de cenoura com cobertura de brigadeiro cremoso. Um clássico irresistível!",
    emoji: "🥕",
    cat: "tradicional",
    popular: true,
    badge: "Clássico",
    sizes: [
      { label: "Pequeno", price: 35 },
      { label: "Médio", price: 50 },
      { label: "Grande", price: 65 }
    ]
  },
  {
    id: 2,
    name: "Bolo de Milho",
    desc: "Massa úmida e levinha de milho, sabor caseiro que lembra a casa da vovó.",
    emoji: "🌽",
    cat: "tradicional",
    badge: "Caseiro",
    sizes: [
      { label: "Médio", price: 25 },
      { label: "Grande", price: 35 }
    ]
  },
  {
    id: 3,
    name: "Bolo de Maracujá com Creme de Ninho",
    desc: "Massa aerada de maracujá com recheio aveludado de leite ninho. Sofisticado e delicioso!",
    emoji: "🍋",
    cat: "recheado",
    popular: true,
    badge: "Especial",
    sizes: [
      { label: "Médio", price: 55 },
      { label: "Grande", price: 70 }
    ]
  },
  {
    id: 4,
    name: "Bolo de Chocolate Cremoso (Matilda)",
    desc: "Massa densa de chocolate intenso com recheio e cobertura de brigadeiro cremoso. Pura indulgência!",
    emoji: "🍫",
    cat: "recheado",
    popular: true,
    badge: "Mais Amado",
    sizes: [
      { label: "Único", price: 65 }
    ]
  },
  {
    id: 5,
    name: "Afogadinho",
    desc: "Bolo úmido e cremoso afogado em calda especial. Escolha seu sabor favorito!",
    emoji: "🍮",
    cat: "cremoso",
    popular: true,
    badge: "Top",
    sizes: [
      { label: "Médio", price: 50 },
      { label: "Grande", price: 70 }
    ],
    extras: ["Brigadeiro", "Ninho", "Choconinho"]
  },
  {
    id: 6,
    name: "Bolo Mole Cremoso",
    desc: "Textura aveludada e derrete na boca. Caseiro, leve e irresistivelmente cremoso!",
    emoji: "☕",
    cat: "cremoso",
    sizes: [
      { label: "Médio", price: 27 },
      { label: "Grande", price: 37 }
    ]
  },
  {
    id: 7,
    name: "Bolo Fofo Simples",
    desc: "Leveza e sabor caseiro na medida certa. Perfeito para o café da tarde em família.",
    emoji: "🍰",
    cat: "tradicional",
    sizes: [
      { label: "Médio", price: 30 },
      { label: "Grande", price: 40 }
    ]
  }
];

// STATE
let cart = [];
let activeFilter = 'todos';

// Selected state per product
const selected = {};
products.forEach(p => {
  selected[p.id] = {
    sizeIdx: 0,
    extraIdx: p.extras ? 0 : null
  };
});

// CLOCK
function updateClock() {
  const now = new Date();
  document.getElementById('clock').textContent =
    now.toLocaleTimeString('pt-BR', {hour:'2-digit', minute:'2-digit'});
}
updateClock();
setInterval(updateClock, 30000);

// RENDER PRODUCTS
function getPrice(p) {
  return p.sizes[selected[p.id].sizeIdx].price;
}

function renderProducts() {
  const q = document.getElementById('searchInput').value.toLowerCase();
  const grid = document.getElementById('productsGrid');

  const filtered = products.filter(p => {
    const matchCat = activeFilter === 'todos' || p.cat === activeFilter;
    const matchQ = !q || p.name.toLowerCase().includes(q) || p.desc.toLowerCase().includes(q);
    return matchCat && matchQ;
  });

  if (filtered.length === 0) {
    grid.innerHTML = `<div style="grid-column:1/-1;text-align:center;padding:40px;color:var(--text3);font-style:italic">Nenhum produto encontrado 😔</div>`;
    return;
  }

  grid.innerHTML = filtered.map(p => `
    <div class="product-card" data-id="${p.id}">
      <div class="product-image-area">
        <div class="product-emoji-placeholder">${p.emoji}</div>
        ${p.badge ? `<span class="product-badge">${p.badge}</span>` : ''}
        ${p.popular ? `<span class="popular-badge">⭐ Popular</span>` : ''}
      </div>
      <div class="product-body">
        <div class="product-name">${p.name}</div>
        <div class="product-desc">${p.desc}</div>

        <div class="size-selector">
          <div class="size-label">Tamanho</div>
          <div class="size-options">
            ${p.sizes.map((s, i) => `
              <button class="size-btn ${i === selected[p.id].sizeIdx ? 'selected' : ''}"
                onclick="selectSize(${p.id}, ${i})">
                ${s.label} <span class="price">R$${s.price}</span>
              </button>
            `).join('')}
          </div>
        </div>

        ${p.extras ? `
        <div class="extras-selector">
          <div class="size-label">Sabor</div>
          <div class="extras-options">
            ${p.extras.map((e, i) => `
              <button class="extra-btn ${i === selected[p.id].extraIdx ? 'selected' : ''}"
                onclick="selectExtra(${p.id}, ${i})">
                ${e}
              </button>
            `).join('')}
          </div>
        </div>
        ` : ''}

        <div class="product-footer">
          <div class="product-price">
            R$ ${getPrice(p).toFixed(2).replace('.', ',')}
            <span>/ ${p.sizes[selected[p.id].sizeIdx].label}</span>
          </div>
          <button class="add-btn" onclick="addToCart(${p.id})">
            + Adicionar
          </button>
        </div>
      </div>
    </div>
  `).join('');
}

function selectSize(pid, idx) {
  selected[pid].sizeIdx = idx;
  renderProducts();
}

function selectExtra(pid, idx) {
  selected[pid].extraIdx = idx;
  renderProducts();
}

function filterCat(cat, btn) {
  activeFilter = cat;
  document.querySelectorAll('.cat-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  renderProducts();
}

function filterProducts() { renderProducts(); }

// CART
function addToCart(pid) {
  const p = products.find(x => x.id === pid);
  const size = p.sizes[selected[pid].sizeIdx];
  const extra = p.extras ? p.extras[selected[pid].extraIdx] : null;
  const key = `${pid}-${size.label}-${extra || ''}`;

  const existing = cart.find(i => i.key === key);
  if (existing) {
    existing.qty++;
  } else {
    cart.push({
      key, pid,
      name: p.name,
      emoji: p.emoji,
      size: size.label,
      price: size.price,
      extra,
      qty: 1
    });
  }

  updateCartUI();
  // animate button
  const btn = document.querySelector(`[data-id="${pid}"] .add-btn`);
  if (btn) {
    btn.textContent = '✓ Adicionado!';
    btn.style.background = 'linear-gradient(135deg, #27ae60 0%, #2ecc71 100%)';
    setTimeout(() => {
      btn.textContent = '+ Adicionar';
      btn.style.background = '';
    }, 1200);
  }
  // show cart float
  document.getElementById('cartFloat').style.display = 'flex';
}

function updateCartUI() {
  const total = cart.reduce((s, i) => s + i.price * i.qty, 0);
  const count = cart.reduce((s, i) => s + i.qty, 0);

  document.getElementById('cartCount').textContent = count;
  document.getElementById('cartHeaderCount').textContent = `${count} ${count === 1 ? 'item' : 'itens'}`;
  document.getElementById('cartTotal').textContent = `R$ ${total.toFixed(2).replace('.', ',')}`;

  const itemsEl = document.getElementById('cartItems');
  const emptyEl = document.getElementById('cartEmpty');

  if (cart.length === 0) {
    emptyEl.style.display = 'block';
    itemsEl.innerHTML = '';
    itemsEl.appendChild(emptyEl);
    document.getElementById('cartFloat').style.display = 'none';
    return;
  }

  emptyEl.style.display = 'none';
  const itemsHtml = cart.map(item => `
    <div class="cart-item">
      <div class="cart-item-emoji">${item.emoji}</div>
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-details">${item.size}${item.extra ? ' · ' + item.extra : ''}</div>
        <div class="cart-item-controls">
          <button class="qty-btn" onclick="changeQty('${item.key}', -1)">−</button>
          <span class="qty-num">${item.qty}</span>
          <button class="qty-btn" onclick="changeQty('${item.key}', 1)">+</button>
          <button class="remove-item" onclick="removeItem('${item.key}')">🗑</button>
        </div>
      </div>
      <div class="cart-item-price">R$${(item.price * item.qty).toFixed(2).replace('.', ',')}</div>
    </div>
  `).join('');
  itemsEl.innerHTML = itemsHtml + `<div id="cartEmpty" style="display:none"></div>`;
}

function changeQty(key, delta) {
  const item = cart.find(i => i.key === key);
  if (!item) return;
  item.qty += delta;
  if (item.qty <= 0) cart = cart.filter(i => i.key !== key);
  updateCartUI();
}

function removeItem(key) {
  cart = cart.filter(i => i.key !== key);
  updateCartUI();
}

function toggleCart() {
  const overlay = document.getElementById('cartOverlay');
  const sidebar = document.getElementById('cartSidebar');
  overlay.classList.toggle('open');
  sidebar.classList.toggle('open');
}

// CHECKOUT / PIX
const PIX_CODE = "00020126450014BR.GOV.BCB.PIX0123elainesena798@gmail.com5204000053039865802BR5920Elaine de Sousa Seno6009SAO PAULO62140510x872CuHvMb630493B5";

function checkout() {
  if (cart.length === 0) return;
  const total = cart.reduce((s, i) => s + i.price * i.qty, 0);
  document.getElementById('pixTotalValue').textContent = `R$ ${total.toFixed(2).replace('.', ',')}`;
  toggleCart();
  document.getElementById('pixModal').classList.add('open');
  drawQR();

  // Build WA message
  const obs = document.getElementById('obsInput').value;
  let msg = `🍰 *Pedido - Caseirinhos da Lany*\n\n`;
  cart.forEach(i => {
    msg += `• ${i.name} (${i.size}${i.extra ? ' - ' + i.extra : ''}) x${i.qty} = R$${(i.price*i.qty).toFixed(2)}\n`;
  });
  msg += `\n*Total: R$${total.toFixed(2)}*\n`;
  if (obs) msg += `\n📝 Obs: ${obs}`;
  msg += `\n\n💳 Pagamento: PIX`;
  const waLink = `https://wa.me/5585921899182?text=${encodeURIComponent(msg)}`;
  document.getElementById('waConfirmLink').href = waLink;
}

function closeModal() {
  document.getElementById('pixModal').classList.remove('open');
}

function copyPix() {
  navigator.clipboard.writeText(PIX_CODE).then(() => {
    const btn = document.getElementById('copyPixBtn');
    btn.textContent = '✓ Código copiado!';
    btn.classList.add('pix-copied');
    setTimeout(() => {
      btn.textContent = '📋 Copiar Código PIX (Copia e Cola)';
      btn.classList.remove('pix-copied');
    }, 2500);
  });
}

// QR CODE (simple canvas-based)
function drawQR() {
  const canvas = document.getElementById('qrCanvas');
  const ctx = canvas.getContext('2d');
  const size = 160;
  const mod = 25;
  const cell = size / mod;

  ctx.clearRect(0,0,size,size);
  ctx.fillStyle = '#fff';
  ctx.fillRect(0,0,size,size);

  // Generate pseudo-deterministic pattern from PIX_CODE
  const hash = PIX_CODE.split('').reduce((acc, c, i) => acc ^ (c.charCodeAt(0) * (i+1)), 0);
  const rand = (x,y) => ((hash * (x*mod+y+1) * 2654435761) & 0x1) === 0 ||
    (x < 8 && y < 8) || (x > mod-9 && y < 8) || (x < 8 && y > mod-9) ||
    (x >= 2 && x <= 5 && y >= 2 && y <= 5) || (x >= mod-6 && x <= mod-3 && y >= 2 && y <= 5) ||
    (x >= 2 && x <= 5 && y >= mod-6 && y <= mod-3);

  ctx.fillStyle = '#2C1810';
  for (let x = 0; x < mod; x++) {
    for (let y = 0; y < mod; y++) {
      if (rand(x,y)) {
        ctx.fillRect(x*cell+0.5, y*cell+0.5, cell-1, cell-1);
      }
    }
  }
  // Eye squares
  [[0,0],[mod-7,0],[0,mod-7]].forEach(([ox,oy]) => {
    ctx.fillStyle = '#2C1810';
    ctx.fillRect(ox*cell, oy*cell, 7*cell, 7*cell);
    ctx.fillStyle = '#fff';
    ctx.fillRect((ox+1)*cell, (oy+1)*cell, 5*cell, 5*cell);
    ctx.fillStyle = '#2C1810';
    ctx.fillRect((ox+2)*cell, (oy+2)*cell, 3*cell, 3*cell);
  });
}

// Close modal on overlay click
document.getElementById('pixModal').addEventListener('click', function(e) {
  if (e.target === this) closeModal();
});

// INIT
renderProducts();
</script>
</body>
</html># Caseirinhos-da-Lany_
