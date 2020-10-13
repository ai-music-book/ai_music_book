# AI作曲本のサポートページです。

## 本ページの内容
- 各章ごとの生成・学習サンプルコマンド、ウェブリンクのURL
- 生成や学習に使用するMIDIファイル
- モデル作成用の参考となるmelody_rnn_model.py
- Magentaバージョンアップに伴うエラー対応策
- 正誤表

サンプルコマンドはご自身の環境や実行内容に合わせパスや生成曲数などを変更して実行してください。
コマンドはコピペの際にスペース一つ、全角文字が一つ含まれる、だけでもエラーが出ますので、ご自身で確認もお願いします。
特に改行文字```^``` （キャレット）や ```\``` （バックスラッシュ）の後にスペースが含まれてしまう場合がありますのでご注意を。
Windowsの改行文字 ```^``` （キャレット）はコマンドプロンプトの場合です。
PowerShellの場合は ``` ` ``` （バッククオート）となります。

Windowsでコピペがうまくいかない場合
Windows TerminalでコマンドプロンプトやPowerShellを使用してコピペがうまくいかない場合は
```CTRL + SHIFT + v```（ペーストの場合）
を試してみてください。

生成音楽視聴用のYouTube動画や、学習済みデータダウンロード用のURLは、クリックする事で該当ページに移動できます。
MIDIファイルはダウンロードして該当のファイルを使用してください。
melody_rnn_model.pyは第１１章の独自モデルの開発において、ご自身で作成する際の参考用です。
こちらもご自身の用途に合わせ適宜変更してください。

Magenta（含むTensorFlowなどの依存ライブラリ）の更新によって新たに発生したエラーがある場合、その対策もここに記載します。
