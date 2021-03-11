# BLE_TEST
1000m タイムトライアルサイト　使い方

　1000mタイムトライアルサイトの使い方の説明です。

 

　 3本ローラーを使った1000mタイムトライアル時、タイムの計測と動画撮影・保存を行います。スピードセンサーはBluetooth Low Energy（BLE）に対応したものを使用してください。スピードケイデンス一体型のセンサーでもOKです。

　Windows 10のMicrosft Edgeで使用することを念頭に作りました。インターネットエクスプローラでは動かないと思いますが、ChromeやFirefoxの新しいものなら動くようです。スマホ（Android 7.0の古いもの）でも何とか動きました。

 

（追記）3月5日現在

　時刻計測にバグがあります。今朝、3本ローラーを使って実際に走って試してみたところ、実際より30秒近い差があるタイムが表示されてしまいました。

　また、CPUにATOM x5-z8300を使っている4年前のWindows10タブレットを使用したところ動画のコマ落ちがひどくて使えませんでした。

（追記）3月6日現在

　衝撃的な事実。時刻計測はバグではなかった。センサー内部の時計がずれているために、時刻計測がおかしなことになっていたことが判明。Cyplusのセンサーに換えて、XOSSのセンサーを使用したところ、真っ当そうな値が出た（XOSSのセンサーはCyplusのセンサーの電池蓋のツメが折れたため、念のために購入していたもの）。

　市販のサイコンではセンサーの時計を信用せず、自前の時計を使って計測しているのかもしれない。とりあえず、センサーを取り換えて様子をみよう。それでも不安なようなら、時刻計測の時計をパソコン側に持ってくることにしよう。

　XOSSのセンサーを使って撮影した動画はこちら。

https://youtu.be/GW5inyjE84I

（追記）3月10日現在

　いきなり終了してしまうバグを修正。時刻計測をすべてパソコン側に変更。時刻計測開始のタイミングもスタート時開始に変更。低スペックパソコン用に解像度を落としたもの（1000m Time Trial (fc2.com)）を用意。 

（追記）3月11日現在

　時刻計測をセンサー側に戻した。理由は速度表示が不安定になったため。０になったり、突然100ｋｍ/ｈを超すような表示が出たりとばらつく。考えてみれば当然で、ホイールが1回転した時の時刻ではなく、センサーが累積ホイール回転数値を返してきたタイミングの時刻を計測していたから。

 

 （使い方）

１．プロフィールの入力

　まず、プロフィールの入力を行います。英語で作ってみたのは、外国でも使ってくれたら面白いな、と思ったのと、日本語の読み上げ音声が不自然だったから。

　"Name"（名前）と"Tyre Circumstance"（タイヤ周長）は必須入力項目（名前は、英語

かローマ字で入力してください。ゴール後に参加者名の読み上げを行ってくれます。）。

　あとの項目は任意で結構ですが、入力が終わったらConfirmボタンを押してください。


２．スピードセンサーの接続

　Connect speed sensorボタンを押してください。小さな窓が開きます。

　最初にペアリング可能な機器を探してみつかったら、窓に表示されます（上記例ではXOSSのスピードセンサー。探すのに少し時間がかかることがあります。スピードセンサーがスリープ状態になっていると見つからないことがありますので、接続前には少しセンサーを動かして、スリープ状態から起こしてあげてください。）。

　次にペアリングしたい機器を選択してペアリングボタンを押します（スピードセンサとケイデンスセンサの両方を使用している場合には、２つのセンサーが検出されます。その場合にはスピードセンサーの方を選択するようにしてください。）。

　Bluetooth Low Energyを使用したスピードセンサーを使用してください。スピードケイデンス一体型センサーでもOKです。

　下の"BLE Status"窓に"> Notification started”と表示されたら、センサーが接続されてデータを取得できる状態になったことを示します。

　エラーになったら、もう一度Connect speed sensorボタンを押してみてください。

　何度やっても接続しないけれど、ほかのパソコン・スマホでは接続できる場合がありました。その時は、パソコンの「設定」→「デバイス」→「ブルートゥースとその他のデバイス」の接続機器のリストから、いったん削除することで接続できるようになったこともありました。

　それ以上の不具合対応はわかりませんので、ご勘弁。すみません、私も素人同然なので。

 

３．スタート

　センサーとの接続が確認されたらStart your trialボタンを押します。まず、カメラの使用を求めてくると思いますが、許可するとパソコンやスマホのカメラが起動して画面に表示され、録画が開始されます。なお、カメラの画像をどこかのサーバーに送るというような処理はしていませんのでご安心ください。画像データがあるのはユーザ機器の中だけです。　ボタンを押して30秒後にトライアルがはじまります。

　冒頭書いた理由から音声はすべて英語です（ブラウザが英語音声読み上げ対応していない場合には、不自然な日本語風の英語発音になります）。ちなみに、最初の言葉は"1000 meters time trial by cycle rollers. On your mark."。"On your mark"って、「位置について」みたいな意味らしいです。

