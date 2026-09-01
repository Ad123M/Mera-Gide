<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mera-Gide · Ayurveda</title>
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
    }

    body {
      background: #f5f2ec;
      color: #1e3a2f;
      padding: 1.5rem;
    }

    .container {
      max-width: 1300px;
      margin: 0 auto;
      background: #ffffff;
      border-radius: 32px;
      box-shadow: 0 20px 40px rgba(0, 20, 10, 0.08);
      padding: 2rem 2.5rem;
      transition: 0.25s;
    }

    /* ----- HEADER / LOGO & NAV ----- */
    .header {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      border-bottom: 2px solid #eae3da;
      padding-bottom: 1.2rem;
      margin-bottom: 2rem;
    }

    .logo-area {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-icon {
      background: #1e4d3a;
      color: #f5efe8;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      font-weight: 600;
      letter-spacing: -0.5px;
      box-shadow: 0 6px 12px rgba(26, 67, 45, 0.15);
    }

    .logo-text {
      font-size: 2rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      color: #1a3b2c;
    }
    .logo-text span {
      font-weight: 300;
      color: #5d7e6b;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      font-weight: 500;
    }
    .nav-links a {
      text-decoration: none;
      color: #2d4f3d;
      font-size: 1.05rem;
      transition: 0.2s;
      border-bottom: 2px solid transparent;
      padding-bottom: 4px;
    }
    .nav-links a:hover {
      border-bottom-color: #4b7b5e;
      color: #0d2b1d;
    }

    /* ----- ADMIN UPLOAD CARD (prominent) ----- */
    .admin-upload-section {
      background: #f0f7f2;
      border-radius: 28px;
      padding: 2rem 2.2rem;
      margin-bottom: 2.8rem;
      border: 1px solid #d7e3da;
      box-shadow: inset 0 2px 6px rgba(0,0,0,0.02);
    }

    .admin-upload-grid {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 1.5rem;
    }

    .upload-box {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .upload-box label {
      background: #ffffff;
      padding: 0.8rem 1.6rem;
      border-radius: 60px;
      border: 1px dashed #5f8b72;
      color: #1a3b2c;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 10px;
      transition: 0.2s;
      box-shadow: 0 2px 6px rgba(0,0,0,0.02);
    }
    .upload-box label:hover {
      background: #e4efe7;
      border-color: #2f6b4a;
    }
    .upload-box label i {
      color: #2a6b47;
      font-size: 1.3rem;
    }
    #fileInput {
      display: none;
    }
    .file-preview {
      font-size: 0.95rem;
      background: #fff;
      padding: 0.4rem 1.2rem;
      border-radius: 40px;
      color: #29543b;
      border: 1px solid #c6d9cd;
    }

    .admin-buttons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn {
      border: none;
      padding: 0.9rem 2.2rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 1rem;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      cursor: pointer;
      transition: 0.2s;
      background: #f0f0f0;
      color: #1e3a2f;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.02);
    }

    .btn-primary {
      background: #1e4d3a;
      color: white;
      box-shadow: 0 6px 14px rgba(27, 77, 53, 0.25);
    }
    .btn-primary:hover {
      background: #123b2b;
      transform: scale(1.01);
    }
    .btn-outline {
      background: transparent;
      border: 2px solid #1e4d3a;
      color: #1e4d3a;
    }
    .btn-outline:hover {
      background: #1e4d3a0c;
    }
    .btn-success {
      background: #1f6e47;
      color: white;
      box-shadow: 0 6px 14px rgba(27, 77, 53, 0.2);
    }
    .btn-success:hover {
      background: #135536;
    }
    .btn-warning {
      background: #cf9e4b;
      color: #1f2d21;
    }
    .btn-warning:hover {
      background: #c08d37;
    }

    /* ----- SELLER & PAYMENT PROCESS CARDS ----- */
    .process-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      margin: 2.5rem 0 2.8rem 0;
    }

    .process-card {
      background: #fafcfa;
      border-radius: 24px;
      padding: 1.8rem 1.8rem 2rem;
      border: 1px solid #e2ede6;
      transition: 0.2s;
      box-shadow: 0 6px 12px rgba(0, 20, 10, 0.02);
    }
    .process-card:hover {
      border-color: #b9cfc0;
      box-shadow: 0 12px 24px rgba(30, 60, 40, 0.06);
    }

    .process-card h3 {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 1.5rem;
      font-weight: 600;
      color: #173b2a;
      margin-bottom: 0.8rem;
    }
    .process-card h3 i {
      color: #2f6b4a;
      font-size: 1.8rem;
      width: 2rem;
    }
    .process-card p {
      color: #3f5f4b;
      margin-bottom: 1.6rem;
      line-height: 1.5;
    }

    .card-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin-top: 0.5rem;
    }
    .card-actions .btn {
      flex: 1 0 auto;
      justify-content: center;
    }

    /* ----- PRODUCT SHOWCASE (Griinar Ayurveda) ----- */
    .product-showcase {
      background: #eef5ef;
      border-radius: 28px;
      padding: 2rem 2.2rem;
      margin: 2.8rem 0 2.8rem 0;
      border: 1px solid #d3e2d7;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
    }

    .product-info {
      display: flex;
      align-items: center;
      gap: 1.8rem;
      flex-wrap: wrap;
    }
    .product-badge {
      background: #1e4d3a;
      color: #f3faf3;
      padding: 0.6rem 1.8rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 0.9rem;
      letter-spacing: 0.4px;
    }
    .product-name {
      font-size: 1.8rem;
      font-weight: 700;
      color: #0d3321;
    }
    .product-name small {
      font-weight: 400;
      font-size: 1rem;
      color: #3f6a51;
      margin-left: 8px;
    }

    .product-cta .btn {
      background: #274f39;
      color: white;
    }
    .product-cta .btn:hover {
      background: #0b3824;
    }

    /* ----- FOOTER LINKS (About, Contact, T&C, Privacy) ----- */
    .footer-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2.5rem 3.5rem;
      border-top: 2px solid #e3e9e3;
      padding-top: 2rem;
      margin-top: 2rem;
      font-size: 1rem;
    }

    .footer-links a {
      text-decoration: none;
      color: #2b4f3a;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: 0.15s;
      border-bottom: 1px solid transparent;
    }
    .footer-links a i {
      color: #346f4b;
      font-size: 1.1rem;
    }
    .footer-links a:hover {
      border-bottom-color: #346f4b;
      color: #0c291d;
    }

    .footer-copy {
      text-align: center;
      margin-top: 1.8rem;
      color: #5b7d68;
      font-size: 0.9rem;
      letter-spacing: 0.3px;
    }

    /* admin upload status */
    .upload-status {
      margin-top: 1rem;
      font-weight: 500;
      color: #1b4d34;
      background: #e2efe6;
      padding: 0.3rem 1.2rem;
      border-radius: 40px;
      display: inline-block;
    }

    /* responsive */
    @media (max-width: 700px) {
      .container { padding: 1.5rem; }
      .header { flex-direction: column; align-items: start; gap: 1rem; }
      .nav-links { gap: 1.2rem; }
      .admin-upload-grid { flex-direction: column; align-items: stretch; }
      .upload-box { flex-direction: column; align-items: stretch; }
      .admin-buttons { justify-content: stretch; }
      .admin-buttons .btn { flex: 1; justify-content: center; }
    }
  </style>
