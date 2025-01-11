#### Completed Tasks
target: aarch64-unknown-linux-gnu
- using aarch64 to emulate arm architecture, unknown provider, linux os, gnu C compiler
- After qemu, emulating the 2017 version(raspberry) failed to handle the complex functions due to size restrictions(277 mb)
so now using fvp to emulate functions
- related to ARM Cortex-A series models(from [arm fvps](https://developer.arm.com/Tools%20and%20Software/Fixed%20Virtual%20Platforms/Arm%20Architecture%20FVPs))
- compiles correctly, not a tarbell file but extracts right after clicking on it!
- fvp model is FVP_Base_RevC-2xAEMvA inside FVP_Base_RevC-2xAEMvA_11.27_19_Linux64/Base_RevC_AEMvA_pkg/models/Linux64_GCC-9.3
- model runs directly from path specification(need to create a makefile to contain the model running configurations, fvp environment)
- fuzzrmirsi builds inside ./target/aarch64-unknown-linux-gnu/release/

#### Remaining Tasks
1. figure out how to simulate with FVP_Base_RevC-2xAEMvA with all 4 terminals
2. log outputs as per the rust project
3. simulate some basic rmi & rsi functions
4. simulate tests as realms and try mvp of that(including test data, working, log output)
