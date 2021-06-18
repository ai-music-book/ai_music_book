## 第６章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 6-2-1 Improv RNNの生成コマンド例 

リスト6.2(Windows)
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

リスト6.3(macOS)
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60]" \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=16 \
--render_chords=True
```

## 6-2-2 Improv RNN primer_melodyの生成コマンド 

リスト6.4(Windows)
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

リスト6.5(macOS)
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=16 \
--render_chords=True
```

## 6-2-3 primer_midiを使用してきらきら星の続き生成コマンド

リスト6.6(Windows)
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

リスト6.7(macOS) 
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_midi=/Users/User-name/Documents/twinkle.mid \
--backing_chords="C G Am Em F C F G" \
--steps_per_chord=8 \
--render_chords=True
```

## 6-3-3 Improv RNN ４和音7thコードでの生成コマンド

リスト6.8(Windows)
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[65, -2, -2, -2, 65, -2, 67, 69, -2, -2, -2, -1, 65, -1, 69, -2]" ^
--backing_chords="Fmaj7 Bm7b5 Em7 Am7” ^
--steps_per_chord=16 ^
--render_chords=True 
```

リスト6.9(macOS)
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[65, -2, -2, -2, 65, -2, 67, 69, -2, -2, -2, -1, 65, -1, 69, -2]" \
--backing_chords="Fmaj7 Bm7b5 Em7 Am7” \
--steps_per_chord=16 \
--render_chords=True
```

## 6-3-5 テンションコードを使用した音楽生成 コマンド 

リスト6.10(Windows)
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

リスト6.11(macOS) 
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="Cmaj9 G11 Am9 Em7b13 Fmaj7#11 Cmaj9 Fmaj7#11 G9" \
--steps_per_chord=16 \
--render_chords=True
```

## 6-3-6 分数コードを使用した音楽生成 コマンド

リスト6.12(Windows)
```
improv_rnn_generate ^
--config=chord_pitches_improv ^
--bundle_file=¥Users¥User-name¥Documents¥chord_pitches_improv.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " ^
--backing_chords="Cmaj9 G11/B Am9 Em7b13/G Fmaj7#11 Cmaj9/E Fmaj7#11 G9" ^
--steps_per_chord=16 ^
--render_chords=True 
```

リスト6.13(macOS)
```
improv_rnn_generate \
--config=chord_pitches_improv \
--bundle_file=/Users/User-name/Documents/chord_pitches_improv.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, 60, -1, -2, 67, -1, -2, -2, 67, 67, 67, -1, -2, -2] " \
--backing_chords="Cmaj9 G11/B Am9 Em7b13/G Fmaj7#11 Cmaj9/E Fmaj7#11 G9" \
--steps_per_chord=16 \
--render_chords=True
```
