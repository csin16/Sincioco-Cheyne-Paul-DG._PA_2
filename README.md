_Cheyne Paul DG. Sincioco-2ECEA_PA-2_

_PA#2 NUMERICAL PYTHON (NUMPY)_

# __About the Programming Assignment__

This programming assignment aims to hone our skills in making different arrays. This task requires us to create various arrays and apply them to different problems. 
-------------------------------------------------------------------------------------------------------------------------------------------
1. __NORMALIZATION PROBLEM: In this problem, create a random 5 x 5 ndarray and store it in a variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy. Normalization is one of the most basic preprocessing techniques in data analytics. This involves the centering and scaling process. Centering means subtracting the data from the mean, and scaling means dividing by its standard deviation.__
   
__Code__
```
import numpy as np
X = np.random.random((5,5)) #create a randomized 5x5 array
Z = ((X - X.mean())/X.std()) #normalize each element in the array
np.save('X_normalized.npy',Z)
Y = np.load("X_normalized.npy")
print ("Normalized ndarray")
print (Y)
```
__Description__: This problem shows the use of a randomized ndarray. With the use of numpy to create arrays, variable X was used to store a randomized 5x5 array __X = np.random.random((5,5))__. Then the computed mean __X.mean()__ of all the elements was subtracted from each element in the array, and was divided by the computed standard deviation __X.std()__. 

__Example:__
```
Output:
Normalized ndarray
[[-0.83146983  1.44805869  0.18237473 -1.67843109 -0.04263363]
 [-0.65749699  1.46537768  0.43235874 -1.28961128  0.17113216]
 [-1.42770585 -0.38290863  1.02248893 -1.61408889  1.23089544]
 [ 0.043057    0.00859165  0.66907931 -0.83896047  0.8401589 ]
 [ 1.47394395 -0.66175132  0.35792072 -1.17443278  1.25405282]]
```
-------------------------------------------------------------------------------------------------------------------------------------------
2. __DIVISIBLE BY 3 PROBLEM: Create the following 10 x 10 ndarray, which is the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy__
   
__Code__
```
i = 1
A = [] #list for squared numbers
B = [] #list for divisible numbers

for i in range (1,101): #loop to get the square from 1 to 100
    squared = i**2
    A.append(squared) #store squared numbers into the square list
    if i % 3 == 0: #condition to store a number into the divisible list
        B.append(squared)
        
sq = np.array(A) #store the square list into sq array
sq.resize(10,10) #resize the array into 10x10
div = np.array(B) #store the divisible list into div array
div.resize(3,11)

print("10x10 Squared Array")
print(sq)

np.save('div_by_3.npy',div)
C = np.load("div_by_3.npy")
print ("Divisible by 3")
print (C)
```
__Description__: This problem also shows the use of an array. With the use of A __A = []__ and B __B = []__ as lists to store each number, a for loop __for i in range (1,101)__ was used to store numbers ranging from 1 to 100. Then, each number in the loop was squared __squared = i**2__ and was put in list A __A.append(squared)__. An if statement was utilized to get the numbers divisible by 3 __if i % 3 == 0__ and was put in list B __B.append(squared)__. After that, lists A and B __sq = np.array(A) div = np.array(B)__ were stored into arrays sq and div and were resized to 10x10 __sq.resize(10,10)__ and 3x10 __div.resize(3,11)__.

__Example:__
```
Output:
10x10 Squared Array
[[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]
Divisible by 3
[[   9   36   81  144  225  324  441  576  729  900 1089]
 [1296 1521 1764 2025 2304 2601 2916 3249 3600 3969 4356]
 [4761 5184 5625 6084 6561 7056 7569 8100 8649 9216 9801]]
```
-------------------------------------------------------------------------------------------------------------------------------------------
__Lessons Learned__:

This programming assignment taught me to use arrays in different ways. It taught me to make use of various types of attributes in an array. Using loops to store numbers in it or generating random numbers. This prograaming assignment expanded my knowledge in coding.

__Tech(s) Used__: Jupyter Notebook
