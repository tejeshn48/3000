# FUNCTION TOOLS

The functools module, which is included in Python’s standard library, provides essential functionality for working with high-order functions (a function that returns a function or takes another function as an argument ). You can reuse or enhance the utility of your functions or callable objects without having to rewrite them using these capabilities. This simplifies the process of building reusable and maintainable code.
The functools module has 11 functions in the current stable release, They are as follows:

* reduce()
* lru_cache()
* partial()
* partial method()
* single dispatch()
* singledispatchmethod()
* cached_property()
* total_ordering()
* update_wrapper()
* wraps()
* cmp_to_key()

## Reduce():
A function and an iterable are passed to the reduce(function, sequence) function. It applies the supplied function to all members of the iterable in a cumulative manner from left to right before returning a single value.
```
Syntax : reduce(function, sequence[, initial]) -> value
```

## lru cache()
Is a decorator that wraps a function in a memoizing callable that saves up to maximize the results of a function call and returns the stored value when the function is called again with the same inputs. When an expensive or I/O bound function is called repeatedly with the same arguments, it can save time.
It primarily employs two data structures: a dictionary to map a function’s parameters to its output and a linked list to maintain track of the function.
```
Syntax : lru_cache(maxsize=128, typed=False)
```

## Partial():

Partial functions are derived functions with some input parameters that have already been assigned. The partial() method in Function is used to construct partial functions/objects, which is an important feature because it allows for:

Replication of existing functions with some parameters already set.
In a well-documented manner, create a newer version of an existing function.
The partial function also has valuable characteristics that can be used to track partial functions and objects. These are some of them:
* args - Returns the preassigned positional arguments to the partial function.
* keywords - Returns the pre-assigned keyword arguments to the partial function.
* func - Returns the name of the parent function as well as its location.
```
Syntax : partial(func, /, *args, **keywords)
```

##### EX :
Using the conventional function

def squared(num):
return pow(num, 2)
print(list(map(squared, range(0, 10))))

##### OUTPUT:
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

##### EX:
using partial() from the functools

from functools import partial
print(list(map(partial(pow, exp=2), range(0, 10))))

##### OUTPUT :
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

## Partialmethod():

A method specification rather than a callable method. You can think of it as a method’s partial(). The partial method() method provides a new partial method descriptor, which is similar to partial but is intended to be used as
```
syntax :  partial method(func, *args, **keywords)
```
    
## Single dispatch():

The first is a generic function, which is a function made up of numerous functions that all perform the same task for different types. The dispatch algorithm determines which implementation will be utilized during a call.

The second is the Single dispatch, which is a type of generic function dispatch in which the implementation is determined by a single argument’s type.
With this in mind, the single dispatch decorator in the functool converts a basic function into a generic function whose behavior is determined by the type of its first parameter. 

## Single dispatch_method():

It’s a decorator that works in the same way as @singledispatch, but for methods instead of functions.

## Cached_Property():

The cached property() decorator changes a class method into a property whose value is calculated only once and then cached as a normal attribute throughout the life of the instance, as the name suggests. Except for the caching functionality, it’s comparable to @property. It’s handy for attributes of instances that are normally functionally permanent but are computationally expensive.

## Total_Ordering():

If you want to make a class that compares different numbers, for example. All of the rich comparison methods would almost certainly need to be implemented. However, because this is likely to be tiresome and unnecessary, you can just implement the eq and gt methods and rely on total ordering to fill in the gaps.

## Update_Wrapper():

It makes a wrapper function’s metadata look like the wrapped function. In the case of partial functions, the updated wrapper(partial, parent) will update the partial function’s documentation( doc ) and name( name ) to match the parent function’s.
```
Syntax :  update_wrapper(wrapper, wrapped[, assigned][, updated])
```
     
## Wraps():

It’s just a shortcut for calling the updated wrapper() on the decorated function. It’s the same as calling partial(update wrapper, wrapped=wrapped, assigned=assigned, updated=updated, wrapped=wrapped).

## Cmp_to_key():

It converts a key function from an old-style comparison function. Any callable that accepts two parameters, compares them, and returns a negative number for less-than, zero for equality, or a positive number for greater-than is referred to as a comparison function. The operator. item getter() key function is an example of a callable that accepts one argument and returns another value to be used as the sort key. Tools like sorted(), min(), max(), and itertools. group by using key functions ().
```
Syntax: function(iterable, key=cmp_to_key(cmp_function)) 
```
    
    
# Itertools

Itertool is one of the most amazing Python 3 standard libraries. Python provides excellent documentation of the itertools but in this tutorial, we will discuss a few important and useful functions or iterators of itertools The key thing about itertools is that the functions of this library are used to make memory-efficient and precise code


