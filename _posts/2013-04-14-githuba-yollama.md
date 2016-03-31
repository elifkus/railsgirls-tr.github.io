* * *

layout: default

title: Uygulamanızı Github'a Yolllama

permalink: githuba-yollama

* * *

# Uygulamanızı GitHub'a yollama

*Alyson La, [@realalysonla](https://www.twitter.com/realalysonla) tarafından oluşturuldu*

## Başlamadan önce yapmanız gerekenler

### Git & GitHub

  * Git'in yüklü olup olmadığını kontrol edin
    
      * Terminalde `git --version`(tercihen 1.8 ya da üstü) yazın

  * Eğer değilse, Git'i indirin \[here\] (http://git-scm.com/downloads). Ardından lokal Git profilini kur - Terminalde:
    
      * `git config --global user.name "your-name"` yazın
      * `git config --global user.email "your-email"` yazın
    
      * *Git'in yapılandırılmış olup olmadığını kontrol etmek için şu kodu yazabilirsin* `git config --list`

  * Ücretsiz [GitHub](https://github.com) hesabı oluşturun ya da zaten hesabınız varsa giriş yapın

**EĞİTMEN:** Git, versiyon kontrol ve açık kaynak hakkında biraz konuşun

## Komut satırını kullanarak uygulamanı Github'a yollamak

GitHub profilinde "new repo"ya tıklayın ona bir isim (örnek: rails-girls verin, kısa bir açıklama ekleyin, "public" repo seçeneğini seçin ve "create repository"ye tıklayın.

Komut satırında--railsgirls dosyana `cd` ettiğinden emin ol--ve şunu yaz:

`git init`

Bu, projende bir git repository'si başlatır

*Not:* Eğer [Heroku rehberi](/heroku)'ni zaten bitirdiysen, zaten bir git repository'si başlattın & sonraki adımlara geçebilirsin.

Sonra railsgirls dizininde `README.rdoc` adlı bir dosya olup olmadığını kontrol edin:

<div class="os-specific">
  <div class="nix">
    <code>ls README.rdoc</code>
  </div>
  
  <div class="win">
    <code>dir README.rdoc</code>
  </div>
</div>

Eğer öyle bir dosya yoksa, şunu yazarak oluşturun:

`touch README.rdoc`

Ya da bir Windows ortamında kullanıyorsan, onun yerine şu komutu yaz:

`type nul > README.rdoc`

**EĞİTMEN:** Biraz README.rdoc hakkında konuşun

Sonra şunu yazın:

`git status`

Bu senin çalışma dizinindeki tüm dosyaları listeler.

**EĞİTMEN:** Bazı favori git komutların hakkında konuşun

Sonra şunu yazın:

`git add .`

Bu şimdiye kadarli tüm dosyaları & değişiklikleri staging areaya ekler.

Sonra şunu yazın:

`git commit -m "ilk commit"`

"ilk commit" mesajını ekleyerek tüm dosyalarını commit eder

Daha sonra şunu yazın:

`git remote add origin https://github.com/username/rails-girls.git`

*Github repo sayfanızda repo URL'sini bulabilirsiniz. Elle girmek yerine ordan kopyalayıp yapıştırabilirsiniz. Github repo sayfanızdan linki, yanındaki pano ikonunu tıklayarak kopyalabilirsiniz.*

Bu "origin" adı verilen Github'da oluşturduğunuz depoya işaret eden bir remote, ya da *bağlantı*, oluşturur.

Sonra şunu yazın:

`git push -u origin master`

Bu commitlerini GitHub'taki "master" branchine gönderir

Tebrikler uygulaman GitHub'ta! Yukarıda kullandığın url'ye giderek kontrol et: https://github.com/usrname/railsgirls (.git kısmı olmadan)

Değişiklik yapıp onları GitHub'a yollamaya devam etmek istiyorsan, sadece şu üç komuta ihtiyacın var:

`git add .`

`git commit -m "commit mesajınızı buraya yazın"`

`git push origin master`

## Sırada ne var?

### Açık kaynak topluluğunun bir parçası olma

  * Github'da Rails Girls'ü & eğitmenlerinizi takip edin
  * Onların projelerini yıldızla yıldızla ya da izle
  * Bir repoyu [fork](https://help.github.com/articles/fork-a-repo) et, sonra clone et ve forkuna değişiklikleri yolla. [Pull request](https://help.github.com/articles/using-pull-requests) göndererek değişiklikleri kaynağı ile paylaş!
  * Bir hata bulduğunda projede bir konu oluştur
  * Diğer açık kaynaklı projeleri keşfet - programlama dili ya da anahtar kelime ile arat

### Daha fazla Git öğrenme

  * [trygit.org](http://try.github.io/)'u kontrol et
  * [Git Cheatsheet](https://na1.salesforce.com/help/doc/en/salesforce_git_developer_cheatsheet.pdf)'i kullan
  * [git-scm.org](http://git-scm.com/)'daki git komutlarına bak