# AI作曲本のサポートページです。
## 本ページの内容
- 各章ごとの生成・学習サンプルコマンド、ウェブリンクのURL
- 生成や学習に使用するMIDIファイル
- モデル作成用の参考となるmelody_rnn_model.py
- Magentaバージョンアップに伴うエラー対応策
- 正誤表
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。
コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。
特に改行文字`^` （キャレット）や `\` （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。
Windowsの改行文字 `^` （キャレット）はコマンドプロンプトの場合です。
PowerShellの場合は ``` ` ``` （バッククオート）となります。

*- Windowsでコピペがうまくいかない場合
Windows TerminalでコマンドプロンプトやPowerShellを使用してコピペがうまくいかない場合は
`CTRL + SHIFT + v`（ペーストの場合）
を試してみてください。*

生成音楽視聴用のYouTube動画や、学習済みデータダウンロード用のURLは、クリックする事で該当ページに移動できます。
MIDIファイルはダウンロードして該当のファイルを使用してください。
melody_rnn_model.pyは第１１章の独自モデルの開発において、ご自身で作成する際の参考用です。
こちらもご自身の用途に合わせ適宜変更してください。
Magenta（含むTensorFlowなどの依存ライブラリ）の更新によって新たに発生したエラーがある場合、その対策もここに記載します。
## 第１章
### 1-1
#### 1-1-1
- AIで自動作曲し音楽生成のリアル動画
https://youtu.be/oulHBPrFa8c
- AIで自動生成したピアノ曲
https://youtu.be/ovtD_2zGOQo
### 1-2
#### 1-2-1
- Magentaウェブサイト
https://magenta.tensorflow.org/
#### 1-2-2
- バッハのDoodle
https://www.google.com/doodles/celebrating-johann-sebastian-bach
補足解説
TensorFlowウェブサイト
https://www.tensorflow.org/
## 第２章
### 2-2
#### 2-2-2
- Pythonウェブサイト
https://www.python.org/
## 第３章
#### 3-1-3
- Melody RNNのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/melody_rnn
#### 3-2-1
- Melody RNN 生成コマンド実行例
- Windows例
```
melody_rnn_generate ^
--config=basic_rnn ^
--bundle_file=¥Users¥User-name¥Documents¥basic_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--num_steps=64 ^
--qpm=120.0 ^
--primer_melody="[60]"
```
- Mac例
```
melody_rnn_generate \
--config=basic_rnn \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/basic_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_melody="[60]"
```
#### 3-2-3
Melody RNN 生成曲のYouTube動画URL
https://youtu.be/tjzXqiiQxDI
MuseScoreダウンロードページ
https://musescore.org/ja/download
#### 3-3-2
Melody RNN primer_midi 生成コマンド実行例
- Windows例
```
melody_rnn_generate ^
--config=basic_rnn ^
--bundle_file=¥Users¥User-name¥Documents¥basic_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--num_steps=64 ^
--qpm=120.0 ^
--primer_midi=¥Users¥User-name¥Documents¥song001.mid
```
- Mac例
```
melody_rnn_generate \
--config=basic_rnn \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/basic_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_midi=/Users/KazuyukiIida/Dropbox/aimusic/song001.mid
```
## 第４章
#### 4-2-1
Drums RNNのGitHubページ
https://GitHub.com/tensorflow/magenta/tree/master/magenta/models/drums_rnn
#### 4-2-2
Drums RNN 生成コマンド実行例
- Windows例
```
drums_rnn_generate ^
--config=one_drum ^
--bundle_file=¥Users¥User-name¥Documents¥drum_kit_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--num_steps=256 ^
--qpm=120.0 ^
--primer_drums="[(36,)]"
```
- Mac例
```
melody_rnn_generate \
--config=one_drum \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/drum_kit_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--num_steps=256 \
--qpm=120.0 \
--primer_drums="[(36,)]"
```
#### 4-2-2
Drums RNN 生成曲視聴YouTube
https://youtu.be/pBuPmrNURxY
#### 4-3-2
Drums RNN primer_midi 生成コマンド実行例

