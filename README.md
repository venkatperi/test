### <a name='classes'>API</a>

 Class |  Summary
 ------| ------------
 <code>[AtomEnvironment](#class-AtomEnvironment)</code> | Atom global for dealing with packages, themes, menus, and the window.
 <code>[BufferedNodeProcess](#class-BufferedNodeProcess)</code> | Like <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/buffered-process.coffee#L21">{BufferedProcess}</a>, but accepts a Node script as the command to run.
 <code>[BufferedProcess](#class-BufferedProcess)</code> | A wrapper which provides standard error/output line buffering for Node's ChildProcess.
 <code>[Clipboard](#class-Clipboard)</code> | Represents the clipboard used for copying and pasting in Atom.
 <code>[Color](#class-Color)</code> | A simple color class returned from {Config::get} when the value at the key path is of type 'color'. 
 <code>[CommandRegistry](#class-CommandRegistry)</code> | Associates listener functions with commands in a context-sensitive way using CSS selectors. You can access a global instance of this class via `atom.commands`, and commands registered there will be presented in the command palette.
 <code>[Config](#class-Config)</code> | Used to access all of Atom's configuration details.
 <code>[ContextMenuManager](#class-ContextMenuManager)</code> | Provides a registry for commands that you'd like to appear in the context menu.
 <code>[Cursor](#class-Cursor)</code> | The `Cursor` class represents the little blinking line identifying where text can be inserted.
 <code>[Decoration](#class-Decoration)</code> | Represents a decoration that follows a `{DisplayMarker}`. A decoration is basically a visual representation of a marker. It allows you to add CSS classes to line numbers in the gutter, lines, and add selection-line regions around marked ranges of text.
 <code>[DeserializerManager](#class-DeserializerManager)</code> | Manages the deserializers used for serialized state
 <code>[GitRepository](#class-GitRepository)</code> | Represents the underlying git operations performed by Atom.
 <code>[GrammarRegistry](#class-GrammarRegistry)</code> | Syntax class holding the grammars used for tokenizing.
 <code>[Gutter](#class-Gutter)</code> | Represents a gutter within a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.
 <code>[LayerDecoration](#class-LayerDecoration)</code> | Represents a decoration that applies to every marker on a given layer. Created via {TextEditor::decorateMarkerLayer}. 
 <code>[MenuManager](#class-MenuManager)</code> | Provides a registry for menu items that you'd like to appear in the application menu.
 <code>[NotificationManager](#class-NotificationManager)</code> | A notification manager used to create <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/notification.coffee#L6">{Notification}</a>s to be shown to the user.
 <code>[Notification](#class-Notification)</code> | A notification to the user containing a message and type. 
 <code>[PackageManager](#class-PackageManager)</code> | Package manager for coordinating the lifecycle of Atom packages.
 <code>[Package](#class-Package)</code> | Loads and activates a package's main module and resources such as stylesheets, keymaps, grammar, editor properties, and menus. 
 <code>[Pane](#class-Pane)</code> | A container for presenting content in the center of the workspace. Panes can contain multiple items, one of which is *active* at a given time. The view corresponding to the active item is displayed in the interface. In the default configuration, tabs are also displayed for each item.
 <code>[Panel](#class-Panel)</code> | A container representing a panel on the edges of the editor window. You should not create a `Panel` directly, instead use {Workspace::addTopPanel} and friends to add panels.
 <code>[Project](#class-Project)</code> | Represents a project that's opened in Atom.
 <code>[ScopeDescriptor](#class-ScopeDescriptor)</code> | Wraps an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `String`s. The Array describes a path from the root of the syntax tree to a token including _all_ scope names for the entire path.
 <code>[Selection](#class-Selection)</code> | Represents a selection in the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>. 
 <code>[StyleManager](#class-StyleManager)</code> | A singleton instance of this class available via `atom.styles`, which you can use to globally query and observe the set of active style sheets. The `StyleManager` doesn't add any style elements to the DOM on its own, but is instead subscribed to by individual `<atom-styles>` elements, which clone and attach style elements in different contexts. 
 <code>[Task](#class-Task)</code> | Run a node script in a separate process.
 <code>[TextEditor](#class-TextEditor)</code> | This class represents all essential editing state for a single `{TextBuffer}`, including cursor and selection positions, folds, and soft wraps. If you're manipulating the state of an editor, use this class. If you're interested in the visual appearance of editors, use `{TextEditorElement}` instead.
 <code>[ThemeManager](#class-ThemeManager)</code> | Handles loading and activating available themes.
 <code>[TooltipManager](#class-TooltipManager)</code> | Associates tooltips with HTML elements or selectors.
 <code>[ViewRegistry](#class-ViewRegistry)</code> | `ViewRegistry` handles the association between model and view types in Atom. We call this association a View Provider. As in, for a given model, this class can provide a view via {::getView}, as long as the model/view association was registered via {::addViewProvider}
 <code>[Workspace](#class-Workspace)</code> | Represents the state of the user interface for the entire window. An instance of this class is available via the `atom.workspace` global.

<h3> <a name="class-AtomEnvironment">AtomEnvironment</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Atom global for dealing with packages, themes, menus, and the window.</p>
<p>An instance of this class is always available as the &#x60;atom&#x60; global. </p>


<table width="100%">
<tr><td colspan="2"><h5>Properties</h5></td></tr>

<tr>
  <td><b><code>commands</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/command-registry.coffee#L46">{CommandRegistry}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>config</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/config.coffee#L344">{Config}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>clipboard</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/clipboard.coffee#L16">{Clipboard}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>contextMenu</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/context-menu-manager.coffee#L43">{ContextMenuManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>menu</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/menu-manager.coffee#L61">{MenuManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>keymaps</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A `{KeymapManager}` instance </p>


</td> </tr>

<tr>
  <td><b><code>tooltips</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/tooltip-manager.coffee#L47">{TooltipManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>notifications</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/notification-manager.coffee#L10">{NotificationManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>project</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/project.coffee#L19">{Project}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>grammars</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/grammar-registry.coffee#L16">{GrammarRegistry}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>packages</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package-manager.coffee#L30">{PackageManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>themes</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/theme-manager.coffee#L11">{ThemeManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>styles</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/style-manager.coffee#L12">{StyleManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>deserializers</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/deserializer-manager.coffee#L23">{DeserializerManager}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>views</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/view-registry.coffee#L47">{ViewRegistry}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>workspace</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/workspace.coffee#L27">{Workspace}</a> instance </p>


</td> </tr>

<tr>
  <td><b><code>textEditors</code></b></td>
  <td width="20%"><code>Public</code></td>
</tr>

<tr><td colspan="2">
<p> A `{TextEditorRegistry}` instance </p>


</td> </tr>

<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidBeep(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called whenever {::beep} is called.</li>
</ul>

<p>Invoke the given callback whenever {::beep} is called.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillThrowError(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called whenever there is an unhandled error<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>originalError</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> the original error object</li>
<li><code>message</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> the original error object</li>
<li><code>url</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Url to the file where the error originated.</li>
<li><code>line</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
<li><code>column</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
<li><code>preventDefault</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> call this to avoid popping up the dev tools.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when there is an unhandled error, but
before the devtools pop open</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidThrowError(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called whenever there is an unhandled error<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>originalError</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> the original error object</li>
<li><code>message</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> the original error object</li>
<li><code>url</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Url to the file where the error originated.</li>
<li><code>line</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
<li><code>column</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback whenever there is an unhandled error.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>inDevMode(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current window is in development mode.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>inSafeMode(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current window is in safe mode.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>inSpecMode(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current window is running specs.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getVersion(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the version of the Atom application.</p>

<em>Returns</em>
<ul>
<li>Returns the version text <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isReleasedVersion(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current version is an official release.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getWindowLoadTime(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the time taken to completely load the current window.</p>
<p>This time include things like loading and activating packages, creating
DOM elements for the editor, and reading the config.</p>

<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of milliseconds taken to load the window or null
if the window hasn&#39;t finished loading yet.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLoadSettings(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the load settings for the current window.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing all the load setting key/value pairs.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>open(</b>params<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>pathsToOpen</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> paths to open.</li>
<li><code>newWindow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, true to always open a new window instead of reusing existing windows depending on the paths to open.</li>
<li><code>devMode</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, true to open the window in development mode. Development mode loads the Atom source from the locally cloned repository and also loads all the packages in ~/.atom/dev/packages</li>
<li><code>safeMode</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, true to open the window in safe mode. Safe mode prevents all packages installed to ~/.atom/packages from loading. </li>
</ul>
</li>
</ul>

<p>Open a new Atom window using the given options.</p>
<p>Calling this method without an options parameter will open a prompt to pick
a file/folder to open in the new window.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>pickFolder(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call once the user has confirmed the selection.<ul>
<li><code>paths</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> paths that the user selected, or <code>null</code> if the user dismissed the dialog. </li>
</ul>
</li>
</ul>

<p>Prompt the user to select one or more folders.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>close(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Close the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getSize(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the size of current window.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> in the format <code>{width: 1000, height: 700}</code></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setSize(</b>width, height<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>width</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of pixels.</li>
<li><code>height</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of pixels. </li>
</ul>

<p>Set the size of current window.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getPosition(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the position of current window.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> in the format <code>{x: 10, y: 20}</code></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setPosition(</b>x, y<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>x</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of pixels.</li>
<li><code>y</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of pixels. </li>
</ul>

<p>Set the position of current window.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getCurrentWindow(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the current window </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>center(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move current window to the center of the screen. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>focus(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Focus the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>show(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Show the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>hide(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Hide the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>reload(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Reload the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isMaximized(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current window is maximized.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isFullScreen(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if the current window is in full screen mode.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setFullScreen(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Set the full screen state of the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>toggleFullScreen(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Toggle the full screen state of the current window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>beep(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Visually and audibly trigger a beep. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>confirm(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>message</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message to display.</li>
<li><code>detailedMessage</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> detailed message to display.</li>
<li><code>buttons</code> Either an array of strings or an object where keys are button names and the values are callbacks to invoke when clicked.</li>
</ul>
</li>
</ul>

<p>A flexible way to open a dialog akin to an alert dialog.</p>

<em>Returns</em>
<ul>
<li>Returns the chosen button index <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> if the buttons option was an array.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>openDevTools(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Open the dev tools for the current window.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves when the DevTools have been opened.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>toggleDevTools(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Toggle the visibility of the dev tools for the current window.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves when the DevTools have been opened or
closed.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>executeJavaScriptInDevTools(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Execute code in dev tools. </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-BufferedNodeProcess">BufferedNodeProcess</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Like <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/buffered-process.coffee#L21">{BufferedProcess}</a>, but accepts a Node script as the command
to run.</p>
<p>This is necessary on Windows since it doesn&#x27;t support shebang &#x60;#!&#x60; lines.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>constructor(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>command</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the JavaScript script to execute.</li>
<li><code>args</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of arguments to pass to the script (optional).</li>
<li><code>options</code> The options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> to pass to Node&#39;s <code>ChildProcess.spawn</code><pre><code>  method (optional).
</code></pre></li>
<li><code>stdout</code> The callback <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that receives a single argument which<pre><code> contains the standard output from the command. The callback is
 called as data is received but it&#39;s buffered to ensure only
 complete lines are passed until the source stream closes. After
 the source stream has closed all remaining data is sent in a
 final call (optional).
</code></pre></li>
<li><code>stderr</code> The callback <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that receives a single argument which<pre><code> contains the standard error output from the command. The
 callback is called as data is received but it&#39;s buffered to
 ensure only complete lines are passed until the source stream
 closes. After the source stream has closed all remaining data
 is sent in a final call (optional).
</code></pre></li>
<li><code>exit</code> The callback <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> which receives a single argument<pre><code>containing the exit status (optional).
</code></pre></li>
</ul>
</li>
</ul>

<p>Runs the given Node script by spawning a new child process.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-BufferedProcess">BufferedProcess</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A wrapper which provides standard error/output line buffering for
Node&#x27;s ChildProcess.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>constructor(</b>options<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>command</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> command to execute.</li>
<li><code>args</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of arguments to pass to the command (optional).</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> (optional) The options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> to pass to Node&#39;s <code>ChildProcess.spawn</code> method.</li>
<li><code>stdout</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> (optional) The callback that receives a single argument which contains the standard output from the command. The callback is called as data is received but it&#39;s buffered to ensure only complete lines are passed until the source stream closes. After the source stream has closed all remaining data is sent in a final call.<ul>
<li><code>data</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a></li>
</ul>
</li>
<li><code>stderr</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> (optional) The callback that receives a single argument which contains the standard error output from the command. The callback is called as data is received but it&#39;s buffered to ensure only complete lines are passed until the source stream closes. After the source stream has closed all remaining data is sent in a final call.<ul>
<li><code>data</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a></li>
</ul>
</li>
<li><code>exit</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> (optional) The callback which receives a single argument containing the exit status.<ul>
<li><code>code</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> </li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Runs the given command by spawning a new child process.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onWillThrowError(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> callback<ul>
<li><code>errorObject</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>error</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> the error object</li>
<li><code>handle</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> call this to indicate you have handled the error. The error will not be thrown if this function is called.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Will call your callback when an error will be raised by the process.
Usually this is due to the command not being available or not on the PATH.
You can call &#x60;handle()&#x60; on the object passed to your callback to indicate
that you have handled this error.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}`</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>kill(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Terminate the process. </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Clipboard">Clipboard</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents the clipboard used for copying and pasting in Atom.</p>
<p>An instance of this class is always available as the &#x60;atom.clipboard&#x60; global.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>write(</b>text[, metadata]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>text</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to store.</li>
<li><code>metadata</code> The additional info to associate with the text. </li>
</ul>

<p>Write the given text to the clipboard.</p>
<p>The metadata associated with the text is available by calling
{::readWithMetadata}.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>read(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Read the text from the clipboard.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>readWithMetadata(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Read the text from the clipboard and return both the text and the
associated metadata.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:</p>
</li>
<li><p><code>text</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> clipboard text.</p>
</li>
<li><code>metadata</code> The metadata stored by an earlier call to {::write}.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Color">Color</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A simple color class returned from {Config::get} when the value
at the key path is of type &#x27;color&#x27;. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>parse(</b>value<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>value</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> such as <code>&#39;white&#39;</code>, <code>#ff00ff</code>, or <code>&#39;rgba(255, 15, 60, .75)&#39;</code> or an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with <code>red</code>, <code>green</code>, <code>blue</code>, and <code>alpha</code> properties.</li>
</ul>

<p>Parse a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> into a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/color.coffee#L7">{Color}</a>.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/color.coffee#L7">{Color}</a> or <code>null</code> if it cannot be parsed.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>toHexString(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> in the form <code>&#39;#abcdef&#39;</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>toRGBAString(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> in the form <code>&#39;rgba(25, 50, 75, .9)&#39;</code>.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-CommandRegistry">CommandRegistry</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Associates listener functions with commands in a
context-sensitive way using CSS selectors. You can access a global instance of
this class via &#x60;atom.commands&#x60;, and commands registered there will be
presented in the command palette.</p>
<p>The global command registry facilitates a style of event handling known as
<em>event delegation</em> that was popularized by jQuery. Atom commands are expressed
as custom DOM events that can be invoked on the currently focused element via
a key binding or manually via the command palette. Rather than binding
listeners for command events directly to DOM nodes, you instead register
command event listeners globally on &#x60;atom.commands&#x60; and constrain them to
specific kinds of elements with CSS selectors.</p>
<p>Command names must follow the &#x60;namespace:action&#x60; pattern, where &#x60;namespace&#x60;
will typically be the name of your package, and &#x60;action&#x60; describes the
behavior of your command. If either part consists of multiple words, these
must be separated by hyphens. E.g. &#x60;awesome-package:turn-it-up-to-eleven&#x60;.
All words should be lowercased.</p>
<p>As the event bubbles upward through the DOM, all registered event listeners
with matching selectors are invoked in order of specificity. In the event of a
specificity tie, the most recently registered listener is invoked first. This
mirrors the &quot;cascade&quot; semantics of CSS. Event listeners are invoked in the
context of the current DOM node, meaning &#x60;this&#x60; always points at
&#x60;event.currentTarget&#x60;. As is normally the case with DOM events,
&#x60;stopPropagation&#x60; and &#x60;stopImmediatePropagation&#x60; can be used to terminate the
bubbling process and prevent invocation of additional listeners.</p>
<h2 id="example">Example</h2>
<p>Here is a command that inserts the current date in an editor:</p>
<p>&#x60;&#x60;&#x60;coffee
atom.commands.add &#x27;atom-text-editor&#x27;,
  &#x27;user:insert-date&#x27;: (event) -&gt;
    editor &#x3D; @getModel()
    editor.insertText(new Date().toLocaleString())
&#x60;&#x60;&#x60;</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>add(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Add one or more command listeners associated with a selector.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
added command handler(s).</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>findCommands(</b>params<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing one or more of the following keys:<ul>
<li><code>target</code> A DOM node that is the hypothetical target of a given command.</li>
</ul>
</li>
</ul>

<p>Find all registered commands matching a query.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>s containing the following keys:</p>
</li>
<li><p><code>name</code> The name of the command. For example, <code>user:insert-date</code>.</p>
</li>
<li><code>displayName</code> The display name of the command. For example,
<code>User: Insert Date</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>dispatch(</b>target, commandName<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>target</code> The DOM node at which to start bubbling the command event.</li>
<li><code>commandName</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> indicating the name of the command to dispatch. </li>
</ul>

<p>Simulate the dispatch of a command on a DOM node.</p>
<p>This can be useful for testing when you want to simulate the invocation of a
command on a detached DOM node. Otherwise, the DOM node in question needs to
be attached to the document so the event bubbles up to the root node to be
processed.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onWillDispatch(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called before dispatching each command<ul>
<li><code>event</code> The Event that will be dispatched </li>
</ul>
</li>
</ul>

<p>Invoke the given callback before dispatching a command event.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidDispatch(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called after dispatching each command<ul>
<li><code>event</code> The Event that was dispatched </li>
</ul>
</li>
</ul>

<p>Invoke the given callback after dispatching a command event.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Config">Config</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Used to access all of Atom&#x27;s configuration details.</p>
<p>An instance of this class is always available as the &#x60;atom.config&#x60; global.</p>
<h2 id="getting-and-setting-config-settings-">Getting and setting config settings.</h2>
<p>&#x60;&#x60;&#x60;coffee</p>
<h1 id="note-that-with-no-value-set-get-returns-the-setting-x27-s-default-value-">Note that with no value set, ::get returns the setting&#x27;s default value.</h1>
<p>atom.config.get(&#x27;my-package.myKey&#x27;) # -&gt; &#x27;defaultValue&#x27;</p>
<p>atom.config.set(&#x27;my-package.myKey&#x27;, &#x27;value&#x27;)
atom.config.get(&#x27;my-package.myKey&#x27;) # -&gt; &#x27;value&#x27;
&#x60;&#x60;&#x60;</p>
<p>You may want to watch for changes. Use {::observe} to catch changes to the setting.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.set(&#x27;my-package.myKey&#x27;, &#x27;value&#x27;)
atom.config.observe &#x27;my-package.myKey&#x27;, (newValue) -&gt;</p>
<h1 id="-x60-observe-x60-calls-immediately-and-every-time-the-value-is-changed">&#x60;observe&#x60; calls immediately and every time the value is changed</h1>
<p>  console.log &#x27;My configuration changed:&#x27;, newValue
&#x60;&#x60;&#x60;</p>
<p>If you want a notification only when the value changes, use {::onDidChange}.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.onDidChange &#x27;my-package.myKey&#x27;, ({newValue, oldValue}) -&gt;
  console.log &#x27;My configuration changed:&#x27;, newValue, oldValue
&#x60;&#x60;&#x60;</p>
<h3 id="value-coercion">Value Coercion</h3>
<p>Config settings each have a type specified by way of a
<a href="json-schema.org">schema</a>. For example we might an integer setting that only
allows integers greater than &#x60;0&#x60;:</p>
<p>&#x60;&#x60;&#x60;coffee</p>
<h1 id="when-no-value-has-been-set-x60-get-x60-returns-the-setting-x27-s-default-value">When no value has been set, &#x60;::get&#x60; returns the setting&#x27;s default value</h1>
<p>atom.config.get(&#x27;my-package.anInt&#x27;) # -&gt; 12</p>
<h1 id="the-string-will-be-coerced-to-the-integer-123">The string will be coerced to the integer 123</h1>
<p>atom.config.set(&#x27;my-package.anInt&#x27;, &#x27;123&#x27;)
atom.config.get(&#x27;my-package.anInt&#x27;) # -&gt; 123</p>
<h1 id="the-string-will-be-coerced-to-an-integer-but-it-must-be-greater-than-0-so-is-set-to-1">The string will be coerced to an integer, but it must be greater than 0, so is set to 1</h1>
<p>atom.config.set(&#x27;my-package.anInt&#x27;, &#x27;-20&#x27;)
atom.config.get(&#x27;my-package.anInt&#x27;) # -&gt; 1
&#x60;&#x60;&#x60;</p>
<h2 id="defining-settings-for-your-package">Defining settings for your package</h2>
<p>Define a schema under a &#x60;config&#x60; key in your package main.</p>
<p>&#x60;&#x60;&#x60;coffee
module.exports &#x3D;</p>
<h1 id="your-config-schema">Your config schema</h1>
<p>  config:
    someInt:
      type: &#x27;integer&#x27;
      default: 23
      minimum: 1</p>
<p>  activate: (state) -&gt; # ...</p>
<h1 id="-">...</h1>
<p>&#x60;&#x60;&#x60;</p>
<p>See <a href="https://atom.io/docs/latest/hacking-atom-package-word-count">package docs</a> for
more info.</p>
<h2 id="config-schemas">Config Schemas</h2>
<p>We use <a href="http://json-schema.org">json schema</a> which allows you to define your value&#x27;s
default, the type it should be, etc. A simple example:</p>
<p>&#x60;&#x60;&#x60;coffee</p>
<h1 id="we-want-to-provide-an-x60-enablething-x60-and-a-x60-thingvolume-x60-">We want to provide an &#x60;enableThing&#x60;, and a &#x60;thingVolume&#x60;</h1>
<p>config:
  enableThing:
    type: &#x27;boolean&#x27;
    default: false
  thingVolume:
    type: &#x27;integer&#x27;
    default: 5
    minimum: 1
    maximum: 11
&#x60;&#x60;&#x60;</p>
<p>The type keyword allows for type coercion and validation. If a &#x60;thingVolume&#x60; is
set to a string &#x60;&#x27;10&#x27;&#x60;, it will be coerced into an integer.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.set(&#x27;my-package.thingVolume&#x27;, &#x27;10&#x27;)
atom.config.get(&#x27;my-package.thingVolume&#x27;) # -&gt; 10</p>
<h1 id="it-respects-the-min-max">It respects the min / max</h1>
<p>atom.config.set(&#x27;my-package.thingVolume&#x27;, &#x27;400&#x27;)
atom.config.get(&#x27;my-package.thingVolume&#x27;) # -&gt; 11</p>
<h1 id="if-it-cannot-be-coerced-the-value-will-not-be-set">If it cannot be coerced, the value will not be set</h1>
<p>atom.config.set(&#x27;my-package.thingVolume&#x27;, &#x27;cats&#x27;)
atom.config.get(&#x27;my-package.thingVolume&#x27;) # -&gt; 11
&#x60;&#x60;&#x60;</p>
<h3 id="supported-types">Supported Types</h3>
<p>The &#x60;type&#x60; keyword can be a string with any one of the following. You can also
chain them by specifying multiple in an an array. For example</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: [&#x27;boolean&#x27;, &#x27;integer&#x27;]
    default: 5</p>
<h1 id="then">Then</h1>
<p>atom.config.set(&#x27;my-package.someSetting&#x27;, &#x27;true&#x27;)
atom.config.get(&#x27;my-package.someSetting&#x27;) # -&gt; true</p>
<p>atom.config.set(&#x27;my-package.someSetting&#x27;, &#x27;12&#x27;)
atom.config.get(&#x27;my-package.someSetting&#x27;) # -&gt; 12
&#x60;&#x60;&#x60;</p>
<h4 id="string">string</h4>
<p>Values must be a string.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;string&#x27;
    default: &#x27;hello&#x27;
&#x60;&#x60;&#x60;</p>
<h4 id="integer">integer</h4>
<p>Values will be coerced into integer. Supports the (optional) &#x60;minimum&#x60; and
&#x60;maximum&#x60; keys.</p>
<p>&#x60;&#x60;&#x60;coffee
  config:
    someSetting:
      type: &#x27;integer&#x27;
      default: 5
      minimum: 1
      maximum: 11
&#x60;&#x60;&#x60;</p>
<h4 id="number">number</h4>
<p>Values will be coerced into a number, including real numbers. Supports the
(optional) &#x60;minimum&#x60; and &#x60;maximum&#x60; keys.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;number&#x27;
    default: 5.3
    minimum: 1.5
    maximum: 11.5
&#x60;&#x60;&#x60;</p>
<h4 id="boolean">boolean</h4>
<p>Values will be coerced into a Boolean. &#x60;&#x27;true&#x27;&#x60; and &#x60;&#x27;false&#x27;&#x60; will be coerced into
a boolean. Numbers, arrays, objects, and anything else will not be coerced.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;boolean&#x27;
    default: false
&#x60;&#x60;&#x60;</p>
<h4 id="array">array</h4>
<p>Value must be an Array. The types of the values can be specified by a
subschema in the &#x60;items&#x60; key.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;array&#x27;
    default: [1, 2, 3]
    items:
      type: &#x27;integer&#x27;
      minimum: 1.5
      maximum: 11.5
&#x60;&#x60;&#x60;</p>
<h4 id="color">color</h4>
<p>Values will be coerced into a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/color.coffee#L7">{Color}</a> with &#x60;red&#x60;, &#x60;green&#x60;, &#x60;blue&#x60;, and &#x60;alpha&#x60;
properties that all have numeric values. &#x60;red&#x60;, &#x60;green&#x60;, &#x60;blue&#x60; will be in
the range 0 to 255 and &#x60;value&#x60; will be in the range 0 to 1. Values can be any
valid CSS color format such as &#x60;#abc&#x60;, &#x60;#abcdef&#x60;, &#x60;white&#x60;,
&#x60;rgb(50, 100, 150)&#x60;, and &#x60;rgba(25, 75, 125, .75)&#x60;.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;color&#x27;
    default: &#x27;white&#x27;
&#x60;&#x60;&#x60;</p>
<h4 id="object-grouping-other-types">object / Grouping other types</h4>
<p>A config setting with the type &#x60;object&#x60; allows grouping a set of config
settings. The group will be visualy separated and has its own group headline.
The sub options must be listed under a &#x60;properties&#x60; key.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;object&#x27;
    properties:
      myChildIntOption:
        type: &#x27;integer&#x27;
        minimum: 1.5
        maximum: 11.5
&#x60;&#x60;&#x60;</p>
<h3 id="other-supported-keys">Other Supported Keys</h3>
<h4 id="enum">enum</h4>
<p>All types support an &#x60;enum&#x60; key, which lets you specify all the values the
setting can take. &#x60;enum&#x60; may be an array of allowed values (of the specified
type), or an array of objects with &#x60;value&#x60; and &#x60;description&#x60; properties, where
the &#x60;value&#x60; is an allowed value, and the &#x60;description&#x60; is a descriptive string
used in the settings view.</p>
<p>In this example, the setting must be one of the 4 integers:</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;integer&#x27;
    default: 4
    enum: [2, 4, 6, 8]
&#x60;&#x60;&#x60;</p>
<p>In this example, the setting must be either &#x27;foo&#x27; or &#x27;bar&#x27;, which are
presented using the provided descriptions in the settings pane:</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    type: &#x27;string&#x27;
    default: &#x27;foo&#x27;
    enum: [
      {value: &#x27;foo&#x27;, description: &#x27;Foo mode. You want this.&#x27;}
      {value: &#x27;bar&#x27;, description: &#x27;Bar mode. Nobody wants that!&#x27;}
    ]
&#x60;&#x60;&#x60;</p>
<p>Usage:</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.set(&#x27;my-package.someSetting&#x27;, &#x27;2&#x27;)
atom.config.get(&#x27;my-package.someSetting&#x27;) # -&gt; 2</p>
<h1 id="will-not-set-values-outside-of-the-enum-values">will not set values outside of the enum values</h1>
<p>atom.config.set(&#x27;my-package.someSetting&#x27;, &#x27;3&#x27;)
atom.config.get(&#x27;my-package.someSetting&#x27;) # -&gt; 2</p>
<h1 id="if-it-cannot-be-coerced-the-value-will-not-be-set">If it cannot be coerced, the value will not be set</h1>
<p>atom.config.set(&#x27;my-package.someSetting&#x27;, &#x27;4&#x27;)
atom.config.get(&#x27;my-package.someSetting&#x27;) # -&gt; 4
&#x60;&#x60;&#x60;</p>
<h4 id="title-and-description">title and description</h4>
<p>The settings view will use the &#x60;title&#x60; and &#x60;description&#x60; keys to display your
config setting in a readable way. By default the settings view humanizes your
config key, so &#x60;someSetting&#x60; becomes &#x60;Some Setting&#x60;. In some cases, this is
confusing for users, and a more descriptive title is useful.</p>
<p>Descriptions will be displayed below the title in the settings view.</p>
<p>For a group of config settings the humanized key or the title and the
description are used for the group headline.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  someSetting:
    title: &#x27;Setting Magnitude&#x27;
    description: &#x27;This will affect the blah and the other blah&#x27;
    type: &#x27;integer&#x27;
    default: 4
&#x60;&#x60;&#x60;</p>
<p><strong>Note</strong>: You should strive to be so clear in your naming of the setting that
you do not need to specify a title or description!</p>
<p>Descriptions allow a subset of
<a href="https://help.github.com/articles/github-flavored-markdown/">Markdown formatting</a>.
Specifically, you may use the following in configuration setting descriptions:</p>
<ul>
<li><strong>bold</strong> - &#x60;<strong>bold</strong>&#x60;</li>
<li><em>italics</em> - &#x60;<em>italics</em>&#x60;</li>
<li><a href="https://atom.io">links</a> - &#x60;<a href="https://atom.io">links</a>&#x60;</li>
<li>&#x60;code spans&#x60; - &#x60;\&#x60;code spans\&#x60;&#x60;</li>
<li>line breaks - &#x60;line breaks&lt;br/&gt;&#x60;</li>
<li><del>strikethrough</del> - &#x60;<del>strikethrough</del>&#x60;</li>
</ul>
<h4 id="order">order</h4>
<p>The settings view orders your settings alphabetically. You can override this
ordering with the order key.</p>
<p>&#x60;&#x60;&#x60;coffee
config:
  zSetting:
    type: &#x27;integer&#x27;
    default: 4
    order: 1
  aSetting:
    type: &#x27;integer&#x27;
    default: 4
    order: 2
&#x60;&#x60;&#x60;</p>
<h2 id="best-practices">Best practices</h2>
<ul>
<li>Don&#x27;t depend on (or write to) configuration keys outside of your keypath.</li>
</ul>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>observe(</b>keyPath[, options], callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key to observe</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>scope</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> describing a path from the root of the syntax tree to a token. Get one by calling {editor.getLastCursor().getScopeDescriptor()}. See {::get} for examples. See <a href="https://atom.io/docs/latest/behind-atom-scoped-settings-scopes-and-scope-descriptors">the scopes docs</a> for more information.</li>
</ul>
</li>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call when the value of the key changes.<ul>
<li><code>value</code> the new value of the key</li>
</ul>
</li>
</ul>

<p>Add a listener for changes to a given key path. This is different
than {::onDidChange} in that it will immediately call your callback with the
current value of the config entry.</p>
<h3 id="examples">Examples</h3>
<p>You might want to be notified when the themes change. We&#x27;ll watch
&#x60;core.themes&#x60; for changes</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.observe &#x27;core.themes&#x27;, (value) -&gt;</p>
<h1 id="do-stuff-with-value">do stuff with value</h1>
<p>&#x60;&#x60;&#x60;</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` with the following keys on which you can call
<code>.dispose()</code> to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChange(</b>[keyPath][, options], callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key to observe. Must be specified if <code>scopeDescriptor</code> is specified.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>scope</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> describing a path from the root of the syntax tree to a token. Get one by calling {editor.getLastCursor().getScopeDescriptor()}. See {::get} for examples. See <a href="https://atom.io/docs/latest/behind-atom-scoped-settings-scopes-and-scope-descriptors">the scopes docs</a> for more information.</li>
</ul>
</li>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call when the value of the key changes.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>newValue</code> the new value of the key</li>
<li><code>oldValue</code> the prior value of the key.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Add a listener for changes to a given key path. If &#x60;keyPath&#x60; is
not specified, your callback will be called on changes to any key.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` with the following keys on which you can call
<code>.dispose()</code> to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>get(</b>keyPath[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key to retrieve.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>sources</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> source names. If provided, only values that were associated with these sources during {::set} will be used.</li>
<li><code>excludeSources</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> source names. If provided, values that  were associated with these sources during {::set} will not be used.</li>
<li><code>scope</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> describing a path from the root of the syntax tree to a token. Get one by calling {editor.getLastCursor().getScopeDescriptor()} See <a href="https://atom.io/docs/latest/behind-atom-scoped-settings-scopes-and-scope-descriptors">the scopes docs</a> for more information.</li>
</ul>
</li>
</ul>

<p>Retrieves the setting for the given key.</p>
<h3 id="examples">Examples</h3>
<p>You might want to know what themes are enabled, so check &#x60;core.themes&#x60;</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.get(&#x27;core.themes&#x27;)
&#x60;&#x60;&#x60;</p>
<p>With scope descriptors you can get settings within a specific editor
scope. For example, you might want to know &#x60;editor.tabLength&#x60; for ruby
files.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.ruby&#x27;]) # &#x3D;&gt; 2
&#x60;&#x60;&#x60;</p>
<p>This setting in ruby files might be different than the global tabLength setting</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.get(&#x27;editor.tabLength&#x27;) # &#x3D;&gt; 4
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.ruby&#x27;]) # &#x3D;&gt; 2
&#x60;&#x60;&#x60;</p>
<p>You can get the language scope descriptor via
{TextEditor::getRootScopeDescriptor}. This will get the setting specifically
for the editor&#x27;s language.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.get(&#x27;editor.tabLength&#x27;, scope: @editor.getRootScopeDescriptor()) # &#x3D;&gt; 2
&#x60;&#x60;&#x60;</p>
<p>Additionally, you can get the setting at the specific cursor position.</p>
<p>&#x60;&#x60;&#x60;coffee
scopeDescriptor &#x3D; @editor.getLastCursor().getScopeDescriptor()
atom.config.get(&#x27;editor.tabLength&#x27;, scope: scopeDescriptor) # &#x3D;&gt; 2
&#x60;&#x60;&#x60;</p>

<em>Returns</em>
<ul>
<li>Returns the value from Atom&#39;s default settings, the user&#39;s configuration
file in the type specified by the configuration schema.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getAll(</b>keyPath[, options]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key to retrieve</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> see the <code>options</code> argument to {::get}</li>
</ul>

<p>Get all of the values for the given key-path, along with their
associated scope selector.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>s with the following keys:</p>
</li>
<li><p><code>scopeDescriptor</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> with which the value is associated</p>
</li>
<li><code>value</code> The value for the key-path</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>set(</b>keyPath, value[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key.</li>
<li><code>value</code> The value of the setting. Passing <code>undefined</code> will revert the setting to the default value.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>scopeSelector</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>. eg. &#39;.source.ruby&#39; See <a href="https://atom.io/docs/latest/behind-atom-scoped-settings-scopes-and-scope-descriptors">the scopes docs</a> for more information.</li>
<li><code>source</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> The name of a file with which the setting is associated. Defaults to the user&#39;s config file.</li>
</ul>
</li>
</ul>

<p>Sets the value for a configuration setting.</p>
<p>This value is stored in Atom&#x27;s internal configuration file.</p>
<h3 id="examples">Examples</h3>
<p>You might want to change the themes programmatically:</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.set(&#x27;core.themes&#x27;, [&#x27;atom-light-ui&#x27;, &#x27;atom-light-syntax&#x27;])
&#x60;&#x60;&#x60;</p>
<p>You can also set scoped settings. For example, you might want change the
&#x60;editor.tabLength&#x60; only for ruby files.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.config.get(&#x27;editor.tabLength&#x27;) # &#x3D;&gt; 4
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.ruby&#x27;]) # &#x3D;&gt; 4
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.js&#x27;]) # &#x3D;&gt; 4</p>
<h1 id="set-ruby-to-2">Set ruby to 2</h1>
<p>atom.config.set(&#x27;editor.tabLength&#x27;, 2, scopeSelector: &#x27;.source.ruby&#x27;) # &#x3D;&gt; true</p>
<h1 id="notice-it-x27-s-only-set-to-2-in-the-case-of-ruby">Notice it&#x27;s only set to 2 in the case of ruby</h1>
<p>atom.config.get(&#x27;editor.tabLength&#x27;) # &#x3D;&gt; 4
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.ruby&#x27;]) # &#x3D;&gt; 2
atom.config.get(&#x27;editor.tabLength&#x27;, scope: [&#x27;source.js&#x27;]) # &#x3D;&gt; 4
&#x60;&#x60;&#x60;</p>

<em>Returns</em>
<ul>
<li><p>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></p>
</li>
<li><p><code>true</code> if the value was set.</p>
</li>
<li><code>false</code> if the value was not able to be coerced to the type specified in the setting&#39;s schema.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>unset(</b>keyPath[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>scopeSelector</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>. See {::set}</li>
<li><code>source</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>. See {::set} </li>
</ul>
</li>
</ul>

<p>Restore the setting at &#x60;keyPath&#x60; to its default value.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getSources(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all of the &#x60;source&#x60; <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s with which
settings have been added via {::set}. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getSchema(</b>keyPath<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>keyPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the key.</li>
</ul>

<p>Retrieve the schema for a specific key path. The schema will tell
you what type the keyPath expects, and other metadata about the config
option.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> eg. <code>{type: &#39;integer&#39;, default: 23, minimum: 1}</code>.</li>
<li>Returns <code>null</code> when the keyPath has no schema specified, but is accessible
from the root schema.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getUserConfigPath(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the config file being used. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>transact(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to execute while suppressing calls to handlers. </li>
</ul>

<p>Suppress calls to handler functions registered with {::onDidChange}
and {::observe} for the duration of &#x60;callback&#x60;. After &#x60;callback&#x60; executes,
handlers will be called once if the value for their key-path has changed.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-ContextMenuManager">ContextMenuManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Provides a registry for commands that you&#x27;d like to appear in the
context menu.</p>
<p>An instance of this class is always available as the &#x60;atom.contextMenu&#x60;
global.</p>
<h2 id="context-menu-cson-format">Context Menu CSON Format</h2>
<p>&#x60;&#x60;&#x60;coffee
&#x27;atom-workspace&#x27;: [{label: &#x27;Help&#x27;, command: &#x27;application:open-documentation&#x27;}]
&#x27;atom-text-editor&#x27;: [{
  label: &#x27;History&#x27;,
  submenu: [
    {label: &#x27;Undo&#x27;, command:&#x27;core:undo&#x27;}
    {label: &#x27;Redo&#x27;, command:&#x27;core:redo&#x27;}
  ]
}]
&#x60;&#x60;&#x60;</p>
<p>In your package&#x27;s menu &#x60;.cson&#x60; file you need to specify it under a
&#x60;context-menu&#x60; key:</p>
<p>&#x60;&#x60;&#x60;coffee
&#x27;context-menu&#x27;:
  &#x27;atom-workspace&#x27;: [{label: &#x27;Help&#x27;, command: &#x27;application:open-documentation&#x27;}]
  ...
&#x60;&#x60;&#x60;</p>
<p>The format for use in {::add} is the same minus the &#x60;context-menu&#x60; key. See
{::add} for more information. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>add(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>itemsBySelector</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> whose keys are CSS selectors and whose values are <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>s of item <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>s containing the following keys:<ul>
<li><code>label</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing the menu item&#39;s label.</li>
<li><code>command</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing the command to invoke on the target of the right click that invoked the context menu.</li>
<li><code>enabled</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the menu item should be clickable. Disabled menu items typically appear grayed out. Defaults to <code>true</code>.</li>
<li><code>submenu</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of additional items.</li>
<li><code>type</code> If you want to create a separator, provide an item  with <code>type: &#39;separator&#39;</code> and no other keys.</li>
<li><code>visible</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the menu item should appear in the menu. Defaults to <code>true</code>.</li>
<li><code>created</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called on the item each time a context menu is created via a right click. You can assign properties to <code>this</code> to dynamically compute the command, label, etc. This method is actually called on a clone of the original item template to prevent state from leaking across context menu deployments. Called with the following argument:<ul>
<li><code>event</code> The click event that deployed the context menu.</li>
</ul>
</li>
<li><code>shouldDisplay</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called to determine whether to display this item on a given context menu deployment. Called with the following argument:<ul>
<li><code>event</code> The click event that deployed the context menu.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Add context menu items scoped by CSS selectors.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
added menu items.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Cursor">Cursor</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>The &#x60;Cursor&#x60; class represents the little blinking line identifying
where text can be inserted.</p>
<p>Cursors belong to <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>s and have some metadata attached in the form
of a `{DisplayMarker}`. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangePosition(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>oldBufferPosition</code> `{Point}`</li>
<li><code>oldScreenPosition</code> `{Point}`</li>
<li><code>newBufferPosition</code> `{Point}`</li>
<li><code>newScreenPosition</code> `{Point}`</li>
<li><code>textChanged</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
<li><code>Cursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> that triggered the event</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the cursor has been moved.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the cursor is destroyed</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeVisibility(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>visibility</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the cursor&#x27;s visibility has changed</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setScreenPosition(</b>screenPosition[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenPosition</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of two numbers: the screen row, and the screen column.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>autoscroll</code> A Boolean which, if <code>true</code>, scrolls the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> to wherever the cursor moves to. </li>
</ul>
</li>
</ul>

<p>Moves a cursor to a given screen position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getScreenPosition(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the screen position of the cursor as a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setBufferPosition(</b>bufferPosition[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of two numbers: the buffer row, and the buffer column.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>autoscroll</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to autoscroll to the new position. Defaults to <code>true</code> if this is the most recently added cursor, <code>false</code> otherwise. </li>
</ul>
</li>
</ul>

<p>Moves a cursor to a given buffer position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getBufferPosition(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the current buffer position as an Array.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getScreenRow(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the cursor&#39;s current screen row.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getScreenColumn(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the cursor&#39;s current screen column.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBufferRow(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Retrieves the cursor&#x27;s current buffer row. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getBufferColumn(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the cursor&#39;s current buffer column.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentBufferLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the cursor&#39;s current buffer row of text excluding its line
ending.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isAtBeginningOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns whether the cursor is at the start of a line.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isAtEndOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns whether the cursor is on the line return character.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getMarker(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the underlying `{DisplayMarker}` for the cursor.
Useful with overlay <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isSurroundedByWhitespace(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Identifies if the cursor is surrounded by whitespace.</p>
<p>&quot;Surrounded&quot; here means that the character directly before and after the
cursor are both whitespace.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isBetweenWordAndNonWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>This method returns false if the character before or after the cursor is
whitespace.</p>

<em>Returns</em>
<ul>
<li>Returns whether the cursor is currently between a word and non-word
character. The non-word characters are defined by the
<code>editor.nonWordCharacters</code> config value.</li>
<li>Returns a Boolean.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isInsideWord(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot; (default: {::wordRegExp}).</li>
</ul>
</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns whether this cursor is between a word&#39;s start and end.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getIndentLevel(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the indentation level of the current line.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getScopeDescriptor(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Retrieves the scope descriptor for the cursor&#x27;s current position.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>hasPrecedingCharactersOnLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns true if this cursor has no non-whitespace characters before
its current position.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isLastCursor(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Identifies if this cursor is the last in the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.</p>
<p>&quot;Last&quot; is defined as the most recently added cursor.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>moveUp(</b>[rowCount][, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to move (default: 1)</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>moveToEndOfSelection</code> if true, move to the left of the selection if a selection exists. </li>
</ul>
</li>
</ul>

<p>Moves the cursor up one screen row.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveDown(</b>[rowCount][, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to move (default: 1)</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>moveToEndOfSelection</code> if true, move to the left of the selection if a selection exists. </li>
</ul>
</li>
</ul>

<p>Moves the cursor down one screen row.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveLeft(</b>[columnCount][, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to move (default: 1)</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>moveToEndOfSelection</code> if true, move to the left of the selection if a selection exists. </li>
</ul>
</li>
</ul>

<p>Moves the cursor left one screen column.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveRight(</b>[columnCount][, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to move (default: 1)</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>moveToEndOfSelection</code> if true, move to the right of the selection if a selection exists. </li>
</ul>
</li>
</ul>

<p>Moves the cursor right one screen column.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToTop(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the top of the buffer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBottom(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the bottom of the buffer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfScreenLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the buffer line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToFirstCharacterOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the first character in the
line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfScreenLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the end of the line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the end of the buffer line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the end of the word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfNextWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the next word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the previous word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the next word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToPreviousSubwordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the previous subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToNextSubwordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the next subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>skipLeadingWhitespace(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the buffer line, skipping all
whitespace. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfNextParagraph(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the next paragraph </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfPreviousParagraph(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the cursor to the beginning of the previous paragraph </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getPreviousWordBoundaryBufferPosition(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot;  (default: {::wordRegExp}) </li>
</ul>
</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns buffer position of previous word boundary. It might be on
the current word, or the previous word.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getNextWordBoundaryBufferPosition(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot;  (default: {::wordRegExp}) </li>
</ul>
</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns buffer position of the next word boundary. It might be on
the current word, or the previous word.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBeginningOfCurrentWordBufferPosition(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot; (default: {::wordRegExp}).</li>
<li><code>includeNonWordCharacters</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to include non-word characters in the default word regex. Has no effect if wordRegex is set.</li>
<li><code>allowPrevious</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the beginning of the previous word can be returned.</li>
</ul>
</li>
</ul>

<p>Retrieves the buffer position of where the current word starts.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getEndOfCurrentWordBufferPosition(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot;  (default: {::wordRegExp})</li>
<li><code>includeNonWordCharacters</code> A Boolean indicating whether to include non-word characters in the default word regex. Has no effect if wordRegex is set.</li>
</ul>
</li>
</ul>

<p>Retrieves the buffer position of where the current word ends.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBeginningOfNextWordBufferPosition(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot; (default: {::wordRegExp}).</li>
</ul>
</li>
</ul>

<p>Retrieves the buffer position of where the next word starts.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentWordBufferRange(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>wordRegex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> indicating what constitutes a &quot;word&quot; (default: {::wordRegExp}). </li>
</ul>
</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the buffer Range occupied by the word located under the cursor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentLineBufferRange(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>includeNewline</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> which controls whether the Range should include the newline. </li>
</ul>
</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the buffer Range for the current line.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentParagraphBufferRange(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Retrieves the range for the current paragraph.</p>
<p>A paragraph is defined as a block of text surrounded by empty lines or comments.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentWordPrefix(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the characters preceding the cursor in the current word.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setVisible(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Sets whether the cursor is visible. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isVisible(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the visibility of the cursor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>compare(</b>otherCursor<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>otherCursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> to compare against </li>
</ul>

<p>Compare this cursor&#x27;s buffer position to another cursor&#x27;s buffer position.</p>
<p>See {Point::compare} for more details.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>clearAutoscroll(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Prevents this cursor from causing scrolling. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>clearSelection(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Deselects the current selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>wordRegExp(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>includeNonWordCharacters</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to include non-word characters in the regex. (default: true)</li>
</ul>
</li>
</ul>

<p>Get the RegExp used by the cursor to determine what a &quot;word&quot; is.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>subwordRegExp(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>backwards</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to look forwards or backwards for the next subword. (default: false)</li>
</ul>
</li>
</ul>

<p>Get the RegExp used by the cursor to determine what a &quot;subword&quot; is.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a>.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Decoration">Decoration</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents a decoration that follows a `{DisplayMarker}`. A decoration is
basically a visual representation of a marker. It allows you to add CSS
classes to line numbers in the gutter, lines, and add selection-line regions
around marked ranges of text.</p>
<p><a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> objects are not meant to be created directly, but created with
{TextEditor::decorateMarker}. eg.</p>
<p>&#x60;&#x60;&#x60;coffee
range &#x3D; editor.getSelectedBufferRange() # any range you like
marker &#x3D; editor.markBufferRange(range)
decoration &#x3D; editor.decorateMarker(marker, {type: &#x27;line&#x27;, class: &#x27;my-line-class&#x27;})
&#x60;&#x60;&#x60;</p>
<p>Best practice for destroying the decoration is by destroying the `{DisplayMarker}`.</p>
<p>&#x60;&#x60;&#x60;coffee
marker.destroy()
&#x60;&#x60;&#x60;</p>
<p>You should only use {Decoration::destroy} when you still need or do not own
the marker. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Destroy this marker.</p>
<p>If you own the marker, you should use {DisplayMarker::destroy} which will destroy
this decoration. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeProperties(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>oldProperties</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> the old parameters the decoration used to have</li>
<li><code>newProperties</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> the new parameters the decoration now has</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>When the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> is updated via {Decoration::update}.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> is destroyed</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getId(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>An id unique across all <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> objects </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getMarker(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the marker associated with this <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getProperties(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>&#39;s properties.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setProperties(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>newProperties</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> eg. <code>{type: &#39;line-number&#39;, class: &#39;my-new-class&#39;}</code> </li>
</ul>

<p>Update the marker with new Properties. Allows you to change the decoration&#x27;s class.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-DeserializerManager">DeserializerManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Manages the deserializers used for serialized state</p>
<p>An instance of this class is always available as the &#x60;atom.deserializers&#x60;
global.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>add(</b>deserializers<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>deserializers</code> One or more deserializers to register. A deserializer can be any object with a <code>.name</code> property and a <code>.deserialize()</code> method. A common approach is to register a <em>constructor</em> as the deserializer for its instances by adding a <code>.deserialize()</code> class method. When your method is called, it will be passed serialized state as the first argument and the `{Atom}` environment object as the second argument, which is useful if you wish to avoid referencing the <code>atom</code> global. </li>
</ul>

<p>Register the given class(es) as deserializers.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deserialize(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>state</code> The state <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> to deserialize. </li>
</ul>

<p>Deserialize the state and params.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-GitRepository">GitRepository</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents the underlying git operations performed by Atom.</p>
<p>This class shouldn&#x27;t be instantiated directly but instead by accessing the
&#x60;atom.project&#x60; global and calling &#x60;getRepositories()&#x60;. Note that this will
only be available when the project is backed by a Git repository.</p>
<p>This class handles submodules automatically by taking a &#x60;path&#x60; argument to many
of the methods.  This &#x60;path&#x60; argument will determine which underlying
repository is used.</p>
<p>For a repository with submodules this would have the following outcome:</p>
<p>&#x60;&#x60;&#x60;coffee
repo &#x3D; atom.project.getRepositories()[0]
repo.getShortHead() # &#x27;master&#x27;
repo.getShortHead(&#x27;vendor/path/to/a/submodule&#x27;) # &#x27;dead1234&#x27;
&#x60;&#x60;&#x60;</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>open(</b>path, options<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the Git repository to open.</li>
<li><code>options</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>refreshOnWindowFocus</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, <code>true</code> to refresh the index and statuses when the window is focused.</li>
</ul>
</li>
</ul>

<p>Creates a new GitRepository instance.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/git-repository.coffee#L44">{GitRepository}</a> instance or <code>null</code> if the repository could not be opened.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Destroy this <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/git-repository.coffee#L44">{GitRepository}</a> object.</p>
<p>This destroys any tasks and subscriptions and releases the underlying
libgit2 repository handle. This method is idempotent. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when this GitRepository&#x27;s destroy() method
is invoked.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeStatus(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>path</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> the old parameters the decoration used to have</li>
<li><code>pathStatus</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the status. This value can be passed to {::isStatusModified} or {::isStatusNew} to get more information.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a specific file&#x27;s status has
changed. When a file is updated, reloaded, etc, and the status changes, this
will be fired.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeStatuses(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when a multiple files&#x27; statuses have
changed. For example, on window focus, the status of all the paths in the
repo is checked. If any of them have changed, this will be fired. Call
{::getPathStatus(path)} to get the status for your path of choice.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getType(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> indicating the type of version control system used by
this repository.</p>

<em>Returns</em>
<ul>
<li>Returns <code>&quot;git&quot;</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPath(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path of the repository.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getWorkingDirectory(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> working directory path of the repository.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isProjectAtRoot(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns true if at the root, false if in a subfolder of the
repository.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>relativize(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Makes a path relative to the repository&#x27;s working directory. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>hasBranch(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns true if the given branch exists.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getShortHead(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository contains submodules.</li>
</ul>

<p>Retrieves a shortened version of the HEAD reference value.</p>
<p>This removes the leading segments of &#x60;refs/heads&#x60;, &#x60;refs/tags&#x60;, or
&#x60;refs/remotes&#x60;.  It also shortens the SHA-1 of a detached &#x60;HEAD&#x60; to 7
characters.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isSubmodule(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>

<p>Is the given path a submodule in the repository?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getAheadBehindCount(</b>reference, path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>reference</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> branch reference name.</li>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository contains submodules. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the number of commits behind the current branch is from the
its upstream remote branch.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCachedUpstreamAheadBehindCount(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository has submodules.</li>
</ul>

<p>Get the cached ahead/behind commit counts for the current branch&#x27;s
upstream branch.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:</p>
</li>
<li><p><code>ahead</code>  The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of commits ahead.</p>
</li>
<li><code>behind</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of commits behind.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getConfigValue(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository has submodules. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the git configuration value specified by the key.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getOriginURL(</b>[path]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository has submodules. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the origin url of the repository.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getUpstreamBranch(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repo to get this information for, only needed if the repository contains submodules.</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the upstream branch for the current HEAD, or null if there
is no upstream branch for the current HEAD.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> branch name such as <code>refs/remotes/origin/master</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getReferences(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository to get this information for, only needed if the repository has submodules.</li>
</ul>

<p>Gets all the local and remote references.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:</p>
</li>
<li><p><code>heads</code>   An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of head reference names.</p>
</li>
<li><code>remotes</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of remote reference names.</li>
<li><code>tags</code>    An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of tag reference names.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getReferenceTarget(</b>reference, path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>reference</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> reference to get the target of.</li>
<li><code>path</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repo to get the reference target for. Only needed if the repository contains submodules. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the current <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> SHA for the given reference.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPathModified(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns true if the given path is modified.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the <code>path</code> is modified.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPathNew(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns true if the given path is new.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the <code>path</code> is new.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPathIgnored(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>

<p>Is the given path ignored?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the <code>path</code> is ignored.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getDirectoryStatus(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>

<p>Get the status of a directory in the repository&#x27;s working directory.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the status. This value can be passed to
{::isStatusModified} or {::isStatusNew} to get more information.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPathStatus(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the status of a single path in the repository.</p>
<p>&#x60;path&#x60; A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> repository-relative path.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the status. This value can be passed to
{::isStatusModified} or {::isStatusNew} to get more information.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCachedPathStatus(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path in the repository, relative or absolute.</li>
</ul>

<p>Get the cached status for the given path.</p>

<em>Returns</em>
<ul>
<li>Returns a status <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> or null if the path is not in the cache.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isStatusModified(</b>status<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>status</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the status.</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns true if the given status indicates modification.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the <code>status</code> indicates modification.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isStatusNew(</b>status<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>status</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the status.</li>
</ul>


<em>Returns</em>
<ul>
<li>Returns true if the given status indicates a new path.</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the <code>status</code> indicates a new path.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getDiffStats(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to check.</li>
</ul>

<p>Retrieves the number of lines added and removed to a path.</p>
<p>This compares the working directory contents of the path to the &#x60;HEAD&#x60;
version.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:</p>
</li>
<li><p><code>added</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of added lines.</p>
</li>
<li><code>deleted</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of deleted lines.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLineDiffs(</b>path, text<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path relative to the repository.</li>
<li><code>text</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to compare against the <code>HEAD</code> contents</li>
</ul>

<p>Retrieves the line diffs comparing the &#x60;HEAD&#x60; version of the given
path and the given text.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of hunk <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>s with the following keys:</p>
</li>
<li><p><code>oldStart</code> The line <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of the old hunk.</p>
</li>
<li><code>newStart</code> The line <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of the new hunk.</li>
<li><code>oldLines</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of lines in the old hunk.</li>
<li><code>newLines</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of lines in the new hunk</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>checkoutHead(</b>path<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>path</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to checkout.</li>
</ul>

<p>Restore the contents of a path in the working directory and index
to the version at &#x60;HEAD&#x60;.</p>
<p>This is essentially the same as running:</p>
<p>&#x60;&#x60;&#x60;sh
  git reset HEAD -- &lt;path&gt;
  git checkout HEAD -- &lt;path&gt;
&#x60;&#x60;&#x60;</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that&#39;s true if the method was successful.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>checkoutReference(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>reference</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> reference to checkout.</li>
<li><code>create</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> value which, if true creates the new reference if it doesn&#39;t exist.</li>
</ul>

<p>Checks out a branch in your repository.</p>

<em>Returns</em>
<ul>
<li>Returns a Boolean that&#39;s true if the method was successful.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-GrammarRegistry">GrammarRegistry</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Syntax class holding the grammars used for tokenizing.</p>
<p>An instance of this class is always available as the &#x60;atom.grammars&#x60; global.</p>
<p>The Syntax class also contains properties for things such as the
language-specific comment regexes. See {::getProperty} for more details. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>selectGrammar(</b>filePath, fileContents<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>filePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> file path.</li>
<li><code>fileContents</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> of text for the file path.</li>
</ul>

<p>Select a grammar for the given file path and file contents.</p>
<p>This picks the best match by checking the file path and contents against
each grammar.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Grammar}`, never null.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getGrammarScore(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing how well the grammar matches the
<code>filePath</code> and <code>contents</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>grammarOverrideForPath(</b>filePath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>filePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> file path.</li>
</ul>

<p>Get the grammar override for the given file path.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Grammar}` or .</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setGrammarOverrideForPath(</b>filePath, scopeName<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>filePath</code> A non-empty <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> file path.</li>
<li><code>scopeName</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> such as <code>&quot;source.js&quot;</code>.</li>
</ul>

<p>Set the grammar override for the given file path.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Grammar}` or .</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clearGrammarOverrideForPath(</b>filePath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>filePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> file path.</li>
</ul>

<p>Remove the grammar override for the given file path.</p>

<em>Returns</em>
<ul>
<li>Returns .</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clearGrammarOverrides(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Remove all grammar overrides.</p>

<em>Returns</em>
<ul>
<li>Returns .</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Gutter">Gutter</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents a gutter within a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.</p>
<p>See {TextEditor::addGutter} for information on creating a gutter. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Destroys the gutter. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeVisible(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>gutter</code> The gutter whose visibility changed.</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the gutter&#x27;s visibility changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the gutter is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>hide(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Hide the gutter. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>show(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Show the gutter. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isVisible(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Determine whether the gutter is visible.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>decorateMarker(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>marker</code> A `{DisplayMarker}` you want this decoration to follow.</li>
<li><code>decorationParams</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> representing the decoration. It is passed to {TextEditor::decorateMarker} as its <code>decorationParams</code> and so supports all options documented there.<ul>
<li><code>type</code> <strong>Caveat</strong>: set to <code>&#39;line-number&#39;</code> if this is the line-number gutter, <code>&#39;gutter&#39;</code> otherwise. This cannot be overridden.</li>
</ul>
</li>
</ul>

<p>Add a decoration that tracks a `{DisplayMarker}`. When the marker moves,
is invalidated, or is destroyed, the decoration will be updated to reflect
the marker&#x27;s state.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> object</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-LayerDecoration">LayerDecoration</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents a decoration that applies to every marker on a given
layer. Created via {TextEditor::decorateMarkerLayer}. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Destroys the decoration. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isDestroyed(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Determine whether this decoration is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getProperties(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get this decoration&#x27;s properties.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setProperties(</b>newProperties<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>newProperties</code> See {TextEditor::decorateMarker} for more information on the properties. The <code>type</code> of <code>gutter</code> and <code>overlay</code> are not supported on layer decorations. </li>
</ul>

<p>Set this decoration&#x27;s properties.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setPropertiesForMarker(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>marker</code> The `{DisplayMarker}` or `{Marker}` for which to override properties.</li>
<li><code>properties</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing properties to apply to this marker. Pass <code>null</code> to clear the override. </li>
</ul>

<p>Override the decoration properties for a specific marker.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-MenuManager">MenuManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Provides a registry for menu items that you&#x27;d like to appear in the
application menu.</p>
<p>An instance of this class is always available as the &#x60;atom.menu&#x60; global.</p>
<h2 id="menu-cson-format">Menu CSON Format</h2>
<p>Here is an example from the <a href="https://github.com/atom/tree-view/blob/master/menus/tree-view.cson">tree-view</a>:</p>
<p>&#x60;&#x60;&#x60;coffee
[
  {
    &#x27;label&#x27;: &#x27;View&#x27;
    &#x27;submenu&#x27;: [
      { &#x27;label&#x27;: &#x27;Toggle Tree View&#x27;, &#x27;command&#x27;: &#x27;tree-view:toggle&#x27; }
    ]
  }
  {
    &#x27;label&#x27;: &#x27;Packages&#x27;
    &#x27;submenu&#x27;: [
      &#x27;label&#x27;: &#x27;Tree View&#x27;
      &#x27;submenu&#x27;: [
        { &#x27;label&#x27;: &#x27;Focus&#x27;, &#x27;command&#x27;: &#x27;tree-view:toggle-focus&#x27; }
        { &#x27;label&#x27;: &#x27;Toggle&#x27;, &#x27;command&#x27;: &#x27;tree-view:toggle&#x27; }
        { &#x27;label&#x27;: &#x27;Reveal Active File&#x27;, &#x27;command&#x27;: &#x27;tree-view:reveal-active-file&#x27; }
        { &#x27;label&#x27;: &#x27;Toggle Tree Side&#x27;, &#x27;command&#x27;: &#x27;tree-view:toggle-side&#x27; }
      ]
    ]
  }
]
&#x60;&#x60;&#x60;</p>
<p>Use in your package&#x27;s menu &#x60;.cson&#x60; file requires that you place your menu
structure under a &#x60;menu&#x60; key.</p>
<p>&#x60;&#x60;&#x60;coffee
&#x27;menu&#x27;: [
  {
    &#x27;label&#x27;: &#x27;View&#x27;
    &#x27;submenu&#x27;: [
      { &#x27;label&#x27;: &#x27;Toggle Tree View&#x27;, &#x27;command&#x27;: &#x27;tree-view:toggle&#x27; }
    ]
  }
]
&#x60;&#x60;&#x60;</p>
<p>See {::add} for more info about adding menu&#x27;s directly. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>add(</b>items<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>items</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of menu item <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>s containing the keys:<ul>
<li><code>label</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> menu label.</li>
<li><code>submenu</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of sub menu items.</li>
<li><code>command</code> An optional <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> command to trigger when the item is clicked.</li>
</ul>
</li>
</ul>

<p>Adds the given items to the application menu.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
added menu items.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>update(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Refreshes the currently visible menu. </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-NotificationManager">NotificationManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A notification manager used to create <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/notification.coffee#L6">{Notification}</a>s to be shown
to the user.</p>
<p>An instance of this class is always available as the &#x60;atom.notifications&#x60;
global. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidAddNotification(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called after the notification is added.<ul>
<li><code>notification</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/notification.coffee#L6">{Notification}</a> that was added.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback after a notification has been added.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addSuccess(</b>message[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>detail</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with additional details about the notification.</li>
<li><code>dismissable</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether this notification can be dismissed by the user. Defaults to <code>false</code>.</li>
<li><code>icon</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of an icon from Octicons to display in the notification header. Defaults to <code>&#39;check&#39;</code>. </li>
</ul>
</li>
</ul>

<p>Add a success notification.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addInfo(</b>message[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>detail</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with additional details about the notification.</li>
<li><code>dismissable</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether this notification can be dismissed by the user. Defaults to <code>false</code>.</li>
<li><code>icon</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of an icon from Octicons to display in the notification header. Defaults to <code>&#39;info&#39;</code>. </li>
</ul>
</li>
</ul>

<p>Add an informational notification.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addWarning(</b>message[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>detail</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with additional details about the notification.</li>
<li><code>dismissable</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether this notification can be dismissed by the user. Defaults to <code>false</code>.</li>
<li><code>icon</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of an icon from Octicons to display in the notification header. Defaults to <code>&#39;alert&#39;</code>. </li>
</ul>
</li>
</ul>

<p>Add a warning notification.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addError(</b>message[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>detail</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with additional details about the notification.</li>
<li><code>dismissable</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether this notification can be dismissed by the user. Defaults to <code>false</code>.</li>
<li><code>icon</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of an icon from Octicons to display in the notification header. Defaults to <code>&#39;flame&#39;</code>. </li>
</ul>
</li>
</ul>

<p>Add an error notification.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addFatalError(</b>message[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>detail</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with additional details about the notification.</li>
<li><code>dismissable</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether this notification can be dismissed by the user. Defaults to <code>false</code>.</li>
<li><code>icon</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of an icon from Octicons to display in the notification header. Defaults to <code>&#39;bug&#39;</code>. </li>
</ul>
</li>
</ul>

<p>Add a fatal error notification.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getNotifications(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get all the notifications.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/notification.coffee#L6">{Notification}</a>s.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Notification">Notification</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A notification to the user containing a message and type. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidDismiss(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the notification is dismissed.</li>
</ul>

<p>Invoke the given callback when the notification is dismissed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDisplay(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the notification is displayed.</li>
</ul>

<p>Invoke the given callback when the notification is displayed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getType(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> type.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getMessage(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> message.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>dismiss(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Dismisses the notification, removing it from the UI. Calling this programmatically
will call all callbacks added via &#x60;onDidDismiss&#x60;. </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-PackageManager">PackageManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Package manager for coordinating the lifecycle of Atom packages.</p>
<p>An instance of this class is always available as the &#x60;atom.packages&#x60; global.</p>
<p>Packages can be loaded, activated, and deactivated, and unloaded:</p>
<ul>
<li>Loading a package reads and parses the package&#x27;s metadata and resources
such as keymaps, menus, stylesheets, etc.</li>
<li>Activating a package registers the loaded resources and calls &#x60;activate()&#x60;
on the package&#x27;s main module.</li>
<li>Deactivating a package unregisters the package&#x27;s resources  and calls
&#x60;deactivate()&#x60; on the package&#x27;s main module.</li>
<li>Unloading a package removes it completely from the package manager.</li>
</ul>
<p>Packages can be enabled/disabled via the &#x60;core.disabledPackages&#x60; config
settings and also by calling &#x60;enablePackage()/disablePackage()&#x60;. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidLoadInitialPackages(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when all packages have been loaded.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidActivateInitialPackages(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when all packages have been activated.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidActivatePackage(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be invoked when a package is activated.<ul>
<li><code>package</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was activated.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a package is activated.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDeactivatePackage(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be invoked when a package is deactivated.<ul>
<li><code>package</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was deactivated.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a package is deactivated.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidLoadPackage(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be invoked when a package is loaded.<ul>
<li><code>package</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was loaded.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a package is loaded.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidUnloadPackage(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be invoked when a package is unloaded.<ul>
<li><code>package</code> The <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was unloaded.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a package is unloaded.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getApmPath(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the path to the apm command.</p>
<p>Uses the value of the &#x60;core.apmPath&#x60; config setting if it exists.</p>
<p>Return a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> file path to apm. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getPackageDirPaths(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the paths being used to look for packages.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> directory paths.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>resolvePackagePath(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Resolve the given package name to a path on disk.</p>
<p>Return a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> folder path or undefined if it could not be resolved. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isBundledPackage(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Is the package with the given name bundled with Atom?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>enablePackage(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Enable the package with the given name.</p>

<em>Returns</em>
<ul>
<li>Returns the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was enabled or null if it isn&#39;t loaded.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>disablePackage(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Disable the package with the given name.</p>

<em>Returns</em>
<ul>
<li>Returns the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> that was disabled or null if it isn&#39;t loaded.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPackageDisabled(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Is the package with the given name disabled?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActivePackages(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the active <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a>s. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getActivePackage(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Get the active <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> with the given name.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> or .</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPackageActive(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Is the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> with the given name active?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLoadedPackages(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the loaded <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a>s </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getLoadedPackage(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Get the loaded <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> with the given name.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/package.coffee#L16">{Package}</a> or .</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isPackageLoaded(</b>name<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>name</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> package name.</li>
</ul>

<p>Is the package with the given name loaded?</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getAvailablePackagePaths(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s of all the available package paths.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getAvailablePackageNames(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s of all the available package names.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getAvailablePackageMetadata(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s of all the available package metadata.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Package">Package</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Loads and activates a package&#x27;s main module and resources such as
stylesheets, keymaps, grammar, editor properties, and menus. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidDeactivate(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback when all packages have been activated.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isCompatible(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Are all native modules depended on by this package correctly
compiled against the current version of Atom?</p>
<p>Incompatible packages cannot be activated.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, true if compatible, false if incompatible.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>rebuild(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Rebuild native modules in this package&#x27;s dependencies for the
current version of Atom.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves with an object containing <code>code</code>,
<code>stdout</code>, and <code>stderr</code> properties based on the results of running
<code>apm rebuild</code> on the package.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBuildFailureOutput(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>If a previous rebuild failed, get the contents of stderr.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> or null if no previous build failure occurred.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Pane">Pane</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A container for presenting content in the center of the workspace.
Panes can contain multiple items, one of which is <em>active</em> at a given time.
The view corresponding to the active item is displayed in the interface. In
the default configuration, tabs are also displayed for each item.</p>
<p>Each pane may also contain one <em>pending</em> item. When a pending item is added
to a pane, it will replace the currently pending item, if any, instead of
simply being added. In the default configuration, the text in the tab for
pending items is shown in italics. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangeFlexScale(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the pane is resized<ul>
<li><code>flexScale</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the panes <code>flex-grow</code>; ability for a flex item to grow if necessary.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the pane resizes</p>
<p>The callback will be invoked when pane&#x27;s flexScale property changes.
Use {::getFlexScale} to get the current value.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which &#39;.dispose()&#39; can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeFlexScale(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with the current and future values of the {::getFlexScale} property.<ul>
<li><code>flexScale</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the panes <code>flex-grow</code>; ability for a flex item to grow if necessary.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with the current and future values of
{::getFlexScale}.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidActivate(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the pane is activated.</li>
</ul>

<p>Invoke the given callback when the pane is activated.</p>
<p>The given callback will be invoked whenever {::activate} is called on the
pane, even if it is already active at the time.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillDestroy(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called before the pane is destroyed.</li>
</ul>

<p>Invoke the given callback before the pane is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the pane is destroyed.</li>
</ul>

<p>Invoke the given callback when the pane is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeActive(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the value of the {::isActive} property changes.<ul>
<li><code>active</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the pane is active.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the value of the {::isActive}
property changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeActive(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with the current and future values of the {::isActive} property.<ul>
<li><code>active</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the pane is active.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with the current and future values of the
{::isActive} property.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with when items are added.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The added pane item.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating where the item is located.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when an item is added to the pane.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with when items are removed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The removed pane item.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating where the item was located.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when an item is removed from the pane.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillRemoveItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with when items are removed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The pane item to be removed.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating where the item is located. </li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback before an item is removed from the pane.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidMoveItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with when items are moved.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The removed pane item.</li>
<li><code>oldIndex</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating where the item was located.</li>
<li><code>newIndex</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating where the item is now located.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when an item is moved within the pane.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeItems(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with current and future items.<ul>
<li><code>item</code> An item that is present in {::getItems} at the time of subscription or that is added at some later time.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with all current and future items.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeActiveItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with when the active item changes.<ul>
<li><code>activeItem</code> The current active item.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the value of {::getActiveItem}
changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeActiveItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with the current and future active items.<ul>
<li><code>activeItem</code> The current active item.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with the current and future values of
{::getActiveItem}.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillDestroyItem(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called before items are destroyed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The item that will be destroyed.</li>
<li><code>index</code> The location of the item.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback before items are destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to
unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getItems(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the items in this pane.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActiveItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the active pane item in this pane.</p>

<em>Returns</em>
<ul>
<li>Returns a pane item.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>itemAtIndex(</b>index<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>

<p>Return the item at the given index.</p>

<em>Returns</em>
<ul>
<li>Returns an item or <code>null</code> if no item exists at the given index.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>activateNextItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Makes the next item active. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>activatePreviousItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Makes the previous item active. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveItemRight(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Move the active tab to the right. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveItemLeft(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Move the active tab to the left </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getActiveItemIndex(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the index of the active item.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>activateItemAtIndex(</b>index<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> </li>
</ul>

<p>Activate the item at the given index.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>activateItem(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>pending</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating that the item should be added in a pending state if it does not yet exist in the pane. Existing pending items in a pane are replaced with new pending items when they are opened. </li>
</ul>
</li>
</ul>

<p>Make the given item <em>active</em>, causing it to be displayed by
the pane&#x27;s view.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addItem(</b>item[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> The item to add. It can be a model with an associated view or a view.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index at which to add the item. If omitted, the item is added after the current active item.</li>
<li><code>pending</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating that the item should be added in a pending state. Existing pending items in a pane are replaced with new pending items when they are opened.</li>
</ul>
</li>
</ul>

<p>Add the given item to the pane.</p>

<em>Returns</em>
<ul>
<li>Returns the added item.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addItems(</b>items[, index]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>items</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items to add. Items can be views or models with associated views. Any objects that are already present in the pane&#39;s current items will not be added again.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> index at which to add the items. If omitted, the item is #   added after the current active item.</li>
</ul>

<p>Add the given items to the pane.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of added items.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>moveItem(</b>item, index<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> The item to move.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index to which to move the item. </li>
</ul>

<p>Move the given item to the given index.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveItemToPane(</b>item, pane, index<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> The item to move.</li>
<li><code>pane</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> to which to move the item.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index to which to move the item in the given pane. </li>
</ul>

<p>Move the given item to the given index on another pane.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>destroyActiveItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Destroy the active item and activate the next item. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>destroyItem(</b>item<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> Item to destroy </li>
</ul>

<p>Destroy the given item.</p>
<p>If the item is active, the next item will be activated. If the item is the
last item, the pane will be destroyed if the &#x60;core.destroyEmptyPanes&#x60; config
setting is &#x60;true&#x60;.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>destroyItems(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Destroy all items. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>destroyInactiveItems(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Destroy all items except for the active item. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveActiveItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Save the active item. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveActiveItemAs(</b>[nextAction]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>nextAction</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> which will be called after the item is successfully saved. </li>
</ul>

<p>Prompt the user for a location and save the active item with the
path they select.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveItem(</b>item[, nextAction]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> The item to save.</li>
<li><code>nextAction</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> which will be called with no argument after the item is successfully saved, or with the error if it failed. The return value will be that of <code>nextAction</code> or <code>undefined</code> if it was not provided </li>
</ul>

<p>Save the given item.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveItemAs(</b>item[, nextAction]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> The item to save.</li>
<li><code>nextAction</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> which will be called with no argument after the item is successfully saved, or with the error if it failed. The return value will be that of <code>nextAction</code> or <code>undefined</code> if it was not provided </li>
</ul>

<p>Prompt the user for a location and save the active item with the
path they select.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveItems(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Save all items. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>itemForURI(</b>uri<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>uri</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing a URI. </li>
</ul>

<p>Return the first item that matches the given URI or undefined if
none exists.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>activateItemForURI(</b>uri<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>uri</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing a URI.</li>
</ul>

<p>Activate the first item that matches the given URI.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether an item matching the URI was found.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isActive(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Determine whether the pane is active.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>activate(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Makes this pane the <em>active</em> pane, causing it to gain focus. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Close the pane and destroy all its items.</p>
<p>If this is the last pane, all the items will be destroyed but the pane
itself will not be destroyed. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>splitLeft(</b>[params]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>items</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items to add to the new pane.</li>
<li><code>copyActiveItem</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true will copy the active item into the new split pane</li>
</ul>
</li>
</ul>

<p>Create a new pane to the left of this pane.</p>

<em>Returns</em>
<ul>
<li>Returns the new <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>splitRight(</b>[params]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>items</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items to add to the new pane.</li>
<li><code>copyActiveItem</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true will copy the active item into the new split pane</li>
</ul>
</li>
</ul>

<p>Create a new pane to the right of this pane.</p>

<em>Returns</em>
<ul>
<li>Returns the new <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>splitUp(</b>[params]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>items</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items to add to the new pane.</li>
<li><code>copyActiveItem</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true will copy the active item into the new split pane</li>
</ul>
</li>
</ul>

<p>Creates a new pane above the receiver.</p>

<em>Returns</em>
<ul>
<li>Returns the new <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>splitDown(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>params</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>items</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items to add to the new pane.</li>
<li><code>copyActiveItem</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true will copy the active item into the new split pane</li>
</ul>
</li>
</ul>

<p>Creates a new pane below the receiver.</p>

<em>Returns</em>
<ul>
<li>Returns the new <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Panel">Panel</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A container representing a panel on the edges of the editor window.
You should not create a &#x60;Panel&#x60; directly, instead use {Workspace::addTopPanel}
and friends to add panels.</p>
<p>Examples: <a href="https://github.com/atom/tree-view">tree-view</a>,
<a href="https://github.com/atom/status-bar">status-bar</a>,
and <a href="https://github.com/atom/find-and-replace">find-and-replace</a> all use
panels. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>destroy(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Destroy and remove this panel from the UI. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeVisible(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the pane is destroyed.<ul>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true when the panel has been shown</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the pane hidden or shown.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the pane is destroyed.<ul>
<li><code>panel</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a> this panel</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the pane is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the panel&#39;s item.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPriority(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating this panel&#39;s priority.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isVisible(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> true when the panel is visible.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>hide(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Hide this panel </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>show(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Show this panel </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Project">Project</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents a project that&#x27;s opened in Atom.</p>
<p>An instance of this class is always available as the &#x60;atom.project&#x60; global. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangePaths(</b>callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called after the project paths change.<ul>
<li><code>projectPaths</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> project paths.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the project paths change.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getRepositories(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/git-repository.coffee#L44">{GitRepository}</a>s associated with the project&#x27;s
directories.</p>
<p>This method will be removed in 2.0 because it does synchronous I/O.
Prefer the following, which evaluates to a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves to an
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Repository}` objects:</p>
<p>&#x60;&#x60;&#x60;
Promise.all(atom.project.getDirectories().map(
    atom.project.repositoryForDirectory.bind(atom.project)))
&#x60;&#x60;&#x60;</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>repositoryForDirectory(</b>directory<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>directory</code> `{Directory}` for which to get a `{Repository}`.</li>
</ul>

<p>Get the repository for a given directory asynchronously.</p>

<em>Returns</em>
<ul>
<li><p>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves with either:</p>
</li>
<li><p>`{Repository}` if a repository can be created for the given directory</p>
</li>
<li><code>null</code> if no repository can be created for the given directory.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPaths(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s containing the paths of the project&#x27;s
directories. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setPaths(</b>projectPaths<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>projectPaths</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> paths. </li>
</ul>

<p>Set the paths of the project&#x27;s directories.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addPath(</b>projectPath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>projectPath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> The path to the directory to add. </li>
</ul>

<p>Add a path to the project&#x27;s list of root paths</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>removePath(</b>projectPath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>projectPath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> The path to remove. </li>
</ul>

<p>remove a path from the project&#x27;s list of root paths.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getDirectories(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Directory}`s associated with this project. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>relativizePath(</b>fullPath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>fullPath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> An absolute path.</li>
</ul>

<p>Get the path to the project directory that contains the given path,
and the relative path from that project directory to the given path.</p>

<em>Returns</em>
<ul>
<li><p>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> with two elements:</p>
</li>
<li><p><code>projectPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the project directory that contains the
given path, or <code>null</code> if none is found.</p>
</li>
<li><code>relativePath</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> The relative path from the project directory to
the given path.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>contains(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>pathToCheck</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path</li>
</ul>

<p>Determines whether the given path (real or symbolic) is inside the
project&#x27;s directory.</p>
<p>This method does not actually check if the path exists, it just checks their
locations relative to each other.</p>

<em>Returns</em>
<ul>
<li>Returns whether the path is inside the project&#39;s root directory.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-ScopeDescriptor">ScopeDescriptor</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Wraps an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of &#x60;String&#x60;s. The Array describes a path from the
root of the syntax tree to a token including <em>all</em> scope names for the entire
path.</p>
<p>Methods that take a &#x60;ScopeDescriptor&#x60; will also accept an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Strings}`
scope names e.g. &#x60;[&#x27;.source.js&#x27;]&#x60;.</p>
<p>You can use &#x60;ScopeDescriptor&#x60;s to get language-specific config settings via
{Config::get}.</p>
<p>You should not need to create a &#x60;ScopeDescriptor&#x60; directly.</p>
<ul>
<li>{Editor::getRootScopeDescriptor} to get the language&#x27;s descriptor.</li>
<li>{Editor::scopeDescriptorForBufferPosition} to get the descriptor at a
specific position in the buffer.</li>
<li>{Cursor::getScopeDescriptor} to get a cursor&#x27;s descriptor based on position.</li>
</ul>
<p>See the <a href="https://atom.io/docs/latest/behind-atom-scoped-settings-scopes-and-scope-descriptors">scopes and scope descriptor guide</a>
for more information. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>constructor(</b>object<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>object</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>scopes</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s </li>
</ul>
</li>
</ul>

<p>Create a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> object.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getScopesArray(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Selection">Selection</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents a selection in the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangeRange(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>oldBufferRange</code> `{Range}`</li>
<li><code>oldScreenRange</code> `{Range}`</li>
<li><code>newBufferRange</code> `{Range}`</li>
<li><code>newScreenRange</code> `{Range}`</li>
<li><code>selection</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> that triggered the event</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the selection was moved.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the selection was destroyed</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getScreenRange(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the screen `{Range}` for the selection.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setScreenRange(</b>screenRange[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRange</code> The new `{Range}` to use.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> options matching those found in {::setBufferRange}. </li>
</ul>

<p>Modifies the screen range for the selection.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getBufferRange(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the buffer `{Range}` for the selection.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setBufferRange(</b>bufferRange[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> The new `{Range}` to select.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the keys:<ul>
<li><code>preserveFolds</code> if <code>true</code>, the fold settings are preserved after the selection moves.</li>
<li><code>autoscroll</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to autoscroll to the new range. Defaults to <code>true</code> if this is the most recently added selection, <code>false</code> otherwise. </li>
</ul>
</li>
</ul>

<p>Modifies the buffer `{Range}` for the selection.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getBufferRowRange(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the starting and ending buffer rows the selection is
highlighting.</li>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of two <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>s: the starting row, and the ending row.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isEmpty(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Determines if the selection contains anything. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isReversed(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Determines if the ending position of a marker is greater than the
starting position.</p>
<p>This can happen when, for example, you highlight text &quot;up&quot; in a `{TextBuffer}`. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isSingleScreenLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns whether the selection is a single line or not.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getText(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the text in the selection.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>intersectsBufferRange(</b>bufferRange<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> A `{Range}` to check against.</li>
</ul>

<p>Identifies if a selection intersects with a given buffer range.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>intersectsWith(</b>otherSelection<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>otherSelection</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> to check against.</li>
</ul>

<p>Identifies if a selection intersects with another selection.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clear(</b>[options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>autoscroll</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to autoscroll to the new range. Defaults to <code>true</code> if this is the most recently added selection, <code>false</code> otherwise. </li>
</ul>
</li>
</ul>

<p>Clears the selection, moving the marker to the head.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToScreenPosition(</b>position<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> An instance of `{Point}`, with a given <code>row</code> and <code>column</code>. </li>
</ul>

<p>Selects the text from the current cursor position to a given screen
position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBufferPosition(</b>position<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> An instance of `{Point}`, with a given <code>row</code> and <code>column</code>. </li>
</ul>

<p>Selects the text from the current cursor position to a given buffer
position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectRight(</b>[columnCount]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to select (default: 1) </li>
</ul>

<p>Selects the text one position right of the cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectLeft(</b>[columnCount]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to select (default: 1) </li>
</ul>

<p>Selects the text one position left of the cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectUp(</b>[rowCount]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to select (default: 1) </li>
</ul>

<p>Selects all the text one position above the cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectDown(</b>[rowCount]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to select (default: 1) </li>
</ul>

<p>Selects all the text one position below the cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToTop(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the top of
the buffer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBottom(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the bottom
of the buffer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectAll(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text in the buffer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the
beginning of the line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToFirstCharacterOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the first
character of the line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToEndOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the end of
the screen line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToEndOfBufferLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the end of
the buffer line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the
beginning of the word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToEndOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the end of
the word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfNextWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the
beginning of the next word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects text to the previous word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects text to the next word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToPreviousSubwordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects text to the previous subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToNextSubwordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects text to the next subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfNextParagraph(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the
beginning of the next paragraph. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfPreviousParagraph(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Selects all the text from the current cursor position to the
beginning of the previous paragraph. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Modifies the selection to encompass the current word.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>expandOverWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Expands the newest selection to include the entire word on which
the cursors rests. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectLine(</b>row<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>row</code> The line <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> to select (default: the row of the cursor). </li>
</ul>

<p>Selects an entire line in the buffer.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>expandOverLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Expands the newest selection to include the entire line on which
the cursor currently rests.</p>
<p>It also includes the newline character. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>insertText(</b>text[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>text</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the text to add</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with keys:<ul>
<li><code>select</code> if <code>true</code>, selects the newly added text.</li>
<li><code>autoIndent</code> if <code>true</code>, indents all inserted text appropriately.</li>
<li><code>autoIndentNewline</code> if <code>true</code>, indent newline appropriately.</li>
<li><code>autoDecreaseIndent</code> if <code>true</code>, decreases indent level appropriately (for example, when a closing bracket is inserted).</li>
<li><code>normalizeLineEndings</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> (default: true)</li>
<li><code>undo</code> if <code>skip</code>, skips the undo stack for this operation. </li>
</ul>
</li>
</ul>

<p>Replaces text at the current selection.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>backspace(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the first character before the selection if the selection
is empty otherwise it deletes the selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or, if nothing is selected, then all
characters from the start of the selection back to the previous word
boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or, if nothing is selected, then all
characters from the start of the selection up to the next word
boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes from the start of the selection to the beginning of the
current word if the selection is empty otherwise it deletes the selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes from the beginning of the line which the selection begins on
all the way through to the end of the selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>delete(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or the next character after the start of the
selection if the selection is empty. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>If the selection is empty, removes all text from the cursor to the
end of the line. If the cursor is already at the end of the line, it
removes the following newline. If the selection isn&#x27;t empty, only deletes
the contents of the selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfWord(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or all characters from the start of the
selection to the end of the current word if nothing is selected. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfSubword(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or all characters from the start of the
selection to the end of the current word if nothing is selected. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfSubword(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the selection or all characters from the start of the
selection to the end of the current word if nothing is selected. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteSelectedText(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes only the selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes the line at the beginning of the selection if the selection
is empty unless the selection spans multiple lines in which case all lines
are removed. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>joinLines(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Joins the current line with the one below it. Lines will
be separated by a single space.</p>
<p>If there selection spans more than one line, all the lines are joined together. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>outdentSelectedRows(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Removes one level of indent from the currently selected rows. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>autoIndentSelectedRows(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Sets the indentation level of all selected rows to values suggested
by the relevant grammars. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>toggleLineComments(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Wraps the selected lines in comments if they aren&#x27;t currently part
of a comment.</p>
<p>Removes the comment if they are currently wrapped in a comment. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cutToEndOfLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Cuts the selection until the end of the screen line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cutToEndOfBufferLine(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Cuts the selection until the end of the buffer line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cut(</b>maintainClipboard, fullLine<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>maintainClipboard</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> (default: false) See {::copy}</li>
<li><code>fullLine</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> (default: false) See {::copy} </li>
</ul>

<p>Copies the selection to the clipboard and then deletes it.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>copy(</b>maintainClipboard, fullLine<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>maintainClipboard</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> if <code>true</code>, a specific metadata property is created to store each content copied to the clipboard. The clipboard <code>text</code> still contains the concatenation of the clipboard with the current selection. (default: false)</li>
<li><code>fullLine</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> if <code>true</code>, the copied text will always be pasted at the beginning of the line containing the cursor, regardless of the cursor&#39;s horizontal position. (default: false) </li>
</ul>

<p>Copies the current selection to the clipboard.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>fold(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Creates a fold containing the current selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>indentSelectedRows(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>If the selection spans multiple rows, indent all of them. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addSelectionBelow(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the selection down one row. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addSelectionAbove(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Moves the selection up one row. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>merge(</b>otherSelection[, options]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>otherSelection</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> to merge with.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> options matching those found in {::setBufferRange}. </li>
</ul>

<p>Combines the given selection into this selection and then destroys
the given selection.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>compare(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>otherSelection</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> to compare against </li>
</ul>

<p>Compare this selection&#x27;s buffer range to another selection&#x27;s buffer
range.</p>
<p>See {Range::compare} for more details.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-StyleManager">StyleManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>A singleton instance of this class available via &#x60;atom.styles&#x60;,
which you can use to globally query and observe the set of active style
sheets. The &#x60;StyleManager&#x60; doesn&#x27;t add any style elements to the DOM on its
own, but is instead subscribed to by individual &#x60;&lt;atom-styles&gt;&#x60; elements,
which clone and attach style elements in different contexts. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>observeStyleElements(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called with style elements.<ul>
<li><code>styleElement</code> An <code>HTMLStyleElement</code> instance. The <code>.sheet</code> property will be null because this element isn&#39;t attached to the DOM. If you want to attach this element to the DOM, be sure to clone it first by calling <code>.cloneNode(true)</code> on it. The style element will also have the following non-standard properties:<ul>
<li><code>sourcePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing the path from which the style element was loaded.</li>
<li><code>context</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> indicating the target context of the style element.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke &#x60;callback&#x60; for all current and future style elements.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to cancel the
subscription.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddStyleElement(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called with style elements.<ul>
<li><code>styleElement</code> An <code>HTMLStyleElement</code> instance. The <code>.sheet</code> property will be null because this element isn&#39;t attached to the DOM. If you want to attach this element to the DOM, be sure to clone it first by calling <code>.cloneNode(true)</code> on it. The style element will also have the following non-standard properties:<ul>
<li><code>sourcePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing the path from which the style element was loaded.</li>
<li><code>context</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> indicating the target context of the style element.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke &#x60;callback&#x60; when a style element is added.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to cancel the
subscription.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveStyleElement(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called with style elements.<ul>
<li><code>styleElement</code> An <code>HTMLStyleElement</code> instance.</li>
</ul>
</li>
</ul>

<p>Invoke &#x60;callback&#x60; when a style element is removed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to cancel the
subscription.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidUpdateStyleElement(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is called with style elements.<ul>
<li><code>styleElement</code> An <code>HTMLStyleElement</code> instance. The <code>.sheet</code> property  will be null because this element isn&#39;t attached to the DOM. The style  element will also have the following non-standard properties:<ul>
<li><code>sourcePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing the path from which the style element was loaded.</li>
<li><code>context</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> indicating the target context of the style element.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke &#x60;callback&#x60; when an existing style element is updated.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to cancel the
subscription.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getStyleElements(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get all loaded style elements. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getUserStyleSheetPath(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the path of the user style sheet in &#x60;~/.atom&#x60;.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Task">Task</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Run a node script in a separate process.</p>
<p>Used by the fuzzy-finder and <a href="https://github.com/atom/atom/blob/master/src/scan-handler.coffee">find in project</a>.</p>
<p>For a real-world example, see the <a href="https://github.com/atom/atom/blob/master/src/scan-handler.coffee">scan-handler</a>
and the <a href="https://github.com/atom/atom/blob/4a20f13162f65afc816b512ad7201e528c3443d7/src/project.coffee#L245">instantiation of the task</a>.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>once(</b>taskPath, args<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>taskPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the CoffeeScript/JavaScript file which exports a single <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to execute.</li>
<li><code>args</code> The arguments to pass to the exported function.</li>
</ul>

<p>A helper method to easily launch and run a task once.</p>

<em>Returns</em>
<ul>
<li>Returns the created <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/task.coffee#L40">{Task}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>constructor(</b>taskPath<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>taskPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the CoffeeScript/JavaScript file that exports a single <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to execute. </li>
</ul>

<p>Creates a task. You should probably use {.once}</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>start(</b>args[, callback]<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>args</code> The arguments to pass to the function exported by this task&#39;s script.</li>
<li><code>callback</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call when the task completes. </li>
</ul>

<p>Starts the task.</p>
<p>Throws an error if this task has already been terminated or if sending a
message to the child process fails.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>send(</b>message<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>message</code> The message to send to the task. </li>
</ul>

<p>Send message to the task.</p>
<p>Throws an error if this task has already been terminated or if sending a
message to the child process fails.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>on(</b>eventName, callback<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>eventName</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> name of the event to handle.</li>
<li><code>callback</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call when the event is emitted.</li>
</ul>

<p>Call a function when an event is emitted by the child process</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` that can be used to stop listening for the event.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>once(</b>taskPath, args<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>taskPath</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path to the CoffeeScript/JavaScript file which exports a single <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to execute.</li>
<li><code>args</code> The arguments to pass to the exported function.</li>
</ul>

<p>A helper method to easily launch and run a task once.</p>

<em>Returns</em>
<ul>
<li>Returns the created <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/task.coffee#L40">{Task}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>terminate(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Forcefully stop the running task.</p>
<p>No more events are emitted once this method is called. </p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-TextEditor">TextEditor</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>This class represents all essential editing state for a single
`{TextBuffer}`, including cursor and selection positions, folds, and soft wraps.
If you&#x27;re manipulating the state of an editor, use this class. If you&#x27;re
interested in the visual appearance of editors, use `{TextEditorElement}`
instead.</p>
<p>A single `{TextBuffer}` can belong to multiple editors. For example, if the
same file is open in two different panes, Atom creates a separate editor for
each pane. If the buffer is manipulated the changes are reflected in both
editors, but each maintains its own cursor position, folded lines, etc.</p>
<h2 id="accessing-texteditor-instances">Accessing TextEditor Instances</h2>
<p>The easiest way to get hold of &#x60;TextEditor&#x60; objects is by registering a callback
with &#x60;::observeTextEditors&#x60; on the &#x60;atom.workspace&#x60; global. Your callback will
then be called with all current editor instances and also when any editor is
created in the future.</p>
<p>&#x60;&#x60;&#x60;coffee
atom.workspace.observeTextEditors (editor) -&gt;
  editor.insertText(&#x27;Hello World&#x27;)
&#x60;&#x60;&#x60;</p>
<h2 id="buffer-vs-screen-coordinates">Buffer vs. Screen Coordinates</h2>
<p>Because editors support folds and soft-wrapping, the lines on screen don&#x27;t
always match the lines in the buffer. For example, a long line that soft wraps
twice renders as three lines on screen, but only represents one line in the
buffer. Similarly, if rows 5-10 are folded, then row 6 on screen corresponds
to row 11 in the buffer.</p>
<p>Your choice of coordinates systems will depend on what you&#x27;re trying to
achieve. For example, if you&#x27;re writing a command that jumps the cursor up or
down by 10 lines, you&#x27;ll want to use screen coordinates because the user
probably wants to skip lines <em>on screen</em>. However, if you&#x27;re writing a package
that jumps between method definitions, you&#x27;ll want to work in buffer
coordinates.</p>
<p><strong>When in doubt, just default to buffer coordinates</strong>, then experiment with
soft wraps and folds to ensure your code interacts with them correctly. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangeTitle(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the buffer&#x27;s title has changed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangePath(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the buffer&#x27;s path, and therefore title, has changed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChange(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke the given callback synchronously when the content of the
buffer changes.</p>
<p>Because observers are invoked synchronously, it&#x27;s important not to perform
any expensive operations via this method. Consider {::onDidStopChanging} to
delay expensive operations until after changes stop occurring.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidStopChanging(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Invoke &#x60;callback&#x60; when the buffer&#x27;s contents change. It is
emit asynchronously 300ms after the last buffer change. This is a good place
to handle changes to the buffer without compromising typing performance.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeCursorPosition(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>oldBufferPosition</code> `{Point}`</li>
<li><code>oldScreenPosition</code> `{Point}`</li>
<li><code>newBufferPosition</code> `{Point}`</li>
<li><code>newScreenPosition</code> `{Point}`</li>
<li><code>textChanged</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
<li><code>cursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> that triggered the event</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> is moved. If there are
multiple cursors, your callback will be called for each cursor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeSelectionRange(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>oldBufferRange</code> `{Range}`</li>
<li><code>oldScreenRange</code> `{Range}`</li>
<li><code>newBufferRange</code> `{Range}`</li>
<li><code>newScreenRange</code> `{Range}`</li>
<li><code>selection</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> that triggered the event</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a selection&#x27;s screen range changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeSoftWrapped(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when soft wrap was enabled or disabled.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeEncoding(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the buffer&#x27;s encoding has changed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeGrammar(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>grammar</code> `{Grammar}`</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the grammar that interprets and
colorizes the text has been changed. Immediately calls your callback with
the current grammar.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeGrammar(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>grammar</code> `{Grammar}`</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the grammar that interprets and
colorizes the text has been changed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeModified(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the result of {::isModified} changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidConflict(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a></li>
</ul>

<p>Calls your &#x60;callback&#x60; when the buffer&#x27;s underlying file changes on
disk at a moment when the result of {::isModified} is true.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillInsertText(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> event <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>text</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> text to be inserted</li>
<li><code>cancel</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> Call to prevent the text from being inserted</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; before text has been inserted.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidInsertText(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>event</code> event <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>text</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> text to be inserted</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; after text has been inserted.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidSave(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called after the buffer is saved.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>path</code> The path to which the buffer was saved.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback after the buffer is saved to disk.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroy(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the editor is destroyed.</li>
</ul>

<p>Invoke the given callback when the editor is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeCursors(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>cursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> that was added</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> is added to the editor.
Immediately calls your callback for each existing cursor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddCursor(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>cursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> that was added</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> is added to the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveCursor(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>cursor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> that was removed</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> is removed from the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeSelections(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>selection</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> that was added</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> is added to the editor.
Immediately calls your callback for each existing selection.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddSelection(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>selection</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> that was added</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> is added to the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveSelection(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>selection</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> that was removed</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> is removed from the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeDecorations(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>decoration</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a></li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; with each <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> added to the editor.
Calls your &#x60;callback&#x60; immediately for any existing decorations.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddDecoration(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>decoration</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> that was added</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> is added to the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveDecoration(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>decoration</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> that was removed</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> is removed from the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangePlaceholderText(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>placeholderText</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> new text</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when the placeholder text is changed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBuffer(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Retrieves the current `{TextBuffer}`. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>observeGutters(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>gutter</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> that currently exists/was added.</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> is added to the editor.
Immediately calls your callback for each existing gutter.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddGutter(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>gutter</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> that was added.</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> is added to the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidRemoveGutter(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a><ul>
<li><code>name</code> The name of the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> that was removed.</li>
</ul>
</li>
</ul>

<p>Calls your &#x60;callback&#x60; when a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a> is removed from the editor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getTitle(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the editor&#x27;s title for display in other parts of the
UI such as the tabs.</p>
<p>If the editor&#x27;s buffer is saved, its title is the file name. If it is
unsaved, its title is &quot;untitled&quot;.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLongTitle(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get unique title for display in other parts of the UI, such as
the window title.</p>
<p>If the editor&#x27;s buffer is unsaved, its title is &quot;untitled&quot;
If the editor&#x27;s buffer is saved, its unique title is formatted as one
of the following,</p>
<ul>
<li>&quot;&lt;filename&gt;&quot; when it is the only editing buffer with this file name.</li>
<li>&quot;&lt;filename&gt; — &lt;unique-dir-prefix&gt;&quot; when other buffers have this file name.</li>
</ul>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPath(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path of this editor&#39;s text buffer.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getEncoding(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> character set encoding of this editor&#39;s text
buffer.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setEncoding(</b>encoding<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>encoding</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> character set encoding name such as &#39;utf8&#39; </li>
</ul>

<p>Set the character set encoding to use in this editor&#x27;s text
buffer.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isModified(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> <code>true</code> if this editor has been modified.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isEmpty(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> <code>true</code> if this editor has no content.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>save(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Saves the editor&#x27;s text buffer.</p>
<p>See {TextBuffer::save} for more details. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>saveAs(</b>filePath<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>filePath</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> path. </li>
</ul>

<p>Saves the editor&#x27;s text buffer as the given path.</p>
<p>See {TextBuffer::saveAs} for more details.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the entire contents of the editor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getTextInBufferRange(</b>range<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>.</li>
</ul>

<p>Get the text in the given `{Range}` in buffer coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLineCount(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the number of lines in the buffer.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getScreenLineCount(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the number of screen lines in the
editor. This accounts for folds.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLastBufferRow(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the last zero-indexed buffer row
number of the editor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLastScreenRow(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing the last zero-indexed screen row
number of the editor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>lineTextForBufferRow(</b>bufferRow<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing a zero-indexed buffer row. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the contents of the line at the
given buffer row.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>lineTextForScreenRow(</b>screenRow<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> representing a zero-indexed screen row. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the contents of the line at the
given screen row.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCurrentParagraphBufferRange(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the `{Range}` of the paragraph surrounding the most recently added
cursor.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setText(</b>text<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>text</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to replace with </li>
</ul>

<p>Replaces the entire contents of the buffer with the given <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setTextInBufferRange(</b>range, text[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>.</li>
<li><code>text</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a></li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>normalizeLineEndings</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> (default: true)</li>
<li><code>undo</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> &#39;skip&#39; will skip the undo system</li>
</ul>
</li>
</ul>

<p>Set the text in the given `{Range}` in buffer coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns the `{Range}` of the newly-inserted text.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>insertText(</b>text[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>text</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the text to insert.</li>
<li><code>options</code> See {Selection::insertText}.</li>
</ul>

<p>For each selection, replace the selected text with the given text.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}` when the text has been inserted</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false when the text has not been inserted</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>insertNewline(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, replace the selected text with a newline. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>delete(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete the character
following the cursor. Otherwise delete the selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>backspace(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete the character
preceding the cursor. Otherwise delete the selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>mutateSelectedText(</b>fn<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>fn</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that will be called once for each <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>. The first    argument will be a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a> and the second argument will be the    <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> index of that selection. </li>
</ul>

<p>Mutate the text of all the selections in a single transaction.</p>
<p>All the changes made inside the given <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> can be reverted with a
single call to {::undo}.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>transpose(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, transpose the selected text.</p>
<p>If the selection is empty, the characters preceding and following the cursor
are swapped. Otherwise, the selected characters are reversed. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>upperCase(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Convert the selected text to upper case.</p>
<p>For each selection, if the selection is empty, converts the containing word
to upper case. Otherwise convert the selected text to upper case. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>lowerCase(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Convert the selected text to lower case.</p>
<p>For each selection, if the selection is empty, converts the containing word
to upper case. Otherwise convert the selected text to upper case. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>toggleLineCommentsInSelection(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Toggle line comments for rows intersecting selections.</p>
<p>If the current grammar doesn&#x27;t support comments, does nothing. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>insertNewlineBelow(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each cursor, insert a newline at beginning the following line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>insertNewlineAbove(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each cursor, insert a newline at the end of the preceding line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete all characters
of the containing word that precede the cursor. Otherwise delete the
selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Similar to {::deleteToBeginningOfWord}, but deletes only back to the
previous word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Similar to {::deleteToEndOfWord}, but deletes only up to the
next word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfSubword(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete all characters
of the containing subword following the cursor. Otherwise delete the selected
text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfSubword(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete all characters
of the containing subword following the cursor. Otherwise delete the selected
text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete all characters
of the containing line that precede the cursor. Otherwise delete the
selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfLine(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is not empty, deletes the
selection; otherwise, deletes all characters of the containing line
following the cursor. If the cursor is already at the end of the line,
deletes the following newline. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteToEndOfWord(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, delete all characters
of the containing word following the cursor. Otherwise delete the selected
text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>deleteLine(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Delete all lines intersecting selections. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>undo(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Undo the last change. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>redo(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Redo the last change. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>transact(</b>[groupingInterval], fn<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>groupingInterval</code> The <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> of milliseconds for which this transaction should be considered &#39;groupable&#39; after it begins. If a transaction with a positive <code>groupingInterval</code> is committed while the previous transaction is still &#39;groupable&#39;, the two transactions are merged with respect to undo and redo.</li>
<li><code>fn</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to call inside the transaction. </li>
</ul>

<p>Batch multiple operations as a single undo/redo step.</p>
<p>Any group of operations that are logically grouped from the perspective of
undoing and redoing should be performed in a transaction. If you want to
abort the transaction, call {::abortTransaction} to terminate the function&#x27;s
execution and revert any changes performed up to the abortion.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>abortTransaction(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Abort an open transaction, undoing any operations performed so far
within the transaction. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>createCheckpoint(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Create a pointer to the current state of the buffer for use
with {::revertToCheckpoint} and {::groupChangesSinceCheckpoint}.</p>

<em>Returns</em>
<ul>
<li>Returns a checkpoint value.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>revertToCheckpoint(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Revert the buffer to the state it was in when the given
checkpoint was created.</p>
<p>The redo stack will be empty following this operation, so changes since the
checkpoint will be lost. If the given checkpoint is no longer present in the
undo history, no changes will be made to the buffer and this method will
return &#x60;false&#x60;.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the operation succeeded.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>groupChangesSinceCheckpoint(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Group all changes since the given checkpoint into a single
transaction for purposes of undo/redo.</p>
<p>If the given checkpoint is no longer present in the undo history, no
grouping will be performed and this method will return &#x60;false&#x60;.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether the operation succeeded.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>screenPositionForBufferPosition(</b>bufferPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of [row, column].</li>
<li><code>options</code> An options hash for {::clipScreenPosition}.</li>
</ul>

<p>Convert a position in buffer-coordinates to screen-coordinates.</p>
<p>The position is clipped via {::clipBufferPosition} prior to the conversion.
The position is also clipped via {::clipScreenPosition} following the
conversion, which only makes a difference when &#x60;options&#x60; are supplied.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>bufferPositionForScreenPosition(</b>bufferPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of [row, column].</li>
<li><code>options</code> An options hash for {::clipScreenPosition}.</li>
</ul>

<p>Convert a position in screen-coordinates to buffer-coordinates.</p>
<p>The position is clipped via {::clipScreenPosition} prior to the conversion.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>screenRangeForBufferRange(</b>bufferRange<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> `{Range}` in buffer coordinates to translate into screen coordinates.</li>
</ul>

<p>Convert a range in buffer-coordinates to screen-coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>bufferRangeForScreenRange(</b>screenRange<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRange</code> `{Range}` in screen coordinates to translate into buffer coordinates.</li>
</ul>

<p>Convert a range in screen-coordinates to buffer-coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clipBufferPosition(</b>bufferPosition<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> The `{Point}` representing the position to clip.</li>
</ul>

<p>Clip the given `{Point}` to a valid position in the buffer.</p>
<p>If the given `{Point}` describes a position that is actually reachable by the
cursor based on the current contents of the buffer, it is returned
unchanged. If the `{Point}` does not describe a valid position, the closest
valid position is returned instead.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clipBufferRange(</b>range<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> The `{Range}` to clip.</li>
</ul>

<p>Clip the start and end of the given range to valid positions in the
buffer. See {::clipBufferPosition} for more information.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clipScreenPosition(</b>screenPosition[, options]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenPosition</code> The `{Point}` representing the position to clip.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>clipDirection</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> If <code>&#39;backward&#39;</code>, returns the first valid position preceding an invalid position. If <code>&#39;forward&#39;</code>, returns the first valid position following an invalid position. If <code>&#39;closest&#39;</code>, returns the first valid position closest to an invalid position. Defaults to <code>&#39;closest&#39;</code>.</li>
</ul>
</li>
</ul>

<p>Clip the given `{Point}` to a valid position on screen.</p>
<p>If the given `{Point}` describes a position that is actually reachable by the
cursor based on the current contents of the screen, it is returned
unchanged. If the `{Point}` does not describe a valid position, the closest
valid position is returned instead.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>clipScreenRange(</b>range[, options]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> The `{Range}` to clip.</li>
<li><code>options</code> See {::clipScreenPosition} <code>options</code>.</li>
</ul>

<p>Clip the start and end of the given range to valid positions on screen.
See {::clipScreenPosition} for more information.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>decorateMarker(</b>marker, decorationParams<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>marker</code> A `{DisplayMarker}` you want this decoration to follow.</li>
<li><code>decorationParams</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> representing the decoration e.g. <code>{type: &#39;line-number&#39;, class: &#39;linter-error&#39;}</code><ul>
<li><code>type</code> There are several supported decoration types. The behavior of the types are as follows:<ul>
<li><code>line</code> Adds the given <code>class</code> to the lines overlapping the rows  spanned by the <code>DisplayMarker</code>.</li>
<li><code>line-number</code> Adds the given <code>class</code> to the line numbers overlapping the rows spanned by the <code>DisplayMarker</code>.</li>
<li><code>highlight</code> Creates a <code>.highlight</code> div with the nested class with up to 3 nested regions that fill the area spanned by the <code>DisplayMarker</code>.</li>
<li><code>overlay</code> Positions the view associated with the given item at the head or tail of the given <code>DisplayMarker</code>, depending on the <code>position</code> property.</li>
<li><code>gutter</code> Tracks a `{DisplayMarker}` in a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>. Created by calling {Gutter::decorateMarker} on the desired <code>Gutter</code> instance.</li>
<li><code>block</code> Positions the view associated with the given item before or after the row of the given <code>TextEditorMarker</code>, depending on the <code>position</code> property.</li>
</ul>
</li>
<li><code>class</code> This CSS class will be applied to the decorated line number, line, highlight, or overlay.</li>
<li><code>item</code> An `{HTMLElement}` or a model <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with a corresponding view registered. Only applicable to the <code>gutter</code>, <code>overlay</code> and <code>block</code> types.</li>
<li><code>onlyHead</code> If <code>true</code>, the decoration will only be applied to the head of the <code>DisplayMarker</code>. Only applicable to the <code>line</code> and <code>line-number</code> types.</li>
<li><code>onlyEmpty</code> If <code>true</code>, the decoration will only be applied if the associated <code>DisplayMarker</code> is empty. Only applicable to the <code>gutter</code>, <code>line</code>, and <code>line-number</code> types.</li>
<li><code>onlyNonEmpty</code> If <code>true</code>, the decoration will only be applied if the associated <code>DisplayMarker</code> is non-empty. Only applicable to the <code>gutter</code>, <code>line</code>, and <code>line-number</code> types.</li>
<li><code>position</code> Only applicable to decorations of type <code>overlay</code> and <code>block</code>, controls where the view is positioned relative to the <code>TextEditorMarker</code>. Values can be <code>&#39;head&#39;</code> (the default) or <code>&#39;tail&#39;</code> for overlay decorations, and <code>&#39;before&#39;</code> (the default) or <code>&#39;after&#39;</code> for block decorations.</li>
</ul>
</li>
</ul>

<p>Add a decoration that tracks a `{DisplayMarker}`. When the
marker moves, is invalidated, or is destroyed, the decoration will be
updated to reflect the marker&#x27;s state.</p>
<p>The following are the supported decorations types:</p>
<ul>
<li><strong>line</strong>: Adds your CSS &#x60;class&#x60; to the line nodes within the range
  marked by the marker</li>
<li><strong>line-number</strong>: Adds your CSS &#x60;class&#x60; to the line number nodes within the
  range marked by the marker</li>
<li><strong>highlight</strong>: Adds a new highlight div to the editor surrounding the
  range marked by the marker. When the user selects text, the selection is
  visualized with a highlight decoration internally. The structure of this
  highlight will be
&#x60;&#x60;&#x60;html
  &lt;div class&#x3D;&quot;highlight &lt;your-class&gt;&quot;&gt;<pre><code>&amp;lt;!-- Will be one region for each row in the range. Spans 2 lines? There will be 2 regions. --&amp;gt;
&amp;lt;div class&amp;#x3D;&amp;quot;region&amp;quot;&amp;gt;&amp;lt;/div&amp;gt;
</code></pre>  &lt;/div&gt;
&#x60;&#x60;&#x60;</li>
<li><strong>overlay</strong>: Positions the view associated with the given item at the head
  or tail of the given &#x60;DisplayMarker&#x60;.</li>
<li><strong>gutter</strong>: A decoration that tracks a `{DisplayMarker}` in a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>. Gutter
  decorations are created by calling {Gutter::decorateMarker} on the
  desired &#x60;Gutter&#x60; instance.</li>
<li><strong>block</strong>: Positions the view associated with the given item before or
  after the row of the given &#x60;TextEditorMarker&#x60;.</li>
</ul>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a> object</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>decorateMarkerLayer(</b>markerLayer, decorationParams<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>markerLayer</code> A `{DisplayMarkerLayer}` or `{MarkerLayer}` to decorate.</li>
<li><code>decorationParams</code> The same parameters that are passed to {TextEditor::decorateMarker}, except the <code>type</code> cannot be <code>overlay</code> or <code>gutter</code>.</li>
</ul>

<p>Add a decoration to every marker in the given marker layer. Can
be used to decorate a large number of markers without having to create and
manage many individual decorations.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/layer-decoration.coffee#L9">{LayerDecoration}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getDecorations(</b>[propertyFilter]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>propertyFilter</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing key value pairs that the returned decorations&#39; properties must match.</li>
</ul>

<p>Get all decorations.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLineDecorations(</b>[propertyFilter]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>propertyFilter</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing key value pairs that the returned decorations&#39; properties must match.</li>
</ul>

<p>Get all decorations of type &#x27;line&#x27;.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLineNumberDecorations(</b>[propertyFilter]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>propertyFilter</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing key value pairs that the returned decorations&#39; properties must match.</li>
</ul>

<p>Get all decorations of type &#x27;line-number&#x27;.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getHighlightDecorations(</b>[propertyFilter]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>propertyFilter</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing key value pairs that the returned decorations&#39; properties must match.</li>
</ul>

<p>Get all decorations of type &#x27;highlight&#x27;.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getOverlayDecorations(</b>[propertyFilter]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>propertyFilter</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing key value pairs that the returned decorations&#39; properties must match.</li>
</ul>

<p>Get all decorations of type &#x27;overlay&#x27;.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/decoration.coffee#L37">{Decoration}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>markBufferRange(</b>range, properties<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a></li>
<li><code>properties</code> A hash of key-value pairs to associate with the marker. There are also reserved property names that have marker-specific meaning.<ul>
<li><code>maintainHistory</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> Whether to store this marker&#39;s range before and after each change in the undo history. This allows the marker&#39;s position to be restored more accurately for certain undo/redo operations, but uses more time and memory. (default: false)</li>
<li><code>reversed</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> Creates the marker in a reversed orientation. (default: false)</li>
<li><code>invalidate</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Determines the rules by which changes to the buffer <em>invalidate</em> the marker. (default: &#39;overlap&#39;) It can be any of the following strategies, in order of fragility:</li>
</ul>
</li>
<li><strong>never</strong>: The marker is never marked as invalid. This is a good choice for
markers representing selections in an editor.</li>
<li><strong>surround</strong>: The marker is invalidated by changes that completely surround it.</li>
<li><strong>overlap</strong>: The marker is invalidated by changes that surround the
start or end of the marker. This is the default.</li>
<li><strong>inside</strong>: The marker is invalidated by changes that extend into the
inside of the marker. Changes that end at the marker&#39;s start or
start at the marker&#39;s end do not invalidate the marker.</li>
<li><strong>touch</strong>: The marker is invalidated by a change that touches the marked
region in any way, including changes that end at the marker&#39;s
start or start at the marker&#39;s end. This is the most fragile strategy.</li>
</ul>

<p>Create a marker on the default marker layer with the given range
in buffer coordinates. This marker will maintain its logical location as the
buffer is changed, so if you mark a particular word, the marker will remain
over that word even if the word&#x27;s location in the buffer changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarker}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>markScreenRange(</b>range, properties<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>range</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a></li>
<li><code>properties</code> A hash of key-value pairs to associate with the marker. There are also reserved property names that have marker-specific meaning.<ul>
<li><code>maintainHistory</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> Whether to store this marker&#39;s range before and after each change in the undo history. This allows the marker&#39;s position to be restored more accurately for certain undo/redo operations, but uses more time and memory. (default: false)</li>
<li><code>reversed</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> Creates the marker in a reversed orientation. (default: false)</li>
<li><code>invalidate</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Determines the rules by which changes to the buffer <em>invalidate</em> the marker. (default: &#39;overlap&#39;) It can be any of the following strategies, in order of fragility:</li>
</ul>
</li>
<li><strong>never</strong>: The marker is never marked as invalid. This is a good choice for
markers representing selections in an editor.</li>
<li><strong>surround</strong>: The marker is invalidated by changes that completely surround it.</li>
<li><strong>overlap</strong>: The marker is invalidated by changes that surround the
start or end of the marker. This is the default.</li>
<li><strong>inside</strong>: The marker is invalidated by changes that extend into the
inside of the marker. Changes that end at the marker&#39;s start or
start at the marker&#39;s end do not invalidate the marker.</li>
<li><strong>touch</strong>: The marker is invalidated by a change that touches the marked
region in any way, including changes that end at the marker&#39;s
start or start at the marker&#39;s end. This is the most fragile strategy.</li>
</ul>

<p>Create a marker on the default marker layer with the given range
in screen coordinates. This marker will maintain its logical location as the
buffer is changed, so if you mark a particular word, the marker will remain
over that word even if the word&#x27;s location in the buffer changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarker}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>markBufferPosition(</b>bufferPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> A `{Point}` or point-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a></li>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>invalidate</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Determines the rules by which changes to the buffer <em>invalidate</em> the marker. (default: &#39;overlap&#39;) It can be any of the following strategies, in order of fragility:</li>
</ul>
</li>
<li><strong>never</strong>: The marker is never marked as invalid. This is a good choice for
markers representing selections in an editor.</li>
<li><strong>surround</strong>: The marker is invalidated by changes that completely surround it.</li>
<li><strong>overlap</strong>: The marker is invalidated by changes that surround the
start or end of the marker. This is the default.</li>
<li><strong>inside</strong>: The marker is invalidated by changes that extend into the
inside of the marker. Changes that end at the marker&#39;s start or
start at the marker&#39;s end do not invalidate the marker.</li>
<li><strong>touch</strong>: The marker is invalidated by a change that touches the marked
region in any way, including changes that end at the marker&#39;s
start or start at the marker&#39;s end. This is the most fragile strategy.</li>
</ul>

<p>Create a marker on the default marker layer with the given buffer
position and no tail. To group multiple markers together in their own
private layer, see {::addMarkerLayer}.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarker}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>markScreenPosition(</b>screenPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenPosition</code> A `{Point}` or point-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a></li>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>invalidate</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> Determines the rules by which changes to the buffer <em>invalidate</em> the marker. (default: &#39;overlap&#39;) It can be any of the following strategies, in order of fragility:</li>
</ul>
</li>
<li><strong>never</strong>: The marker is never marked as invalid. This is a good choice for
markers representing selections in an editor.</li>
<li><strong>surround</strong>: The marker is invalidated by changes that completely surround it.</li>
<li><strong>overlap</strong>: The marker is invalidated by changes that surround the
start or end of the marker. This is the default.</li>
<li><strong>inside</strong>: The marker is invalidated by changes that extend into the
inside of the marker. Changes that end at the marker&#39;s start or
start at the marker&#39;s end do not invalidate the marker.</li>
<li><strong>touch</strong>: The marker is invalidated by a change that touches the marked
region in any way, including changes that end at the marker&#39;s
start or start at the marker&#39;s end. This is the most fragile strategy.<ul>
<li><code>clipDirection</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> If <code>&#39;backward&#39;</code>, returns the first valid position preceding an invalid position. If <code>&#39;forward&#39;</code>, returns the first valid position following an invalid position. If <code>&#39;closest&#39;</code>, returns the first valid position closest to an invalid position. Defaults to <code>&#39;closest&#39;</code>.</li>
</ul>
</li>
</ul>

<p>Create a marker on the default marker layer with the given screen
position and no tail. To group multiple markers together in their own
private layer, see {::addMarkerLayer}.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarker}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>findMarkers(</b>properties<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>properties</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing properties that each returned marker must satisfy. Markers can be associated with custom properties, which are compared with basic equality. In addition, several reserved properties can be used to filter markers based on their current range:<ul>
<li><code>startBufferRow</code> Only include markers starting at this row in buffer   coordinates.</li>
<li><code>endBufferRow</code> Only include markers ending at this row in buffer   coordinates.</li>
<li><code>containsBufferRange</code> Only include markers containing this `{Range}` or   in range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> in buffer coordinates.</li>
<li><code>containsBufferPosition</code> Only include markers containing this `{Point}`   or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code> in buffer coordinates.</li>
</ul>
</li>
</ul>

<p>Find all `{DisplayMarker}`s on the default marker layer that
match the given properties.</p>
<p>This method finds markers based on the given properties. Markers can be
associated with custom properties that will be compared with basic equality.
In addition, there are several special properties that will be compared
with the range of the markers rather than their properties.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{DisplayMarker}`s</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getMarker(</b>id<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>id</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> id of the marker </li>
</ul>

<p>Get the `{DisplayMarker}` on the default layer for the given
marker id.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getMarkers(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get all `{DisplayMarker}`s on the default marker layer. Consider
using {::findMarkers} </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getMarkerCount(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the number of markers in the default marker layer.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addMarkerLayer(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing the following keys:<ul>
<li><code>maintainHistory</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether marker state should be restored on undo/redo. Defaults to <code>false</code>.</li>
<li><code>persistent</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether or not this marker layer should be serialized and deserialized along with the rest of the buffer. Defaults to <code>false</code>. If <code>true</code>, the marker layer&#39;s id will be maintained across the serialization boundary, allowing you to retrieve it via {::getMarkerLayer}.</li>
</ul>
</li>
</ul>

<p>Create a marker layer to group related markers.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarkerLayer}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getMarkerLayer(</b>id<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>id</code> The id of the marker layer to retrieve.</li>
</ul>

<p>Get a `{DisplayMarkerLayer}` by id.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarkerLayer}` or `` if no layer exists with the
given id.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getDefaultMarkerLayer(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the default `{DisplayMarkerLayer}`.</p>
<p>All marker APIs not tied to an explicit layer interact with this default
layer.</p>

<em>Returns</em>
<ul>
<li>Returns a `{DisplayMarkerLayer}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCursorBufferPosition(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the position of the most recently added cursor in buffer
coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCursorBufferPositions(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the position of all the cursor positions in buffer coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Point}`s in the order they were added</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setCursorBufferPosition(</b>position[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code></li>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing the following keys:<ul>
<li><code>autoscroll</code> Determines whether the editor scrolls to the new cursor&#39;s position. Defaults to true. </li>
</ul>
</li>
</ul>

<p>Move the cursor to the given position in buffer coordinates.</p>
<p>If there are multiple cursors, they will be consolidated to a single cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getCursorAtScreenPosition(</b>position<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code></li>
</ul>

<p>Get a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> at given screen coordinates `{Point}`</p>

<em>Returns</em>
<ul>
<li>Returns the first matched <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a> or</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCursorScreenPosition(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the position of the most recently added cursor in screen
coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Point}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCursorScreenPositions(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the position of all the cursor positions in screen coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Point}`s in the order the cursors were added</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setCursorScreenPosition(</b>position[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code></li>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> combining options for {::clipScreenPosition} with:<ul>
<li><code>autoscroll</code> Determines whether the editor scrolls to the new cursor&#39;s position. Defaults to true. </li>
</ul>
</li>
</ul>

<p>Move the cursor to the given position in screen coordinates.</p>
<p>If there are multiple cursors, they will be consolidated to a single cursor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addCursorAtBufferPosition(</b>bufferPosition<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code></li>
</ul>

<p>Add a cursor at the given position in buffer coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addCursorAtScreenPosition(</b>screenPosition<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenPosition</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <code>[row, column]</code></li>
</ul>

<p>Add a cursor at the position in screen coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>hasMultipleCursors(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether or not there are multiple cursors.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>moveUp(</b>[lineCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>lineCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of lines to move </li>
</ul>

<p>Move every cursor up one row in screen coordinates.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveDown(</b>[lineCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>lineCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of lines to move </li>
</ul>

<p>Move every cursor down one row in screen coordinates.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveLeft(</b>[columnCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to move (default: 1) </li>
</ul>

<p>Move every cursor left one column.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveRight(</b>[columnCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to move (default: 1) </li>
</ul>

<p>Move every cursor right one column.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of its line in buffer coordinates. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfScreenLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of its line in screen coordinates. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToFirstCharacterOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the first non-whitespace character of its line. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the end of its line in buffer coordinates. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfScreenLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the end of its line in screen coordinates. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of its surrounding word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToEndOfWord(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the end of its surrounding word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToTop(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the top of the buffer.</p>
<p>If there are multiple cursors, they will be merged into a single cursor. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBottom(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the bottom of the buffer.</p>
<p>If there are multiple cursors, they will be merged into a single cursor. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfNextWord(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of the next word. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the previous word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the next word boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToPreviousSubwordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the previous subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToNextSubwordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the next subword boundary. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfNextParagraph(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of the next paragraph. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>moveToBeginningOfPreviousParagraph(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Move every cursor to the beginning of the previous paragraph. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getLastCursor(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns the most recently added <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getWordUnderCursor(</b>[options]<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> See {Cursor::getBeginningOfCurrentWordBufferPosition}. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the word surrounding the most recently added cursor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getCursors(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get an Array of all <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/cursor.coffee#L14">{Cursor}</a>s. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getCursorsOrderedByBufferPosition(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get all `{Cursors}`s, ordered by their position in the buffer
instead of the order in which they were added.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelectedText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the selected text of the most recently added selection.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelectedBufferRange(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the `{Range}` of the most recently added selection in buffer
coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelectedBufferRanges(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the `{Range}`s of all selections in buffer coordinates.</p>
<p>The ranges are sorted by when the selections were added. Most recent at the end.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Range}`s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setSelectedBufferRange(</b>bufferRange[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>.</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation.</li>
<li><code>preserveFolds</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, which if <code>true</code> preserves the fold settings after the selection is set. </li>
</ul>
</li>
</ul>

<p>Set the selected range in buffer coordinates. If there are multiple
selections, they are reduced to a single selection with the given range.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setSelectedBufferRanges(</b>bufferRanges[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRanges</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Range}`s or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>s.</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation.</li>
<li><code>preserveFolds</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, which if <code>true</code> preserves the fold settings after the selection is set. </li>
</ul>
</li>
</ul>

<p>Set the selected ranges in buffer coordinates. If there are multiple
selections, they are replaced by new selections with the given ranges.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getSelectedScreenRange(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the `{Range}` of the most recently added selection in screen
coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelectedScreenRanges(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the `{Range}`s of all selections in screen coordinates.</p>
<p>The ranges are sorted by when the selections were added. Most recent at the end.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Range}`s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setSelectedScreenRange(</b>screenRange[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRange</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>.</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation. </li>
</ul>
</li>
</ul>

<p>Set the selected range in screen coordinates. If there are multiple
selections, they are reduced to a single selection with the given range.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setSelectedScreenRanges(</b>screenRanges[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRanges</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of `{Range}`s or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>s.</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation. </li>
</ul>
</li>
</ul>

<p>Set the selected ranges in screen coordinates. If there are multiple
selections, they are replaced by new selections with the given ranges.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addSelectionForBufferRange(</b>bufferRange[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> A `{Range}`</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation.</li>
<li><code>preserveFolds</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, which if <code>true</code> preserves the fold settings after the selection is set.</li>
</ul>
</li>
</ul>

<p>Add a selection for the given range in buffer coordinates.</p>

<em>Returns</em>
<ul>
<li>Returns the added <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addSelectionForScreenRange(</b>screenRange[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRange</code> A `{Range}`</li>
<li><code>options</code> An options <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>:<ul>
<li><code>reversed</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to create the selection in a reversed orientation.</li>
<li><code>preserveFolds</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>, which if <code>true</code> preserves the fold settings after the selection is set. Returns the added <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>. </li>
</ul>
</li>
</ul>

<p>Add a selection for the given range in screen coordinates.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBufferPosition(</b>position<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> An instance of `{Point}`, with a given <code>row</code> and <code>column</code>. </li>
</ul>

<p>Select from the current cursor position to the given position in
buffer coordinates.</p>
<p>This method may merge selections that end up intesecting.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToScreenPosition(</b>position<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>position</code> An instance of `{Point}`, with a given <code>row</code> and <code>column</code>. </li>
</ul>

<p>Select from the current cursor position to the given position in
screen coordinates.</p>
<p>This method may merge selections that end up intesecting.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectUp(</b>[rowCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to select (default: 1)</li>
</ul>

<p>Move the cursor of each selection one character upward while
preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intesecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectDown(</b>[rowCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>rowCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of rows to select (default: 1)</li>
</ul>

<p>Move the cursor of each selection one character downward while
preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intesecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectLeft(</b>[columnCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to select (default: 1)</li>
</ul>

<p>Move the cursor of each selection one character leftward while
preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intesecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectRight(</b>[columnCount]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>columnCount</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> number of columns to select (default: 1)</li>
</ul>

<p>Move the cursor of each selection one character rightward while
preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intesecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToTop(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Select from the top of the buffer to the end of the last selection
in the buffer.</p>
<p>This method merges multiple selections into a single selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBottom(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Selects from the top of the first selection in the buffer to the end
of the buffer.</p>
<p>This method merges multiple selections into a single selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectAll(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Select all text in the buffer.</p>
<p>This method merges multiple selections into a single selection. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move the cursor of each selection to the beginning of its line
while preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intesecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToFirstCharacterOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move the cursor of each selection to the first non-whitespace
character of its line while preserving the selection&#x27;s tail position. If the
cursor is already on the first character of the line, move it to the
beginning of the line.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToEndOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Move the cursor of each selection to the end of its line while
preserving the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfWord(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Expand selections to the beginning of their containing word.</p>
<p>Operates on all selections. Moves the cursor to the beginning of the
containing word while preserving the selection&#x27;s tail position. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToEndOfWord(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Expand selections to the end of their containing word.</p>
<p>Operates on all selections. Moves the cursor to the end of the containing
word while preserving the selection&#x27;s tail position. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToPreviousSubwordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, move its cursor to the preceding subword
boundary while maintaining the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToNextSubwordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, move its cursor to the next subword boundary
while maintaining the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectLinesContainingCursors(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each cursor, select the containing line.</p>
<p>This method merges selections on successive lines. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectWordsContainingCursors(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Select the word surrounding each cursor. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToPreviousWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, move its cursor to the preceding word boundary
while maintaining the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToNextWordBoundary(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, move its cursor to the next word boundary while
maintaining the selection&#x27;s tail position.</p>
<p>This method may merge selections that end up intersecting. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfNextWord(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Expand selections to the beginning of the next word.</p>
<p>Operates on all selections. Moves the cursor to the beginning of the next
word while preserving the selection&#x27;s tail position. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfNextParagraph(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Expand selections to the beginning of the next paragraph.</p>
<p>Operates on all selections. Moves the cursor to the beginning of the next
paragraph while preserving the selection&#x27;s tail position. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectToBeginningOfPreviousParagraph(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Expand selections to the beginning of the next paragraph.</p>
<p>Operates on all selections. Moves the cursor to the beginning of the next
paragraph while preserving the selection&#x27;s tail position. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>selectMarker(</b>marker<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>marker</code> A `{DisplayMarker}`</li>
</ul>

<p>Select the range of the given marker if it is valid.</p>

<em>Returns</em>
<ul>
<li>Returns the selected `{Range}` or `` if the marker is invalid.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLastSelection(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the most recently added <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelections(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get current <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>s.</p>

<em>Returns</em>
<ul>
<li>Returns: An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSelectionsOrderedByBufferPosition(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get all <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>s, ordered by their position in the buffer
instead of the order in which they were added.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/selection.coffee#L10">{Selection}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>selectionIntersectsBufferRange(</b>bufferRange<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRange</code> A `{Range}` or range-compatible <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>.</li>
</ul>

<p>Determine if a given range in buffer coordinates intersects a
selection.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>scan(</b>regex, iterator<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>regex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> to search for.</li>
<li><code>iterator</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that&#39;s called on each match<ul>
<li><code>object</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>match</code> The current regular expression match.</li>
<li><code>matchText</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with the text of the match.</li>
<li><code>range</code> The `{Range}` of the match.</li>
<li><code>stop</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to terminate the scan.</li>
<li><code>replace</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> with a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to replace the match. </li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Scan regular expression matches in the entire buffer, calling the
given iterator function on each match.</p>
<p>&#x60;::scan&#x60; functions as the replace method as well via the &#x60;replace&#x60;</p>
<p>If you&#x27;re programmatically modifying the results, you may want to try
{::backwardsScanInBufferRange} to avoid tripping over your own changes.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>scanInBufferRange(</b>regex, range, iterator<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>regex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> to search for.</li>
<li><code>range</code> A `{Range}` in which to search.</li>
<li><code>iterator</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that&#39;s called on each match with an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing the following keys:<ul>
<li><code>match</code> The current regular expression match.</li>
<li><code>matchText</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with the text of the match.</li>
<li><code>range</code> The `{Range}` of the match.</li>
<li><code>stop</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to terminate the scan.</li>
<li><code>replace</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> with a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to replace the match. </li>
</ul>
</li>
</ul>

<p>Scan regular expression matches in a given range, calling the given
iterator function on each match.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>backwardsScanInBufferRange(</b>regex, range, iterator<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>regex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> to search for.</li>
<li><code>range</code> A `{Range}` in which to search.</li>
<li><code>iterator</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that&#39;s called on each match with an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> containing the following keys:<ul>
<li><code>match</code> The current regular expression match.</li>
<li><code>matchText</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> with the text of the match.</li>
<li><code>range</code> The `{Range}` of the match.</li>
<li><code>stop</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to terminate the scan.</li>
<li><code>replace</code> Call this <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> with a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to replace the match. </li>
</ul>
</li>
</ul>

<p>Scan regular expression matches in a given range in reverse order,
calling the given iterator function on each match.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getSoftTabs(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether softTabs are enabled for this
editor.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setSoftTabs(</b>softTabs<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>softTabs</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> </li>
</ul>

<p>Enable or disable soft tabs for this editor.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>toggleSoftTabs(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Toggle soft tabs for this editor </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getTabLength(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the on-screen length of tab characters.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setTabLength(</b>tabLength<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>tabLength</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> length of a single tab. Setting to <code>null</code> will fallback to using the <code>editor.tabLength</code> config setting </li>
</ul>

<p>Set the on-screen length of tab characters. Setting this to a
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> This will override the &#x60;editor.tabLength&#x60; setting.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>usesSoftTabs(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Determine if the buffer uses hard or soft tabs.</p>

<em>Returns</em>
<ul>
<li>Returns <code>true</code> if the first non-comment line with leading whitespace starts
with a space character.</li>
<li>Returns <code>false</code> if it starts with a hard tab (<code>\t</code>).</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> or  if no non-comment lines had leading
whitespace.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getTabText(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the text representing a single level of indent.</p>
<p>If soft tabs are enabled, the text is composed of N spaces, where N is the
tab length. Otherwise the text is a tab character (&#x60;\t&#x60;).</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isSoftWrapped(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Determine whether lines in this editor are soft-wrapped.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setSoftWrapped(</b>softWrapped<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>softWrapped</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a></li>
</ul>

<p>Enable or disable soft wrapping for this editor.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>toggleSoftWrapped(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Toggle soft wrapping for this editor</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getSoftWrapColumn(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Gets the column at which column will soft wrap </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>indentationForBufferRow(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the indentation level of the given a buffer row.</p>

<em>Returns</em>
<ul>
<li><p>Returns how deeply the given row is indented based on the soft tabs and
tab length settings of this editor. Note that if soft tabs are enabled and
the tab length is 2, a row with 4 leading spaces would have an indentation
level of 2.</p>
</li>
<li><p><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the buffer row.</p>
</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setIndentationForBufferRow(</b>bufferRow, newLevel[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the buffer row.</li>
<li><code>newLevel</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the new indentation level.</li>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>preserveLeadingWhitespace</code> <code>true</code> to preserve any whitespace already at  the beginning of the line (default: false). </li>
</ul>
</li>
</ul>

<p>Set the indentation level for the given buffer row.</p>
<p>Inserts or removes hard tabs or spaces based on the soft tabs and tab length
settings of this editor in order to bring it to the given indentation level.
Note that if soft tabs are enabled and the tab length is 2, a row with 4
leading spaces would have an indentation level of 2.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>indentSelectedRows(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Indent rows intersecting selections by one level. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>outdentSelectedRows(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Outdent rows intersecting selections by one level. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>indentLevelForLine(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the indentation level of the given line of text.</p>

<em>Returns</em>
<ul>
<li><p>Returns how deeply the given line is indented based on the soft tabs and
tab length settings of this editor. Note that if soft tabs are enabled and
the tab length is 2, a row with 4 leading spaces would have an indentation
level of 2.</p>
</li>
<li><p><code>line</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing a line of text.</p>
</li>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>autoIndentSelectedRows(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Indent rows intersecting selections based on the grammar&#x27;s suggested
indent level. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getGrammar(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the current `{Grammar}` of this editor. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>setGrammar(</b>grammar<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>grammar</code> `{Grammar}` </li>
</ul>

<p>Set the current `{Grammar}` of this editor.</p>
<p>Assigning a grammar will cause the editor to re-tokenize based on the new
grammar.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getRootScopeDescriptor(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a> that includes this editor&#39;s language.
e.g. <code>[&#39;.source.ruby&#39;]</code>, or <code>[&#39;.source.coffee&#39;]</code>. You can use this with
{Config::get} to get language specific config values.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>scopeDescriptorForBufferPosition(</b>bufferPosition<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> A `{Point}` or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of [row, column].</li>
</ul>

<p>Get the syntactic scopeDescriptor for the given position in buffer
coordinates. Useful with {Config::get}.</p>
<p>For example, if called with a position inside the parameter list of an
anonymous CoffeeScript function, the method returns the following array:
&#x60;[&quot;source.coffee&quot;, &quot;meta.inline.function.coffee&quot;, &quot;variable.parameter.function.coffee&quot;]&#x60;</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/scope-descriptor.coffee#L21">{ScopeDescriptor}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>bufferRangeForScopeAtCursor(</b>scopeSelector<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>scopeSelector</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> selector. e.g. <code>&#39;.source.ruby&#39;</code></li>
</ul>

<p>Get the range in buffer coordinates of all tokens surrounding the
cursor that match the given scope selector.</p>
<p>For example, if you wanted to find the string surrounding the cursor, you
could call &#x60;editor.bufferRangeForScopeAtCursor(&quot;.string.quoted&quot;)&#x60;.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Range}`.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isBufferRowCommented(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Determine if the given row is entirely a comment </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>copySelectedText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, copy the selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cutSelectedText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, cut the selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>pasteText(</b>[options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> See {Selection::insertText}. </li>
</ul>

<p>For each selection, replace the selected text with the contents of
the clipboard.</p>
<p>If the clipboard contains the same number of selections as the current
editor, each selection will be replaced with the content of the
corresponding clipboard selection text.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cutToEndOfLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, cut all characters
of the containing screen line following the cursor. Otherwise cut the selected
text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>cutToEndOfBufferLine(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, if the selection is empty, cut all characters
of the containing buffer line following the cursor. Otherwise cut the
selected text. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>foldCurrentRow(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Fold the most recent cursor&#x27;s row based on its indentation level.</p>
<p>The fold will extend from the nearest preceding line with a lower
indentation level up to the nearest following row with a lower indentation
level. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>unfoldCurrentRow(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Unfold the most recent cursor&#x27;s row by one level. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>foldBufferRow(</b>bufferRow<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>. </li>
</ul>

<p>Fold the given row in buffer coordinates based on its indentation
level.</p>
<p>If the given row is foldable, the fold will begin there. Otherwise, it will
begin at the first foldable row preceding the given row.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>unfoldBufferRow(</b>bufferRow<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> </li>
</ul>

<p>Unfold all folds containing the given row in buffer coordinates.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>foldSelectedLines(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>For each selection, fold the rows it intersects. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>foldAll(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Fold all foldable lines. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>unfoldAll(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Unfold all existing folds. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>foldAllAtIndentLevel(</b>level<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>level</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>. </li>
</ul>

<p>Fold all foldable lines at the given indent level.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isFoldableAtBufferRow(</b>bufferRow<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>

<p>Determine whether the given row in buffer coordinates is foldable.</p>
<p>A <em>foldable</em> row is a row that <em>starts</em> a row range that can be folded.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isFoldableAtScreenRow(</b>bufferRow<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>

<p>Determine whether the given row in screen coordinates is foldable.</p>
<p>A <em>foldable</em> row is a row that <em>starts</em> a row range that can be folded.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>toggleFoldAtBufferRow(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Fold the given buffer row if it isn&#x27;t currently folded, and unfold
it otherwise. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>isFoldedAtCursorRow(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Determine whether the most recently added cursor&#x27;s row is folded.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isFoldedAtBufferRow(</b>bufferRow<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>

<p>Determine whether the given row in buffer coordinates is folded.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isFoldedAtScreenRow(</b>screenRow<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenRow</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
</ul>

<p>Determine whether the given row in screen coordinates is folded.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addGutter(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following fields:<ul>
<li><code>name</code> (required) A unique <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to identify this gutter.</li>
<li><code>priority</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> that determines stacking order between   gutters. Lower priority items are forced closer to the edges of the   window. (default: -100)</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> specifying whether the gutter is visible   initially after being created. (default: true)</li>
</ul>
</li>
</ul>

<p>Add a custom <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>.</p>

<em>Returns</em>
<ul>
<li>Returns the newly-created <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getGutters(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get this editor&#x27;s gutters.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>gutterWithName(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the gutter with the given name.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/gutter.coffee#L9">{Gutter}</a>, or <code>null</code> if no gutter exists for the given name.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>scrollToCursorPosition(</b>[options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>center</code> Center the editor around the cursor if possible. (default: true) </li>
</ul>
</li>
</ul>

<p>Scroll the editor to reveal the most recently added cursor if it is
off-screen.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>scrollToBufferPosition(</b>bufferPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>bufferPosition</code> An object that represents a buffer position. It can be either an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> (<code>{row, column}</code>), <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> (<code>[row, column]</code>), or `{Point}`</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>center</code> Center the editor around the position if possible. (default: false) </li>
</ul>
</li>
</ul>

<p>Scrolls the editor to the given buffer position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>scrollToScreenPosition(</b>screenPosition[, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>screenPosition</code> An object that represents a screen position. It can be either  an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> (<code>{row, column}</code>), <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> (<code>[row, column]</code>), or `{Point}`</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>center</code> Center the editor around the position if possible. (default: false) </li>
</ul>
</li>
</ul>

<p>Scrolls the editor to the given screen position.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getPlaceholderText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Retrieves the greyed out placeholder of a mini editor.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>setPlaceholderText(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>placeholderText</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> text that is displayed when the editor has no content. </li>
</ul>

<p>Set the greyed out placeholder of a mini editor. Placeholder text
will be displayed when the editor has no content.</p>

<em>Returns</em>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-ThemeManager">ThemeManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Handles loading and activating available themes.</p>
<p>An instance of this class is always available as the &#x60;atom.themes&#x60; global. </p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>onDidChangeActiveThemes(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> </li>
</ul>

<p>Invoke &#x60;callback&#x60; when style sheet changes associated with
updating the list of active themes have completed.</p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>getLoadedThemeNames(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s of all the loaded theme names.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLoadedThemes(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the loaded themes.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActiveThemeNames(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>s all the active theme names.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActiveThemes(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">


<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the active themes.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getEnabledThemeNames(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Get the enabled theme names from the config.</p>

<em>Returns</em>
<ul>
<li>Returns an array of theme names in the order that they should be activated.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-TooltipManager">TooltipManager</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Associates tooltips with HTML elements or selectors.</p>
<p>You can get the &#x60;TooltipManager&#x60; via &#x60;atom.tooltips&#x60;.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>add(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>target</code> An <code>HTMLElement</code></li>
<li><code>options</code> See <a href="http://getbootstrap.com/javascript/#tooltips-options">http://getbootstrap.com/javascript/#tooltips-options</a> for a full list of options. You can also supply the following additional options:<ul>
<li><code>title</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to use for the text in the tip. If given a function, <code>this</code> will be set to the <code>target</code> element.</li>
<li><code>trigger</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> that&#39;s the same as Bootstrap &#39;click | hover | focus  | manual&#39;, except &#39;manual&#39; will show the tooltip immediately.</li>
<li><code>keyBindingCommand</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing a command name. If you specify this option and a key binding exists that matches the command, it will be appended to the title or rendered alone if no title is specified.</li>
<li><code>keyBindingTarget</code> An <code>HTMLElement</code> on which to look up the key binding. If this option is not supplied, the first of all matching key bindings for the given command will be rendered.</li>
</ul>
</li>
</ul>

<p>Add a tooltip to the given element.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
tooltip.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-ViewRegistry">ViewRegistry</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>&#x60;ViewRegistry&#x60; handles the association between model and view
types in Atom. We call this association a View Provider. As in, for a given
model, this class can provide a view via {::getView}, as long as the
model/view association was registered via {::addViewProvider}</p>
<p>If you&#x27;re adding your own kind of pane item, a good strategy for all but the
simplest items is to separate the model and the view. The model handles
application logic and is the primary point of API interaction. The view
just handles presentation.</p>
<p>View providers inform the workspace how your model objects should be
presented in the DOM. A view provider must always return a DOM node, which
makes <a href="http://www.html5rocks.com/en/tutorials/webcomponents/customelements/">HTML 5 custom elements</a>
an ideal tool for implementing views in Atom.</p>
<p>You can access the &#x60;ViewRegistry&#x60; object via &#x60;atom.views&#x60;.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>addViewProvider(</b>[modelConstructor], createView<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>modelConstructor</code> Constructor <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> for your model. If a constructor is given, the <code>createView</code> function will only be used for model objects inheriting from that constructor. Otherwise, it will will be called for any object.</li>
<li><code>createView</code> Factory <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> that is passed an instance of your model and must return a subclass of <code>HTMLElement</code> or <code>undefined</code>. If it returns <code>undefined</code>, then the registry will continue to search for other view providers.</li>
</ul>

<p>Add a provider that will be used to construct views in the
workspace&#x27;s view layer based on model objects in its model layer.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
added provider.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getView(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>object</code> The object for which you want to retrieve a view. This can be a pane item, a pane, or the workspace itself.</li>
</ul>

<p>Get the view associated with an object in the workspace.</p>
<p>If you&#x27;re just <em>using</em> the workspace, you shouldn&#x27;t need to access the view
layer, but view layer access may be necessary if you want to perform DOM
manipulation that isn&#x27;t supported via the model API.</p>
<h2 id="view-resolution-algorithm">View Resolution Algorithm</h2>
<p>The view associated with the object is resolved using the following
sequence</p>
<ol>
<li>Is the object an instance of &#x60;HTMLElement&#x60;? If true, return the object.</li>
<li>Does the object have a property named &#x60;element&#x60; with a value which is
an instance of &#x60;HTMLElement&#x60;? If true, return the property value.</li>
<li>Is the object a jQuery object, indicated by the presence of a &#x60;jquery&#x60;
property? If true, return the root DOM element (i.e. &#x60;object[0]&#x60;).</li>
<li>Has a view provider been registered for the object? If true, use the
provider to create a view associated with the object, and return the
view.</li>
</ol>
<p>If no associated view is returned by the sequence an error is thrown.</p>

<em>Returns</em>
<ul>
<li>Returns a DOM element.</li>
</ul>

</td></tr>

</table>


 <a href="#" target="_blank"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/line.png" width="100%" height="1px"></a>

 

<h3> <a name="class-Workspace">Workspace</a> <b><sub><sup><code>CLASS  </code></sup></sub></b> <a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a></h3>

<p>Represents the state of the user interface for the entire window.
An instance of this class is available via the &#x60;atom.workspace&#x60; global.</p>
<p>Interact with this object to open files, be notified of current and future
editors, and manipulate panes. To add panels, use {Workspace::addTopPanel}
and friends.</p>


<table width="100%">
<tr><td colspan="2"></td></tr>
<tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>

<tr>
<td><code>:: <b>observeTextEditors(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with current and future text editors.<ul>
<li><code>editor</code> An <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> that is present in {::getTextEditors} at the time of subscription or that is added at some later time.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with all current and future text
editors in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observePaneItems(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with current and future pane items.<ul>
<li><code>item</code> An item that is present in {::getPaneItems} at the time of  subscription or that is added at some later time.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with all current and future panes items
in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeActivePaneItem(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the active pane item changes.<ul>
<li><code>item</code> The active pane item.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the active pane item changes.</p>
<p>Because observers are invoked synchronously, it&#x27;s important not to perform
any expensive operations via this method. Consider
{::onDidStopChangingActivePaneItem} to delay operations until after changes
stop occurring.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidStopChangingActivePaneItem(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the active pane item stopts changing.<ul>
<li><code>item</code> The active pane item.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the active pane item stops
changing.</p>
<p>Observers are called asynchronously 100ms after the last active pane item
change. Handling changes here rather than in the synchronous
{::onDidChangeActivePaneItem} prevents unneeded work if the user is quickly
changing or closing tabs and ensures critical UI feedback, like changing the
highlighted tab, gets priority over work that can be done asynchronously.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeActivePaneItem(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the active pane item changes.<ul>
<li><code>item</code> The current active pane item.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with the current active pane item and
with all future active pane items in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidOpen(</b>callback<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called whenever an item is opened.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>uri</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representing the opened URI. Could be <code>undefined</code>.</li>
<li><code>item</code> The opened item.</li>
<li><code>pane</code> The pane in which the item was opened.</li>
<li><code>index</code> The index of the opened item on its pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback whenever an item is opened. Unlike
{::onDidAddPaneItem}, observers will be notified for items that are already
present in the workspace when they are reopened.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddPane(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called panes are added.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>pane</code> The added pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a pane is added to the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillDestroyPane(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called before panes are destroyed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>pane</code> The pane to be destroyed.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback before a pane is destroyed in the
workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroyPane(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called panes are destroyed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>pane</code> The destroyed pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a pane is destroyed in the
workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observePanes(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with current and future panes.<ul>
<li><code>pane</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> that is present in {::getPanes} at the time of  subscription or that is added at some later time.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with all current and future panes in the
workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidChangeActivePane(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when the active pane changes.<ul>
<li><code>pane</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> that is the current return value of {::getActivePane}.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when the active pane changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>observeActivePane(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called with the current and future active# panes.<ul>
<li><code>pane</code> A <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> that is the current return value of {::getActivePane}.</li>
</ul>
</li>
</ul>

<p>Invoke the given callback with the current active pane and when
the active pane changes.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddPaneItem(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when pane items are added.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The added pane item.</li>
<li><code>pane</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> containing the added item.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index of the added item in its pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a pane item is added to the
workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onWillDestroyPaneItem(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called before pane items are destroyed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The item to be destroyed.</li>
<li><code>pane</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> containing the item to be destroyed.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index of the item to be destroyed in its pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a pane item is about to be
destroyed, before the user is prompted to save it.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidDestroyPaneItem(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when pane items are destroyed.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>item</code> The destroyed item.</li>
<li><code>pane</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> containing the destroyed item.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index of the destroyed item in its pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a pane item is destroyed.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>onDidAddTextEditor(</b>callback<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>callback</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called panes are added.<ul>
<li><code>event</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with the following keys:<ul>
<li><code>textEditor</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> that was added.</li>
<li><code>pane</code> <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> containing the added text editor.</li>
<li><code>index</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating the index of the added text editor in its  pane.</li>
</ul>
</li>
</ul>
</li>
</ul>

<p>Invoke the given callback when a text editor is added to the
workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to unsubscribe.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>open(</b>[uri][, options]<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>uri</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> containing a URI.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>initialLine</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating which row to move the cursor to initially. Defaults to <code>0</code>.</li>
<li><code>initialColumn</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> indicating which column to move the cursor to initially. Defaults to <code>0</code>.</li>
<li><code>split</code> Either &#39;left&#39;, &#39;right&#39;, &#39;up&#39; or &#39;down&#39;. If &#39;left&#39;, the item will be opened in leftmost pane of the current active pane&#39;s row. If &#39;right&#39;, the item will be opened in the rightmost pane of the current active pane&#39;s row. If only one pane exists in the row, a new pane will be created. If &#39;up&#39;, the item will be opened in topmost pane of the current active pane&#39;s column. If &#39;down&#39;, the item will be opened in the bottommost pane of the current active pane&#39;s column. If only one pane exists in the column, a new pane will be created.</li>
<li><code>activatePane</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to call {Pane::activate} on containing pane. Defaults to <code>true</code>.</li>
<li><code>activateItem</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether to call {Pane::activateItem} on containing pane. Defaults to <code>true</code>.</li>
<li><code>pending</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> indicating whether or not the item should be opened in a pending state. Existing pending items in a pane are replaced with new pending items when they are opened.</li>
<li><code>searchAllPanes</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. If <code>true</code>, the workspace will attempt to activate an existing item for the given URI on any pane. If <code>false</code>, only the active pane will be searched for an existing item for the same URI. Defaults to <code>false</code>.</li>
</ul>
</li>
</ul>

<p>Opens the given URI in Atom asynchronously.
If the URI is already open, the existing item for that URI will be
activated. If no URI is given, or no registered opener can open
the URI, a new empty <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> will be created.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that resolves to the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> for the file URI.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>isTextEditor(</b>object<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>object</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> you want to perform the check against. </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> that is <code>true</code> if <code>object</code> is a <code>TextEditor</code>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>buildTextEditor(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Create a new text editor.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>reopenItem(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">

<p>Asynchronously reopens the last-closed item&#x27;s URI if it hasn&#x27;t already been
reopened.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> that is resolved when the item is opened</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>addOpener(</b>opener<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>opener</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be called when a path is being opened.</li>
</ul>

<p>Register an opener for a uri.</p>
<p>An <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> will be used if no openers return a value.</p>

<em>Returns</em>
<ul>
<li>Returns a `{Disposable}` on which <code>.dispose()</code> can be called to remove the
opener.</li>
</ul>
<p>Note that the opener will be called if and only if the URI is not already open
in the current pane. The searchAllPanes flag expands the search from the
current pane to all panes. If you wish to open a view of a different type for
a file that is already open, consider changing the protocol of the URI. For
example, perhaps you wish to preview a rendered version of the file <code>/foo/bar/baz.quux</code>
that is already open in a text editor view. You could signal this by calling
{Workspace::open} on the URI <code>quux-preview://foo/bar/baz.quux</code>. Then your opener
can check the protocol for quux-preview and only handle those URIs that match.</p>

</td></tr>

<tr>
<td><code>:: <b>getPaneItems(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get all pane items in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of items.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActivePaneItem(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the active <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>&#x27;s active item.</p>

<em>Returns</em>
<ul>
<li>Returns an pane item <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getTextEditors(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get all text editors in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActiveTextEditor(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get the active item if it is an <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a> or `` if the current active item is not an
<a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/text-editor.coffee#L60">{TextEditor}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getPanes(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get all panes in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>s.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getActivePane(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Get the active <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a>.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>activateNextPane(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Make the next pane active. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>activatePreviousPane(</b><b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">

<p>Make the previous pane active. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>paneForURI(</b>uri<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>uri</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> uri</li>
</ul>

<p>Get the first <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> with an item for the given URI.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> or `` if no pane exists for the given URI.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>paneForItem(</b>item<b>)</b></code></td>
<td><code>Extended</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> Item the returned pane contains.</li>
</ul>

<p>Get the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> containing the given item.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/pane.coffee#L18">{Pane}</a> or `` if no pane exists for the given item.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getBottomPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items at the bottom of the editor window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addBottomPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the bottom of the editor window.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getLeftPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items to the left of the editor window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addLeftPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the left of the editor window.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getRightPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items to the right of the editor window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addRightPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the right of the editor window.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getTopPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items at the top of the editor window. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addTopPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the top of the editor window above the tabs.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getHeaderPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items in the header. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addHeaderPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the header.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getFooterPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the panel items in the footer. </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addFooterPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the latter. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item to the footer.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>getModalPanels(</b><b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">

<p>Get an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of all the modal panel items </p>

<em>Returns</em>

</td></tr>

<tr>
<td><code>:: <b>addModalPanel(</b>options<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>item</code> Your panel content. It can be a DOM element, a jQuery element, or a model with a view registered via {ViewRegistry::addViewProvider}. We recommend the model option. See {ViewRegistry::addViewProvider} for more information.</li>
<li><code>visible</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> false if you want the panel to initially be hidden (default: true)</li>
<li><code>priority</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> Determines stacking order. Lower priority items are forced closer to the edges of the window. (default: 100)</li>
</ul>
</li>
</ul>

<p>Adds a panel item as a modal dialog.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a></li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>panelForItem(</b>item<b>)</b></code></td>
<td><code>Essential</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>item</code> Item the panel contains </li>
</ul>


<em>Returns</em>
<ul>
<li>Returns the <a href="https://github.com/atom/atom/blob/v1.9.0-dev/src/panel.coffee#L12">{Panel}</a> associated with the given item.</li>
<li>Returns
<code>null</code> when the item has no panel.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>scan(</b>regex[, options], iterator<b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>regex</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> to search with.</li>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a><ul>
<li><code>paths</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of glob patterns to search within.</li>
<li><code>onPathsSearched</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> to be periodically called with number of paths searched.</li>
</ul>
</li>
<li><code>iterator</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> callback on each file found.</li>
</ul>

<p>Performs a search across all files in the workspace.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a> with a <code>cancel()</code> method that will cancel all
of the underlying searches that were started as part of this scan.</li>
</ul>

</td></tr>

<tr>
<td><code>:: <b>replace(</b><b>)</b></code></td>
<td><code>Public</code></td> </tr>
<tr><td colspan="2">
<ul>
<li><code>regex</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">{RegExp}</a> to search with.</li>
<li><code>replacementText</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> to replace all matches of regex with.</li>
<li><code>filePaths</code> An <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of file path strings to run the replace on.</li>
<li><code>iterator</code> A <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function">{Function}</a> callback on each file with replacements:<ul>
<li><code>options</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with keys <code>filePath</code> and <code>replacements</code>.</li>
</ul>
</li>
</ul>

<p>Performs a replace across all the specified files in the project.</p>

<em>Returns</em>
<ul>
<li>Returns a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">{Promise}</a>.</li>
</ul>

</td></tr>

</table>






