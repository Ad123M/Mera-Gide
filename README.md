
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.5">
  <title>Mera-Gide · Green Ayurveda</title>
  <!-- Tailwind via CDN + custom green theme -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    body { background: #f7f9f6; font-family: 'Segoe UI', Roboto, system-ui, sans-serif; }
    .mera-green { color: #2b6e3b; }
    .mera-bg { background-color: #e4f0e0; }
    .mera-border { border-color: #a6c8a0; }
    .hover-green:hover { background-color: #2b6e3b; color: white; }
    .card-shadow { box-shadow: 0 8px 20px rgba(43, 110, 59, 0.08); }
    .nav-link { transition: all 0.2s; cursor: pointer; }
    .nav-link:hover { color: #1e4f2a; }
    .logo-leaf { color: #2b6e3b; }
    .badge-pending { background: #fbbf24; color: #1e1e1e; }
    .badge-approved { background: #22c55e; color: white; }
    .badge-rejected { background: #ef4444; color: white; }
    .product-card { transition: transform 0.2s; cursor: pointer; }
    .product-card:hover { transform: scale(1.01); }
    .hamburger-line { width: 24px; height: 2px; background: #1e3a2a; margin: 5px 0; }
    .clickable { cursor: pointer; }
    .toast-message { position: fixed; bottom: 20px; right: 20px; background: #2b6e3b; color: white; padding: 12px 24px; border-radius: 40px; box-shadow: 0 4px 12px rgba(0,0,0,0.2); z-index: 999; transition: all 0.3s; }
  </style>
</head>
<body>

<!-- ========== HEADER ========== -->
<header class="bg-white shadow-md sticky top-0 z-50 border-b border-mera-border">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 flex items-center justify-between h-20">
    <!-- Logo + brand -->
    <div class="flex items-center gap-2 clickable" onclick="showToast('🌿 Welcome to Mera-Gide')">
      <div class="flex items-center">
        <i class="fas fa-leaf text-3xl mera-green"></i>
        <span class="text-2xl font-bold ml-1 mera-green tracking-tight">Mera-Gide</span>
        <span class="hidden sm:inline text-xs ml-1 bg-mera-bg px-2 py-0.5 rounded-full text-gray-700">Ayurveda</span>
      </div>
    </div>

    <!-- Desktop nav (hidden on mobile) -->
    <nav class="hidden md:flex items-center gap-5 text-sm font-medium text-gray-700">
      <a class="nav-link" onclick="showToast('🏠 Home')">Home</a>
      <a class="nav-link" onclick="showToast('🛍️ Shop')">Shop</a>
      <a class="nav-link" onclick="showToast('📂 Categories')">Categories</a>
      <a class="nav-link" onclick="showToast('📖 About Us')">About</a>
      <a class="nav-link" onclick="showToast('📞 Contact')">Contact</a>
      <a class="nav-link mera-green font-semibold" onclick="showToast('👤 Seller Dashboard')">Seller</a>
      <a class="nav-link" onclick="showToast('🔐 Login')"><i class="far fa-user"></i> Login</a>
      <a class="nav-link relative" onclick="showToast('🛒 Cart')"><i class="fas fa-shopping-cart text-lg"></i><span class="absolute -top-1 -right-2 bg-red-500 text-white text-xs rounded-full px-1.5">3</span></a>
    </nav>

    <!-- Search (desktop) -->
    <div class="hidden md:flex items-center bg-mera-bg rounded-full px-4 py-1.5 w-56">
      <i class="fas fa-search text-gray-500"></i>
      <input type="text" placeholder="Search products..." class="bg-transparent outline-none ml-2 w-full text-sm" onkeydown="if(event.key==='Enter') showToast('🔍 Searching: '+this.value)">
    </div>

    <!-- Mobile hamburger + icons -->
    <div class="flex md:hidden items-center gap-4">
      <i class="fas fa-search text-gray-700 text-lg clickable" onclick="showToast('🔍 Search')"></i>
      <i class="fas fa-shopping-cart text-lg mera-green relative clickable" onclick="showToast('🛒 Cart')"><span class="absolute -top-1 -right-2 bg-red-500 text-white text-xs rounded-full px-1.5">3</span></i>
      <button id="hamburgerBtn" class="focus:outline-none">
        <div class="hamburger-line"></div><div class="hamburger-line"></div><div class="hamburger-line"></div>
      </button>
    </div>
  </div>
  <!-- mobile menu (hidden) -->
  <div id="mobileMenu" class="hidden md:hidden bg-white border-t border-mera-border px-4 pb-4 flex flex-col gap-2 text-sm font-medium">
    <a class="py-1 border-b border-gray-100 clickable" onclick="showToast('🏠 Home');toggleMobile()">Home</a>
    <a class="py-1 border-b border-gray-100 clickable" onclick="showToast('🛍️ Shop');toggleMobile()">Shop</a>
    <a class="py-1 border-b border-gray-100 clickable" onclick="showToast('📂 Categories');toggleMobile()">Categories</a>
    <a class="py-1 border-b border-gray-100 clickable" onclick="showToast('📖 About');toggleMobile()">About</a>
    <a class="py-1 border-b border-gray-100 clickable" onclick="showToast('📞 Contact');toggleMobile()">Contact</a>
    <a class="py-1 border-b border-gray-100 text-mera-green font-bold clickable" onclick="showToast('👤 Seller');toggleMobile()">Seller</a>
    <a class="py-1 clickable" onclick="showToast('🔐 Login');toggleMobile()"><i class="far fa-user mr-2"></i>Login</a>
  </div>
</header>

<main class="max-w-7xl mx-auto px-4 sm:px-6 py-6">

  <!-- ===== HERO ===== -->
  <section class="relative rounded-2xl overflow-hidden bg-gradient-to-r from-[#e2f0da] to-[#c7dfbe] p-8 md:p-12 mb-12">
    <div class="relative z-10 max-w-2xl">
      <h1 class="text-4xl md:text-5xl font-extrabold text-gray-800 leading-tight">Natural Wellness. <span class="text-[#2b6e3b]">Trusted Ayurveda.</span></h1>
      <p class="text-lg md:text-xl text-gray-700 mt-3">Discover Green Ayurveda products for your everyday wellness.</p>
      <div class="flex flex-wrap gap-4 mt-6">
        <a class="bg-[#2b6e3b] hover:bg-[#1f5230] text-white font-semibold px-8 py-3 rounded-full shadow-lg transition clickable" onclick="showToast('🛍️ Shop Now')">Shop Now</a>
        <a class="bg-white text-[#2b6e3b] font-semibold px-8 py-3 rounded-full shadow-md hover:bg-gray-50 transition clickable" onclick="showToast('📝 Become a Seller')">Become a Seller</a>
      </div>
    </div>
    <div class="absolute right-0 bottom-0 opacity-20 text-9xl"><i class="fas fa-leaf"></i></div>
  </section>

  <!-- ===== FEATURED CATEGORIES ===== -->
  <section class="mb-12">
    <h2 class="text-2xl font-bold text-gray-800 mb-4 flex items-center"><i class="fas fa-tags mera-green mr-2"></i> Featured Categories</h2>
    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-6 gap-4">
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('🌿 Herbal Products')"><i class="fas fa-seedling text-3xl mera-green"></i><p class="font-medium mt-1">Herbal</p></div>
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('🪷 Ayurveda')"><i class="fas fa-spa text-3xl mera-green"></i><p class="font-medium mt-1">Ayurveda</p></div>
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('💄 Natural Beauty')"><i class="fas fa-leaf text-3xl mera-green"></i><p class="font-medium mt-1">Natural Beauty</p></div>
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('🧴 Personal Care')"><i class="fas fa-hand-sparkles text-3xl mera-green"></i><p class="font-medium mt-1">Personal Care</p></div>
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('🌱 Herbal Wellness')"><i class="fas fa-mortar-pestle text-3xl mera-green"></i><p class="font-medium mt-1">Herbal Wellness</p></div>
      <div class="bg-white rounded-xl p-4 text-center shadow card-shadow hover:shadow-lg transition clickable" onclick="showToast('🍎 Organic Products')"><i class="fas fa-apple-alt text-3xl mera-green"></i><p class="font-medium mt-1">Organic</p></div>
    </div>
  </section>

  <!-- ===== FEATURED PRODUCTS ===== -->
  <section class="mb-12">
    <div class="flex justify-between items-center mb-4">
      <h2 class="text-2xl font-bold text-gray-800"><i class="fas fa-star text-yellow-500 mr-2"></i>Featured Products</h2>
      <a class="text-mera-green font-medium clickable" onclick="showToast('🛍️ View All Products')">View All →</a>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <!-- product card 1 -->
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Ashwagandha Root - ₹499')">
        <div class="h-48 bg-mera-bg flex items-center justify-center text-5xl text-[#2b6e3b]"><i class="fas fa-leaf"></i></div>
        <div class="p-4">
          <h3 class="font-bold text-gray-800">Ashwagandha Root</h3>
          <p class="text-sm text-gray-500">Pure herbal supplement</p>
          <div class="flex items-center gap-2 mt-1"><span class="text-lg font-bold text-[#2b6e3b]">₹499</span><span class="text-sm line-through text-gray-400">₹799</span><span class="text-xs bg-red-100 text-red-600 px-2 py-0.5 rounded-full">-38%</span></div>
          <div class="flex items-center text-yellow-400 text-sm"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i><span class="text-gray-500 ml-1">(124)</span></div>
          <div class="flex items-center gap-2 mt-2"><span class="text-xs bg-green-100 text-green-700 px-2 py-0.5 rounded-full"><i class="fas fa-check-circle"></i> In Stock</span></div>
          <div class="flex gap-2 mt-3">
            <button class="flex-1 bg-[#2b6e3b] text-white py-1.5 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')"><i class="fas fa-cart-plus mr-1"></i>Add</button>
            <button class="flex-1 border border-[#2b6e3b] text-[#2b6e3b] py-1.5 rounded-full text-sm hover:bg-mera-bg transition" onclick="event.stopPropagation(); showToast('⚡ Buy Now')">Buy Now</button>
          </div>
        </div>
      </div>
      <!-- product card 2 -->
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Triphala Churna - ₹299')">
        <div class="h-48 bg-mera-bg flex items-center justify-center text-5xl text-[#2b6e3b]"><i class="fas fa-seedling"></i></div>
        <div class="p-4">
          <h3 class="font-bold text-gray-800">Triphala Churna</h3>
          <p class="text-sm text-gray-500">Digestive wellness</p>
          <div class="flex items-center gap-2 mt-1"><span class="text-lg font-bold text-[#2b6e3b]">₹299</span><span class="text-sm line-through text-gray-400">₹450</span><span class="text-xs bg-red-100 text-red-600 px-2 py-0.5 rounded-full">-33%</span></div>
          <div class="flex items-center text-yellow-400 text-sm"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><span class="text-gray-500 ml-1">(89)</span></div>
          <div class="flex items-center gap-2 mt-2"><span class="text-xs bg-green-100 text-green-700 px-2 py-0.5 rounded-full"><i class="fas fa-check-circle"></i> In Stock</span></div>
          <div class="flex gap-2 mt-3">
            <button class="flex-1 bg-[#2b6e3b] text-white py-1.5 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')"><i class="fas fa-cart-plus mr-1"></i>Add</button>
            <button class="flex-1 border border-[#2b6e3b] text-[#2b6e3b] py-1.5 rounded-full text-sm hover:bg-mera-bg transition" onclick="event.stopPropagation(); showToast('⚡ Buy Now')">Buy Now</button>
          </div>
        </div>
      </div>
      <!-- product card 3 -->
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Neem & Tulsi Soap - ₹199')">
        <div class="h-48 bg-mera-bg flex items-center justify-center text-5xl text-[#2b6e3b]"><i class="fas fa-spa"></i></div>
        <div class="p-4">
          <h3 class="font-bold text-gray-800">Neem & Tulsi Soap</h3>
          <p class="text-sm text-gray-500">Natural skin care</p>
          <div class="flex items-center gap-2 mt-1"><span class="text-lg font-bold text-[#2b6e3b]">₹199</span><span class="text-sm line-through text-gray-400">₹299</span><span class="text-xs bg-red-100 text-red-600 px-2 py-0.5 rounded-full">-33%</span></div>
          <div class="flex items-center text-yellow-400 text-sm"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><span class="text-gray-500 ml-1">(210)</span></div>
          <div class="flex items-center gap-2 mt-2"><span class="text-xs bg-green-100 text-green-700 px-2 py-0.5 rounded-full"><i class="fas fa-check-circle"></i> In Stock</span></div>
          <div class="flex gap-2 mt-3">
            <button class="flex-1 bg-[#2b6e3b] text-white py-1.5 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')"><i class="fas fa-cart-plus mr-1"></i>Add</button>
            <button class="flex-1 border border-[#2b6e3b] text-[#2b6e3b] py-1.5 rounded-full text-sm hover:bg-mera-bg transition" onclick="event.stopPropagation(); showToast('⚡ Buy Now')">Buy Now</button>
          </div>
        </div>
      </div>
      <!-- product card 4 -->
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Brahmi Oil - ₹349')">
        <div class="h-48 bg-mera-bg flex items-center justify-center text-5xl text-[#2b6e3b]"><i class="fas fa-mortar-pestle"></i></div>
        <div class="p-4">
          <h3 class="font-bold text-gray-800">Brahmi Oil</h3>
          <p class="text-sm text-gray-500">Hair & scalp care</p>
          <div class="flex items-center gap-2 mt-1"><span class="text-lg font-bold text-[#2b6e3b]">₹349</span><span class="text-sm line-through text-gray-400">₹500</span><span class="text-xs bg-red-100 text-red-600 px-2 py-0.5 rounded-full">-30%</span></div>
          <div class="flex items-center text-yellow-400 text-sm"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i><span class="text-gray-500 ml-1">(67)</span></div>
          <div class="flex items-center gap-2 mt-2"><span class="text-xs bg-green-100 text-green-700 px-2 py-0.5 rounded-full"><i class="fas fa-check-circle"></i> In Stock</span></div>
          <div class="flex gap-2 mt-3">
            <button class="flex-1 bg-[#2b6e3b] text-white py-1.5 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')"><i class="fas fa-cart-plus mr-1"></i>Add</button>
            <button class="flex-1 border border-[#2b6e3b] text-[#2b6e3b] py-1.5 rounded-full text-sm hover:bg-mera-bg transition" onclick="event.stopPropagation(); showToast('⚡ Buy Now')">Buy Now</button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== WHY CHOOSE ===== -->
  <section class="bg-white rounded-2xl p-8 shadow card-shadow mb-12">
    <h2 class="text-2xl font-bold text-center text-gray-800 mb-6"><i class="fas fa-check-circle mera-green"></i> Why Mera-Gide?</h2>
    <div class="grid grid-cols-2 md:grid-cols-5 gap-4 text-center">
      <div class="clickable" onclick="showToast('🌿 Natural Selection')"><i class="fas fa-leaf text-3xl mera-green"></i><p class="font-medium mt-1">Natural Selection</p></div>
      <div class="clickable" onclick="showToast('🤝 Trusted Sellers')"><i class="fas fa-handshake text-3xl mera-green"></i><p class="font-medium mt-1">Trusted Sellers</p></div>
      <div class="clickable" onclick="showToast('🔒 Secure Payments')"><i class="fas fa-lock text-3xl mera-green"></i><p class="font-medium mt-1">Secure Payments</p></div>
      <div class="clickable" onclick="showToast('🚚 Easy Ordering')"><i class="fas fa-truck text-3xl mera-green"></i><p class="font-medium mt-1">Easy Ordering</p></div>
      <div class="clickable" onclick="showToast('🎧 Customer Support')"><i class="fas fa-headset text-3xl mera-green"></i><p class="font-medium mt-1">Customer Support</p></div>
    </div>
  </section>

  <!-- ===== SELLER CTA ===== -->
  <section class="bg-gradient-to-r from-[#d4e8ce] to-[#b8d6ae] rounded-2xl p-8 md:p-12 text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-800">🌿 Sell Your Green Ayurveda Products on Mera-Gide</h2>
    <p class="text-lg text-gray-700 mt-2">Reach thousands of wellness seekers.</p>
    <a class="inline-block mt-4 bg-[#2b6e3b] hover:bg-[#1f5230] text-white font-semibold px-10 py-3 rounded-full shadow-lg transition clickable" onclick="showToast('📝 Seller Registration')">Become a Seller</a>
  </section>

  <!-- ===== SHOP / PRODUCT GRID (demo) ===== -->
  <section class="mb-8">
    <div class="flex flex-wrap items-center justify-between gap-3 mb-4">
      <h2 class="text-2xl font-bold text-gray-800"><i class="fas fa-store mera-green"></i> Shop</h2>
      <div class="flex flex-wrap gap-2 text-sm">
        <select class="bg-white border border-mera-border rounded-full px-3 py-1.5" onchange="showToast('📂 Category: '+this.value)"><option>All Categories</option><option>Herbal</option><option>Ayurveda</option></select>
        <select class="bg-white border border-mera-border rounded-full px-3 py-1.5" onchange="showToast('📊 Sort: '+this.value)"><option>Price: Low to High</option><option>Price: High to Low</option></select>
        <button class="bg-mera-bg px-4 py-1.5 rounded-full text-gray-700 border border-mera-border clickable" onclick="showToast('🔍 Filter applied')"><i class="fas fa-filter"></i> Filter</button>
      </div>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Amla Powder - ₹249')"><div class="h-40 bg-mera-bg flex items-center justify-center text-4xl text-[#2b6e3b]"><i class="fas fa-seedling"></i></div><div class="p-3"><h4 class="font-bold">Amla Powder</h4><div class="flex items-center gap-2"><span class="font-bold text-[#2b6e3b]">₹249</span><span class="text-xs line-through">₹399</span></div><button class="w-full mt-2 bg-[#2b6e3b] text-white py-1 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')">Add to Cart</button></div></div>
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Shilajit Resin - ₹699')"><div class="h-40 bg-mera-bg flex items-center justify-center text-4xl text-[#2b6e3b]"><i class="fas fa-spa"></i></div><div class="p-3"><h4 class="font-bold">Shilajit Resin</h4><div class="flex items-center gap-2"><span class="font-bold text-[#2b6e3b]">₹699</span><span class="text-xs line-through">₹999</span></div><button class="w-full mt-2 bg-[#2b6e3b] text-white py-1 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')">Add to Cart</button></div></div>
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Tulsi Drops - ₹179')"><div class="h-40 bg-mera-bg flex items-center justify-center text-4xl text-[#2b6e3b]"><i class="fas fa-leaf"></i></div><div class="p-3"><h4 class="font-bold">Tulsi Drops</h4><div class="flex items-center gap-2"><span class="font-bold text-[#2b6e3b]">₹179</span><span class="text-xs line-through">₹250</span></div><button class="w-full mt-2 bg-[#2b6e3b] text-white py-1 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')">Add to Cart</button></div></div>
      <div class="bg-white rounded-2xl shadow card-shadow overflow-hidden product-card" onclick="showToast('📦 Moringa Caps - ₹399')"><div class="h-40 bg-mera-bg flex items-center justify-center text-4xl text-[#2b6e3b]"><i class="fas fa-mortar-pestle"></i></div><div class="p-3"><h4 class="font-bold">Moringa Caps</h4><div class="flex items-center gap-2"><span class="font-bold text-[#2b6e3b]">₹399</span><span class="text-xs line-through">₹550</span></div><button class="w-full mt-2 bg-[#2b6e3b] text-white py-1 rounded-full text-sm hover:bg-[#1f5230] transition" onclick="event.stopPropagation(); showToast('🛒 Added to Cart')">Add to Cart</button></div></div>
    </div>
  </section>

  <!-- ===== ADMIN / SELLER DASHBOARD preview (interactive) ===== -->
  <div class="grid md:grid-cols-3 gap-6 mb-8 p-4 bg-white rounded-2xl shadow card-shadow border border-mera-border">
    <div class="text-center clickable" onclick="showToast('📦 Total Products: 12')"><span class="text-2xl font-bold mera-green">12</span><p class="text-gray-600">Total Products</p></div>
    <div class="text-center clickable" onclick="showToast('⏳ Pending Approval: 3')"><span class="text-2xl font-bold text-yellow-500">3</span><p class="text-gray-600">Pending Approval</p></div>
    <div class="text-center clickable" onclick="showToast('💰 Total Sales: ₹24,500')"><span class="text-2xl font-bold text-green-600">₹24.5K</span><p class="text-gray-600">Total Sales</p></div>
  </div>

  <!-- ===== DISCLAIMER ===== -->
  <div class="text-xs text-gray-500 border-t border-gray-200 pt-6 mt-6 italic">
    <i class="fas fa-info-circle"></i> Ayurvedic products are not intended to diagnose, treat, cure, or prevent any disease. Consult your physician before use.
  </div>
</main>

<!-- ===== FOOTER ===== -->
<footer class="bg-[#1e3a2a] text-white mt-8">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 py-10 grid grid-cols-2 md:grid-cols-4 gap-8">
    <div><h4 class="font-bold text-lg flex items-center clickable" onclick="showToast('🌿 Mera-Gide')"><i class="fas fa-leaf mr-2"></i>Mera-Gide</h4><p class="text-sm text-gray-300 mt-2">Green Ayurveda marketplace</p></div>
    <div><h5 class="font-semibold">Quick</h5><ul class="text-sm text-gray-300 space-y-1 mt-2"><li class="clickable" onclick="showToast('🏠 Home')">Home</li><li class="clickable" onclick="showToast('🛍️ Shop')">Shop</li><li class="clickable" onclick="showToast('📖 About')">About</li><li class="clickable" onclick="showToast('📞 Contact')">Contact</li></ul></div>
    <div><h5 class="font-semibold">Customer</h5><ul class="text-sm text-gray-300 space-y-1 mt-2"><li class="clickable" onclick="showToast('👤 My Account')">My Account</li><li class="clickable" onclick="showToast('📦 My Orders')">My Orders</li><li class="clickable" onclick="showToast('🛒 Cart')">Cart</li></ul></div>
    <div><h5 class="font-semibold">Legal</h5><ul class="text-sm text-gray-300 space-y-1 mt-2"><li class="clickable" onclick="showToast('📜 Terms')">Terms</li><li class="clickable" onclick="showToast('🔒 Privacy')">Privacy</li><li class="clickable" onclick="showToast('↩️ Returns')">Returns</li><li class="clickable" onclick="showToast('🚚 Shipping')">Shipping</li></ul></div>
  </div>
  <div class="border-t border-gray-600 text-center text-sm text-gray-300 py-4 flex flex-wrap justify-center gap-4">
    <span>© 2026 Mera-Gide. All rights reserved.</span>
    <span>
      <i class="fab fa-instagram clickable" onclick="showToast('📸 Instagram')"></i> 
      <i class="fab fa-facebook ml-2 clickable" onclick="showToast('📘 Facebook')"></i> 
      <i class="fab fa-youtube ml-2 clickable" onclick="showToast('▶️ YouTube')"></i>
    </span>
  </div>
</footer>

<!-- Toast notification -->
<div id="toast" class="toast-message" style="display: none; transform: translateY(20px); opacity: 0;"></div>

<script>
  // Mobile hamburger toggle
  document.getElementById('hamburgerBtn')?.addEventListener('click', function() {
    document.getElementById('mobileMenu').classList.toggle('hidden');
  });
  function toggleMobile() {
    document.getElementById('mobileMenu')?.classList.add('hidden');
  }

  // Toast system
  let toastTimeout;
  function showToast(message) {
    const toast = document.getElementById('toast');
    toast.textContent = message;
    toast.style.display = 'block';
    toast.style.transform = 'translateY(0)';
    toast.style.opacity = '1';
    clearTimeout(toastTimeout);
    toastTimeout = setTimeout(() => {
      toast.style.transform = 'translateY(20px)';
      toast.style.opacity = '0';
      setTimeout(() => { toast.style.display = 'none'; }, 300);
    }, 2200);
  }

  // Click feedback for all interactive elements (optional)
  document.querySelectorAll('.clickable, .nav-link, button, select, .product-card').forEach(el => {
    if (!el.onclick) {
      el.addEventListener('click', function(e) {
        // if it doesn't have its own handler, we can add a subtle feedback
        if (!this.dataset.toast && !this.closest('.product-card')?.dataset.toast) {
          // only if not already handled
        }
      });
    }
  });

  // Quick demo: show toast on page load
  window.addEventListener('load', () => {
    setTimeout(() => showToast('🌿 Welcome to Mera-Gide!'), 400);
  });
</script>

</body>
</html>
