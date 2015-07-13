# consolver
Trying to upload a csv to database?  Notice that your csv has duplicated, contradictory, and/or incomplete rows for the same record?  Use consolver to consolidate and resolve conflicts!

The full-bodied function is console_and_resolve.  It will take you from a raw csv through (simple terminal input) choosing the variables that constitute the unique identifier (re: database constraints) and features of interest (nonoverlapping subsets of the csv columns).  From there it will take you through either simple terminal input to resolve duplicated row conflicts,default conflicts to mode (mode_default=False for never, =0 for always, =1 for if mode is more than 75% of values), default conflicts to the set of sorted values joine by "\_" (underscore=True; if mode_default not false this is secondary to mode_default choice), or some combination thereof.  It will produce a row consolidated file (\<file\>\_consolidated\_\<unique\_id column names\>.csv), a consolidated and resolved csv (\<file\>\_consolidated\_\<unique id variable names\>\_resolved.csv) and a json file that logged all the changes by unique identifier, feature changed, list of values chosen from, and chosen value.  console\_and\_resolve can be re-run with that logged changes json and the same file or and updated version.

Other functions and helper functions, including those to tally values in each column and perform terminal input choices, are modular and directly accesible.  They may be renamed bacause the names aren't particularly good right now.

Yaay.
