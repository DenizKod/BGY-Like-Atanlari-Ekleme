# Like-Atanlar--Ekleme

### ADIM 1

<p>- Facebook dilini Türkçe yap</p>
<p>- Tampermonkey eklentisi tarayıcınıza ekleyin</p>
<p>- Yeni Betik oluştura tıklayın</p>

![image](https://github.com/DenizKod/ARK-ISTEGI-IPTAL-ETME/assets/168285638/7e1b2696-803e-447a-ae3f-f7844a44d28f)

### Aşağıdaki kodu kopyala betik sayfasındaki tüm kodları baştan sona sil ve bunu ekle. "dosya" sekmesine tıkla ve "kaydet"
```
// ==UserScript==
// @name         Like atanları ekleme F2 ile çalışır
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Like atanları ekleme F2 ile çalışır
// @author       Deniz KOD
// @match        www.facebook.com/groups/bgyagain3
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    document.addEventListener('keydown', function(e) {
        if (e.key === 'F2') {
            console.log("Arkadaş ekleme işlemi başlatıldı.");
            addFriendsAutomatically();
        }
    });

    function addFriendsAutomatically() {
        const friendButtons = document.querySelectorAll('div[aria-label="Arkadaş Ekle"]');
        friendButtons.forEach(button => {
            button.click();
            console.log("Arkadaş Ekle butonuna tıklandı.");
        });

        if (friendButtons.length === 0) {
            console.log("Daha fazla 'Arkadaş Ekle' butonu bulunamadı.");
        }
    }
})();
```

F2 tuşuna basınca çalışır.
