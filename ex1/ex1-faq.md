## LECTURE VIDEO FAQ
θ

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

### Q3) I am using Octave, and I get some errors when I run the submit script. What can I  do?
Do not use Octave 3.8 or 4.0.0 - they have errors for the submit script. Use Octave 6.2.0 (or later), or switch to MATLAB Online.

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
This will happen if you are using Octave 4.0.0. Octave 4.0.0 is broken. Do not use it. See Q3 above.

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
  
### Q17) (not used)

### Q18) Can I change my email address during the course?
No. This will confuse the exercise grader.

### Q19: How do I fix this error? "Unable to submit: You used an invalid email or your token may have expired "

Check that you have not changed your email address.

If your email address has a '+' character, replace it with "%2B".  Similar for any other punctuation characters - replace them with the appropriate HTML character code when you enter your email address in the submit script.

Check that your computer's time is set correctly. Some students report that having the time set incorrectly may cause this error.

### Q20) Submission Error: curl: (35) schannel: failed to retrieve ALPN result
a) In submitWithConfiguration, try changing this:

[code, responseBody] = system(sprintf('echo jsonBody=%s | curl -k -X POST -d @- %s', body, submissionUrl));

... to this

[code, responseBody] = system(sprintf('echo jsonBody=%s | curl -k -X POST -d @- %s --no-alpn', body, submissionUrl));

b) If this fix does not work, try using the CLI instead of the GUI.

### Q21) Problems due to using International keyboard settings
If you're using an International keyboard (German, French, New Zealand, etc) your keyboard may have mapped a different character to the 'single quote' key than the Octave/MATLAB language expects you to use. This can cause problems in your script files that are difficult to debug. This is especially a problem with the matrix "transpose" operator, and single-quotes used in some of the patch files.

If you are using a Mac computer, you can configure the single- and double-quotes in the system preferences.  

### Q22) In the Forum threads, the code boxes are blank where the patch instructions should be. Why?
They're not blank; the page doesn't render correctly if you're using Firefox.

### Q23) When I run the submit script, I get an error message that includes "input file does not exist".
(Note: with the programming exercise script updates in January 2017, this message should no longer be seen).

A) (removed - obsolete)

B) (removed - obsolete)

C) Check that all of your functions return values of the correct size. Especially in exercises (such as ex6) where the return value is a vector, the grader server will reject your reply if the vector is too long. It won't send back a file of grading results for display on your console, resulting in the 'input file does not exist" error.

D) If you connect to the internet via a proxy server, you must provide the proxy settings to Octave/MATLAB.

### Q24) (removed)

### Q25) If you are using MATLAB and see an error message like this...
Submission failed: unexpected error: Invalid field name: 'x0x_0x${sprintf('%X',unicode2native($))}__0x${sprintf('%X',unic'.

... it typically means you're using a version of MATLAB that is too old. Use the MATLAB version that is provided with this course.

### Q26 I am using OS X and TextEdit, and keep getting error messages when I use the single-quote (apostrophe) character, like when I want to transpose a vector or matrix. How do I fix it?
Choose Substitutions from the Edit menu and turn off smart quotes.  

### Q27) How can I fix a script file that I modified using OS X "TextEdit" and now has formatting characters in it and won't execute?
TextEdit opens a new document in rich text mode by default, but you can easily convert a document to plain text at any time. To do so, make sure the document you wish to convert is open and selected, then go to Format > Make Plain Text in the TextEdit menu bar. Alternatively, you can use the keyboard shortcut Shift-Command-T.  

### Q28) I'm using MATLAB, now do I fix this error when I submit my work for grading?
!! Submission failed: unexpected error: Error using urlread (line 94) 

Could not POST to URL. 

!! Please try again later.

Your version of MATLAB is probably too old, and doesn't support the functions that are used in the submit script. Use the MATLAB version that is provided with this course.

### Q29) How do I know if I passed the programming exercise when I run the submit script?
The submit script will report one of these three things on your console:

If your code has a syntax error or a runtime error, the script will crash and report an error message.
If your code returns the correct values, the text "Nice work!" will be reported in the "Feedback" column on the console. You may also be awarded some points, if the exercise is not optional.
If your code returns an incorrect value, the "Feedback" column will remain blank. This means your code does not work correctly.
Your results will be available in the "Grades" menu later, sometimes it is very slow to update.

### Q30) When I run the submit script, I get an error that says I need to install the "Parallel Computing Toolbox". Why?
Check on these potential fixes:

Verify that you have extracted all of the contents of the programming exercise zip folder. That includes all of the folders and sub-folders. See item Q6 above for details.
Verify that you have set your working folder to the one that contains the submit.m script for this exercise.

  ### Q31) I got an error about "curl: (35) schannel:" or "fatal SSL/TLS alert"
Students report that the submit script does not work if you are using Octave with Windows XP.

### Q32) In the video lecture on Feature Normalization, why does normalizing the features help gradient descent work better?
The problem stems from the difficulty in finding a good learning rate "alpha".

If you set it too high, then the changes in theta will be too large for one of the features, and that part of the gradient descent process will actually diverge.

If you set the learning rate low enough that it works for all of the features, then the learning is very slow, and you might need an infinite number of iterations to get to the minimum solution.

Normalizing the features fixes this problem, because the gradients for all features will be similar in magnitude. You can safely use a large learning rate and a small number of iterations.

### Q33) Why is my regularized cost value J too big?
Most often this is because "1/(2*m)" and "(1/2*m)" give vastly different results. This is due to the order-of-operations rules and parenthesis grouping. 

### Q34) In the Octave Tutorial, the "hist()" command doesn't work.
If Octave crashes when you type "hist(w)", try the command "graphics_toolkit('gnu_plot')" first. Also, see the "Installation Issues" section of the Resources menu. See also FAQ Q11 above.
