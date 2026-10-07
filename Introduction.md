# QSE (aiGL) 
 
## Introduction
As AI is gaining tracktion, statistical programming in the Pharma Industry is evolving, and we need to evolve with it.

QSE - Quality Spec Execution is the first attempt to make AI and statistical programming aligned.

Keep in mind that this is V0.1.

## ToDo
 - [ ] A file parser (in development)
 - [ ] Test cases 

## Licensing
GPL V3 applies - In short. You've received it free. You give it away for free or pay.

## What is it
AI's work on prompts and most AI currently have a limit on the number of files that can be shared with it. Prompt's will be the new programming code for the future - an aiGL of sorts. The purpose behind QSE is to have a prompt generator that can be read by AI and that is more human friendly, and industry safe. Ambiguity and vagueness is not something Pharma embraces.

Part of the constraints faced by programmers in the Pharma industry is what can go into a specification. These have to be written in a very specific manner which is not sufficient for AI. We tell what's be done not how, which is not what will be needed for AI. The SAP and ADRG supports this but leaves programmers clamoring through multiple files leading to a lose in productivity, and opening the door to vagueness and Ambiguity.

As this is V0.1 the primary problem to address is prompts or instructions.

### The Language
As AI will be doing all the heavy lifting the language is nothing more than a JSON file. The Language file is nothing more than a setup file on how the "Setup md file used by AI" should be interpreted. See details.

#### Naming convention
Any alpha numeric value.
No spacing in between
Substitute space with _

### QSE File format
The file by design is very similar to a markdown file. It is based on a predefined structure to ensure that creation and reading is consistent. To ensure that the files supplied to AI is kept to a minimum you can have multiple instructions in one file. See details

### Executing in AI
Run the following command in AI: 
Using qSpcExe_symbols.json executed the instruction in ADSL_age.md

#### Results
The results should generate but also importantly highlight the following:
Both rules include 12 as written.

I resolved that operationally by assigning 12 to group 1, because the first matching rule occurs first. That resolution is my implementation choice, not something specified by the source.

Also, the constraint permits ages through 80, while the supplied categorisation rules stop at 45, so ages >45 through 80 have no specified agegr1 assignment.

For qSpecExe testing, I'd therefore flag two specification queries: AGE = 12 boundary ownership, and AGE >45 through 80 classification.


## Flow chart
Flow chart based on ADaM specifications.

```mermaid
flowchart TD
  s(SAP)--> A(Annotated Shells)
  A-->SP(ADaM Specifications)-->H(Human Interaction)-->AI(Execute Instruction file) --> H1(Human Interaction Execute and verify results)

```

## AI Uploading 

### Mandatory
The following files are mandatory to be be uploaded:
- qSpcExe_symbols.json - This is the controller file.
- instruction file in md or text format.

### Recommended
The following files are strongly recommended to be be uploaded along with the mandatory ones:
- SAP or Protocol for SDTM
- Annotated shells or aCRF for SDTM
- Export of all datsets along with the Labels and variable names. SAS Proc Content
