# users
会員テーブル


|  フィールド名  |  キー  |  データ型  |  桁数  |  NULL  |  DEFAULT  |  説明  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|  id  |  PK  |  SERIAL  |    |  N  |    |  会員ID オートインクリメント  |
|  name|    |  VARCHAR  |  50  |  N  |    |  会員名  |
|  email  |  UQ  |  VARCHAR  |  250  |  N  |    |  メールアドレス  |
|  password  |    |  TEXT  |    |  N  |    |  パスワード  |
|  postcode  |    |  VARCHAR  |  7  |  N  |    |  郵便番号（ハイフンなし）  |
|  address  |    |  VARCHAR  |  200  |  N  |    |  住所  |
|  tel  |    |  VARCHAR  |  13  |  N  |    |  電話番号（ハイフンなし）  |
|  birthday  |    |  DATE  |    |  N  |    |  誕生日  |
|  is_admin  |    |  BOOLEAN  |  1  |  N  |    |  true:管理者 false:一般会員  |
|  deleted_at  |    |  TIMESTAMP  |    |  Y  |    |  削除（退会）日時  |
