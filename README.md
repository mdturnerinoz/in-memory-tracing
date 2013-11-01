# In Memory Tracing

## Requriements

- C code that will trace in memory when called
- Flexible: will allow: caller-defined values to be passed: page boundary, max entries, wrap limit, number of entries per call, ???
- It must be aligned on a page boundary of the given system
- page faulting should be avoided if used by kernel code
- Concept based on the MVT/MVS internal trace at page 0 +x’54’
- Will need utility code to dump out the trace entries when needed
- Tracing must be able to be turned on and off via a function call
- Must have multi-language "wrappers" so it can be called by other-than-C (perhaps even difference language formats that are incompatible with C library calls (e.g. Java, OJBC, C#) 
- More to come as I think of it ...

## Usage

## Functions

## Testing

- There will need to be code to test the callable functions provided with this project.