Sunlight Upload
===============================
上传文件类
----------------------------
```
功能包含：
1. 文件大小验证
2. 文件格式验证
3. 支持生成子目录
```

使用例子
------------------------------
```
<?php
if (isset($_FILES)) {
	include 'SunlightUpload.php';
	$upload = new SunlightUpload(array('exts' => array('jpg', 'png', 'gif', 'zip'), 'maxSize' => 102400));
	$reslut = $upload->upload('file');
	if (!$reslut) {
		$reslut = $upload->error;
	}
	print_r($reslut);
}

?>
```