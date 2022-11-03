<h1 align="center">Mina Protocol Berkley Testnet (ZKapp oluşturma)

## Mina Protocol, Layer-1 blok zincirleri arasında “minimal” blok zinciri olarak tanımlanan ve bilinen en hafif blok zinciri olma ünvanına sahiptir. Ölçeklendirme adına gelecekte çok fazla konuşulacak bir proje (boyut sadece 22kb). Bu Test işlemlerinin herhangi bir getirisi yok sadece eğitim amaçlı öğrenmek isteyenler için anlatıyorum ilerleyen zamanlarda ödüllü testneti gelecek, yayınlanınca sizlerle paylaşacağız.

## Video [Linki](https://youtu.be/jf5dvWblYek) 

## Sunucuyu nerden nasıl alacağınızı bilmiyorsanız node eğitim serimizi izleyebilirsiniz. [Node Eğitim Serisi](https://www.youtube.com/playlist?list=PLKxGUfdcj7MVXls2OvTpwx6CnpVJN685w) veya bir önce kurduğumuz manta suncunuzu sıfırlayarak kurabilirsiniz işlemler tamamlandıktan sonra sunucuyu isterseniz tamamen silebilirsiniz. 
 
![image](https://docs.minaprotocol.com/img/homepage/zkapp_developers.png)
## Tekrar hatırlatalım ödüllü bir testnet değil sadece projeyi ilerlyen zamnlarda çok sık duyacağımızı düşünüyoruz bu yüzden öğrenmek hepimiz için iyi olacaktır.

### Sistem Gereksinimleri
 - kurulum için sistemin özellikleri çok önemli değil, zaten bitirdikten sonra vps sıfırlayacağız dileyen arkadaşlar silebilir. kurulumu için node js üzerinde ilerleteceğiz, ben ubunutu üzerinde node js kurarak devam edeceğim dilerseniz aldığınız sunucuyu direk nodejs uyumlu alabilirsiniz.
 - NodeJS 16+
 - NPM 6+
 - Git 2+
 - disk boyutu önemsiz

 # Kurulum için 2 tane seçeneğimiz bulunuyor isterseniz kendi örneğinizi oluşturabilirsiniz, örnek kurulum üzerinden devam edeceğim. [Burdan](https://docs.minaprotocol.com/zkapps/how-to-write-a-zkapp) option B veya diğer detaylarıda kontrol edebilirsiniz.

<h1 align="center">Örnek Kurulum

  ## Root yetkisi almak için aşağğıdaki kodu giriyoruz bazı sunucularda bunu sürekli girmemiz gerekiyor. eğer bunu girmezseniz yazdığınız kodun başına sudo komutunu yazarkata devam edebilirsiniz ancak karışıklık olmaması için aşğıdaki komutu yazmanızı tavsiye ederim. ( root: Windows cihazlarda olduğu gibi yönetici olarak çalıştırmamıza, yani bize yetki veren bir komuttur.)
  ```
  sudo su
  cd
  ```

 ## Aşşağıdaki komutlarla sunucumuzdaki güncellemeleri, yükseltmeleri kontrol ediyoruz, sondaki -y işareti gelen onay işlemlerini otamatik olarak onaylanmasını sağlayacaktır.

  ```
 sudo apt-get update && sudo apt-get upgrade -y
  ```

 ## Bu komut ile bize gerekli olan dependencies ları indiriyoruz:Bağımlılık (dependency) kurulumda ihtiyaç duyduğumuz dışarıdan eklediğimiz kaynaklar ya da bileşenlerdir.

 ```
sudo apt install curl git build-essential
 ```

  ## Bizden istenilen özelliklere uygun olarak node kuruyoruz
   ```
sudo apt-get install nodejs
 ```
```
sudo apt install npm
```
 ## versiyonları kontrol ediyoruz çıktıda 16 üstü değilse yükseltme yapamamız gerekiyor örnek olara versiyon cıktısı 10 ile başlıyorsa 10. versiyon kurulu, bu yüzden yükseltme gerekiyor.
```
nodejs -v
```

```
npm -v
```
  
   ## Yükseltme gerekiyorsa burdaki komutları ekleyip 18'e yükseltebilirsiniz.
   
   ```
   curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```
   ```
sudo apt-get install nodejs
```
# Versiyonları kontrol edelim. versiyon çıktısı node için 18 ile başlarsa sorun yok.

```
node -v
```

```
npm -v
```

## Zkapp kurulumu:
  ```
  npm install -g zkapp-cli
  ```
 ```
zk example sudoku
```
# eğer init hatası verirse yani giriş isterse alttaki komutları kendinize göre düzenleyip devam edin Email adresinizi ve isim yazın.

```
git config --global user.email (mail adresiniz)
```
```
git config --global user.name (kullanıcı ismi)
```
```
cd sudoku
```
```
npm run test
```
```
npm run build
```
```
npm run start
```
 
 
```
zk config
```
# 
-Chose a name: berkeley 
-Apı url: https://proxy.berkeley.minaexplorer.com/graphql
-Transaction fee: 0.1

Çıktıda verilen linki alıp tarayıcımıza yapıştırıyoruz daha sonra Request diyip test tokenleri alıyoruz. yeni bloğun oluşmasını bekliyoruz videodan görebilirsiniz.

##Yeni Blok oluştuktan sonra 

```
zk deploy berkeley
 
  ```
işlemler bukadar videodaki gibi çıktı aldıysanız sorun yok berkeley test ağına bir işlem göndermiş olduk.

Mina [Discord](https://discord.gg/minaprotocol)
 

