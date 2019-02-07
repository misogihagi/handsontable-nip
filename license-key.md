ライセンスキー
-----------
商用ライセンスを購入すると、Handsontableのライセンスキーを受け取ります。
それはあなたのアカウントの[my.handsontable.com](https://my.handsontable.com/)で利用可能になるでしょう。

以下の例のように、ライセンスキーを設定セクションに貼り付けてください。



    var container = document.getElementById('example');
    var hot = new Handsontable(container, {
      data: data,
      rowHeaders: true,
      colHeaders: true,
      licenseKey: '00000-00000-00000-00000-00000'
    });


ライセンスキーは文字列として渡されるため、引用符（''）で囲む必要があります。

Handsontableの商用ライセンスの価格は[こちら](https://handsontable.com/pricing)を確認してください。

このページの改善にご協力ください  
[日本語に問題がある場合](https://github.com/misogihagi/handsontable-nip/wiki)  
[Handsontableそのもの](https://github.com/handsontable/docs/edit/6.2.2/tutorials/licensing.html)
