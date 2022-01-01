John Henry's Nim Coding Guidelines
==================================

1. When doing a release build, make sure to compile it with static linking,
   link-time optimization, and C's memory allocator. The flags needed should be put inside the ``nim.cfg`` file.

   Flags::
     -d:release --gc:orc -d:useMalloc -d:lto --passL:-static

2. Variables must have explicit types. 

3. Always put parentheses when calling procs.

4. Use the explicit ``range``  keyword when creating types. Use the shorthand 
   when using ranges in control flow keywords.

5. Always use ``{.pure.}`` enums over unpure enums. 