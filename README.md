# Adamnite-Testnet-Beta
<h1 align="center"> <img src="https://pbs.twimg.com/media/FgbLe38XoAE7ImO?format=png&name=large" width="650"></h1>

### Güncelleme yapıyoruz: 
```
sudo apt update && sudo apt upgrade -y
```
* Aşağıdaki işlemde "access-token" yerine yazılacak kod için hemen aşağıdaki adımları izleyin.
```
git clone https://"access-token"@github.com/Adamnite/goAdamnite.git
```
### Aşağıdaki adımları yapın:

Kendi github profilinizden aşağıdaki adımları izleyin.
settings -> developer settings -> personal access tokens -> tokens classic -> generate new token
Bu adımlardan sonra açılan pencerede 
 * repo
 * write:packages
 * gist
 * notifications
 * write:discussion
kutucuklarını işaretleyin ve en altta ``Generate Token`` tuşuna basın.
#### Yukarıdaki adımlardan sonra
 * ``"access-token"`` yerine --> ``ghp_tkUD99pU.......................`` şeklinde yukarıda ``Generate Token`` yaptığınızda oluşan kodu yazın.
 
</br>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/560QzDh/a1.png" alt="a1" border="0"></a>
<a href="https://ibb.co/bRtPffZ"><img src="https://i.ibb.co/prqxmm8/a2.png" alt="a2" border="0"></a>
<a href="https://ibb.co/BzpGZ8Z"><img src="https://i.ibb.co/znMFRKR/a3.png" alt="a3" border="0"></a>
</br>

```
cd goAdamnite/Ubuntu
```

```
chmod +x goAdamnite/Ubuntu/gnite
```
* Aşağıdaki komutu girdikten sonra şifre oluşturmanızı isteyecek. Şifre girdikten sonra bir süre bekletecek. sonra size public key ve secret key verecek. Not edin kaybetmeyin!!!
```
./gnite account new
```

```
screen -S adamnite
```
```
./gnite
```


### Token Gönderme (token gelince yapacağız): 
* [Discord](https://discord.gg/adamnite-921093307533230111) kanalından test token isteyin. Şimdilik DM'den ``Tsimafei#6578`` veya ``Toucan#5099``. 8 saat içinde yanıt almazsanız, DM ``Arch2230``.
* goAdamnite/Ubuntu klasörünün içinde olduğunuzdan emin olun.
* Yukarıda almış olduğunuz public key aşağıdaki --> "your public address" ile değiştirin 

Bakiyenizi kontrol edin:  ``./gnite-test --balance "your public address"``
* ``"alıcıadres"`` --> göndermek istediğiniz kişinin adresi
* ``"gönderenadress"`` --> sizin adresiniz
* ``"miktar"`` --> miktar girin. 0.01 şeklinde miktar girmeyin sadece 1, 2, 3 şeklinde sayı girebilirsiniz
* Bana göndermek isterseniz ``48kZMAfGrBA4VfjMC6xAM4nE6VRj``

```
./gnite-test --sendaddr gönderenadres --recaddr alıcıadres --amount miktar  --password şifreniz
```

### Stake
* ``"alıcıadres"`` --> stake edeceğiniz kişinin adresi
* ``"gönderenadress"`` --> sizin adresiniz
* ``"miktar"`` --> miktar girin. 0.01 şeklinde miktar girmeyin sadece 1, 2, 3 şeklinde sayı girebilirsiniz
* Bana göndermek isterseniz ``48kZMAfGrBA4VfjMC6xAM4nE6VRj``
* Dikkat!!! kodlarda Token Gönderme ve stake arasındaki tek fark ``--txtype true``
```
./gnite-test --sendaddr gönderenadres --recaddr alıcıadres --amount miktar  --password şifreniz --txtype true
```
### Hatalar ve Düzeltme işlemleri:

*  ``./gnite-test -h`` kullanılabilecek komutları görebilmek için.
* ``./gnite-test --balance "your public address"`` bakiye kontrolü yaparken ``-bash: ./gnite-test: Permission denied`` hatası alırsanız. aşağıdaki komutları girin.
```
cd goAdamnite/Ubuntu
chmod +x gnite-test
```
* ``EROR[11-28|15:26:58] could not decrypt key with given password`` --> hatası aldığınızda --password flagı en sonda olmamalı
* ``flag provided but not defined: -tx0.0type`` --> hatası alırsanız göndereceğiniz tutar kesirli demektir. Tam sayı yapınız.
* ``./gnite-test: Permission denied`` --> hatası için ``chmod +x gnite-test`` komutunu deneyin. goAdamnite/Ubuntu klasörünün içinde oldunuzdan emin olun.
* ``EROR[11-30|07:17:27] open /root/.adamnite/keys/ADAMNITE-54317a786d6467647345385657467269447867555666465346777a: no such file or directory`` --> hatası alırsanız. Winscp ile sunucunuza bağlanın ``/root/.adamnite/keys/`` klasörüne gidin. ``ADAMNITE-00`` ile başlayan dosyanın başındaki iki tane sıfırı silin.
