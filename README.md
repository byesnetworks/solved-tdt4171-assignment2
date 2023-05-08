Download Link: https://assignmentchef.com/product/solved-tdt4171-assignment2
<br>
<h1>1       Hidden Markov Model</h1>

Some tourists are curious if there are fish in a nearby lake. They are unable to observe whether this is true or not by staring into the lake. However, they can observe whether or not there are birds nearby that a↵ect the presence of fish. Based on their instincts, the tourists propose the following domain theory:

<ol>

 <li>The prior probability of fish nearby (that is, without any observation) is 0<em>.</em></li>

 <li>The probability of fish nearby on day <em>t </em>is 0<em>.</em>8 given there are fish nearby on day <em>t </em>1, and 0<em>.</em>3 if not.</li>

 <li>The probability of birds nearby on day <em>t </em>if there are fish nearby on the same day is 0<em>.</em>75, and 0<em>.</em>2 if not.</li>

</ol>

The following evidence is given

<table width="412">

 <tbody>

  <tr>

   <td width="227">•   <strong>e</strong><sub>1 </sub>= {birds nearby}•   <strong>e</strong><sub>2 </sub>= {birds nearby}•   <strong>e</strong><sub>3 </sub>= {no birds nearby}</td>

   <td width="185">•   <strong>e</strong><sub>4 </sub>= {birds nearby}•   <strong>e</strong><sub>5 </sub>= {no birds nearby}•   <strong>e</strong><sub>6 </sub>= {birds nearby}</td>

  </tr>

 </tbody>

</table>

We will denote the state variable for fish nearby on day <em>t </em>by <em>X<sub>t</sub></em>.

<h2>Instructions</h2>

Use programming to solve all exercises in this section involving computation. The results need to be extracted from the program and well documented in a human-readable format that is easy to understand in a PDF file. Additionally, write a few sentences to give the results some context. The results can, for example, be plotted using Matplotlib [1] to give a more straightforward overview.

The code must be runnable without any modifications after delivery. Moreover, the code must be readable and contain comments explaining it. We recommend that Python with the package NumPy [2] be used for the programming exercises. It is not allowed to use libraries, such as Scikit-learn [3] to solve the tasks.

<h2>Problems</h2>

<ul>

 <li>Formulate the information given above as a hidden Markov model, and provide the complete probability tables for the model.</li>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,…,</em>6<em>.                                                           </em>(1)

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:6</sub>)<em>, </em>for <em>t </em>= 7<em>,…,</em>30<em>.                                                          </em>

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us. What happens to the distribution in Equation (2) as <em>t </em>increases?

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:6</sub>)<em>, </em>for <em>t </em>= 0<em>,…,</em>5<em>.                                                           </em>

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<ul>

 <li>Compute</li>

</ul>

