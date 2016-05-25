### <a name='classes'>API</a>

Class |  Summary
------| ------------
  <code>[Interval](#class-Interval)</code> | The undefined class represents a line segment on the   the number line.

### <a name="class-Interval">Interval</a><b><sub><sup><code>CLASS </code></sup></sub></b><a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a>

<p>The undefined class represents a line segment on the
  the number line.</p>
<p>An <a href="http://mathworld.wolfram.com/Interval.html">interval</a>
is a connected portion of the real line.</p>
<p>Also see <a href="http://www.gdmc.nl/oosterom/atti.pdf">A Small Set of Formal Topological Relationships Suitable
  for End User Interaction</a></p>
<p>A couple of definitions:</p>
<ul>
<li>The boundary of an undefined is set of its two endpoints.</li>
<li>The interior of an undefined is the set of all points
in the undefined less its boundary (endpoints).</li>
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
      <p>undefined The start/left endpoint of this undefined </p>
  
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
      <p>undefined The end/right endpoint of this undefined </p>
  
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
      <p>undefined True if this undefined has the same start and end points </p>
  
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
  <li><code>arg1</code> can be a undefined or an undefined or undefined or a undefined</li>
  <li><code>arg2</code> undefined</li>
  </ul>
  
      <p>Creates a immutable undefined object</p>
  <p><code>arg1</code> can be a:</p>
  <ul>
  <li>undefined: <code>&lt;number&gt; &lt;sep&gt; &lt;number&gt;</code> where sep
  can be any one of a comma, semicolon, or a space</li>
  <li>undefined  of two undefineds</li>
  <li>undefined with one of these key combinations:
    <code>{from, to}</code> <code>{start, end}</code>  <code>{a, b}</code></li>
  <li>a undefined, in which case <code>arg2</code> must be defined</li>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Checks if this undefined contains the other.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if this undefined <code>contains</code> the other other.</li>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Checks if this undefined overlaps another.</p>
  <p>For two undefineds to overlap they must have some points
  but not all points.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if this undefined overlaps the other.</li>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Checks if this undefined is fully within another.</p>
  <p>undefined X is said to be within another undefined Y if
  X is completely within Y and neither of their endpoints touch.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if this undefined is within the other.</li>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Checks if this undefined touches anothe.</p>
  <p>Two line segments touch, if:</p>
  <ul>
  <li>one their endpoints touch</li>
  <li>their interiors do not share any common points</li>
  </ul>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if this undefined touches the other.</li>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Checks if this undefined is <code>disjoint</code> with another.</p>
  <p>Two undefineds are disjoint if they have no points in common,
  i.e. if their intersection is the empty set.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if this undefined is disjoint with the other.</li>
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
  <li><code>others</code> {Arrayundefined} One or more intervals</li>
  </ul>
  
      <p>Calculates the union of the given undefined</p>
  <p>A union of intervals can result in an array of unconnected parts.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns undefined</p>
  </li>
  <li><p>Returns undefined of undefined</p>
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Calculates the intersection, i.e. the points where they concur.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns an undefined with the intersection or `` if the two do
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Calculates the difference between this undefined and another.</p>
  <p>The difference between undefined X and Y is all of the points
  in X which are not in Y.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns the difference which is one of:</p>
  </li>
  <li><p>undefined</p>
  </li>
  <li>{Arrayundefined}
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Compute an XOR with the given undefined</p>
  <p>The set of elements belonging to one but not both of two given sets.
  It is therefore the union of the complement of A with respect to
  B and B with respect to  A, and corresponds to the XOR operation in
  Boolean logic.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li><p>Returns the difference which is one of:</p>
  </li>
  <li><p>undefined</p>
  </li>
  <li>{Arrayundefined}
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
  <li><code>other</code> the other undefined</li>
  </ul>
  
      <p>Check if both undefineds are equal.</p>
  <p>Two intervals are equal if their line segments are equal,
  i.e same start and end points.</p>
  
      <p>  <strong>Returns</strong></p>
  <ul>
  <li>Returns undefined. True if the undefineds are equal.</li>
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
      
      <p>Get a undefined representation of this undefined</p>
  <p>Return undefined</p>
  
      
    </td>
  </tr>
  
</table>

  


