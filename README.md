# Open-craft
Using various AI models on my own (Gemini, Qwen, DeepSeek, and ChatGPT), I created my own game inspired by Minecraft.



🇹🇷 Türkçe Açıklama

Genel Bakış

Bu oyun tarayıcı üzerinde çalışan, kurulum gerektirmeyen bir voxel hayatta kalma oyunudur. Tüm grafikler, kullanıcı arayüzü, fizik sistemi ve oyun mantığı tek HTML dosyasında bulunur. Three.js kullanılarak gerçek zamanlı 3B dünya oluşturulur. minecraft_pe_final.html

Dünya

* 200×200 blok büyüklüğünde dünya
* 64 blok yükseklik
* Dinamik arazi oluşturma
* Tepeler
* Ağaçlar
* Taş katmanları
* Toprak
* Çimen
* Kum
* Demir cevheri
* Kömür cevheri

Dünya tamamen kod ile üretilmektedir (procedural generation). 

Bloklar

Oyunda şu bloklar bulunur:

* Tahta
* Kütük
* Yaprak
* Cam
* Kum
* Taş
* Çimen
* Toprak
* Çalışma masası
* Fırın
* Demir cevheri
* Kömür cevheri
* Kırıktaş
* Meşale

Ayrıca envanter eşyaları:

* Kömür
* Odun kömürü
* Çubuk
* Demir külçesi

minecraft_pe_final.html

Gerçekçi Işık Sistemi

Oyunun en dikkat çekici kısmı budur.

Minecraft’a benzer şekilde:

* Meşaleler ışık yayar.
* Işık duvarlardan geçmez.
* Cam ve yaprak gibi saydam bloklardan geçebilir.
* BFS (Breadth First Search) algoritması ile ışık hesaplanır.
* Gündüz ve gece farklı aydınlatma kullanılır.

Bu sistem klasik voxel ışıklandırmasına oldukça yakındır. minecraft_pe_final.html

Fizik

Oyunda birçok fizik kuralı vardır:

* Kum boşlukta düşer.
* Desteksiz meşaleler kırılır.
* Ağaç kesildiğinde bağlantısı kopan yapraklar zamanla çürür.
* Oyuncu bloklarla çarpışır.
* Yer çekimi uygulanır.

minecraft_pe_final.html

Oynanış

Oyuncu:

* yürüyebilir
* zıplayabilir
* blok kırabilir
* blok yerleştirebilir
* envanter kullanabilir
* üretim yapabilir
* fırın kullanabilir

Ayrıca:

* Hayatta Kalma modu
* Yaratıcı mod
* Uçuş modu
* Gündüz/Gece geçişi

bulunmaktadır. 

Mobil Arayüz

Tamamen telefonlar için tasarlanmıştır.

İçerir:

* Sanal joystick
* Kamera kontrol alanı
* Zıplama tuşu
* Kırma tuşu
* Yerleştirme tuşu
* Envanter
* Hotbar
* FPS göstergesi
* Koordinatlar

minecraft_pe_final.html

Grafikler

Dokuların tamamı kodla oluşturuluyor.

Hiçbir PNG kullanılmıyor.

Her blok:

* Canvas üzerinde çiziliyor.
* Pixel-art görünümü korunuyor.
* Nearest Filter kullanılıyor.
* Mipmap kapalı.
* Minecraft’ın eski dokularına benzer sade stil hedefleniyor.

minecraft_pe_final.html

Performans

Kod performans için çeşitli optimizasyonlar içeriyor:

* Instanced Mesh
* Render mesafesi
* Görünmeyen blokları çizmeme
* Dinamik ışık güncellemesi
* Yakındaki fizik hesaplamaları

Bu sayede mobil cihazlarda daha yüksek FPS hedefleniyor. minecraft_pe_final.html

⸻

🇬🇧 English Description

Overview

This project is a browser-based voxel sandbox game inspired by the early versions of Minecraft Pocket Edition. It runs entirely inside a single HTML file using Three.js, with no installation required. All gameplay systems, graphics, UI, and world generation are implemented directly in JavaScript. minecraft_pe_final.html

World

The game features a procedurally generated voxel world consisting of:

* 200 × 200 blocks
* 64-block build height
* Hills and terrain variation
* Trees
* Grass
* Dirt
* Stone
* Sand
* Iron ore
* Coal ore

Every world is generated dynamically through code rather than prebuilt maps. minecraft_pe_final.html

Gameplay Features

Players can:

* Explore the world
* Break blocks
* Place blocks
* Collect resources
* Manage an inventory
* Craft items
* Use crafting tables
* Smelt materials inside furnaces

The game also includes:

* Survival Mode
* Creative Mode
* Flying
* Day/Night switching

minecraft_pe_final.html

Advanced Lighting

One of the project’s strongest technical features is its voxel lighting engine.

It includes:

* Torch-based dynamic lighting
* BFS light propagation
* No light leaking through solid blocks
* Light transmission through transparent blocks
* Separate sunlight and torch lighting
* Dynamic brightness calculations

This closely resembles the lighting behavior found in classic Minecraft. minecraft_pe_final.html

Physics

The game simulates several Minecraft-inspired mechanics:

* Falling sand
* Unsupported torches breaking
* Leaf decay after tree removal
* Collision detection
* Gravity
* Player movement physics

minecraft_pe_final.html

Mobile Controls

The interface is designed specifically for touchscreen devices and includes:

* Virtual joystick
* Camera look area
* Jump button
* Break button
* Place button
* Inventory system
* Hotbar
* FPS counter
* Coordinates display

minecraft_pe_final.html

Graphics

Instead of image assets, every texture is generated procedurally using the HTML Canvas API, resulting in a lightweight pixel-art appearance inspired by early Minecraft PE. minecraft_pe_final.html

Performance

The engine is optimized for mobile hardware using techniques such as:

* Instanced rendering
* Limited render distance
* Hidden-face culling
* Dynamic lighting updates
* Localized physics simulation

These optimizations help maintain smooth performance while rendering thousands of voxel blocks. 
