Добавила .travis.yml
```

language: cpp

script:
- cd solver_application
- cmake .
- make
- cd ..
- cd hello_world_application
- cmake .
- make

addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
      - mingw-w64
```

Добавила строчку 

```
set(CMAKE_CXX_STANDARD 11)
```
в оба CMakeLists.txt

Подключила трейвис
