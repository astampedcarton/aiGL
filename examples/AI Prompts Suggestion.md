# Prompts in AI usage

## Example 1
Using the supplied language-definition file (aiGL.json) as the authoritative definition of the specification language, interpret and execute the supplied specification file (Example_2.md).

Derive the meaning and behaviour of all syntax, symbols, sections, directives, and references from the language definition. Execute each specification block according to those definitions. Follow all defined constraints, verification rules, traceability requirements, and ambiguity-handling behaviour.

Do not silently infer, correct, or resolve requirements that are unspecified, contradictory, or ambiguous. Report such cases explicitly.

### Notes 
This example is a bit more detailed and could be reduced to.

## Example 2
Interpret and execute the specification in Example_2.md, using aiGL.json as the authoritative definition of the specification language. Do not assume semantics not defined by the language definition.

### Notes
In both examples it's important that language is clear and explicitly clear. The more ambigous the less reliable the results.
