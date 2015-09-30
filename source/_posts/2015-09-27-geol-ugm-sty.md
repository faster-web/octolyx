---
layout: post
title: "Paket Penulisan Skripsi atau Tesis geol-ugm.sty LaTeX / LyX "
date: 2015-09-27 5:12 PM
comments: true
external-url:
categories:
author: Gema Buj
published: true
categories: [latex, lyx, writing, publishing]
code_dir: source/downloads/code
---

[LyX](http://www.lyx.org) dan merupakan salah satu dari document processor yang sangat handal dalam mendesain layout naskah yang konsisten. LyX merupakan perangkat lunak front-end dari [LaTeX](https://www.latex-project.org), sehingga tanpa LaTeX perangkat lunak ini tidak dapat dijalankan. Sebagian besar desain layout yang disediakan oleh LaTeX dan LyX merupakan standard internasional yang mana biasanya universitas di Indonesia akan merasa 'gengsi' untuk memakainya. 

Pada kesempatan ini penulis mencoba memberikan salah satu solusi untuk menjembatani antara paket LaTeX yang sudah tersedia dan kebutuhan layout Skripsi atau Referat/Karya Tulis Ilmiah di Indonesia. Paket ini penulis beri nama [geol-ugm.sty](http://warmada.staff.ugm.ac.id/TextProc/skripsi/geol-ugm.zip). 

<!--more-->

Bagi pengguna di luar UGM silakan memberi nama yang lain. Apa manfaat penggunaan paket ini? Seperti halnya paket-paket lain di LaTeX yang selalu memanjakan penggunanya, paket ini pun demikian. Pengguna tidak perlu memikirkan bagaimana harus melayout tulisan yang dibuat, karena LaTeX dapat melakukannya. Pengguna tidak perlu memikirkan bagaimana harus membuat sampul, lember pengesahan, mengatur gambar. Semua ini dikerjakan oleh LaTeX melalui paket ini. Jadi, pengguna cukup memikirkan isinya.

## Pra-desain paket
Untuk mempercepat penyelesaian perancangannya, pra-desain paket geol-ugm.sty ini menggunakan kelebihan-kelebihan paket LaTeX yang sudah tersedia, seperti `titlesec.sty`, `helvet.sty`, `caption2.sty`, `setspace.sty`, `textcase.sty`, `hyperref.sty`, `mathptmx.sty`, `courier.sty`, `eso-pic.sty`, `graphicx.sty`, `hyphenat.sty`, `dcolumn.sty`, dan `ifthen.sty`. Semua paket ini sebagian besar telah disediakan oleh CTAN. Namun, pada perkembangan selanjutnya diharapkan pemakaian ekstra paket ini sebisa mungkin diminimalkan. Hal ini bertujuan untuk mempermudah instalasi dan mengurangi dependensi paket.

``` tex
\usepackage[twosup]{geol-ugm} 
\pubtype{Skripsi} 
\degree{Sarjana (Strata-1)} 
\department{Jurusan Teknik Geologi} 
\faculty{Fakultas Teknik} 
\university{Universitas Medang Kemulan} 
\authortext{Penyusun} 
\idnum{87/13678/TK/15057} 
\city{Yogyakarta} 
\date {2006} 
\supervisor{Shakuntala} 
\idsup{134 222 256} 
\cosupervisor{Rani Mukherjee} 
\idcos{132 333 345}
```
