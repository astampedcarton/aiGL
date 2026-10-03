  Purpose:
   To derive the age of a person
  
  Language Target:
   Write the code in SAS for me.

  Out Variable:
   agegr1

  Rules + datatype:
   agegr1 = [ADSL.AGE] between 2 and 12 is 1
   agegr1 = [ADSL.AGE] between 12 and 45 is 2

  When: 
  Missing AGE @/OUT/ is missing
    
  Constraint
  AGE > 2 and AGE <=80

  Trace:
  [ADSL.AGE]

  Verify
    AGE is > 0 and does not contain character values

  Ambiguity
   Missing AGE should be queried.
