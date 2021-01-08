# dummy-vugen

# This test can be used to create LoadRunner result sets, than can be used for demoing, to show how specific issues can be created. A few notes:

It does not actually go against any website.
Instead, all of the "transaction times" are created by using sleep statements. 
Sleep is used (as opposed to lr_think_time), so that transaction times are independent of run-time settings. Some comments on usage:

* There is a run-time additional parameter, so that if the script is used in multpile groups in the controller, each group can have diferent performance.
* All transactions include random variations so that it looks more realistic
* There is also a random value, with will cause a script error. If this condition is triggered, the script does goto http://advantageonlineshopping.com, 
so that snapshot on error can be demoed
* There is also a random value for script abort, in case you want to demo that

If you have questions, feel free to reach out to ron.sercely@microfocus.com
