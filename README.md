# Code Scan & Review with CodeQL

  <turbo-frame id="repo-content-turbo-frame" target="_top" data-turbo-action="advance" class="">
      <div id="repo-content-pjax-container" class="repository-content " >
    
    


    
      
<div class="clearfix container-xl px-3 px-md-4 px-lg-5 mt-4">
    
  <div >
            


        <nav aria-label="Breadcrumb" data-view-component="true" class="mb-2">
  <ol>
      <li data-view-component="true" class="breadcrumb-item "><a href="/GopiNJ/jw-community-CodeScan/security/code-scanning" data-view-component="true">Code scanning alerts</a></li>
      <li data-view-component="true" class="breadcrumb-item  breadcrumb-item-selected"><a aria-current="page" href="/GopiNJ/jw-community-CodeScan/security/code-scanning/93" data-view-component="true">#93</a></li>
  </ol>
</nav>
  </div>

<div >
  <div>
    <div class="d-flex">
      <h1 class="flex-auto text-normal mb-2 lh-condensed f1 wb-break-word">Unsafe dynamic method access</h1>
              <span class="d-flex">
              <details id="close-alert-menu" data-view-component="true" class="dropdown details-overlay details-reset mb-1">
    <summary aria-haspopup="true" role="button" data-view-component="true" class="btn-sm btn">    Dismiss alert
                    <div class="dropdown-caret"></div>
</summary>
  <details-menu data-view-component="true" class="SelectMenu right-0">    <alert-dismissal-details>
    <form data-target="alert-dismissal-details.form" data-turbo="true" data-turbo-frame="_self" action="/GopiNJ/jw-community-CodeScan/security/code-scanning/close" accept-charset="UTF-8" method="post"><input type="hidden" name="_method" value="put" autocomplete="off" /><input type="hidden" name="authenticity_token" value="pVxQY2KTEcOxiLtms6bfHDMkYOWJ9x6TSsEva1Zr5iU4-tv2zOinsBOnsKJMTYPJsM0K6SGyfiycUp7Ja1z8tg" autocomplete="off" />
      <div class="SelectMenu-modal color-fg-default">
        <header class="SelectMenu-header">
          <span class="SelectMenu-title">Select a reason to dismiss</span>
          <button class="SelectMenu-closeButton" type="button" aria-label="Close menu" data-action="click:alert-dismissal-details#reset" data-toggle-for="close-alert-menu">
            <svg aria-label="Close menu" role="img" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-x">
    <path fill-rule="evenodd" d="M3.72 3.72a.75.75 0 011.06 0L8 6.94l3.22-3.22a.75.75 0 111.06 1.06L9.06 8l3.22 3.22a.75.75 0 11-1.06 1.06L8 9.06l-3.22 3.22a.75.75 0 01-1.06-1.06L6.94 8 3.72 4.78a.75.75 0 010-1.06z"></path>
</svg>
          </button>
        </header>

        <ul class="px-3 py-2" role="radiogroup" data-target="alert-dismissal-details.radiogroup">
            <li role="radio" class="list-style-none" >
              <label>
                <div class="form-checkbox my-2">
                  <input type="radio" name="reason" value="WONT_FIX" data-action="click:alert-dismissal-details#show">
                  <div class="cursor-pointer pb-2 border-bottom">
                    Won&#39;t fix
                    <p class="note">This alert is not relevant</p>
                  </div>
                </div>
              </label>
            </li>
            <li role="radio" class="list-style-none" >
              <label>
                <div class="form-checkbox my-2">
                  <input type="radio" name="reason" value="FALSE_POSITIVE" data-action="click:alert-dismissal-details#show">
                  <div class="cursor-pointer pb-2 border-bottom">
                    False positive
                    <p class="note">This alert is not valid</p>
                  </div>
                </div>
              </label>
            </li>
            <li role="radio" class="list-style-none" >
              <label>
                <div class="form-checkbox my-2">
                  <input type="radio" name="reason" value="USED_IN_TESTS" data-action="click:alert-dismissal-details#show">
                  <div class="cursor-pointer ">
                    Used in tests
                    <p class="note">This alert is not in production code</p>
                  </div>
                </div>
              </label>
            </li>
        </ul>

        <div data-target="alert-dismissal-details.footer" data-view-component="true">
          <div class="SelectMenu-divider border-0 border-top">Dismissal comment</div>
          <footer class="SelectMenu-footer">

            <textarea name="resolution_note" style="min-height:3em;max-height:10em;max-width:100%;min-width:100%" class="form-control input-block mb-2" label="dismissal-comment" aria-label="dismissal comment" maxlength=280 placeholder="Add a comment"></textarea>
            <div data-view-component="true" class="d-flex flex-row flex-justify-end">
                <button data-toggle-for="close-alert-menu" data-action="click:alert-dismissal-details#reset" type="button" data-view-component="true" class="btn">    Cancel
