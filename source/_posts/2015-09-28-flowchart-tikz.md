---
layout: post
title: "Diagram Alir dengan PGF/TikZ dan LaTeX/LyX"
date: 2015-09-28 5:12 PM
comments: true
external-url:
categories:
author: Gema Buj
published: true
categories: [latex, lyx, bagan alir, tikz]
code_dir: source/downloads/code
---

Barangkali timbul suatu pertanyaan, **mengapa memilih program gnuplot?** Banyak alasan mengapa memilih program berbasis CLI lebih mudah dibandingkan program berbasis GUI. Alasan yang paling masuk akal adalah bahwa program yang berbasis CLI tidak membutuhkan terminal grafik yang bagus. Anda memakai komputer ``butut'' pun masih bisa membuat grafik dengan kualitas cetak yang sangat baik. Kadangkala data mentah yang diperoleh dari suatu pengukuran perlu melalui proses awal sebelum diplot ke dalam grafik, misalnya koreksi tertentu. Minimal kita akan bekerja beberapa kali untuk menghasilkan grafik dari data mentah ini. Pertama melakukan perhitungan koreksi dan kedua melakukan pengeplotan. Memang tidak terlalu sulit melakukan hal seperti ini pada program berbasis GUI karena sudah disediakan spreadsheet untuk melakukan perhitungannya.

Dalam program gnuplot yang berbasis CLI kita tidak perlu melakukan perhitungan seperti itu, karena program ini dapat melakukan perhitungan bersama-sama dengan pengeplotan. Hal ini yang membuat program ini jauh lebih cepat dalam membuat grafik dibandingkan dengan program berbasis GUI.

<!--more-->

``` tex
%-------------------------%
% tikz elemen parameters
%-------------------------%
\tikzstyle{decision}=[diamond, draw, fill=magenta!10, node distance=0em, text width=2cm, text centered]
\tikzstyle{line}=[draw, -latex']
\tikzstyle{line2}=[draw]
\tikzstyle{elli}=[ellipse, draw, fill=orange!30, node distance=5em, text width=2.3cm, text centered]
\tikzstyle{block}=[rectangle, draw, fill=cyan!20, node distance=5em, text width=3.5cm, text centered]
\tikzstyle{block0}=[rectangle, draw, fill=orange!15, node distance=3em, text width=3cm, text centered]
\tikzstyle{block1}=[rectangle, draw, fill=yellow!15, node distance=3em, text width=3cm, text centered]
\tikzstyle{block2}=[rectangle, draw, fill=cyan!15, node distance=3em, text width=3cm, text centered]
\tikzstyle{block3}=[rectangle, draw, fill=yellow!15, node distance=3em, text width=1.2cm, text centered]
\tikzstyle{startstop}=[rectangle, rounded corners, draw, fill=green!20, node distance=1em, text width=2cm, text centered]
\begin{center}
\begin{tikzpicture}

%-------------------------%
% entitas
%-------------------------%
\node[startstop](start){MULAI};
\node[block1, below of=start, yshift=-2em, xshift=0em](data){Data seismik, stratigrafi atau geologi};
\node[block0, below of=data, yshift=-2em, xshift=0em](interpret){Interpretasi};
\node[block2, below of=interpret, yshift=-2em, xshift=0em](konsep){Model konseptual};
\node[block0, left of=konsep, yshift=0em, xshift=-8em](alternatif){Model alternatif atau analisis sensitivitas};
\node[block0, below of=konsep, yshift=-2em, xshift=0em](diskrit){Diskritisasi};
\node[block2, below of=diskrit, yshift=-2em, xshift=0em](finite){\textit{Finite-element model}};
\node[decision, below of=finite, yshift=-8em, xshift=0em](kalibrasi){Kalibrasi data};
\node[block2, left of=kalibrasi, yshift=0em, xshift=-8em](bad){Hasil tidak sesuai \textit{(bad match)}};
\node[block2, right of=kalibrasi, yshift=0em, xshift=8em](good){Hasil sesuai \textit{(good match)}};
\node[block0, below of=good, yshift=-5em](aplikasi){Pemakaian atau aplikasi model};
\node[startstop, left of=aplikasi, xshift=-10em](stop){SELESAI};

%-------------------------%
% legenda
%-------------------------%
\node[startstop, above of=start, yshift=4em, xshift=-15em](legstartstop){Mulai / Selesai};
\node[block1, right of=legstartstop, xshift=6em](leginput){Masukan / Input};
\node[block0, right of=leginput, xshift=7em](legproses){Proses / Tindakan};
\node[block2, right of=leginput, xshift=17em](legoutput){Keluaran / Output};

%-------------------------%
% panah
%-------------------------%
\path[line](start)--(data);
\path[line](data)--(interpret);
\path[line](interpret)--(konsep);
\path[line](konsep)--(diskrit);
\path[line](diskrit)--(finite);
\path[line](finite)--(kalibrasi);
\path[line](kalibrasi)--(bad);
\path[line](bad)--(alternatif);
\path[line](alternatif)--(konsep);
\path[line](kalibrasi)--(good);
\path[line](good)--(aplikasi);
\path[line](aplikasi)--(stop);
\end{tikzpicture} % akhir flowchart
\end{center}
```
