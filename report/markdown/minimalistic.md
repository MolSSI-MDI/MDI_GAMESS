# Minimalistic MDI Communication Test

This test verifies that the engine is capable of basic communication with an external engine.

## Failure Resolution

If this test fails, ensure that you have followed each of the steps outlined below.

### Step 1: Make the MDI Library Available to the Engine

In order to pass this test, the engine must be capable of calling the functions that are defined by the MDI Library, such as `MDI_Init()`.
The process for enabling this is fundamentally different depending on whether the engine is written in a compiled or interpreted language.

**Compiled Languages:** In the case of codes written in compiled languages, this requires that the code be compiled and linked against the MDI Library.

**Interpreted Languages:** The only interpreted language currently supported by MDI is Python.
If your engine is written in Python, you should first install the MDI Library during the `build_image` step in `mdimechanic.yml`.
This can be done trivially using `pip` (*e.g.* `pip install pymdi`).
Your engine can then import the MDI Library where needed (*e.g.* `import mdi`).

### Step 2: Initialize the MDI Library

Your code must initialize the MDI Library by calling the `MDI_Init()` function.
If your code uses the Message Passing Interface (MPI), you should call `MDI_Init()` after the call to `MPI_Init()`.
Otherwise, `MDI_Init()` should be called as early your code as possible.

### Step 3: Support Basic MDI Communication