</button>
                <button type="submit" data-view-component="true" class="btn-primary btn ml-2">    Dismiss alert
</button></div>
              <input type="hidden" name="number[]" value="93">


            <div class="js-scanning-bulk-action-items" hidden>
            </div>
          </footer>
</div>      </div>
</form>    </alert-dismissal-details>
</details-menu>
</details>        </span>

    </div>
  </div>
  <div class="mb-2"><span class="mr-1 d-inline-block"><span title="Status: Open" data-view-component="true" class="State State--open"><svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-shield">
    <path fill-rule="evenodd" d="M7.467.133a1.75 1.75 0 011.066 0l5.25 1.68A1.75 1.75 0 0115 3.48V7c0 1.566-.32 3.182-1.303 4.682-.983 1.498-2.585 2.813-5.032 3.855a1.7 1.7 0 01-1.33 0c-2.447-1.042-4.049-2.357-5.032-3.855C1.32 10.182 1 8.566 1 7V3.48a1.75 1.75 0 011.217-1.667l5.25-1.68zm.61 1.429a.25.25 0 00-.153 0l-5.25 1.68a.25.25 0 00-.174.238V7c0 1.358.275 2.666 1.057 3.86.784 1.194 2.121 2.34 4.366 3.297a.2.2 0 00.154 0c2.245-.956 3.582-2.104 4.366-3.298C13.225 9.666 13.5 8.36 13.5 7V3.48a.25.25 0 00-.174-.237l-5.25-1.68zM9 10.5a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.75a.75.75 0 10-1.5 0v3a.75.75 0 001.5 0v-3z"></path>
</svg> Open</span></span>        <span class="color-fg-muted">
            in <span class="branch-name">7.0-SNAPSHOT</span>
          <relative-time datetime="2022-08-22T10:08:47Z" class="no-wrap">Aug 22, 2022</relative-time>
        </span>

</div>
</div>

<div data-view-component="true" class="gutter-condensed gutter-lg d-flex">

  <div data-view-component="true" class="flex-shrink-0 col-9">
            <div class="d-flex">
        </div>


        <div class="file js-file js-details-container Details Details--on open mt-2"  data-details-container-group="file">
    <div class="d-flex file-header js-file-header">
      <div class="file-info d-flex flex-auto min-width-0">
        <div class="flex-self-center lh-default py-1">
            <a href="/GopiNJ/jw-community-CodeScan/blob/4949fc0052e9da5b6c903ed4f0678ed6ef4fb9db/wflow-consoleweb/src/main/webapp/js/ace/worker-xquery.js#L206-L206" class="Link--primary">wflow-consoleweb/src/main/webapp/js/ace/<b>worker-xquery.js</b>:206</a>
          <clipboard-copy data-copy-feedback="Copied!" aria-label="Copy" value="wflow-consoleweb/src/main/webapp/js/ace/worker-xquery.js:206" data-view-component="true" class="Link--onHover color-fg-muted mx-1">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
    <svg style="display: none;" aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check color-fg-success">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
</clipboard-copy>
        </div>
      </div>

      
    </div>
        
<div class="d-flex flex-column flex-items-center text-center pt-4 pb-2 px-2" >
  <h4>Preview unavailable</h4>
  <p class="color-fg-muted">This snippet is too large to be displayed. This may be because it is minified.</p>
