##
This is a teacher/TA only page that gives instructors guidance on their teacher-led 30-45 minutes. This page is followed by the student-driven activity that will be completed after the more teacher-led time slot.

Instructors can create slides, examples, or other visual aids to help bring the concepts to life.

## Learning Objectives
Students Will Be Able To...
1. Explain the purpose of Style Guides
1. Apply a style guide to their code
1. Setup and use an automated style checker

## Outline of what to cover and suggested interactions
**1.0 The Development Pipeline**
In industry, what happens after a developer writes code and pushes it to Github?
   * Have students throw their guesses into chat before you answer this
   
   1. Static Analysis
   1. Tests
   1. Code Review
   1. Deployment
   
1.1 Static Analysis
Static code analysis is a general term for algorithms that check code. There are tons of static analysis tools out there which check everything from attempting to detect bugs to checking style. Sometimes these tools are referred to as linters.

**2.0 Style Guides**
Why might a company or group of developers want to follow a style guide?
  * Have students throw their guesses into chat before you answer this
  
  Example reasons:
  * Makes large code bases easier to read
  * Gives developers consistent experience (ex. maximum line length)
  * Agreed upon rules make code reviews faster/easier

2.1 PEP 8
https://www.python.org/dev/peps/pep-0008/

2.2 Show pycodestyle
https://pypi.org/project/pycodestyle/

Live code...
1. Installing pycodestyle
1. Creating a file with bad syntax - here is some code
      ```python
          def dec(x):
              x=x-1
              return x

          def add(x,y):
              return x+y


          class electro_bike:
              def __init__(self, speed, color):
                  self.speed = speed
                  self.color = color


              def 1_more_speed(self):
                  self.speed += 1


          x=3
          y=2

          if x>y:
            print(add(x,y)>dec(x))
      ```
1. Run `pycodestyle --first file_name.py` on terminal

1. Think aloud as you are interpreting the errors and fixing them

1. Re-run linter to show there are no more errors

**3.0 CI**
Continuous integration is a setup that provides developers automated feedback every time they integrate their code into a repository (hopefully many times a day). There are tons of tools for this (maybe list a few you have used or that are popular). Instead of manually re-running a style checker, you can setup CI so that you get feedback on your style every time you commit.

3.1 Github Actions
To keep things simple, we are going to start our CI journey with Github Actions. 
https://docs.github.com/en/actions/quickstart

3.1.1 YAML
YAML, similar to JSON, is a computer-readable format. Unlike JSON, but similar to Python, YAML uses white space for structure so be careful of indention!

3.2 Option 1: Manually use pycodestyle
https://github.com/SEO-Tech-Accelerator/python-style-checker-example/blob/master/.github/workflows/checkstyle.yaml

3.3 Option 2: wemake-python-styleguide
https://github.com/marketplace/actions/wemake-python-styleguide

**4.0 Closing**

4.1 Questions?

4.2 Give a sentence overview of the activity they are about to do

4.3 Explain how to get help from Instructors and TAs


## Teaching Tips

### Live Coding
Don't just show learners an already built system -- start from absolute scratch like they'll be doing and MAKE MISTAKES! Normalize making the mistake -- everyone does it. Normalize asking for help -- everyone should do it. Model how to listen to someone's suggestion and try it out -- they will be doing paired programming and need to see good examples of how navigators can support drivers.

## Example Solution to Activity
[https://github.com/edeitrick/python-style-checker-example](https://github.com/edeitrick/python-style-checker-example)

