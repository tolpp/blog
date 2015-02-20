---
layout: post
title:  "Consecutive Integer Checking Algorithm ile GCD hesabı"
date:   2012-09-26 01:55:00
tags: Science
categories: Science
mathjax: false
---

Consecutive Integer Checking Algorithm (Ardışık Tamsayı Kontrol Algoritması) EBOB hesabı için kullanılabilecek diğer algoritmalardan.

<!--<a href="http://tolpp.com/category/ders/algorithm-analysis/">Algorithm Analysis</a> dersinde işlenenleri <a href="http://tolpp.com/ogrenme-notlari/">notlar şeklinde alacağım</a> demiştim. Ancak bildiğim ve sıkıcı algoritmalar üzerinde bu kadar durmayı düşünmüyordum. Ama yine de,-->

Algoritmanın çalışma mantığı şu :

**m** ve **n** şeklinde EBOB değeri bulunacak iki tamsayımız olsun. Bunlardan küçük olan değer **t** olarak seçilir. Her iki sayı da **t**'ye bölünür. Eğer kalan 0 ise EBOB değeri **t**'dir. Değilse **t** değeri sürekli bir azaltılarak bölme işlemi yinelenir. Yani ;

1. **t** 'ye *min*{**m**, **n**} değerini ata.
2. **m**'yi **t**'ye böl. Kalan 0 ise 3. adıma değilse 4.adıma geç.
3. **n**'yi **t**'ye böl. Kalan 0 ise EBOB değeri olarak **t**'yi döndür.
4. **t'**yi bir azalt ve 2.adıma dön.

Pseudocode:
<script src="https://gist.github.com/tolpp/e897f60cf28734f51231.js"></script>

Java :
<script src="https://gist.github.com/tolpp/a55487fcc7aaa3ae44b6.js"></script>
<!--Bu yazı [öğrenme notları]({{site.baseurl}}/ogrenme-notlari/)'nın bir parçasıdır.-->