<template>
  <div class="product-container">
    <!-- Kategori Yolu -->
    <div class="breadcrumb">
      <span>Ana Sayfa</span> / 
      <span>Takı & Aksesuar</span> / 
      <span>Erkek Gözlük</span> / 
      <span>Retro Moda Punk Buhar Stili...</span>
    </div>
    
    <!-- Ürün Sayfası Ana Alan -->
    <div class="product-main">
      <!-- Sol Kolon: Görseller & Yorumlar -->
      <div class="left-column">
        <!-- Ürün Galerisi -->
        <div class="product-gallery">
          <div class="thumbnail-list">
            <div 
              v-for="(image, index) in thumbnails"
              :key="index"
              class="thumbnail-wrapper"
              @click="selectedImage = image"
            >
              <img 
                :src="image" 
                :class="['thumbnail-image', { active: selectedImage === image }]"
                alt="Ürün küçük resim"
              />
            </div>
          </div>
          <div class="main-image-container">
            <img :src="selectedImage" alt="Ürün ana görsel" class="main-image" />
            <button class="share-button">
              <i class="fas fa-share-alt"></i>
            </button>
          </div>
        </div>
        
        <!-- Müşteri Yorumları -->
        <div class="review-section">
          <!-- Üst Kısım: Toplam İnceleme, Ortalama Puan ve Onay Mesajı -->
          <div class="review-overview">
            <h2 class="review-count-title">2.198 İnceleme</h2>
            <div class="review-average">
              <span class="review-average-score">4.7</span>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
              </div>
            </div>
            <div class="verification-text">Tüm incelemeler doğrulanmıştır</div>
          </div>
          
          <!-- Örnek Yorum Kartı (Yıldız Kaldırıldı) -->
          <div class="review-item">
            <div class="review-author">
              Ezgi Ekin 
              <span class="review-date">- 28 Eyl 2024</span>
              <span class="review-latest">• En yeni</span>
            </div>
            <!-- BURADAKİ YILDIZ KISMI KALDIRILDI
            <div class="review-stars">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star-half-alt"></i>
            </div>
            -->
            <div class="review-text">
              Gayet kaliteli, beğendim.
            </div>
          </div>
        </div>
      </div>
      
      <!-- Sağ Kolon: Ürün Bilgileri -->
      <div class="product-info">
        <!-- Üst Kısım: Başlık, Değerlendirme, Rozetler -->
        <div class="product-header">
          <br>
          <h1 class="product-title">
            Retro Moda Punk Buhar Stili Gözlükler, Kare Çerçeveli Erkek ve Kadın Parti Dekoratif Gözlük
          </h1>
          <br/>
          <div class="product-meta">
            <div class="rating">
              <span class="rating-score">4.7</span>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
              </div>
              <span class="review-count">(2.198 inceleme)</span>
            </div>
            <div class="badges">
              <span class="badge seller-badge">En Çok Satan Ürün</span>
              <span class="badge category">Erkek Gözlük İçinde</span>
            </div>
          </div>
        </div>
        
        <!-- Fiyat Bölümü -->
        <div class="price-section">
          <div class="price">
            <span class="amount">94</span>  
            <span class="decimal">,05 TL</span>
            <span class="price-info">Tavsiye edilen perakende satış fiyatı nedir?</span>
          </div>
          <div class="original-price">
          </div>
          <!-- Ücretsiz Kargo Bilgisi / Tek Satır -->
          <div class="free-shipping-text">
            <i class="fas fa-check" style="color: #0bc15c;"></i>
            Tüm siparişlerde ücretsiz kargo
          </div>
        </div>

        <!-- Varyant (Renk Seçimi) -->
        <div class="variant-section">
          <div class="variant-title">Renk: Siyah Çerçeve/gri Film</div>
          <div class="variant-options">
            <div 
              v-for="(variant, index) in variants"
              :key="index"
              :class="['variant-item', { active: selectedVariant === index }]"
              @click="selectedVariant = index"
            >
              <img :src="variant.image" :alt="variant.name" />
              <span class="variant-name">{{ variant.name }}</span>
            </div>
          </div>
        </div>

        <!-- Miktar Seçimi -->
        <div class="quantity-section">
          <label>Miktar</label>
          <select v-model="quantity" class="quantity-select">
            <option v-for="n in 10" :key="n" :value="n">{{ n }}</option>
          </select>
        </div>

        <!-- Sepete Ekle Butonu + İndirim Etiketi -->
        <div class="cart-button-wrapper">
          <button class="add-to-cart">Sepete Ekle</button>
          <span class="discount-badge">%10 İNDİRİM</span>
        </div>

        <!-- Ek Bilgiler / Alt Kısım -->
        <div class="additional-info">
          <!-- Vergi & Gümrük -->
          <div class="info-item">
            <i class="fas fa-box"></i>
            <div class="info-texts">
              <strong>Vergi ve Gümrük Politikası</strong>
              <p>Tüm ithalat vergilerinin tashi ettiği için siparişten sonra herhangi bir ek ödeme gerekmez.</p>
            </div>
          </div>
          <!-- Kargo Detayları -->
          <div class="info-item">
            <i class="fas fa-truck"></i>
            <div class="info-texts">
              <strong>Tüm siparişlerde ücretsiz kargo</strong>
              <p>Teslimat: 8-26 Nis | Kargo şirketi: MNG • ARAS</p>
              <p>Ücretsiz iade • Fiyat Düzenleme</p>
            </div>
          </div>
          <!-- Alışveriş Güvenliği -->
          <div class="info-item">
            <i class="fas fa-shield-alt"></i>
            <div class="info-texts">
              <strong>Alışveriş güvenliği</strong>
              <p>• Güvenli Ödeme Seçenekleri</p>
              <p>• Güvenli lojistik</p>
              <p>• Gizliliği koru</p>
              <p>• Satın alma koruması</p>
            </div>
          </div>
        </div>
      </div> <!-- product-info Sonu -->
    </div> <!-- product-main Sonu -->
  </div>
