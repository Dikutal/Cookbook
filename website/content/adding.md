title: Adding recipes
---

Adding recipes
==============
The easiest way to add a new recipe is to fork our Github-repository and send us a pull-request (see below).

If you want to make many changes, we can also give you direct access to the repository. Send a request to dikutal@diku.dk with our Github-username.

Forking
-------
 * Log in to Github
 * Go to https://github.com/Dikutal/Cookbook
 * Push the "Fork"-button in the upper right corner
 
A copy of the repository in the current state will be made and added to your profile. I for instance have a fork of the repository on my profile: https://github.com/dybber/Cookbook

You can now make all the changes you like in your local repository and when you are done, you can send them to us by issueing a pull request.

Pull-request
------------
A pull-request is a message you can send on Github from one repository owner to another:

  "Hey there! I have made all these sweet changes to your code and I think you would benefit from merging them into your version"

Then the receiver can accept by pushing a button on Githube and the changes will be merged.

Testing
-------
To test your changes you should install Wok and dependencies as mentioned in the README: https://github.com/dybber/Cookbook/blob/master/README.md

To test, go into the website-directory and issue "wok --server", then a webserver will spawn on http://localhost:8000/ where you can view the website including all changes.
