# 注意事项

编译 g2o with QGLViewer

1. 首先安装qt5
   ```shell
   brew install qt5
   ```
2. 编译安装QGLViewer
   注釋QGLViewer/QGLViewer.pro文件下面行, 編譯成dylib, 方便g2o找到
   ```shell
   macx|darwin-g++ {
	# Default setting creates a Mac framework. Comment out this line to create a dylib instead.
	# !staticlib: CONFIG *= lib_bundle
   ```

   ```shell
   /path/to/qmake PREFIX=/usr/local/
   make
   make install
   ```
3. 编译安装 g2o with QGLViewer  
   g2o 可能找不到qt5, 需要手動指定`QT5_DIR`