</head>
<body>

<div class="container">

  <!-- Header with logo -->
  <header class="header">
    <div class="logo-area">
      <div class="logo-icon">MG</div>
      <div class="logo-text">Mera<span>-Gide</span></div>
    </div>
    <div class="nav-links">
      <a href="#"><i class="fas fa-home"></i> Home</a>
      <a href="#"><i class="fas fa-seedling"></i> Shop</a>
      <a href="#"><i class="fas fa-user-md"></i> Ayurveda</a>
    </div>
  </header>

  <!-- ADMIN IMAGE UPLOAD SECTION (prominent) -->
  <section class="admin-upload-section">
    <div class="admin-upload-grid">
      <div class="upload-box">
        <label for="fileInput">
          <i class="fas fa-cloud-upload-alt"></i> Choose Image
        </label>
        <input type="file" id="fileInput" accept="image/*">
        <span class="file-preview" id="filePreview">No file selected</span>
      </div>
      <div class="admin-buttons">
        <button class="btn btn-primary" id="uploadBtn"><i class="fas fa-upload"></i> Upload</button>
        <button class="btn btn-outline" id="clearBtn"><i class="fas fa-undo-alt"></i> Clear</button>
      </div>
    </div>
    <div id="uploadStatus" class="upload-status"><i class="fas fa-check-circle"></i> Ready for upload</div>
  </section>

  <!-- SELLER + PAYMENT PROCESS (two cards) -->
  <div class="process-grid">
    <!-- Seller Process Card -->
    <div class="process-card">
      <h3><i class="fas fa-store-alt"></i> Seller Process</h3>
      <p>Verify & onboard sellers. Manage products, inventory, and orders seamlessly.</p>
      <div class="card-actions">
        <button class="btn btn-primary" id="sellerBtn"><i class="fas fa-user-check"></i> Start Seller</button>
        <button class="btn btn-outline" id="sellerStatusBtn"><i class="fas fa-info-circle"></i> Status</button>
      </div>
      <div id="sellerFeedback" style="margin-top: 14px; font-size:0.95rem; color: #1b5b3a;"></div>
    </div>

    <!-- Payment Process Card -->
    <div class="process-card">
      <h3><i class="fas fa-credit-card"></i> Payment Process</h3>
      <p>Secure payments, refunds & transaction history. Fast & reliable.</p>
      <div class="card-actions">
        <button class="btn btn-success" id="paymentBtn"><i class="fas fa-coins"></i> Proceed Payment</button>
        <button class="btn btn-warning" id="paymentHistoryBtn"><i class="fas fa-clock"></i> History</button>
      </div>
      <div id="paymentFeedback" style="margin-top: 14px; font-size:0.95rem; color: #1b5b3a;"></div>
    </div>
  </div>

  <!-- Griinar Ayurveda product banner (side) -->
  <div class="product-showcase">
    <div class="product-info">
      <span class="product-badge"><i class="fas fa-leaf"></i> Herbal</span>
      <span class="product-name">Griinar Ayurveda <small>· traditional wellness</small></span>
    </div>
    <div class="product-cta">
      <button class="btn"><i class="fas fa-shopping-bag"></i> Explore</button>
    </div>
  </div>

  <!-- FOOTER: About, Contact, Terms, Privacy -->
  <div class="footer-links">
    <a href="#"><i class="fas fa-info-circle"></i> About Us</a>
    <a href="#"><i class="fas fa-envelope"></i> Contact Us</a>
    <a href="#"><i class="fas fa-file-contract"></i> Terms & Conditions</a>
    <a href="#"><i class="fas fa-lock"></i> Privacy Policy</a>
  </div>
  <div class="footer-copy">
    <i class="fas fa-copyright"></i> 2026 Mera-Gide · Griinar Ayurveda
  </div>

