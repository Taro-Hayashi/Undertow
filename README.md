# Undertow / Undertow Alterna ビルドガイド

- [キット内容](#キット内容)
- [組み立て](#組み立て)
- [キーのカスタマイズ](#キーのカスタマイズ)
- [その他](#その他)

## キット内容
![画像を添付](img/) 
||部品名|数| |
|-|-|-|-|
|1|メインボード|1||
|2|ボトムプレート|1||
|3|支柱|8|2種類あります|
||M2なべねじ（銀）|12|10mm|
||M2ワッシャー（銀）|||
||M2スプリングワッシャー（銀）|||
||M2なべねじ（黒）|4|8mm|
||M2ワッシャー（黒）|4||
||M2スプリングワッシャー（黒）|4||
||M2ナット（黒）|||
||M3角ナット|||
||M3なべねじ|||
||14pピンソケット|2||
||40pピンヘッダー|2||
||ジャンパーピン|8||
||MOSFET|1|LEDを発光させる場合に使用します|
||10kΩ抵抗|2|LEDを発光させる場合に使用します|

### キット以外に必要なもの
![画像を添付](img/) 
|部品名|数| |
|-|-|-|
|Killer Whale 側面ユニット|2||
|キースイッチ|4||
|キーキャップ|4||
|RP2040-Zero|1||
|Type-C USBケーブル|1||

### オプション
|部品名|数| |
|-|-|-|
|コンスルー|23ピン分|RP2040-Zeroを付け外しする場合|
|ピンソケット|23ピン分|RP2040-Zeroを付け外しする場合|
|RP2040-Zero|2つ付けると両側ともに使えます。|

## 組み立て
Undertow / Undertow Alternaには裏表と前後がありお好みの形状で組み立てることができます。 
![画像を添付](img/) 
ビルドガイドではUndertowを使いこのように組み立てます。  
![画像を添付](img/) 

### （オプション）LEDを発光させる場合
MOSFETと10kΩ抵抗をはんだ付けします。  
![画像を添付](img/) 

### 支柱の組み立て
M2なべねじ（銀）12本にM2ワッシャー（銀）を通します。  
![画像を添付](img/) 

支柱の保護フィルムをはがし、2種2つずつにスペーサーをなべねじで止めます。  
![画像を添付](img/) 

M3角ナットをスリットに立てます。
![画像を添付](img/) 

支柱で挟み込み、M2ワッシャー、M2スプリングワッシャー、M2ナットの順に通して固定します。  
![画像を添付](img/) 

### 側面ユニットへの支柱の取り付け
シルク印刷を見て側面ユニットの取り付け方を確認します。  
![画像を添付](img/) 

スイッチプレートを外した側面ユニットに支柱を差し込み、M3なべねじで止めます。  
![画像を添付](img/) 

側面ユニットの傾きに合わせてスイッチプレートや保護プレートを取り付けます。適宜各ユニットのビルドガイドをご覧ください。  
![画像を添付](img/) 

### ピンソケットのはんだ付け
14pピンソケット2本から6pを4本切り出します。  
![画像を添付](img/) 

側面ユニットのピンヘッダーに差し込み、側面ユニットの支柱をメインボードに差し込みM3なべねじで止めます。はんだ付けが終わったら外すのできつく締めないでください。  
![画像を添付](img/) 

ピンソケットをメインボードにはんだ付けして、ねじを外して側面ユニットと支柱をメインボードから外します。  
![画像を添付](img/) 

### RP2040-Zeroへのテストファームウェアの書き込み
こちらのuf2ファイルをダウンロードしてください。  
- !URL!

BOOTボタンを押しながらUSBケーブルでPCと接続するとRPI-RP2というドライブとして認識されるのでダウンロードしたuf2ファイルをドラッグアンドドロップするとキーボードとして認識されるようになります。  
![画像を添付](img/) 

### RP2040-Zeroのはんだ付け
RP2040-Zeroをピンソケットをはんだ付けしたのと同じ面に取り付けます。  
RP2040-Zeroに付属しているピンヘッダをメインボードに差し込み、RP2040-Zeroを乗せます。  
> [!IMPORTANT] 
> 組み立て方で裏表が異なります。シルク印刷の5V、0、7、15ピンの位置を合わせてください。
> ![画像を添付](img/)

![画像を添付](img/) 

ピンヘッダの足を切りRP2040-Zeroにはんだ付けします。  
![画像を添付](img/)  

裏返してRP2040-Zeroをメインボードに固定します。  
![画像を添付](img/)  

### ピンヘッダーのはんだ付け
ピンヘッダーをピンソケットをはんだ付けしたのと同じ面に取り付けます。  
40pピンヘッダー2本から4pを16個切り出します。  
![画像を添付](img/)  

枠内にはんだ付けします。  
> [!NOTE] 
> 面倒なら使う予定のユニット分だけでも大丈夫です。
![画像を添付](img/)  

使用する側面ユニットの種類にジャンパーピンを4つずつ差し込みます。  
![画像を添付](img/)  

### ボトムプレートの取り付け
ボトムプレートをメインボードに当てて、ボトムプレート側からM2なべネジ（黒）を差し込みます。  
![画像を添付](img/)   

反対側にワッシャー、スプリングワッシャー、ナットを取り付けます。  
![画像を添付](img/)  

### 側面ユニットの取り付け
側面ユニットのピンヘッダーをピンソケットに差し込みながら支柱をメインボードに差し込み、M3なべねじで固定します。  
![画像を添付](img/)  

ゴム足をボトムプレートに取り付けたら完成です。  
![画像を添付](img/)  

USBケーブルを差し込んで側面ユニットの反応を確かめてください。

## キーのカスタマイズ
### ファームウェアの更新
こちらのuf2ファイルをダウンロードしてください。
-  !URL!

一度USBケーブルを外し、画像に示したキーを押しながらPCに接続してしばらく待つとRPI-RP2ドライブが出てきます。  
![画像を添付](img/)  
うまくいかない場合はテストファームウェアを書き込んだ時と同様にRP2040-ZeroのBOOTボタンを押しながらUSBケーブルを差しこんでください。  

RPI-RP2ドライブにダウンロードしたuf2ファイルをドラッグアンドドロップしたらファームウェアの更新完了です。  

### Remapへの接続
Google Chrome（もしくはChromiumベースのブラウザ）でRemapにアクセスしてください。
- !URL!

青いボタンを押してUndertowを選ぶと接続できます。
![画像を添付](img/)   

### 保存と復元

### 形の変更
裏表、前後、Alternaとの切り替えはこちらから行えます。

### キーの割り当て
下の一覧からを上のキーにドラッグアンドドロップするとキー設定を変更することができます。
![画像を添付](img/)

### 特殊なキーの割り当て
FUNCTIONSタブのVIA USER KEYにOSに関わらず使えるショートカットやトラックボール、OLEDなどの設定をするキーがあります。

### LEDの調整


