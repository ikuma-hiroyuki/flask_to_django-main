## 更新メモ

### 2022/11/27 15:00

- mysql用のライブラリと、関連の設定ファイルを削除しました  
  Mac, Linux では mysqlclient のインストールが一筋縄ではいかないので、 requirements.txt から削除しました。  
  関連で、 config/mysql.py を削除しました。  
  この readme.md からも関連の記述を削除しました。

#### katoさんが当初リリースされた版からの主要な変更点というか、見どころメモ:

| ファイルパス          | 変更点                                          |
|-----------------|----------------------------------------------|
| metal/models.py | データベースの列名を変更した。                              |
| metal/views.py  | 新規にページを追加した。|
| metal/urls.py   | views.py での変更を反映。                            |

| url          | 変更点
|--------------|------------------------------------|
| /metal/_/    | /metal/ の関数 view 版                 |
| /metal/_buy/ | /metal/buy/ の関数 view 版             |
| /metal/buy/  | 購入完了時に thanks ページでメッセージを表示するようにした。 |
| /stock/      | 新規追加。                              |
| /stock/buy/  | 新規追加。クラスベースのview。                  |
| /stock/_buy/ | 新規追加。関数ベースのview。                   |

### 2022/12/11 08:00

django-debug-toolbar を導入しました。  

### 2022/12/13

- `./stock/vies.py`に`StockPurchaseList`を追加しました。
- `./stock/urls.py`の`urlpatterns`に`purchase_list`を追加しました。
- `./templates/stock/purchase_list.html`を追加しました。
- `./config/settings.py`の`INSTALLED_APPS`に`django_bootstrap5`を追加しました。
- ライブラリ `django-bootstrap5`をインストールしました。
- `requirements.txt`に`bootstrap5`を追加しました。