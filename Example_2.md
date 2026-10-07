 Open:
  Purpose:
   To derive the age of a person
  
  Language_Target:
   Write the code in SAS for me.

  Out_Variable:
   agegr1

  Rules:
   agegr1 = [ADSL.AGE] between 2 and 11 is 1
   agegr1 = [ADSL.AGE] between 12 and 45 is 2

  When: 
  Missing AGE @/OT/ is missing
    
  Constraint:
  AGE > 2 and AGE <=80

  Trace:
  [ADSL.AGE]

  Verify:
    AGE is > 0 and does not contain character values

  Ambiguity:
   Missing AGE should be queried.
Close:

Open:
  Purpose: 
    Derive the Baseline Flag
  Language Target: Write the code in SAS for me
  Input_data:
    ADLB
  Out_Variable : 
    ABLFL
  Rules: 
    Flag as 'Y' the last OBS per PARAMCD where the ADT is <= TRTSDT
  When : 
    Only derive if the ADT and TRTSDT is both not missing
  Constraint: 
    ABLFL can only have one 'Y' Per parameter, per subject.
    ABLFL can not be flagged on obs where ADT > TRTSDT 
  Trace :
    [ADLB.PARAMCD],
    [ADLB.ADT]
    [ADLB.TRTSDT] 
  
  Verify :
    ABLFL is not flag for records where ADT > TRTSDT or where  ADT or TRTSDT is missing
  Ambiguity :
    ADT, TRTSDT that is missing while SAFFL and FASFL is Y must be queried  
Close:

FINAL:
Create a single file with all derivations in one file