</div>

<!-- JavaScript for interactions (upload, seller, payment) -->
<script>
  (function() {
    // DOM refs
    const fileInput = document.getElementById('fileInput');
    const filePreview = document.getElementById('filePreview');
    const uploadStatus = document.getElementById('uploadStatus');
    const uploadBtn = document.getElementById('uploadBtn');
    const clearBtn = document.getElementById('clearBtn');

    const sellerBtn = document.getElementById('sellerBtn');
    const sellerStatusBtn = document.getElementById('sellerStatusBtn');
    const sellerFeedback = document.getElementById('sellerFeedback');

    const paymentBtn = document.getElementById('paymentBtn');
    const paymentHistoryBtn = document.getElementById('paymentHistoryBtn');
    const paymentFeedback = document.getElementById('paymentFeedback');

    // ----- IMAGE UPLOAD (admin) -----
    fileInput.addEventListener('change', function(e) {
      if (this.files && this.files.length > 0) {
        filePreview.textContent = this.files[0].name;
        uploadStatus.innerHTML = `<i class="fas fa-file-image"></i> File ready: ${this.files[0].name}`;
      } else {
        filePreview.textContent = 'No file selected';
        uploadStatus.innerHTML = `<i class="fas fa-check-circle"></i> Ready for upload`;
      }
    });

    uploadBtn.addEventListener('click', function() {
      if (fileInput.files && fileInput.files.length > 0) {
        const fileName = fileInput.files[0].name;
        // Simulate upload process
        uploadStatus.innerHTML = `<i class="fas fa-spinner fa-pulse"></i> Uploading ${fileName} ...`;
        setTimeout(() => {
          uploadStatus.innerHTML = `<i class="fas fa-check-circle" style="color: #1a6e41;"></i> ✅ Image "${fileName}" uploaded successfully (admin)`;
          filePreview.textContent = fileName + ' ✓';
        }, 1200);
      } else {
        uploadStatus.innerHTML = `<i class="fas fa-exclamation-triangle" style="color:#b47d3a;"></i> No image selected. Please choose a file.`;
      }
    });

    clearBtn.addEventListener('click', function() {
      fileInput.value = '';
      filePreview.textContent = 'No file selected';
      uploadStatus.innerHTML = `<i class="fas fa-undo-alt"></i> Cleared. Ready for upload.`;
    });

    // ----- SELLER PROCESS -----
    let sellerActive = false;
    sellerBtn.addEventListener('click', function() {
      sellerActive = !sellerActive;
      if (sellerActive) {
        sellerFeedback.innerHTML = `<i class="fas fa-check-circle" style="color:#1d733d;"></i> Seller process started. Verification in progress...`;
        sellerBtn.innerHTML = '<i class="fas fa-pause-circle"></i> Stop Seller';
        sellerBtn.style.background = '#b18a4a';
      } else {
        sellerFeedback.innerHTML = `<i class="fas fa-stop-circle"></i> Seller process stopped.`;
        sellerBtn.innerHTML = '<i class="fas fa-user-check"></i> Start Seller';
        sellerBtn.style.background = '#1e4d3a';
      }
    });

    sellerStatusBtn.addEventListener('click', function() {
      const status = sellerActive ? '🟢 Active' : '⚪ Inactive';
      sellerFeedback.innerHTML = `<i class="fas fa-info-circle"></i> Seller status: ${status} (use "Start Seller" to toggle)`;
    });

    // ----- PAYMENT PROCESS -----
    let paymentActive = false;
    paymentBtn.addEventListener('click', function() {
      paymentActive = !paymentActive;
      if (paymentActive) {
        paymentFeedback.innerHTML = `<i class="fas fa-check-circle" style="color:#1d733d;"></i> Payment gateway active. Proceed with transaction.`;
        paymentBtn.innerHTML = '<i class="fas fa-ban"></i> Abort Payment';
        paymentBtn.style.background = '#ac6f3a';
      } else {
        paymentFeedback.innerHTML = `<i class="fas fa-times-circle"></i> Payment session ended.`;
        paymentBtn.innerHTML = '<i class="fas fa-coins"></i> Proceed Payment';
        paymentBtn.style.background = '#1f6e47';
      }
    });

    paymentHistoryBtn.addEventListener('click', function() {
      paymentFeedback.innerHTML = `<i class="fas fa-clock"></i> Showing recent payment history (demo) – last transaction: ₹499.00 (Griinar Churna)`;
    });

    // additional: click on product showcase (just feedback)
    document.querySelector('.product-cta .btn')?.addEventListener('click', function(e) {
      e.preventDefault();
      alert('🌿 Griinar Ayurveda – pure herbal products. Explore our range!');
    });

    // footer links demo (prevent navigation)
    document.querySelectorAll('.footer-links a').forEach(link => {
      link.addEventListener('click', function(e) {
        e.preventDefault();
        const text = this.innerText.trim();
        alert(`📄 ${text} – page will be displayed. (demo)`);
      });
    });

    // logo click (fun)
    document.querySelector('.logo-area')?.addEventListener('click', function() {
      alert('🌱 Mera-Gide · your Ayurveda companion');
    });

  })();
</script>

</body>
</html>
