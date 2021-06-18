# Magentaで開発 AI作曲 サポートページ
<a href="https://canplay-music.com/aimusicbook/" target="blank">
<img src="https://canplay-music.com/wp-content/uploads/2021/06/aimusicbook.jpeg" title="Magenta AI MUSIC BOOK" width="450" height="600">
</a>

## Magentaで開発 AI作曲について
音楽のAIプログラミングとAI作曲について学べる<a href="https://canplay-music.com/">MUSIC TECH ACADEMY CANPLAY</a>の<a href="https://canplay-music.com/music-ai/">MUSIC AIプログラミング講義</a>の内容をまとめた解説本です。

## 本ページの内容
- 各章ごとの生成・学習サンプルコマンド（各章ディレクトリから確認）
- ウェブリンクのURL（当ページに記載）
- 生成や学習に使用するMIDIファイル（ai-music-book_midi.zip）
- モデル作成用の参考となる`melody_rnn_model.py`
- Magentaバージョンアップに伴うエラー対応策
- 正誤表

サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。
コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。
特に改行文字`^` （キャレット）や `\` （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。
Windowsの改行文字 `^` （キャレット）はコマンドプロンプトの場合です。
PowerShellの場合は ``` ` ``` （バッククオート）となります。

*Windowsでコピペがうまくいかない場合
Windows TerminalでコマンドプロンプトやPowerShellを使用してコピペがうまくいかない場合は
`CTRL + SHIFT + v`（ペーストの場合）
を試してみてください。*

生成音楽視聴用のYouTube動画や、学習済みデータダウンロード用のURLは、クリックする事で該当ページに移動できます。
MIDIファイルはダウンロードして該当のファイルを使用してください。
`melody_rnn_model.py`は第１１章の独自モデルの開発において、ご自身で作成する際の参考用です。
こちらもご自身の用途に合わせ適宜変更してください。

#### Magentaのバージョンアップ&エラー情報について
Magenta（含むTensorFlowなどの依存ライブラリ）のバージョンアップや、更新によって新たにエラーが出る場合の対策も併せて記載しますので実行に問題がある場合は確認をしてみてください。

