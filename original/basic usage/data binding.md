    <div class="static-content">
  <div class="example-container clearfix">
    <div class="index-list">
      <ul>
        <li><a href="https://handsontable.com/docs/6.2.2/tutorial-data-binding.html#page-reference">Understand binding as reference</a></li>
        <li><a href="https://handsontable.com/docs/6.2.2/tutorial-data-binding.html#page-copy">Working with copy of data</a></li>
      </ul>
    </div>

    <div class="example-container clearfix" name="reference">
      <h3 id="page-reference">Understand binding as a reference</h3>
      <p>
        Handsontable binds to your data source (list of arrays or list of objects) by reference. Therefore, all the data entered
        in the grid will alter the original data source. In complex applications, you may want to change
        the data source from outside Handsontable. A change being made will not be presented
        on the screen unless you refresh the grid on the screen using the <a href="https://handsontable.com/docs/6.2.2/Core.html#render">render</a> method.
      </p>

      <div data-jsfiddle="example1">
        <div id="example1" class="hot handsontable"><div class="ht_master handsontable" style="position: relative; overflow: visible;"><div class="wtHolder" style="position: relative; overflow: visible;"><div class="wtHider" style="width: 360px; height: 139px;"><div class="wtSpreader" style="position: relative; top: 0px; left: 0px;"><table class="htCore"><colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup><thead></thead><tbody><tr><td class=""></td><td class="">Ford</td><td class="">Nissan</td><td class="">Toyota</td><td class="">Honda</td><td class="">Mazda</td><td class="">Ford</td></tr><tr><td class="">2017</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2018</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2019</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2020</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2021</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr></tbody></table><div class="htBorders"><div style="position: absolute; top: 0px; left: 0px;"><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div></div><div style="position: absolute; top: 0px; left: 0px;"><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div></div></div></div></div></div></div><div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div><div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div><div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div></div>
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
        <script data-jsfiddle="example1">
          var
            data1 = [
              ['', 'Tesla', 'Nissan', 'Toyota', 'Honda', 'Mazda', 'Ford'],
              ['2017', 10, 11, 12, 13, 15, 16],
              ['2018', 10, 11, 12, 13, 15, 16],
              ['2019', 10, 11, 12, 13, 15, 16],
              ['2020', 10, 11, 12, 13, 15, 16],
              ['2021', 10, 11, 12, 13, 15, 16]
            ],
            container1 = document.getElementById('example1'),
            settings1 = {
              data: data1
            },
            hot1;

          hot1 = new Handsontable(container1, settings1);
          data1[0][1] = 'Ford'; // change "Tesla" to "Ford" programmatically
          hot1.render();</script><pre class="javascript"><code class="hljs"><span class="code-line"><span class="hljs-keyword">var</span></span>
