
各大视频站播放地址解析

## 代码结构
1. `scorpio`工程是核心代码，与业务相关的所有代码都放置在该工程下面
2. `stardustx`工程是项目用到到所有公共代码，包括第三方包(包括用`go get`命令安装)都放置在该工程下面

## 安装
1. 进入`scorpio`目录，执行`setup-gopath.sh`脚本，该脚本会把当前目录和`stardustx`项目设置为`gopath`
2. 提交代码之前先手动执行`format-src.sh`脚本，该脚本会用`golang`的标准方式格式化代码
3. 也可以直接在`git`本地的`pre-commit`的`hook`文件中加上上面格式化的脚本，避免每次手动执行

## 运行
1. 可以在`scorpio`根目录中新建一个`bin`文件夹
2. 进入`bin`文件夹，执行命令`go build scorpio/mathapp`
3. 在`bin`目录下面会生成一个`mathapp`的可执行文件，执行命令`./mathapp`即可得到运行结果
4. 也可以直接在`scorpio`根目录下面直接执行命令`go run src/scorpio/mathapp/main.go`得到运行结果
