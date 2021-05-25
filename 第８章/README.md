## 第８章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 8-2-2 Pianoroll RNNで複雑な和音メロディー曲の生成コマンド

Windows例
```
pianoroll_rnn_nade_generate ^
--bundle_file=¥Users¥User-name¥Documents¥pianoroll_rnn_nade.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--qpm=90 ^
--num_outputs=10 ^
--num_steps=128 ^
--primer_pianoroll="[(67,64,60), (62,), (64,), (65,), (69,67, 64), (), (70,), (65, 62)]"
```

Mac例
```
pianoroll_rnn_nade_generate \
--bundle_file=/Users/User-name/Documents/pianoroll_rnn_nade.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--qpm=90 \
--num_outputs=10 \
--num_steps=128 \
--primer_pianoroll="[(67,64,60), (62,), (64,), (65,), (69,67, 64), (), (70,), (65, 62)]"
```
