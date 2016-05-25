### <a name='classes'>API</a>

Class |  Summary
------| ------------
  <code>[Interval](#class-Interval)</code> | The <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> class represents a line segment on the   the number line.

### <a name="class-Interval">Interval</a><b><sub><sup><code>CLASS </code></sup></sub></b><a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a>

<p>The <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> class represents a line segment on the
  the number line.</p>
<p>An <a href="http://mathworld.wolfram.com/Interval.html">interval</a>
is a connected portion of the real line.</p>
<p>Also see <a href="http://www.gdmc.nl/oosterom/atti.pdf">A Small Set of Formal Topological Relationships Suitable
  for End User Interaction</a></p>
<p>A couple of definitions:</p>
<ul>
<li>The boundary of an <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is set of its two endpoints.</li>
<li>The interior of an <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is the set of all points
in the <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> less its boundary (endpoints).</li>
</ul>


<table width="100%">
    <tr>
      <td colspan="4"><h4>Properties</h4></td>
    </tr>
  
      <tr>
        <td><code>:: <b>a</b>  </code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
          <p><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The start/left endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> </p>
  
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>b</b>  </code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
          <p><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The end/right endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> </p>
  
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>degenerate</b>  </code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
          <p><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> True if this `{Instance}` has the same start and end points </p>
  
        </td>
      </tr>
  
    <tr>
      <td colspan="2"></td>
    </tr>
    <tr>
      <td colspan="4"><h4>Methods</h4></td>
    </tr>
  
      <tr>
        <td><code>:: <b>constructor(</b> arg1[, arg2] <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>arg1</code> can be a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> or an <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> or a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a></li>
  <li><code>arg2</code> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> <code>arg1</code> can be a:<ul>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a>: <code>&lt;number&gt; &lt;sep&gt; &lt;number&gt;</code> where sep
  can be any one of a comma, semicolon, or a space</li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a>  of two <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>s</li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">{Object}</a> with one of these key combinations:
  <code>{from, to}</code> <code>{start, end}</code>  <code>{a, b}</code></li>
  <li>a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a>, in which case <code>arg2</code> must be defined<pre><code>Creates a immutable <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> object
  </code></pre></li>
  </ul>
  </li>
  </ul>
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>contains(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Checks if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> contains the other.
      __Returns__
      * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> &amp;#x60;contains&amp;#x60; the other other.
  </code></pre></li>
  </ul>
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>overlaps(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Checks if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> overlaps another.
  </code></pre></li>
  </ul>
  <p>For two <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>s to overlap they must have some points
  but not all points.
              <strong>Returns</strong></p>
  <pre><code>        * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> overlaps the other.
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>within(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Checks if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is fully within another.
  </code></pre></li>
  </ul>
  <p><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> X is said to be within another <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> Y if
  X is completely within Y and neither of their endpoints touch.
              <strong>Returns</strong></p>
  <pre><code>        * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is within the other.
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>touches(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Checks if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> touches anothe.
  </code></pre></li>
  </ul>
  <p>Two line segments touch, if:</p>
  <ul>
  <li>one their endpoints touch</li>
  <li>their interiors do not share any common points<pre><code>      __Returns__
        * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> touches the other.
  </code></pre></li>
  </ul>
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>disjoint(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Checks if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is &amp;#x60;disjoint&amp;#x60; with another.
  </code></pre></li>
  </ul>
  <p>Two <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>s are disjoint if they have no points in common,
  i.e. if their intersection is the empty set.
              <strong>Returns</strong></p>
  <pre><code>        * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> is disjoint with the other.
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>union(</b> others <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>others</code> {Array<a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>} One or more intervals<pre><code>  Calculates the union of the given `{Intervals}`
  </code></pre></li>
  </ul>
  <p>A union of intervals can result in an array of unconnected parts.
              <strong>Returns</strong></p>
  <pre><code>        * Returns <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
  
          * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">{Array}</a> of <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>intersection(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Calculates the intersection, i.e. the points where they concur.
      __Returns__
      * Returns an <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> with the intersection or &amp;#x60;&amp;#x60; if the two do
    not intersect.
  </code></pre></li>
  </ul>
        </td>
      </tr>
  
      <tr>
        <td><code>:: <b>difference(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Calculates the difference between this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> and another.
  </code></pre></li>
  </ul>
  <p>The difference between <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> X and Y is all of the points
  in X which are not in Y.
              <strong>Returns</strong></p>
  <pre><code>        * Returns the difference which is one of:
  
        * <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
        * {Array<a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>}
        *
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>xor(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Compute an XOR with the given <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
  </code></pre></li>
  </ul>
  <p>The set of elements belonging to one but not both of two given sets.
  It is therefore the union of the complement of A with respect to
  B and B with respect to  A, and corresponds to the XOR operation in
  Boolean logic.
              <strong>Returns</strong></p>
  <pre><code>        * Returns the difference which is one of:
  
        * <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
        * {Array<a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>}
        *
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>equals(</b> other <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <ul>
  <li><code>other</code> the other <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a><pre><code>  Check if both <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>s are equal.
  </code></pre></li>
  </ul>
  <p>Two intervals are equal if their line segments are equal,
  i.e same start and end points.
              <strong>Returns</strong></p>
  <pre><code>        * Returns <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a>. True if the <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>s are equal.
  </code></pre>      </td>
      </tr>
  
      <tr>
        <td><code>:: <b>toString(</b>  <b>)</b></code></td>
        <td width="8%" align="center"><sub>public</sub></td>
        <td width="8%" align="center"><sub>instance</sub></td>
        <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
      </tr>
      <tr>
        <td colspan="4">
  <pre><code>      Get a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a> representation of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a>
  </code></pre><p>Return <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">{String}</a></p>
        </td>
      </tr>
  
</table>

  


