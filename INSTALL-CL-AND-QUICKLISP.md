Installing Common Lisp and Quicklisp
-

### Installing/choosing the Common Lisp implementation:
[Install SBCL](http://www.sbcl.org/). This means clicking on your architecture [from this table](http://www.sbcl.org/platform-table.html) and running the platform specific installer.
If using Linux, an easier way to install is to enter
`apt-get install sbcl` at the command line.

### How to run the Common Lisp REPL
Most implementations start through an executable that has a similar name as the implementation. In the case of installing SBCL with a Linux package manager, entering `sbcl` at the command line will run SBCL. However, there are installation situations in which you may need to execute a script or navigate to a directory to run the Common Lisp implementation, and this is implementation specific. 

### Using Quicklisp:
[Quicklisp webpage](https://www.quicklisp.org/beta/)  
What is Quicklisp? Quicklisp is the de facto package manager for Common Lisp. 
#### Installation
[Installation instructions](https://www.quicklisp.org/beta/#installation)
1. Download the [quicklisp.lisp](https://beta.quicklisp.org/quicklisp.lisp) file. 
2. Open up your Common Lisp REPL
3. [Load](http://clhs.lisp.se/Body/f_load.htm) the file into Common Lisp. It should look something like this:  
`CL-USER> (load "~/path-to-the-quicklisp-file-goes-here/quicklisp.lisp")`
4. Install quicklisp in the default home location. For a custom installation directory, see the [quicklisp website](https://www.quicklisp.org/beta/#loading).  
`CL-USER> (quicklisp-quickstart:install)`
5. [optional] Add quicklisp to implementation startup with   
`CL-USER> (ql:add-to-init-file)`

Everything Quicklisp downloads, which is for the most part Common Lisp code, should be inside the `quicklisp` directory. Removing quicklisp amounts to deleting the `quicklisp` directory and being careful to remove the [Optional from step 5 above] code added by quicklisp to the implementation initialization file.
#### For returning quicklisp users:
1. Open the Common Lisp REPL
2. If quicklisp has been added to implementation startup as in step 5 above then it is already loaded. Otherwise:  
`CL-USER (load "~/path-to-quicklisp/quicklisp/setup.lisp")`
