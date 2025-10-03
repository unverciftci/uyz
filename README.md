# Üretken Yapay Zekaya Giriş - Ders Notları

## 1. Giriş ve Temel Kavramlar

### 1.1 Yapay Zeka Nedir?

Yapay zeka (AI - Artificial Intelligence), makinelerin insan benzeri zeka gerektiren görevleri yerine getirmesini sağlayan teknolojiler bütünüdür. Bu görevler şunları içerir:
- Öğrenme
- Problem çözme
- Karar verme
- Dil anlama ve üretme
- Görsel algılama

### 1.2 Üretken Yapay Zeka (Generative AI)

**Üretken AI**, yeni içerik oluşturabilen yapay zeka sistemleridir. Geleneksel AI sistemlerinden farkı, sadece analiz yapmak veya sınıflandırmak yerine özgün içerik üretebilmesidir.

**Üretebileceği içerik türleri:**
- Metin (makaleler, kod, şiir)
- Görüntü (resim, çizim, fotoğraf)
- Ses (müzik, konuşma)
- Video
- 3D modeller

### 1.3 Geleneksel AI vs Üretken AI

**Geleneksel AI (Ayırt Edici/Discriminative AI):**
- Veriyi sınıflandırır veya etiketler
- Örnek: Bir resmin kedi mi köpek mi olduğunu söyler
- Karar verir, tahmin eder

**Üretken AI:**
- Yeni veri örnekleri oluşturur
- Örnek: Kedi resmi çizer
- Yaratıcı çıktılar üretir

---

## 2. Üretken AI'ın Tarihsel Gelişimi

### 2.1 Önemli Kilometre Taşları

**2014 - GANs (Generative Adversarial Networks)**
- Ian Goodfellow tarafından geliştirildi
- İki sinir ağının rekabet ederek öğrenmesi prensibine dayanır
- Gerçekçi görüntü üretiminde çığır açtı

**2017 - Transformer Mimarisi**
- "Attention is All You Need" makalesi ile tanıtıldı
- Modern dil modellerinin temelini oluşturdu
- Paralel işleme ve uzun mesafe bağımlılıklarını anlama yeteneği

**2018-2020 - GPT Serisi**
- GPT-1, GPT-2, GPT-3 modellerinin geliştirilmesi
- Dil modellerinde devasa ölçekleme
- GPT-3: 175 milyar parametre

**2021-2022 - Diffusion Modelleri**
- DALL-E, Midjourney, Stable Diffusion
- Metin-görüntü dönüşümünde büyük başarı
- Yüksek kaliteli görsel üretim

**2022-2025 - Yaygın Kullanım Dönemi**
- ChatGPT'nin piyasaya sürülmesi
- Claude, Gemini gibi alternatif modeller
- Multimodal modeller (metin, görüntü, ses birlikte)

---

## 3. Temel Teknolojiler ve Mimariler

### 3.1 Derin Öğrenme (Deep Learning)

Üretken AI'ın temelinde derin öğrenme yatar. Çok katmanlı sinir ağları kullanarak karmaşık kalıpları öğrenir.

**Temel Bileşenler:**
- Nöronlar: Bilgi işleyen temel birimler
- Katmanlar: Nöronların organize edildiği yapılar
- Ağırlıklar: Öğrenilen parametreler
- Aktivasyon fonksiyonları: Non-lineer dönüşümler

### 3.2 Transformer Mimarisi

Modern dil modellerinin kalbi olan transformer mimarisi, self-attention mekanizmasına dayanır.

**Temel Özellikler:**
- Self-Attention: Dizinin farklı pozisyonlarına farklı önem verir
- Paralel İşleme: RNN'lerin aksine paralel çalışabilir
- Pozisyonel Kodlama: Kelime sırasını anlamak için
- Encoder-Decoder Yapısı: Girdi işleme ve çıktı üretme

**Avantajları:**
- Uzun mesafe bağımlılıklarını yakalama
- Daha hızlı eğitim
- Daha iyi ölçeklenebilirlik

### 3.3 Büyük Dil Modelleri (LLM - Large Language Models)

Milyarlarca kelime üzerinde eğitilen, insan dilini anlayan ve üreten dev modellerdir.

