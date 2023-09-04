```
rm -rf build/ && mkdir build && cd build
cmake -DCMAKE_INSTALL_PREFIX="$(pwd)/install" ..
cmake --build .
cmake --install .
```