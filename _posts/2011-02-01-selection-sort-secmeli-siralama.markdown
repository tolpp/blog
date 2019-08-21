---
layout: post
title:  "Selection Sort (Seçmeli Sıralama)"
date:   2011-02-01 17:58:00
tags: [sıralama algoritmaları, seçmeli sıralama, selection sort]
categories: [Sıralama Algoritmaları]
---
<img class=" " title="Selection Sort Animate" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/Selection_sort_animation.gif" alt="Seçmeli arama animasyonu" width="202" height="202" align="right" border="1"/>

Seçmeli arama (selection sort) her bir adım sonunda en küçük değerin en başa getirildiği sıralama algoritmasıdır. Dizi içinde dolaşılarak en küçük değer en başa getirilir. Dizideki eleman sayısı N kadar dolaşma işlemi tekrarlandığında dizi üzerinde sırama ede edilmiş olur.
<h4>Performans</h4>
Dizimiz üzerinde N tane eleman olsun. Bu durumda N kadar kontrol döngüsü çalıştırılır. Bu döngülerden 1. için N, 2.iin N-1 ... N-1. için 2, N.için 1 adet kontrol yapılır. Yani bu sayıları dizi toplamı alırsak N x(N+1)/2 = (N<strong><sup>2</sup></strong>+N)/2 kontrol yapılmış olur. Bu da worst-case <strong>O (n<sup>2</sup>)</strong> karmaşıklık anlamına gelir.

Buradan seçmeli sıralamanın çok performanslı bir sıralama olmadığını görebiliriz. Bu yüzden büyük diziler yerine, minik dizilerde kulanılması daha mantıklı olacaktır. Tercih sebebi ise yazımı çok kolay bil algoritmaya sahip olmasıdır.
<h4>Adım-Adım Uygulama</h4>
Elimizde 5 1 4 2 8 değerlerine sahip 5 elemanlı bir dizi olsun. Bunu selection sort kullanarak adım adım sıralayalım:<br/>

<strong>İlk döngü:</strong><br/>
( <span style="text-decoration: underline;"><span style="color: #ff0000;">5</span></span> 1 4 2 8 )<br/>
( 5 <span style="text-decoration: underline;"><span style="color: #ff0000;">1</span></span> 4 2 8 )<br/>
( 5 <span style="color: #ff0000;">1</span> <span style="text-decoration: underline;">4</span> 2 8 )<br/>
( 5 <span style="color: #ff0000;">1</span> 4 <span style="text-decoration: underline;">2</span> 8 )<br/>
( 5 <span style="color: #ff0000;">1</span> 4 2 <span style="text-decoration: underline;">8</span> ) --&gt;( <strong>1</strong> 5 4 2 8 )<br/>

<strong>İkinci döngü:</strong><br/>
(<strong> 1</strong> <span style="color: #ff0000;"><span style="text-decoration: underline;">5</span></span> 4 2 8 )<br/>
(<strong> 1</strong> 5 <span style="color: #ff0000;"><span style="text-decoration: underline;">4</span></span> 2 8 )<br/>
(<strong> 1</strong> 5 4 <span style="color: #ff0000;"><span style="text-decoration: underline;">2</span></span> 8 )<br/>
(<strong> 1</strong> 5 4 <span style="color: #ff0000;">2</span> <span style="text-decoration: underline;">8</span> ) --&gt; ( <strong>1 2 </strong>4 5 8 )<br/>

<strong>Üçüncü Döngü:</strong><br/>
(<strong> 1 2 </strong><span style="text-decoration: underline;"><span style="color: #ff0000;">4</span></span> 5 8 )<br/>
(<strong> 1 2 </strong><span style="color: #ff0000;">4</span> <span style="text-decoration: underline;">5</span> 8 )<br/>
(<strong> 1 2 </strong><span style="color: #ff0000;">4</span> 5 <span style="text-decoration: underline;">8</span> ) --&gt; (<strong> 1 2 4</strong> 5 8 )<br/>

<strong>Dördüncü Döngü:</strong><br/>
( <strong>1 2 4</strong> <span style="text-decoration: underline;"><span style="color: #ff0000;">5</span></span> 8 )<br/>
(<strong> 1 2 4</strong> <span style="color: #ff0000;">5</span> <span style="text-decoration: underline;">8</span> ) --&gt; (<strong> 1 2 4 5</strong> 8 )<br/>

Sıralı dizim : ( 1 2 4 5 8 )

Algoritma gösterilirken, altı çizili değerler o an en küçük kontrolünün yapıldığı değerlerdir. kırmızılarsa o ana kadar karşılaşılan en küçük değer indexini tutar.

Ayrıca dikat edilirse, 2.döngüde sıralı dizi elde edilmesine rağmen iki döngü daha yapılmıştır.Bu yüzden en iyi durumda bile (best-case) algoritma <strong>O (n<strong><sup>2</sup></strong>)</strong> zaman karmaşıklığında çalışmaktadır
<h4>Pseudocode</h4>
<script src="https://gist.github.com/tolpp/20c1c3ad091b11260bb4.js"></script>
<h4>Kaynaklar</h4>
<a href="https://en.wikipedia.org/wiki/Selection_sort">https://en.wikipedia.org/wiki/Selection_sort</a>