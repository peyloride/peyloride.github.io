---
layout: post
title: 'Github Pages üzerine Jekyll Kurulumu - Genel Düzenlemeler '
date: '2017-02-20 20:22:48 +0300'
published: true
---

İkinci aşama olarak ise kurduğumuz temayı kendimize göre ayarlayıp kişisel linklerin vs. ayarlanmasını yapalım. Bunun için örrnek olarak kendi kullandığım ve bir önceki yazımda belirttiğim tema üzerinden anlatacağım.

İlk iş olarak genel ayarların bulunduğu **_config.yml** dosyası içerisinde bazı satırları düzeltmemiz gerekiyor.

{% highlight YAML %}
# Site settings
title: Yudish Tira  # Blogun başlığı

tagline: "I'm the eldest.I don't lie, I never will!" # Başlığın altında yazmasını istediğiniz metin/slogan

picture: yudish.jpg #images klasörü altına koyacağınız 100x100'lük fotoğrafınız

email: hello@email.com #email adresiniz

description: > # Tarayıcıda blogun başlığının devamında yazacak olan metin
  Yudish is a minimal Jekyll theme for content oriented websites with less distractions.

baseurl: "/yudish" # Blog için alt bir yönlendirme için, kullanmayacaksanız boş bırakın

url: "http://webjeda.com" # Blog'un adresi

brand-color: '#e74c3c' # Temanın renklerinin bağlı olduğu ana değişken

permalink: ':title/'
{% endhighlight %}

Genel ayarları yaptıktan sonra, Disqus yorumlarını eklemek ve Google Web Analytics'i eklemek için şu satırları da düzenlememiz gerekiyor.

{% highlight YAML %}
disqus-shortname: webjeda-sample
analytics: UA-83979019-1
{% endhighlight%}

Bu ayarlar için Disqus'dan bir kısa-ad, Google Web Analytics'den de kendi sitenize özel oluşturulmuş ID'nizi almanız gerekiyor.

Kullandığım bu temanın orjinalinde olmasa da, fotoğrafın altındaki sosyal linkler çoğu temada halihazırda bulunuyor. Genellikle bu ikonların doğru linklere yönlendirilmesi için ise yine aynı dosyada aşağıdaki satırların düzenlenmesi gerekiyor.

{% highlight YAML %}
#Social Links
# Delete the lines you don't need
# about 5 elements are recomended
github_username:  peyloride
facebook_username: okanb3
twitter_username: okanbinli
linkedin_username: okanbinli
instagram_username:  okanbinli
{% endhighlight %}

Bunların haricinde ise daha teknik konularda ayarlar bulunmakta. Bunlardan bazılarını aşağıda açıklamaya çalıştım.

{% highlight YAML %}
# Footer'da görünecek sitenin sahibine dair logo/yazı
credits: webjeda #credits on the footer
version: 1.0

# Derleme seçenekleri
markdown: kramdown
kramdown:
  input: GFM
highlighter: rouge

sass:
  style: compressed
  
# Html için sıkıştırma seçenekleri
compress_html:
  clippings: [html,div, p, ul, td, h1, h2, h3, h4,link, meta, footer, nav, img, header, hr, br, head, style, li, ul, ol, time, main, script, title]
  comments: ["<!-- ", " -->"]
  endings: [all]
  ignore:
    envs: [local]
  blanklines: false
  profile: false
  startings: []
  
 
# Prose.io adresinden komut satırı kullanmadan sitenize yeni yazı eklemek veya düzenlemek için
prose:
  rooturl: ''
  siteurl: 'http://prose.github.io/starter/'
  relativeLinks: 'http://prose.github.io/starter/links.jsonp'
  media: 'images'
  ignore:
    - index.md
    - _config.yml
    - /_layouts
    - /_includes

# Jekyll ile beraber kullanablieceğiniz bazı eklentiler(gemler)
gems: [jekyll-paginate, jekyll-seo-tag]
{% endhighlight %}

Bu ayarları yaptıktan sonra değişikliklerin geçerli olması için bir önceki yazımın sonunda yaptığımız gibi git kullanarak bu değişiklikleri commit haline getirip, push komutu ile yollamamız gerekmekte.