</div>

  <div class="border-top">
    <div class="js-skip-tagsearch">
  <div class="d-inline-block border px-3 py-2 text-small color-border-danger-emphasis" style="border-width: 0 0 0 3px !important;">
    <div class="text-mono code-scanning-font-size-inherit cs-message">
      Invocation of method derived from <details class="d-inline details-overlay mb-0" data-deferred-details-content-url="/GopiNJ/jw-community-CodeScan/security/code-scanning/related-location?commit_oid=4949fc0052e9da5b6c903ed4f0678ed6ef4fb9db&amp;end_column=30&amp;end_line=197&amp;file_path=wflow-consoleweb%2Fsrc%2Fmain%2Fwebapp%2Fjs%2Face%2Fworker-xquery.js&amp;start_column=29&amp;start_line=197">    <summary data-view-component="true" class="btn-link">    user-controlled value</summary>  <div class="dropdown-menu dropdown-menu-s mt-2 width-full" style="top: auto">    <include-fragment class="m-2">      <div class="text-center" data-show-on-error="" hidden="">        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-alert">    <path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path></svg>        Error loading related location      </div>      <svg data-hide-on-error="true" style="box-sizing: content-box; color: var(--color-icon-primary);" width="32" height="32" viewBox="0 0 16 16" fill="none" data-view-component="true" class="anim-rotate">  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke"></circle>  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path></svg>    </include-fragment>  </div></details> may lead to remote code execution.
    </div>

      <div class="mt-2">
          <span class="text-bold color-fg-muted d-inline-block mr-3">
            CodeQL
          </span>
          <span class="d-inline-block">
            <details class="details-reset details-overlay details-overlay-dark js-dropdown-details my-2 mr-2" data-deferred-details-content-url="/GopiNJ/jw-community-CodeScan/security/code-scanning/93/code-paths?ref=refs%2Fheads%2F7.0-SNAPSHOT">
              <summary class="btn-link text-bold" aria-haspopup="dialog">Show paths</summary>
              <details-dialog class="Box Box--overlay Box-overlay--wide d-flex flex-column anim-fade-in fast overflow-auto" style="width: 800px">
                <include-fragment class="my-6">
                  <div class="text-center" data-show-on-error hidden>
                    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-alert">
    <path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path>
</svg>
                    Error loading code paths
                  </div>
                  <svg data-hide-on-error="true" style="box-sizing: content-box; color: var(--color-icon-primary);" width="32" height="32" viewBox="0 0 16 16" fill="none" data-view-component="true" class="anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" />
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke" />
</svg>
                </include-fragment>
              </details-dialog>
            </details>
          </span>
      </div>
  </div>
</div>

  </div>

</div>


        <div class="Box Box--condensed mt-3 Details js-details-container">
          <div class="Box-header p-3 d-md-flex">
              <div class="mr-md-5" >
                <h3 class="Box-title mb-1">Tool</h3>
                <div class="f6">CodeQL</div>
              </div>
            <div class="mr-md-5 mt-3 mt-md-0">
              <h3 class="Box-title mb-1">Rule ID</h3>
              <div class="text-mono f6">js/unsafe-dynamic-method-access</div>
            </div>
              <div class="mr-5 mt-3 mt-md-0" >
                <h3 class="Box-title mb-1">Query</h3>
                <a class="Link--primary d-block f6" href="https://github.com/github/codeql/blob/f30b735443ec9f7528b51628a16510dce4ea0a56/javascript/ql/src/Security/CWE-094/UnsafeDynamicMethodAccess.ql" target="_blank" rel="noopener noreferrer">View source</a>
              </div>
          </div>

            <div class="Box-body markdown-body comment-body position-relative border-bottom-0 Details-content--shown" >
              <p>Calling a user-controlled method on certain objects can lead to invocation of unsafe functions, such as <code>eval</code> or the <code>Function</code> constructor. In particular, the global object contains the <code>eval</code> function, and any function object contains the <code>Function</code> constructor in its <code>constructor</code> property.</p>
            </div>
            <div class="Box-body markdown-body comment-body position-relative Details-content--hidden" >
              <p>Calling a user-controlled method on certain objects can lead to invocation of unsafe functions, such as <code>eval</code> or the <code>Function</code> constructor. In particular, the global object contains the <code>eval</code> function, and any function object contains the <code>Function</code> constructor in its <code>constructor</code> property.</p>
<h2>Recommendation</h2>
<p>Avoid invoking user-controlled methods on the global object or on any function object. Whitelist the permitted method names or change the type of object the methods are stored on.</p>
<h2>Example</h2>
<p>In the following example, a message from the document's parent frame can invoke the <code>play</code> or <code>pause</code> method. However, it can also invoke <code>eval</code>. A malicious website could embed the page in an iframe and execute arbitrary code by sending a message with the name <code>eval</code>.</p>
<div class="highlight highlight-source-js"><pre><span class="pl-c">// API methods</span>
<span class="pl-k">function</span> <span class="pl-en">play</span><span class="pl-kos">(</span><span class="pl-s1">data</span><span class="pl-kos">)</span> <span class="pl-kos">{</span>
  <span class="pl-c">// ...</span>
<span class="pl-kos">}</span>
<span class="pl-k">function</span> <span class="pl-en">pause</span><span class="pl-kos">(</span><span class="pl-s1">data</span><span class="pl-kos">)</span> <span class="pl-kos">{</span>
  <span class="pl-c">// ...</span>
<span class="pl-kos">}</span>