全てのMIDIファイルとmelody_rnn_model.pyはこちらのリンク先ページからダウンロードできます。
（zipファイルになっておりますので解凍してご使用ください）
* [Magentaで開発 AI作曲 ファイルダウンロードページ](https://canplay-music.com/ai-music-book-downloads/)


## 第１章
#### 1-1-1
- AIで自動作曲し音楽生成実行中の動画
https://youtu.be/oulHBPrFa8c

- AIで自動生成したピアノ曲
https://youtu.be/ovtD_2zGOQo

#### 1-2-1
- Magentaウェブサイト
https://magenta.tensorflow.org/

#### 1-2-2
- バッハのDoodle
https://www.google.com/doodles/celebrating-johann-sebastian-bach

- 補足解説
TensorFlowウェブサイト
https://www.tensorflow.org/


## 第２章
#### 2-2-2
- Pythonウェブサイト
https://www.python.org/


## 第３章

- 第３章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%93%E7%AB%A0

#### 3-1-3
- Melody RNNのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/melody_rnn

#### 3-2-3
- Melody RNN 生成曲のYouTube動画
https://youtu.be/tjzXqiiQxDI

- MuseScoreダウンロードページ
https://musescore.org/ja/download


## 第４章

- 第４章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%94%E7%AB%A0

#### 4-2-1
- Drums RNNのGitHubページ
https://GitHub.com/tensorflow/magenta/tree/master/magenta/models/drums_rnn

#### 4-2-2
- Drums RNN 生成曲視聴YouTube動画
https://youtu.be/pBuPmrNURxY

#### 4-3-2
- Drums RNN primer_midi 生成曲のYouTube動画
https://youtu.be/HWkqKxB_rNs


## 第５章

- 第５章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%95%E7%AB%A0

#### 5-1-1
- MuiscVAE生成比較動画
https://youtu.be/K0_XQOf_CJw

#### 5-1-3
- GrooVaeの仕組み
https://youtu.be/BeMiYihe09s

#### 5-1-4
- MusicVAEのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/music_vae

#### 5-2-2
- MusicVae sampleモード生成曲のYouTube動画
https://youtu.be/oa5T1mp1zdk

#### 5-2-3
- MusicVAE Interplateモード生成曲のYouTube動画
https://youtu.be/Kqe0TAisazg

#### 5-3-1
- MusicVAE nade-drums_2bar_full生成曲のYouTube動画
https://youtu.be/sQEsK1VNEyw

#### 5-3-2
- MusicVAE groovae_4bar生成曲のYouTube動画
https://youtu.be/tjB6HyDvPHE

#### 5-3-3
- MusicVAE groovae_2bar_add_closed_hh生成曲視聴YouTube動画
https://youtu.be/4q7zMi0jiuo


## 第６章

- 第６章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%96%E7%AB%A0

#### 6-1-3
- Improv RNNのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/improv_rnn

#### 6-2-1
- Improv RNN生成曲のYouTube動画
https://youtu.be/43iCXzK9iYg

#### 6-2-2
- Improv RNN primer_melodyを駆使した カノン進行生成曲YouTube動画
https://youtu.be/gZBf7cgqyMI

#### 6-2-3
- primer_midiを使用してきらきら星の続き生成曲YouTube動画
https://youtu.be/3Hb8MEcO3MA

#### 6-3-3
- Improv RNN ４和音7thコードでの生成曲YouTube動画
https://youtu.be/0RGkVaTwfRE

#### 6-3-5
- テンションコードのカノン進行で生成したメロディーYouTube動画
https://youtu.be/iTBLo_VIAAg

#### 6-3-6
- 分数コードを使用した生成曲YouTube動画
https://youtu.be/wCeFboc_TVk


## 第７章

- 第７章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%97%E7%AB%A0

#### 7-1-2
- GitHubのPolyphony RNNページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/polyphony_rnn

#### 7-2-2
- バッハの様な合唱曲の生成YouTube動画
https://youtu.be/HEHgOEyOysw

#### 7-2-3
- 和音を基にした合唱生成曲のYouTube動画
https://youtu.be/R8OqWrjeF4E

#### 7-2-4
- 既存の楽曲にバッハ風ハーモニーを加えた生成曲YouTube動画
https://youtu.be/cR3cmAo6haw


## 第８章

- 第８章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%98%E7%AB%A0

#### 8-1-2
- GitHubのPianoroll RNNのページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/pianoroll_rnn_nade

#### 8-2-2
- Pianoroll RNNで複雑な和音メロディー曲視聴YouTube動画
https://youtu.be/g9MXuGXdiwY


## 第９章

- 第９章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%99%E7%AB%A0

#### 9-1-2
- YAMAHA E-Piano-Competitionの各演奏MIDIファイル
http://www.piano-e-competition.com/midiinstructions.asp

- GitHubのPerformance RNNページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/performance_rnn

#### 9-2-2
- Performance RNNで高度なピアノ演奏曲生成曲視聴YouTube動画
https://youtu.be/MA8i_Mol4c8

- Performance RNNブルース風の生成曲視聴YouTube動画
https://youtu.be/JPXheXQE4gI


## 第１０章
- 第１０章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%91%EF%BC%90%E7%AB%A0


## 第１１章
- 第１１章サンプルコマンド<br>
https://github.com/ai-music-book/ai_music_book/tree/master/%E7%AC%AC%EF%BC%91%EF%BC%91%E7%AB%A0

#### 11-1-3
Gitダウンロードリンク
- Windows
https://gitforwindows.org/

- Mac
https://sourceforge.net/projects/git-osx-installer/files/

- Magentaレポジトリのダウンロード（ZIPファイル）
https://github.com/tensorflow/magenta

- Magentaの過去のリリース一覧
https://github.com/magenta/magenta/releases

#### 11-2-1
Atom
https://atom.io/


## 第１２章
#### 12-1
- A.I.Duet
https://experiments.withgoogle.com/ai/ai-duet/view/

- Piano Genie
http://piano-genie.glitch.me/

- NSynth Sound Maker
https://experiments.withgoogle.com/ai/sound-maker/view/

- Melody Mixer
https://experiments.withgoogle.com/ai/melody-mixer/view/

- PerformanceRNN
https://magenta.tensorflow.org/demos/performance_rnn/

- Latent Loops
https://teampieshop.github.io/latent-loops/

- Beat Blender
https://experiments.withgoogle.com/ai/beat-blender/view/

- Multitrack Chords
https://codepen.io/iansimon/full/GGRYJZ

- MultiTrack Interpolating
https://codepen.io/iansimon/full/Bxgbgz/

- Piano Scribe
https://piano-scribe.glitch.me/

#### 12-2
- Magenta Studio ダウンロードリンク
https://magenta.tensorflow.org/studio

Magenta Studio YouTube各YouTube動画
- CONTINUE
https://youtu.be/5WYAK_J_XLU

- GENERATE 4BARS
https://youtu.be/-8bMPJ_Zo9E

- INTERPOLATE
https://youtu.be/D2ASaVMKZRs

- GrooVAE
https://youtu.be/3MmuWFkgYUY

- DRUMIFY
https://youtu.be/eYUaYzfZUCo

