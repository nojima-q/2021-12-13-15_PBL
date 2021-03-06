# がん研究会PBL　シラバス　〜Transcriptome解析〜

## 日時

2021年12月13日(月) 13時−17時\
2021年12月15日(水) 13時−17時


## 場所
研究所4階　435セミナー室 (基本的にzoom開催ですが、期間中、講師の先生がおられる435セミナー室でも（密にならない範囲で）受講可能です。また、エラー等が遠隔で解消できない時には、直接指導を受けることができます)。

## 講義の概要と学習目標
公共データベースに格納されているRNA-Seqデータを取得し、発現変動遺伝子（Differentially expressed genes; DEGs）の検出、DEGsを用いた各種エンリッチメント解析を行う。


## 用意するもの
コンピュータ１台


## 環境
OS：Windows、Mac、Linux（Windowsの場合は仮想でUNIX OSを入れるか、[Cygwin](https://www.cygwin.com/)等を利用して下さい。）\
Cygwinのインストール方法は、下記を参照して下さい。\
[![http://img.youtube.com/vi/kMjD6KWdqxM/sddefault.jpg](https://img.youtube.com/vi/kMjD6KWdqxM/0.jpg)](https://www.youtube.com/watch?v=kMjD6KWdqxM)\
Cygwinを利用する場合は、下記の一部のツールの実行にJavaとPerlが必要です。それぞれインストールして下さい。\
解析後半では、RStudioを使用します。


## 使用するツール
### 端末上で操作
SRA Toolkit (https://github.com/ncbi/sra-tools/wiki/01.-Downloading-SRA-Toolkit) \
FastQC (https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) \
Trimmomatic (http://www.usadellab.org/cms/?page=trimmomatic) \
HISAT2 (http://daehwankimlab.github.io/hisat2/) \
featureCounts (http://subread.sourceforge.net/)
### RStudio上で操作
```
install.packages("BiocManager")
install.packages("ggplot2")
install.packages("reshape2")
BiocManager::install("GenomicFeatures")
BiocManager::install("clusterProfiler")
BiocManager::install("biomaRt")
BiocManager::install("org.Hs.eg.db")
BiocManager::install("DOSE")
```

## スケジュール
１日目：各種ツールのインストール、下記解析計画のチュートリアル\
２日目：自主学習 \
３日目：チュートリアルに従って、各自取得データを解析

## 解析計画
#### 端末上で操作
1	公共データベースの紹介、データの取得方法\
2	FASTQファイルの形式、クオリティーコントロールについて\
3	アダプターの除去およびリードのトリミング\
4	リファレンスゲノムファイル、アノテーションファイルの取得\
5	リファレンスゲノムへのマッピング\
6	マッピングデータから遺伝子ごとにリードのカウントデータを取得する
#### RStudio上で操作
7	カウントデータをTPM値に変換する\
8	DEGsの検出\
9	エンリッチメント解析

## 講義資料・チュートリアル
https://github.com/nojima-q/2021-12-13-15_PBL_analysis.git
