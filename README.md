# テスト手順
## 大まかな流れ

①Unity起動

②メタバース内の各モニタ前に移動

③モニターをクリック

④演習室の仮想マシンにアクセス(noVNC）
　`PASS:aaaaaa`

⑤端末を開く

⑥課題内容に沿って課題を解く

⑦最後にMicrosoft formsで回答してもらう



# 課題内容

## 課題１　基本操作について


* kadai，testディレクトリの作成

`【home/e1b20XXX/】`

　ルートがこのようになるように作成する。以後、testディレクトリを作業ディレクトリとする。
　また、端末に【pwd】と入力することで現在のディレクトリを確認することができる。

　ディレクトリは【mkdir ディレクトリ名】で作成可能である。

　今回の場合は【mkdir -p kadai/test】となる。
　※現在のディレクトリが『home/e1b20XXX』の場合。違う場合は端末に【cd】と打ち込み、ホームディレクトリへ戻る。
　　また、コマンドオプション『-p』は階層のあるディレクトリ作成時に必須であるため、打ち忘れないようにする。


* ディレクトリ作成後、testディレクトリへ移動する

　ディレクトリの移動には『cdコマンド』を使用する。今回は下記のプログラムを打ち込む。

`【cd kadai/test】`


# 課題２　Hello Worldを出力するプログラムの作成(test1.c)


　nanoエディタを使用し、Hello Worldを表示するプログラムを作成する。
　操作については以下を参考にする。


①端末に【nano test1.c】と入力する

②nanoエディタが起動したら、下記のプログラムを入力する


```c:test1.c
#include <stdio.h>

int main(void){

 printf("Hello World\n");

return 0;
}
```

③入力終了後、CTRL＋Sを押して保存し、CTRL+Xでnanoエディタを終了する。


* ファイルのコンパイルを行う。コンパイル文は以下の通り

`gcc test1.c -o test1.exe`

もしくは

`gcc -o test1.exe test1.c`


* コンパイル確認後、ファイルを実行する。実行文は以下の通り

`./test1.exe`


実行後、端末に　Hello World　と表示されるとOKです。




# 課題３　生年月日を表示するプログラムの作成（test2.c）

　scanfを用いて、端末に入力された生年月日を表示するプログラムを作成する。

①端末に【nano test2.c】と入力する

②nanoエディタが起動したら、下記のプログラムを入力する

```c:test2.c
#include <stdio.h>

int main(void){

 int y = 0;
 int m = 0;
 int d = 0;

 printf("生年月日の年を西暦で入力してください：x = ");

 scanf("%d", &y);

 printf("生年月日の月を入力してください：m = ");

 scanf("%d", &m);

 printf("生年月日の日を入力してください：d = ");

 scanf("%d", &d);

 printf("あなたの生年月日は%d年%d月%d日です\n", y, m, d);

return 0;
}
```

③入力終了後、CTRL＋Sを押して保存し、CTRL+Xでnanoエディタを終了する。


* ファイルのコンパイルを行う。コンパイル文は以下の通り

`gcc test2.c -o test2.exe`

もしくは

`gcc -o test2.exe test2.c`


* コンパイル確認後、ファイルを実行する。実行文は以下の通り

`./test2.exe`


実行後、生年月日を入力し『あなたの生年月日はyyyy年mm月dd日です』と表示されるとOKです。
※yyyymmddのところは自分が入力した値で出力されるはずです。




# 課題４　端末に入力された２つの値を足すプログラムの作成（test3.c）


　scanfを用いて、端末に入力された2つの値を計算するプログラムを作成する。

①端末に【nano test3.c】と入力する

②nanoエディタが起動したら、下記のプログラムを入力する


```c:test3.c
#include <stdio.h>

int main(void){

 int a = 0;
 int b = 0;

 printf("1つ目の数値を入力してください：a = ");

 scanf("%d", &a);

 printf("2つ目の数値を入力してください：b = ");

 scanf("%d", &b);

 printf("a ＋ b = %d", a + b);
 printf("a － b = %d", a - b);
 printf("a × b = %d", a * b);
 printf("a ÷ b = %d", a / b);

return 0;
}
```


③ 入力終了後、CTRL＋Sを押して保存し、CTRL+Xでnanoエディタを終了する。


* ファイルのコンパイルを行う。コンパイル文は以下の通り

`gcc test3.c -o test3.exe`

もしくは

`gcc -o test3.exe test3.c`


* コンパイル確認後、ファイルを実行する。実行文は以下の通り

`./test3.exe`


実行後、入力した2つの値の足し算、引き算、掛け算、割り算が表示されればOKです。




# 課題５　入力された2つの数値の剰余を求めるプログラムの作成(test4.c)

　剰余（あまりのこと）を求めるプログラムを作成する。
　剰余は『％』で求めることができます。


①端末に【nano test4.c】と入力する

②nanoエディタが起動したら、下記のプログラムを入力する


```c:test3.c
#include <stdio.h>

int main(void){

 int a = 0;
 int b = 0;

 printf("1つ目の数値を入力してください：a = ");

 scanf("%d", &a);

 printf("2つ目の数値を入力してください：b = ");

 scanf("%d", &b);

 printf("a ÷ b の余りは%d", a % b);

return 0;
}
```


③入力終了後、CTRL＋Sを押して保存し、CTRL+Xでnanoエディタを終了する。


* ファイルのコンパイルを行う。コンパイル文は以下の通り

`gcc test4.c -o test4.exe`

もしくは

`gcc -o test4.exe test4.c`


* コンパイル確認後、ファイルを実行する。実行文は以下の通り

`./test4.exe`


実行後、入力した2つの値の剰余が表示されればOKです。
例）７ ÷ ５の余りは２



# 課題６　入力されたyyyymmdd形式の値から年月日を表示するプログラムの作成(test5.c)

　yyyymmdd形式からyyyy年mm月dd日に変換するプログラムを作成する。

　ファイル名は『test5.c』とし、nanoエディタを用いて作成する。
　作成後、gccでコンパイルを行う。

　成功していれば『20230101』を入力すると『2023年01月01日』と表示される。

　このプログラムは自力で作成する。


* コンパイル文は以下の通り

`gcc test5.c -o test5.exe`

もしくは

`gcc -o test5.exe test5.c`


* コンパイル確認後、ファイルを実行する。実行文は以下の通り

`./test5.exe`


以上です。ご協力ありがとうございました！！！
最後にformsでアンケートの記入お願いします。


## https://forms.gle/YUoEHzgvexfJ7Ck89