- Windows例
```
drums_rnn_generate ^
--config=one_drum ^
--bundle_file=¥Users¥User-name¥Documents¥ drum_kit_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=1 ^
--num_steps=256 ^
--qpm=120.0 ^
--primer_midi=¥Users¥User-name¥Documents¥song001.mid
```
- Mac例
```
drums_rnn_generate \
--config=one_drum \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/drum_kit_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=1 \
--num_steps=256 \
--qpm=120.0 \
--primer_midi=/Users/KazuyukiIida/Dropbox/aimusic/drums001.mid
```
Drums RNN primer_midi 生成曲のYouTube動画URL
https://youtu.be/HWkqKxB_rNs
## 第５章
#### 5-1-1
MuiscVAE生成比較動画
https://youtu.be/K0_XQOf_CJw
#### 5-1-3
GrooVaeの仕組み
https://youtu.be/BeMiYihe09s
#### 5-1-4
MusicVAEのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/music_vae
#### 5-2-2
MusicVAE Sampleモード生成コマンド例
- Windows例
```
music_vae_generate ^
--config=hierdec-trio_16bar ^
--checkpoint_file=¥Users¥User-name¥Documents¥hierdec-trio_16bar.tar ^
--mode=sample ^
--num_outputs=10 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music
```
- Mac例
```
music_vae_generate \
--config=hierdec-trio_16bar \
--checkpoint_file=/Users/KazuyukiIida/Dropbox/aimusic/hierdec-trio_16bar.tar \
--mode=sample \
--num_outputs=10 \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music/
```
#### 5-2-2
MusicVae sampleモード生成曲のYouTube動画URL
https://youtu.be/oa5T1mp1zdk
#### 5-2-3
MusicVAE Interplateモード生成コマンド例
- Windows例
```
music_vae_generate ^
--config=hierdec-trio_16bar ^
--checkpoint_file=¥Users¥User-name¥Documents¥hierdec-trio_16bar.tar ^
--mode=interpolate ^
--num_outputs=10 ^
--input_midi_1=¥Users¥User-name¥Documents¥interpolate01.mid ^
--input_midi_2=¥Users¥User-name¥Documents¥interpolate02.mid ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music
```
- Mac例
```
music_vae_generate \
--config=hierdec-trio_16bar \
--checkpoint_file=/Users/KazuyukiIida/Dropbox/aimusic/hierdec-trio_16bar.tar \
--mode=interpolate \
--num_outputs=10 \
--input_midi_1=/Users/KazuyukiIida/Dropbox/aimusic/interpolate01.mid \
--input_midi_2=/Users/KazuyukiIida/Dropbox/aimusic/interpolate02.mid \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music
```
#### 5-2-3
MusicVAE Interplateモード生成曲のYouTube動画URL
https://youtu.be/Kqe0TAisazg
#### 5-3-1
MusicVAE nade-drums_2bar_full 生成コマンド例
- Windows例
```
music_vae_generate ^
--config=nade-drums_2bar_full ^
--checkpoint_file=¥Users¥User-name¥Documents¥nade-drums_2bar_full.tar ^
--mode=sample ^
--num_outputs=10 ^
--temperature=1.0 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music
```
- Mac例
```
music_vae_generate \
--config=nade-drums_2bar_full \
--checkpoint_file=/Users/KazuyukiIida/Dropbox/aimusic/nade-drums_2bar_full.tar \
--mode=sample \
--num_outputs=10 \
--temperature=1.0 \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music
```
MusicVAE nade-drums_2bar_full生成曲のYouTube動画URL
https://youtu.be/sQEsK1VNEyw
#### 5-3-2
MusicVAE groovae_4barの生成コマンド例
- Windows例
```
music_vae_generate ^
--config=groovae_4bar ^
--checkpoint_file=¥Users¥User-name¥Documents¥groovae_4bar.tar ^
--mode=sample ^
--num_outputs=10 ^
--temperature=1.0 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music
```
- Mac例
```
music_vae_generate \
--config=groovae_4bar \
--checkpoint_file=/Users/KazuyukiIida/Dropbox/aimusic/groovae_4bar.tar \
--mode=sample \
--num_outputs=10 \
--temperature=1.0 \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music
```
MusicVAE groovae_4bar生成曲のYouTube動画URL
https://youtu.be/tjB6HyDvPHE

