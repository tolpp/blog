---
layout: post
title:  "Bubble Sort (Kabarcık Sıralama)"
date:   2011-01-27 06:41:00
tags: Algoritmalar
categories: "Siralama Algoritmalari"
---

<img title="bubblesort_animate" src="http://upload.wikimedia.org/wikipedia/commons/3/37/Bubble_sort_animation.gif" alt="" width="224" height="190" align="right" border="1"/> Kabarcık sıralamanın gerçekleşimini gösteren animasyon

Sinking sort olarak da geçen bu sıralama algoritması, komşu olan her iki eleman arasında bir karşılaştırma yapar ve eğer istenenin tersi bir sıralama varsa swapping (yer değiştirme) işlemi uygular. Bu işlem ilk ugulandığında en büyük sayımız en sona yerleşir. Elimizde N elemanlı bir dizi olduğunu kabul edersek, tam bir sıralama elde edebilmemiz için N-1 kere diziyi baştan sona dolaşmamız gerekir.
<h4>Performans</h4>
Bubble sort, ortalama (avarage) ve en kötü durumda(worst-case) <strong>O(<em>n</em><sup>2</sup>)</strong> zaman karmaşıklığına sahiptir. Best-case durumunda O(n) karmaşıklığı olabilir. Bunun için her bir ikili kontrol döngüsü sonunda bir yer değiştirme (swapping) işlemi yapılmış mı diye kontrol edilir.
<h4>Adım-Adım Uygulama</h4>
Elimizde  5 1 4 2 8 değerlerine sahip 5 elemanlı bir dizi olsun. Bunu bubble sort kullanarak adım adım sıralayalım:<br/>
<!--more-->
<strong>İlk Döngü:</strong><br/>
( <strong>5</strong> <strong>1</strong> 4 2 8 ) --&gt; ( <strong>1</strong> <strong>5</strong> 4 2 8 ), İlk iki elemanı karşılaştırıyorum ve swapping yapıyorum. <br/>
( 1 <strong>5</strong> <strong>4</strong> 2 8 ) --&gt; ( 1 <strong>4</strong> <strong>5</strong> 2 8 ),  5 &gt; 4 swap yapıyorum<br/>
( 1 4 <strong>5</strong> <strong>2</strong> 8 ) --&gt; ( 1 4 <strong>2</strong> <strong>5</strong> 8 ), 5 &gt; 2 swap yapıyorum<br/>
( 1 4 2 <strong>5</strong> <strong>8</strong> ) --&gt; ( 1 4 2 <strong>5</strong> <strong>8</strong> ), 8&gt;5 olduğundan bu adımda swap yapmıyorum<br/>
<strong>İkinci Döngü:</strong><br/>
( <strong>1</strong> <strong>4</strong> 2 5 8 ) --&gt; ( <strong>1</strong> <strong>4</strong> 2 5 8 )<br/>
( 1 <strong>4</strong> <strong>2</strong> 5 8 ) --&gt; ( 1 <strong>2</strong> <strong>4</strong> 5 8 ),  4 &gt; 2 swap yapıyorum<br/>
( 1 2 <strong>4</strong> <strong>5</strong> 8 ) --&gt; ( 1 2 <strong>4</strong> <strong>5</strong> 8 )<br/>
<span style="text-decoration: line-through;">( 1 2 4 <strong>5</strong> <strong>8</strong> ) </span>--&gt;<span style="text-decoration: line-through;"> ( 1 2 4 <strong>5</strong> <strong>8</strong> )</span>, İlk döngüm bittiğine göre sondaki elemanımın en büyük olduğunu biliyorum. gereksiz bir adımdır.<br/>
Sıralama işlemi tamamlandı, fakat bunu algoritma bilmiyor bunun için bir adım daha dolaşır.<br/>
<strong>Üçüncü Döngü:</strong><br/>
( <strong>1</strong> <strong>2</strong> 4 5 8 ) --&gt; ( <strong>1</strong> <strong>2</strong> 4 5 8 )<br/>
( 1 <strong>2</strong> <strong>4</strong> 5 8 ) --&gt; ( 1 <strong>2</strong> <strong>4</strong> 5 8 ) --&gt; İki karşılaştırmada swap işlemi yapmadığımdan sıralama gerçekleşmiştir.<br/>
<span style="text-decoration: line-through;">( 1 2 <strong>4</strong> <strong>5</strong> 8 ) </span>--&gt;<span style="text-decoration: line-through;"> ( 1 2 <strong>4</strong> <strong>5</strong> 8 ), </span>sondan bir önceki adıma da ikinci döngü sayesinde bakmama gerek yoktur.<br/>
<span style="text-decoration: line-through;">( 1 2 4 <strong>5</strong> <strong>8</strong> ) </span>--&gt;<span style="text-decoration: line-through;"> ( 1 2 4 <strong>5</strong> <strong>8</strong> )</span>, gereksiz adım<br/>
<h4>Pseudocode</h4>
<script src="https://gist.github.com/tolpp/404288218998a512b1be.js"></script>
Bu pseudocode, bubble sort algoritması için uygulanan iyileştirmeleri de beraberinde içerir. Buna göre, zaten olması gereken yerde olan son elemanları kontrol etmez (n değerinin sürekli değişmesi sayesinde) ve bir swap işlemi gerçekleştirilmemişse zaten dizi sıralı diyerek algoritmayı bitirir.
<h4>Kaynaklar</h4>
<a href="http://en.wikipedia.org/wiki/Bubble_sort">http://en.wikipedia.org/wiki/Bubble_sort</a>