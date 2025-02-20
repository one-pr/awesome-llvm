Awesome Clang [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
------

This doc was originally forked from https://github.com/ingve/awesome-clang and then maintained by me. However I prefer a monorepo for both LLVM and Clang, so moved here.

# Websites
- Project site: http://clang.llvm.org, and [its doxygen docs](https://clang.llvm.org/doxygen/index.html)
- [Clang @ LLVM Discourse](https://discourse.llvm.org/c/clang/6)
- [Clang @ StackOverflow](http://stackoverflow.com/questions/tagged/clang)
- [Clang @ reddit](https://www.reddit.com/r/Clang/)
- [Clang @ GitHub](https://github.com/topics/clang)
- [Open Projects](https://clang.llvm.org/OpenProjects.html)

# Tutorials

- 🐉 [Clang Compiler User’s Manual](https://clang.llvm.org/docs/UsersManual.html)
   - 🐉 [Clang Driver Configuration files](https://clang.llvm.org/docs/UsersManual.html#configuration-files), see also [GCC spec files](https://gcc.gnu.org/onlinedocs/gcc-13.2.0/gcc/Spec-Files.html) and [the tutorial](https://wozniak.ca/blog/2024/01/02/1/index.html)
- 🐉 [“Clang” CFE Internals Manual](https://clang.llvm.org/docs/InternalsManual.html) - good start for Clang frontend developers
- 🐉 [Clang Toolchain](https://clang.llvm.org/docs/Toolchain.html) - Toolchains when using Clang compiler driver
- 🐉 [Introduction to the Clang AST](https://clang.llvm.org/docs/IntroductionToTheClangAST.html) - a gentle introduction to the mysteries of the Clang AST.
- 🐉 [Matching the Clang AST](https://clang.llvm.org/docs/LibASTMatchers.html) - how to use Clang’s LibASTMatchers to match interesting nodes of the AST and execute code that uses the matched nodes.
- 🐉 [AST Matcher Reference](https://clang.llvm.org/docs/LibASTMatchersReference.html) - AST matchers implemented by Clang.
- 🐉 [Modules](https://clang.llvm.org/docs/Modules.html) - C++ modules
- :octocat: https://github.com/banach-space/clang-tutor - A collection of out-of-tree Clang plugins for teaching and learning
- :octocat: https://github.com/ronnie88597/Notes/tree/master/clang
- 📹 [Create your own Refactoring Tool in Clang](https://www.youtube.com/watch?v=8PndHo7jjHk) - Richard Thompson's presentation from C++Now 2014.
- 📹 [Refactoring C++ with Clang](https://www.youtube.com/watch?v=yuIOGfcOH0k) - Chandler Carruth's talk from C++Now 2012.
- 📹 [Automatic C++ source code generation with clang](https://www.youtube.com/watch?v=aPTyatTI42k) - Sergei Sadovnikov's ACCU 2017 talk.
- [Quick overview of how Clang works internally](http://cppdepend.com/blog/?p=321) - cppdepend's quick introduction
- [C Support in Clang](https://clang.llvm.org/c_status.html) and [C Defect Report Support in Clang](https://clang.llvm.org/cxx_dr_status.html)
- [C++ Support in Clang](https://clang.llvm.org/cxx_status.html) and [C++ Defect Report Support in Clang](https://clang.llvm.org/cxx_dr_status.html)
- [Data flow analysis: an informal introduction](https://clang.llvm.org/docs/DataFlowAnalysisIntro.html) - Clang's docs about data flow analysis, etc


# Official Tools/Libraries
- [libclang:](https://clang.llvm.org/doxygen/group__CINDEX.html) -  C Interface to Clang.
  - [Introduction to libclang](https://www.mikeash.com/pyblog/friday-qa-2014-01-24-introduction-to-libclang.html)
  - [Skipping library code in gdb with help from libClang](https://jefftrull.github.io/c++/gdb/python/libclang/llvm/2018/04/30/stepping-with-libclang.html) - using libClang’s Python bindings.
- [LibTooling](https://clang.llvm.org/docs/LibTooling.html) - library to support writing standalone tools based on Clang
  - [Tutorial for building tools using LibTooling and LibASTMatchers](https://clang.llvm.org/docs/LibASTMatchersTutorial.html)
  - [Modern source-to-source transformation with Clang and libTooling](https://eli.thegreenplace.net/2014/05/01/modern-source-to-source-transformation-with-clang-and-libtooling)
  - [AST matchers and Clang refactoring tools](https://eli.thegreenplace.net/2014/07/29/ast-matchers-and-clang-refactoring-tools)
  - [Compilation databases for Clang-based tools](https://eli.thegreenplace.net/2014/05/21/compilation-databases-for-clang-based-tools)
  - [LibTooling Example](https://kevinaboos.wordpress.com/2013/07/23/clang-tutorial-part-ii-libtooling-example/)
- [clang-check](http://clang.llvm.org/docs/ClangCheck.html) - Error checking and AST dumping based on [LibTooling](http://clang.llvm.org/docs/LibTooling.html)
- [scan-build](http://clang-analyzer.llvm.org/) - Clang Static Analyzer
- [scan-view](http://clang-analyzer.llvm.org/) - Clang Static Analysis Viewer
- [clang-tidy](http://clang.llvm.org/extra/clang-tidy.html) - [Lint-like checks and beyondslides](http://llvm.org/devmtg/2014-04/PDFs/Talks/clang-tidy%20LLVM%20Euro%202014.pdf)
- [clangd](https://clangd.llvm.org/) - clangd language server (for [LSP](https://microsoft.github.io/language-server-protocol/))
  - [CppCon 2018 -- Clangd: architecture of a scalable C++ language server](https://www.youtube.com/watch?v=5HIyAXj1YNQ)
  - [Clangd for Neovim](https://github.com/p00f/clangd_extensions.nvim)
  - [Clangd for VSCode](https://github.com/clangd/vscode-clangd)
  - [Clangd for Emacs](https://emacs-lsp.github.io/lsp-mode/page/lsp-clangd/)
- [clang-format](http://clang.llvm.org/docs/ClangFormat.html)
  - [clang-format docs](https://clang.llvm.org/docs/ClangFormat.html) - A tool to format C/C++/Java/JavaScript/Objective-C/Protobuf code.
  - [style options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) - clang-format style options.
  - [configurator](https://zed0.co.uk/clang-format-configurator/) -  clang-format configurator.
- [clang-tidy](https://clang.llvm.org/extra/clang-tidy/) - clang-based C++ linter tool.
  - [List of clang-tidy checks](https://clang.llvm.org/extra/clang-tidy/checks/list.html)
  - [Writing a basic clang static analysis check](https://bbannier.github.io/blog/2015/05/02/Writing-a-basic-clang-static-analysis-check.html)
- [pp-trace](https://clang.llvm.org/extra/pp-trace.html) - tool that traces preprocessor activity.
- [Clang Static Analyzer](https://clang-analyzer.llvm.org/index.html) - a source code analysis tool that finds bugs in C, C++, and Objective-C programs.
  - [scan-build](https://clang-analyzer.llvm.org/scan-build.html) -Running the analyzer from the command line (inactively maintained for cross-translation-unit analysis)
  - [Static Analysis with clang](https://btorpey.github.io/blog/2015/04/27/static-analysis-with-clang/)
  - [clang-analyzer-guide](https://github.com/haoNoQ/clang-analyzer-guide) An easy guide to Clang Static Analyzer extension.
- [AddressSanitizer](https://clang.llvm.org/docs/AddressSanitizer.html) - a fast memory error detector.
  - [overview by Mike Ash](https://www.mikeash.com/pyblog/friday-qa-2015-07-03-address-sanitizer.html)
- [ClangIR](https://github.com/llvm/clangir/tree/main) - A new (MLIR based) high-level IR for clang

# Unofficial Tools/Libraries
- [Checked C](https://github.com/microsoft/checkedc) - an extension to C that lets programmers write C code that is guaranteed by the compiler to be type-safe
- [C++ Insights](https://github.com/andreasfertig/cppinsights) - a clang-based tool which does source to source transformation. Its goal is it to make things visible which normally, and intentionally, happen behind the scenes. [Live/online demo](https://cppinsights.io/) available.
- [CodeChecker](https://github.com/Ericsson/codechecker) - an analyzer tooling, defect database and viewer extension for the Clang Static Analyzer and Clang Tidy
  - [docs](https://codechecker.readthedocs.io/en/latest/)
- [QT Clazy](https://github.com/KDE/clazy) - Qt-oriented static code analyzer based on the Clang framework (as a plugin and a standalone tool on top of libtooling)
- [trailofbits/VAST](https://github.com/trailofbits/vast) - VAST: MLIR for Program Analysis
- [trailofbits/PASTA](https://github.com/trailofbits/pasta) - Peter's Amazing Syntax Tree Analyzer
- [naivesystems/analyze](https://github.com/naivesystems/analyze) - NaiveSystems' analyzer (community version), 
- [kythe/Kythe](https://github.com/kythe/kythe) - a pluggable, (mostly) language-agnostic ecosystem for building tools that work with code
- [ccls](https://github.com/MaskRay/ccls) - a C++ language server, similar to clangd
  - [ccls for Neovim](https://github.com/ranjithshegde/ccls.nvim)
  - [ccls for VSCode](https://github.com/MaskRay/vscode-ccls/tree/master)
  - [ccls for Emacs](https://emacs-lsp.github.io/lsp-mode/page/lsp-ccls/)
- [sourcegraph/scip-clang](https://github.com/sourcegraph/scip-clang) - SCIP indexer for C and C++
- [sourcegraph/lsif-clang](https://github.com/sourcegraph/lsif-clang) - LSIF generator for C, C++ and Objective C
- [Clang Power Tools](https://github.com/Caphyon/clang-power-tools) - Visual Studio extension with Clang/LLVM tools (`clang++`, `clang-tidy` and `clang-format`).
- [rtags](https://github.com/Andersbakken/rtags) - A c/c++ client/server indexer for c/c++/objc[++]
- [llvm-clang-samples](https://github.com/eliben/llvm-clang-samples) - Examples of LLVM and Clang written by Dr. [Eli Bendersky](http://eli.thegreenplace.net/)
- [clang-llvm-tutorial](https://github.com/lijiansong/clang-llvm-tutorial) - clang & llvm examples
- [Bear](https://github.com/rizsotto/Bear) - A tool that generates a compilation database for clang tooling
- [compiledb](https://github.com/nickdiego/compiledb) -- Tool for generating Clang's JSON Compilation Database files for *make-based* build systems.
- [codebrowser](https://github.com/KDAB/codebrowser) - Woboq CodeBrowser
- [oclint](https://github.com/oclint) - A static source code analysis tool to improve quality and reduce defects for C, C++ and Objective-C
- [CppNameLint](https://github.com/dougpuob/cppnamelint) - a naming convention linter of C/C++ source code Based on libtooling
- [irony-mode](https://github.com/Sarcasm/irony-mode) - A C/C++ minor mode for Emacs powered by libclang.
- [c99-to-c89](https://github.com/libav/c99-to-c89/) - Tool to convert C99 code to MSVC-compatible C89.
- [ClangKit](https://github.com/macmade/ClangKit) - Objective-C frontend to LibClang.
- [cppast](https://github.com/foonathan/cppast) - Library to parse and work with the C++ AST (based on libclang, **to be archived**)
- [lloccount](https://github.com/neolynx/lloccount) - C/C++ Logical Lines Of Code Counter.
- [libclangmm](https://github.com/cppit/libclangmm) - C++-wrapper for libclang (developed for [juCi++](https://github.com/cppit/jucipp)) (based on libclang, **archived**)
- [Customizable Naming Convention Checker](https://github.com/mapbox/cncc/) - similar to clang-format, but for naming conventions only.
- [standardese](https://github.com/standardese/standardese) - A (work-in-progress) nextgen Doxygen for C++ (based on libclang)
- [C++Now 2017: clang-useful](https://github.com/peter-can-talk/cppnow-2017/tree/master)
- [clang-experiments](https://github.com/pr0g/clang-experiments/tree/main)
- [SCRT/avcleaner](https://github.com/SCRT/avcleaner) - C/C++ source obfuscator for antivirus bypass (based on libtooling)
- https://github.com/aras-p/ClangBuildAnalyzer - Clang build analysis tool using -ftime-trace
- [ClangQL](https://github.com/frabert/ClangQL) - Query C++ codebases using SQLite, based on Clangd indexing results

# Other Relevant Resources
- [GCC Static Analyzer](https://gcc.gnu.org/wiki/StaticAnalyzer)
- [godbolt - compiler explorer](https://godbolt.org/)
- https://github.com/AnthonyCalandra/modern-cpp-features
- https://github.com/andreasfertig/programming-with-cpp20
