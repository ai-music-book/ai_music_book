## 第１１章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。
 
## 11-1-4
pip install -e .

Pythonファイルを使用した生成コマンド
Windows例
 ```
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnnmelody_rnn_generate.py ^
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
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_generate.py \
--config=basic_rnn \
--bundle_file=/Users/User-name/Documents/basic_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=5 \
--num_steps=64 \
--qpm=120.0 \
--primer_melody=”[60]” 
 ```

11-2-5
独自モデル設定 例 
'midi500_8bars_rnn':
    MelodyRnnConfig(
        generator_pb2.GeneratorDetails(
            id='midi500_8bars_rnn',
            description='midi500_8bars_rnn RNN with lookback encoding and attention.'),
        note_seq.KeyMelodyEncoderDecoder(
            min_note=0, max_note=128),
        contrib_training.HParams(
            batch_size=128,
            rnn_layer_sizes=[128, 128],
            dropout_keep_prob=0.5,
            attn_length=40,
            clip_norm=3,
            learning_rate=0.001),
        min_note=0,
        max_note=128,
        transpose_to_key=None),


11-2-6
独自モデル学習コマンド例
Windows
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥melody_rnn_train.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥training_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--num_training_steps=9000
 
Mac 
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_train.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--sequence_example_file=/Users/User-name/Documents/sequence_examples/training_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--num_training_steps=9000


評価コマンド例 
Windows
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥melody_rnn_train.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--sequence_example_file=¥Users¥User-name¥Documents¥sequence_examples¥eval_melodies.tfrecord ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--num_training_steps=9000 ^
--eval

Mac
python /Users/User-name/magenta/magenta/models/melody_rnn/melody_rnn_train.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--sequence_example_file=/Users/User-name/Documents/sequence_examples/eval_melodies.tfrecord \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--num_training_steps=9000 \
--eval 


TensorBoardコマンド例
Windows
tensorboard --logdir=¥Users¥User-name¥Documents¥logdir

Mac
tensorboard --logdir=/Users/User-name/Documents/logdir
 

実行後 
http://localhost:6006 
でブラウザからTensorBoardを開きます。 


学習中のチェックポイントファイルでの生成コマンド例
Windows
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--primer_melody="[60]"

Mac
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--primer_melody="[60]"


11-2-7
学習済みデータ作成コマンド例
Windows
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--run_dir=¥Users¥User-name¥Documents¥logdir¥run1 ^
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" ^
--bundle_file=¥Users¥User-name¥Downloads¥midi500_8bars_rnn.mag ^
--save_generator_bundle

Mac
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--run_dir=/Users/User-name/Documents/logdir/run1 \
--hparams="batch_size=64,rnn_layer_sizes=[64,64]" \
--bundle_file=/Users/User-name/Downloads/midi500_8bars_rnn.mag \
--save_generator_bundle


独自モデルでの生成コマンド例
Windows
python ¥Users¥User-name¥magenta¥magenta¥models¥melody_rnn¥ melody_rnn_generate.py ^
--config=midi500_8bars_rnn ^
--bundle_file=¥Users¥User-name¥Downloads¥midi500_8bars_rnn.mag ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music ^
--num_outputs=10 ^
--num_steps=128 ^
--primer_melody="[60]"
 
Mac
python /Users/User-name/magenta/magenta/models/melody_rnn/ melody_rnn_generate.py \
--config=midi500_8bars_rnn \
--bundle_file=/Users/User-name/Downloads/midi500_8bars_rnn.mag \
--output_dir=/Users/User-name/Documents/magenta-music \
--num_outputs=10 \
--num_steps=128 \
--primer_melody="[60]"