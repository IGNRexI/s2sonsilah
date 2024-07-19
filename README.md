# Game Server Emulator for Son Silah (S2)

Bu proje, Son Silah (S2) oyunu için geliştirilmiş bir oyun sunucu emülatörüdür. Bu emülatör, oyunun bazı temel fonksiyonlarını taklit eder ve oyunun sunucu tarafındaki iletişimi yönetir.

## Özellikler

- **Kullanıcı Giriş:** Kullanıcı adı ve şifre ile kullanıcı doğrulaması yapar.
- **Sunucu Listesi:** Bağlanılabilir sunucuların listesini sağlar.
- **Komut Satırı Kontrolü:** Sunucuyu komut satırından yönetebilmek için konsol komutları sağlar.

## Bağımlılıklar

- Node.js
- uuid
- winston

## Başlatma

Sunucuyu başlatmak için aşağıdaki adımları izleyin:

1. Gerekli bağımlılıkları yükleyin:
    ```bash
    npm install
    ```

2. Sunucuyu başlatın:
    ```bash
    node server.js
    ```

## Proje Yapısı

- `Packet` sınıfı: Gelen veri paketlerini işler.
- `GameServer` sınıfı: Sunucu bağlantılarını yönetir ve gelen verileri işler.
- `GameClient` sınıfı: Bağlı olan istemciyi temsil eder.
- `GameDatabase` sınıfı: Kullanıcı doğrulamasını yapar ve kullanıcı bilgilerini yönetir.

## Komutlar

- `userlist`: Bağlı olan kullanıcıların listesini gösterir.

---

## Önemli Notlar

- **CN (Client Notify):** İstemci bildirimleri.
- **SN (Server Notify):** Sunucu bildirimleri.
- **CQ (Client Query):** İstemci sorguları.
- **SA (Server Answer):** Sunucu yanıtları.
- **NN (Client/Server Notify):** İstemci/Sunucu bildirimleri.

Bu iki satır kod hata kodu ve hata sebebini temsil eder:
```js
writeUInt16LE(0, 6);
writeUInt32LE(0, 8);
```
