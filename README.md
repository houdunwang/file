#上传组件

File组件提供非常方便的上传处理与下载等相关功能

##上传

####实例化对象
```
$obj = new \houdunwang\file\File();
```

####初始化配置

```
//初始化配置
$obj->init( [
	//允许上传类型
	'type' => 'jpg,jpeg,gif,png,zip,rar,doc,txt,pem',
	//允许上传大小单位KB
	'size' => 10000,
	//上传路径
	'path' => 'attachment',
] );
```

####上传文件

```
$files = $obj->make();
```

####指定上传表单

```
$obj->upload('ico');
```
####设置上传类型

```
$obj->type('jpg,png,txt')->upload();
```

####设置上传大小

```
$obj->type('jpg,png,txt')->size(2000000)->upload();
```

####获取上传错误

```
$obj->getError();
```

####设置上传目录

```
$obj->path('News')->upload();
```

##下载

####下载文件处理
```
//下载z.zip，下载文件名不a.zip
$obj->download('z.zip','a.zip');
```