# bootstrap_practice

## 概要

<p>
元々は、Bootstrapの書籍を見ながら、写経するために作ったプロジェクト。
</p>
<p>
そこから、livecal(Fireloop野津さんに頼まれて進めているプロジェクトの仮称)の中で登録用のフォームを作成する必要があったため、そのままこの中でそのフォームを作成している。あまりお行儀が良いとは言えない。
</p>

## gitの設定
```
$ git remote -v
origin  https://github.com/cohyou/bootstrap_practice (fetch)
origin  https://github.com/cohyou/bootstrap_practice (push)
```

さらに、bootstrap-calendarというライブラリを使っているが、marginなど、form用に直接修正している。これはそもそもどうしましょうかね。submodule扱いなので、新しくforkしないといけないのでしょうか。
```Diff
diff --git a/dist/css/bootstrap-datepicker.css b/dist/css/bootstrap-datepicker.css
index 3cc60cd..e7b7aa9 100644
--- a/dist/css/bootstrap-datepicker.css
+++ b/dist/css/bootstrap-datepicker.css
@@ -10,6 +10,7 @@
   -moz-border-radius: 4px;
   border-radius: 4px;
   direction: ltr;
+  margin-left: 350px;
 }
 .datepicker-inline {
   width: 220px;
@@ -474,4 +475,4 @@

   margin-left: -5px;
   margin-right: -5px;
   -/*# sourceMappingURL=bootstrap-datepicker.css.map */
   \ No newline at end of file
   +/*# sourceMappingURL=bootstrap-datepicker.css.map */
   diff --git a/dist/css/bootstrap-datepicker3.css b/dist/css/bootstrap-datepicker3.css
   index 0a60427..cdcdc30 100644
   --- a/dist/css/bootstrap-datepicker3.css
   +++ b/dist/css/bootstrap-datepicker3.css
   @@ -681,4 +681,4 @@ fieldset[disabled] .datepicker table tr td span.active.disabled:hover.focus {
      margin-left: -5px;
      margin-right: -5px;
    }
   -/*# sourceMappingURL=bootstrap-datepicker3.css.map */
   \ No newline at end of file

   +/*# sourceMappingURL=bootstrap-datepicker3.css.map */
```
## 起動方法

- 写経した各サンプルに関しては、直接htmlをブラウザで起動する。
- livecal(概要を参照)用のフォームは`live_info_edit.html`なので、同様にブラウザで起動する。ただし、`live_info_edit.html`ではなぜかdatepickerやプルダウンが動作していない。
- と思ったら、livecal用のファイルは`color_sample`以下、`calendar.html`と`edit_live_info.html`のようです。`index.html`は配色を色々と試した跡がありますね。

## 見本にしたサイト

- 元のURLがすぐにはわからないが、calendar/calendar.htmlは、参考にした管理サイトからそのままCSSやjsごともらってきたものである。
