## 3-2-1 Melody RNN 生成コマンド実行例

Windows例
```
melody_rnn_generate ^
--config=basic_rnn ^
--bundle_file=¥Users¥User-name¥Documents¥basic_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=5 ^
--num_steps=64 ^
--qpm=120.0 ^
--primer_melody=”[60]”
```

Mac例
```
melody_rnn_generate \
--config=basic_rnn \
--bundle_file=/Users/User-name/Documents/basic_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_melody=”[60]”
```

## 3-3-2 Melody RNN primer_midi 生成コマンド実行例

Windows例
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

Mac例
```
melody_rnn_generate \
--config=basic_rnn \
--bundle_file=/Users/User-name/Documents/basic_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_midi=/Users/User-name/Documents/song001.mid
```