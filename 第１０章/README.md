## 第１０章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 10-2-2 NoteSequence（tfrecord）の作成

リスト10.1(Windows)
```
convert_dir_to_note_sequences ^
--input_dir=¥Users¥User-name¥Documents¥midi500 ^
--output_file=¥Users¥User-name¥Documents¥noteseq¥notesequences.tfrecord ^
--recursive 
```

リスト10.2(macOS)
```
convert_dir_to_note_sequences \
--input_dir= /Users/User-name/Documents/midi500 \
--output_file= /Users/User-name/Documents/noteseq/notesequences.tfrecord \
--recursive
 ```
 
## 10-2-3 学習データと評価データの作成コマンド

リスト10.3(Windows)
```
melody_rnn_create_dataset ^
--config=attention_rnn ^
--input= ¥Users¥User-name¥Documents¥noteseq¥notesequences.tfrecord ^
--output_dir= ¥Users¥User-name¥Documents¥sequence_examples ^
--eval_ratio=0.2 
```
 
リスト10.4(macOS)
```
melody_rnn_create_dataset \
--config=attention_rnn \
--input=/Users/User-name/Documents/noteseq/notesequences.tfrecord \
--output_dir=/Users/User-name/Documents/sequence_examples \
--eval_ratio=0.2
```

## 10-2-4 学習（トレーニング）コマンド

リスト10.5(Windows)
```
melody_rnn_train ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥training_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--num_training_steps=10000 
```

リスト10.6(macOS)
```
melody_rnn_train \
--config=attention_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--sequence_example_file=/Users/User-name/Documents/sequence_examples/training_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--num_training_steps=10000
```

## 10-2-5 評価コマンド

リスト10.7(Windows)
```
melody_rnn_train ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥eval_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--num_training_steps=10000 ^
--eval
```

リスト10.8(macOS)
```
melody_rnn_train \
--config=attention_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--sequence_example_file=/Users/User-name/Documents/sequence_examples/eval_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--num_training_steps=10000 \
--eval
```

## 10-2-6 TensorBoardで学習の確認

リスト10.9(Windows)
```
tensorboard --logdir=¥Users¥User-name¥Documents¥logdir
 ```
 
リスト10.10(macOS)
```
tensorboard --logdir=/Users/User-name/Documents/logdir
```

実行後 <br>
http://localhost:6006
<br>
でブラウザからTensorBoardを開きます。 


## 10-2-7 音楽生成コマンド

リスト10.11(Windows)
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

リスト10.12(macOS)
```
melody_rnn_generate \
--config=attention_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--primer_melody="[60]"
```

## 10-2-8 学習済みデータ（Bundleファイル）作成コマンド

リスト10.13(Windows)
```
melody_rnn_generate ^
--config=attention_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" ^
--bundle_file=¥Users¥User-name¥Downloads¥aimusic_book_rnn.mag ^
--save_generator_bundle
```

リスト10.14(macOS)
```
melody_rnn_generate \
--config=attention_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64],attn_length=40" \
--bundle_file=/Users/User-name/Downloads/aimusic_book_rnn.mag \
--save_generator_bundle
```