<span class="code-line">  data1 = [</span>
<span class="code-line">    [<span class="hljs-string">''</span>, <span class="hljs-string">'Tesla'</span>, <span class="hljs-string">'Nissan'</span>, <span class="hljs-string">'Toyota'</span>, <span class="hljs-string">'Honda'</span>, <span class="hljs-string">'Mazda'</span>, <span class="hljs-string">'Ford'</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2017'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2018'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2019'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2020'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2021'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>]</span>
<span class="code-line">  ],</span>
<span class="code-line">  container1 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example1'</span>),</span>
<span class="code-line">  settings1 = {</span>
<span class="code-line">    <span class="hljs-attr">data</span>: data1</span>
<span class="code-line">  },</span>
<span class="code-line">  hot1;</span>
<span class="code-line"></span>
<span class="code-line">hot1 = <span class="hljs-keyword">new</span> Handsontable(container1, settings1);</span>
<span class="code-line">data1[<span class="hljs-number">0</span>][<span class="hljs-number">1</span>] = <span class="hljs-string">'Ford'</span>; <span class="hljs-comment">// change "Tesla" to "Ford" programmatically</span></span>
<span class="code-line">hot1.render();</span>
</code></pre>
      </div>
    </div>

    <div class="example-container clearfix head-gap" name="rendering">
      <h3 id="page-copy">Working with copy of data</h3>
      <p>
        In case you want to keep a separate working copy of data for Handsontable, it is suggested
        to clone the data source before loading it into Handsontable. This can be done with
        <code>JSON.parse(JSON.stringify(data))</code> or another deep-cloning function.
      </p>
      <div data-jsfiddle="example2">
        <div id="example2" class="hot handsontable"><div class="ht_master handsontable" style="position: relative; overflow: visible;"><div class="wtHolder" style="position: relative; overflow: visible;"><div class="wtHider" style="width: 360px; height: 139px;"><div class="wtSpreader" style="position: relative; top: 0px; left: 0px;"><table class="htCore"><colgroup><col style="width: 50px;"><col style="width: 50px;"><col style="width: 53px;"><col style="width: 53px;"><col style="width: 52px;"><col style="width: 52px;"><col style="width: 50px;"></colgroup><thead></thead><tbody><tr><td class=""></td><td class="">Tesla</td><td class="">Nissan</td><td class="">Toyota</td><td class="">Honda</td><td class="">Mazda</td><td class="">Ford</td></tr><tr><td class="">2017</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2018</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2019</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2020</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr><tr><td class="">2021</td><td class="">10</td><td class="">11</td><td class="">12</td><td class="">13</td><td class="">15</td><td class="">16</td></tr></tbody></table><div class="htBorders"><div style="position: absolute; top: 0px; left: 0px;"><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current" style="background-color: rgb(75, 137, 255); height: 2px; width: 2px; display: none;"></div><div class="wtBorder current corner" style="background-color: rgb(75, 137, 255); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div></div><div style="position: absolute; top: 0px; left: 0px;"><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill" style="background-color: rgb(255, 0, 0); height: 1px; width: 1px; display: none;"></div><div class="wtBorder fill corner" style="background-color: rgb(255, 0, 0); height: 6px; width: 6px; border: 1px solid rgb(255, 255, 255); display: none;"></div></div></div></div></div></div></div><div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div><div class="ht_clone_bottom handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div><div class="ht_clone_left handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;"><div class="wtHolder" style="position: relative;"><div class="wtHider"><div class="wtSpreader" style="position: relative;"><table class="htCore"><colgroup></colgroup><thead></thead><tbody></tbody></table></div></div></div></div></div>
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
        <script data-jsfiddle="example2">
          var
            data2 = [
              ['', 'Tesla', 'Nissan', 'Toyota', 'Honda', 'Mazda', 'Ford'],
              ['2017', 10, 11, 12, 13, 15, 16],
              ['2018', 10, 11, 12, 13, 15, 16],
              ['2019', 10, 11, 12, 13, 15, 16],
              ['2020', 10, 11, 12, 13, 15, 16],
              ['2021', 10, 11, 12, 13, 15, 16]
            ],
            container2 = document.getElementById('example2'),
            hot2;

          hot2 = new Handsontable(container2, {
            data: JSON.parse(JSON.stringify(data2))
          });</script><pre class="javascript"><code class="hljs"><span class="code-line"><span class="hljs-keyword">var</span></span>
<span class="code-line">  data2 = [</span>
<span class="code-line">    [<span class="hljs-string">''</span>, <span class="hljs-string">'Tesla'</span>, <span class="hljs-string">'Nissan'</span>, <span class="hljs-string">'Toyota'</span>, <span class="hljs-string">'Honda'</span>, <span class="hljs-string">'Mazda'</span>, <span class="hljs-string">'Ford'</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2017'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2018'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2019'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2020'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>],</span>
<span class="code-line">    [<span class="hljs-string">'2021'</span>, <span class="hljs-number">10</span>, <span class="hljs-number">11</span>, <span class="hljs-number">12</span>, <span class="hljs-number">13</span>, <span class="hljs-number">15</span>, <span class="hljs-number">16</span>]</span>
<span class="code-line">  ],</span>
<span class="code-line">  container2 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example2'</span>),</span>
<span class="code-line">  hot2;</span>
<span class="code-line"></span>
<span class="code-line">hot2 = <span class="hljs-keyword">new</span> Handsontable(container2, {</span>
<span class="code-line">  <span class="hljs-attr">data</span>: <span class="hljs-built_in">JSON</span>.parse(<span class="hljs-built_in">JSON</span>.stringify(data2))</span>
<span class="code-line">});</span>
</code></pre>
      </div>
    </div>
  </div>
  <p class="gap-top-xsmall">
    <a href="https://github.com/handsontable/docs/edit/6.2.2/tutorials/data-binding.html" class="edit-doc" target="_blank">
      Help us improve this page
    </a>
  </p>
</div>
  
