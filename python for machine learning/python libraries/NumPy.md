python libraries for machine learning
<br>
1. NumPy (নামপি)<br>
2.matplatlib<br>
3.SciPy<br>
etc.<br>

<br><br><br><br>code / commands: <br><br>
1.NumPy: (NumPy হল একটি linear algebra library , fast calulate)<br>
to check numpy is instaled or not? :  !pip install numpy<br>
if not then :   pip install numpy<br>
to import and use numpy library : import numpy as np  # np == numpy<br>
 
<br>

arr=np.array([1,2,3,4])  #creating numpy array
<br>
or,
<br>
if we make a nested array: then,<br> <br>

puthon_list=[[1,2,3,4],[6,7,8,9]]<br>
arr=np.array(python_list)<br>
here the out put will be like a matrix <br>
<br><br>
####Now,<br>
'arange' a function in numpy libreries. <br>
it usded to make numpy array in a range of numbers.<br>
now, arange has 3 parameters.<br>
(start,end, step_size) <br>
if step size is not given the default is 1<br>
<br>
<br>
arrr=np.arange(0,10,2)<br>
arrr<br>
<br>
<br>
যদি  এমন একটা matrix বানাতে হই যেখানে matrix এর সব ০ তাহলে, function আছে, 'zeros' যেখানে ২ টা parameter আছে. parameter হিসেবে যদি ১টা নাম্বার দেই, যেমন ৫, তাহলে সুধু ৫টা ০ দিয়ে row matrix বানাবে<br>

যদি ২টা parameter ইই দেই তবে ১ম টা row , পরের টা column.<br>
তবে ২তাইই ((row, column )) double ব্রাকেট এর মদ্ধে থাকবে।<br><br>
print(np.zeros(5))<br>
print()<br>
np.zeros((3,4))<br><br><br>



তবে এখানে সব floating point এ আছে।
<br>
ইন্তেগের করতে হোলে<br>
np.zeros((4,3),dtype="int" )<br><br><br><br>


এখন, 'zeros' এর মত 'ones' একটা function আছে।<br>

np.ones((4,3)) <br><br><br>

আরেক টা function আছে 'full'<br>
np.full((row,column), 10)<br>
তাহলে row, column সব ১০ দারা fill হবে <br><br>
np.full((3,4), 10)<br>
or,<br><br>
1d matrix এর জন্ন<br> 
np.full(5, 10) <br> <br>
<br> <br>

identity matrix:<br>
eye(row)<br>
<br><br>
output:<br><br>
array([[1., 0., 0., 0.],<br>
       [0., 1., 0., 0.],<br>
       [0., 0., 1., 0.],<br>
       [0., 0., 0., 1.]])<br>


<br><br><br>
এখন একটি গুরুত্তপুরন function:
<br>
<strong>'linspace'</strong>
<br>
np.linspace(start,end, divide)
এখানে start= 0 হোলে এবং end=10 হোলে এবং divide=5 হোলে,<br>
০ থেকে ১০ এর মধ্যে ৫ ভাগে ভাগ হয়ে <br>
[0. , 2.5 , 5. , 7.5 , 10. ]
<br>
বেপারটা এমন যে,<br>
একটা সরল রেখা আক্তে হবে যার স্থানাঙ্ক ০ থেকে ১০
<br>
এখন এর মধ্যে সমান ৫ টা পয়েন্ট বের করতে হবে। তাহলে point গুলা হবে ঃ <br>
np.linspace(০,১০,৫) <br>
[0. , 2.5 , 5. , 7.5 , 10. ]<br>

<br><br>
code: np.linspace(-1,1,10) <br>
output:array([-1.        , -0.77777778, -0.55555556, -0.33333333, -0.11111111, 0.11111111,  0.33333333,  0.55555556,  0.77777778,  1.        ])

<br><br><br><br>
এবার log_space দিয়ে evenly distribution
<br> <strong> 'logspace' function</strong><br>
'linspace' এর মতইই just extra একটা পারামেটার আছে function  এ , 'base' <br>
যেটা , result কত base Log দেখতে চাচ্ছি তা নির্দেশ করে or, exp এও দেখা যাবে<br>
আর এই পারামেটার ছাড়া হোলে by default base 10 এএ দেখাবে
<br><br>
np.logspace(0,10,5) # here,(log_base 10) base =10<br>
np.logspace(0,10,5, base =2) # here,(log_base 2) base =2<br>
np.logspace(0,10,5, base =np.e ) # here,(log_base epsilon) base =epsilon<br><br>

<br>

 <img width="450" src= "pic/log_space_point_distribution.JPG"/> <br>
 <br><br><br>
<strong> diagonal matrix making function 'diag':</strong><br>
code: np.diag([1,2,3])
output: array([[1, 0, 0],
              [0, 2, 0],
              [0, 0, 3]])


<br><br><br>
<strong>Random Number: </strong><br>
random number generating function<br>
np.random.rand(4) #1d matrix<br>
np.random.rand(4,3) #2d matrix<br>
np.random.rand(4,4,4) #3d matrix<br>

code:<br>
print(np.random.rand(4)) #1d matrix<br>
print("")<br>
print("")<br>
print(np.random.rand(2,2)) #2d matrix<br>
print("")<br>
print("")<br>
print(np.random.rand(2,2,2)) #3d matrix)<br>
print("")<br>
print("")<br><br>

output: <br>
[0.47174969 0.61137453 0.50886639 0.36165707]<br>
<br><br>

[[0.55637462 0.30024987]<br>
 [0.4895491  0.73093113]]<br>