**Eğitim Süreci:**
1. **Pre-training (Ön Eğitim):** Büyük metin korpusu üzerinde denetimsiz öğrenme
2. **Fine-tuning (İnce Ayar):** Spesifik görevler için özelleştirme
3. **RLHF (Reinforcement Learning from Human Feedback):** İnsan geri bildirimiyle iyileştirme

**Önemli LLM'ler:**
- GPT serisi (OpenAI)
- Claude (Anthropic)
- Gemini (Google)
- LLaMA (Meta)

### 3.4 Diffusion Modelleri

Görüntü üretiminde kullanılan, gürültüden net görüntü elde etme prensibine dayanan modellerdir.

**Çalışma Prensibi:**
1. Forward Process: Temiz görüntüye adım adım gürültü ekleme
2. Reverse Process: Gürültüden temiz görüntüyü geri elde etme
3. Eğitim: Gürültü giderme sürecini öğrenme

**Popüler Modeller:**
- DALL-E 3
- Stable Diffusion
- Midjourney
- Imagen

---

## 4. Prompt Engineering (İstem Mühendisliği)

### 4.1 Prompt Nedir?

Prompt, üretken AI sistemine verilen talimattır. İyi bir prompt, kaliteli çıktı almanın anahtarıdır.

### 4.2 Etkili Prompt Yazma Teknikleri

**1. Açık ve Net Olun**
- Kötü: "Makale yaz"
- İyi: "Yapay zekanın eğitimdeki etkileri hakkında 500 kelimelik bir makale yaz"

**2. Bağlam Sağlayın**
- Kötü: "Kod yaz"
- İyi: "Python'da bir CSV dosyasını okuyup, pandas DataFrame'e dönüştüren kod yaz"

**3. Format Belirtin**
- "Yanıtını madde madde ver"
- "Tablo formatında göster"
- "JSON formatında çıktı ver"

**4. Örnekler Verin (Few-Shot Learning)**
```
Girdi: Hava çok güzel.
Duygu: Pozitif

Girdi: Bu çok kötü bir deneyimdi.
Duygu: Negatif

Girdi: Bugün markete gittim.
Duygu: ?
```

**5. Rol Atayın**
- "Sen bir Python uzmanısın..."
- "Sen bir pazarlama danışmanısın..."

**6. Adım Adım Düşünmeyi Teşvik Edin**
- "Adım adım düşünerek çöz"
- "Chain of thought" yaklaşımı

### 4.3 Yaygın Prompt Hataları

- Çok belirsiz talimatlar
- Bağlam eksikliği
- Çelişkili istekler
- Aşırı karmaşık promptlar

---

## 5. Üretken AI'ın Uygulama Alanları

### 5.1 Metin Üretimi

**İçerik Oluşturma:**
- Blog yazıları
- Sosyal medya içerikleri
- Ürün açıklamaları
- E-posta şablonları

**Yazılım Geliştirme:**
- Kod üretimi
- Kod açıklaması
- Debugging yardımı
- Dökümantasyon yazımı

**Akademik Çalışmalar:**
- Araştırma özetleme
- Literatür taraması
- Fikir üretimi
- Metin düzenleme

### 5.2 Görüntü Üretimi

**Tasarım ve Sanat:**
- Konsept tasarımları
- Dijital sanat eserleri
- Logo ve marka görselleri
- İllüstrasyonlar

**Pazarlama:**
- Reklam görselleri
- Ürün mockup'ları
- Sosyal medya görselleri

**Oyun ve Film Endüstrisi:**
- Karakter tasarımları
- Ortam konseptleri
- Texture üretimi

### 5.3 Ses ve Müzik

- Müzik kompozisyonu
- Ses efektleri
- Sesli kitap anlatımı
- Podcast üretimi
- Dil çevirisi ve dublaj

### 5.4 Video Üretimi

- Kısa video klipleri
- Animasyonlar
- Eğitim videoları
- Deepfake teknolojisi

### 5.5 Kod ve Yazılım

- Otomatik kod tamamlama
- Test kodu üretimi
- Kod refactoring önerileri
- API dökümantasyonu

---

## 6. Etik ve Toplumsal Etkiler

### 6.1 Önemli Etik Sorunlar

**1. Telif Hakkı ve Fikri Mülkiyet**
- AI'ın ürettiği içeriğin sahipliği kime ait?
- Eğitim verilerindeki telif hakları
- Sanatçıların haklarının korunması

