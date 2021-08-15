### Q1) How do I get started?

(insert the "Important Notes for New ML Students" here)

Familiarize yourself with the Resources menu (see the links on the left side of your browswer) and the Discussion Forums. 

Questions regarding Machine Learning should be posted on the course Discussion Forums

Technical issues/suggestions regarding the videos should either be reported via the small flag icon on the bottom right of the videos, or via the Help Center.
Certificate related issues should also be sent to the Help Center.

### Q2) What are the course pre-requisites?

You will do best in this course if you have:

Experience in at least one programming language.
Are not frightened of solving a system of linear equations.
...which is another way of saying...

Know how to multiply matrices and vectors.
Lacking those skills, you can still complete the course, but it will take considerably more time and study.   

The course is not heavy in math - linear algebra is a benefit, some statistics is helpful, calculus is not required.
 
If you do not have any programming experience, consider taking an introduction to programming course, such as Mathwork's "MATLAB Onramp".

### Q3) Why does the cost function include multiplying by 1/(2m)?

The '1/m' portion is so that the cost is scaled to a per-example basis. Later in the course we will be comparing the cost value J for different sizes of training sets.

The '1/2' portion is a calculus trick, so that it will cancel with the '2' which appears in the numerator when we compute the partial derivatives. This saves us a computation in the cost function.

### Q4) In the cost function, why don't we use absolute value instead of the squared error?

The absolute value has some bad characteristics for minimization.

 The gradient is not continuous, because the absolute value function is not differentiable at its minimum point.
It does not emphasize the correction of large errors. 
The abs() function is also not very mathematically efficient. 

### Q5) I found an error in one of the video lectures. Should I post about it on the Forum?

No. There are lots and lots of errors in the video lectures. We keep a list of them in the Errata sections of the Resources menu.

### Q6) Can I use python or R to do the programming exercises?

The short answer is "no". This course is taught using MATLAB or Octave (the open source implementation of the MATLAB language). The grader software is written in MATLAB and tests your code by calling it using MATLAB function calls. Prof Ng explains why he choose MATLAB in the lectures.

### Q7) In the quiz grading, what does "correct response" mean?

Be careful about how you interpret the quiz grading. It is grading your responses, not whether the answer choices are true.

The "correct response" is for you to mark the true statements, and to not mark the false ones.

### Q8) Why can't I get the correct answers for the Week 1 quizzes?

First, read (Q7 above) so you know how the grader provides feedback. 

Next, be very careful you read the quiz questions and answers in great detail. The quizzes are randomly generated each time you re-take a quiz - you may get a different set of questions, a different set of possible answers, and they will all appear in a random order.

The quiz grader doesn't tell you why your answer was wrong - so this can be frustrating especially on those "pick all that apply" questions.

The best way to sort out this dilemma is to keep a record of what your quiz attempts have been - both the questions you were asked AND the answers you tried. This will prevent you from overlooking some subtle difference in the questions, and help you avoid re-using the same answers.

A last bit of advice. Questions that include the word "always" are (nearly) never the correct answer.

After a few attempts at a quiz, you may think that the grader is broken. But the grader is actually correct - but some of the questions are very subtle.

### Q9) What's all this about "regression" vs. "classification"?

Lots of problems in Machine Learning can be solved using either linear prediction or classification prediction. They're both forms of regression. Which method to use depends on how you want to use the output values - do you want a real value, or do you want a label?

"regression" vs. "classification" is a false distinction.

Do not confuse "classification" with "clustering".

Clustering is an unsupervised method - we're just sorting examples into different bins depending on their characteristics - maybe size, maybe color, maybe their genes. There is no "output" value to consider.
