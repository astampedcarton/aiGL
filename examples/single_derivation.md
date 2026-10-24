OPEN ANL01FL_Gen:
  Purpose: 
    Derived Analysis Flag
  Language_Target: 
    Write the code in R for me
  Input_data: 
    [Analysis.ADSL]
    {SAP} SAP_V1.0.docx.
  Logic: 
    Flags the closest Observation (AWTARGET is the closest to 0) for Analysis values (AVAL) that's not missing. Done per parameter code (PARAMCD) per AVISIT. Only for where the analysis date (ADT) is after the Treatment start date. Baseline (ABLFL) is always flagged.
    Flag as Y
  Output: 
    ANL01FL
  Validation: 
    After the derivation check where a parameter does not have a ANL01FL
    Check the logic described against the logic presented in {SAP} Section 10.2.1
  Notes: 
    Create text that can be used in the ADRG

CLOSE ANL01FL_Gen:  