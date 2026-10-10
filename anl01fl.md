Open:
  Purpose: 
    Derive Analysis Flag
  Language Target: 
    Write the code in R for me using Admiral
  Input_data:
    ADEFF
    D: SAP 
  Out_Variable : 
    ANL01FL
  Rules: 
    Flag 'Y' for the last OBS per [ADEFF.PARAMCD] per [.AVISIT] where the [.ADT] is >= [ADSL.TRTSDT] and the [.ADT] is <= [ADSL.TRTEDT]    
    Flag 'Y' when Baseline [ADEFF.ABLFL] is 'Y' 
  When : 
    Only derive if the ADT and TRTSDT is both not missing
    only derive if there the analysis Results [ADEFF.AVAL] is not missing.
  Constraint: 
    ANL01FL can only be populated for post-baseline.
    [.AVISITN], [.ADT] and [.ABLFL] must exist
    
  Trace :
    [ADEFF.PARAMCD],
    [ADEFF.ADT]
    [ADEFF.TRTSDT] 
    [ADEFF.TRTEDT] 
  
  Verify :
    ANL01FL is not flagged  for records where ADT >= TRTSDT or where  ADT or TRTSDT is missing
  Ambiguity :
    ADT, TRTSDT that is missing while SAFFL and FASFL is Y must be queried  
Close:

FINAL:
Create a single file with all derivations in one file