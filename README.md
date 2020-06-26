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
<td>Create a vector from <code>1</code> to <code>4</code>, spaced by <code>1</code>, using the colon (:)</a> operator.</td>
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




	
 

Evenly-spaced vectors
Example	Description
1:4	Create a vector from 1 to 4, spaced by 1, using the colon (:) operator.
1:0.5:4	Create a vector from 1 to 4, spaced by 0.5.
linspace(1,10,5)	Create a vector with 5 elements. The values are evenly spaced from 1 to 10.
 

Creating matrices
Example	Description
rand(2)	Create a square matrix with 2 rows and 2 columns.
zeros(2,3)	Create a rectangular matrix with 2 rows and 3 columns.
 

Indexing
Example	Description
A(end,2)	Access the element in the second column of the last row.
A(2,:)	Access the entire second row
A(1:3,:)	Access all columns of the first three rows.
A(2) = 11	Change the value of the second element an array to 11.
 

Array operations
Example	Description
[1 1; 1 1]*[2 2;2 2]
ans =
     4     4
     4     4	Perform matrix multiplication.
[1 1; 1 1].*[2 2;2 2]
ans =
     2     2
     2     2	Perform element-wise multiplication.
 

Multiple outputs
Example	Description
[xrow,xcol] = size(x)	Save the number of rows and columns in x to two different variables.
[xMax,idx] = max(x)	Calculate the maximum value of x and its corresponding index value.
 

Documentation
Example	Description
doc randi	Open the documentation page for the randi function.
 

Plotting
Example	Description
plot(x,y,"ro-","LineWidth",5)	Plot a red (r) dashed (--) line with a
circle (o) marker, with a heavy line width.
hold on	Add the next line to existing plot.
hold off	Create a new axes for the next plotted line.
title("My Title")	Add a label to a plot.
 

Using tables
Example	Description
data.HeightYards	Extract the variable HeightYards from
the table data.
data.HeightMeters = data.HeightYards*0.9144	Derive a table variable from existing data.
 

Logicals
Example	Description
[5 10 15] > 12	Compare a vector to the value 12.
v1(v1 > 6)	Extract all elements in v1 that are greater than 6.
x(x==999) = 1	Replace all values in x that are equal to 999 with the value 1.
 

Programming
Example	Description
if x > 0.5
    y = 3
else
    y = 4
end	If x is greater than 0.5, set the value of y to 3.

Otherwise, set the value of y to 4.
for c = 1:3
    disp(c)
end	The loop counter (c) progresses through the
values 1:3 (1, 2, and 3).

The loop body displays each value of c.
