<h1 align="center"> Titan Network Ubuntu Kurulum </h1>

Gereklilikleri yükleyelim
sudo apt update
sudo apt install screen

İşlemleri screen içinde yapıyoruz
screen -S titan

Titan Network dosyasını çekelim ve kuralım
wget -c https://github.com/Titannet-dao/titan-node/releases/download/v0.1.18/titan_v0.1.18_linux_amd64.tar.gz -O - | sudo tar -xz -C /usr/local/bin --strip-components=1

Nodu çalıştıralım
İlk kurulumdan sonraki ilk çalıştırma 
/usr/local/bin/titan-edge daemon start --init --url https://test-locator.titannet.io:5000/rpc/v0

Nodu titan hesabımıza bağlayalım
titan-edge bind --hash=identitycodeyazalım https://api-test1.container1.titannet.io/api/v2/device/binding

Nod durursa veya sorun olursa yeniden çalıştırmak için
titan-edge daemon start
Nodu durdurmak için
titan-edge daemon stop

Kurulumdan sonra ana ekrana dönmek için
ctrl+a aynı anda bastıktan sonra screen ekranı komut modu açılır sonrasında +d ye basarak ana ekrana dönebilirsin

çıktın kapattın sonnrasında yeniden açtın ve kontrol etmek istedin
screen -r -d titan

birden fazla screen komutun var adını hatırlayamadın
screen -ls (hepsini görüntüler id ile birlikte) 
