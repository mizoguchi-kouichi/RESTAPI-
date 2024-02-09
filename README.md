# RESTAPIのハンズオンまとめ
***
このRAEDME.mdでは、REATAPIの利用について以下のurlを参考に出来たことを
まとめております。

↓以下のURL  
https://github.com/raisetech-for-student/rest-api-handson?tab=readme-ov-file

***
# ◎GETリクエスト
###  ①ターミナルからGitHubにリクエスト
  -  ここでは、Terminalに下記のコードをコピーしリクエストします。
```
% curl https://api.github.com/zen
```
  -  ここでは、レスポンスで返ってくる値は、定期的に変わるものになります。
 
###  リクエスト結果の写真
  -  結果の赤の線で引いているところがレスポンスの値で、  
     3回リクエストしていますが、全てレスポンスの値が変わっております。       
![①レスポンス結果](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/d1accf0a-556f-4a4f-b046-50eec3c16b03)





### ②プロフィールの情報取得
  -  ここでは、下記のコードを入力して、ユーザのプロフィール情報を取得します。
  -  ここで、扱うURLの　https://api.github.com/users
     には、登録している方のプロフィールの情報がJSONにて管理されております。
  -  私は、この中のidが1の方のデータを取得します。
  -  データの取得の際は、水色の線のURLを使用します。

![スクリーンショット 2024-02-07 161519](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/6d88d624-a10a-444b-8a86-5f6f710aedea)


### リクエスト結果の写真  
   -   リクエスト結果(1)の赤線を引いている箇所が、HTTPレスポンスステータスコードであり、
       「　200　ok 」と出力されていますので、リクエストが成功したことを示します。
   -    水色で記入されている箇所には、Content-Typeとcharset(文字コード)について示しています。
   -    このリクエスト結果からは、  
        Content-Typeが application/json　　charsetがutf-8  
        ということがわかります。
        
リクエスト結果(1)  
![②のレスポンス結果(1)](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/0f58ff9b-36d1-4101-b203-a7376b38bcba)


   -   リクエスト結果(2)からは、今回取得した人のプロフィール情報が出力されています。  
リクエスト結果(2)
![②のレスポンス結果⑵](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/3779546a-51a2-4dbb-8c1b-7fdf72533757)

### ③自分のアクセストークンを使用し情報を取得する
   -   ここでは、自分のgithubの名前とアクセストークンを使用して自分のプロフィールを取得します。
   -   ここで使うコードは下記になります。
```
curl -i -u  GitHubの自分の名前：GitHubのアクセストークン https://api.github.com/user
                                                      ↑半角スペース 
```

   -   リクエスト結果(1)を見て頂くとHTTPレスポンスステータスコードが「　200　ok 」のため  
       リクエストが成功している事になります。
       
リクエスト結果(1)
![③レスポンス結果⑴](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/db4e03e2-f215-4a69-b1d4-af53b7d8797f)

   -   リクエスト結果(2)は、自分のプロフィールのため、白色の四角で消しておりますが  
     　プロフィール情報が出力されたのがわかりました。

![③レスポンス結果⑵](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/b721cb97-3427-43ef-95e7-e9fe9ba3374c)

### ④postmanを使って自分のプロフィール情報を取得する事をリクエストします。
   -   ここでは、postmanで自分のプロフィールを情報を取得するをリクエストします。

### リクエスト結果の写真  

   -   リクエスト結果(1)の線の引いている箇所について解説します。  
   -   赤線の箇所は、HTTPメソッドを選択できます。  
     　今回の目的は情報の取得なので、　「　GET　」　になります。  
   - 　水色の箇所は、認証方法の種類になります。  
   - 　緑色の箇所は、メッセージで「認証が必要です」とレスポンスしております。
     
リクエスト結果(1)
![④のレスポンス結果⑴](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/bc3277c6-e2e3-49e9-a4d8-229edca5e467)



   -   リクエスト結果(2)の線の引いている箇所について解説します。
   -   赤線の箇所は、認証で必要なユーザ名とパスワードを入力しています。
     　今回のパスワードの箇所は、GitHubのアクセストークンになります。
   -   水色の箇所は、ステータスコードになります。
     　コードが　「　200 ok 」のため、リクエストが成功している事になります。

リクエスト結果(2)
![④のレスポンス結果(2)](https://github.com/mizoguchi-kouichi/RESTAPI-handson/assets/156568693/08ab9df9-9b49-4ac2-bec1-8e6990c7b3a2)


以上になります。
