
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.5, user-scalable=yes">
  <title>Mera‑Gide · Green Ayurveda</title>
  <!-- Font Awesome for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      background: #f8fbf7;
      color: #1e2f23;
      line-height: 1.5;
    }

    /* natural green palette */
    :root {
      --green-dark: #1e4a2b;
      --green-mid: #2f6b3a;
      --green-light: #5d8f6b;
      --green-pale: #e2f0e0;
      --green-bg: #f0f7ee;
      --gold: #b68b40;
      --cream: #fcf9f2;
      --white: #ffffff;
      --shadow: 0 8px 24px rgba(30, 50, 30, 0.08);
      --radius: 24px;
      --radius-sm: 16px;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      max-width: 1300px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* logo & branding */
    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      font-size: 1.8rem;
      letter-spacing: -0.5px;
      color: var(--green-dark);
    }

    .logo i {
      font-size: 2.2rem;
      color: var(--green-mid);
      background: var(--green-pale);
      padding: 8px;
      border-radius: 50%;
    }

    .logo span {
      background: linear-gradient(145deg, #1e4a2b, #3d7a4a);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* header / nav */
    .navbar {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      padding: 16px 0;
      border-bottom: 1px solid rgba(30, 74, 43, 0.08);
      background: var(--white);
      border-radius: 0 0 var(--radius) var(--radius);
      box-shadow: var(--shadow);
      margin-bottom: 24px;
      padding-left: 24px;
      padding-right: 24px;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      font-weight: 500;
      font-size: 0.95rem;
    }

    .nav-links a {
      padding: 6px 4px;
      border-bottom: 2px solid transparent;
      transition: 0.2s;
    }

    .nav-links a:hover {
      border-bottom-color: var(--green-mid);
      color: var(--green-dark);
    }

    .nav-actions {
      display: flex;
      gap: 16px;
      align-items: center;
    }

    .btn {
      display: inline-block;
      background: var(--green-mid);
      color: white;
      padding: 10px 22px;
      border-radius: 60px;
      font-weight: 600;
      font-size: 0.9rem;
      border: none;
      cursor: pointer;
      transition: all 0.2s;
      text-align: center;
      box-shadow: 0 4px 8px rgba(47, 107, 58, 0.15);
    }

    .btn-outline {
      background: transparent;
      color: var(--green-dark);
      border: 1.5px solid var(--green-mid);
      box-shadow: none;
    }

    .btn-gold {
      background: var(--gold);
      box-shadow: 0 4px 8px rgba(182, 139, 64, 0.2);
    }

    .btn-sm {
      padding: 6px 16px;
      font-size: 0.8rem;
    }

    .btn:hover {
      transform: translateY(-2px);
      opacity: 0.9;
    }

    /* hero */
    .hero {
      background: linear-gradient(135deg, #eaf7e6 0%, #d4e8d0 100%);
      border-radius: var(--radius);
      padding: 48px 40px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 40px;
      box-shadow: var(--shadow);
    }

    .hero-content h1 {
      font-size: 2.6rem;
      font-weight: 700;
      color: var(--green-dark);
      max-width: 500px;
    }

    .hero-content p {
      font-size: 1.1rem;
      color: #2b4d34;
      margin: 16px 0 24px;
      max-width: 440px;
    }

    .hero-image i {
      font-size: 10rem;
      color: var(--green-mid);
      opacity: 0.5;
      background: rgba(255,255,255,0.3);
      padding: 20px;
      border-radius: 50%;
    }

    /* sections */
    .section-title {
      font-size: 1.8rem;
      font-weight: 600;
      color: var(--green-dark);
      margin: 40px 0 20px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .section-title i {
      color: var(--gold);
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 24px;
      margin-bottom: 40px;
    }

    .product-card {
      background: var(--white);
      border-radius: var(--radius-sm);
      padding: 18px 14px 20px;
      box-shadow: var(--shadow);
      transition: 0.2s;
      border: 1px solid rgba(47, 107, 58, 0.06);
      display: flex;
      flex-direction: column;
    }

    .product-card:hover {
      transform: scale(1.01);
    }

    .product-img {
      background: var(--green-pale);
      height: 150px;
      border-radius: var(--radius-sm);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3.5rem;
      color: var(--green-mid);
      margin-bottom: 12px;
    }

    .product-name {
      font-weight: 600;
      font-size: 1rem;
    }

    .product-price {
      font-weight: 700;
      color: var(--green-dark);
      margin: 6px 0;
    }

    .product-actions {
      display: flex;
      gap: 8px;
      margin-top: 12px;
      flex-wrap: wrap;
    }

    .badge {
      background: var(--green-pale);
      color: var(--green-dark);
      padding: 2px 12px;
      border-radius: 40px;
      font-size: 0.7rem;
      font-weight: 600;
    }

    /* seller panel */
    .seller-panel {
      background: var(--white);
      border-radius: var(--radius);
      padding: 32px;
      box-shadow: var(--shadow);
      margin: 40px 0;
      border-left: 8px solid var(--gold);
    }

    .seller-panel h2 {
      display: flex;
      gap: 12px;
      align-items: center;
      color: var(--green-dark);
    }

    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      margin: 24px 0;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    .form-group input, .form-group select, .form-group textarea {
      padding: 12px 14px;
      border: 1px solid #cfdfd0;
      border-radius: 40px;
      font-size: 0.95rem;
      background: var(--cream);
    }

    .form-group textarea {
      border-radius: 20px;
      resize: vertical;
    }

    .status-badge {
      display: inline-block;
      padding: 4px 16px;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.8rem;
    }

    .status-pending { background: #fdebb3; color: #7a6400; }
    .status-approved { background: #b8e0b8; color: #1f5420; }
    .status-rejected { background: #fccccc; color: #a13d3d; }

    /* admin */
    .admin-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
      gap: 18px;
      background: var(--white);
      padding: 24px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      margin: 20px 0;
    }

    .admin-stat {
      background: var(--green-pale);
      border-radius: var(--radius-sm);
      padding: 16px;
      text-align: center;
      font-weight: 500;
    }

    .admin-stat i {
      font-size: 2rem;
      color: var(--green-mid);
    }

    /* footer */
    .footer {
      background: #1a2d1e;
      color: #d4e2d0;
      padding: 40px 0 20px;
      margin-top: 50px;
      border-radius: var(--radius) var(--radius) 0 0;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
      gap: 30px;
    }

    .footer a {
      color: #b8d0b5;
      display: block;
      margin: 6px 0;
    }

    .footer a:hover { color: white; }

    /* responsive */
    @media (max-width: 800px) {
      .navbar { flex-direction: column; align-items: stretch; gap: 12px; }
      .nav-links { justify-content: center; }
      .hero { flex-direction: column; text-align: center; }
      .hero-content h1 { font-size: 2rem; }
      .form-grid { grid-template-columns: 1fr; }
      .product-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); }
    }

    @media (max-width: 480px) {
      .container { padding: 0 12px; }
      .btn { padding: 8px 14px; font-size: 0.8rem; }
      .logo { font-size: 1.4rem; }
    }

    /* misc */
    .flex { display: flex; gap: 12px; flex-wrap: wrap; align-items: center; }
    .mt-2 { margin-top: 16px; }
    .mb-2 { margin-bottom: 16px; }
    .text-muted { color: #4d6b52; }
    .border-bottom { border-bottom: 1px solid #dde8db; padding-bottom: 16px; }
    .review { background: var(--cream); border-radius: var(--radius-sm); padding: 16px; margin: 8px 0; }
  </style>
</head>
<body>
<div class="container">

  <!-- header -->
  <header class="navbar">
    <div class="logo">
      <i class="fas fa-leaf"></i>
      <span>Mera‑Gide</span>
    </div>
    <nav class="nav-links">
      <a href="#">Home</a>
      <a href="#">Shop</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
      <a href="#">Seller</a>
    </nav>
    <div class="nav-actions">
      <a href="#" class="btn btn-sm"><i class="fas fa-search"></i></a>
      <a href="#" class="btn btn-sm"><i class="fas fa-shopping-cart"></i></a>
      <a href="#" class="btn btn-sm btn-outline">Login</a>
      <a href="#" class="btn btn-sm btn-gold">Become a Seller</a>
    </div>
  </header>

  <!-- hero -->
  <section class="hero">
    <div class="hero-content">
      <h1>Pure Green Ayurveda</h1>
      <p>Herbal wellness crafted by nature — discover Mera‑Gide’s authentic Ayurvedic treasures.</p>
      <a href="#" class="btn btn-gold"><i class="fas fa-store"></i> Shop Now</a>
    </div>
    <div class="hero-image">
      <i class="fas fa-seedling"></i>
    </div>
  </section>

  <!-- featured + latest products -->
  <div class="section-title"><i class="fas fa-star"></i> Featured Products</div>
  <div class="product-grid">
    <div class="product-card"><div class="product-img"><i class="fas fa-mortar-pestle"></i></div><div class="product-name">Ashwagandha Root</div><div class="product-price">₹499 <span class="badge">-20%</span></div><div class="product-actions"><a href="#" class="btn btn-sm">Buy Now</a><a href="#" class="btn btn-sm btn-outline">Add to Cart</a></div></div>
    <div class="product-card"><div class="product-img"><i class="fas fa-flask"></i></div><div class="product-name">Tulsi Drops</div><div class="product-price">₹350</div><div class="product-actions"><a href="#" class="btn btn-sm">Buy Now</a><a href="#" class="btn btn-sm btn-outline">Add to Cart</a></div></div>
    <div class="product-card"><div class="product-img"><i class="fas fa-spa"></i></div><div class="product-name">Neem & Aloe Gel</div><div class="product-price">₹275</div><div class="product-actions"><a href="#" class="btn btn-sm">Buy Now</a><a href="#" class="btn btn-sm btn-outline">Add to Cart</a></div></div>
  </div>

  <div class="section-title"><i class="fas fa-clock"></i> Latest Arrivals</div>
  <div class="product-grid">
    <div class="product-card"><div class="product-img"><i class="fas fa-oil-can"></i></div><div class="product-name">Sesame Massage Oil</div><div class="product-price">₹620</div><div class="product-actions"><a href="#" class="btn btn-sm">Buy Now</a><a href="#" class="btn btn-sm btn-outline">Add to Cart</a></div></div>
    <div class="product-card"><div class="product-img"><i class="fas fa-hand-holding-heart"></i></div><div class="product-name">Brahmi Capsules</div><div class="product-price">₹540</div><div class="product-actions"><a href="#" class="btn btn-sm">Buy Now</a><a href="#" class="btn btn-sm btn-outline">Add to Cart</a></div></div>
  </div>

  <!-- Seller Panel (Add product) -->
  <div class="seller-panel">
    <h2><i class="fas fa-user-plus"></i> Seller Dashboard · Add Product</h2>
    <div class="flex"><span class="badge">Pending</span><span class="badge" style="background:#b8e0b8;">Approved</span><span class="badge" style="background:#fccccc;">Rejected</span></div>
    <div class="form-grid">
      <div class="form-group"><label>Product Name</label><input type="text" value="Triphala Powder" placeholder="e.g. Triphala"></div>
      <div class="form-group"><label>Category</label><select><option>Herbal Supplements</option><option>Personal Care</option><option>Wellness</option></select></div>
      <div class="form-group"><label>Price (₹)</label><input type="number" value="450"></div>
      <div class="form-group"><label>Discount Price</label><input type="number" value="399"></div>
      <div class="form-group"><label>Stock</label><input type="number" value="120"></div>
      <div class="form-group"><label>Seller/Brand</label><input type="text" value="GreenRoot Ayurveda"></div>
      <div class="form-group"><label>Description</label><textarea rows="2">Pure Triphala for digestion & wellness.</textarea></div>
      <div class="form-group"><label>Benefits</label><textarea rows="2">Supports gut health, natural detox</textarea></div>
      <div class="form-group"><label>Ingredients</label><textarea rows="2">Amalaki, Bibhitaki, Haritaki</textarea></div>
      <div class="form-group"><label>Usage Instructions</label><textarea rows="2">Take 1 tsp with warm water</textarea></div>
      <div class="form-group"><label>Upload Images</label><input type="file" multiple accept="image/*"></div>
    </div>
    <div class="flex"><a href="#" class="btn btn-gold"><i class="fas fa-cloud-upload-alt"></i> Submit Product</a> <span class="text-muted">(for admin approval)</span></div>
  </div>

  <!-- admin dashboard snippet -->
  <div class="section-title"><i class="fas fa-user-shield"></i> Admin Dashboard</div>
  <div class="admin-grid">
    <div class="admin-stat"><i class="fas fa-store"></i> 12 Sellers</div>
    <div class="admin-stat"><i class="fas fa-boxes"></i> 48 Products</div>
    <div class="admin-stat"><i class="fas fa-tags"></i> 8 Categories</div>
    <div class="admin-stat"><i class="fas fa-shipping-fast"></i> 23 Orders</div>
    <div class="admin-stat"><i class="fas fa-edit"></i> Approve / Reject</div>
    <div class="admin-stat"><i class="fas fa-images"></i> Manage Banners</div>
  </div>
  <div class="flex"><a href="#" class="btn btn-sm">Manage Products</a><a href="#" class="btn btn-sm btn-outline">View Sellers</a><a href="#" class="btn btn-sm btn-outline">Orders</a></div>

  <!-- customer reviews -->
  <div class="section-title"><i class="fas fa-comment-dots"></i> Customer Reviews</div>
  <div class="review"><i class="fas fa-user-circle"></i> <strong>Priya S.</strong> “Authentic products, fast delivery. Love the Brahmi capsules!” ⭐⭐⭐⭐⭐</div>
  <div class="review"><i class="fas fa-user-circle"></i> <strong>Arjun M.</strong> “The Triphala powder is high quality. Mera-Gide is my go-to store.” ⭐⭐⭐⭐</div>

  <!-- about -->
  <div class="section-title"><i class="fas fa-info-circle"></i> About Mera‑Gide</div>
  <p style="background: white; padding: 20px; border-radius: var(--radius-sm); box-shadow: var(--shadow);">Mera‑Gide is a premium Green Ayurveda wellness destination. We bring you authentic herbal products rooted in ancient wisdom, carefully sourced and crafted for modern well-being. Our mission is to connect you with nature’s finest ingredients — pure, sustainable, and effective.</p>

  <!-- footer -->
  <footer class="footer">
    <div class="footer-grid">
      <div><h4>Mera‑Gide</h4><p style="margin-top: 8px;">Green Ayurveda since 2024</p></div>
      <div><h4>Quick</h4><a href="#">About Us</a><a href="#">Contact</a><a href="#">Terms</a><a href="#">Privacy</a></div>
      <div><h4>Support</h4><a href="#">Shipping</a><a href="#">Returns</a><a href="#">Refund</a></div>
      <div><h4>Connect</h4><a href="#"><i class="fab fa-instagram"></i> Instagram</a><a href="#"><i class="fab fa-youtube"></i> YouTube</a></div>
    </div>
    <div style="border-top: 1px solid #3b5a3b; margin-top: 30px; padding-top: 20px; text-align: center; font-size: 0.9rem;">© 2026 Mera‑Gide · Ayurvedic wellness</div>
  </footer>
</div>
<!-- disclaimer -->
<div style="max-width:1300px; margin: 0 auto; padding: 0 20px 20px; font-size:0.8rem; color: #4e6b53;"><i class="fas fa-info-circle"></i> These products are not intended to diagnose, treat, or cure any disease. Please consult a healthcare professional before use.</div>
</body>
</html>
