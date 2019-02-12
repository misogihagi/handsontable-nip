<div class="static-content">
    <div class="index-list">
        * [Introduction to cell options](https://handsontable.com/docs/6.2.2/tutorial-setting-options.html#page-options)
        * [How does the Cascading Configuration work?](https://handsontable.com/docs/6.2.2/tutorial-setting-options.html#page-config)
        * [The Cascading Configuration model](https://handsontable.com/docs/6.2.2/tutorial-setting-options.html#page-cascading)
    </div>

    <div class="example-container clearfix">
        ### Introduction to cell options

        Any constructor or column option may be overwritten for a particular cell (row/column combination),
        using `cell` array passed to the Handsontable constructor. Example:


            var hot = <span class="hljs-keyword">new</span> Handsontable(document.getElementById(<span class="hljs-string">'example'</span>), {
            <span class="hljs-symbol">  cell:</span> [
                {<span class="hljs-string">row:</span> <span class="hljs-number">0</span>, <span class="hljs-string">col:</span> <span class="hljs-number">0</span>, <span class="hljs-string">readOnly:</span> <span class="hljs-literal">true</span>}
              ]
            });


        Or using cells function property to the Handsontable constructor. Example:


            <span class="hljs-keyword">var</span> hot = <span class="hljs-keyword">new</span> Handsontable(<span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example'</span>), {
              <span class="hljs-attr">cells</span>: <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">row, col, prop</span>) </span>{
                <span class="hljs-keyword">var</span> cellProperties = {}

                <span class="hljs-keyword">if</span> (row === <span class="hljs-number">0</span> && col === <span class="hljs-number">0</span>) {
                  cellProperties.readOnly = <span class="hljs-literal">true</span>;
                }

                <span class="hljs-keyword">return</span> cellProperties;
              }
            })

    </div>

    <div class="example-container clearfix head-gap">
        ### How does the Cascading Configuration work?

        Since Handsontable 0.9 we use Cascading Configuration, which is a fast way to provide configuration options
        for the whole table, along with its columns and particular cells.

        Consider the following example:


            <span class="hljs-built_in">var</span> hot = <span class="hljs-built_in">new</span> Handsontable(document.getElementById('<span class="hljs-built_in">example</span>'), {
              readOnly: <span class="hljs-literal">true</span>,
              <span class="hljs-built_in">columns</span>: [
                {readOnly: <span class="hljs-literal">false</span>},
                {},
                {}
              ],
              cells: function (<span class="hljs-built_in">row</span>, <span class="hljs-built_in">col</span>, prop) {
                <span class="hljs-built_in">var</span> cellProperties = {}

                <span class="hljs-keyword">if</span> (<span class="hljs-built_in">row</span> === <span class="hljs-number">0</span> && <span class="hljs-built_in">col</span> === <span class="hljs-number">0</span>) {
                  cellProperties.readOnly = <span class="hljs-literal">true</span>;
                }

                <span class="hljs-built_in">return</span> cellProperties;
              }
            });


        The above notation will result in all TDs being read only, except for first column TDs
        which will be editable, except for the TD in top left corner which will still be read only.
    </div>

    <div class="example-container clearfix head-gap">
        ### The cascading configuration model

        The Cascading Configuration model is based on prototypal inheritance. It is much faster and memory
        efficient compared to the previous model that used jQuery extend. See it yourself:
        http://jsperf.com/extending-settings

        * **Constructor**

            Configuration options that are provided using first-level


                <span class="hljs-keyword">new</span> Handsontable(<span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example'</span>), {
                  <span class="hljs-attr">option</span>: <span class="hljs-string">'value'</span>
                });


            and `updateSettings` method.

        * **Columns**

            Configuration options that are provided using second-level object


                <span class="hljs-keyword">new</span> Handsontable(<span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example'</span>), {
                  <span class="hljs-attr">columns</span>: {
                    <span class="hljs-attr">option</span>: <span class="hljs-string">'value'</span>
                  }
                });


        * **Cells**

            Configuration options that are provided using second-level function


                <span class="hljs-keyword">new</span> Handsontable(<span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example'</span>), {
                  <span class="hljs-attr">cells</span>: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">row, col, prop</span>) </span>{

                  }
                });


    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/setting-options.html)
</div>