Before learning the Python itertools, you should know the Python iterator and generators. In this article, we will describe itertools for beginners are well as for professionals.

“This module implements some iterator building blocks inspired by constructs from APL, HASKELL, and SML
In simple words, the number of iterators can together create ‘iterator algebra’ which makes it possible to complete the complex task. The functions in itertools are used to produce more complex iterators. Let’s take an example: Python built-in zip() function

Accepts any number of arguments as iterable. It iterates over tuples and returns their corresponding elements

##### EX :

a = [1,2,3]
b= [‘a’, ‘b’, ‘c’]
c = zip(a,b)
print©
Output :
[(1, ‘a’), (2, ‘b’), (3, ‘c’)]
[(1, ‘a’), (2, ‘b’), (3, ‘c’)]

 In the above code, we have passed two lists [1,2,3] and [‘a’, ‘b’, ‘c’] as iterable in the zip() function. These lists return one element at a time. In Python an element that implement .iter() method called iterable.

## The Python zip() function
calls iter() on each of its argument and then calls next() by combining the result into tuple

### Types of Iterator

There are various types of iterators in the itertools module. The list is given below:

* Infinite iterators
* Combinatoric iterators
* Terminating iterators

## Infinite Iterators

Any object that can implement for loop is called an iterator. Lists, tuples, set, dictionaries, and strings are an example of iterators but iterator can also be infinite and this type of iterator is called an infinite iterator
Iterator

1.Argument
2.Results

 1.count(start,step)
start, [step]
start, start+step, step+2*step

2.cycle()
P
p0,p1,….plast

3.repeat()
Elem [,n]
Elem, Elem, Elem,….endlessly or up to n times

### 1. Count(start, stop):
It prints from the start value to infinite. The step argument is optional, if the value is provided to the step then the number of steps will be skipped.

##### EX :
import itertools
for I in itertools.count(10,5):
if i == 50:
break
else:
print(i,end=" ")

##### OUTPUT :
10 15 20 25 30 35 40 45

### 2.Cycle(iterable):
This iterator prints all values in sequence from the passed argument. It cyclically prints the values. Consider the following example:

