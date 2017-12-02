### script标签
#### script描述
script标签表示浏览器解析HTML页面的时候运行这段script脚本，有两种引入方式：
- script标签中直接编写脚本
- 通过script标签的src属性引入外部脚本文件，外部脚本文件内容需用script标签包裹。

script标签可放置在HTML页面的header和body中，推荐放在body尾部，因为浏览器解析HTML页面是由上而下同步解析执行，如果header中要执行的script过多会导致页面元素解析延迟，
此时用户看到的页面是一片空白。  
#### script标签的属性：
- async 可选，表示应该立即下载脚本，但不应妨碍其他操作，只对外部脚本有效。
- charset 可选，表示通过src属性指定的外部脚本的代码的字符集。大多数浏览器会忽略它的值，很少人用。
- defer 可选，表示脚本可以延迟到文档完全被解析和显示后再执行。只对外部脚本文件有效。慎用，因为实际应用中设置defer属性的script标签往往执行顺序不确定。
有些浏览器会忽略这个属性。
- language 已废弃，大多数浏览器忽略。
- src 可选，表示要执行的外部脚本文件路径。
- type 可选，表示编写外部脚本文件的内容类型（也成为MIME类型），如JavaScript脚本文件一般为text/javascript，默认值为text/javascript。
### noscript标签
以下两种情况才会显示noscript的内容：  
- 浏览器不支持脚本
- 浏览器支持脚本但被禁用
