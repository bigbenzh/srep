0. make sure that you have g++ installed.

1. download FreeArc 0.67 alpha source code
   
   - [archive.org](https://web.archive.org/web/20150319192112/http://freearc.org/download/testing/FreeArc-0.67-alpha-sources.tar.bz2)
   
   - [mirror1](https://fa.krinkels.org/?download=1&kcccount=https://fa.krinkels.org/downloads/testing/FreeArc-0.67-alpha-sources.tar.bz2)
   
   - [mirror2](https://github.com/mirror/freearc)

2. download [srep source code ](https://web.archive.org/web/20160417040351/http://freearc.org/download/research/srep32.zip)

3. extract freearc and srep, then place srep.cpp in FREEARC_SOURCE_CODE_DIR/Compression/SREP/, and replace the original srep.cpp file.

4. for version 3.2 there is a name redefinition error in srep.cpp:
   
   `srep.cpp:338:8: error: redefinition of ‘struct MMAP_FILE’`
   
   delete the declaration of MMAP_FILE in srep.cpp line 338.

5. compile srep
   
   ```
   cd FREEARC_SOURCE_CODE_DIR/Compression/SREP/
   chmod +x compile
   ./compile
   ```

Compilation finished. You are able to run ./srep