<br><br>
[[[0.7173619  0.61072548]<br>
  [0.93320895 0.89540955]]<br>

 [[0.41259348 0.95140771]<br>
  [0.50621412 0.76924433]]]<br>


   
<br><br><br>
<strong> make array of random integer numbers:</strong><br>
<br> sample:<br>
np.random.randint(lower limit,lower limit +1 ,কয় টা সংখ্যা লাগবে )
<br> np.random.randint(0,10,10 ) <br>
<img width="450" src= "pic/randint.JPG"/> <br>
<img width="450" src= "pic/2d matric randint.JPG"/> 
<br>
<br><br>

# now
we can reshape the matrix. By 'reshape()'
<br>

#### code:
arr=np.random.randint(0,10,10 )<br>
arr # first making a 1d matrix<br>
arr.reshape(2,5) #re shape the array <br>
#### output:
array([8, 9, 1, 6, 0, 8, 7, 0, 1, 2])<br><br><br>
array([[8, 9, 1, 6, 0],<br>
       [8, 7, 0, 1, 2]])<br>

### or
#### code:
arr=np.random.randint(0,10,(4,3) )<br>
print(arr) # first making a 1d matrix<br>
#re shape the array<br>
print() <br>
print() <br>
arr= arr.reshape(2,6)<br>
print(arr) <br>
#### output:
[[7 6 0]<br>
 [9 1 9]<br>
 [4 8 2]<br>
 [8 2 6]]<br>
<br><br>

[[7 6 0 9 1 9]<br>
 [4 8 2 8 2 6]]<br>


 <br>


### more use of re shape or reshape
### code:
arr = np.arange(1,13).reshape(4,3)<br>
arr2 = np.arange(1,13).reshape(4,3)<br>
print(arr)<br>
### output:
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]

<br><br><br>

### এখন matrix এর মধ্যে ম্যাক্সিমাম value or minumum value or max vlue টা আমার কথায় আছে (index of max value) :
<br>

#### code:
arr=np.random.randint(0,10,(2,6) ) # making a random matrix<br>
print(arr)<br>
print()<br>
print ('max: ',arr.max()) #finds maximum number in the array<br>
print ('index :' ,arr.argmax()) #finds the index of maximum number in the array<br>
print("",end="\n\n")<br>
print ('min: ',arr.min()) #finds min number in the array<br>
print ('index :' ,arr.argmin()) #finds the index of mim number in the array<br>
#### output:
[[8 0 1 8 7 7]<br>
 [5 4 4 9 7 5]]<br>
<br><br>
max:  9<br>
index : 9<br>
min:  0<br>
index : 0<br>
<br><br>

### matrix shape finding / কয় dimention array(1d,2d,3d)?
arr=np.random.randint(0,10,(2,6) ) # making a random matrix<br>
arr.shape ## shape finding<br>

arr.ndim  #কয় dimention array(1d,2d,3d)?<br>

arr.size  #total elements<br>
<br><br>

### data type of a matrix elements
arr=np.random.randint(0,10,(2,6) )<br>
arr.dtype<br>
arr=np.random.rand(2,6)<br>
arr.dtype<br>
<br>
<strong>access a value from 2d matrix</strong>
arr[2][2]<br>
অথবা,<br>
arr[2,2]<br>



<br><br>

### equals to in numpy
#### arr2 = arr  #এটা copy হই না । address pass হই
<br><br>

## to copy array : 

### arr2 =arr.copy()

<br><br>

## selection (select a part of a matrix and make sub matrix):
<img width="450" src= "pic/selection.JPG"/> <br>

#### input:
arr=np.random.randint(0,10,(5,7) )<br>
print(arr)<br>
print()<br>
arr[:2,1:]<br>

#### output:
[[6 5 2 0 0 4 2]<br>
 [4 8 8 5 7 6 2]<br>
 [4 7 7 8 6 2 0]<br>
 [5 0 7 6 3 2 0]<br>
 [0 4 5 9 7 5 2]]<br>

array([[5, 2, 0, 0, 4, 2],<br>
       [8, 8, 5, 7, 6, 2]])<br>
       

## selection (conditional selection):
<img width="450" src= "pic/conditional selection.JPG"/> <br>
arr=np.random.randint(0,10,(5,7) )<br>
print(arr)<br>
print()<br>
print(arr>4)<br>
print()<br>
print(arr[arr>4])<br>
<br><br><br>

### here we can find the all function about numpy arithmatic operations: 
<a src="## https://docs.scipy.org/doc/numpy/reference/ufuncs.html">## https://docs.scipy.org/doc/numpy/reference/ufuncs.html </a>
<br><br><br>

## arethmatic sum of 2 matrix
<br>

#### code:
arr=np.random.randint(0,10,(5,7) )<br>
print(arr)<br>
print()<br>
print(arr+arr)<br>
#### output:
[[5 7 9 6 1 7 3]<br>
 [3 4 5 3 3 3 5]<br>
 [3 1 0 9 1 3 7]<br>
 [5 6 8 9 0 4 3]<br>
 [6 5 2 9 4 0 2]]<br>

[[10 14 18 12  2 14  6]<br>
 [ 6  8 10  6  6  6 10]<br>
 [ 6  2  0 18  2  6 14]<br>
 [10 12 16 18  0  8  6]<br>
 [12 10  4 18  8  0  4]]<br>
 <br>
 same vabe '-', '*', '/'  kora jay
  <br>
 <br>more use: <br>
 arr = np.arange(1,13).reshape(4,3) <br>
arr2 = np.arange(0,12).reshape(4,3) <br>
 <br>
print(arr/arr2) <br>
 
 <br><br><br>