##### EX :
import itertools
temp = 0
for I in itertools.cycle(“123”):
if temp > 7:
break
else:
print(i,end=’ ')
temp = temp+1

##### OUTPUT:
1 2 3 1 2 3 1 2 3 1 2

### 3.Repeat(Val, num):
As the name suggests, it repeatedly prints the passed value for an infinite time. A num argument is an option.

## Combinatoric iterator
The complex combinatorial constructs are simplified by the recursive generators. The permutations, combinations, and Cartesian products are an example of the combinatoric construct.
In Python, there are four types of combinatoric iterators:

### 1. Product():
It is used to calculate the cartesian product of input iterable. In this function, we use the optional repeat keyword argument for the computation of the product of an iterable with itself. The repeat keyword represents the number of repetitions. It returns output in the form of sorted tuples

### 2. Permutations():
It is used to generate all possible permutations of an iterable. The uniqueness of each element depends upon its position instead of values. It accepts two arguments iterable and group_size. If the value of group_size is none or not specified then group_size turns into the length of the iterable.

### 3. Combinations():
It is used to print all the possible combinations (without replacement) of the container which is passed as an argument in the specified group size in sorted order

### 4. Combination_with_replacement():
It accepts two arguments, the first argument is an r-length tuple and the second argument is repetition. It returns a subsequence of length n from the elements of the iterable and repeats the same process. Separate elements may repeat themselves in combination_with_replacement()

## Terminating iterator

erminating iterators are generally used to work on the small input sequence and generate the output based on the functionality of the method used in an iterator.
There are different types of terminating iterators:

1.  Accumulate(iter, func): It takes two arguments, the first argument is iterable and the second is a function that would be followed at each iteration of value in iterable. If the function is not defined in an accumulate() iterator, addition takes place by default. The output iterable depends on the input iterable; if the input iterable contains no value then the output iterable will also be empty.

2.  Drop while(func, seq) - It starts printing the character only after the func.

3.  Filter false(func,seq) - We can assume it by its name, as this iterator prints only those values that return false for the passed function.

4. Islice(iterable, start, stop, step) - It slices the given iterable according to a given position. It accepts four arguments respectively and these are iterable, container, starting pos., ending position, and step(optional).

5. Starmap(func, tuple list) - It takes two arguments; the first argument is function and the second argument is a list that consists of elements in the form of a tuple.

6.  Take while(func, iterable) - It is visa-versa of drop while(). It will print values until it returns a false condition.

7. Tee(iterator, count) - It divides the container into some iterators which are defined in the argument.

8. Zip_longest(iterable1, iterable2, fillval) - It prints the values of iterable alternatively in sequence. If one of the iterable prints all values, the remaining values are filled by the values assigned to fill the value


# TQDM
  
  TQDM : total quality data management
  
Tqdm got its name from the Arabic name tqdm which means ‘progress’. tqdm is a library in Python which is used for creating Progress Meters or Progress Bars. tqdm got its name from the Arabic name taqaddum which means ‘progress’. Implementing tqdm can be done effortlessly in our loops, functions, or even Pandas. bars are pretty useful Progress in Python because:

## Using TQDM
tqdm gives a console kind of progress bar for our processes. Using tqdm is a straightforward process explained in the following steps

First, we need to install our required library tqdm. Open a New Jupyter Notebook and execute
This will complete the installation of tqdm. Restart the Kernel to start using the tqdm

!pip install time

Import the libraries :
Import the newly installed tqdm and time libr*-ary
From tqdm import tqdm

## Using tqdm :

Now we will use the function tqdm() on a simple program with a for a loop.

##### EX:

For me in tq (range(20) ):
Time. sleep (0.5)
Here i is the variable that takes a value of the number 0 to 19 during each iteration. During each iteration, the system will sleep for 0.5 seconds before moving to the next iteration.

The complete code would look like this:
On Completion of Code Execution, we get

From tqdm import tqdm
Import time
For i in tq(range(20)):
Time.sleep(0.5)

We can also give attributes to tqdm() such as desc, which takes a string and will get added as a prefix before the progress bar. Thus,
From tqdm import tqdm

Import time
For i in tqdm (range(20),desc = ‘tqdm() progress bar’);
Time.sleep(0.5)

Apart from the progress bar, tqdm gives additional information such as the number of iterations completed out of the total number of iterations, Total Elapsed Time, Estimated Time to Complete the whole loop, and the speed of the loop in iterations per second (or it/s).on Completion of Code Execution

## Using tqdm_notebook() in pands:

tqdm_notebook() can be used in Pandas. One way is to use them for loops with Pandas Series which works the same as with the loops we have seen earlier. Another way is to use them in Pandas .apply() method use tqdm() or tqdm_notebook() for .apply(), the .apply() needs to be replaced by .progress_apply

Import pandas in PD
df = PD.read-CSV(“WA-Fn-usec-Telco-customer-churn.csv”)
df.head()
Tqdm-notebook.pandas()
df [‘churn’].progress

After code execution, we get

The tqdm_notebook.pandas() is responsible for displaying the progress bar. The progress bar shows the apply function being applied on all values of the Churn column. It is noteworthy that, the progress.apply() works the same as the .apply() method of Pandas.

# Pandas

* Python Pandas is defined as an open-source library that provides high-performance data manipulation in Python. This tutorial is designed for both beginners and professionals.
* It is used for data analysis in Python and was developed by Wes McKinney in 2008. Our Tutorial provides all the basic and advanced concepts of Python Pandas, such as Numpy, Data operation, and Time Series
* The name Pandas is derived from the word Panel Data, which means Econometrics from Multidimensional data. It is used for data analysis in Python and was developed by Wes McKinney in 2008.
* Data analysis requires lots of processing, such as restructuring, cleaning or merging, etc. There are different tools are available for fast data processing, such as Numpy, Scipy, Cython, and Panda. But we prefer Pandas because working with Pandas is fast, simple, and more expressive than other tools.
* Before Pandas, Python was capable of data preparation, but it only provided limited support for data analysis. So, Pandas came into the picture and enhanced the capabilities of data analysis. It can perform five significant steps required for processing and analysis of data irrespective of the origin of the data, i.e., load, manipulate, prepare, model, and analyze.

## Key features of pandas
* It has a fast and efficient DataFrame object with default and customized indexing.
* Used for reshaping and pivoting the data sets.
* Group by data for aggregations and transformations.
* It is used for data alignment and integration of the missing data.
* Provide the functionality of Time Series.
* Process a variety of data sets in different formats like matrix data, tabular heterogeneous, and time series.
* Handle multiple operations of the data sets such as subsetting, slicing, filtering, groupBy, re-ordering, and re-shaping.
* It integrates with other libraries such as SciPy, and scikit-learn.
* Provides fast performance, and If you want to speed it, up, even more, you can use Cython.

## Benefits of pandas

* Data Representation: It represents the data in a form that is suited for data analysis through its DataFrame and Series.

* Clear code: The clear API of the Pandas allows you to focus on the core part of the code. So, it provides clear and concise code for the user.
series is defined as a one-dimensional array that is capable of storing various data types. The row labels of the series are called the index. We can easily convert the list, tuple, and dictionary into series using the "series’ method. A Series cannot contain multiple columns. It has one parameter:
* Data: It can be any list, dictionary, or scalar value.


REVIEW BY CHARAN 
