<div class="static-content">
    <div class="index-list">
        * [Overview](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#overview)
        * [Loading prepared language files](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#loading-language-files)
        * [Demo](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#demo)
        * [Internationalization for features](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#internalization-for-features)
        * [Available languages](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#available-languages)
        * [Hierarchy of all main files connected with internationalization](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#files-hierarchy)
        * [Creating custom languages](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#custom-languages)
        * [Using custom keys in the translation](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#custom-keys)
        * [Static Handsontable methods and properties](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#static-properties)
    </div>

    <div class="example-container clearfix">
        ### Overview

        Internationalization allows Handsontable to easily change the text of the UI for the purpose of translating it to specific languages.
        We provide the developer with predefined languages (which can be applied by loading the language set and changing just one setting) and an ability to use their own language sets,
        created using templates of existing language files.

    </div>

    <div data-alert="" class="alert-box info">**We are looking for contributors who would like to help us in adding new translations to Handsontable. [Learn more](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#custom-languages).**</div>

    <div class="example-container clearfix">
        ### Loading the prepared language files

        To properly use the internationalization feature, you'll need to load the language sets. It's important,
        that they're included after the Handsontable files. You can do it by getting the necessary files (they were created using [UMD standard](https://github.com/umdjs/umd)):


        1.  from `/dist/languages` folder inside your HTML file


                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"text/javascript"</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"dist/handsontable.full.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span>
                <span class="hljs-tag"><<span class="hljs-name">script</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"text/javascript"</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"dist/languages/all.js"</span>></span><span class="undefined"></span><span class="hljs-tag"></<span class="hljs-name">script</span>></span>


            Note: Please keep in mind, that you can also use the minified versions of the files from the `/dist/languages` folder.

        2.  from the `/languages` folder located in the root of the project, to be used by module systems;
            the example below shows how to use it with ECMAScript 6 (you will need a bundler or TypeScript).

            Usage for Handsontable Pro Edition:



                <span class="hljs-keyword">import</span> Handsontable <span class="hljs-keyword">from</span> <span class="hljs-string">'handsontable-pro'</span>;
                <span class="hljs-keyword">import</span> <span class="hljs-string">'handsontable-pro/languages/pl-PL'</span>;


            Usage for Handsontable Community Edition:



                <span class="hljs-keyword">import</span> Handsontable <span class="hljs-keyword">from</span> <span class="hljs-string">'handsontable'</span>;
                <span class="hljs-keyword">import</span> <span class="hljs-string">'handsontable/languages/pl-PL'</span>;



        Languages included this way are ready to use immediately after loading the file. More about other language-specific
        files and language registration for Handsontable can be found in [this section](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#files-hierarchy).

    </div>

    <div class="example-container clearfix">
        ### Demo

        Please right click on a cell to see the translated context menu. Language files were loaded after loading Handsontable.

        <div data-jsfiddle="example1">
            <div id="example1" class="hot handsontable">
                <div class="ht_master handsontable" style="position: relative; overflow: visible;">
                    <div class="wtHolder" style="position: relative; overflow: visible;">
                        <div class="wtHider" style="width: 457px; height: 116px;">
                            <div class="wtSpreader" style="position: relative; top: 0px; left: 0px;">
                                <colgroup><col style="width: 93px;"><col style="width: 72px;"><col style="width: 81px;"><col style="width: 73px;"><col style="width: 88px;"><col style="width: 50px;"></colgroup>

                                ------------ | --------- | --------- | --------- | ---------- | ---
                                Lorem        | ipsum     | dolor     | sit       | 12/1/2015  | 23 
                                adipiscing   | elit      | Ut        | imperdiet | 5/12/2015  | 6  
                                Pellentesque | vulputate | leo       | semper    | 10/23/2015 | 26 
                                diam         | et        | malesuada | libero    | 12/1/2014  | 98 
                                orci         | et        | dignissim | hendrerit | 12/1/2016  | 8.5

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

                <div class="ht_clone_top handsontable" style="position: absolute; top: 0px; left: 0px; overflow: hidden;">
                    <div class="wtHolder" style="position: relative;">
                        <div class="wtHider">
                            <div class="wtSpreader" style="position: relative;">
                                <colgroup></colgroup>



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

                <button class="dump" name="dump" data-dump="#example1" data-instance="hot" title="Print current data source to console">
                          <i class="fa fa-terminal"></i>
                          Dump data to console
                        </button>
            </div>


                <span class="code-line"><span class="hljs-keyword">var</span> example1 = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'example1'</span>);</span>
                <span class="code-line"></span>
                <span class="code-line"><span class="hljs-keyword">var</span> hot = <span class="hljs-keyword">new</span> Handsontable(example1, {</span>
                <span class="code-line">  <span class="hljs-attr">data</span>: dataObj,</span>
                <span class="code-line">  <span class="hljs-attr">contextMenu</span>: <span class="hljs-literal">true</span>,</span>
                <span class="code-line">  <span class="hljs-attr">language</span>: <span class="hljs-string">'pl-PL'</span></span>
                <span class="code-line">});</span>

        </div>
    </div>

    <div class="example-container clearfix">
        ### Internationalization for features

        Below you'll find a list of features which can be translated with the internationalization feature.

        * Dropdown menu
        * Filtering
        * Hiding columns
        * Hiding rows
        * Nesting rows
        * Comments
        * Context menu
        * Custom borders
        * Freezing
        * Merge cells
        * Read-only
    </div>

    <div class="example-container clearfix">
        ### List of available languages

        By default, Handsontable uses the **English - United States** language-country set (`en-US` code) for creating the text of UI elements.
        However, it can be used like every extra, "non-standard" language file, thus the `en-US.js` file can be found in `/dist/languages`, `/languages`
        and `/src/languages` folders. Currently, we also distribute extra language-country files:


        * `de-DE.js` for **German - Germany** (`de-DE` code).

        * `de-CH.js` for **German - Switzerland** (`de-CH` code).

        * `es-MX.js` for **Spanish - Mexico** (`es-MX` code).

        * `fr-FR.js` for **French - France** (`fr-FR` code).

        * `it-IT.js` for **Italian - Italy** (`it-IT` code).

        * `ja-JP.js` for **Japanese - Japan** (`ja-JP` code).

        * `ko-KR.js` for **Korean - Korea** (`ko-KR` code).

        * `lv-LV.js` for **Latvian - Latvia** (`lv-LV` code).

        * `nb-NO.js` for **Norwegian (Bokmål) - Norway** (`nb-NO` code).

        * `nl-NL.js` for **Dutch - Netherlands** (`nl-NL` code).

        * `pl-PL.js` for **Polish - Poland** (`pl-PL` code).

        * `pt-BR.js` for **Portuguese - Brazil** (`pt-BR` code).

        * `ru-RU.js` for **Russian - Russia** (`ru-RU` code).

        * `zh-CN.js` for **Chinese - China** (`zh-CN` code).

        * `zh-TW.js` for **Chinese - Taiwan** (`zh-TW` code).



    </div>

    <div class="example-container clearfix">
        ### Hierarchy of all the main files connected with internationalization

        Information within this paragraph may be useful mainly for people who would like to add new or edit already existing language.
        The simple way of using the prepared languages is [described here](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#loading-language-files).
        All the changes we're mentioning below should be made to [Handsontable CE](https://github.com/handsontable/handsontable).


        In `Handsontable CE`, we currently have 3 folders with files that can be treated as languages files:

        * `/dist/languages`\*
        * `/languages`\*
        * `/src/i18n/languages`

        Files from the two first folders are built as [UMD](https://github.com/umdjs/umd) modules by [webpack](https://webpack.js.org/)
        (can be prepared by using the following npm scripts: `build:languages` and `build:languages.min`).
        The last, `/src` directory contains modules created using the `ES2015` standard.


        To use the language dictionaries, you'll have to register the language sets.
        Registration is a process of loading the dictionaries globally for Handsontable using the `Handsontable.languages.registerLanguageDictionary` method.


        The general purpose of these directories is summarized in the table below:

        Name                  | Files in `/dist/languages` and `/languages` folders              | Files in `/src/i18n/languages` folder                           
        --------------------- | ---------------------------------------------------------------- | ----------------------------------------------------------------
        Usage                 | Included as separate file                                        | Used inside Handsontable as a part of library (default language)
        File source           | Created by webpack during the build process, transpiled by Babel | Created manually, **can be** transpiled by Babel                
        Language registration | Applied in the process of building with webpack                  | **Not** registered automatically                                
        Modifications         | Should **not** be edited, as they're created automatically       | Created and edited manually                                     

        Please keep in mind that the files inside the `/dist/languages` folder are a copy of files located inside `/languages`, with two differences.
        The first folder contains additional, minified versions of the files.
        Also, it doesn't contain the `index.js` file (`/languages` folder contains it for the purpose of easier loading of all the languages).


        Both of these folders contain the `all.js` file, containing all of the language dictionaries.

    </div>

    <div class="example-container clearfix">
        ### Creating custom languages

        You can create custom language sets for your implementations, or share them, as they're easily appliable to any Handsontable implementation.

        #### Language file

        It's really important for us, that the community is a important part of the growth of our library. We encourage you to create and share your translations!

        Additional languages files should be placed in the `src/i18n/languages` folder
        of the [Handsontable CE](https://github.com/handsontable/handsontable) repository with name corresponding to the chosen language code
        (described below, for example: `es-VE.js`). You can incorporate your translations to the Handsontable library
        by sending us a [pull request](https://handsontable.com/docs/tutorial-contributing.html). It's important, that your changes are not made to the `/languages` and
        `/dist/languages` directories! Our release master will generate files which will be placed there in the building process.
        After that, you will be able to use the languages in `Handsontable Pro`

        You can see a full template of a sample language
        at the bottom of this paragraph. We're basing it on
        our [default language pack](https://github.com/handsontable/handsontable/tree/master/src/i18n/languages/en-US.js). Parts of the file creation process are described below.


        1.  The file should start with a comment containing the translation **authors** (separated by commas, for example: _Authors: Chris Wick, John Kyle_),
            **"last updated" date** (in format: _mmm dd, yyyy_, for example: _Last updated: Jan 01, 2017_) and a **description.**


                <span class="hljs-comment">/**
                \* @preserve
                \* Authors: Chris Wick, John Kyle
                \* Last updated: Nov 15, 2017
                \*
                \* Description: Definition file for Spanish - Venezuela language-country.
                \*/</span>


        2.  After that, you'll need to import the dictionary keys to be used in the translation.


                <span class="hljs-keyword">import</span> * <span class="hljs-keyword">as</span> C <span class="hljs-keyword">from</span> <span class="hljs-string">'../constants'</span>;


        3.  The language dictionary object should contain a `languageCode` key (in format: two lowercase letters, hyphen, two uppercase letters,
            for example: _languageCode: 'es-PY'_) which will determine the language code to be used in the language property
            in the `Handsontable` settings and dictionaries keys with their corresponding translations.



                <span class="hljs-keyword">const</span> dictionary = {
                  <span class="hljs-attr">languageCode</span>: <span class="hljs-string">'es-VE'</span>,
                  [C.CONTEXTMENU_ITEMS_ROW_ABOVE]: <span class="hljs-string">'Insertar fila arriba'</span>,
                  ...
                }


        4.  Lastly, place a default export of the created dictionary.


                <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> dictionary;


        5.  A simple, sample language dictionary can look like the snippet below. The `/languages` and `/dist/languages` folders will be generated by the build process.
            Files from those localizations can be included as shown in [this section](https://handsontable.com/docs/6.2.2/tutorial-internationalization.html#loading-language-files).
            After loading them, you will be able to use the language. You can do it by changing the language setting of `Handsontable` to `es-VE`.



                <span class="hljs-comment">/**
                \* @preserve
                \* Authors: Chris Wick, John Kyle
                \* Last updated: Nov 15, 2017
                \*
                \* Description: Definition file for Spanish - Venezuela language-country.
                \*/</span>
                <span class="hljs-keyword">import</span> * <span class="hljs-keyword">as</span> C <span class="hljs-keyword">from</span> <span class="hljs-string">'../constants'</span>;

                <span class="hljs-keyword">const</span> dictionary = {
                  <span class="hljs-attr">languageCode</span>: <span class="hljs-string">'es-VE'</span>,
                  [C.CONTEXTMENU_ITEMS_ROW_ABOVE]: <span class="hljs-string">'Insertar fila arriba'</span>,
                };

                <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> dictionary;


        6.  Import already created file inside the `src/i18n/languages/index.js` file and export it like it's shown in the snippet below (keys in a alphabetical order).


                import deCH from './de-CH';
                 import deDE from './de-DE';
                 import enUS from './en-US';
                <span class="hljs-addition">+import esVE from './es-VE';</span>
                 import plPL from './pl-PL';

                 export {
                   deCH,
                   deDE,
                   enUS,
                <span class="hljs-addition">+  esVE,</span>
                   plPL
                 };


        7.  Voilà! You've created a language which can be used just by you or shared with others.
            We wait for at least 5 positive feedback from users to accept a created [pull request](https://handsontable.com/docs/tutorial-contributing.html).


        #### Local language

        You can register a language dictionary which is not a part of the `Handsontable` package. To do so, use the static
        `Handsontable.languages.registerLanguageDictionary` method and the static constant `Handsontable.languages.dictionaryKeys`
        which are described briefly in the next section.



            <span class="hljs-keyword">const</span> C = Handsontable.languages.dictionaryKeys;

            Handsontable.languages.registerLanguageDictionary({
              <span class="hljs-attr">languageCode</span>: <span class="hljs-string">'morse'</span>,
              <span class="hljs-comment">// Your translation in the Morse code</span>
              [C.FILTERS_BUTTONS_OK]: <span class="hljs-string">'--- -•-'</span>
            });

    </div>

    <div class="example-container clearfix">
        ### Using custom keys in the translation

        You can register a language dictionary containing custom keys. These entries can be used like any other keys, so you're not
        limited to using our pre-defined constants (the ones that are present within `src/i18n/constants.js` file and may
        be accessed by `Handsontable.languages.dictionaryKeys` alias).



            <span class="hljs-keyword">const</span> enUSDictionary = Handsontable.languages.getLanguageDictionary(<span class="hljs-string">'en-US'</span>);

            enUSDictionary.customKey = <span class="hljs-string">'Hello world'</span>;

            Handsontable.languages.registerLanguageDictionary(enUSDictionary); <span class="hljs-comment">// re-registration</span>
            Handsontable.languages.getTranslatedPhrase(<span class="hljs-string">'en-US'</span>, <span class="hljs-string">'customKey'</span>); <span class="hljs-comment">// 'Hello world'</span>



    </div>

    <div class="example-container clearfix">
        ### Static Handsontable methods and properties

        Handsontable has a few static methods and properties connected with languages. They are stored in the `languages` key of the global `Handsontable` variable.
        All of them are described below.

        #### Handsontable.languages.getLanguageDictionary(languageCode: `String`)

        Get language dictionary for specific language code.

        Returns: `Object`

        #### Handsontable.languages.getLanguagesDictionaries()

        Get the registered language dictionaries.

        Returns: `Array`

        #### Handsontable.languages.getTranslatedPhrase(languageCode: `String`, dictionaryKey: `String`, extraArguments: `Mixed`)

        Get the phrase for specified dictionary key.

        Returns: `Object`

        #### Handsontable.languages.registerLanguageDictionary(languageCodeOrDictionary: `Mixed`, dictionary: `Object`)

        Register a language dictionary for a specific language code. After that, it will be possible to use it.

        Returns: `Object`

        #### Handsontable.languages.dictionaryKeys

        Dictionary constants.

        Contains: `Object`
    </div>

    [      Help us improve this page
    ](https://github.com/handsontable/docs/edit/6.2.2/tutorials/internationalization.html)
</div>
