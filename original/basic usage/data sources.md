<div class="static-content">
    <div class="index-list">
        This page shows how to use Handsontable with various data sources:

        * [Array data source](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-array)
        * [Array data source with hidden columns](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-array-hidden)
        * [Object data source](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-object)
        * [Object data source with column as a function](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-column-func)
        * [Object data source with column mapping (nested)](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-nested)
        * [Object data source with custom data schema](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-data-schema)
        * [Function data source and schema](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html#page-property-schema)

        **Please note that Handsontable will change the original data source.**
    </div>

    <div class="example-container clearfix" name="array">
        ### Array data source

        The most popular way of binding data with Handsontable is to use an **array of arrays**.

        <div data-jsfiddle="example1">
            <div id="example1" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 360px; height: 188px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div> | <div class="relative"><span class="colHeader">G</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                                                                             | Tesla                                                        | Nissan                                                       | Toyota                                                       | Honda                                                        | Mazda                                                        | Ford                                                        
                                2017                                                         | 10                                                           | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2018                                                         | 10                                                           | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2019                                                         | 10                                                           | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2020                                                         | 10                                                           | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2021                                                         | 10                                                           | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                                                                             |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 360px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div> | <div class="relative"><span class="colHeader">G</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example1">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example1" data-instance="hot1" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  data = [</span>
                <span class="code-line">    [<span class="hljs-string">''</span>, <span class="hljs-string">'Tesla'</span>, <span class="hljs-string">'Nissan'</span>, <span class="hljs-string">'Toyota'</span>, <span class="hljs-string">'Honda'</span>, <span class="hljs-string">'Mazda'</span>, <span class="hljs-string">'Ford'</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2017'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2018'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2019'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2020'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2021'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>]</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  container1 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example1'</span>),</span>
                <span class="code-line">  hot1;</span>
                <span class="code-line"></span>
                <span class="code-line">hot1 = <span class="hljs-keyword">new</span> Handsontable(container1, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: data,</span>
                <span class="code-line">  <span class="hljs-attr">startRows</span>: <span class="hljs-number">5</span>,</span>
                <span class="code-line">  <span class="hljs-attr">startCols</span>: <span class="hljs-number">5</span>,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="array-hidden">
        ### Array data source with hidden columns

        Let's say, you want the same data source, but without the **Tesla** column:

        <div data-jsfiddle="example2">
            <div id="example2" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 310px; height: 188px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                                                                             | Nissan                                                       | Toyota                                                       | Honda                                                        | Mazda                                                        | Ford                                                        
                                2017                                                         | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2018                                                         | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2019                                                         | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2020                                                         | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                2021                                                         | 11                                                           | 12                                                           | 13                                                           | 15                                                           | 16                                                          
                                                                                             |                                                              |                                                              |                                                              |                                                              |                                                             

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 310px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example2">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example2" data-instance="hot2" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  hiddenData = [</span>
                <span class="code-line">    [<span class="hljs-string">''</span>, <span class="hljs-string">'Tesla'</span>, <span class="hljs-string">'Nissan'</span>, <span class="hljs-string">'Toyota'</span>, <span class="hljs-string">'Honda'</span>, <span class="hljs-string">'Mazda'</span>, <span class="hljs-string">'Ford'</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2017'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2018'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2019'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2020'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'2021'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>]</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  container = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example2'</span>),</span>
                <span class="code-line">  hot2;</span>
                <span class="code-line"></span>
                <span class="code-line">hot2 = <span class="hljs-keyword">new</span> Handsontable(container, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: hiddenData,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span>,</span>
                <span class="code-line">  <span class="hljs-attr">columns</span>: [</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">0</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">2</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">3</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">4</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">5</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-number">6</span>}</span>
                <span class="code-line">  ]</span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="object">
        ### Object data source

        You can use an **array of objects** as a data source.

        <div data-jsfiddle="example3">
            <div id="example3" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 197px; height: 165px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 97px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                1                                                            | Ted Right                                                    |                                                             
                                2                                                            | Frank Honest                                                 |                                                             
                                3                                                            | Joan Well                                                    |                                                             
                                4                                                            | Gail Polite                                                  |                                                             
                                5                                                            | Michael Fair                                                 |                                                             
                                                                                             |                                                              |                                                             

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 197px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 97px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example3">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example3" data-instance="hot3" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  objectData = [</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Ted Right'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Frank Honest'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Joan Well'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">4</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Gail Polite'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">5</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Michael Fair'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>},</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  container3 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example3'</span>),</span>
                <span class="code-line">  hot3;</span>
                <span class="code-line"></span>
                <span class="code-line">hot3 = <span class="hljs-keyword">new</span> Handsontable(container3, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: objectData,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="nested">
        ### Object data source with column as a function

        You can define **columns** as a function. That could be a good choice, when do you want bind data more dynamically.

        <div data-jsfiddle="example4">
            <div id="example4" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 200px; height: 119px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                1                                                            | Ted                                                          | Right                                                        |                                                             
                                2                                                            |                                                              |                                                              |                                                             
                                3                                                            | Joan                                                         | Well                                                         |                                                             
                                                                                             |                                                              |                                                              |                                                             

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 200px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example4">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example4" data-instance="hot4" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span> nestedObjects = [</span>
                <span class="code-line">      {<span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: {<span class="hljs-attr">first</span>: <span class="hljs-string">"Ted"</span>, <span class="hljs-attr">last</span>: <span class="hljs-string">"Right"</span>}, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>},</span>
                <span class="code-line">      {<span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>}, <span class="hljs-comment">// HOT will create missing properties on demand</span></span>
                <span class="code-line">      {<span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">name</span>: {<span class="hljs-attr">first</span>: <span class="hljs-string">"Joan"</span>, <span class="hljs-attr">last</span>: <span class="hljs-string">"Well"</span>}, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>}</span>
                <span class="code-line">    ],</span>
                <span class="code-line">    container4 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example4'</span>),</span>
                <span class="code-line">    hot4;</span>
                <span class="code-line"></span>
                <span class="code-line">hot4 = <span class="hljs-keyword">new</span> Handsontable(container4, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: nestedObjects,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">columns</span>: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">column</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">var</span> columnMeta = {};</span>
                <span class="code-line"></span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (column === <span class="hljs-number">0</span>) {</span>
                <span class="code-line">      columnMeta.data = <span class="hljs-string">'id'</span>;</span>
                <span class="code-line"></span>
                <span class="code-line">    } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (column === <span class="hljs-number">1</span>) {</span>
                <span class="code-line">      columnMeta.data = <span class="hljs-string">'name.first'</span>;</span>
                <span class="code-line"></span>
                <span class="code-line">    } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (column === <span class="hljs-number">2</span>) {</span>
                <span class="code-line">      columnMeta.data = <span class="hljs-string">'name.last'</span>;</span>
                <span class="code-line"></span>
                <span class="code-line">    } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (column === <span class="hljs-number">3</span>) {</span>
                <span class="code-line">      columnMeta.data = <span class="hljs-string">'address'</span>;</span>
                <span class="code-line"></span>
                <span class="code-line">    } <span class="hljs-keyword">else</span> {</span>
                <span class="code-line">      columnMeta = <span class="hljs-literal">null</span>;</span>
                <span class="code-line"></span>
                <span class="code-line">    }</span>
                <span class="code-line"></span>
                <span class="code-line">    <span class="hljs-keyword">return</span> columnMeta;</span>
                <span class="code-line">  },</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="nested">
        ### Object data source with column mapping (nested)

        Some people have nested objects. They can also be used at the data source with a little bit of column
        mapping. The mapping is done using the **columns** option.

        <div data-jsfiddle="example5">
            <div id="example5" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 200px; height: 119px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                1                                                            | Ted                                                          | Right                                                        |                                                             
                                2                                                            |                                                              |                                                              |                                                             
                                3                                                            | Joan                                                         | Well                                                         |                                                             
                                                                                             |                                                              |                                                              |                                                             

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 200px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example5">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example5" data-instance="hot5" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  nestedObjects = [</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: {<span class="hljs-attr">first</span>: <span class="hljs-string">"Ted"</span>, <span class="hljs-attr">last</span>: <span class="hljs-string">"Right"</span>}, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>}, <span class="hljs-comment">// HOT will create missing properties on demand</span></span>
                <span class="code-line">    {<span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">name</span>: {<span class="hljs-attr">first</span>: <span class="hljs-string">"Joan"</span>, <span class="hljs-attr">last</span>: <span class="hljs-string">"Well"</span>}, <span class="hljs-attr">address</span>: <span class="hljs-string">""</span>}</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  container5 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example5'</span>),</span>
                <span class="code-line">  hot5;</span>
                <span class="code-line"></span>
                <span class="code-line">hot5 = <span class="hljs-keyword">new</span> Handsontable(container5, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: nestedObjects,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">columns</span>: [</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'id'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'name.first'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'name.last'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'address'</span>}</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="dataschema">
        ### Object data source with custom data schema

        When you use object data binding, Handsontable needs to know the data structure to create when you add a new
        row. If your data source contains at least one row, Handsontable will figure out the data structure based on the
        first row.

        In case you want to start with an empty data source, you will need to provide the **dataSchema**
        option that contains the data structure for any new row added to the grid.
        The below example shows custom data schema with an empty data source:

        <div data-jsfiddle="example6">
            <div id="example6" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 294px; height: 50px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 88px;"><col style="width: 87px;"><col style="width: 69px;"></colgroup>
                                <div class="relative"><span class="colHeader">ID</span></div> | <div class="relative"><span class="colHeader">First Name</span></div> | <div class="relative"><span class="colHeader">Last Name</span></div> | <div class="relative"><span class="colHeader">Address</span></div>
                                ------------------------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------
                                                                                              |                                                                       |                                                                      |                                                                   

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 294px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 88px;"><col style="width: 87px;"><col style="width: 69px;"></colgroup>
                                <div class="relative"><span class="colHeader">ID</span></div> | <div class="relative"><span class="colHeader">First Name</span></div> | <div class="relative"><span class="colHeader">Last Name</span></div> | <div class="relative"><span class="colHeader">Address</span></div>
                                ------------------------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example6">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example6" data-instance="hot6" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  container = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example6'</span>),</span>
                <span class="code-line">  hot6;</span>
                <span class="code-line"></span>
                <span class="code-line">hot6 = <span class="hljs-keyword">new</span> Handsontable(container, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: [],</span>
                <span class="code-line">  <span class="hljs-attr">dataSchema</span>: {<span class="hljs-attr">id</span>: <span class="hljs-literal">null</span>, <span class="hljs-attr">name</span>: {<span class="hljs-attr">first</span>: <span class="hljs-literal">null</span>, <span class="hljs-attr">last</span>: <span class="hljs-literal">null</span>}, <span class="hljs-attr">address</span>: <span class="hljs-literal">null</span>},</span>
                <span class="code-line">  <span class="hljs-attr">startRows</span>: <span class="hljs-number">5</span>,</span>
                <span class="code-line">  <span class="hljs-attr">startCols</span>: <span class="hljs-number">4</span>,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: [<span class="hljs-string">'ID'</span>, <span class="hljs-string">'First Name'</span>, <span class="hljs-string">'Last Name'</span>, <span class="hljs-string">'Address'</span>],</span>
                <span class="code-line">  <span class="hljs-attr">columns</span>: [</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'id'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'name.first'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'name.last'</span>},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: <span class="hljs-string">'address'</span>}</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap" name="propertyschema">
        ### Function data source and schema

        If your **dataSchema** is actually a constructor of an
        object that doesn't directly expose its members, like a Backbone.js
        model, you can specify functions for the **data** member
        of each **columns** item.


        The below example shows a small example of using such objects:

        <div data-jsfiddle="example7">
            <div id="example7" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 216px; height: 165px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 97px;"><col style="width: 69px;"></colgroup>
                                <div class="relative"><span class="colHeader">ID</span></div> | <div class="relative"><span class="colHeader">Name</span></div> | <div class="relative"><span class="colHeader">Address</span></div>
                                ------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------
                                1                                                             | Ted Right                                                       |                                                                   
                                2                                                             | Frank Honest                                                    |                                                                   
                                3                                                             | Joan Well                                                       |                                                                   
                                4                                                             | Gail Polite                                                     |                                                                   
                                5                                                             | Michael Fair                                                    |                                                                   
                                                                                              |                                                                 |                                                                   

                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; height: 30px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; height: 47px;">
                        <div class="wtHider" style="width: 216px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 97px;"><col style="width: 69px;"></colgroup>
                                <div class="relative"><span class="colHeader">ID</span></div> | <div class="relative"><span class="colHeader">Name</span></div> | <div class="relative"><span class="colHeader">Address</span></div>
                                ------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------


                                <div class="htBorders">
                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div>

                                        <div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>

                                    <div style="position: absolute; top: 0px; left: 0px;">
                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div>

                                        <div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="codeLayout">
            <div class="buttons">
                <button class="jsFiddleLink" data-runfiddle="example7">
                          <i class="fa fa-jsfiddle"></i>
                          Edit
                        </button>

                <button class="dump" name="dump" data-dump="#example7" data-instance="hot7" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  container7 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example7'</span>),</span>
                <span class="code-line">  hot7;</span>
                <span class="code-line"></span>
                <span class="code-line">hot7 = <span class="hljs-keyword">new</span> Handsontable(container7, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: [</span>
                <span class="code-line">    model({<span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Ted Right'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>}),</span>
                <span class="code-line">    model({<span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Frank Honest'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>}),</span>
                <span class="code-line">    model({<span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Joan Well'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>}),</span>
                <span class="code-line">    model({<span class="hljs-attr">id</span>: <span class="hljs-number">4</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Gail Polite'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>}),</span>
                <span class="code-line">    model({<span class="hljs-attr">id</span>: <span class="hljs-number">5</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Michael Fair'</span>, <span class="hljs-attr">address</span>: <span class="hljs-string">''</span>})</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  <span class="hljs-attr">dataSchema</span>: model,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: [<span class="hljs-string">'ID'</span>, <span class="hljs-string">'Name'</span>, <span class="hljs-string">'Address'</span>],</span>
                <span class="code-line">  <span class="hljs-attr">columns</span>: [</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: property(<span class="hljs-string">'id'</span>)},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: property(<span class="hljs-string">'name'</span>)},</span>
                <span class="code-line">    {<span class="hljs-attr">data</span>: property(<span class="hljs-string">'address'</span>)}</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span></span>
                <span class="code-line">});</span>
                <span class="code-line"></span>
                <span class="code-line"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">model</span>(<span class="hljs-params">opts</span>) </span>{</span>
                <span class="code-line">  <span class="hljs-keyword">var</span></span>
                <span class="code-line">    _pub = {},</span>
                <span class="code-line">    _priv = {</span>
                <span class="code-line">      <span class="hljs-string">"id"</span>: <span class="hljs-literal">undefined</span>,</span>
                <span class="code-line">      <span class="hljs-string">"name"</span>: <span class="hljs-literal">undefined</span>,</span>
                <span class="code-line">      <span class="hljs-string">"address"</span>: <span class="hljs-literal">undefined</span></span>
                <span class="code-line">    };</span>
                <span class="code-line"></span>
                <span class="code-line">  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> i <span class="hljs-keyword">in</span> opts) {</span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (opts.hasOwnProperty(i)) {</span>
                <span class="code-line">      _priv[i] = opts[i];</span>
                <span class="code-line">    }</span>
                <span class="code-line">  }</span>
                <span class="code-line"></span>
                <span class="code-line">  _pub.attr = <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">attr, val</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> val === <span class="hljs-string">'undefined'</span>) {</span>
                <span class="code-line">      <span class="hljs-built_in">window</span>.console && <span class="hljs-built_in">console</span>.log(<span class="hljs-string">"\t\tGET the"</span>, attr, <span class="hljs-string">"value of"</span>, _pub);</span>
                <span class="code-line">      <span class="hljs-keyword">return</span> _priv[attr];</span>
                <span class="code-line">    }</span>
                <span class="code-line">    <span class="hljs-built_in">window</span>.console && <span class="hljs-built_in">console</span>.log(<span class="hljs-string">"SET the"</span>, attr, <span class="hljs-string">"value of"</span>, _pub);</span>
                <span class="code-line">    _priv[attr] = val;</span>
                <span class="code-line"></span>
                <span class="code-line">    <span class="hljs-keyword">return</span> _pub;</span>
                <span class="code-line">  };</span>
                <span class="code-line"></span>
                <span class="code-line">  <span class="hljs-keyword">return</span> _pub;</span>
                <span class="code-line">}</span>
                <span class="code-line"></span>
                <span class="code-line"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">property</span>(<span class="hljs-params">attr</span>) </span>{</span>
                <span class="code-line">  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">row, value</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">return</span> row.attr(attr, value);</span>
                <span class="code-line">  }</span>
                <span class="code-line">}</span>

        </div>
    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/data-sources.html)
</div>
