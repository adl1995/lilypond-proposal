**Automated testing and documentation for openLilyLib**
===================

> * Organization: GNU
> * Suborganization: LilyPond

### Personal details ###
* **Name**: Adeel Ahmad
* **Email**: adeelahmadadl1995@gmail.com
* **GitHub**: adl1995
* **Timezone**: UTC +05:00
* **Blog**: http://adl1995.github.io/

### Academic details ###
* **University**: National University of Computer and Emerging Sciences, Islamabad
* **Degree**: Computer Science 
* **Graduation year**: 2018 

Background
----------------
Being good with computers from an early age, I took up Computer Science for my bachelors degree. Although I did not have any coding experience prior to my enrollment in college, I quickly caught up. It opened my eyes to a whole new world, and I started to experience things in a different way. Problem solving was something that interested me deeply. So, I started to solve / learn various mathematical problems and tried to code them.   

In my previous semester, I enrolled myself in Digital Image Processing course. This is when I saw the beauty of mathematics applied in images. How a simple Gaussian function could be used to blur an image simply amazed me. During the tenure of this course I implemented filters (Gaussian, Sobel, Prewitt, Laplacian), edge detectors (Canny, Marr Hildreth), morphological operators (Convex hulling, Erosion, Dilation), object detectors (Generalized Hough transform, simple convolution), and seam carvers. These were implemented purely in Python, making no use of external libraries other than ``Numpy`` and ``Matplotlib``. This attenuated my interest in mathematics and I started linking it with real life. I have showcased these projects on my [GitHub profile](https://github.com/adl1995). The most interesting algorithm I implemented was [Generalized Hough Tranfrom](https://github.com/adl1995/generalised-hough-transform). I was amazed as to how something as simple as an equation of line could lead to detection of objects in images.

Apart from this, I have also been a PHP web developer for almost two years, and I have worked on multitude of projects ranging for SaaS to e-commerce websites. I work remotely on [Upwork](https://www.upwork.com/freelancers/~018e56b8591046f889) and [Fiverr](https://www.fiverr.com/adl1995). My clients are either IT organizations or independent contractors. I have also worked on web automation and data scraping using ``Selenium`` and ``BeautifulSoup``. Although these skills are not required for this organization and have no direct links in my project, it shows that I am persistent and hard-working. The skills that I acquire are through self learning and consistency. Currently I am building an application using [Google Application Engine](https://github.com/adl1995/zoho-portal).

I started collaborating with Open Source organizations only about a month ago, and my experience has been excellent so far. The mentors have been kind, welcoming, and have provided assistance along the way. Given my good problem solving skills, I firmly believe this prestigious organization and its users will benefit by the addition of automated testing and a documentation generator. It would also provide me with a working ground knowledge on various tools, which will be beneficial for my career.

Project Details
---------------

### Mentors ###
> * [Urs Liska](https://github.com/uliska)
> * [Matteo Ceccarello](https://github.com/cecca)

### Abstract ###
> Automated testing is required to ensure modifications in code do not lead to build failures. Some functionality is currently available in [snippets](https://github.com/openlilylib/snippets) repository for openLilyLib. Currently, I am trying to create a test suite for the [oll-core](https://github.com/openlilylib/oll-core/tree/adeel/test-suite2) library. The other main goal of this project is automated documentation. In addition to generating standard HTML files, the process pipeline should involve an intermediate stage where the output should be in JSON / XML format. This would allow third-party websites / applications to retrieve and present data in a 'cleaner' way.

### Detailed description ###
The main goal of this project is to introduce / improve automated testing for the openLilyLib framework. Currently, partial automated testing is achievable through Travis CI. However, this needs to be extended to independent packages. Apart from this a technique / method has to be used for  diminishing build failures, which are caused when source files fail to compile. For improving the frequency of build failures I would suggest to breakdown the code in small components and audit / review each merge request through a series of brief questions. Another way to minimize build failures is by restricting pushes to the `master` branch, and only allow project managers to accept merge requests that have successful build statuses. This ensures that new features don't break the functionality. Apart from this there is some refactoring that needs to be done. 

In the test suite, there lies a Python script named `automated_tests.py`, this recursively looks for files in `usage-examples` directory and compiles them using LilyPond. It then reports the results. If there has been a build failure the repository manager will get notified through Travis CI. To exclude files from a directory an entry should be added in `.simple-tests-exclude` file, when the script  encounters a file within this directory it will essentially skip it.

Thus the importance of automated testing is trivial. There is a chance of lack in product quality if this is not present. It can also improve the development process in many cases. During the tenure of this project, automated testing will be extended to different modules / libraries that lie within openLilyLib.    

The other main objective of this project is documentation generation from source files. The files in a project / package should be recursively searched and parsed for data. The author / contributor of a package would document files either through comments or function headers. In my opinion, the documentation should be generated through docstrings / function headers, this provides a more 'detailed' view of the system. Upon each new push to a repository, a Git hook will compile the documentation and serve it on a web page. In addition to generation of standard HTML files, the process pipeline should involve an intermediate stage where the output should be in JSON / XML format. This would allow third-party websites / applications to retrieve and present data in a 'cleaner' way.

There has been an active discussion on which tool to use for generating documentation. I have suggested to go with `Shpinx` over `Doxygen`, it provides an interface to integrate documentation generation with third party languages. As LilyPond is not a regular language, we need a tool called Context Free Grammar for this purpose. Python already has a package called [Grako](https://bitbucket.org/apalala/grako/src/default/README.rst?fileviewer=file-view-default) which is a parser generator and will be integrated for searching text through CFGs. Once all this is set up, one would essentially execute a `sphinx-build` command and this would parse all the source files and create a clean documentation at the end.

The openLilyLib repository contains a great deal of legacy code. Replacing this with up-to-date structure and porting the old package to the new infrastructure is also a part of this project.

Benefits
-----------
A user, when trying out a new software, always goes through its documentation. It reveals how well managed and organized the software is. If the information is presented in a neat manner, the time to get it running is reduced considerably. In my opinion, a software should provide two branches of documentation, one that is more 'user-friendly' and the other that is more focused towards 'developers'; this could essentially be an API. Of course, numerous softwares already provide this through popup annotations.

Work done
-----
I have actively conversed with Urs Liska and Matteo Ceccarello, the mentors of this project. They assigned me with some qualification tasks. Firstly, I created a test suite for [oll-core](https://github.com/openlilylib/oll-core/tree/adeel/test-suite2) by taking the model from original tests in [snippets](https://github.com/openlilylib/snippets) directory for openLilyLib. The old test suite in snippets required `version "2.17.25"`, however the oll-core package was made for `version "2.19.22"`, so in order to make it compatible the `\loadModule` tag had to be updated.  

Other than this I also made a commit to the GridLY repository (https://github.com/openlilylib/gridly/commits/master). The work basically involved reproducing the package from snippets repository.

Lastly, I set up this (https://github.com/adl1995/lilypond-sphinx) repository for harvesting `.ly` files and to extract documentation from it. The work is still undergoing. I also started to work with Lydoc (https://github.com/Cecca/lydoc), written by Matteo. It makes use of Sphinx and Gecko to extract comments from function headers, it is my opinion to build on top of this current work to avoid reinventing the wheel. 

Communication
---------------------
The current medium of communication is through emails. I actually made contact with the mentors almost two weeks prior to the application start date. They have been very helpful in explaining what the project is. I was also provided write access to the `oll-core` and `GridLY` library for openLilyLib for which I made numerous commits.


## Timeline ##

| Time Period        | Plan           |
| ------------- | ------------- |
| May 04, 2017 - May 30, 2017 **(Community Bonding Period)**      |   <ul><li>Finalize on the deliverables.</li><li>Discuss with mentors and get a final idea on how to approach the problem.<li>Conclude on how and where to extract the documentation from.</li></ul>|
| | **Part 1 starts** |
| May 30, 2017 - June 15, 2017 ( 2 weeks ) | <ul><li>Set up the development environment, get familiar with LilyPond's coding practices.</li><li>Set up the package.</li><li>Write a skeleton layout for the code to implement.</li></ul> |
| June 16, 2017 - June 30, 2017 ( 2 weeks ) | <ul><li>Document and write test cases for the added part.</li><li>**Update 1 : Push code and make sure the test cases pass.**</li></ul>|
| | **Part 1 completed**<br />**Part 2 starts** |
| July 01, 2017 - July 14, 2017 ( 2 weeks ) | <ul><li>Add additional functionalities e.g. ability to generate JSON files which will facilitate users during documentation generation.</li></ul> |
| July 15, 2017 - July 28, 2017 ( 2 weeks ) | <ul><li>Add optimizations, write test cases.</li><li>Update infrastructure for old openLilyLib libraries.</li></ul> |
| | **Part 2 completed** |
| August 21, 2017 - August 29, 2017 **(Students Submit Code and Evaluations)** | <ul><li>Clean up code.</li><li>Improve documentation.</li><li>Add further test cases.</li><li>Code refactoring (if required).</li><li>Resolve merge conflicts (if any).</li></ul> |
| August 29, 2017 - September 05, 2017 | Mentors submit final student evaluations. |
| September 06, 2017 | Results Announced. |

## Availability ##

My final exams end on May 20<sup>th</sup>. So, I will have ample time for the community bonding period. After that, I will be free for the whole summer i.e. almost three months. I do not have any other commitments, so I can focus all my attention to GSoC.


