# Matlab-Basics<br>
Summary of MATLAB Onramp<br>
<b>Basic syntax</b><br>

<table>
<tr><th>Example</th><th>Description</th></tr>
<tr><td>x = pi</td><td>	Create variables with the equal sign (=).<br>
The left-side (x) is the variable name containing the value on the right-side (pi).</td></tr>
<tr><td>y = sin(-5) </td><td>	You can provide inputs to a function using parentheses.</td></tr>
</table>
<br>
<b>Desktop management</b>
<table>
<tr><th>Function</th><th>Example</th><th>Description</th></tr>
<tr><td>save</td><td>	save data.mat</td><td>Save your current workspace to a MAT-file.</td></tr>
<tr><td>load</td><td>	load data.mat</td><td>	Load the variables in a MAT-file to the Workspace.</td></tr>
<tr><td>clear</td><td>clear</td><td>Clear all variables from the Workspace.</td></tr>
<tr><td>clc</td><td>	clc</td><td>Clear all text from the Command Window.</td></tr>
<tr><td>format</td><td>	format long</td><td>Change how numeric output is displayed.</td></tr>
</table>
	
	
<b>Array types</b><br>		
<table>
	<tr> <th> Example</th> <th> Description</th> </tr>
	<tr> <td> 4</td> <td> scalar</td> </tr>
	<tr> <td> [3 5]</td> <td> row vector</td> </tr>
	<tr> <td> [1;3]</td> <td> column vector</td> </tr>
	<tr> <td> [3 4 5;6 7 8]</td> <td>matrix</td> </tr>
</table>
 


	
<h2>Evenly-spaced vectors</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>1:4</code></td>
<td>Create a vector from <code>1</code> to <code>4</code>, spaced by <code>1</code>, using the colon (<code>:</code>)</a> operator.</td>
</tr>
<tr>
<td><code>1:0.5:4</code></td>
<td>Create a vector from <code>1</code> to <code>4</code>, spaced by <code>0.5</code>.</td>
</tr>
<tr>
<td><code>linspace</a>(1,10,5)</code></td>
<td>Create a vector with <code>5</code> elements. The values are evenly spaced from <code>1</code> to <code>10</code>.</td>
</tr>
</tbody>
</table>


<h2>Creating matrices</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>rand<code>(2)</code></td>
<td>Create a square matrix with <code>2</code> rows and <code>2</code> columns.</td>
</tr>
<tr>
<td><code>zeros</a>(2,3)</code></td>
<td>Create a rectangular matrix with <code>2</code> rows and <code>3</code> columns.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Indexing</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>A(end,2)</code></td>
<td>Access the element in the second column of the last row.</td>
</tr>
<tr>
<td><code>A(2,:)</code></td>
<td>Access the entire second row</td>
</tr>
<tr>
<td><code>A(1:3,:)</code></td>
<td>Access all columns of the first three rows.</td>
</tr>
<tr>
<td><code>A(2) = 11</code></td>
<td>Change the value of the second element an array to <code>11</code>.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Array operations</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<pre>[11;11]*[22;22]
ans=
 44
 44</pre>
</td>
<td>Perform matrix multiplication.</td>
</tr>
<tr>
<td>
<pre>[11;11].*[22;22]
ans=
 22
 22</pre>
</td>
<td>Perform element-wise multiplication.</td>
</tr>
</tbody>
</table>



<div>
<h2>Multiple outputs</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>[xrow,xcol] = size(x)</code></td>
<td>Save the number of rows and columns in <code>x</code> to two different variables.</td>
</tr>
<tr>
<td><code>[xMax,idx] = max(x)</code></td>
<td>Calculate the maximum value of <code>x</code> and its corresponding index value.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Documentation</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>doc randi</code></td>
<td>Open the documentation page for the <code>randi</code> function.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Plotting</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>plot(x,y,"ro-","LineWidth",5)</code></td>
<td>Plot a red (<code>r</code>) dashed (<code>--</code>) line with a<br />circle (<code>o</code>) marker, with a heavy line width.</td>
</tr>
<tr>
<td><code>>hold on</code></td>
<td>Add the next line to existing plot.</td>
</tr>
<tr>
<td><code>hold off</code></td>
<td>Create a new axes for the next plotted line.</td>
</tr>
<tr>
<td><code>title("My Title")</code></td>
<td>Add a label to a plot.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Using tables</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>data.HeightYards</code></td>
<td>Extract the variable <code>HeightYards</code> from<br />the table <code>data</code>.</td>
</tr>
<tr>
<td><code>data.HeightMeters = data.HeightYards*0.9144</code></td>
<td>Derive a table variable from existing data.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Logicals</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>[5 10 15] &gt; 12</code></td>
<td>Compare a vector to the value <code>12</code>.</td>
</tr>
<tr>
<td><code>v1(v1 &gt; 6)</code></td>
<td>Extract all elements in <code>v1</code> that are greater than <code>6</code>.</td>
</tr>
<tr>
<td><code>x(x==999) = 1</code></td>
<td>Replace all values in <code>x</code> that are equal to <code>999</code> with the value <code>1</code>.</td>
</tr>
</tbody>
</table>
<p> </p>
<h2>Programming</h2>
<table>
<thead>
<tr>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<pre><ifx&gt;0.5
 y=3
else
 y=4
end</pre>
</td>
<td>If <code>x</code> is greater than <code>0.5</code>, set the value of <code>y</code> to <code>3</code>.<br /><br />Otherwise, set the value of <code>y</code> to <code>4</code>.</td>
</tr>
<tr>
<td>
<pre>forc=1:3
 disp(c)
end</pre>
</td>
<td>The loop counter (<code>c</code>) progresses through the<br />values <code>1:3</code> (<code>1</code>, <code>2</code>, and <code>3</code>).<br /><br />The loop body displays each value of <code>c</code>.</td>
</tr>
</tbody>
</table>
