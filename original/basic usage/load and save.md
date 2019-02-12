<div class="static-content">
    <div class="index-list">
        * [Saving data using afterChange callback](https://handsontable.com/docs/6.2.2/tutorial-load-and-save.html#page-afterchange)
        * [Saving data locally using persistentState](https://handsontable.com/docs/6.2.2/tutorial-load-and-save.html#page-saving)
        * [Why should I use persistentState rather than regular LocalStorage API?](https://handsontable.com/docs/6.2.2/tutorial-load-and-save.html#page-using)
    </div>

    <div class="example-container clearfix">
        ### Saving data using afterChange callback

        Use the **afterChange** callback to track changes made in the table. In the example below,
        `AJAX` is used to load and save grid data. Note that this is just a mockup. Nothing is actually saved.
        You have to implement the server-side part by yourself.


        <div data-jsfiddle="example1" class="ajax-container">
            <div class="controls">
                <button name="load" id="load" class="intext-btn">Load</button>

                <button name="save" id="save" class="intext-btn">Save</button>

                <label><input type="checkbox" name="autosave" id="autosave" checked="checked" autocomplete="off">Autosave</label>
            </div>

            <pre id="example1console" class="console">
            Click "Load" to load data from server
            </pre>

            <div id="example1" class="hot handsontable htRowHeaders htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 350px; height: 211px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">2</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">3</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">4</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">5</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">6</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">7</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             
                                <div class="relative"><span class="rowHeader">8</span></div>                   |                                                              |                                                              |                                                              |                                                              |                                                              |                                                             

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
                        <div class="wtHider" style="width: 350px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


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
                        <div class="wtHider" style="height: 211px;">
                            <div class="wtSpreader" style="position: relative; top: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div>
                                ------------------------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                  
                                <div class="relative"><span class="rowHeader">2</span></div>                  
                                <div class="relative"><span class="rowHeader">3</span></div>                  
                                <div class="relative"><span class="rowHeader">4</span></div>                  
                                <div class="relative"><span class="rowHeader">5</span></div>                  
                                <div class="relative"><span class="rowHeader">6</span></div>                  
                                <div class="relative"><span class="rowHeader">7</span></div>                  
                                <div class="relative"><span class="rowHeader">8</span></div>                  

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

        <div class="codeLayout">
            <div class="buttons">
                <button class="dump" name="dump" data-dump="#example1" data-instance="hot" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span></span>
                <span class="code-line">  $$ = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">id</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">return</span> <span class="hljs-built_in">document</span>.getElementById(id);</span>
                <span class="code-line">  },</span>
                <span class="code-line">  container = $$(<span class="hljs-string">'example1'</span>),</span>
                <span class="code-line">  exampleConsole = $$(<span class="hljs-string">'example1console'</span>),</span>
                <span class="code-line">  autosave = $$(<span class="hljs-string">'autosave'</span>),</span>
                <span class="code-line">  load = $$(<span class="hljs-string">'load'</span>),</span>
                <span class="code-line">  save = $$(<span class="hljs-string">'save'</span>),</span>
                <span class="code-line">  autosaveNotification,</span>
                <span class="code-line">  hot;</span>
                <span class="code-line"></span>
                <span class="code-line">hot = <span class="hljs-keyword">new</span> Handsontable(container, {</span>
                <span class="code-line">  <span class="hljs-attr">startRows</span>: <span class="hljs-number">8</span>,</span>
                <span class="code-line">  <span class="hljs-attr">startCols</span>: <span class="hljs-number">6</span>,</span>
                <span class="code-line">  <span class="hljs-attr">rowHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">afterChange</span>: <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">change, source</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (source === <span class="hljs-string">'loadData'</span>) {</span>
                <span class="code-line">      <span class="hljs-keyword">return</span>; <span class="hljs-comment">//don't save this change</span></span>
                <span class="code-line">    }</span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (!autosave.checked) {</span>
                <span class="code-line">      <span class="hljs-keyword">return</span>;</span>
                <span class="code-line">    }</span>
                <span class="code-line">    clearTimeout(autosaveNotification);</span>
                <span class="code-line">    ajax(<span class="hljs-string">'scripts/json/save.json'</span>, <span class="hljs-string">'GET'</span>, <span class="hljs-built_in">JSON</span>.stringify({<span class="hljs-attr">data</span>: change}), <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">data</span>) </span>{</span>
                <span class="code-line">      exampleConsole.innerText  = <span class="hljs-string">'Autosaved ('</span> + change.length + <span class="hljs-string">' '</span> + <span class="hljs-string">'cell'</span> + (change.length > <span class="hljs-number">1</span> ? <span class="hljs-string">'s'</span> : <span class="hljs-string">''</span>) + <span class="hljs-string">')'</span>;</span>
                <span class="code-line">      autosaveNotification = setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
                <span class="code-line">        exampleConsole.innerText =<span class="hljs-string">'Changes will be autosaved'</span>;</span>
                <span class="code-line">      }, <span class="hljs-number">1000</span>);</span>
                <span class="code-line">    });</span>
                <span class="code-line">  }</span>
                <span class="code-line">});</span>
                <span class="code-line"></span>
                <span class="code-line">Handsontable.dom.addEvent(load, <span class="hljs-string">'click'</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
                <span class="code-line">  ajax(<span class="hljs-string">'scripts/json/load.json'</span>, <span class="hljs-string">'GET'</span>, <span class="hljs-string">''</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">res</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">var</span> data = <span class="hljs-built_in">JSON</span>.parse(res.response);</span>
                <span class="code-line"></span>
                <span class="code-line">    hot.loadData(data.data);</span>
                <span class="code-line">    exampleConsole.innerText = <span class="hljs-string">'Data loaded'</span>;</span>
                <span class="code-line">  });</span>
                <span class="code-line">});</span>
                <span class="code-line"></span>
                <span class="code-line">Handsontable.dom.addEvent(save, <span class="hljs-string">'click'</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
                <span class="code-line">  <span class="hljs-comment">// save all cell's data</span></span>
                <span class="code-line">  ajax(<span class="hljs-string">'scripts/json/save.json'</span>, <span class="hljs-string">'GET'</span>, <span class="hljs-built_in">JSON</span>.stringify({<span class="hljs-attr">data</span>: hot.getData()}), <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">res</span>) </span>{</span>
                <span class="code-line">    <span class="hljs-keyword">var</span> response = <span class="hljs-built_in">JSON</span>.parse(res.response);</span>
                <span class="code-line"></span>
                <span class="code-line">    <span class="hljs-keyword">if</span> (response.result === <span class="hljs-string">'ok'</span>) {</span>
                <span class="code-line">      exampleConsole.innerText = <span class="hljs-string">'Data saved'</span>;</span>
                <span class="code-line">    }</span>
                <span class="code-line">    <span class="hljs-keyword">else</span> {</span>
                <span class="code-line">      exampleConsole.innerText = <span class="hljs-string">'Save error'</span>;</span>
                <span class="code-line">    }</span>
                <span class="code-line">  });</span>
                <span class="code-line">});</span>
                <span class="code-line"></span>
                <span class="code-line">Handsontable.dom.addEvent(autosave, <span class="hljs-string">'click'</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
                <span class="code-line">  <span class="hljs-keyword">if</span> (autosave.checked) {</span>
                <span class="code-line">    exampleConsole.innerText = <span class="hljs-string">'Changes will be autosaved'</span>;</span>
                <span class="code-line">  }</span>
                <span class="code-line">  <span class="hljs-keyword">else</span> {</span>
                <span class="code-line">    exampleConsole.innerText =<span class="hljs-string">'Changes will not be autosaved'</span>;</span>
                <span class="code-line">  }</span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix head-gap">
        ### Saving data locally

        You can save any sort of data in local storage to preserve the table state after
        page reloads. In order to enable the data storage mechanism, the `persistentState`
        option must be set to `true` (you can set it either during the Handsontable initialization
        or using the updateSettings method).


        When `persistentState` is enabled it exposes 3 hooks listed below:

        * [persistentStateSave](https://handsontable.com/docs/6.2.2/Hooks.html#event:persistentStateSave)
        * [persistentStateLoad](https://handsontable.com/docs/6.2.2/Hooks.html#event:persistentStateLoad)
        * [persistentStateReset](https://handsontable.com/docs/6.2.2/Hooks.html#event:persistentStateReset)
    </div>

    <div>
        ### Why should I use persistentState rather than regular LocalStorage API?

        The main reason behind using `persistentState` hooks rather than a regular LocalStorage API
        is that it ensures separation of data stored by multiple Handsontable instances. In other words,
        if you have two (or more) instances of Handsontable on one page, data saved by one instance
        will be inaccessible to the second instance. Those two instances can store data under the same
        key and no data would be overwritten.


        **In order for the data separation to work properly, make sure that each instance
        of Handsontable has a unique `id`.**
    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/load-and-save.html)
</div>
