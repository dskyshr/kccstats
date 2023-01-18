# kccstats
 
慶應通信の成績まとめ用Rmdです。

# DEMO

https://dskyshr.github.io/kccstats/kccstats.html

# Features
 
# Requirement
 
* R
* RStudio
 
Windows10でのみ確認してます。

# Installation
 
# Usage
 
1. "kccstats.csv","kccstats_repo.csv"に自分の成績などを入力して保存します。書き方はNoteを見てください。
2. kccstats.Rmdを起動し実行します。
3. Markdownで出力したいときはknitしてください。必要なライブラリは適宜インストールしてください。

# Note

kccstats.csv
* courseID : 科目の番号。一意であればなんでもOK。
* className : 科目名。
* classGroup : 科目群。半角大文字で入力。
* isRequired : 必修は1、それ以外は0。サンプルでは経済学部必修科目と英語を1にしてます。
* credits : 単位数。
* creditsAccumulation : 累積単位数。"acquireSemester"の早い順に並べて、その時点での累積単位を入力。
* grade	: 成績。S,A,B,C,D のいずれかを入力。
* gradePoints : Sは4, Aは3, Bは2, Cは1, Dは0 を入力。
* GPA : gredePoints/creditの値を入力
* GPAaccumulation :  累積gradePoints。"acquireSemester"の早い順に並べて、その時点での累積gradePointsを入力。
* temporaryGPA :  一時GPA。"acquireSemester"の早い順に並べて、その時点でのGPAを入力。
* courseDivision : 科目区分。認定単位は0, 総合科目は1, 専門科目は2, 卒論・卒試は3。
* acquireSemester	: 単位取得年月。YYYY/MM で入力。
* acquireYear : 単位取得年度。1年目なら1, 2年目なら2, ...。
* examFaultTimes : 科目試験不合格回数。一発合格なら0。
* isFace2FaceExam : 対面試験を実施した科目は1, 代替試験を実施した科目は0。サンプルではオフラインスクーリングは1,オンラインスクーリングは0にしてます。
* isSchooling : スクーリングは1, テキスト科目は0。
* schoolingType : スクーリングのタイプ。夏スクはSS, 週末スクはWS, 夜スクはES, EスクはE。

kccstats_repo.csv
* reportID : レポートの番号。一意であればなんでもOK。ただし分冊があるレポートは分冊ごとに番号をつけてください。
* reportName : レポート名。
* reportDetail : 分冊の番号。
* submitTime : 何回目の提出か。再レポであれば1, 再々レポであれば2, ...。
* receiveDate : レポート提出日。kccchannelに表示されてる提出日をYYYY/MM/DDで入力。
* returnDate : レポート返送日。kccchannelに表示されてる返送日をYYYY/MM/DDで入力。
* result : 結果。合格or不合格。

# Author
 
* dskyshr
* Keio univ, faculty of economics

# License
 
This software is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).
