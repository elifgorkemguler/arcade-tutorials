# On Game + Sprite + Splash @unplugged
Bu mini uygulamada iki şeyi birlikte yapacaksın:
1) Ekrana bir **splash** mesajı göstermek
2) **On game update** bloğunun *içinde* bir **sprite** oluşturmak

## 1. Splash mesajını göster
Aşağıdaki blok, oyunun başında kısa bir mesaj gösterir.
```blocks
game.splash("Merhaba Arcade!", "Hazırsan başlayalım")
```

## 2. On game update bloğunu ekle
Oyunun akışı sırasında belirli aralıklarla çalışacak bir blok ekleyelim. Süreyi 2000 ms bırakabilirsin.
```blocks
game.onUpdateInterval(2000, function () {
	
})
```

## 3. Sprite bloğunu bu bloğun içine yerleştir
`On game update` bloğunun **içine** bir sprite oluşturma bloğu ekle ve basit bir görsel kullan.
```blocks
game.onUpdateInterval(2000, function () {
    let nesne = sprites.create(img`
        . . . 5 . . .
        . . 5 5 5 . .
        . 5 5 5 5 5 .
        . . 5 5 5 . .
        . . . 5 . . .
        . . . . . . .
        . . . . . . .
        . . . . . . .
    `, SpriteKind.Player)
})
```

## 4. Çalıştır
**Play/Simulator** düğmesine bas. Her 2 saniyede bir ekranda yeni bir sprite oluştuğunu göreceksin.
