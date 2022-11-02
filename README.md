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

 # kurulum için 2 tane seçeneğimiz bulunuyor isterseniz kendi örneğinizi oluşturabilirsiniz örnek kurulum üzerinden devam edeceğim. [Burdan] diğer detaylarıda kontrol edebilirsiniz.

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
sudo apt install curl git build-essential \
 ```

  ## Bizden istenilen özelliklere uygun olarak node js kuruyoruz
   ```
sudo apt-get install nodejs
 ```
```
sudo apt install npm
```
 ## versiyonları kontrol ediyoruz çıktıda 16 üstü değilse yükseltme yapamazız gerekiyor örnek olara 10 ile başlıyorsa versiyon cıktısı yükseltme gerekiyor.
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
# Versiyonları tekrar kontrol edelim.

```
node -v
```

```
npm -v
```

## Zkapp kurlumu:
  ```
  npm install -g zkapp-cli
  ```
zk example sudoku

npm run test

npm run testw

npm run build

zk config

https://proxy.berkeley.minaexplorer.com/graphql

 ## Temel gereksinimler sunucu güncelleme

  ```
 sudo apt update && sudo apt upgrade -y
  ```

 ## Sonrasında aşağıdaki komutları sırasıyla giriyoruz.

 ```
sudo apt install git pkg-config build-essential libssl-dev curl jq
 ```
 ```
curl https://sh.rustup.rs -sSf | sh -s -- -y
 ```
 ```
source $HOME/.cargo/env
 ```
 ```
git clone https://github.com/Manta-Network/manta-rs.git
 ```

 ```
cd manta-rs
 ``` 
 ```
cargo run --release --package manta-trusted-setup --all-features --bin groth16_phase2_client register
 ```  
  
## Şimdi kayıt işlemlerini yapıyoruz Buraya twitter kullanıcı adımızı yazıyoruz başında "@" işareti koymadan giriyoruz. Sonrasında mail adresimizi giriyoruz videodan takip edebilirsiniz. burda size verdiği bilgileri not almayı unutmayın formda kullanacağız ve saklayın.

## Kayıt formunu doldurmayı unutmayalım. [Buradan](https://mantanetwork.typeform.com/TrustedSetup) kayıt formuna ulaşabilirsiniz. ayrıca [Discord](https://discord.gg/mantanetwork) Sunucularından katılmayı unutmayın.

  ## Eğer polkadot cüzdanını kullanmayı bilmiyorsanız videodan takip edin formda sizden  KMA adresinizi vermenizi isteyecek, bunun için polkadotjs cüzdana sahip olmanız gerekiyor.
 