**2. Yanlış Bilgi ve Manipülasyon**
- Deepfake videoları
- Sahte haber üretimi
- Sosyal mühendislik saldırıları
- Akademik sahtekarlık

**3. Önyargı ve Adalet**
- Eğitim verilerindeki önyargılar
- Cinsiyet ve ırk ayrımcılığı
- Temsiliyetsizlik sorunları

**4. İş Gücü ve İstihdam**
- Otomasyon ve işsizlik
- Yeni meslek alanları
- Beceri dönüşümü gereksinimleri

**5. Gizlilik**
- Kişisel veri kullanımı
- Veri güvenliği
- İzin ve rıza meselesi

### 6.2 Sorumlu AI Kullanımı

**En İyi Uygulamalar:**
- Üretilen içeriği doğrulama
- AI kullanımını şeffaf açıklama
- İnsan denetimi sağlama
- Etik kılavuzlara uyma
- Önyargıları tanıma ve azaltma

### 6.3 Yasal Düzenlemeler

**AB AI Yasası (AI Act)**
- Risk tabanlı yaklaşım
- Yüksek riskli uygulamalar için katı kurallar

**Diğer Düzenlemeler:**
- Veri koruma yasaları (GDPR, KVKK)
- Telif hakkı modernizasyonu
- Sektörel düzenlemeler

---

## 7. Teknik Kavramlar

### 7.1 Model Parametreleri

**Parametre:** Modelin öğrendiği ağırlık ve bias değerleri
- GPT-3: 175 milyar parametre
- GPT-4: Bilinmiyor (tahmini 1+ trilyon)
- Daha fazla parametre ≠ Her zaman daha iyi

### 7.2 Context Window (Bağlam Penceresi)

Modelin bir seferde işleyebileceği token (kelime parçası) miktarı.
- GPT-3.5: 4K-16K token
- GPT-4: 8K-128K token
- Claude 3: 200K token

### 7.3 Temperature (Sıcaklık)

Modelin ne kadar "yaratıcı" olacağını kontrol eden parametre.
- Düşük (0-0.3): Deterministik, tahmin edilebilir
- Orta (0.5-0.7): Dengeli
- Yüksek (0.8-1.0): Yaratıcı, rastgele

### 7.4 Fine-tuning vs RAG

**Fine-tuning:**
- Modeli spesifik veri üzerinde yeniden eğitme
- Kalıcı değişiklik
- Daha maliyetli

**RAG (Retrieval Augmented Generation):**
- Modele dış bilgi kaynağı sağlama
- Anlık bilgi erişimi
- Daha esnek ve güncel

### 7.5 Hallucination (Halüsinasyon)

AI'ın gerçek olmayan bilgileri kendinden emin bir şekilde üretmesi.

**Nedenleri:**
- Eğitim verilerindeki eksiklikler
- Modelin aşırı genelleme yapması
- Pattern matching'in limitleri

**Önleme Yolları:**
- Cevapları doğrulama
- Kaynak isteme
- Temperature'ı düşürme
- RAG kullanımı

---

## 8. Pratik Uygulamalar ve Araçlar

### 8.1 Popüler Üretken AI Araçları

**Metin:**
- ChatGPT (OpenAI)
- Claude (Anthropic)
- Gemini (Google)
- Copilot (Microsoft)

**Görsel:**
- DALL-E 3 (OpenAI)
- Midjourney
- Stable Diffusion
- Adobe Firefly

**Kod:**
- GitHub Copilot
- Amazon CodeWhisperer
- Tabnine
- Replit AI

**Ses/Müzik:**
- ElevenLabs
- Mubert
- AIVA
- Soundraw

### 8.2 API Kullanımı

Üretken AI modellerine programatik erişim için API'ler kullanılır.

**Temel Adımlar:**
1. API anahtarı alma
2. İstek (request) oluşturma
3. Yanıt (response) işleme
4. Hata yönetimi

**Python Örneği (Konsept):**
```python
import openai

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": "Sen yardımcı bir asistansın."},
        {"role": "user", "content": "Python'da liste nedir?"}
    ],
    temperature=0.7
)

print(response.choices[0].message.content)
```

