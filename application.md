**Automated testing and documentation for openLilyLib**
===================


Personal details
-
* **Name**: Adeel Ahmad
* **Email**: adeelahmadadl1995@gmail.com
* **GitHub username**: adl1995

Project summary
- 
Include LibreOffice extensions (?). The main goal of this project is to introduce / improve automated testing for the *openLilyLib* framework. Currently, partial Automated Testing is achievable through Travis CI. However, this needs to be extended to independent packages. There is also some refactoring that needs to be done. 

The other objective of this project is auto-generated documentation. The files in a project / package should be recursively searched and parsed for data. The author / contributor of the package would document the files (either through comments or function headers). Upon each new push to the repository, a Git hook will compile the documentation and serve it on a web page. 

In addition to the generation of standard HTML files, the process pipeline should involve an intermediate stage where the output should be in JSON / XML format. This would allow third-party websites / applications to retrieve and present data in a 'clean' way.

Benefits
-
The first thing that a user does when trying out a new software is to look at its documentation. It reveals how well managed and organized the software is. If the information is presented in a neat manner, the time to get it running is reduced considerably. In my opinion, a software should provide two branches of documentation, one that is more 'user-friendly' and the other that is more focused towards 'developers'. Of course, numerous softwares already provide this through popup annotations.

Work done
- 
mention Lydoc, Grako, Sphinx, test suite oll-core, gridly.
Deliverables
-

Plans
-

Communication
---------------------
The current medium of communication is through emails. I actually made contact with the mentors almost two weeks prior to the application start date. They have been very helpful in explaining what the project. I was also provided write access to the *oll-core* package for openLilyLib (?), for which I added a test suite, similar to the one already provided in *snippets* repository. ...

Qualification
-----------------

