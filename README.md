#  Install onnxruntime

- use : https://dev.to/wolfram27/setting-up-and-using-onnx-runtime-for-c-in-linux-1ho9

```bash
sudo apt update
sudo apt install build-essential cmake
tar xzf onnxruntime-linux-x64-1.27.0.tgz
cp -r include lib ./external/onnxruntime # path of project
```


# build application

```bash
mkdir build 
cd build
cmake ..
make
```

- put `best_model.onnx` in `build` directory before running application

# run application

```bash
cp ../best_model.onnx ./best_model.onnx
cp ../best_model.onnx.data ./best_model.onnx.data
./application
```