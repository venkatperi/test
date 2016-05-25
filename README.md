### <a name='classes'>API</a>

Class |  Summary
------| ------------
  <code>[Interval](#class-Interval)</code> | The <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> class represents a line segment on the   the number line.

### <a name="class-Interval">Interval</a><b><sub><sup><code>CLASS </code></sup></sub></b><a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a>

<p>The <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> class represents a line segment on the
  the number line.</p>
<p>An <a href="http://mathworld.wolfram.com/Interval.html">interval</a>
is a connected portion of the real line.</p>
<p>Also see <a href="http://www.gdmc.nl/oosterom/atti.pdf">A Small Set of Formal Topological Relationships Suitable
  for End User Interaction</a></p>
<p>A couple of definitions:</p>
<ul>
<li>The boundary of an <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is set of its two endpoints.</li>
<li>The interior of an <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is the set of all points
in the <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> less its boundary (endpoints).</li>
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
      <p><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code> The start/left endpoint of this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> </p>
  
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
      <p><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code> The end/right endpoint of this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> </p>
  
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
      <p><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code> True if this <code>`{Instance}`</code> has the same start and end points </p>
  
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
  <li><code>arg1</code> can be a <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">String</a></code> or an <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Array</a></code> or <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">Object</a></code> or a <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code></li>
  <li><code>arg2</code> <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code></li>
  </ul>
  
      <p>Creates a immutable <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> object</p>
  <p><code>arg1</code> can be a:</p>
  <ul>
  <li><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">String</a></code>: <code>&lt;number&gt; &lt;sep&gt; &lt;number&gt;</code> where sep
  can be any one of a comma, semicolon, or a space</li>
  <li><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Array</a></code>  of two <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code>s</li>
  <li><code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">Object</a></code> with one of these key combinations:
    <code>{from, to}</code> <code>{start, end}</code>  <code>{a, b}</code></li>
  <li>a <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a></code>, in which case <code>arg2</code> must be defined</li>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Checks if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> contains the other.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> <code>contains</code> the other other.</li>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Checks if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> overlaps another.</p>
  <p>For two <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>s to overlap they must have some points
  but not all points.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> overlaps the other.</li>
  </ul>
  
    </td>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Checks if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is fully within another.</p>
  <p><code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> X is said to be within another <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> Y if
  X is completely within Y and neither of their endpoints touch.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is within the other.</li>
  </ul>
  
    </td>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Checks if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> touches anothe.</p>
  <p>Two line segments touch, if:</p>
  <ul>
  <li>one their endpoints touch</li>
  <li>their interiors do not share any common points</li>
  </ul>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> touches the other.</li>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Checks if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is <code>disjoint</code> with another.</p>
  <p>Two <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>s are disjoint if they have no points in common,
  i.e. if their intersection is the empty set.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> is disjoint with the other.</li>
  </ul>
  
    </td>
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
  <li><code>others</code> {Array<code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>} One or more intervals</li>
  </ul>
  
      <p>Calculates the union of the given <code>`{Intervals}`</code></p>
  <p>A union of intervals can result in an array of unconnected parts.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  </li>
  <li><p>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Array</a></code> of <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  </li>
  </ul>
  
    </td>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Calculates the intersection, i.e. the points where they concur.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns an <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> with the intersection or `` if the two do
  not intersect.</li>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Calculates the difference between this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> and another.</p>
  <p>The difference between <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code> X and Y is all of the points
  in X which are not in Y.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns the difference which is one of:</p>
  </li>
  <li><p><code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  </li>
  <li>{Array<code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>}
  *</li>
  </ul>
  
    </td>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Compute an XOR with the given <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  <p>The set of elements belonging to one but not both of two given sets.
  It is therefore the union of the complement of A with respect to
  B and B with respect to  A, and corresponds to the XOR operation in
  Boolean logic.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns the difference which is one of:</p>
  </li>
  <li><p><code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  </li>
  <li>{Array<code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>}
  *</li>
  </ul>
  
    </td>
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
  <li><code>other</code> the other <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></li>
  </ul>
  
      <p>Check if both <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>s are equal.</p>
  <p>Two intervals are equal if their line segments are equal,
  i.e same start and end points.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a></code>. True if the <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code>s are equal.</li>
  </ul>
  
    </td>
  </tr>
  
  <tr>
    <td><code>:: <b>toString(</b>  <b>)</b></code></td>
    <td width="8%" align="center"><sub>public</sub></td>
    <td width="8%" align="center"><sub>instance</sub></td>
    <td width="8%" align="center"><sub><a href="#class-Interval">Interval</a></sub></td>
  </tr>
  <tr>
    <td colspan="4">
      
      <p>Get a <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">String</a></code> representation of this <code><a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">Interval</a></code></p>
  <p>Return <code><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">String</a></code></p>
  
      
    </td>
  </tr>
  
</table>

  


