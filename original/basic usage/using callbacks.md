<div class="static-content">
    <div class="index-list">
        * [Callbacks](https://handsontable.com/docs/6.2.2/tutorial-using-callbacks.html#page-callbacks)
        * [Definition for `source` argument](https://handsontable.com/docs/6.2.2/tutorial-using-callbacks.html#page-source-definition)
        * [`beforeKeyDown` use case](https://handsontable.com/docs/6.2.2/tutorial-using-callbacks.html#page-beforeKeyDown)
    </div>

    <div class="example-container clearfix" name="callbacks">
        ### Callbacks

        This page shows usage of some callbacks available in Handsontable. If you require a new callback to be added,
        please [open an issue](https://github.com/handsontable/handsontable/issues/new).
        Note that some callbacks are checked on this page by default.


        <div data-jsfiddle="example1" class="part-left-container callbacks-container clearfix">
            <div id="example1" class="hot handsontable htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 349px; height: 165px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 52px;"><col style="width: 72px;"><col style="width: 50px;"><col style="width: 75px;"></colgroup>
                                <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div> | <div class="relative"><span class="colHeader">E</span></div> | <div class="relative"><span class="colHeader">F</span></div>
                                ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                                                                             | Tesla                                                        | Mazda                                                        | Mercedes                                                     | Mini                                                         | Mitsubishi                                                  
                                2017                                                         | 0                                                            | 2941                                                         | 4303                                                         | 354                                                          | 5814                                                        
                                2018                                                         | 3                                                            | 2905                                                         | 2867                                                         | 412                                                          | 5284                                                        
                                2019                                                         | 4                                                            | 2517                                                         | 4822                                                         | 552                                                          | 6127                                                        
                                2020                                                         | 2                                                            | 2422                                                         | 5399                                                         | 776                                                          | 4151                                                        
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
                        <div class="wtHider" style="width: 349px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 52px;"><col style="width: 72px;"><col style="width: 50px;"><col style="width: 75px;"></colgroup>
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

            <div id="example1_events">
                <div>0 @0.026 [afterCreateRow] 5, 1, "auto",</div>

                <div>1 @0.142 [afterChange] null, "loadData",</div>
            </div>
        </div>

        <div class="clear-log">
            <button onclick="$('#example1_events').empty()" class="intext-btn">Clear log</button>
        </div>

        **Choose events to be logged:**

        * <label><input type="checkbox" id="check_select_all"><strong>select all</strong></label>
        * <label><input type="checkbox" id="check_afterCellMetaReset"> afterCellMetaReset</label>
        * <label><input type="checkbox" checked="" id="check_afterChange"> afterChange</label>
        * <label><input type="checkbox" id="check_afterChangesObserved"> afterChangesObserved</label>
        * <label><input type="checkbox" id="check_afterContextMenuDefaultOptions"> afterContextMenuDefaultOptions</label>
        * <label><input type="checkbox" id="check_beforeContextMenuSetItems"> beforeContextMenuSetItems</label>
        * <label><input type="checkbox" id="check_afterDropdownMenuDefaultOptions"> afterDropdownMenuDefaultOptions</label>
        * <label><input type="checkbox" id="check_beforeDropdownMenuSetItems"> beforeDropdownMenuSetItems</label>
        * <label><input type="checkbox" id="check_afterContextMenuHide"> afterContextMenuHide</label>
        * <label><input type="checkbox" id="check_beforeContextMenuShow"> beforeContextMenuShow</label>
        * <label><input type="checkbox" id="check_afterContextMenuShow"> afterContextMenuShow</label>
        * <label><input type="checkbox" id="check_afterCopyLimit"> afterCopyLimit</label>
        * <label><input type="checkbox" id="check_beforeCreateCol"> beforeCreateCol</label>
        * <label><input type="checkbox" checked="" id="check_afterCreateCol"> afterCreateCol</label>
        * <label><input type="checkbox" id="check_beforeCreateRow"> beforeCreateRow</label>
        * <label><input type="checkbox" checked="" id="check_afterCreateRow"> afterCreateRow</label>
        * <label><input type="checkbox" id="check_afterDeselect"> afterDeselect</label>
        * <label><input type="checkbox" id="check_afterDestroy"> afterDestroy</label>
        * <label><input type="checkbox" id="check_afterDocumentKeyDown"> afterDocumentKeyDown</label>
        * <label><input type="checkbox" id="check_afterDrawSelection"> afterDrawSelection</label>
        * <label><input type="checkbox" id="check_beforeRemoveCellClassNames"> beforeRemoveCellClassNames</label>
        * <label><input type="checkbox" id="check_afterGetCellMeta"> afterGetCellMeta</label>
        * <label><input type="checkbox" id="check_afterGetColHeader"> afterGetColHeader</label>
        * <label><input type="checkbox" id="check_afterGetRowHeader"> afterGetRowHeader</label>
        * <label><input type="checkbox" id="check_afterInit"> afterInit</label>
        * <label><input type="checkbox" id="check_afterLoadData"> afterLoadData</label>
        * <label><input type="checkbox" id="check_afterMomentumScroll"> afterMomentumScroll</label>
        * <label><input type="checkbox" id="check_afterOnCellCornerMouseDown"> afterOnCellCornerMouseDown</label>
        * <label><input type="checkbox" id="check_afterOnCellCornerDblClick"> afterOnCellCornerDblClick</label>
        * <label><input type="checkbox" id="check_afterOnCellMouseDown"> afterOnCellMouseDown</label>
        * <label><input type="checkbox" id="check_afterOnCellMouseUp"> afterOnCellMouseUp</label>
        * <label><input type="checkbox" id="check_afterOnCellContextMenu"> afterOnCellContextMenu</label>
        * <label><input type="checkbox" id="check_afterOnCellMouseOver"> afterOnCellMouseOver</label>
        * <label><input type="checkbox" id="check_afterOnCellMouseOut"> afterOnCellMouseOut</label>
        * <label><input type="checkbox" checked="" id="check_afterRemoveCol"> afterRemoveCol</label>
        * <label><input type="checkbox" checked="" id="check_afterRemoveRow"> afterRemoveRow</label>
        * <label><input type="checkbox" id="check_afterRender"> afterRender</label>
        * <label><input type="checkbox" id="check_beforeRenderer"> beforeRenderer</label>
        * <label><input type="checkbox" id="check_afterRenderer"> afterRenderer</label>
        * <label><input type="checkbox" id="check_afterScrollHorizontally"> afterScrollHorizontally</label>
        * <label><input type="checkbox" id="check_afterScrollVertically"> afterScrollVertically</label>
        * <label><input type="checkbox" checked="" id="check_afterSelection"> afterSelection</label>
        * <label><input type="checkbox" id="check_afterSelectionByProp"> afterSelectionByProp</label>
        * <label><input type="checkbox" id="check_afterSelectionEnd"> afterSelectionEnd</label>
        * <label><input type="checkbox" id="check_afterSelectionEndByProp"> afterSelectionEndByProp</label>
        * <label><input type="checkbox" id="check_afterSetCellMeta"> afterSetCellMeta</label>
        * <label><input type="checkbox" id="check_afterRemoveCellMeta"> afterRemoveCellMeta</label>
        * <label><input type="checkbox" id="check_afterSetDataAtCell"> afterSetDataAtCell</label>
        * <label><input type="checkbox" id="check_afterSetDataAtRowProp"> afterSetDataAtRowProp</label>
        * <label><input type="checkbox" id="check_afterUpdateSettings"> afterUpdateSettings</label>
        * <label><input type="checkbox" id="check_afterValidate"> afterValidate</label>
        * <label><input type="checkbox" id="check_beforeLanguageChange"> beforeLanguageChange</label>
        * <label><input type="checkbox" id="check_afterLanguageChange"> afterLanguageChange</label>
        * <label><input type="checkbox" id="check_beforeAutofill"> beforeAutofill</label>
        * <label><input type="checkbox" id="check_beforeCellAlignment"> beforeCellAlignment</label>
        * <label><input type="checkbox" id="check_beforeChange"> beforeChange</label>
        * <label><input type="checkbox" id="check_beforeChangeRender"> beforeChangeRender</label>
        * <label><input type="checkbox" id="check_beforeDrawBorders"> beforeDrawBorders</label>
        * <label><input type="checkbox" id="check_beforeGetCellMeta"> beforeGetCellMeta</label>
        * <label><input type="checkbox" id="check_beforeRemoveCellMeta"> beforeRemoveCellMeta</label>
        * <label><input type="checkbox" id="check_beforeInit"> beforeInit</label>
        * <label><input type="checkbox" id="check_beforeInitWalkontable"> beforeInitWalkontable</label>
        * <label><input type="checkbox" id="check_beforeKeyDown"> beforeKeyDown</label>
        * <label><input type="checkbox" id="check_beforeOnCellMouseDown"> beforeOnCellMouseDown</label>
        * <label><input type="checkbox" id="check_beforeOnCellMouseUp"> beforeOnCellMouseUp</label>
        * <label><input type="checkbox" id="check_beforeOnCellContextMenu"> beforeOnCellContextMenu</label>
        * <label><input type="checkbox" id="check_beforeOnCellMouseOver"> beforeOnCellMouseOver</label>
        * <label><input type="checkbox" id="check_beforeOnCellMouseOut"> beforeOnCellMouseOut</label>
        * <label><input type="checkbox" id="check_beforeRemoveCol"> beforeRemoveCol</label>
        * <label><input type="checkbox" id="check_beforeRemoveRow"> beforeRemoveRow</label>
        * <label><input type="checkbox" id="check_beforeRender"> beforeRender</label>
        * <label><input type="checkbox" id="check_beforeSetRangeStartOnly"> beforeSetRangeStartOnly</label>
        * <label><input type="checkbox" id="check_beforeSetRangeStart"> beforeSetRangeStart</label>
        * <label><input type="checkbox" id="check_beforeSetRangeEnd"> beforeSetRangeEnd</label>
        * <label><input type="checkbox" id="check_beforeTouchScroll"> beforeTouchScroll</label>
        * <label><input type="checkbox" id="check_beforeValidate"> beforeValidate</label>
        * <label><input type="checkbox" id="check_beforeValueRender"> beforeValueRender</label>
        * <label><input type="checkbox" id="check_construct"> construct</label>
        * <label><input type="checkbox" id="check_init"> init</label>
        * <label><input type="checkbox" id="check_modifyCol"> modifyCol</label>
        * <label><input type="checkbox" id="check_unmodifyCol"> unmodifyCol</label>
        * <label><input type="checkbox" id="check_unmodifyRow"> unmodifyRow</label>
        * <label><input type="checkbox" id="check_modifyColHeader"> modifyColHeader</label>
        * <label><input type="checkbox" id="check_modifyColWidth"> modifyColWidth</label>
        * <label><input type="checkbox" id="check_modifyRow"> modifyRow</label>
        * <label><input type="checkbox" id="check_modifyRowHeader"> modifyRowHeader</label>
        * <label><input type="checkbox" id="check_modifyRowHeight"> modifyRowHeight</label>
        * <label><input type="checkbox" id="check_modifyData"> modifyData</label>
        * <label><input type="checkbox" id="check_modifyRowData"> modifyRowData</label>
        * <label><input type="checkbox" id="check_modifyGetCellCoords"> modifyGetCellCoords</label>
        * <label><input type="checkbox" id="check_persistentStateLoad"> persistentStateLoad</label>
        * <label><input type="checkbox" id="check_persistentStateReset"> persistentStateReset</label>
        * <label><input type="checkbox" id="check_persistentStateSave"> persistentStateSave</label>
        * <label><input type="checkbox" id="check_beforeColumnSort"> beforeColumnSort</label>
        * <label><input type="checkbox" id="check_afterColumnSort"> afterColumnSort</label>
        * <label><input type="checkbox" id="check_modifyAutofillRange"> modifyAutofillRange</label>
        * <label><input type="checkbox" id="check_modifyCopyableRange"> modifyCopyableRange</label>
        * <label><input type="checkbox" id="check_beforeCut"> beforeCut</label>
        * <label><input type="checkbox" id="check_afterCut"> afterCut</label>
        * <label><input type="checkbox" id="check_beforeCopy"> beforeCopy</label>
        * <label><input type="checkbox" id="check_afterCopy"> afterCopy</label>
        * <label><input type="checkbox" id="check_beforePaste"> beforePaste</label>
        * <label><input type="checkbox" id="check_afterPaste"> afterPaste</label>
        * <label><input type="checkbox" id="check_beforeColumnMove"> beforeColumnMove</label>
        * <label><input type="checkbox" id="check_afterColumnMove"> afterColumnMove</label>
        * <label><input type="checkbox" id="check_beforeRowMove"> beforeRowMove</label>
        * <label><input type="checkbox" id="check_afterRowMove"> afterRowMove</label>
        * <label><input type="checkbox" id="check_beforeColumnResize"> beforeColumnResize</label>
        * <label><input type="checkbox" id="check_afterColumnResize"> afterColumnResize</label>
        * <label><input type="checkbox" id="check_beforeRowResize"> beforeRowResize</label>
        * <label><input type="checkbox" id="check_afterRowResize"> afterRowResize</label>
        * <label><input type="checkbox" id="check_afterGetColumnHeaderRenderers"> afterGetColumnHeaderRenderers</label>
        * <label><input type="checkbox" id="check_afterGetRowHeaderRenderers"> afterGetRowHeaderRenderers</label>
        * <label><input type="checkbox" id="check_beforeStretchingColumnWidth"> beforeStretchingColumnWidth</label>
        * <label><input type="checkbox" id="check_beforeFilter"> beforeFilter</label>
        * <label><input type="checkbox" id="check_afterFilter"> afterFilter</label>
        * <label><input type="checkbox" id="check_modifyColumnHeaderHeight"> modifyColumnHeaderHeight</label>
        * <label><input type="checkbox" id="check_beforeUndo"> beforeUndo</label>
        * <label><input type="checkbox" id="check_afterUndo"> afterUndo</label>
        * <label><input type="checkbox" id="check_beforeRedo"> beforeRedo</label>
        * <label><input type="checkbox" id="check_afterRedo"> afterRedo</label>
        * <label><input type="checkbox" id="check_modifyRowHeaderWidth"> modifyRowHeaderWidth</label>
        * <label><input type="checkbox" id="check_beforeAutofillInsidePopulate"> beforeAutofillInsidePopulate</label>
        * <label><input type="checkbox" id="check_modifyTransformStart"> modifyTransformStart</label>
        * <label><input type="checkbox" id="check_modifyTransformEnd"> modifyTransformEnd</label>
        * <label><input type="checkbox" id="check_afterModifyTransformStart"> afterModifyTransformStart</label>
        * <label><input type="checkbox" id="check_afterModifyTransformEnd"> afterModifyTransformEnd</label>
        * <label><input type="checkbox" id="check_afterViewportRowCalculatorOverride"> afterViewportRowCalculatorOverride</label>
        * <label><input type="checkbox" id="check_afterViewportColumnCalculatorOverride"> afterViewportColumnCalculatorOverride</label>
        * <label><input type="checkbox" id="check_afterPluginsInitialized"> afterPluginsInitialized</label>
        * <label><input type="checkbox" id="check_skipLengthCache"> skipLengthCache</label>
        * <label><input type="checkbox" id="check_afterTrimRow"> afterTrimRow</label>
        * <label><input type="checkbox" id="check_afterUntrimRow"> afterUntrimRow</label>
        * <label><input type="checkbox" id="check_beforeDropdownMenuShow"> beforeDropdownMenuShow</label>
        * <label><input type="checkbox" id="check_afterDropdownMenuShow"> afterDropdownMenuShow</label>
        * <label><input type="checkbox" id="check_afterDropdownMenuHide"> afterDropdownMenuHide</label>
        * <label><input type="checkbox" id="check_hiddenRow"> hiddenRow</label>
        * <label><input type="checkbox" id="check_hiddenColumn"> hiddenColumn</label>
        * <label><input type="checkbox" id="check_beforeAddChild"> beforeAddChild</label>
        * <label><input type="checkbox" id="check_afterAddChild"> afterAddChild</label>
        * <label><input type="checkbox" id="check_beforeDetachChild"> beforeDetachChild</label>
        * <label><input type="checkbox" id="check_afterDetachChild"> afterDetachChild</label>
        * <label><input type="checkbox" id="check_afterBeginEditing"> afterBeginEditing</label>
        * <label><input type="checkbox" id="check_beforeMergeCells"> beforeMergeCells</label>
        * <label><input type="checkbox" id="check_afterMergeCells"> afterMergeCells</label>
        * <label><input type="checkbox" id="check_beforeUnmergeCells"> beforeUnmergeCells</label>
        * <label><input type="checkbox" id="check_afterUnmergeCells"> afterUnmergeCells</label>
        * <label><input type="checkbox" id="check_afterListen"> afterListen</label>
        * <label><input type="checkbox" id="check_afterUnlisten"> afterUnlisten</label>
        * <label><input type="checkbox" id="check_afterContextMenuExecute"> afterContextMenuExecute</label>
        * <label><input type="checkbox" id="check_afterDropdownMenuExecute"> afterDropdownMenuExecute</label>
    </div>

    <div class="codeLayout">
        <div class="buttons">
            <!--<button class="jsFiddleLink" data-runfiddle="example1">-->

            <!--<i class="fa fa-jsfiddle"></i>-->

            <!--Edit-->

            <!--</button>-->

            <button class="dump" name="dump" data-dump="#example1" data-instance="hot" title="Print current data source to console">
                    <i class="fa fa-terminal"></i>
                    Dump data to console
                  </button>
        </div>


            <span class="code-line"><span class="hljs-keyword">var</span></span>
            <span class="code-line">  data = [</span>
            <span class="code-line">    [<span class="hljs-string">''</span>, <span class="hljs-string">'Tesla'</span>, <span class="hljs-string">'Mazda'</span>, <span class="hljs-string">'Mercedes'</span>, <span class="hljs-string">'Mini'</span>, <span class="hljs-string">'Mitsubishi'</span>],</span>
            <span class="code-line">    [<span class="hljs-string">'2017'</span>, <span class="hljs-number">0</span>, <span class="hljs-number">2941</span>, <span class="hljs-number">4303</span>, <span class="hljs-number">354</span>, <span class="hljs-number">5814</span>],</span>
            <span class="code-line">    [<span class="hljs-string">'2018'</span>, <span class="hljs-number">3</span>, <span class="hljs-number">2905</span>, <span class="hljs-number">2867</span>, <span class="hljs-number">412</span>, <span class="hljs-number">5284</span>],</span>
            <span class="code-line">    [<span class="hljs-string">'2019'</span>, <span class="hljs-number">4</span>, <span class="hljs-number">2517</span>, <span class="hljs-number">4822</span>, <span class="hljs-number">552</span>, <span class="hljs-number">6127</span>],</span>
            <span class="code-line">    [<span class="hljs-string">'2020'</span>, <span class="hljs-number">2</span>, <span class="hljs-number">2422</span>, <span class="hljs-number">5399</span>, <span class="hljs-number">776</span>, <span class="hljs-number">4151</span>]</span>
            <span class="code-line">  ],</span>
            <span class="code-line">  example1 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example1'</span>),</span>
            <span class="code-line">  config,</span>
            <span class="code-line">  $hooksList,</span>
            <span class="code-line">  hooks,</span>
            <span class="code-line">  hot;</span>
            <span class="code-line"></span>
            <span class="code-line">config = {</span>
            <span class="code-line">  <span class="hljs-attr">data</span>: data,</span>
            <span class="code-line">  <span class="hljs-attr">minRows</span>: <span class="hljs-number">5</span>,</span>
            <span class="code-line">  <span class="hljs-attr">minCols</span>: <span class="hljs-number">6</span>,</span>
            <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span>,</span>
            <span class="code-line">  <span class="hljs-attr">autoWrapRow</span>: <span class="hljs-literal">true</span>,</span>
            <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
            <span class="code-line">  <span class="hljs-attr">contextMenu</span>: <span class="hljs-literal">true</span></span>
            <span class="code-line">};</span>
            <span class="code-line"></span>
            <span class="code-line">$hooksList = $(<span class="hljs-string">'#hooksList'</span>);</span>
            <span class="code-line">hooks = Handsontable.hooks.getRegistered();</span>
            <span class="code-line"></span>
            <span class="code-line">hooks.forEach(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">hook</span>) </span>{</span>
            <span class="code-line">  <span class="hljs-keyword">var</span> checked = <span class="hljs-string">''</span>;</span>
            <span class="code-line"></span>
            <span class="code-line">  <span class="hljs-keyword">if</span> (hook === <span class="hljs-string">'afterChange'</span> || hook === <span class="hljs-string">'afterSelection'</span> || hook === <span class="hljs-string">'afterCreateRow'</span> || hook === <span class="hljs-string">'afterRemoveRow'</span> ||</span>
            <span class="code-line">      hook === <span class="hljs-string">'afterCreateCol'</span> || hook === <span class="hljs-string">'afterRemoveCol'</span>) {</span>
            <span class="code-line">    checked = <span class="hljs-string">'checked'</span>;</span>
            <span class="code-line">  }</span>
            <span class="code-line">  $hooksList.append(<span class="hljs-string">'<li><label><input type="checkbox" '</span> + checked + <span class="hljs-string">' id="check_'</span> + hook + <span class="hljs-string">'"> '</span> + hook + <span class="hljs-string">'</label></li>'</span>);</span>
            <span class="code-line">  config[hook] = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
            <span class="code-line">    log_events(hook, <span class="hljs-built_in">arguments</span>);</span>
            <span class="code-line">  }</span>
            <span class="code-line">});</span>
            <span class="code-line"></span>
            <span class="code-line"><span class="hljs-keyword">var</span> start = (<span class="hljs-keyword">new</span> <span class="hljs-built_in">Date</span>()).getTime();</span>
            <span class="code-line"><span class="hljs-keyword">var</span> i = <span class="hljs-number">0</span>;</span>
            <span class="code-line"><span class="hljs-keyword">var</span> timer;</span>
            <span class="code-line"><span class="hljs-keyword">var</span> example1_events = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"example1_events"</span>);</span>
            <span class="code-line"></span>
            <span class="code-line"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">log_events</span>(<span class="hljs-params">event, data</span>) </span>{</span>
            <span class="code-line">  <span class="hljs-keyword">if</span> (<span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'check_'</span> + event).checked) {</span>
            <span class="code-line">    <span class="hljs-keyword">var</span> now = (<span class="hljs-keyword">new</span> <span class="hljs-built_in">Date</span>()).getTime(),</span>
            <span class="code-line">      diff = now - start,</span>
            <span class="code-line">      vals, str, div, text;</span>
            <span class="code-line"></span>
            <span class="code-line">    vals = [</span>
            <span class="code-line">      i,</span>
            <span class="code-line">        <span class="hljs-string">"@"</span> + numbro(diff / <span class="hljs-number">1000</span>).format(<span class="hljs-string">'0.000'</span>),</span>
            <span class="code-line">        <span class="hljs-string">"["</span> + event + <span class="hljs-string">"]"</span></span>
            <span class="code-line">    ];</span>
            <span class="code-line"></span>
            <span class="code-line">    <span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> d = <span class="hljs-number">0</span>; d < data.length; d++) {</span>
            <span class="code-line">      <span class="hljs-keyword">try</span> {</span>
            <span class="code-line">        str = <span class="hljs-built_in">JSON</span>.stringify(data[d]);</span>
            <span class="code-line">      }</span>
            <span class="code-line">      <span class="hljs-keyword">catch</span> (e) {</span>
            <span class="code-line">        str = data[d].toString(); <span class="hljs-comment">// JSON.stringify breaks on circular reference to a HTML node</span></span>
            <span class="code-line">      }</span>
            <span class="code-line"></span>
            <span class="code-line">      <span class="hljs-keyword">if</span> (str === <span class="hljs-keyword">void</span> <span class="hljs-number">0</span>) {</span>
            <span class="code-line">        <span class="hljs-keyword">continue</span>;</span>
            <span class="code-line">      }</span>
            <span class="code-line"></span>
            <span class="code-line">      <span class="hljs-keyword">if</span> (str.length > <span class="hljs-number">20</span>) {</span>
            <span class="code-line">        str = <span class="hljs-built_in">Object</span>.prototype.toString.call(data[d]);</span>
            <span class="code-line">      }</span>
            <span class="code-line">      <span class="hljs-keyword">if</span> (d < data.length - <span class="hljs-number">1</span>) {</span>
            <span class="code-line">        str += <span class="hljs-string">','</span>;</span>
            <span class="code-line">      }</span>
            <span class="code-line">      vals.push(str);</span>
            <span class="code-line">    }</span>
            <span class="code-line"></span>
            <span class="code-line">    <span class="hljs-keyword">if</span> (<span class="hljs-built_in">window</span>.console) {</span>
            <span class="code-line">      <span class="hljs-built_in">console</span>.log(i,</span>
            <span class="code-line">          <span class="hljs-string">"@"</span> + numbro(diff / <span class="hljs-number">1000</span>).format(<span class="hljs-string">'0.000'</span>),</span>
            <span class="code-line">          <span class="hljs-string">"["</span> + event + <span class="hljs-string">"]"</span>,</span>
            <span class="code-line">        data);</span>
            <span class="code-line">    }</span>
            <span class="code-line">    div = <span class="hljs-built_in">document</span>.createElement(<span class="hljs-string">"DIV"</span>);</span>
            <span class="code-line">    text = <span class="hljs-built_in">document</span>.createTextNode(vals.join(<span class="hljs-string">" "</span>));</span>
            <span class="code-line"></span>
            <span class="code-line">    div.appendChild(text);</span>
            <span class="code-line">    example1_events.appendChild(div);</span>
            <span class="code-line">    clearTimeout(timer);</span>
            <span class="code-line">    timer = setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{</span>
            <span class="code-line">      example1_events.scrollTop = example1_events.scrollHeight;</span>
            <span class="code-line">    }, <span class="hljs-number">10</span>);</span>
            <span class="code-line"></span>
            <span class="code-line">    i++;</span>
            <span class="code-line">  }</span>
            <span class="code-line">}</span>
            <span class="code-line"></span>
            <span class="code-line">example1 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example1'</span>);</span>
            <span class="code-line">hot = <span class="hljs-keyword">new</span> Handsontable(example1,config);</span>
            <span class="code-line"></span>
            <span class="code-line">$(<span class="hljs-string">'#check_select_all'</span>).click(<span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{</span>
            <span class="code-line">  <span class="hljs-keyword">var</span> state = <span class="hljs-keyword">this</span>.checked;</span>
            <span class="code-line"></span>
            <span class="code-line">  $(<span class="hljs-string">'#hooksList input[type=checkbox]'</span>).each(<span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{</span>
            <span class="code-line">    <span class="hljs-keyword">if</span> (state === <span class="hljs-literal">true</span>) {</span>
            <span class="code-line">      <span class="hljs-keyword">if</span> (<span class="hljs-keyword">this</span>.id === <span class="hljs-string">'check_modifyRow'</span>) {</span>
            <span class="code-line">        <span class="hljs-keyword">return</span>; <span class="hljs-comment">//too much noise in the log</span></span>
            <span class="code-line">      }</span>
            <span class="code-line">    }</span>
            <span class="code-line">    <span class="hljs-keyword">this</span>.checked = state;</span>
            <span class="code-line">  });</span>
            <span class="code-line">});</span>
            <span class="code-line"></span>
            <span class="code-line">$(<span class="hljs-string">'#hooksList input[type=checkbox]'</span>).click(<span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{</span>
            <span class="code-line">  <span class="hljs-keyword">if</span> (!<span class="hljs-keyword">this</span>.checked) {</span>
            <span class="code-line">    <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'check_select_all'</span>).checked = <span class="hljs-literal">false</span>;</span>
            <span class="code-line">  }</span>
            <span class="code-line">});</span>

    </div>

    <div class="example-container clearfix head-gap" name="source-definition">
        ### Definition for `source` argument

        It's worth to mention that some of the hooks are triggered from the inside of the Handsontable (Core) and some from the plugins.
        In some situations it is helpful to know what triggered the callback (if it was done by Handsontable itself, triggered from external code or a user action). That's
        why in crucial hooks Handsontable delivers `source` as an argument which informs you about who've triggered the action. Thanks to
        `source` you can create additional conditions based on that information.


        `source` argument is optional. It takes following values:


        * `auto` - Action triggered by Handsontable and reason for it is releated directly with settings aplied to Handsontable.
                      For instance `afterCreateRow` will be fired with this when `minSpareRows` will be greater then 0;
        * `edit` - Action triggered by Handsontable after the data has been changed (for example after an edit or using `setData*` methods);
        * `loadData` - Action triggered by Handsontable after the `loadData` or `updateSettings({data: myData})`(with `data` property) method has been called;
        * `populateFromArray` - Action triggered by Handsontable after requesting for populating data;
        * `spliceCol` - Action triggered by Handsontable after the column data splicing has been done;
        * `spliceRow` - Action triggered by Handsontable after the row data splicing has been done;
        * `timeValidate` - Action triggered by Handsontable after the time validator has been called (for example after an edit);
        * `dateValidate` - Action triggered by Handsontable after the date validator has been called (for example after an edit);
        * `validateCells` - Action triggered by Handsontable after the validation process has been triggered;
        * `Autofill.fill` - Action triggered by the AutoFill plugin;
        * `Autofill.fill` - Action triggered by the AutoFill plugin;
        * `ContextMenu.clearColumns` - Action triggered by the ContextMenu plugin after the "Clear column" has been clicked;
        * `ContextMenu.columnLeft` - Action triggered by the ContextMenu plugin after the "Insert column on the left" has been clicked;
        * `ContextMenu.columnRight` - Action triggered by the ContextMenu plugin after the "Insert column on the right" has been clicked;
        * `ContextMenu.removeColumn` - Action triggered by the ContextMenu plugin after the "Remove column" has been clicked;
        * `ContextMenu.removeRow` - Action triggered by the ContextMenu plugin after the "Remove Row" has been clicked;
        * `ContextMenu.rowAbove` - Action triggered by the ContextMenu plugin after the "Insert row above" has been clicked;
        * `ContextMenu.rowBelow` - Action triggered by the ContextMenu plugin after the "Insert row below" has been clicked;
        * `CopyPaste.paste` - Action triggered by the CopyPaste plugin after the value has been pasted;
        * `ObserveChanges.change` - Action triggered by the ObserveChanges plugin after the changes has been detected;
        * `UndoRedo.redo` - Action triggered by the UndoRedo plugin after the change has been redone;
        * `UndoRedo.undo` - Action triggered by the UndoRedo plugin after the change has been undone;
        * `GantChart.loadData` - Action triggered by the GantChart plugin after the data has been loaded;
        * `ColumnSummary.set` - Action triggered by the ColumnSummary plugin after the calculation has been done;
        * `ColumnSummary.reset` - Action triggered by the ColumnSummary plugin after the calculation has been reset.



        List of callback that operates on `source` parameter:


        * [afterChange](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterChange)
        * [afterCreateCol](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterCreateCol)
        * [afterCreateRow<](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterCreateRow)
        * [afterSetDataAtCell](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterSetDataAtCell)
        * [afterSetDataAtRowProp](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterSetDataAtRowProp)
        * [afterValidate](https://handsontable.com/docs/6.2.2/Hooks.html#event:afterValidate)
        * [beforeChange](https://handsontable.com/docs/6.2.2/Hooks.html#event:beforeChange)
        * [beforeChangeRender](https://handsontable.com/docs/6.2.2/Hooks.html#event:beforeChangeRender)
        * [beforeCreateCol](https://handsontable.com/docs/6.2.2/Hooks.html#event:beforeCreateCol)
        * [beforeCreateRow](https://handsontable.com/docs/6.2.2/Hooks.html#event:beforeCreateRow)
        * [beforeValidate](https://handsontable.com/docs/6.2.2/Hooks.html#event:beforeValidate)


    </div>

    <div class="example-container clearfix head-gap" name="beforeKeyDown">
        ### `beforeKeyDown` use case

        The following demo uses `beforeKeyDown` callback to modify some key bindings:

        * Pressing 

            <kbd>DELETE</kbd> or 

            <kbd>BACKSPACE</kbd> on a cell deletes the cell and shifts all cells beneath it
                    in the column up resulting in the cursor (which doesn't move) having the value previously beneath it,
                    now in the current cell.

        * Pressing 

            <kbd>ENTER</kbd> in a cell (not changing the value) results in pushing all the cells in the column beneath
                    this cell down one row (including current cell) resulting in a blank cell under the cursor (which hasn't moved).


        <div data-jsfiddle="example2" class="head-gap">
            <div id="example2" class="hot handsontable htRowHeaders htColumnHeaders">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 266px; height: 142px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 65px;"><col style="width: 50px;"><col style="width: 51px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                   | Tesla                                                        | 2017                                                         | black                                                        | black                                                       
                                <div class="relative"><span class="rowHeader">2</span></div>                   | Nissan                                                       | 2018                                                         | blue                                                         | blue                                                        
                                <div class="relative"><span class="rowHeader">3</span></div>                   | Chrysler                                                     | 2019                                                         | yellow                                                       | black                                                       
                                <div class="relative"><span class="rowHeader">4</span></div>                   | Volvo                                                        | 2020                                                         | yellow                                                       | gray                                                        
                                <div class="relative"><span class="rowHeader">5</span></div>                   |                                                              |                                                              |                                                              |                                                             

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
                        <div class="wtHider" style="width: 266px;">
                            <div class="wtSpreader" style="position: relative; left: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"><col style="width: 65px;"><col style="width: 50px;"><col style="width: 51px;"><col style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div> | <div class="relative"><span class="colHeader">A</span></div> | <div class="relative"><span class="colHeader">B</span></div> | <div class="relative"><span class="colHeader">C</span></div> | <div class="relative"><span class="colHeader">D</span></div>
                                ------------------------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------


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
                        <div class="wtHider" style="height: 142px;">
                            <div class="wtSpreader" style="position: relative; top: 0px;">
                                <colgroup><col class="rowHeader" style="width: 50px;"></colgroup>
                                <div class="relative"><span class="colHeader cornerHeader">&nbsp;</span></div>
                                ------------------------------------------------------------------------------
                                <div class="relative"><span class="rowHeader">1</span></div>                  
                                <div class="relative"><span class="rowHeader">2</span></div>                  
                                <div class="relative"><span class="rowHeader">3</span></div>                  
                                <div class="relative"><span class="rowHeader">4</span></div>                  
                                <div class="relative"><span class="rowHeader">5</span></div>                  

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
                <!--<button class="jsFiddleLink" data-runfiddle="example2">-->

                <!--<i class="fa fa-jsfiddle"></i>-->

                <!--Edit-->

                <!--</button>-->

                <button class="dump" name="dump" data-dump="#example2" data-instance="hot2" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span> data = [</span>
                <span class="code-line">    [<span class="hljs-string">'Tesla'</span>, <span class="hljs-number">2017</span>, <span class="hljs-string">'black'</span>, <span class="hljs-string">'black'</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'Nissan'</span>, <span class="hljs-number">2018</span>, <span class="hljs-string">'blue'</span>, <span class="hljs-string">'blue'</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'Chrysler'</span>, <span class="hljs-number">2019</span>, <span class="hljs-string">'yellow'</span>, <span class="hljs-string">'black'</span>],</span>
                <span class="code-line">    [<span class="hljs-string">'Volvo'</span>, <span class="hljs-number">2020</span>, <span class="hljs-string">'yellow'</span>, <span class="hljs-string">'gray'</span>]</span>
                <span class="code-line">  ],</span>
                <span class="code-line">  container = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"example2"</span>),</span>
                <span class="code-line">  lastChange = <span class="hljs-literal">null</span>,</span>
                <span class="code-line">  hot;</span>
                <span class="code-line"></span>
                <span class="code-line">hot = <span class="hljs-keyword">new</span> Handsontable(container, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: data,</span>
                <span class="code-line">  <span class="hljs-attr">colHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">rowHeaders</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">minSpareRows</span>: <span class="hljs-number">1</span>,</span>
                <span class="code-line">  <span class="hljs-attr">beforeChange</span>: <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">changes, source</span>) </span>{</span>
                <span class="code-line">    lastChange = changes;</span>
                <span class="code-line">  }</span>
                <span class="code-line">});</span>
                <span class="code-line"></span>
                <span class="code-line">hot.updateSettings({</span>
                <span class="code-line">    <span class="hljs-attr">beforeKeyDown</span>: <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">e</span>) </span>{</span>
                <span class="code-line">      <span class="hljs-keyword">var</span> selection = hot.getSelected();</span>
                <span class="code-line"></span>
                <span class="code-line">      <span class="hljs-comment">// BACKSPACE or DELETE</span></span>
                <span class="code-line">      <span class="hljs-keyword">if</span> (e.keyCode === <span class="hljs-number">8</span> || e.keyCode === <span class="hljs-number">46</span>) {</span>
                <span class="code-line">        e.stopImmediatePropagation();</span>
                <span class="code-line">        <span class="hljs-comment">// remove data at cell, shift up</span></span>
                <span class="code-line">        hot.spliceCol(selection[<span class="hljs-number">1</span>], selection[<span class="hljs-number">0</span>], <span class="hljs-number">1</span>);</span>
                <span class="code-line">        e.preventDefault();</span>
                <span class="code-line">      }</span>
                <span class="code-line">      <span class="hljs-comment">// ENTER</span></span>
                <span class="code-line">      <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (e.keyCode === <span class="hljs-number">13</span>) {</span>
                <span class="code-line">        <span class="hljs-comment">// if last change affected a single cell and did not change it's values</span></span>
                <span class="code-line">        <span class="hljs-keyword">if</span> (lastChange && lastChange.length === <span class="hljs-number">1</span> && lastChange[<span class="hljs-number">0</span>][<span class="hljs-number">2</span>] == lastChange[<span class="hljs-number">0</span>][<span class="hljs-number">3</span>]) {</span>
                <span class="code-line">          e.stopImmediatePropagation();</span>
                <span class="code-line">          hot.spliceCol(selection[<span class="hljs-number">1</span>], selection[<span class="hljs-number">0</span>], <span class="hljs-number">0</span>, <span class="hljs-string">''</span>); <span class="hljs-comment">// add new cell</span></span>
                <span class="code-line">          hot.selectCell(selection[<span class="hljs-number">0</span>], selection[<span class="hljs-number">1</span>]); <span class="hljs-comment">// select new cell</span></span>
                <span class="code-line">        }</span>
                <span class="code-line">      }</span>
                <span class="code-line"></span>
                <span class="code-line">      lastChange = <span class="hljs-literal">null</span>;</span>
                <span class="code-line">    }</span>
                <span class="code-line">  }</span>
                <span class="code-line">);</span>

        </div>
    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/using-callbacks.html)
</div>
