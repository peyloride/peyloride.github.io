---
title: 'Github Pages üzerine Jekyll Kurulumu '
date: 2017-02-12 17:22:48 Z
layout: post
---

Okuduğunuz bu yazı Jekyll ve Github Pages tarafından size gösterilmekte. Olabildiğince kısa tutup, benzeri bir şeyi nasıl yapabileceğinizden bahsedeceğim.

Normalde bu konu ile ilgili yeterince kaynak bulunmakta. Ancak bunların hemen hepsi İngilizce. Yazımda Türkçe'ye olabildiğince dikkat ederek size bu işlemi anlatacağım.

Öncelikle bir **GitHub hesabı almanız gerekiyor.**

Ardından bu hesabı kullanarak **yeni bir Repository açmanız** ve adını **kullanıcı_adınız.github.io** şeklinde ayarlamalısınız.

<img src="/images/new-repo.png" class="center-image" width="500">

Ardından bu repoyu kendi bilgisayarınıza almanız gerekiyor. Bunun için aşağıdaki gibi repoyu klonlamanız gerekmekte.

{% highlight shell %}
~ $ git clone https://github.com/kullanıcı_adınız/kullanıcı_adınız.github.io
{% endhighlight %}

Bir sonraki aşama için öncelikle klonladığımız klasöre giriş yapmamız gerekiyor. Bunun için terminalden cd(change directory) komutunu kullanarak klasörün içine girelim.

{% highlight shell %}
~ $ cd kullanıcı_adınız.github.io
{% endhighlight %}

Bu aşamada ise size tavsiyem klasik Jekyll şablonu yerine, bir tema seçip onun dosyaları üzerinden ilerlemeniz. Şahsen bu site Webjeda.com'un yaptığı [bir temanın](https://blog.webjeda.com/jekyll-themes/yudish/) kendime göre düzenlenmiş ve ufak tefek bir kaç şey eklenmiş hali.

Başka temaları aramak için ise, [şu adresi](http://jekyllthemes.org/)  ziyaret edip gözünüze güzel geleni indirin.

Tabii hazır tema kullanmak yerine Jekyll sisteminin size sunduğu esneklik sayesinde kendiniz de güzel bir tema hazırlayabilirsiniz ama bu yazının hedef kitlesi bu işe yeni başlayanlar olduğu için şimdilik bunu tavsiye etmiyorum.

Temayı indirdikten sonra arşivi az önce oluşturduğumuz kullanıcı_adınız.github.io klasörüne açın. Bunu terminalden ya da gezgin üzerinden yapabilirsiniz.

Bu aşamadan sonra kısa bir test yayını amacı için terminal üzerinden aşağıdaki komutları uygulayarak sitenizi yayına alabilirsiniz.

{% highlight shell %}
~ $ git add --all
~ $ git commit -m "Initial commit"
~ $ git push -u origin master
{% endhighlight %}

Git kullanımı hakkında bilginiz yoksa [buradaki](https://rogerdudler.github.io/git-guide/index.tr.html) linke tıklayarak öğrenebilirsiniz.

Ve mutlu son. Eğer her şeyi doğru yaptıysanız, siteniz şu anda yayında olmalı. Tam adresi ise: [http://kullanıcı_adınız.github.io](http://kullanıcı_adınız.github.io)
