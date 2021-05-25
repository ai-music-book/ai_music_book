## 第７章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 7-2-2 バッハ風合唱曲の生成コマンド

Windows例
```
polyphony_rnn_generate ^
--bundle_file=¥Users¥User-name¥Documents¥polyphony_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--temperature=1.0 ^
--qpm=120.0 ^
--primer_melody="[60, -2, -2, -2, 60, -2, -2, -2, 67, -2, -2, -2, 67, -2, -2, -2, 69, -2, -2, -2, 69, -2, -2, -2, 67, -2, -2, -2, -2, -2, -2, -2]" ^
--condition_on_primer=False ^
--inject_primer_during_generation=False 
```

Mac例
```
polyphony_rnn_generate \
--bundle_file=/Users/User-name/Documents/polyphony_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--temperature=1.0 \
--qpm=120.0 \
--primer_melody="[60, -2, -2, -2, 60, -2, -2, -2, 67, -2, -2, -2, 67, -2, -2, -2, 69, -2, -2, -2, 69, -2, -2, -2, 67, -2, -2, -2, -2, -2, -2, -2]" \
--condition_on_primer=False \
--inject_primer_during_generation=False
```

## 7-2-3 和音を基にした合唱曲の生成 コマンド

Windows例
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

Mac例
```
polyphony_rnn_generate \
--bundle_file=/Users/User-name/Documents/polyphony_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--num_steps=133 \
--temperature=1.0 \
--qpm=120.0 \
--primer_pitches="[67,64,60]" \
--condition_on_primer=True \
--inject_primer_during_generation=False
```

## 7-2-4 既存の楽曲にバッハ合唱曲風ハーモニーを加える音楽生成コマンド

Windows例 
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

Mac例 
```
polyphony_rnn_generate \
--bundle_file=/Users/User-name/Documents/polyphony_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=1 \
--num_steps=385 \
-primer_midi=/Users/User-name/Downloads/twinkle_full.mid \
--condition_on_primer=False \
--inject_primer_during_generation=True
```

