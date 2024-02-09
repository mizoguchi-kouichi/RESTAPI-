# RESTAPIのハンズオンまとめ
***
このRAEDME.mdでは、REATAPIの利用について以下のurlを参考に出来たことを
まとめております。

↓以下のURL  
https://github.com/raisetech-for-student/rest-api-handson?tab=readme-ov-file

***
# ◎GETリクエスト
###  ①ターミナルからGitHubにリクエスト
  -  ここでは、Terminalから下記のコードをコピーしリクエストします。
  -  ここでは、レスポンスで返ってくる値は、定期的に変わるものになります。
 
###  リクエスト結果の写真
  -  結果の赤の線で引いているところがレスポンスの値で、  
     3回リクエストしていますが、全てレスポンスの値が変わっております。       
![①レスポンス結果](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/d1accf0a-556f-4a4f-b046-50eec3c16b03)





### ②プロフィールの情報取得
  -  ここでは、下記のコードを入力して、ユーザのプロフィール情報を取得します。
  -  ここで、扱うURLの　https://api.github.com/usersには、46人のプロフィールの情報が
　　 JSONにて管理されております。
  -  私は、この中のidが1の方のデータを取得します。
  -  データの取得の際は、水色の線のURLを使用します。

![スクリーンショット 2024-02-07 161519](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/6d88d624-a10a-444b-8a86-5f6f710aedea)


### リクエスト結果の写真  
   -   リクエスト結果(1)の赤線を引いている箇所が、HTTPレスポンスステータスコードであり、
       「　200　ok 」と出力されていますので、リクエストが成功したことを示します。
   -    水色で記入されている箇所には、Content-Typeとcharset(文字コード)について示しています。
   -    このリクエスト結果からは、
   -    Content-Typeが application/json　　charsetがutf-8
        ということがわかります。
        
リクエスト結果(1)  
![②のレスポンス結果(1)](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/0f58ff9b-36d1-4101-b203-a7376b38bcba)


   -   リクエスト結果(2)からは、今回取得した人のプロフィール情報が出力されています。  
リクエスト結果(2)
![②のレスポンス結果⑵](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/3779546a-51a2-4dbb-8c1b-7fdf72533757)

### ③自分のアクセストークンを使用し情報を取得する















