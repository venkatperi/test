### <a name='classes'>API</a>

Class |  Summary
------| ------------
  <code>[Interval](#class-Interval)</code> | The <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> class represents a line segment on the   the number line.

### <a name="class-Interval">Interval</a><b><sub><sup><code>CLASS </code></sup></sub></b><a href="#classes"><img src="https://rawgit.com/venkatperi/atomdoc-md/master/assets/octicons/arrow-up.svg" alt="Back to Class List" height= "18px"></a>

<p>  The <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> class represents a line segment on the
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
      <td><code>:: <b>a</b>  <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The start/left endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> 
  </code></pre>      </td>
      </tr>
  
      <tr>
      <td><code>:: <b>b</b>  <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The end/right endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> 
  </code></pre>      </td>
      </tr>
  
      <tr>
      <td><code>:: <b>degenerate</b>  <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> True if this `{Instance}` has the same start and end points 
  </code></pre>      </td>
      </tr>
  
    <tr>
      <td colspan="2"></td>
    </tr>
    <tr>
      <td colspan="4"><h4>Methods</h4></td>
    </tr>
  
      <tr>
      <td><code>:: <b>constructor</b>    <b>(</b>arg1[, arg2]<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>contains</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>overlaps</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>within</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>touches</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>disjoint</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>union</b>    <b>(</b>others<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>intersection</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>difference</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>xor</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>equals</b>    <b>(</b>other<b>)</b></code></td>
        <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          <em>Returns</em>
          
        </td>
      </tr>
  
      <tr>
      <td><code>:: <b>toString</b>  <td width="8%"><b><sub>public</sub></b></td>
        <td width="8%"><b><sub>instance</sub></b></td>
        <td width="8%"><b><sub><code><a href="#class-Interval">Interval</a></code></sub></b></td>
      </tr>
      <tr>
        <td colspan="4">
  
  
          
        </td>
      </tr>
  
</table>

  


