   # 📖 Book Shopping Website Case Study

   Bu proje, modern web teknolojileri kullanılarak geliştirilmiş bir e-ticaret sitesi ürün sayfasıdır. Kullanıcıların ürünleri detaylı bir şekilde inceleyebileceği, farklı varyasyonları seçebileceği ve alışveriş sepetine ekleyebileceği zengin bir kullanıcı deneyimi sunmayı amaçlamaktadır.

   ![Vue](https://img.shields.io/badge/Vue.js-3-4FC08D?style=for-the-badge&logo=vue.js)
   ![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=for-the-badge&logo=vite)
   ![Pinia](https://img.shields.io/badge/Pinia-yellow?style=for-the-badge&logo=pine-script)
   ![Vue Router](https://img.shields.io/badge/Vue_Router-4-35495E?style=for-the-badge&logo=vue.js)
   ![Axios](https://img.shields.io/badge/Axios-blue?style=for-the-badge&logo=axios)
   ![MIT License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)

   ---

   ## 🖼️ Proje Görünümü

   *Projenizin bir ekran görüntüsünü veya GIF'ini buraya ekleyebilirsiniz.*

   ![Proje Ekran Görüntüsü](https://via.placeholder.com/800x450.png?text=Proje+Ekran+Görüntüsü)


   ## ✨ Özellikler

   - **📸 Ürün Galerisi:** Kullanıcıların ürünün birden fazla resmini küçük görsellerle veya ana resim olarak görüntülemesine olanak tanır.
   - **🎨 Varyasyon Seçimi:** Renk, model gibi farklı ürün varyantları arasında seçim yapma imkanı sunar.
   - **⭐ Müşteri Yorumları:** Diğer müşterilerin ürün hakkındaki yorumlarını ve puanlamalarını gösterir.
   - **🛒 Sepete Ekle:** Kullanıcılar ürünleri sepetlerine ekleyebilir ve alışverişe devam edebilir.
   - **🚚 Ücretsiz Kargo:** Tüm siparişlerde ücretsiz kargo avantajı sunulur.
   - **💰 Fiyatlandırma ve İndirimler:** Ürün fiyatları ve mevcut indirimler net bir şekilde sergilenir.
   - **📱 Duyarlı Tasarım:** Proje, farklı ekran boyutlarına (mobil, tablet, masaüstü) uyumlu olarak geliştirilmiştir.

   ## 🛠️ Kullanılan Teknolojiler

   - **Frontend:**
   - [**Vue 3**](https://vuejs.org/): Kullanıcı arayüzü oluşturmak için kullanılan ana JavaScript çatısı.
   - [**Vite**](https://vitejs.dev/): Hızlı ve modern bir geliştirme ortamı sunan build aracı.
   - [**Vue Router**](https://router.vuejs.org/): Tek sayfa uygulamalarında (SPA) yönlendirme işlemleri için kullanılır.
   - [**Pinia**](https://pinia.vuejs.org/): Vue uygulamaları için merkezi durum yönetimi (state management) kütüphanesi.
   - **Veri Alışverişi:**
   - [**Axios**](https://axios-http.com/): API istekleri yapmak için kullanılan popüler bir HTTP istemcisi.
   - **Stil ve İkonlar:**
   - **CSS / SCSS:** Bileşenlerin ve sayfa düzeninin stilendirilmesi için kullanılır.
   - [**Font Awesome**](https://fontawesome.com/): Proje genelinde ikon kullanımı için entegre edilmiştir.

   ## 📂 Proje Yapısı

   Projenin temel dosya yapısı aşağıda gösterilmiştir:

   ```
   /src
   ├── assets/         # Resimler, fontlar gibi statik varlıklar
   ├── components/     # Tekrar kullanılabilir Vue bileşenleri
   │   ├── Header.vue
   │   └── ProductDetails.vue
   ├── App.vue         # Ana Vue bileşeni
   ├── main.js         # Vue uygulamasının başlangıç noktası
   └── style.css       # Global stil dosyası
   ```

   ## 🚀 Kurulum ve Başlatma

   Projeyi yerel makinenizde çalıştırmak için aşağıdaki adımları izleyin:

   1.  **Depoyu klonlayın:**
      ```bash
      git clone https://github.com/kullanici-adiniz/proje-adiniz.git
      cd proje-adiniz
      ```

   2.  **Bağımlılıkları yükleyin:**
      Tercih ettiğiniz paket yöneticisini kullanabilirsiniz:
      ```bash
      # npm ile
      npm install

      # yarn ile
      yarn install

      # pnpm ile
      pnpm install
      ```

   3.  **Geliştirme sunucusunu başlatın:**
      ```bash
      npm run dev
      ```
      Uygulama varsayılan olarak `http://localhost:5173` adresinde çalışacaktır.

   ### 📜 Kullanılabilir Komutlar

   - `npm run dev`: Geliştirme sunucusunu başlatır.
   - `npm run build`: Projeyi üretim için derler ve `dist` klasörünü oluşturur.
   - `npm run preview`: Üretim derlemesini yerel olarak test etmek için bir sunucu başlatır.

   ## 🤝 Katkıda Bulunma

   Bu projeye katkıda bulunmak isterseniz, lütfen aşağıdaki adımları izleyin:

   1.  Bu depoyu **fork**'layın.
   2.  Yeni bir özellik veya düzeltme için kendi dalınızı oluşturun (`git checkout -b ozellik/yeni-ozellik`).
   3.  Değişikliklerinizi yapın ve **commit**'leyin (`git commit -m 'Yeni bir özellik eklendi'`).
   4.  Dalınızı ana depoya **push**'layın (`git push origin ozellik/yeni-ozellik`).
   5.  Bir **Pull Request** (PR) açın.

   ## 📄 Lisans

   Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.
