# CCPS-393-Project-1

Write a Unix /bin/bash program to search a medication list (medslist) and produce a report as requested by the user.

Program Requirements
- Continually prompt the user to enter a Medication Code or portion thereof (should not have to re-run program for each search).ï¿½ Use “ZZZ” to exit program from the "Enter Medication Code" prompt.
- Ask the user if s/he wishes to see the corresponding Generic Name (G/g) or Dose (D/d); reject any other input with an error message (“Please enter only P or S.”) and re-prompt user continually if necessary.
- Search only the Medication Code field of the data file displaying the all occurrences of matching Medication Code (s) and corresponding Generic Name or Dose. 
E.g. A search for the Medication Code "6314", should not display any information about Medication Code "5341209". i.e. the search must be restricted to the information in the Medication Code field. 
- Include partial matches of Medication Code (e.g. 234 is contained in Medication Code 12345). 
- Use the sample data file from the course website.  Sample file is not exhaustive or representative of all situations. For example, don't expect particular values in the Category field (only letters, etc.) to limit your search of the Medication Code field. 
- If no part is found, output "No such Medication Code."
- If you create any temporary files, they must be cleaned up by your program before it terminates.
- Your program must perform its search and report strictly based on column numbers.  The data file may contain any type of character in any field.  (e.g. do not assume that the Medication Code consists of only numbers or that the Dose must contain letters) 
- Your program must not use any text processing utilities like awk, sed, or perl.  
- Your program must work on any data file of the format given above - not just the given sample data file.

Sample execution (not exhaustive testing):
$ search
Enter Medication Code? 6314
See Generic Name (G/g) or Dose (D/d)? G
A6314    ifosfamide
Enter Medication Code? 23
See Generic Name (G/g) or Dose (D/d)? j
Please enter only G or D.
See Generic Name (G/g) or Dose (D/d)? d
   12345 ug         200
9230     pg        6000
Enter Medication Code? foo
See Generic Name (G/g) or Dose (D/d)? D
No such Medication Code.
Enter Medication Code? ZZZ
Good bye.
$
