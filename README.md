# jjstringify

Purpose: You have two groups working on your app for ios and android.
The ios group is ahead and has its english strings translated to lets say
french, spanish. Meanwhile android app has a english strings.xml and
some/most of strings are common between ios and android. But the strings
ID are different even for these commong english strings between the ios
and the android version.

You want to reuse the translated strings in ios in Android project. 

Steps: 

1. Go to your ios en.lproj 
2. cat *.strings > x_en_strings.strings
3. Use https://github.com/josem/bruno or http://members.home.nl/bas.de.reuver/files/stringsconvert.html
   to covert this to x_en_strings.xml
4. Similarly follow steps 1-3 above for the translated language in ios  
   e.g fr.lproj to get a x_fr_strings.xml
5. make a workable folder, e.g station. Copy x_en_strings.xml and x_fr_strings.xml (example for french language)
  to this directory. 
6. Now Copy your English version of Android projects' strings.xml in this folder as a_en_strings.xml
7. download the bash script(updater) from this git repo.
8. Prerequisites for running ./updater
     a. xmlstarlet
     b. sed
9. Do ./updater in this working folder which we have called station
10. Your translated android strings for the language are in results.xml
