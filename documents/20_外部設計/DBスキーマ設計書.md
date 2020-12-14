# データベース定義
- データベース名：shopping
- ユーザ名：student
- パスワード：himitu

# テーブル定義

## categories
カテゴリテーブル

|  フィールド名  |  キー  |  データ型  |  桁数  |  NULL  |  DEFAULT  |  説明  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  PK  |  SERIAL  |    |  N  |    |  カテゴリID オートインクリメント  |
|  name  |    |  VARCHAR  |  100  |  N  |    |  カテゴリ名  |

## items
商品テーブル

|  フィールド名  |  キー  |  データ型  |  桁数  |  NULL  |  DEFAULT  |  説明  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  PK  |  SERIAL  |    |  N  |    |  商品ID オートインクリメント  |
|  category_id  |  FK  |  INTEGER  |    |  N  |    |  カテゴリID  |
|  name  |    |  VARCHAR  |  100  |  N  |    |  商品名  |
|  detail  |    |  TEXT  |    |  N  |    |  商品説明  |
|  price  |    |  INTEGER  |    |  N  |    |  価格  |

# users
ユーザテーブル

|  フィールド名  |  キー  |  データ型  |  桁数  |  NULL  |  DEFAULT  |  説明  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  PK  |  SERIAL  |    |  N  |    |  会員ID オートインクリメント  |
|  name|    |  VARCHAR  |  50  |  N  |    |  会員名  |
|  email  |  UK  |  VARCHAR  |  250  |  N  |    |  メールアドレス  |
|  password  |    |  TEXT  |    |  N  |    |  パスワード  |
|  postcode  |    |  VARCHAR  |  7  |  N  |    |  郵便番号（ハイフンなし）  |
|  address  |    |  VARCHAR  |  200  |  N  |    |  住所  |
|  tel  |    |  VARCHAR  |  13  |  N  |    |  電話番号（ハイフンなし）  |
|  birthday  |    |  DATE  |    |  N  |    |  生年月日  |
|  is_admin  |    |  BOOLEAN  |  1  |  N  |  FALSE  |  TRUE:管理者 FALSE:一般会員  |
|  deleted_at  |    |  TIMESTAMP  |    |  Y  |    |  削除日時（退会日時）  |