<span class="pl-smi">window</span><span class="pl-kos">.</span><span class="pl-en">addEventListener</span><span class="pl-kos">(</span><span class="pl-s">"message"</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ev</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
    <span class="pl-k">let</span> <span class="pl-s1">message</span> <span class="pl-c1">=</span> <span class="pl-c1">JSON</span><span class="pl-kos">.</span><span class="pl-en">parse</span><span class="pl-kos">(</span><span class="pl-s1">ev</span><span class="pl-kos">.</span><span class="pl-c1">data</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

    <span class="pl-c">// Let the parent frame call the 'play' or 'pause' function </span>
    <span class="pl-smi">window</span><span class="pl-kos">[</span><span class="pl-s1">message</span><span class="pl-kos">.</span><span class="pl-c1">name</span><span class="pl-kos">]</span><span class="pl-kos">(</span><span class="pl-s1">message</span><span class="pl-kos">.</span><span class="pl-c1">payload</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre></div>
<p>Instead of storing the API methods in the global scope, put them in an API object or Map. It is also good practice to prevent invocation of inherited methods like <code>toString</code> and <code>valueOf</code>.</p>
<div class="highlight highlight-source-js"><pre><span class="pl-c">// API methods</span>
<span class="pl-k">let</span> <span class="pl-s1">api</span> <span class="pl-c1">=</span> <span class="pl-kos">{</span>
  <span class="pl-en">play</span>: <span class="pl-k">function</span><span class="pl-kos">(</span><span class="pl-s1">data</span><span class="pl-kos">)</span> <span class="pl-kos">{</span>
    <span class="pl-c">// ...</span>
  <span class="pl-kos">}</span><span class="pl-kos">,</span>
  <span class="pl-en">pause</span>: <span class="pl-k">function</span><span class="pl-kos">(</span><span class="pl-s1">data</span><span class="pl-kos">)</span> <span class="pl-kos">{</span>
    <span class="pl-c">// ...</span>
  <span class="pl-kos">}</span>
<span class="pl-kos">}</span><span class="pl-kos">;</span>

<span class="pl-smi">window</span><span class="pl-kos">.</span><span class="pl-en">addEventListener</span><span class="pl-kos">(</span><span class="pl-s">"message"</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ev</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
    <span class="pl-k">let</span> <span class="pl-s1">message</span> <span class="pl-c1">=</span> <span class="pl-c1">JSON</span><span class="pl-kos">.</span><span class="pl-en">parse</span><span class="pl-kos">(</span><span class="pl-s1">ev</span><span class="pl-kos">.</span><span class="pl-c1">data</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

    <span class="pl-c">// Let the parent frame call the 'play' or 'pause' function</span>
    <span class="pl-k">if</span> <span class="pl-kos">(</span><span class="pl-c1">!</span><span class="pl-s1">api</span><span class="pl-kos">.</span><span class="pl-en">hasOwnProperty</span><span class="pl-kos">(</span><span class="pl-s1">message</span><span class="pl-kos">.</span><span class="pl-c1">name</span><span class="pl-kos">)</span><span class="pl-kos">)</span> <span class="pl-kos">{</span>
      <span class="pl-k">return</span><span class="pl-kos">;</span>
    <span class="pl-kos">}</span>
    <span class="pl-s1">api</span><span class="pl-kos">[</span><span class="pl-s1">message</span><span class="pl-kos">.</span><span class="pl-c1">name</span><span class="pl-kos">]</span><span class="pl-kos">(</span><span class="pl-s1">message</span><span class="pl-kos">.</span><span class="pl-c1">payload</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre></div>
<h2>References</h2>
<ul>
<li>OWASP: <a href="https://www.owasp.org/index.php/Code_Injection" rel="nofollow">Code Injection</a>.</li>
<li>MDN: <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects#Function_properties" rel="nofollow">Global functions</a>.</li>
<li>MDN: <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function" rel="nofollow">Function constructor</a>.</li>
<li>Common Weakness Enumeration: <a href="https://cwe.mitre.org/data/definitions/94.html" rel="nofollow">CWE-94</a>.</li>
</ul>
            </div>
