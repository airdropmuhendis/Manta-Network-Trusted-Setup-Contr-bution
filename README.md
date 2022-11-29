<h1 align="center">Manta Network Trusted Setup Contrıbution

## Manta Network, kısaca zkSNARKs üzerine inşa edilmiş blockchain projeleri için gizliliği sağlayan bir gizlilik protokolüdür. Trusted Setup Kurulumu için [buraya](https://docs.manta.network/docs/concepts/TrustedSetup) da bakabilirsiniz.

## Bir önceki kayıt adımını yapmadıysanız önce ordaki işlemleri yapın hala yapabilirsiniz daha sonra burdan devam edin. Video [Linki](https://youtu.be/jf5dvWblYek) 

## Manta Network için Sunucuyu nerden nasıl alacağınızı bilmiyorsanız node eğitim serimizi izleyebilirsiniz. [Node Eğitim Serisi](https://www.youtube.com/playlist?list=PLKxGUfdcj7MVXls2OvTpwx6CnpVJN685w)

![image](https://docs.manta.network/img/guides/trusted-setup-stages.svg)
## Manta Network için daha önceden kayıt kısmını yapmıştık burda ise katkı bölümünü tamamlayacağız.

### Sistem Gereksinimleri
 - kurulum için sistemin özellikleri çok önemli değil. tweet işleminden sonra sunucuyu silebilirsiniz veya sıfırlayıp farklı bir kurulum yapabilirsiniz.
 - Ubuntu 20.04
 - 2 CPU
 - 4GB RAM
 - disk boyutu önemsiz

<h1 align="center">Otomatik Kurulum

  ## Root yetkisi almak için aşağğıdaki kodu giriyoruz bazı sunucularda bunu sürekli girmemiz gerekiyor. eğer bunu girmezseniz yazdığınız kodun başına sudo komutunu yazarkata devam edebilirsiniz ancak karışıklık olmaması için aşğıdaki komutu yazmanızı tavsiye ederim. ( root: Windows cihazlarda olduğu gibi yönetici olarak çalıştırmamıza, yani bize yetki veren bir komuttur.)
  ```
  sudo su
  cd
  ```

 ## Aşşağıdaki komutlarla sunucumuzdaki güncellemeleri, yükseltmeleri kontrol ediyoruz, ve gerekli olan bağımlılıkları kütüphaneleri indiriyoruz. sondaki -y işareti gelen onay işlemlerini otamatik olarak onaylanmasını sağlayacaktır.

  ```
 sudo apt update && sudo apt upgrade -y

  ```
  
```
sudo apt install pkg-config build-essential git libssl-dev curl jq
```

Rust yüklüyoruz
```
curl https://sh.rustup.rs/ -sSf | sh -s -- -y
```
```
source $HOME/.cargo/env
```
manta rs githuptan veri çekelim.
```
git clone https://github.com/Manta-Network/manta-rs.git
```
screen yükleyip screen açalım
```
sudo apt install screen
```
```
screen -S mantacontrıbution
```
manta dizinine gelelim
```
cd manta-rs
```
```
cargo run --release --all-features --bin groth16_phase2_client contribute
```
 # Burda bir önceki adımda yaptığımız işlemler sonucunda bize verilen screet keyi kullanıyoruz. bize ne kadar süre bekliyeceğimizi ve önümüzde kaç kişi olduğunu söyliyecek, sıra bize geldiğinde işlemler tamamlanacak ve bize verdiği tweet linkinide paylaşmayı unutmayalım zorunlu değil ama yapılabilir.
 
 screenden çıkmak için ctrl +A+D kullanıyoruz.
 
 tekrar screene girmek için
 ```
 screen -r
 ```



  
 

