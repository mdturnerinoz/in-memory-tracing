# In Memory Tracing

## Requriements

- C code that will trace in memory when called
- Flexible: will allow: caller-defined values to be passed: page boundary, max entries, wrap limit, number of entries per call, ???
- It must be aligned on a page boundary of the given system
- page faulting should be avoided if used by kernel code
- Concept based on the MVT/MVS internal trace at page 0 +x’54’
- Will need utility code to dump out the trace entries when needed. This must include: in a dump/debug session and then later while a process is active and perhaps even remotely (e.g. RPC).
- Tracing must be able to be turned on and off via a function call (with entries indicating it was off or "lost entries")
- Must have multi-language "wrappers" so it can be called by other-than-C (perhaps even difference language formats that are incompatible with C library calls (e.g. C++, Java, OBJC, C#) (C will be the first and the others will come after it as I find the time/energy... :0) )
- Entires must be varied sizes (needs more thought): 8-bit, 16-bit, 32-bit, 64-bit, 128-bit (??): and all must fit within the max per-call size (and within the page boundary). Note that the base items (id, time-stamp, caller id/location) must fit within the basic scheme well-enough to provide information while not impinging too much on the data needed to be traced (i.e. Not too big per item but big "enough")
- More to come as I think of it :0) ...

## Usage

## Functions

## Testing

- There will need to be code to test the callable functions provided with this project.