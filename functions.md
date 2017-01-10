### 2. Matlab Functions

Functions absracts the specific logic and performs the task described in the logic when it is called.

#### 2.1 Function usage

Using a function requires 3 things

- Function name
- Arguments to be passed
- Store the result if it returns

Syntax ` return_value = function_name (arg1, arg2, ..) `

Example :

```Matlab
% returns rows and columns present in vector (matrix) y (i.e) rows = 3, columns = 6
[rows, column] = size(y);

% returns the number of columns present in vector (matrix) y  (i.e) 6
columns = length(y);

% returns the total number of elements present in vector (matrix) y (i.e) 18
number_of_elements = numel(y);
```

__Question__:  what happens if use function `disp(y)` and try to store the result in a variable like `r = disp(y)` ?

#### 2.2 Function definition

It inovlves defining the logic in a seperate `.m` file. Below example explains the definition of  `add ` function (function name should be same as the file name). It performs the addition of 2 variable `num_1 and num_2` and stores the value in variable result and return it when ever the function is called.

- create a folder to logically organize your function. In this case it is `+math`
```
+math
|____ add.m
```

- create a function from matlab editor inside the folder 
```Matlab
function result = add(num_1, num_2)
%% This functions add 2 numbers
% 	usage : r = math.add(10, 20)

	result = num_1 + num_2;
end
```

__Anonymous function handle__


```add = @(num_1, num_2) num_1 + num_2; ```