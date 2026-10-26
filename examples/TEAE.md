OPEN TRTEMFL:

PURPOSE: Treatment Emergent Adverse Event

LANGUAGE_TARGET:
R
Input_Data:
 [ANALYSIS.ADSL]
 [TABULATE.AE]
 D:Library_meta
Logic:
  Flag as Y all observations where the [AE.ASTDT] is on or after the [ADSL.TRTSDT] and the [AE.ASTDT] is before [ADSL.TRTEDT]. IF [AE.ASTDT] is missing impute as start day of the applicable month but [AE.ASTDT] can not be before [ADSL.TRTSDT]
Output:

Validation:
The variable must exist in D:Library_meta.
 
Notes:
Convert the logic into a non-technical text that can be used in the ADRG.
CLOSE TRTEMFL:

FINAL:
