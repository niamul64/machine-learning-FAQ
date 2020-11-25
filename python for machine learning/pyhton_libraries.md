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
array([[1., 0., 0., 0.],
       [0., 1., 0., 0.],
       [0., 0., 1., 0.],
       [0., 0., 0., 1.]])


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
log_space_point_distribution.JPG
 <img width="300" src= "pic/log_space_point_distribution.JPG"/> <br>