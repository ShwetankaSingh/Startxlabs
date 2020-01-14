# Startxlabs
Assignment 1
1) Get number of hours, minutes and seconds from number of seconds.
For example :  If number of seconds provided are 129 , then number of hours will be 0 , minutes 2, seconds 9.
Input :  Number of seconds.
Output : “Hours = ‘number of hours’, minutes = ‘number of minutes’ , seconds = ‘number of seconds’ ”

Solution:

<!doctype html>
<html>
<head>
<script>
function fun(){
var a,min,sec,hr;
a=Number(document.getElementById("tos").value);
min=parseInt(a/60);
sec=parseInt(a%60);
hr=parseInt(min/60);
min=parseInt(min%60);
document.getElementById("h").value= hr;
document.getElementById("m").value= min;
document.getElementById("s").value= sec;
}
</script>
</head>
<body>
Enter the number of seconds : <input id="tos">
<br><br>
<button onclick="fun()">Click</button>
<br><br>
Hours:<input id="h">
<br><br>
minutes:<input id="m">
<br><br>
seconds:<input id="s">
</body>
</html>



2) You are given  two numbers L and R, you have to find if XOR of all the numbers in range L to R (L,R both inclusive) is odd or even.
Input:
The first line will contain T, number of testcases.
Each testcase contains a single line of input, two integers L,R.

Output:
For each testcase, in the new line print "Odd" if the XOR in the range is odd, else print "Even".
Sample Input:
  4
  1 4
  2 6
  3 3
  2 3

Sample Output:
  Even
  Even
  Odd
  Odd

Solution :

<!doctype html>
<html>
<head>
<script>
function odd_even(){
var no;
no=Number(document.getElementById("no_input").value);
var inputArray = [];
var outputArray = [];
for(var i=0; i<no; i++) {
	//Taking Input from user
	inputArray[i] = prompt('Enter Elements l & r');
}
for(var i=0;i<no;i++)
{
var e=inputArray[i];
var a=e[0];
var b=e[2];
var d=a;
for(var j=a+1;j<=b;j++)
{
d=d^j;
}
if(d%2==0)
{
outputArray[i]="Even";
}
else
{
outputArray[i]="Odd";
}
}
document.write("Input:"+"<br />");
document.write(no+"<br />");
for (var i = 0; i < no; i++)  
{ 
    document.write(inputArray[i]+"<br />");
} 
document.write("<br />"+"Output:"+"<br />");
for (i = 0; i < no; i++)  
{ 
    document.write(outputArray[i]+"<br />");
} 
}
</script>
</head>
<body>
Enter number of testcases : <input id="no_input"><br />
<button onclick="odd_even()">Click me</button>
</body>
</html>     





3) You are given with T number of strings. You need to sort the strings according to their first character.
Input :
4
“AXXX”
“UVVVV”
“PGGGG”
“BOOUU”

Output :
“AXXX”
“BOOUU”
“PGGGG”
“UVVVV”


Solution:

<script>
function sort(){
var no;
no=Number(document.getElementById("no_input").value);
var inputArray = [];

for(var i=0; i<no; i++) {
	//Taking Input from user
	inputArray[i] = prompt('Enter Element ' + (i+1));
}
document.write("Input:"+"<br />");
for (i = 0; i < no; i++)  
{ 
    document.write(inputArray[i]+"<br />");
} 
inputArray.sort();
document.write("<br />"+"Output:"+"<br />");
for (i = 0; i < no; i++)  
{ 
    document.write(inputArray[i]+"<br />");
} 

}
</script>
</head>
<body>
Enter Number of Strings:<input id="no_input"><br />
<button onclick="sort()">Click me</button>
</body>
</html>
