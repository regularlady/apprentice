## How to Ask for Help

As you are learning to code, several challenges will get in your way and learning how to ask for help is an art.  

* Developer Tool Issue
* Debugging Code
* Foggy Problem
* The Nuts and Bolts of Implementation

__Developer Tool Issues__

Ever messed up Git before? We all have. When my students suffer from a bad installation, I ask them to message me with this information.

    Operating System:
    Installation Steps:
    Error Logs:

__Debugging Code__

Every error is an opportunity to learn, almost always about yourself as a developer.

Bugs are a mystery that are always interesting to crack. Then after the mystery is solved, you can do even better by looking through all your code for similar errors you may have made; and write an automated test to ensure the error will not happen unknowingly again.   

First, try to read the logs for the error. The logs will often print the line that is erroring out with the first couple of lines.

Second, begin finding bugs by reproducing the problem. Start by getting exact input if you can. Try reproducing the problem in your dev env with as little data as possible. I ask for my students to collect all the conditions present when the problem occurred (for example, other users, data types, etc).

Here are some suggestions from the Elements of Programming Style:

* Make sure all variables are initialized before use.
* Don't stop at one bug (there are always more).
* Watch for off-by-one "end" errors.
* Test programs at their boundary values.
* Program defensively.

Once my students are at a dead end, I ask them to push up their code and tell me the following:

1. Commit URL:
2. I expected x to happen when I did x, but x happened instead.
3. I tried x.

__Foggy Problem__

At times, the problem is that the requirement is not clear enough.

I ask my students to message me what they think the requirement is. Many times we (requirement writers) combine requirements, change terminology, and add extra words to our requirements because we haven’t appropriately described or visualized how the requirements fit together and what purpose they serve.

I ask my students to then break it down further.

* What arguments are being sent in?
  * What class are they?
  * Example: 1 Array => ["the", "great", "gatsby"]

* What value should be returned?   
  * What class should it be?
  * Example: 1 String => "The Great Gatsby"

__The Nuts and Bolts of Implementation__         

A solution can be clear but the actual implementation steps might stump a new developer.

Excellent guide to follow: [Solving Problems, Breaking it Down](https://simpleprogrammer.com/2011/01/08/solving-problems-breaking-it-down/)

Stack Overflow is a major tool that developers use. It is where the world's developers get answers, share knowledge & find jobs. I recommend that students [learn](http://stackoverflow.com/tour) how to use the SO as early in their careers as possible. 
