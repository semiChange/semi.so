|author|contact|
|-----------|-----------|
|semi|wechat:wxsmcg|

#
`How to use`
- download semi.so ,put ini load folder eg. /usr/lib64/php/modules
+ modify php.ini add line "extension=semi.so"
- restart httpd or nginx



## namespace
>Semi
```c
Semi\Semi
```

## class  
>Semi
```c
new \Semi\Semi(s.conf);
```


## property
>private mac    // string
>queue          // array


## mothod
```c
// 构造函数
// @filename  配置文件路径 , 配置文件必须为标准的json格式, 不要有注释
// 返回值 无
__construct(filename)
{    
}    


// 超级打印
// @v	任意类型
// @d 是否 die d=1  exit
// 返回 无
s_print(v,d=0)
{
}

// 获取机器码
// @os=[linux]
s_getMacAddr(os = "linux")
{
}

// 加色 , 背景, 前景 
// @str 字符串
// @fg 	前景 [white]  black red green yellow blue purple skyblue
// @bg 	背景 [black]
//	30m 黑色字 , 40m 黑色底
//	31m 红色字 , 41m 红色底
//	32m 绿色字 , 42m 绿色底
//	33m 蓝色字 , 43m 黄色底
//	34m 黄色字 , 44m 蓝色底
//	35m 紫色字 , 45m 紫色底
//	36m 天蓝字 , 46m 天蓝底
//	37m 白色字 , 47m 白底黑
//  @return string
s_color(string str,string fg="white",string bg="black")
{
}

// 解析字符串 
// @str = 1234567890abcdefghijklmnopqrstuvwxyz // ?判断纯hex
// @arr = array(
// 		"header"=>array(
// 			2,
// 			function($t){return $t."123";}	// must return value
// 		),
// 		"aa"=>2,
// 		"bb"=>5,
// 		"cc"=>7
// )
// @return array(k=>v,k=>v)
s_parse(s_str_hex,a_arr = [])
{
}

// json 字符串 unicode
// @s_str
// 返回字符串
s_json_encode(s_str){
} 

// mysql sel sql produce
// @array , tablename ,where
// @return string
s_sel(a_fields,s_table,s_where="")
{
}
  
// ins sql
// string @tablename, 
// array @array(fields=>values)
// 键值对方式  'name'=>'tom'
// string @return 
s_ins(s_table,a_f_v)
{
}

// upd sql
// tablename , key=>val , where
// return sql
s_upd(s_table, a_f_v, s_where="1")
{
}

// curl request
// @url    
// @data
s_curl(s_url, a_data = [])
{
}

// hex string  , semi:xxxx => xxxx
// string @s_head , is filter head for debug
// String @s_msg  , is a binary stream
// return string s_hexres
s_hexfilter(s_head,s_msg)
{
}

// for log record 
// @msg mix
// @s_pathFilename 
s_log(m_msg,s_pathFilename)
{
}


// for pri and pub generate  2048bit
s_keygen()
{
}

// encrypt string 
// @s_str string 
// @s_key string
s_encrypt(string s_str,string s_key){
}

// encrypt string 
// @s_str string 
// @s_key string
s_decrypt(s_str,s_key)
{
}



```







===
[baidu](https://www.baidu.com "123")

[lianjie][1]

[1]:https://www.baidu.com

- [x] 需求分析
- [ ] 交付

`biaoji`
