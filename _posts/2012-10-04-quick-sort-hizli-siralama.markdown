---
layout: post
title:  "Quick Sort (Hızlı Sıralama)"
date:   2012-10-04 00:44:00
tags: Quicksort
categories: Sıralama Algoritmaları
---

<img class="alignright size-full wp-image-68" title="Sorting_quicksort_anim" alt="" src="{{site.baseurl}}/assets/images/2011/04/Sorting_quicksort_anim.gif" width="220" height="168" />
Quick sort (hızlı sıralama) sıralama algoritması, parçala ve çözümle (divide and conquer) mantığıyla çalışan, best-case **O(nlogn)**, worst-case **O(n^2)** zaman karmaşıklığı ile en çok kullanılan sıralama algoritmalarındandır.

**Algoritmayı şu üç adımla inceleyebiliriz.**

1. Liste içerisinden pivot olacak bir eleman seçilir.
2. Pivot değerden küçük olanlar pivottan önce, büyük olanlar pivottan sonra olacak şekilde elemanlar liste içerisinde yer değiştirilir.
3. Pivotun öncesindeki ve sonrasındaki değerler ayrı bir liste kabul edilip quick sort algoritması bu listeler için yeniden çalıştırılır.

**Pseudocode :**
<script src="https://gist.github.com/tolpp/676593ce32b36974fb27.js"></script>
**Java :**
<script src="https://gist.github.com/tolpp/bcf7908f41f09ea258b2.js"></script>