</template>

<script>
export default {
  name: 'ProductDetails',
  data() {
    return {
      /* Seçili ana görsel */
      selectedImage: '/images/1.png',
      
      /* Küçük resimler */
      thumbnails: [
        '/images/1.png',
        '/images/2.png',
        '/images/3.png',
        '/images/4.png'
      ],
      
      /* Varyantlar (örnek) */
      variants: [
        { name: 'Gümüş Çerçeve',       image: '/images/1.png' },
        { name: 'Gümüş Çerçeve/mavi',  image: '/images/2.png' },
        { name: 'Siyah Çerçeve/gri',    image: '/images/3.png' }
      ],
      
      /* Hangi varyant seçili */
      selectedVariant: 0,
      
      /* Miktar */
      quantity: 1
    }
  }
}
</script>

<style scoped>
/* Örnek (Mevcut CSS'nizle aynıysa eklemeyebilirsiniz) */

/* Genel Container */
.product-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  font-family: sans-serif;
}

/* Breadcrumb */
.breadcrumb {
  font-size: 14px;
  margin-bottom: 20px;
  color: #666;
}
.breadcrumb span {
  cursor: pointer;
  transition: color 0.3s;
}
.breadcrumb span:hover {
  color: #f27a1a;
}

/* Ana Alan */
.product-main {
  display: flex;
  gap: 40px;
  align-items: flex-start;
}

/* --- SOL KOLON (Galeri + Yorumlar) --- */
.left-column {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 30px;
}

/* Galeri */
.product-gallery {
  display: flex;
  gap: 20px;
}
.thumbnail-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.thumbnail-wrapper {
  width: 60px;
  height: 60px;
  border: 1px solid #ddd;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.thumbnail-image {
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
  transition: border 0.3s;
}
.thumbnail-image.active {
  border: 2px solid #f27a1a;
}
.main-image-container {
  flex: 1;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid #eee;
  padding: 10px;
  background: #fff;
}
.main-image {
  max-width: 100%;
  height: auto;
}
.share-button {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: white;
  border: none;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  cursor: pointer;
}

