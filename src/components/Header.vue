<template>
  <header class="header">
    <!-- Üst bant -->
    <div class="top-banner">
      <div class="banner-content">
        <div class="banner-left">
          <i class="fas fa-truck"></i>
          <span>Ücretsiz kargo > <span class="highlight">İnanılmaz</span></span>
        </div>
        <div class="banner-center">
          <i class="fas fa-shopping-cart"></i>
          <span>Sipariş alt limiti MyShop'da birtakım sipariş alt sınırları vardır.</span>
        </div>
        <div class="banner-right">
          <i class="fas fa-mobile-alt"></i>
          <span>MyShop Uygulamasını İndirin</span>
        </div>
      </div>
    </div>

    <!-- Ana header -->
    <div class="main-header">
      <div class="header-content">
        <!-- Logo -->
        <a href="/" class="logo">
          <img
            src="/public/images/store.png"
            alt="MyShop"
            class="logo-image"
          />
        </a>

        <!-- Menü -->
        <div class="nav-items">
          <a href="#" class="nav-item">
            <i class="fas fa-fire"></i>
            En Çok Satan Ürünler
          </a>
          <a href="#" class="nav-item">
            <i class="fas fa-star"></i>
            5 Yıldızlı
          </a>
          <a href="#" class="nav-item">Yeni gelenler</a>
          <div class="dropdown">
            <button class="dropdown-btn">
              Kategoriler
              <i class="fas fa-chevron-down"></i>
            </button>
          </div>
        </div>

        <!-- Arama Kutusu -->
        <div class="search-container">
          <div class="search-bar">
            <input type="text" placeholder="glasses" />
            <button class="search-btn">
              <i class="fas fa-search"></i>
            </button>
          </div>
        </div>

        <!-- Kullanıcı İşlemleri -->
        <div class="user-actions">
          <a href="#" class="action-item user">
            <i class="fas fa-user"></i>
            <div class="action-text">
              <span>Oturum aç / Kayıt</span>
              <span class="sub-text">Siparişler ve Hesap</span>
            </div>
          </a>
          <a href="#" class="action-item">
            <i class="fas fa-question-circle"></i>
            <span>Destek</span>
          </a>
          <a href="#" class="action-item">
            <div class="language-selector">
              <span class="flag">🇹🇷</span>
              <span>TR</span>
            </div>
          </a>
          <!-- Sepet -->
          <a href="#" class="action-item cart">
            <!-- Büyütülmüş sepet ikonu ve metin -->
            <i class="fas fa-shopping-cart cart-icon"></i>
            <span>Sepetim</span>
          </a>
        </div>
      </div>
    </div>

    <!-- Breadcrumb -->
    <nav class="breadcrumb">
      <div class="breadcrumb-content">
        <a href="/">Ana Sayfa</a>
        <span class="separator">/</span>
        <a href="/taki-aksesuar">Takı & Aksesuar</a>
        <span class="separator">/</span>
        <a href="/erkek-gozluk">Erkek Gözlük</a>
        <span class="separator">/</span>
        <span class="current">Retro Moda Punk Buhar Stili...</span>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
/* Genel header ayarları */
.header {
  width: 100%;
  background: white;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
}

/* Üst banner */
.top-banner {
  background: #000;
  color: white;
  height: 32px;
  display: flex;
  align-items: center;
}
.banner-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  width: 100%;
}
.banner-left, .banner-center, .banner-right {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
}
.banner-left i, .banner-center i, .banner-right i {
  color: #90EE90;
  font-size: 16px;
}
.highlight {
  color: #90EE90;
}

/* Ana header */
.main-header {
  height: 68px;
  border-bottom: 1px solid #e5e5e5;
  display: flex;
  align-items: center;
  background: white;
}
.header-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 32px;
  padding: 0 20px;
  width: 100%;
}

/* Logo */
.logo {
  width: 90px;
  display: flex;
  align-items: center;
  text-decoration: none;
}
.logo-image {
  width: 100%;
  height: auto;
}

/* Menü öğeleri */
.nav-items {
  display: flex;
  align-items: center;
  gap: 24px;
  margin-right: 16px;
}
.nav-item {
  display: flex;
  align-items: center;
  gap: 6px;
  color: #111;
  text-decoration: none;
  font-size: 13px;
  white-space: nowrap;
  font-weight: 500;
}
.nav-item i {
  font-size: 16px;
}

/* Açılır kategori butonu */
.dropdown-btn {
  display: flex;
  align-items: center;
  gap: 6px;
  background: none;
  border: none;
  cursor: pointer;
  font-size: 13px;
  color: #111;
  font-weight: 500;
}

/* Arama kutusu */
.search-container {
  flex: 1;
  max-width: 580px;
}
.search-bar {
  display: flex;
  align-items: center;
  background: #f3f3f3;
  border-radius: 20px;
  padding: 0 16px;
  height: 40px;
  border: 2px solid transparent;
}
.search-bar:focus-within {
  border-color: #111;
}
.search-bar input {
  flex: 1;
  border: none;
  background: none;
  height: 100%;
  font-size: 14px;
  padding: 0;
}
.search-bar input:focus {
  outline: none;
}
.search-bar input::placeholder {
  color: #666;
}
.search-btn {
  background: #111;
  border: none;
  color: white;
  cursor: pointer;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Kullanıcı işlemleri */
.user-actions {
  display: flex;
  align-items: center;
  gap: 40px;
  margin-left: 16px;
  width: auto;
}

/* Buton & öğe stilleri */
.action-item {
  display: flex;
  align-items: center;
  gap: 10px;
  color: #111;
  text-decoration: none;
  font-size: 14px;
  padding: 8px 16px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
  white-space: nowrap;
}
.action-item:hover {
  background-color: #f3f3f3;
}
.action-item.user {
  gap: 12px;
  font-size: 15px;
}
.action-text {
  display: flex;
  flex-direction: column;
  line-height: 1.2;
  text-align: left;
}
.sub-text {
  color: #666;
  font-size: 12px;
}

/* Sepet ikonunu büyütüp yanına "Sepetim" yazdık */
.cart-icon {
  font-size: 20px; /* Mevcut boyuttan daha büyük isterseniz 24px veya 28px yapabilirsiniz */
  margin-right: 6px;
}

/* Dil seçimi */
.language-selector {
  display: flex;
  align-items: center;
  gap: 4px;
}
.flag {
  font-size: 16px;
}

/* Breadcrumb */
.breadcrumb {
  background: white;
  border-bottom: 1px solid #e5e5e5;
  padding: 12px 0;
}
.breadcrumb-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
}
.breadcrumb a {
  color: #666;
  text-decoration: none;
}
.breadcrumb a:hover {
  color: #111;
}
.breadcrumb .separator {
  color: #666;
}
.breadcrumb .current {
  color: #111;
}
</style>