#### 5-3-3
MusicVAE groovae_2bar_add_closed_hhの生成コマンド例
- Windows例
```
music_vae_generate ^
--config=groovae_2bar_add_closed_hh ^
--checkpoint_file= ¥Users¥User-name¥groovae_2bar_add_closed_hh.tar ^
--mode=interpolate ^
--num_outputs=2 ^
--temperature=0.1 ^
--input_midi_1=¥Users¥User-name¥Documents¥no-hh-8beat.mid ^
--input_midi_2=¥Users¥User-name¥Documents¥no-hh-16beat.mid ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music
```
- Mac例
```
music_vae_generate \
--config=groovae_2bar_add_closed_hh \
--checkpoint_file= /Users/User-name/groovae_2bar_add_closed_hh.tar \
--mode=interpolate \
--num_outputs=2 \
--temperature=0.1 \
--input_midi_1=/Users/KazuyukiIida/Dropbox/aimusic/no-hh-8beat.mid \
--input_midi_2=/Users/KazuyukiIida/Dropbox/aimusic/no-hh-16beat.mid \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music
```
MusicVAE groovae_2bar_add_closed_hh生成曲視聴YouTube
https://youtu.be/4q7zMi0jiuo
## 第６章
#### 6-1-3
Improv RNNのGitHubページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/improv_rnn
#### 6-2-1
Improv RNNの生成コマンド例
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60]" ^
--backing_chords="C G Am Em F C F G" ^
--steps_per_chord=16 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60]" \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=16 \
--render_chords=True
```
Improv RNN生成曲のYouTube動画URL
https://youtu.be/43iCXzK9iYg
#### 6-2-2
Improv RNN primer_melodyを駆使したカノン進行生成曲のYouTube動画URL
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " ^
--backing_chords="C G Am Em F C F G" ^
--steps_per_chord=16 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=16 \
--render_chords=True
```
Improv RNN primer_melodyを駆使した カノン進行生成曲YouTube視聴動画URL
https://youtu.be/gZBf7cgqyMI
#### 6-2-3 
primer_midiを使用してきらきら星の続き生成コマンド
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_midi=¥Users¥User-name¥Documents¥twinkle.mid ^
--backing_chords="C G Am Em F C F G" ^
--steps_per_chord=8 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_midi=/Users/KazuyukiIida/Dropbox/aimusic/twinkle.mid \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=8 \
--render_chords=True
```
primer_midiを使用してきらきら星の続き生成曲YouTube動画
https://youtu.be/3Hb8MEcO3MA
#### 6-3-3
Improv RNN ４和音7thコードでの生成コマンド
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[65, -2, -2, -2, 65, -2, 67, 69, -2, -2, -2, -1, 65, -1, 69, -2]" ^
--backing_chords="Fmaj7 Bm7b5 Em7 Am7" ^
--steps_per_chord=16 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[65, -2, -2, -2, 65, -2, 67, 69, -2, -2, -2, -1, 65, -1, 69, -2]" \
--backing_chords="Fmaj7 Bm7b5 Em7 Am7" \
--steps_per_chord=16 \
--render_chords=True
```
Improv RNN ４和音7thコードでの生成曲YouTube動画
https://youtu.be/0RGkVaTwfRE
#### 6-３-5 
テンションコードを使用した音楽生成 コマンド
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " ^
--backing_chords="Cmaj9 G11 Am9 Em7b13 Fmaj7#11 Cmaj9 Fmaj7#11 G9" ^
--steps_per_chord=16 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="Cmaj9 G11 Am9 Em7b13 Fmaj7#11 Cmaj9 Fmaj7#11 G9" \
--steps_per_chord=16 \
--render_chords=True
```
テンションコードのカノン進行で生成したメロディーYouTube動画
https://youtu.be/iTBLo_VIAAg
#### 6-３-6 
分数コードを使用した音楽生成 コマンド
- Windows例
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " ^
--backing_chords="Cmaj9/C G11/B Am9 Em7b13/G Fmaj7#11 Cmaj9/E Fmaj7#11 G9" ^
--steps_per_chord=16 ^
--render_chords=True
```
- Mac例
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/chord_pitches_improv.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="Cmaj9/C G11/B Am9 Em7b13/G Fmaj7#11 Cmaj9/E Fmaj7#11 G9" \
--steps_per_chord=16 \
--render_chords=True
```

分数コードを使用した生成曲YouTube動画
https://youtu.be/wCeFboc_TVk
##第７章
#### 7-1-2
GitHubのPolyphony RNNページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/polyphony_rnn
#### 7-2-2
バッハの様な合唱曲の生成コマンド
- Windows例
```
polyphony_rnn_generate ^
--bundle_file=¥Users¥User-name¥Documents¥polyphony_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, -2, 60, -2, -2, -2, 67, -2, -2, -2, 67, -2, -2, -2, ^
69, -2, -2, -2, 69, -2, -2, -2, 67, -2, -2, -2, -2, -2, -2, -2]" ^
--condition_on_primer=False ^
--inject_primer_during_generation=False
```
- Mac例
```
polyphony_rnn_generate \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/polyphony_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, -2, 60, -2, -2, -2, 67, -2, -2, -2, 67, -2, -2, -2, \
69, -2, -2, -2, 69, -2, -2, -2, 67, -2, -2, -2, -2, -2, -2, -2]" \
--condition_on_primer=False \
--inject_primer_during_generation=False
```
バッハの様な合唱曲の生成YouTube動画
https://youtu.be/HEHgOEyOysw
#### 7-2-３ 
和音を基にした合唱曲の生成 コマンド
- Windows例
```
polyphony_rnn_generate ^
--bundle_file=¥Users¥User-name¥Documents¥polyphony_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=133 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_pitches="[67,64,60]" ^
--condition_on_primer=True ^
--inject_primer_during_generation=False
```
- Mac例
```
polyphony_rnn_generate \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/polyphony_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--num_steps=133 \
--temperature=1.0 \
--qpm=120.0 \
--primer_pitches="[67,64,60]" \
--condition_on_primer=True \
--inject_primer_during_generation=False
```
和音を基にした合唱生成曲のYouTube動画
https://youtu.be/R8OqWrjeF4E 

#### 7-2-4 
既存の楽曲にバッハ風ハーモニーを加える音楽生成コマンド
- Windows例
```
polyphony_rnn_generate ^
--bundle_file=¥Users¥User-name¥Documents¥polyphony_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=1 ^
--num_steps=385 ^
-primer_midi=¥Users¥User-name¥Downloads¥twinkle_full.mid ^
--condition_on_primer=False ^
--inject_primer_during_generation=True
 ```
- Mac例
```
polyphony_rnn_generate \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/polyphony_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=1 \
--num_steps=385 \
-primer_midi=/Users/User-name/Downloads/twinkle_full.mid \
--condition_on_primer=False \
--inject_primer_during_generation=True
```
既存の楽曲にバッハ風ハーモニーを加えた生成曲YouTube動画
https://youtu.be/cR3cmAo6haw


## 第８章
#### 8-1-2
GitHubのPianoroll RNNのページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/pianoroll_rnn_nade

#### 8-2-2
Pianoroll RNNで複雑な和音メロディー曲の生成コマンド
- Windows例
```
pianoroll_rnn_nade_generate ^
--bundle_file=¥Users¥User-name¥Documents¥pianoroll_rnn_nade.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--qpm=90 ^
--num_outputs=10 ^
--num_steps=128 ^
--primer_pianoroll="[(67,64,60), (62,), (64,), (65,), (69,67, 64), (), (70,), (65, 62)]"
```
- Mac例
```
pianoroll_rnn_nade_generate \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/pianoroll_rnn_nade.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--qpm=90 \
--num_outputs=10 \
--num_steps=128 \
--primer_pianoroll="[(67,64,60), (62,), (64,), (65,), (69,67, 64), (), (70,), (65, 62)]"
```
Pianoroll RNNで複雑な和音メロディー曲視聴YouTube動画
https://youtu.be/g9MXuGXdiwY 

## 第９章
#### 9-1-2
YAMAHA E-Piano-Competitionの各演奏MIDIファイル
http://www.piano-e-competition.com/midiinstructions.asp

GitHubのPerformance RNNページ
https://github.com/tensorflow/magenta/tree/master/magenta/models/performance_rnn
#### 9-2-2
Performance RNNで高度なピアノ演奏曲の生成コマンド
- Windows例
```
performance_rnn_generate ^
--config=multiconditioned_performance_with_dynamics ^
--bundle_file=¥Users¥User-name¥Documents¥magenta-model¥multiconditioned_performance_with_dynamics.mag ^
--output_dir=¥Users¥YoshihiroSaito¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=3000 ^
--notes_per_second=4 ^
--pitch_class_histogram="[2, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 1]" ^
--primer_pitches="[71,67,64,60]"
```
- Mac例
```
performance_rnn_generate \
--config=multiconditioned_performance_with_dynamics \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/magenta-model/multiconditioned_performance_with_dynamics.mag \
--output_dir=/Users/YoshihiroSaito/Documents/magenta-music \
--num_outputs=10 \
--num_steps=3000 \
--notes_per_second=4 \
--pitch_class_histogram="[2, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 1]" \
--primer_pitches="[71,67,64,60]"
```
Performance RNNで高度なピアノ演奏曲生成曲視聴YouTubeリンク
https://youtu.be/MA8i_Mol4c8

Performance RNNブルース風の生成曲視聴YouTubeリンク
https://youtu.be/JPXheXQE4gI

## 第１０章
#### 10-2-2
NoteSequence（tfrecord）の作成
- Windows例
```
convert_dir_to_note_sequences ^
--input_dir=¥Users¥User-name¥Documents¥midi500 ^
--output_file=¥Users¥User-name¥Documents¥noteseq¥notesequences.tfrecord ^
--recursive
```
- Mac例
```
convert_dir_to_note_sequences \
--input_dir= /Users/KazuyukiIida/Dropbox/aimusic/midi500 \
--output_file= /Users/KazuyukiIida/Dropbox/aimusic/noteseq/notesequences.tfrecord \
--recursive
```
#### 10-2-3
学習データと評価データの作成コマンド
- Windows例
```
melody_rnn_create_dataset ^
--config=atention_rnn ^
--input= ¥Users¥User-name¥Documents¥noteseq¥notesequences.tfrecord ^
--output_dir= ¥Users¥User-name¥Documents¥sequence_examples ^
--eval_ratio=0.2
```
Mac
```
melody_rnn_create_dataset \
--config=attention_rnn \
--input=/Users/KazuyukiIida/Dropbox/aimusic/noteseq/notesequences.tfrecord \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/sequence_examples \
--eval_ratio=0.2
```
#### 10-2-4 
学習（トレーニング）コマンド
- Windows例
```
melody_rnn_train ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥training_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--num_training_steps=10000
```
- Mac例
```
melody_rnn_train \
--config=attention_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--sequence_example_file=/Users/KazuyukiIida/Dropbox/aimusic/sequence_examples/training_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--num_training_steps=10000
```
#### 10-2-5 
評価コマンド
- Windows例
```
melody_rnn_train ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥eval_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--num_training_steps=10000 ^
--eval
```
- Mac例
```
melody_rnn_train \
--config=attention_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--sequence_example_file=/Users/KazuyukiIida/Dropbox/aimusic/sequence_examples/eval_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--num_training_steps=10000 \
--eval
```
#### 10-2-6 
TensorBoardで学習の確認

- Windows例
```
tensorboard --logdir=¥Users¥User-name¥Documents¥logdir
```
- Mac例
```
tensorboard --logdir=/Users/KazuyukiIida/Dropbox/aimusic/logdir
```

#### 10-2-7 
音楽生成コマンド

- Windows例
```
melody_rnn_generate ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--primer_melody="[60]"
```
- Mac例
```
melody_rnn_generate \
--config=attention_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--primer_melody="[60]"
```
#### 10-2-8 
学習済みデータ（Bundleファイル）作成コマンド

- Windows例
```
melody_rnn_generate ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--bundle_file=¥Users¥User-name¥Downloads¥aimusic_book_rnn.mag ^
--save_generator_bundle
```
- Mac例
```
melody_rnn_generate \
--config=attention_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--bundle_file=/Users/User-name/Downloads/aimusic_book_rnn.mag \
--save_generator_bundle
```

## 第１１章
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
- Pythonファイルを使用した生成コマンド
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnnmelody_rnn_generate.py ^
--config=basic_rnn ^
--bundle_file=¥Users¥User-name¥Documents¥basic_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--num_steps=64 ^
--qpm=120.0 ^
--primer_melody="[60]"
```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_generate.py \
--config=basic_rnn \
--bundle_file=/Users/KazuyukiIida/Dropbox/aimusic/basic_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_melody="[60]"
```
#### 11-2-5
独自モデル設定 例
```
midi500_8bars_rnn': MelodyRnnConfig(
        generator_pb2.GeneratorDetails(
            id='midi500_8bars_rnn',
            description='500 8bars midi files with lookback'),
        magenta.music.LookbackEventSequenceEncoderDecoder(
            magenta.music.MelodyOneHotEncoding(
                min_note=0,
                max_note=128)),
        contrib_training.HParams(
            batch_size=64,
            rnn_layer_sizes=[64, 64],
            dropout_keep_prob=0.5,
            clip_norm=5,
            learning_rate=0.001),
        min_note=48,
        max_note=84,
        transpose_to_key=0)