/* Yorumlar */
.review-section {
  border-top: 1px solid #eee;
  padding-top: 20px;
}
.review-overview {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 16px;
  margin-bottom: 16px;
}
.review-count-title {
  font-size: 18px;
  font-weight: bold;
  margin: 0;
}
.review-average {
  display: flex;
  align-items: center;
  gap: 8px;
}
.review-average-score {
  font-size: 20px;
  font-weight: bold;
  color: #f27a1a;
}
.stars {
  color: #f27a1a;
  display: flex;
  gap: 2px;
}
.verification-text {
  font-size: 13px;
  color: #0bc15c;
}
.review-item {
  margin-bottom: 20px;
  border-bottom: 1px solid #eee;
  padding-bottom: 15px;
}
.review-author {
  font-weight: bold;
  color: #333;
  margin-bottom: 4px;
}
.review-date,
.review-latest {
  font-size: 13px;
  color: #999;
  margin-left: 5px;
}
/* review-stars KALDIRILDI */

/* Tekil yorum metni */
.review-text {
  font-size: 14px;
  color: #444;
  margin-top: 4px;
}

/* --- SAĞ KOLON (Ürün Bilgileri) --- */
.product-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

/* Başlık & Meta */
.product-header {
  margin-bottom: 15px;
}
.product-title {
  font-size: 22px;
  font-weight: 600;
  color: #333;
  margin: 0;
  line-height: 1.4;
}
.product-meta {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.rating {
  display: flex;
  align-items: center;
  gap: 8px;
}
.rating-score {
  font-weight: bold;
}
.review-count {
  color: #666;
  font-size: 14px;
}
/* Badges */
.badges {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 4px;
}
.badge {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  font-size: 12px;
}
.seller-badge {
  background-color: #e7f3ef;
  color: #0bc15c;
}
.category {
  background-color: #eaf2ff;
  color: #3971e6;
}

/* Fiyat Bölümü */
.price-section {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.price {
  font-size: 32px;
  font-weight: bold;
}
.decimal {
  font-size: 24px;
}
.original-price {
  color: #666;
  font-size: 14px;
}
.price-info {
  display: block;
  font-size: 12px;
  color: #888;
  margin-top: 3px;
}
.free-shipping-text {
  font-size: 14px;
  color: #333;
  display: flex;
  align-items: center;
  gap: 6px;
}

/* Varyant Bölümü */
.variant-section {
  margin-top: 10px;
}
.variant-title {
  margin-bottom: 10px;
  font-weight: bold;
  font-size: 14px;
}
.variant-options {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}
.variant-item {
  border: 2px solid #ddd;
  padding: 5px;
  cursor: pointer;
  text-align: center;
  border-radius: 4px;
  transition: border-color 0.3s;
  width: 100px;
}
.variant-item.active {
  border-color: #f27a1a;
}
.variant-item img {
  width: 60px;
  height: 60px;
  object-fit: cover;
}
.variant-name {
  display: block;
  font-size: 12px;
  margin-top: 5px;
}

/* Miktar Bölümü */
.quantity-section {
  display: flex;
  align-items: center;
  gap: 10px;
}
.quantity-section label {
  font-weight: bold;
}
.quantity-select {
  padding: 6px;
  border: 1px solid #ddd;
  border-radius: 4px;
  width: 80px;
}

/* Sepete Ekle + İndirim */
.cart-button-wrapper {
  display: flex;
  align-items: center;
  gap: 10px;
}
.add-to-cart {
  padding: 14px 20px;
  background-color: #f27a1a;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s;
}
.add-to-cart:hover {
  background-color: #d86500;
}
.discount-badge {
  background-color: #0bc15c;
  color: #fff;
  padding: 4px 8px;
  border-radius: 4px;
  font-weight: bold;
  font-size: 13px;
}

/* Alt Bilgiler */
.additional-info {
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid #eee;
  font-size: 14px;
  line-height: 1.4;
}

.info-item {
  margin-bottom: 16px;
}
.info-texts strong {
  font-size: 14px;
  color: #333;
}
.info-texts p {
  margin: 4px 0 0 0;
  color: #444;
  font-size: 13px;
}
</style>
