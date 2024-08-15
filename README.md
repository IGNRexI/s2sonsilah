# https://discord.gg/cso2

Bu proje, Son Silah (S2) oyunu için geliştirilmiş bir oyun sunucu emülatörüdür. Bu emülatör, oyunun bazı temel fonksiyonlarını taklit eder ve oyunun sunucu tarafındaki iletişimi yönetir.

## Serveri Çalıştırmak İçin Yapılması Gerekenler.
- therawserver'in çalışması için oyunun dosyalarını çıkartmanız gerekiyor
- oyunun dosyalarını çıkartmak için Game Klasörüne ArchiveExtractor.exe Atıyorsunuz ve o klasör de olan Game.Res00 dosyasını ArchiveExtractor.exe üzerine sürükleyerek bırakıyorsunuz. dosyalar çıktıktan sonra Extracted klasörün içinde oluyor klasöre girip ctrl-a yap sağ tık yap sonra kes yazısına bas. sonra geri gelip ctrl-v tusuna bas bu kadar.
- geri gelip Default.archcfg dosyasını editliyorsunuz ve içideki herşeyi silip sadece Game yazıyorsunuz.
- bu verdiğim [game.rar](https://s6.dosya.tc/server21/eibrvk/Game.rar.html)'ı indir aç içinde verdiğim GameClient.dll GameServer.dll şu iki dosyayı game klasörüne at.
- [s2.rar](https://s2.dosya.tc/server31/ldi0p0/s2.rar.html) bu indir aç bunun içindekileri direkt theraw.exe'nin olduğu dizine atın.
- sonra LaunchServer.bat çalıştırın sonra Shell.exe çalıştırın sonra hooks.ct açın (cheat engine) kurulu olması lazım. cheat engine ekranı geldiğinde therawserver.exeyi seçip listedekli kutulara tıklamanız lazım.
- sonra lobi.js serveri başlatın therawserver.exe direkt bağlanacaktır. (sonrasında login.js serveri başlatabilirsiniz.)
## Emeği Geçenler (bu liste sürekli güncellenecektir) :)

- Agumon (oihd)
- CauSXOXO
- rssvxoxo
- TRojen610
- akiy33 (aki6)

## İndirilmesi Gerekenler.
- **TheRaw.Exe** https://s2.dosya.tc/server31/px4l3u/TheRaw.exe.html
- **Start.Bat** Start TheRaw.exe -arch game +windowed 1 -windowtitle "S2 Son Silah" +EnablePrefetch 1  +gs_ip 127.0.0.1 +gs_port 12000 +FlashDevMode 1.0 +ShowLog 1.0 +DediLog 1.0 +FlashRecieveLog 1.0 -noextra

## Özellikler

- **Kullanıcı Giriş:** Kullanıcı adı ve şifre ile kullanıcı doğrulaması yapar.
- **Sunucu Listesi:** Bağlanılabilir sunucuların listesini sağlar.
- **Channel Listesi:** Bağlanılabilir kanalların listesini sağlar.

## Bağımlılıklar

- Node.js
- uuid

## Başlatma

Sunucuyu başlatmak için aşağıdaki adımları izleyin:

1. Gerekli bağımlılıkları yükleyin:
    ```bash
    npm install
    ```

2. Login Serveri başlatın:
    ```bash
    node login.js
    ```
2. Lobi Serveri başlatın:
    ```bash
    node lobi.js
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
- **Zaten Giriş Yaptınız:** 0x210101
- **Giriş Başarısız:** 0x210102
- **İsim Girmediniz:** 0x210201
- **Yasaklı Kelime İçermektedir:** 0x210202
- **İsminiz Çok Kısa:** 0x210203
- **İsminiz Çok Uzun:** 0x210204
- **Zaten Dükkandasınız:** 0x240101
---

## Fotoğraflar
Kullanıcı adı veya şifre yanlış girildiğinde aşağıdaki hata mesajını alırsınız:
![image](https://github.com/user-attachments/assets/6a7d0399-903a-4a46-a351-87d4134ddadc)

![image](https://github.com/user-attachments/assets/e4b7d274-dc3c-429a-a6b3-06b3df667ef2)

![image](https://github.com/user-attachments/assets/6a4e9f86-e6bc-4f94-af8b-42c90f6eed13)

![image](https://github.com/user-attachments/assets/5b76a785-3397-40b6-871c-1a2cc440c285)

![image](https://github.com/user-attachments/assets/7ec26525-1155-4738-a346-80a96fb78ae1)



---
## Lisans

MIT lisansı altında lisanslıdır, daha fazla bilgi için LICENSE konusuna bakın.

Bu projenin Joygame ile bağlantısı yoktur. S2 Son Silah bu şirkete aittir.
