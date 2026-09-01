
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mera-Gide · Green Ayurveda</title>
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
    }

    body {
      background: #f8fbf6;
      color: #1e3a2f;
    }

    /* scrollbar */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #e0e8e0; }
    ::-webkit-scrollbar-thumb { background: #2b5e3b; border-radius: 12px; }

    .container {
      max-width: 1300px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* header */
    .navbar {
      background: #ffffffdd;
      backdrop-filter: blur(8px);
      box-shadow: 0 4px 20px rgba(0, 30, 10, 0.05);
      padding: 0.8rem 0;
      position: sticky;
      top: 0;
      z-index: 100;
      border-bottom: 2px solid #b7d7b0;
    }

    .nav-flex {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: 700;
      color: #1a4d2a;
      letter-spacing: -0.5px;
    }
    .logo i {
      color: #3a8f4b;
      margin-right: 6px;
    }

    .nav-links {
      display: flex;
      gap: 1.8rem;
      align-items: center;
      flex-wrap: wrap;
    }

    .nav-links a {
      text-decoration: none;
      color: #1e3a2f;
      font-weight: 500;
      font-size: 0.95rem;
      transition: 0.2s;
      border-bottom: 2px solid transparent;
      padding-bottom: 4px;
    }
    .nav-links a:hover {
      border-bottom-color: #3a8f4b;
      color: #0f2b1d;
    }

    .btn-outline {
      background: transparent;
      border: 1.5px solid #2b5e3b;
      padding: 0.4rem 1.2rem;
      border-radius: 40px;
      font-weight: 600;
      color: #1e4a2a;
      cursor: pointer;
      transition: 0.2s;
    }
    .btn-outline:hover {
      background: #2b5e3b;
      color: white;
    }

    .btn-primary {
      background: #2b5e3b;
      border: none;
      padding: 0.5rem 1.6rem;
      border-radius: 40px;
      font-weight: 600;
      color: white;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 4px 8px rgba(43, 94, 59, 0.2);
    }
    .btn-primary:hover {
      background: #1f452b;
      transform: scale(0.97);
    }

    .badge-cart {
      background: #c44545;
      color: white;
      border-radius: 30px;
      padding: 0.1rem 0.7rem;
      font-size: 0.8rem;
      margin-left: 4px;
    }

    /* hero */
    .hero {
      background: linear-gradient(145deg, #e6f3e4, #d0e8cb);
      border-radius: 32px;
      padding: 3rem 2.5rem;
      margin: 2rem 0;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
    }
    .hero h1 {
      font-size: 2.6rem;
      font-weight: 700;
      color: #103a20;
    }
    .hero p {
      font-size: 1.2rem;
      max-width: 500px;
      margin: 0.8rem 0;
      color: #1c452a;
    }

    /* search */
    .search-box {
      display: flex;
      gap: 0.5rem;
      margin: 1.8rem 0 0.5rem;
      flex-wrap: wrap;
    }
    .search-box input {
      flex: 1;
      padding: 0.75rem 1.2rem;
      border: 2px solid #b7d7b0;
      border-radius: 60px;
      font-size: 1rem;
      background: white;
      min-width: 200px;
    }
    .search-box input:focus {
      outline: none;
      border-color: #2b5e3b;
    }

    /* categories */
    .categories {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem 1.2rem;
      margin: 1.8rem 0;
    }
    .cat-chip {
      background: white;
      padding: 0.4rem 1.5rem;
      border-radius: 40px;
      border: 1px solid #c0dbb8;
      font-weight: 500;
      cursor: pointer;
      transition: 0.15s;
      box-shadow: 0 2px 6px rgba(0,0,0,0.02);
    }
    .cat-chip.active, .cat-chip:hover {
      background: #2b5e3b;
      color: white;
      border-color: #2b5e3b;
    }

    /* product grid */
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 2rem 1.5rem;
      margin: 2rem 0 3rem;
    }
    .product-card {
      background: white;
      border-radius: 24px;
      padding: 1.2rem 1rem 1.2rem;
      box-shadow: 0 8px 24px rgba(0, 30, 10, 0.06);
      transition: 0.2s;
      border: 1px solid #e3efe0;
      display: flex;
      flex-direction: column;
    }
    .product-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 16px 32px rgba(43, 94, 59, 0.12);
    }
    .product-card img {
      width: 100%;
      height: 140px;
      object-fit: cover;
      border-radius: 16px;
      background: #eef6ec;
    }
    .product-card h4 {
      margin: 0.6rem 0 0.2rem;
      font-size: 1rem;
    }
    .product-card .price {
      font-weight: 700;
      color: #1d4a2a;
      font-size: 1.1rem;
    }
    .product-card .cat-tag {
      font-size: 0.7rem;
      background: #e3efe0;
      padding: 0.2rem 0.8rem;
      border-radius: 30px;
      display: inline-block;
      margin: 0.2rem 0 0.4rem;
    }
    .product-card .actions {
      margin-top: auto;
      display: flex;
      gap: 6px;
      flex-wrap: wrap;
    }
    .btn-sm {
      padding: 0.25rem 1rem;
      border-radius: 40px;
      border: none;
      background: #e9f3e7;
      font-weight: 600;
      color: #1f452b;
      cursor: pointer;
      transition: 0.1s;
      font-size: 0.8rem;
    }
    .btn-sm.add {
      background: #2b5e3b;
      color: white;
    }
    .btn-sm.add:hover {
      background: #1d4028;
    }

    /* cart sidebar */
    .cart-panel {
      background: #ffffff;
      border-radius: 28px;
      padding: 1.8rem;
      box-shadow: 0 12px 40px rgba(0,0,0,0.06);
      margin: 2rem 0;
      border: 1px solid #d6e8d0;
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid #e3efe0;
      padding: 0.6rem 0;
    }
    .cart-total {
      font-weight: 700;
      font-size: 1.2rem;
      margin-top: 0.8rem;
    }

    /* forms */
    .form-card {
      background: white;
      padding: 2rem;
      border-radius: 28px;
      box-shadow: 0 8px 24px rgba(0,30,10,0.04);
      margin: 1.5rem 0;
      border: 1px solid #ddecd8;
    }
    .form-group {
      margin-bottom: 1rem;
    }
    .form-group label {
      font-weight: 600;
      display: block;
      margin-bottom: 0.2rem;
    }
    .form-group input, .form-group select {
      width: 100%;
      padding: 0.6rem 1rem;
      border: 2px solid #ddecd8;
      border-radius: 30px;
      background: #fafff9;
    }
    .form-group input:focus {
      border-color: #2b5e3b;
      outline: none;
    }

    /* admin / seller panels */
    .panel-tabs {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      margin: 1rem 0;
    }
    .tab-btn {
      background: white;
      border: 1px solid #b7d7b0;
      padding: 0.5rem 1.8rem;
      border-radius: 40px;
      font-weight: 600;
      cursor: pointer;
    }
    .tab-btn.active {
      background: #2b5e3b;
      color: white;
      border-color: #2b5e3b;
    }

    .badge-status {
      background: #f1c40f;
      color: #1e3a2f;
      padding: 0.1rem 1rem;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 600;
    }

    .grid-2col {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
    }

    .footer-links {
      margin: 3rem 0 1rem;
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      justify-content: center;
      border-top: 1px solid #d6e8d0;
      padding-top: 2rem;
    }
    .footer-links a {
      color: #1e4a2a;
      text-decoration: none;
      font-weight: 500;
    }

    .hidden { display: none; }
    .flex { display: flex; gap: 1rem; flex-wrap: wrap; align-items: center; }

    /* responsive */
    @media (max-width: 680px) {
      .hero h1 { font-size: 2rem; }
      .nav-flex { flex-direction: column; gap: 0.8rem; }
      .product-grid { grid-template-columns: 1fr 1fr; }
    }
    @media (max-width: 440px) {
      .product-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <div class="navbar">
    <div class="container nav-flex">
      <div class="logo"><i class="fas fa-leaf"></i> Mera-Gide</div>
      <div class="nav-links">
        <a href="#" onclick="showMain()">Home</a>
        <a href="#" onclick="showSellers()">Seller</a>
        <a href="#" onclick="showAdmin()">Admin</a>
        <span style="cursor:pointer" onclick="toggleCart()"><i class="fas fa-shopping-cart"></i> Cart <span id="cartCount" class="badge-cart">0</span></span>
      </div>
    </div>
  </div>

  <div class="container" id="appMain">
    <!-- HERO -->
    <div class="hero">
      <div>
        <h1>🌿 Green Ayurveda</h1>
        <p>Pure, herbal & organic wellness. Discover authentic products from trusted sellers.</p>
        <div class="search-box">
          <input type="text" id="searchInput" placeholder="Search products..." oninput="filterProducts()" />
          <button class="btn-primary" onclick="filterProducts()"><i class="fas fa-search"></i> Search</button>
        </div>
      </div>
      <div style="font-size:4rem; opacity:0.5;">🌱</div>
    </div>

    <!-- categories -->
    <div class="categories" id="categoryList">
      <span class="cat-chip active" data-cat="all">All</span>
      <span class="cat-chip" data-cat="Ayurveda">Ayurveda</span>
      <span class="cat-chip" data-cat="Herbal">Herbal</span>
      <span class="cat-chip" data-cat="Beauty">Beauty</span>
      <span class="cat-chip" data-cat="Personal Care">Personal Care</span>
      <span class="cat-chip" data-cat="Wellness">Wellness</span>
      <span class="cat-chip" data-cat="Organic">Organic</span>
    </div>

    <!-- product grid -->
    <div id="productGrid" class="product-grid"></div>

    <!-- cart panel -->
    <div id="cartPanel" class="cart-panel hidden">
      <h3><i class="fas fa-shopping-bag"></i> Your Cart</h3>
      <div id="cartItems"></div>
      <div class="cart-total" id="cartTotal">Total: ₹0</div>
      <button class="btn-primary" onclick="checkout()">Proceed to Checkout</button>
    </div>

    <!-- info pages (dummy) -->
    <div class="footer-links">
      <a href="#" onclick="showInfo('about')">About</a>
      <a href="#" onclick="showInfo('contact')">Contact</a>
      <a href="#" onclick="showInfo('terms')">Terms</a>
      <a href="#" onclick="showInfo('privacy')">Privacy</a>
      <a href="#" onclick="showInfo('return')">Returns</a>
      <a href="#" onclick="showInfo('shipping')">Shipping</a>
    </div>
  </div>

  <!-- seller panel (hidden) -->
  <div id="sellerPanel" class="container hidden">
    <h2><i class="fas fa-store"></i> Seller Panel</h2>
    <div class="panel-tabs">
      <span class="tab-btn active" onclick="showSellerTab('register')">Register</span>
      <span class="tab-btn" onclick="showSellerTab('login')">Login</span>
      <span class="tab-btn" onclick="showSellerTab('dashboard')">Dashboard</span>
    </div>
    <div id="sellerRegister" class="form-card">
      <h4>Seller Registration</h4>
      <div class="form-group"><label>Full Name</label><input id="sellerName" placeholder="Your name" /></div>
      <div class="form-group"><label>Brand</label><input id="sellerBrand" placeholder="Brand name" /></div>
      <div class="form-group"><label>Email</label><input id="sellerEmail" type="email" placeholder="seller@example.com" /></div>
      <div class="form-group"><label>Mobile</label><input id="sellerMobile" placeholder="+91 98765 43210" /></div>
      <div class="form-group"><label>Password</label><input id="sellerPassword" type="password" placeholder="min 6 chars" /></div>
      <button class="btn-primary" onclick="registerSeller()">Register</button>
      <p id="sellerMsg" style="margin-top:0.6rem;"></p>
    </div>
    <div id="sellerLogin" class="form-card hidden">
      <h4>Seller Login</h4>
      <div class="form-group"><label>Email</label><input id="sellerLoginEmail" placeholder="seller@example.com" /></div>
      <div class="form-group"><label>Password</label><input id="sellerLoginPass" type="password" /></div>
      <button class="btn-primary" onclick="loginSeller()">Login</button>
      <p id="sellerLoginMsg"></p>
    </div>
    <div id="sellerDashboard" class="form-card hidden">
      <h4>Your Products <span style="font-weight:400;font-size:0.9rem;">(pending approval)</span></h4>
      <div id="sellerProductList"></div>
      <hr style="margin:1.5rem 0;" />
      <h4>Add New Product</h4>
      <div class="form-group"><label>Name</label><input id="prodName" placeholder="Product name" /></div>
      <div class="form-group"><label>Category</label><input id="prodCategory" placeholder="e.g. Ayurveda" /></div>
      <div class="form-group"><label>Price (₹)</label><input id="prodPrice" type="number" placeholder="299" /></div>
      <div class="form-group"><label>Image URL (demo)</label><input id="prodImage" placeholder="https://via.placeholder.com/200" /></div>
      <button class="btn-primary" onclick="addSellerProduct()">Submit for Approval</button>
      <p id="sellerProdMsg"></p>
    </div>
  </div>

  <!-- admin panel -->
  <div id="adminPanel" class="container hidden">
    <h2><i class="fas fa-user-shield"></i> Admin</h2>
    <div class="panel-tabs">
      <span class="tab-btn active" onclick="showAdminTab('login')">Login</span>
      <span class="tab-btn" onclick="showAdminTab('dashboard')">Dashboard</span>
    </div>
    <div id="adminLogin" class="form-card">
      <h4>Admin Login</h4>
      <div class="form-group"><label>Email</label><input id="adminEmail" value="admin@mera-gide.com" /></div>
      <div class="form-group"><label>Password</label><input id="adminPass" type="password" value="admin123" /></div>
      <button class="btn-primary" onclick="loginAdmin()">Login</button>
      <p id="adminMsg"></p>
    </div>
    <div id="adminDashboard" class="hidden">
      <div class="grid-2col" style="margin-bottom:1rem;">
        <div class="form-card"><h4>📦 Products</h4><span id="adminProdCount">0</span></div>
        <div class="form-card"><h4>⏳ Pending</h4><span id="adminPendingCount">0</span></div>
      </div>
      <div id="adminProductList"></div>
      <hr style="margin:2rem 0;" />
      <h4>➕ Add Product (Admin)</h4>
      <div class="form-group"><label>Name</label><input id="adminProdName" /></div>
      <div class="form-group"><label>Category</label><input id="adminProdCat" /></div>
      <div class="form-group"><label>Price</label><input id="adminProdPrice" type="number" /></div>
      <div class="form-group"><label>Image URL</label><input id="adminProdImg" placeholder="https://via.placeholder.com/200" /></div>
      <button class="btn-primary" onclick="adminAddProduct()">Add Product</button>
    </div>
  </div>

  <script>
    // ---------- DATA ----------
    let products = JSON.parse(localStorage.getItem('meraProducts')) || [];
    let cart = JSON.parse(localStorage.getItem('meraCart')) || [];
    let sellers = JSON.parse(localStorage.getItem('meraSellers')) || [];
    let orders = JSON.parse(localStorage.getItem('meraOrders')) || [];
    let currentCategory = 'all';
    let adminLogged = false;
    let sellerLogged = null;

    // seed demo products
    if (products.length === 0) {
      products = [
        { id: 1, name: 'Ashwagandha Root', category: 'Ayurveda', price: 450, image: 'https://via.placeholder.com/200/9bc89b/1e3a2f?text=Ashwagandha', approved: true },
        { id: 2, name: 'Tulsi Drops', category: 'Herbal', price: 299, image: 'https://via.placeholder.com/200/b7d7b0/1e3a2f?text=Tulsi', approved: true },
        { id: 3, name: 'Neem Face Wash', category: 'Beauty', price: 350, image: 'https://via.placeholder.com/200/c0dbb8/1e3a2f?text=Neem', approved: true },
        { id: 4, name: 'Triphala Churna', category: 'Wellness', price: 520, image: 'https://via.placeholder.com/200/d0e8cb/1e3a2f?text=Triphala', approved: true },
        { id: 5, name: 'Organic Coconut Oil', category: 'Organic', price: 600, image: 'https://via.placeholder.com/200/e3efe0/1e3a2f?text=Coconut', approved: true },
        { id: 6, name: 'Brahmi Capsules', category: 'Ayurveda', price: 390, image: 'https://via.placeholder.com/200/d6e8d0/1e3a2f?text=Brahmi', approved: true },
      ];
      localStorage.setItem('meraProducts', JSON.stringify(products));
    }

    // ---------- RENDER ----------
    function renderProducts(filter = 'all', search = '') {
      const grid = document.getElementById('productGrid');
      let list = products.filter(p => p.approved !== false);
      if (filter !== 'all') list = list.filter(p => p.category === filter);
      if (search) list = list.filter(p => p.name.toLowerCase().includes(search.toLowerCase()));
      if (list.length === 0) { grid.innerHTML = '<p style="grid-column:1/-1; text-align:center;">No products found 🌿</p>'; return; }
      grid.innerHTML = list.map(p => `
        <div class="product-card">
          <img src="${p.image || 'https://via.placeholder.com/200/b7d7b0/1e3a2f?text=Herbal'}" alt="${p.name}" />
          <h4>${p.name}</h4>
          <span class="cat-tag">${p.category}</span>
          <div class="price">₹${p.price}</div>
          <div class="actions">
            <button class="btn-sm add" onclick="addToCart(${p.id})"><i class="fas fa-plus"></i> Add</button>
          </div>
        </div>
      `).join('');
      updateCartBadge();
    }

    function filterProducts() {
      const search = document.getElementById('searchInput').value;
      renderProducts(currentCategory, search);
    }

    // category clicks
    document.getElementById('categoryList').addEventListener('click', (e) => {
      if (e.target.dataset.cat) {
        document.querySelectorAll('.cat-chip').forEach(c => c.classList.remove('active'));
        e.target.classList.add('active');
        currentCategory = e.target.dataset.cat;
        renderProducts(currentCategory, document.getElementById('searchInput').value);
      }
    });

    // ---------- CART ----------
    function updateCartBadge() {
      document.getElementById('cartCount').textContent = cart.reduce((sum, i) => sum + i.qty, 0);
    }

    function addToCart(productId) {
      const p = products.find(x => x.id === productId);
      if (!p) return;
      const existing = cart.find(x => x.id === productId);
      if (existing) { existing.qty++; } else { cart.push({ id: p.id, name: p.name, price: p.price, qty: 1, image: p.image }); }
      localStorage.setItem('meraCart', JSON.stringify(cart));
      updateCartBadge();
      renderCart();
    }

    function renderCart() {
      const container = document.getElementById('cartItems');
      if (cart.length === 0) { container.innerHTML = '<p>Cart is empty</p>'; document.getElementById('cartTotal').textContent = 'Total: ₹0'; return; }
      container.innerHTML = cart.map((item, idx) => `
        <div class="cart-item">
          <span>${item.name} × ${item.qty}</span>
          <span>₹${item.price * item.qty} 
            <button class="btn-sm" onclick="removeFromCart(${idx})">✕</button>
          </span>
        </div>
      `).join('');
      const total = cart.reduce((sum, i) => sum + i.price * i.qty, 0);
      document.getElementById('cartTotal').textContent = `Total: ₹${total}`;
    }

    function removeFromCart(idx) {
      cart.splice(idx, 1);
      localStorage.setItem('meraCart', JSON.stringify(cart));
      renderCart();
      updateCartBadge();
    }

    function toggleCart() {
      const panel = document.getElementById('cartPanel');
      panel.classList.toggle('hidden');
      if (!panel.classList.contains('hidden')) renderCart();
    }

    function checkout() {
      if (cart.length === 0) return alert('Cart is empty');
      const order = { id: Date.now(), items: [...cart], total: cart.reduce((s, i) => s + i.price * i.qty, 0), status: 'confirmed', date: new Date().toLocaleDateString() };
      orders.push(order);
      localStorage.setItem('meraOrders', JSON.stringify(orders));
      cart = [];
      localStorage.setItem('meraCart', JSON.stringify(cart));
      renderCart();
      updateCartBadge();
      alert('✅ Order placed! (UPI/QR placeholder) \nTotal: ₹' + order.total);
    }

    // ---------- SELLER ----------
    function showSellers() {
      document.getElementById('appMain').classList.add('hidden');
      document.getElementById('sellerPanel').classList.remove('hidden');
      document.getElementById('adminPanel').classList.add('hidden');
      renderSellerProducts();
    }

    function showMain() {
      document.getElementById('appMain').classList.remove('hidden');
      document.getElementById('sellerPanel').classList.add('hidden');
      document.getElementById('adminPanel').classList.add('hidden');
      renderProducts(currentCategory);
    }

    function showSellerTab(tab) {
      document.getElementById('sellerRegister').classList.toggle('hidden', tab !== 'register');
      document.getElementById('sellerLogin').classList.toggle('hidden', tab !== 'login');
      document.getElementById('sellerDashboard').classList.toggle('hidden', tab !== 'dashboard');
    }

    function registerSeller() {
      const name = document.getElementById('sellerName').value.trim();
      const brand = document.getElementById('sellerBrand').value.trim();
      const email = document.getElementById('sellerEmail').value.trim();
      const mobile = document.getElementById('sellerMobile').value.trim();
      const password = document.getElementById('sellerPassword').value.trim();
      if (!name || !brand || !email || !mobile || !password) return alert('Fill all fields');
      if (sellers.find(s => s.email === email)) return document.getElementById('sellerMsg').innerText = 'Email already registered.';
      sellers.push({ name, brand, email, mobile, password, approved: false });
      localStorage.setItem('meraSellers', JSON.stringify(sellers));
      document.getElementById('sellerMsg').innerHTML = '✅ Registration submitted. Wait for admin approval.';
    }

    function loginSeller() {
      const email = document.getElementById('sellerLoginEmail').value.trim();
      const pass = document.getElementById('sellerLoginPass').value.trim();
      const seller = sellers.find(s => s.email === email && s.password === pass);
      if (!seller) return document.getElementById('sellerLoginMsg').innerText = 'Invalid credentials';
      if (!seller.approved) return document.getElementById('sellerLoginMsg').innerText = '⏳ Pending admin approval.';
      sellerLogged = seller;
      document.getElementById('sellerLoginMsg').innerHTML = '✅ Logged in.';
      showSellerTab('dashboard');
      renderSellerProducts();
    }

    function renderSellerProducts() {
      const list = document.getElementById('sellerProductList');
      const sellerProducts = products.filter(p => p.sellerEmail === sellerLogged?.email);
      if (!sellerLogged) { list.innerHTML = '<p>Login to see your products</p>'; return; }
      list.innerHTML = sellerProducts.map(p => `
        <div style="display:flex;justify-content:space-between;border-bottom:1px solid #ddecd8;padding:0.4rem 0;">
          <span>${p.name} (₹${p.price})</span>
          <span class="badge-status">${p.approved ? '✅ Approved' : '⏳ Pending'}</span>
        </div>
      `).join('') || '<p>No products yet.</p>';
    }

    function addSellerProduct() {
      if (!sellerLogged) return alert('Login first');
      const name = document.getElementById('prodName').value.trim();
      const category = document.getElementById('prodCategory').value.trim();
      const price = parseFloat(document.getElementById('prodPrice').value);
      const image = document.getElementById('prodImage').value.trim() || 'https://via.placeholder.com/200/b7d7b0/1e3a2f?text=Herbal';
      if (!name || !category || !price) return alert('Fill product details');
      const newProd = { id: Date.now(), name, category, price, image, approved: false, sellerEmail: sellerLogged.email };
      products.push(newProd);
      localStorage.setItem('meraProducts', JSON.stringify(products));
      document.getElementById('sellerProdMsg').innerHTML = '✅ Product submitted for approval.';
      renderSellerProducts();
    }

    // ---------- ADMIN ----------
    function showAdmin() {
      document.getElementById('appMain').classList.add('hidden');
      document.getElementById('sellerPanel').classList.add('hidden');
      document.getElementById('adminPanel').classList.remove('hidden');
    }

    function showAdminTab(tab) {
      document.getElementById('adminLogin').classList.toggle('hidden', tab !== 'login');
      document.getElementById('adminDashboard').classList.toggle('hidden', tab !== 'dashboard');
      if (tab === 'dashboard' && adminLogged) renderAdminDashboard();
    }

    function loginAdmin() {
      const email = document.getElementById('adminEmail').value.trim();
      const pass = document.getElementById('adminPass').value.trim();
      if (email === 'admin@mera-gide.com' && pass === 'admin123') {
        adminLogged = true;
        document.getElementById('adminMsg').innerHTML = '✅ Logged in.';
        showAdminTab('dashboard');
        renderAdminDashboard();
      } else {
        document.getElementById('adminMsg').innerHTML = '❌ Invalid credentials';
      }
    }

    function renderAdminDashboard() {
      const all = products;
      const pending = all.filter(p => p.approved === false);
      document.getElementById('adminProdCount').textContent = all.length;
      document.getElementById('adminPendingCount').textContent = pending.length;
      const container = document.getElementById('adminProductList');
      container.innerHTML = all.map(p => `
        <div style="display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid #e3efe0;padding:0.5rem 0;flex-wrap:wrap;">
          <span><strong>${p.name}</strong> (${p.category}) ₹${p.price} ${p.approved ? '✅' : '⏳'}</span>
          <span>
            ${!p.approved ? `<button class="btn-sm" onclick="approveProduct(${p.id})">Approve</button>` : ''}
            <button class="btn-sm" onclick="deleteProduct(${p.id})">Delete</button>
          </span>
        </div>
      `).join('');
    }

    function approveProduct(id) {
      const p = products.find(x => x.id === id);
      if (p) { p.approved = true; localStorage.setItem('meraProducts', JSON.stringify(products)); renderAdminDashboard(); }
    }

    function deleteProduct(id) {
      if (!confirm('Delete this product?')) return;
      products = products.filter(p => p.id !== id);
      localStorage.setItem('meraProducts', JSON.stringify(products));
      renderAdminDashboard();
      renderProducts(currentCategory);
    }

    function adminAddProduct() {
      const name = document.getElementById('adminProdName').value.trim();
      const category = document.getElementById('adminProdCat').value.trim();
      const price = parseFloat(document.getElementById('adminProdPrice').value);
      const image = document.getElementById('adminProdImg').value.trim() || 'https://via.placeholder.com/200/b7d7b0/1e3a2f?text=Herbal';
      if (!name || !category || !price) return alert('Fill all fields');
      products.push({ id: Date.now(), name, category, price, image, approved: true });
      localStorage.setItem('meraProducts', JSON.stringify(products));
      renderAdminDashboard();
      renderProducts(currentCategory);
    }

    // info pages (dummy)
    function showInfo(page) {
      const msgs = {
        about: '🌿 Mera-Gide: Authentic Green Ayurveda marketplace. Pure wellness since 2025.',
        contact: '📧 support@mera-gide.com  |  📞 +91 98765 43210',
        terms: '📜 Terms: Use at your own discretion. All products are herbal & natural.',
        privacy: '🔒 Privacy: We value your data. No sharing with third parties.',
        return: '🔄 Return Policy: 7-day return on unused products.',
        shipping: '🚚 Shipping: Free delivery on orders above ₹499.'
      };
      alert(msgs[page] || 'Page info');
    }

    // init
    renderProducts();
    updateCartBadge();
  </script>
</body>
</html>
