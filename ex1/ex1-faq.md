## LECTURE VIDEO FAQ

### Q1) Where can I find notes on the lecture videos?

The Resources menu contains notes for each week.

The lecture slides are in the "Review" section of each lesson.

### Q2) I found an error in one of the video lectures. Should I post about it on the Forum?

No. There are lots of errors in the video lectures. There is a list of them in the Errata sections of the Resources menu.

### Q3) In the "Features and Polynomial Regression" video, why does Prof Ng talk about one of the curves "going back down"?

See the "Week 2 Lecture Notes" section of the Resources menu.

### Q4) Where can I get the data files used in the Octave/MATLAB video tutorial?

See the "Week 2 Lecture Notes" section of the Resources menu.

## QUIZ FAQ 

### Q1) I keep getting the quiz question on feature scaling incorrect. What should I do?

Make sure you are using a dot '.' for decimal and not a comma ','. Round-off to the correct number of places after the decimal point. Finally, see <this tutorial>

### Q2) Does the quiz use column or row vectors?

All vectors are column vectors.

### Q3) What type of feature scaling does the quiz use?

Use range() for the quizzes. 

## PROGRAMMING ASSIGNMENT FAQ

  Note: Tutorials and additional Test Cases are available in the Resources menu.    

### Q1) How do I get started?

Be sure you've watched all of the Week 1 and Week 2 videos, including the Octave/MATLAB tutorial series. 
Download each programming assignment from the "Course Home" or "Grades" menus. That's also where you get the "Token" that the submit script asks for.
Follow the instructions in the ex1.pdf file. 
Never use the addpath() command to fix a problem with your folder structures.  See Q6 below. 
Read the page  "Programming tips from Mentors" in the Week 2 course content. 
Do not use Wordpad or TextEdit to edit your script files. Use the editor built into the Octave or MATLAB GUI, or use a text-editor such as Notepad++."
If you use WINRAR to extract the contents of the programming exercise zip files be sure that you also extract the sub-folders.
### Q2) When I run the submit script, I do not see the option to submit individual parts as shown in the videos. Why?

The submit process was changed after the videos were recorded. Now all parts of the exercise are evaluated each time you run the submit script. 

### Q3) I am using Octave 4.0.0, and I get some errors when I run the submit script. What can I  do?

Do not use Octave 4.0.0 - it has a fatal error for the submit script. Use Octave 4.0.1 (or later), or MATLAB. 

See the "Installation Issues" section of the Resources menu. 

### Q4a) When I run the submit script, I get one of these errors:

!! Submission failed: Grader response is an HTML message
unexpected error: Error using urlreadwrite
submitWithConfiguration ... Grader sent no response
Failed to connect to www-origin.coursera.org port 443: Connection refused
Submission failed: element number 1 undefined in return list
Your computer may have a proxy server, firewall, or anti-virus protection that is blocking the submit script from connecting to the server where the grader runs. You need to resolve this issue yourself. MATLAB/Octave have menu settings for your proxy configuration. 

Another cause is if your computer does not have the curl() utility installed. Test this using the command "system('curl -V')" in the Octave console.

If you have a strong regional firewall, try using a VPN.

### Q4b) When I run the submit script, I get an HTML error that includes "Oops, an error occurred"

This will happen if you are using Octave 4.0.0. Octave 4.0.0 is broken. Install Octave 4.0.1 or later.

Another cause of this error is if you have more than one Coursera account, or if you registered through Facebook. If so, contact the Help Center. 

### Q5) I get the correct answer "32.07" for the cost value, so why doesn't the grader give me any points?

That test case uses all-zeros for the theta values, and is not a robust test of your code. The submit grader uses a more complex test. Your code must work with any data set.

Test your code using the additional test cases from the Resources menu.

### Q6) When I run the submit script, I get an error like this, what can I do about it?Name is nonexistent or not a directory: .\lib   > In path (line 109)  In addpath (line 88)  In submit (line 2)  Undefined function or variable submitWithConfiguration'.

1) Never use the "addpath()" command from the console. Many exercises use the same script file names, and "addpath()" can cause submit.m to find the wrong function.  

2) Check if you extracted all of the contents of the exercise zip file correctly. You should have the following folders, each with some files:
'
/ex1  - use this folder to run the ex1 and submit scripts.
/ex1/lib
/ex1/lib/jsonlab
'
Also make sure you are in the correct working directory. Use the 'pwd' command to check to see if you are using /ex1.

### Q7) The videos tell us to use "\theta^T*xθ T∗x" but I get a dimensions mismatch error when I use it. Why?

See the Programming tips from Mentors for an explanation of the difference between \theta^T*xθT ∗x and X*\thetaX∗θ.

### Q8) In ex1_multi, why is my house price prediction not the same for both methods?

If the two predictions are very far apart, it probably means you did not normalize the features of the prediction when using theta from the gradient descent method. This means you should:

create a vector of the prediction features, such as "[1650 3]".
subtract 'mu', then divide element-wise by 'sigma'. mu and sigma were returned by featureNormalize().
add a bias unit
multiply by theta
If the two predictions are off by a few percent, then you need to modify the learning rate and the number of iterations in ex1_multi.m. If you handle the normalization correctly and pick good values for the learning rate and number of iterations, then you can get the same price for both GD and the NE method.

### Q9) I am using a Mac with Octave and I see the 'unknown or ambiguous terminal type' error. What should I do?

See the tips for OS X users in the Resources menu.

### Q10) I run my code and get the error "Not enough input arguments" or "x undefined near line <--->". How do I fix it?

To test your code from the console, you must provide the data parameters it needs by putting some data between the parenthesis.  If you just type in the function name with no parenthesis and no data variables, you will get a runtime error.

### Q11) Why does Octave hang or crash with a blank plot figure?

Some Octave versions are is distributed without the required font files. So the first time you generate a figure plot, Octave takes a couple of minutes to generate the font files. During this time, Octave looks like it has crashed. But it has not. It is still generating the fonts in the background. Just wait a minute or two, and the fonts will be generated, execution will resume, and all plots in the future will be displayed promptly.

### Q14) In ex1_multi.m, the theta values are different for gradient descent and the Normal equation. Is that OK?

Yes. Theta is calculated from the values of the features. Since gradient descent uses normalized features, the theta values will be different than the Normal equation theta, which uses the raw features. See also Q8.

### Q15) How do I know my results for the optional assignments?

The submit grader's results table will say "0/0 Nice work!" if your results are correct, and will just say "0/0" if they are not.

### Q16) Can I use both Octave and MATLAB?

Not easily. They store the "token.mat" file in different formats, so if you switch between Octave and MATLAB, you have to manually delete the "token.mat" file from your exercise folder every time.

### Q18) Can I change my email address during the course?

No. This will confuse the exercise grader.
