# aiGL - (ai Generation Language)
 
## Introduction
As AI is gaining traction. No industry has been left untouched. We've started embracing it more.

It all started with the idea of Quality Spec Execution, but quickly evolved to aiGL. As this is a platform/framework rather than a program.

Clearer instructions means less time spend talking to AI. 

Keep in mind that this is V0.1.

## Licensing
Apache License 2.0.

## What is it
AI's work on prompts and most AI currently have a limit on the number of files that can be shared with it. Prompt's have become the new programming code for the future. Programmers are natural AI's, but we've now move one level up to a place where we've found frustration over the years - vague specifications.

The purpose behind aiGL is to have a structure flexible language that you define based on instructions you create that can be read by AI and that is more human friendly, clearer and flexible. Ambiguity and vagueness is not something industries embrace.

By nature spec tend to be vague with a certain level of attained knowledge assumed. We largely tell what's be done, not how, and we treat AI the same. All of this leaves programmers clamouring through multiple documents that may or may not say the same leading to a loss in productivity. 

As this is V0.1 the primary problem to address is language setup and instructions.

### The Language
As AI will be doing all the heavy lifting the language is nothing more than a JSON file, that you create and maintain. It's nothing more than a setup file on how the "Setup md file used by AI" should be interpreted. See details.

#### Naming convention
Any alpha numeric value.
No spacing in between
Substitute space with _

### When to use
This is a question not everyone asks, but is a very important question. Almost any language can be used to solve a problem. The question that needs answering is if it's the right tool for the job.

If you have for example `Set to Y when Age < 12` and there is no other significance around it, you might actually be wasting time.
if you have for example `Set to Y when Age < 12 and is from South Africa with parents aged >= 30. Flagging parents with age < 30 if the age is 12` you have a better use.

The general rule to apply is if it's got multiple dependencies you have a good use case. 

### aiGL Instruction File format
The file format by design is very similar to a markdown file. It is based on a predefined structure to ensure that creation and reading is consistent. To ensure that the files supplied to AI is kept to a minimum you can have multiple instructions in one file. See details

### Executing in AI
Run the following command in AI: 
Using aiGL.json executed the instruction in ADSL_age.md

#### Results
Don't simply ignore what's written read through the results before copying the content. 

## AI Uploading 

### Mandatory
The following files are mandatory to be be uploaded:
- aiGL.json - This is the language controller file.
- instruction file in md or text format.

### Recommended
The following files are strongly recommended to be be uploaded along with the mandatory ones:
 - Any source documents to support the instructions
 - Any additional notes that can provide clarity

#### Example for the Pharma industry
- SAP or Protocol for SDTM
- Annotated shells extract in JSON format or aCRF for SDTM
- Export of all datasets along with the Labels and variable names. i.e. SAS Proc Content