### 8.3 Model Değerlendirme Metrikleri

**Metin için:**
- BLEU: Çeviri kalitesi
- ROUGE: Özetleme kalitesi
- Perplexity: Model belirsizliği

**Görsel için:**
- FID (Fréchet Inception Distance)
- IS (Inception Score)
- İnsan değerlendirmesi

---

## 9. Gelecek Trendleri

### 9.1 Multimodal AI

Metin, görüntü, ses ve video gibi farklı modaliteleri birlikte işleyebilen modeller.

**Örnekler:**
- GPT-4 Vision
- Gemini Ultra
- Claude 3

**Uygulamalar:**
- Görsel sorgulama
- Video analizi ve üretimi
- Çok modlu etkileşim

### 9.2 Küçük ve Verimli Modeller

Daha az kaynak kullanan, cihaz üzerinde çalışabilen modeller.

**Avantajları:**
- Düşük maliyet
- Gizlilik (veri yerel kalır)
- Hızlı yanıt
- İnternet bağımlılığı yok

### 9.3 Agentic AI

Özerk görevler yapabilen, araç kullanan, plan yapabilen AI sistemleri.

**Yetenekler:**
- Çoklu adımlı problem çözme
- Araç kullanımı (web arama, hesaplama vb.)
- Hedef belirleme ve planlama
- Çevreyle etkileşim

### 9.4 Kişiselleştirilmiş AI

Bireysel kullanıcılara özgü, kişisel verilerle özelleştirilmiş modeller.

**Uygulamalar:**
- Kişisel asistanlar
- Özel eğitim sistemleri
- Sağlık takibi
- Üretkenlik araçları

---

## 10. Öğrenme Kaynakları

### 10.1 Online Kurslar

- Coursera: Deep Learning Specialization (Andrew Ng)
- Fast.ai: Practical Deep Learning for Coders
- DeepLearning.AI: Generative AI courses
- Stanford CS224N: NLP with Deep Learning

### 10.2 Kitaplar

- "Deep Learning" - Ian Goodfellow, Yoshua Bengio, Aaron Courville
- "Generative Deep Learning" - David Foster
- "Natural Language Processing with Transformers" - Lewis Tunstall et al.

### 10.3 Araştırma Kaynakları

- arXiv.org: AI araştırma makaleleri
- Papers with Code: Kod ile makaleler
- Hugging Face: Model ve dataset merkezi
- Google Scholar: Akademik arama

### 10.4 Topluluklar

- Reddit: r/MachineLearning, r/artificial
- Discord: Çeşitli AI toplulukları
- Twitter/X: AI araştırmacılarını takip
- Stack Overflow: Teknik sorular

---

## Özet ve Sonuç

Üretken yapay zeka, teknoloji dünyasında devrim niteliğinde bir gelişmedir. Metin, görüntü, ses ve video gibi farklı modalitelerde yeni içerikler üretebilme yeteneği, sayısız uygulama alanı yaratmaktadır.

**Önemli Çıkarımlar:**
- Üretken AI hızla gelişiyor ve yaygınlaşıyor
- Temel teknolojileri anlamak önemli (transformers, diffusion)
- Prompt engineering kritik bir beceri
- Etik kullanım ve sorumluluk şart
- Sürekli öğrenme gerekli

**Geleceğe Bakış:**
Üretken AI teknolojisi, eğitimden sağlığa, sanattan bilime kadar her alanda dönüştürücü etki yaratacak. Bu teknolojileri anlayan, etik çerçevede kullanan ve geliştiren bireyler, geleceğin dijital dünyasında önemli roller üstleneceklerdir.

---

## Sorular ve Tartışma Konuları

1. Üretken AI'ın sanat ve yaratıcılık üzerindeki etkileri nelerdir?
2. AI tarafından üretilen içeriğin yasal statüsü ne olmalıdır?
3. Hallucination sorununu tamamen çözmek mümkün mü?
4. Küçük vs büyük modeller tartışması: Hangisi daha sürdürülebilir?
5. İnsan-AI işbirliği nasıl optimize edilebilir?
6. Üretken AI'ın eğitim sistemleri üzerindeki uzun vadeli etkileri neler olacak?

---

**Son Güncelleme:** Ekim 2025  
**Hazırlayan:** Claude (Anthropic)
