## 第４章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 4-2-2 Drums RNN 生成コマンド実行例

リスト4.2(Windows)
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

リスト4.3(macOS)
```
melody_rnn_generate \
--config=one_drum \
--bundle_file=/Users/User-name/Documents/drum_kit_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--num_steps=256 \
--qpm=120.0 \
--primer_drums="[(36,)]"
```

## 4-3-2 Drums RNN primer_midi 生成コマンド実行例

リスト4.4(Windows)
```
drums_rnn_generate ^
--config=one_drum ^
--bundle_file=¥Users¥User-name¥Documents¥drum_kit_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=1 ^
--num_steps=256 ^
--qpm=120.0 ^
--primer_midi=¥Users¥User-name¥Documents¥song001.mid
```

リスト4.5(macOS)
```
drums_rnn_generate \
--config=one_drum \
--bundle_file=/Users/User-name/Documents/drum_kit_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=1 \
--num_steps=256 \
--qpm=120.0 \
--primer_midi=/Users/User-name/Documents/drums001.mid
```
