---
layout: post
title:  "Euclid Algoritması (Euclid's algorithm)"
date:   2012-09-26 01:28:00
tags: [gcd, euclid]
categories: [Algoritmalar]
mathjax: true
---
Euclid Algoritması en büyük ortak böleni (EBOB)[GCD (Greatest Common Divisor )] bulmak için kullanılabilecek en etkin algoritmalardan biridir. $$O((logn)^2)$$ zaman karmaşıklığına sahiptir.

**ebob(m, n) = ebob(n, m mod n)** 'i doğrulayacak şekilde çalışır.

Pseudocode ile :
<script src="https://gist.github.com/tolpp/994ed969e13695675cde.js"></script>

Java kodu :
<script src="https://gist.github.com/tolpp/90c3aa4649705ac43475.js"></script>

<!--Bu yazı [öğrenme notları]({{site.baseurl/ogrenme-notlari/}})-->