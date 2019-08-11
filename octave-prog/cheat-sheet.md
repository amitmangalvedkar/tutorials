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
`  
%{   
  content goes here   
}%   
`   
3. Comment with help: Use `#` at the beginning of every output that needs to be displayed   

## Output and Input Commands ##

## Constants, Variables and Assignments ##

## Arrays - Scalars, Vectors, Matrices, Tensors ##

## Dictionary, Tuple, JSON ##

## Conditions ##

## Looping ##

## Functions - No argument, Multiple arguments, Overridding, Overloading ##

## Classes - Fields, Object Methods, Static Methods ##

## Classes - Inheritance, Multiple Inheritance ##

## Sockets - Server Socket, Client Socket, SSL Socket ##
