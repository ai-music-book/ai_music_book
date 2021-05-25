## 第９章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 9-2-2 Performance RNNで高度なピアノ演奏曲の生成コマンド

Windows例
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

Mac例
```
performance_rnn_generate \
--config=multiconditioned_performance_with_dynamics \
--bundle_file=/Users/User-name/Documents/magenta-model/multiconditioned_performance_with_dynamics.mag \
--output_dir=/Users/YoshihiroSaito/Documents/magenta-music \
--num_outputs=10 \
--num_steps=3000 \
--notes_per_second=4 \
--pitch_class_histogram="[2, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 1]" \
--primer_pitches="[71,67,64,60]"
```