argmax <strong>P</strong>(<em>x</em><sub>1</sub><em>,…,x<sub>t </sub></em><sub>1</sub><em>,X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,…,</em>6<em>.                                             </em>

<em>x</em>1<em>,…,x<sub>t </sub></em><sub>1</sub>

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<h1>2       Dynamic Bayesian Network</h1>

<h2>5 points</h2>

Some tourists visiting a cabin are interested in finding out if there are animals nearby. They can observe outside of their window every day whether there are animal tracks and whether the food they placed outside is gone. Furthermore, they believe that the animal tracks and the food placed outside are conditionally independent given animals nearby (<em>AnimalTracks<sub>t </sub></em>?? <em>FoodGone<sub>t </sub></em>| <em>AnimalsNearby<sub>t</sub></em>). Based on gut feelings, the tourists provide the following domain theory:

<ol>

 <li>The prior probability of animals nearby (that is, without any observation) is 0<em>.</em></li>

 <li>The probability of animals nearby on day <em>t </em>is 0<em>.</em>8 given that there were animals nearby on day <em>t </em>1, and 0<em>.</em>3 if not.</li>

 <li>The probability of animal tracks on day <em>t </em>if there are animals nearby on the same day is 0<em>.</em>7, and 0<em>.</em>2 if not.</li>

 <li>The probability of the food gone on day <em>t </em>if there are animals nearby on the same day is 0<em>.</em>3, and 0<em>.</em>1 if not.</li>

</ol>

The following evidence is given

<ul>

 <li><strong>e</strong><sub>1 </sub>= {animal tracks<em>,</em>food gone} <strong>e</strong><sub>3 </sub>= {no animal tracks<em>,</em>food not gone}</li>

 <li><strong>e</strong><sub>2 </sub>= {no animal tracks<em>,</em>food gone} <strong>e</strong><sub>4 </sub>= {animal tracks<em>,</em>food not gone}</li>

</ul>

We will denote the state variable for animals nearby on day <em>t </em>by <em>X<sub>t</sub></em>.

<h2>Instructions</h2>

Solve by hand all exercises in this section involving computation, not by programming. The results must be accompanied by steps to solve them and justifications, not only the final results.

<h2>Problems</h2>

(a) Formulate the information given above as a dynamic Bayesian network and provide the complete probability tables for the model.

<table width="527">

 <tbody>

  <tr>

   <td width="512">(b) Compute</td>

   <td width="16"> </td>

  </tr>

  <tr>

   <td width="512"><strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,</em>2<em>,</em>3<em>,</em>4<em>.</em>(c) Compute</td>

   <td width="16">(5)</td>

  </tr>

  <tr>

   <td width="512"><strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:4</sub>)<em>, </em>for <em>t </em>= 5<em>,</em>6<em>,</em>7<em>,</em>8<em>.</em></td>

   <td width="16">(6)</td>

  </tr>

 </tbody>

</table>

(d) By forecasting further and further into the future, you should see that the probability converges towards a fixed point. Verify that

<table width="526">

 <tbody>

  <tr>

   <td width="510"><em>t</em>!1 | h i lim <strong>P</strong>(<em>X<sub>t </sub></em><strong>e</strong><sub>1:4</sub>) = 0<em>.</em>6<em>,</em>0<em>.</em>4 <em>.</em>(e) Compute</td>

   <td width="16">(7)</td>

  </tr>

  <tr>

   <td width="510"><strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:4</sub>)<em>, </em>for <em>t </em>= 0<em>,</em>1<em>,</em>2<em>,</em>3<em>.</em></td>

   <td width="16">(8)</td>

  </tr>

 </tbody>

</table>

<h1>References</h1>

<ul>

 <li>D. Hunter. Matplotlib: A 2d graphics environment. <em>Computing in Science &amp; Engineering</em>, 9(3):90–95, 2007.</li>

 <li>Charles R. Harris, K. Jarrod Millman, St´efan J van der Walt, Ralf Gommers, Pauli Virtanen, David Cournapeau, Eric Wieser, Julian Taylor, Sebastian Berg, Nathaniel J. Smith, Robert Kern,</li>

</ul>

Matti Picus, Stephan Hoyer, Marten H. van Kerkwijk, Matthew Brett, Allan Haldane, Jaime Fern´andez del R´ıo, Mark Wiebe, Pearu Peterson, Pierre G´erard-Marchant, Kevin Sheppard, Tyler Reddy, Warren Weckesser, Hameer Abbasi, Christoph Gohlke, and Travis E. Oliphant. Array programming with NumPy. <em>Nature</em>, 585:357–362, 2020.

<ul>

 <li>Pedregosa, G. Varoquaux, A. Gramfort, V. Michel, B. Thirion, O. Grisel, M. Blondel, P. Prettenhofer, R. Weiss, V. Dubourg, J. Vanderplas, A. Passos, D. Cournapeau, M. Brucher, M. Perrot, and E. Duchesnay. Scikit-learn: Machine learning in Python. <em>Journal of Machine Learning Research</em>, 12:2825–2830, 2011.</li>

</ul>