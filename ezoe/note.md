# Note

読書メモ:

## 概要

`$ g++ -o hello.out hello.cpp`

### コンパイラオプション

`$ g++ -std=c++17 -Wall --pedantic-errors -o a.out a.cpp b.cpp c.cpp`

### ヘッダーファイルの省略

`$ g++ -include all.h -std=c++17 -o hello2.out hello2.cpp`

### precompiled header

`$ time g++ -std=c++17 -Wall --pedantic-errors -include all.h -o hello2.out hello2.cpp`

`$ g++ -std=c++17 -Wall --pedantic-errors -x c++-header -o all.h.gch all.h`

`$ time g++ -std=c++17 -Wall --pedantic-errors -include all.h -o hello2.out hello2.cpp`

- before:
  + real    0m0.883s
  + user    0m0.609s
  + sys     0m0.266s

- after
  + real    0m0.300s
  + user    0m0.094s
  + sys     0m0.141s
