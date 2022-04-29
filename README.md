# Schedule_Bot
Googleスプレッドシート上にある時間割が更新されたらTwitterとLINEにその時間割を投稿するBotです。
たまに真っ白な時間割が投稿される場合もありますが、その10分後にはちゃんとした時間割が投稿されるのでご安心を。
LINEで通知を受け取りたい場合は@M1_SchedulesのDMへどうぞ。


--------------------------------------------------------------------------------------
[大雑把な解説]
1.10分おきにスプレッドシートが更新されているかどうかチェック

    [チェック方法]
      
	①今日の時間割をスクショし、トリミング(now.png)
	
	②前日スクショしたの時間割の画像(事前にGoogleDriveへアップロード済み)を取得(upload.png)
	
	③「①」と「②」の画像を比較
	
		[一致する(=更新されていない)場合] → プログラム終了、次の10分でまた実行
		
		[一致しない(=更新されている)場合] →「2.」に進む
		

2.今日スクショした時間割の画像をGoogleDriveへアップロード(明日比較するときに使用)



3.画像をツイートし、LINE Notify経由で送信してプログラム終了

--------------------------------------------------------------------------------------
