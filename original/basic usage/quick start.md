<div class="static-content">
    <div class="index-list">
        Follow these steps to install Handsontable:

        1.  [Install](https://handsontable.com/docs/6.2.2/tutorial-quick-start.html#page-install)
        2.  [Create](https://handsontable.com/docs/6.2.2/tutorial-quick-start.html#page-create)
        3.  [Initialize](https://handsontable.com/docs/6.2.2/tutorial-quick-start.html#page-bind)
        4.  [Alternative installation](https://handsontable.com/docs/6.2.2/tutorial-quick-start.html#page-alternative)
    </div>

    <div class="example-container clearfix" name="install">
        ### Step 1: Install

        <div class="tabs-alternative">
            <div class="tabs handsontable-switcher">
                <div class="tab switch active">
                    * Install Handsontable Pro
                    * Install Community Edition

                    <div class="tabs-content">
                        <div id="tab-content-pro" aria-hidden="false" class="content active">
                            [There are many ways](https://handsontable.com/pro-download.html) to install Handsontable Pro
                            but we suggest using [npm](https://www.npmjs.com/package/handsontable-pro).
                            Just type in the following command:



                                npm install handsontable-pro


                            After the installation process is finished, embed this code inside your HTML file:


                                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"node_modules/handsontable-pro/dist/handsontable.full.min.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span>
                                <span class="hljs-tag"><<span class="hljs-name">link</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"node_modules/handsontable-pro/dist/handsontable.full.min.css"</span> <span class="hljs-attr">rel</span>=<span class="hljs-string">"stylesheet"</span> <span class="hljs-attr">media</span>=<span class="hljs-string">"screen"</span>></span>


                            Alternatively, use a CDN:


                                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.jsdelivr.net/npm/handsontable-pro@6.2.2/dist/handsontable.full.min.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span><span class="hljs-tag"><<span class="hljs-name">link</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"https://cdn.jsdelivr.net/npm/handsontable-pro@6.2.2/dist/handsontable.full.min.css"</span> <span class="hljs-attr">rel</span>=<span class="hljs-string">"stylesheet"</span> <span class="hljs-attr">media</span>=<span class="hljs-string">"screen"</span>></span>

                        </div>

                        <div id="tab-content-ce" aria-hidden="true" class="content">
                            [There are many ways](https://handsontable.com/ce-download.html) to install Handsontable CE
                            but we suggest using
                            [npm](https://www.npmjs.com/package/handsontable).
                            Just type in the following command:



                                npm install handsontable


                            After the installation process is finished, embed this code inside your HTML file:


                                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"node_modules/handsontable/dist/handsontable.full.min.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span>
                                <span class="hljs-tag"><<span class="hljs-name">link</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"node_modules/handsontable/dist/handsontable.full.min.css"</span> <span class="hljs-attr">rel</span>=<span class="hljs-string">"stylesheet"</span> <span class="hljs-attr">media</span>=<span class="hljs-string">"screen"</span>></span>


                            Alternatively, use a CDN:


                                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.jsdelivr.net/npm/handsontable@6.2.2/dist/handsontable.full.min.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span><span class="hljs-tag"><<span class="hljs-name">link</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"https://cdn.jsdelivr.net/npm/handsontable@6.2.2/dist/handsontable.full.min.css"</span> <span class="hljs-attr">rel</span>=<span class="hljs-string">"stylesheet"</span> <span class="hljs-attr">media</span>=<span class="hljs-string">"screen"</span>></span>

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="example-container clearfix" name="create">
        ### Step 2: Create

        Add an empty `<div>` element that will be turned into a spreadsheet.
        Let's give this element an "example" ID.


        `<div id="example"></div>`
    </div>

    <div class="example-container clearfix" name="bind">
        ### Step 3: Initialize

        In the next step, pass a reference to that `<div id="example">` element and fill
        it with sample data:


            <span class="hljs-keyword">var</span> data = [
              [<span class="hljs-string">""</span>, <span class="hljs-string">"Ford"</span>, <span class="hljs-string">"Tesla"</span>, <span class="hljs-string">"Toyota"</span>, <span class="hljs-string">"Honda"</span>],
              [<span class="hljs-string">"2017"</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>],
              [<span class="hljs-string">"2018"</span>, <span class="hljs-number">20</span>, <span class="hljs-number">11</span>, <span class="hljs-number">14</span>, <span class="hljs-number">13</span>],
              [<span class="hljs-string">"2019"</span>, <span class="hljs-number">30</span>, <span class="hljs-number">15</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>]
            ];

            <span class="hljs-keyword">var</span> container = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example'</span>);
            <span class="hljs-keyword">var</span> hot = <span class="hljs-keyword">new</span> Handsontable(container, {
              <span class="hljs-attr">data</span>: data,
              <span class="hljs-attr">rowHeaders</span>: <span class="hljs-literal">true</span>,
              <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,
              <span class="hljs-attr">filters</span>: <span class="hljs-literal">true</span>,
              <span class="hljs-attr">dropdownMenu</span>: <span class="hljs-literal">true</span>
            });

    </div>

    <div class="example-container clearfix" name="result">
        ### Step 4: The result

        That's it, now your Handsontable Pro is up and ready to use:

        <div data-jsfiddle="example">
            <div id="example" class="hot handsontable htRowHeaders htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 305px; height: 119px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 52px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">A</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">B</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">C</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">D</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">E</span>
                                </div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                   |                                                                                                        | Ford                                                                                                   | Tesla                                                                                                  | Toyota                                                                                                 | Honda                                                                                                 
                                <div class="relative"><span class="rowHeader">2</span></div>                   | 2017                                                                                                   | 10                                                                                                     | 11                                                                                                     | 12                                                                                                     | 13                                                                                                    
                                <div class="relative"><span class="rowHeader">3</span></div>                   | 2018                                                                                                   | 20                                                                                                     | 11                                                                                                     | 14                                                                                                     | 13                                                                                                    
                                <div class="relative"><span class="rowHeader">4</span></div>                   | 2019                                                                                                   | 30                                                                                                     | 15                                                                                                     | 12                                                                                                     | 13                                                                                                    

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
                        <div class="wtHider" style="width: 305px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 52px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">A</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">B</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">C</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">D</span>
                                </div> | <div class="relative">
                                    <button class="changeType"></button><span class="colHeader">E</span>
                                </div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------


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

                <div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; width: 54px; transform: translate3d(0px, 0px, 0px);">
                    <div class="wtHolder" style="position: relative; width: 71px;">
                        <div class="wtHider" style="height: 119px;">
                            <div class="wtSpreader" style="position: relative; top: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div>
                                ------------------------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                  
                                <div class="relative"><span class="rowHeader">2</span></div>                  
                                <div class="relative"><span class="rowHeader">3</span></div>                  
                                <div class="relative"><span class="rowHeader">4</span></div>                  

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

                <div class="ht_clone_top_left_corner handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden; transform: translate3d(0px, 0px, 0px); height: 30px; width: 54px;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup><col class="rowHeader" style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div>
                                ------------------------------------------------------------------------------


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
            </div>
        </div>

        You are probably wondering how to not only bind the data source but also save the changes made
        in Handsontable Pro? Head to
        [Binding data](https://handsontable.com/docs/6.2.2/tutorial-data-binding.html) page to learn more about it.

    </div>

    <div class="example-container clearfix" name="alternative">
        ### Alternative installation

        Find all the available installation options on the
        [Download Handsontable Pro](https://handsontable.com/pro-download.html) page or [Download Handsontable CE](https://handsontable.com/ce-download.html) page.

    </div>

    <div class="example-container clearfix" name="nextsteps">
        ### Next steps

        * [How to connect the data source?](https://handsontable.com/docs/6.2.2/tutorial-data-sources.html)
        * [How to load and save data?](https://handsontable.com/docs/6.2.2/tutorial-load-and-save.html)
        * [How to create a custom HTML inside a cell or header?](https://handsontable.com/docs/6.2.2/demo-custom-renderers.html)
        * [How to validate data?](https://handsontable.com/docs/6.2.2/demo-data-validation.html)
    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/quick-start.html)
</div>
