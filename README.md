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
        <td colspan="2"><h4>Properties</h4></td>
      </tr>
    
        <tr>
          <td><b><code>a</code></b></td>
          <td width="8%"><sub><code>Public</code></sub></td>
          <td width="8%"><sub><code></code></sub></td>
          <td width="8%"><sub><code><sub><code><a href="#class-"></a></code></sub></code></sub></td>
        </tr>
    
        <tr>
          <td colspan="2">
    <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The start/left endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> 
    </code></pre>      </td>
        </tr>
    
        <tr>
          <td><b><code>b</code></b></td>
          <td width="8%"><sub><code>Public</code></sub></td>
          <td width="8%"><sub><code></code></sub></td>
          <td width="8%"><sub><code><sub><code><a href="#class-"></a></code></sub></code></sub></td>
        </tr>
    
        <tr>
          <td colspan="2">
    <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">{Number}</a> The end/right endpoint of this <a href="https://github.com/venkatperi/line-segment-ops/blob/v0.1.0/lib/Interval.coffee#L20">{Interval}</a> 
    </code></pre>      </td>
        </tr>
    
        <tr>
          <td><b><code>degenerate</code></b></td>
          <td width="8%"><sub><code>Public</code></sub></td>
          <td width="8%"><sub><code></code></sub></td>
          <td width="8%"><sub><code><sub><code><a href="#class-"></a></code></sub></code></sub></td>
        </tr>
    
        <tr>
          <td colspan="2">
    <pre><code>      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">{Boolean}</a> True if this `{Instance}` has the same start and end points 
    </code></pre>      </td>
        </tr>
    
      <tr>
        <td colspan="2"></td>
      </tr>
    <tr> <td colspan="2"> <h4>Methods</h4> </td> </tr>
    
    <tr>
    <td><code>:: <b>constructor(</b>arg1[, arg2]<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>contains(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>overlaps(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>within(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>touches(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>disjoint(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>union(</b>others<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>intersection(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>difference(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>xor(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>equals(</b>other<b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    <em>Returns</em>
    
    </td></tr>
    
    <tr>
    <td><code>:: <b>toString(</b><b>)</b></code></td>
    <td><code>Public</code></td> </tr>
    <tr><td colspan="2">
    
    
    
    </td></tr>
    
  </table>
  
  


