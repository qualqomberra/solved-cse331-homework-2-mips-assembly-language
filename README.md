Download Link: https://assignmentchef.com/product/solved-cse331-homework-2-mips-assembly-language
<br>
In this assignment you will write a MIPS assembly program and test it using MARS instruction set simulator.

You will be given an integer array <strong>arr</strong> and a number <strong>num</strong>. The task is to find if a subset of array elements can sum up to the target <strong>num</strong>. If not possible you will output “Not possible!”. If it is possible, output “Possible!”. You can use every array element only once. Only positive integers are allowed as array elements. Finding only one combination is enough to output “Possible!”.

<ol>

 <li> In C++, you will write a recursive function named <strong>CheckSumPossibility</strong> as below:</li>

</ol>

int CheckSumPossibility(int num, int arr[], int size)

The function respectively gets the target number, the array and the size of the array. It returns 1 if a subset of the array can sum up to the target number and otherwise if it is not possible it outputs a 0. The sample output for six sample runs with 8 element array examples is as shown below. The numbers in parenthesis (black text) are for showing the possibility. Blue text is user input, red text is program output. 8 is the array size, 129 is the target number:

8 129

41 67 34 0 69 24 78 58

Not possible!

8 129

62 64 5 45 81 27 61 91

Not possible!

8 129

95 42 27 36 91 4 2 53

Possible! (36 91 2)

8 129

92 82 21 16 18 95 47 26

Possible! (92 21 16)

8 129

71 38 69 12 67 99 35 94

Possible! (35 94)

8 129

3 11 22 33 73 64 41 11   Not possible!

The main function is as below:

<table width="582">

 <tbody>

  <tr>

   <td width="582"> int main(){     int arraySize;     int arr[MAX_SIZE];     int num;     int returnVal;cin &gt;&gt; arraySize;     cin &gt;&gt; num;for(int i = 0; i &lt; arraySize; ++i){         cin &gt;&gt; arr[i];}          returnVal = CheckSumPossibility(num, arr, arraySize);if(returnVal == 1){         cout &lt;&lt; “Possible!” &lt;&lt; endl;}     else     {                 cout &lt;&lt; “Not possible!” &lt;&lt; endl;}return 0;}</td>

  </tr>

 </tbody>

</table>




<ol start="2">

 <li>(70pts) Write your program in MARS assembly with the guidance of the C++ code you wrote for part 1. You will read the input array from the console as shown in above <strong>main()</strong>.</li>

</ol>



















RULES:

<ul>

 <li>You can use pseudo instructions in MARS.</li>

 <li>Comment your assembly using your C++ code. For instance:</li>

</ul>




<ul>

 <li>Obey the contract, which defines the usage of MIPS registers.</li>

 <li>You have to write <strong>CheckSumPossibility</strong> as a procedure in assembly.</li>

 <li>Recursive backtracking implementation will get full credit. Any other accurately working implementation will get -15pts.</li>

 <li>For possible cases, if you also print the corresponding array elements in your assembly program (similar to shown in parenthesis in the above sample output) you get 10 extra points.</li>

 <li>For recursive backtracking you can check the lecture given by Marty Stepp from Stanford University:</li>

</ul>

<a href="https://youtu.be/cR8YjEJrb-A">https://youtu.be/cR8YjEJrb</a><a href="https://youtu.be/cR8YjEJrb-A">–</a><a href="https://youtu.be/cR8YjEJrb-A">A</a>

<ul>

 <li>Anyone using a compiler instead of writing the assembly manually will get 0pts.</li>

 <li>Do not cheat, do not help anyone either. Otherwise both sides will get 0pts.</li>

</ul>

Hint for C++ part, which also affects the assembly program:

<ol>

 <li>Actually the recursive backtracking is an easier solution. An accurate implementation of the <strong>CheckSumPossibility</strong> function is even less than 20 lines of C/C++ code.</li>

 <li>As an optimization,

  <ol>

   <li>you must ignore the next recursive calls when the sum exceeded the target number <strong>num</strong>.</li>

   <li>your program should stop when only one possible combination is found.</li>

  </ol></li>

 <li>You do not need any other helper function than the</li>

</ol>

<strong>CheckSumPossibility</strong> function.