```
Jump to definition機能について詳しく知りたい方はこちらをご覧ください。
https://canplay-music.com/2019/06/16/jumptodef/
#### 11-2-6
独自モデル学習コマンド例
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥melody_rnn_train.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥training_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--num_training_steps=9000
 ```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_train.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--sequence_example_file=/Users/KazuyukiIida/Dropbox/aimusic/sequence_examples/training_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--num_training_steps=9000
```
評価コマンド例
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥melody_rnn_train.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥eval_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--num_training_steps=9000 ^
--eval
```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_train.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--sequence_example_file=/Users/KazuyukiIida/Dropbox/aimusic/sequence_examples/eval_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--num_training_steps=9000 \
--eval
```
TensorBoardコマンド例
- Windows例
```
tensorboard --logdir=¥Users¥User-name¥Documents¥logdir
```
- Mac例
```
tensorboard --logdir=/Users/KazuyukiIida/Dropbox/aimusic/logdir
```
実行後
http://localhost:6006
でブラウザからTensorBoardを開きます。

学習中のチェックポイントファイルでの生成コマンド例
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--primer_melody="[60]"
```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--primer_melody="[60]"
```
#### 11-2-7
学習済みデータ作成コマンド例
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--bundle_file=¥Users¥User-name¥Downloads¥midi500_8bars_rnn.mag ^
--save_generator_bundle
```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/KazuyukiIida/Dropbox/aimusic/logdir/run1 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--bundle_file=/Users/User-name/Downloads/midi500_8bars_rnn.mag \
--save_generator_bundle
```
独自モデルでの生成コマンド例
- Windows例
```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--bundle_file=¥Users¥User-name¥Downloads¥midi500_8bars_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--primer_melody="[60]"
```
- Mac例
```
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--bundle_file=/Users/User-name/Downloads/midi500_8bars_rnn.mag \
--output_dir=/Users/KazuyukiIida/Dropbox/aimusic/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--primer_melody="[60]"
```
## 第１２章
#### 12-1-2
TensorFlowサイトのGPU環境ソフトウェア要件情報
https://www.tensorflow.org/install/gpu
#### 12-2-1
NVIDIA GPUドライバダウンロードページ
https://www.nvidia.co.jp/Download/index.aspx?lang=jp
#### 12-2-2
CUDA Toolkitダウンロードページ
https://developer.nvidia.com/cuda-downloads
#### 12-2-3
cuDNNダウンロードページ
https://developer.nvidia.com/rdp/cudnn-download
## 第１３章
#### 13-1
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
#### 13-2
- Magenta Studio ダウンロードリンク
https://magenta.tensorflow.org/studio
- Magenta Studio YouTube動画リンク
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
