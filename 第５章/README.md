## 第５章サンプルコマンド
サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。 コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。 特に改行文字^ （キャレット）や \ （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。 Windowsの改行文字 ^ （キャレット）はコマンドプロンプトの場合です。 PowerShellの場合は ` （バッククオート）となります。

## 5-2-2 MusicVAE Sampleモード生成コマンド例 

Windows例
```
music_vae_generate ^ 
--config=hierdec-trio_16bar ^ 
--checkpoint_file=¥Users¥User-name¥Documents¥hierdec-trio_16bar.tar ^ 
--mode=sample ^ 
--num_outputs=10 ^ 
--output_dir=¥Users¥User-name¥Documents¥magenta-music 
```

Mac例
```
music_vae_generate \ 
--config=hierdec-trio_16bar \ 
--checkpoint_file=/Users/User-name/Documents/hierdec-trio_16bar.tar \ 
--mode=sample \ 
--num_outputs=10 \ 
--output_dir=/Users/User-name/Documents/magenta-music
```

## 5-2-3 MusicVAE Interplateモード生成コマンド例 

Windows例
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

Mac例
```
music_vae_generate \ 
--config=hierdec-trio_16bar \ 
--checkpoint_file=/Users/User-name/Documents/hierdec-trio_16bar.tar \ 
--mode=interpolate \ 
--num_outputs=10 \ 
--input_midi_1=/Users/User-name/Documents/interpolate01.mid \ 
--input_midi_2=/Users/User-name/Documents/interpolate02.mid \ 
--output_dir=/Users/User-name/Documents/magenta-music
```

## 5-3-1 MusicVAE nade-drums_2bar_full 生成コマンド例 
Windows例 
```
music_vae_generate ^ 
--config=nade-drums_2bar_full ^ 
--checkpoint_file=¥Users¥User-name¥Documents¥nade-drums_2bar_full.tar ^ 
--mode=sample ^ 
--num_outputs=10 ^ 
--temperature=1.0 ^ 
--output_dir=¥Users¥User-name¥Documents¥magenta-music 
```

Mac例 
```
music_vae_generate \ 
--config=nade-drums_2bar_full \ 
--checkpoint_file=/Users/User-name/Documents/nade-drums_2bar_full.tar \ 
--mode=sample \ 
--num_outputs=10 \ 
--temperature=1.0 \ 
--output_dir=/Users/User-name/Documents/magenta-music
```

## 5-3-2 MusicVAE groovae_4barの生成コマンド例 

Windows例 
```
music_vae_generate ^
--config=groovae_4bar ^
--checkpoint_file=¥Users¥User-name¥Documents¥groovae_4bar.tar ^
--mode=sample ^
--num_outputs=10 ^
--temperature=1.0 ^
--output_dir=¥Users¥User-name¥Documents¥magenta-music 
```

Mac例 
```
music_vae_generate \
--config=groovae_4bar \
--checkpoint_file=/Users/User-name/Documents/groovae_4bar.tar \
--mode=sample \
--num_outputs=10 \
--temperature=1.0 \
--output_dir=/Users/User-name/Documents/magenta-music
```

## 5-3-3 MusicVAE groovae_2bar_add_closed_hhの生成コマンド例 

Windows例 
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

Mac例 
```
music_vae_generate \ 
--config=groovae_2bar_add_closed_hh \ 
--checkpoint_file= /Users/User-name/groovae_2bar_add_closed_hh.tar \ 
--mode=interpolate \ 
--num_outputs=2 \ 
--temperature=0.1 \ 
--input_midi_1=/Users/User-name/Documents/no-hh-8beat.mid \ 
--input_midi_2=/Users/User-name/Documents/no-hh-16beat.mid \
--output_dir=/Users/User-name/Documents/magenta-music
```
