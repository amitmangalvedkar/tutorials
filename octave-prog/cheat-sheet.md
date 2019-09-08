# Octave Programming #

## File Extension, Installer, Compilation, Execution, REPL, Help ##
### File Extension ###
.m as MATLAB calls its script files as M-files

### Installation, Compilation and Execution ###
#### On-prem ####

#### Docker based ####
`docker pull epflsti/octave-x11-novnc-docker`  
`docker run -p 8083:8083 -ti epflsti/octave-x11-novnc-docker:latest`  
`firefox http://localhost:8083`  
If your source files are in your host `docker run -p 8083:8083 -ti -v $(pwd):/source epflsti/octave-x11-novnc-docker:latest`  


## Comments ##
1. Single-line comment: `%` or `#`   
2. Multiple-line comment:   
```  
%{   
  content goes here   
}%   
```   
3. Comment with help: Use `#` at the beginning of every output that needs to be displayed   


## Output and Input Commands ##   
### Output ###   
`disp` always ends in a newline
```
disp ("The value of pi is: ")
disp (pi)
```
`list_in_columns` return a string containing the elements of arg listed in columns with an overall maximum width of width and optional prefix prefix.

### Input ###    
The `input` and `menu` functions are normally used for managing an interactive dialog with a user.  
```
ans = input ("Pick a number, any number! ")
```  
The `yes_or_no` takes one argument `prompt` that should end in a space, the `yes_or_no` appends the string `(yes or no)` at the end
The keyboard function is normally used for doing simple debugging.
```
x = kbhit ();
```

## File Operations: Output (Append and Overwrite), Input, Seek, Delete ##   

### Save and Load ###
```
A = [1:3; 4:6; 7:9]   
save myfile.mat A   
```
The above operation saves matrix A in the file myfile.mat   
```  
load myfile.mat
```
The above operation loads the content of myfile.mat into A.      
There are lots of options available such as `csvwrite`, `csvread`, `textscan`, `dlmread`, etc

## Constants, Variables and Assignments ##

## Arrays - Scalars, Vectors, Matrices, Tensors ##

### Vectors ###
```
x = [1, 2, 3]
```
This stores row vector in x
```
y = [1; 2; 3]
```
This stores column vector in y

### Matrices ###
```
x = [1,0,0;0,1,0;0,0,1]
```
This creates an identity matrix

### Tensors ###
Typically, Tela, a software package similar to Matlab and (GNU) Octave, is used for tensors.   
For MATLAB, an open source package tensor toolbox for MATLAB, managed by Sandia National labs, is available

## Dictionary, Tuple, JSON ##
### Dictionary ###
```
x.a = 1;
x.b = [1, 2; 3, 4];
x.c = "string";
```
creates dictionary having the following structure   
```
{
  a = 1
  b =

    1  2
    3  4

  c = string
}
```
Similarly
```
x.b.d = 3;
```
creates
```
x.b
{
  d=3
}
```

## Conditions ##
```
if (rem (x, 2) == 0)
  printf ("x is even\n");
elseif (rem (x, 3) == 0)
  printf ("x is odd and divisible by 3\n");
else
  printf ("x is odd\n");
endif
```
## Looping ##
Octave's `while` statement looks like this:
```
while (condition)
 body
endwhile
```

## Functions - No argument, Multiple arguments, Overridding, Overloading ##

## String Manipulation ##

## Database Operations ##

## Classes - Fields, Object Methods, Static Methods ##

## Classes - Inheritance, Multiple Inheritance ##

## Packages and Namespaces ##   
### Community Packages ###   
### Creating Packages ###   

## Sockets - Server Socket, Client Socket, SSL Socket, Raw Sockets ##

## Multithreading ##