　カウントダウンが終わって、赤いランプが付いたらスタートです。実はTime欄に出てくるストップウォッチみたいに流れていく数字も、読み上げ音声の秒もお飾りで、実際の計測には使っていません。ですから、スピードメータの立ち上がりが遅くて、最初は速度が0km/hと表示されるかもしれませんが気にしないでください（走り始めて１秒から2秒は時速0km/hと表示されると思います。）。

　スピードセンサーの仕組みが、1秒おきに累積ホイール回転数とそれを記録した時の時間（単位は1/1024秒）を送ってくるというものなので、スタート後に最初の１回転を記録した時間（T０秒とします。）とその時の累積回転数（C0とします）を起点として計測します。距離が1000ｍを超えた後ホイールが１回転したときの時間（T1秒とします。この時の回転数はタイヤ周長が2096ｍｍの場合には（C0＋478）回転。この間の走行距離（2096mm×478回転=1001.888m）と起点の時間から、1000ｍ走行のタイムを計算しています（（T1-T0）×1000/1001.888）。計測精度はタイヤ周長がクリティカルですね。タイヤ周長が2ミリ違えば、距離が１ｍ変わったのと同じですから。同じ700×23ｃでも、タイヤの種類、摩耗具合、体重、空気圧などでタイヤ周長は変わってきますので、タイムは一応1/100秒単位まで計算していますが、他の自転車の記録と比較する際はご注意ください。

　遊びで、残り400mになったときにジャン（打鐘音）を入れています。(17) KEIRIN【JKA】-競輪- - YouTubeにジャンの動画があったので、その一つから録音して音源にしています。念のため、競輪公式サイトにあった問い合わせフォームに照会中ですが、ダメと言われたら削除します。また、速度が時速100キロを超えたら、昭和の車にあったような速度警告音（キンコン）が鳴るように設定しています（私の今の実力では時速100キロなんて到底出ませんけど。）。このあたりは和風テイスト。

　1000ｍ走行が終わったら、ゴールの声とタイムの読み上げがあって計測終了です。

　なお、無限ループを避けるため、スタート後180秒（6分）以内にゴールすること（平均時速10㎞ですね）を前提にプログラムしました。ゴールまで6分以上かかった場合にどうなるかは確認していません。

 

４．録画について

 　ゴールすると自動的に録画が終了して、"Download  Video file"というリンクが付いたメッセージが現れます。クリックすると、"movie.webm"という名前のファイルがダウンロードできます。このファイルを動画再生すると、本ホームページ上部の情報（タイムトライアル中のタイムや速度やリザルトとカメラ画像）が映っているはずです。残念ながら音声が入っていません。多分、入れ方があるのだと思いますが、やり方を発見していません（navigator.mediaDevices.getUserMediaで、audioをtrueにしても、音は記録されませんでした。ハウリングが起きてうるさいだけなので、今はfalseにしています。音の記録のやり方がわかったら実装するかも。）。

　下部の"Stop Video and Download"ボタンはゴールしなかった場合に使用します。1000mを走り切った方には不要ですので押さないようにしてください。（3月6日ボタン削除）

　 

５．今後の予定

 〇youtubeへのアップ機能：

　決まったチャンネルを作って、そこにアップできるようにすれば、交流の場になるかも。

〇記録の記録

　サイトで計測した結果をボタン一つで登録するような機能を持たせれば、自分の記録の一覧性ができて励みになるだけでなく、ほかの人の記録も参考になると思います。年代ごとにベストタイムを競うなんてのも楽しいかも。世界中の人たちが記録するようなことになれば更に面白い。

　ただ、実装するとデータベースの管理責任ができてきますので気が重い。安全なサイトをつくるのは技術的にも難しそう。誰かやってくれないかな。自分で使ってないのでわからないけど、既存のサービス（Strava）とか、うまく使えないのかな。

〇見た目

　センスが無いので地味な見た目だけれど、もう少し格好良くしたい。

〇他のセンサ

　ケイデンスやパワーメータの数字を表示。面倒くさそう。

〇コード

　ちゃんとプログラムを作る人に取ったら、ひどいコードの書き方をしていると思う。<script>や<style?>の中身も音源データも一つにまとめていてるし、あちこちのサンプルプログラムの切り貼り細工。なんとかしたいとは思うけれど、なんともならなそう。githubでさらけ出しているので誰かなんとかしてくれないかな。


github.com

 〇普及　？

　たとえば、何か自転車のイベントがあった際に、3本ローラーとパソコンとBLE対応のスピードセンサーさえあれば、簡単に1000mタイムトライアル記録会が開催できると思います。

　ミノウラさん、アイデア採用してくれないかな、3本ローラーの販促になると思うけど。

