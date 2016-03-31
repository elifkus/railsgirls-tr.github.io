* * *

layout: default title: Uygulamanıza Gravatar Eklemek permalink: gravatar-eklemek

* * *

# Uygulamanıza Gravatar Eklemek

*Catherine Jones tarafından oluşturuldu*

Bu kılavuz [uygulama geliştirme kılavuzunu](http://guides.railsgirls.com/app/) takip ederek Rails Girls uygulamasını oluşturduğunuzu ve [Devise](http://guides.railsgirls.com/devise/) kullanarak kimlik doğrulamayı eklediğinizi varsayar.

### Önemli

Bunun çalışması için e-posta adresinize kayıtlı Gravatar'ın olması gerekmektedir. Eğer kayıtlı değilseniz [gravatar.com](http://en.gravatar.com/) dan hemen kaydolabilirsiniz.

## *1.* Gravtastic gemini Eklemek

Gemfile'ınızı açın ve `devise` geminizin aştına aşağıdakini ekleyin

{% highlight ruby %} gem 'gravtastic' {% endhighlight %}

Terminalde şunu çalıştırın

{% highlight sh %} bundle install {% endhighlight %}

Bu gravtastic gemini yükleyecek. Sonra rails sunucunuzu yeniden başlatmayı unutmayın.

## *2.* Uygulamanızda Gravatar kurmak

`app/models/user.rb` dosyasını açın ve

{% highlight ruby %} include Gravtastic gravtastic {% endhighlight %}

ilk satırdan hemen sonra şu satırları ekleyin.

## *3* Gravatar'ı Yapılandırmak

`app/views/layouts/application.html.erb` dosyasını açın ve

{% highlight erb %} <% if user_signed_in? %> {% endhighlight %}

bölümüne aşağıdaki parçadan önce

{% highlight erb %} <% else %> {% endhighlight %}

ekleyin

{% highlight erb %} <%= image_tag current_user.gravatar_url %> {% endhighlight %}

Şimdi uygulamanızı tarayıcınızda açın ve Gravatar ile ilişkilendirilmiş bir email adresi ile giriş yapın. Gravatar'ınızı görebiliyor olmalısınız.