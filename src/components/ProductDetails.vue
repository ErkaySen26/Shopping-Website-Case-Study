<template>
  <div class="product-container">
    <div class="breadcrumb">
      <span>Ana Sayfa</span> / <span>Takı & Aksesuar</span> / <span>Erkek Gözlük</span> / <span>Retro Moda Punk Buhar Stili...</span>
    </div>
    
    <div class="product-main">
      <div class="product-gallery">
        <div class="thumbnail-list">
          <div v-for="(image, index) in thumbnails" 
               :key="index"
               class="thumbnail-wrapper"
               @click="selectedImage = image">
            <img :src="image" 
                 :class="['thumbnail-image', { active: selectedImage === image }]"
                 alt="Ürün küçük resim" />
          </div>
        </div>
        <div class="main-image-container">
          <img :src="selectedImage" alt="Ürün ana görsel" class="main-image" />
          <button class="share-button">
            <i class="fas fa-share-alt"></i>
          </button>
        </div>
      </div>

      <div class="product-info">
        <h1 class="product-title">
          Retro Moda Punk Buhar Stili Gözlükler, Kare Çerçeveli Erkek ve Kadın Parti Dekoratif Gözlük
        </h1>

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

        <div class="price-section">
          <div class="price">
            <span class="amount">94</span>
            <span class="decimal">,05 TL</span>
          </div>
          <div class="original-price">
            <span>TEFF 464,10 TL</span>
            <span class="price-info">Tavsiye edilen perakende satış fiyatı nedir?</span>
          </div>
        </div>

        <div class="shipping-info highlight">
          <i class="fas fa-check"></i>
          <span>Tüm siparişlerde ücretsiz kargo</span>
          <span class="tag">İnanılmaz</span>
        </div>

        <div class="variant-section">
          <div class="variant-title">Renk: Siyah Çerçeve/gri Film</div>
          <div class="variant-options">
            <div v-for="(variant, index) in variants" 
                 :key="index"
                 :class="['variant-item', { active: selectedVariant === index }]"
                 @click="selectedVariant = index">
              <img :src="variant.image" :alt="variant.name" />
              <span class="variant-name">{{ variant.name }}</span>
            </div>
          </div>
        </div>

        <div class="quantity-section">
          <label>Miktar</label>
          <select v-model="quantity" class="quantity-select">
            <option v-for="n in 10" :key="n" :value="n">{{ n }}</option>
          </select>
        </div>

        <button class="add-to-cart">
          Sepete Ekle
        </button>

        <div class="additional-info">
          <div class="info-item">
            <i class="fas fa-box"></i>
            <span>Vergi ve Gümrük Politikası</span>
            <i class="fas fa-chevron-right"></i>
          </div>
          <div class="info-item">
            <i class="fas fa-truck"></i>
            <span>Tüm siparişlerde ücretsiz kargo</span>
            <div class="delivery-time">Teslimat: 8-26 Nis</div>
          </div>
          <div class="info-item">
            <i class="fas fa-shield-alt"></i>
            <span>Alışveriş güvenliği</span>
            <i class="fas fa-chevron-right"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductDetails',
  data() {
    return {
      selectedImage: '/images/gozluk-1.jpg',
      thumbnails: [
        '/images/gozluk-1.jpg',
        '/images/gozluk-2.jpg',
        '/images/gozluk-3.jpg',
        '/images/gozluk-4.jpg'
      ],
      variants: [
        { name: 'Gümüş Çerçeve', image: '/images/gumus.jpg' },
        { name: 'Gümüş Çerçeve/mavi', image: '/images/gumus.jpg' },
        { name: 'Siyah Çerçeve/gri', image: '/images/siyah.jpg' }
      ],
      selectedVariant: 0,
      quantity: 1
    }
  }
}
</script>

<style scoped>
.product-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.breadcrumb {
  color: #666;
  font-size: 14px;
  margin-bottom: 20px;
}

.breadcrumb span {
  cursor: pointer;
}

.breadcrumb span:hover {
  color: #f27a1a;
}

.product-main {
  display: flex;
  gap: 40px;
}

.product-gallery {
  flex: 1;
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
}

.thumbnail-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.thumbnail-image.active {
  border: 2px solid #f27a1a;
}

.main-image-container {
  flex: 1;
  position: relative;
}

.main-image {
  width: 100%;
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

.product-info {
  flex: 1;
}

.product-title {
  font-size: 20px;
  margin-bottom: 15px;
  color: #333;
}

.product-meta {
  margin-bottom: 20px;
}

.rating {
  display: flex;
  align-items: center;
  gap: 8px;
}

.rating-score {
  font-weight: bold;
}

.stars {
  color: #f27a1a;
}

.badges {
  margin-top: 10px;
}

.badge {
  display: inline-block;
  padding: 4px 8px;
  margin-right: 8px;
  border-radius: 4px;
  font-size: 12px;
}

.seller-badge {
  background-color: #e7f3ef;
  color: #0bc15c;
}

.price-section {
  margin: 20px 0;
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
  margin-top: 5px;
}

.shipping-info.highlight {
  background-color: #fff5eb;
  padding: 12px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 20px 0;
}

.tag {
  background-color: #f27a1a;
  color: white;
  padding: 2px 8px;
  border-radius: 4px;
  font-size: 12px;
  margin-left: auto;
}

.variant-section {
  margin: 20px 0;
}

.variant-title {
  margin-bottom: 10px;
  font-weight: bold;
}

.variant-options {
  display: flex;
  gap: 10px;
}

.variant-item {
  border: 2px solid #ddd;
  padding: 5px;
  cursor: pointer;
  text-align: center;
  border-radius: 4px;
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

.quantity-section {
  margin: 20px 0;
}

.quantity-select {
  padding: 8px;
  border: 1px solid #ddd;
  border-radius: 4px;
  width: 100px;
}

.add-to-cart {
  width: 100%;
  padding: 15px;
  background-color: #f27a1a;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  margin-bottom: 20px;
}

.add-to-cart:hover {
  background-color: #d86500;
}

.additional-info {
  border-top: 1px solid #eee;
  padding-top: 20px;
}

.info-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 12px 0;
  border-bottom: 1px solid #eee;
  color: #666;
}

.delivery-time {
  margin-left: auto;
  color: #333;
}
</style>
