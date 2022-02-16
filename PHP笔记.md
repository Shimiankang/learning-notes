# PHP笔记


##### PHP 官方手册：https://www.php.net/manual-lookup.php?pattern=manuai%2Fzh%2F&lang=zh&scope=404quickref

print_r ( )    打印

include在引入不存文件时产生一个警告且脚本还会继续执行，

require则会导致一个致命性错误且脚本停止执行。

phpinfo ( ) 查看php详细信息

$变量名 = 值 ;

$a='1' ;  $b="1$a" ;   双引号与单引号的区别 ： 单引号不识别变量名，

##### 而双引号识别；	

echo $a;   打印  print ( ) 打印 两者的区别是 echo 没有返回值而

print（）有返回值；

form 表单里：$GET $POST   两个传值方式

$FILE    form表单后面必须加  enctype=" multipart/form-data "；

##### 服务器端：检索文件，并相应客户端的HTTP请求=Apache、Nginx=服务器；

B/S架构的软件：phpstudy_pro，

server = 服务器

borrow = 浏览器

WAMP :  W = window       A=Apache        M=MySqL         P=php

WNMP：W = window       N=Nginx        M=MySqL         P=php

##### 同理还有  MAMP 就是苹果电脑的 还有 LAMP 是Linux的；

echo substr("Hello world",6);  字符返回‘world’

substr(string,start,length)  字符串截取

##### PHP函数：

```php
1 exit(); // 退出 执行到这一步 下面的代码就不会执行了；
```
#### PHP数学函数：

###### 常见的：

abs ( ) 求绝对值  ； floor ( ) 舍去法取整； ceil（） 进一法取整； round（） 四舍五入； min（）最小值；max（）最大值；

##### 完整一点的：

| 函数                                                         | 描述                                                  |
| :----------------------------------------------------------- | :---------------------------------------------------- |
| [abs()](https://www.runoob.com/php/func-math-abs.html)       | 返回一个数的绝对值。                                  |
| [acos()](https://www.runoob.com/php/func-math-acos.html)     | 返回一个数的反余弦。                                  |
| [acosh()](https://www.runoob.com/php/func-math-acosh.html)   | 返回一个数的反双曲余弦。                              |
| [asin()](https://www.runoob.com/php/func-math-asin.html)     | 返回一个数的反正弦。                                  |
| [asinh()](https://www.runoob.com/php/func-math-asinh.html)   | 返回一个数的反双曲正弦。                              |
| [atan()](https://www.runoob.com/php/func-math-atan.html)     | 返回一个数的反正切。                                  |
| [atan2()](https://www.runoob.com/php/func-math-atan2.html)   | 返回两个变量 x 和 y 的反正切。                        |
| [atanh()](https://www.runoob.com/php/func-math-atanh.html)   | 返回一个数的反双曲正切。                              |
| [base_convert()](https://www.runoob.com/php/func-math-base-convert.html) | 在任意进制之间转换数字。                              |
| [bindec()](https://www.runoob.com/php/func-math-bindec.html) | 把二进制数转换为十进制数。                            |
| [ceil()](https://www.runoob.com/php/func-math-ceil.html)     | 向上舍入为最接近的整数。                              |
| [cos()](https://www.runoob.com/php/func-math-cos.html)       | 返回一个数的余弦。                                    |
| [cosh()](https://www.runoob.com/php/func-math-cosh.html)     | 返回一个数的双曲余弦。                                |
| [decbin()](https://www.runoob.com/php/func-math-decbin.html) | 把十进制数转换为二进制数。                            |
| [dechex()](https://www.runoob.com/php/func-math-dechex.html) | 把十进制数转换为十六进制数。                          |
| [decoct()](https://www.runoob.com/php/func-math-decoct.html) | 把十进制数转换为八进制数。                            |
| [deg2rad()](https://www.runoob.com/php/func-math-deg2rad.html) | 将角度值转换为弧度值。                                |
| [exp()](https://www.runoob.com/php/func-math-exp.html)       | 返回 Ex 的值。                                        |
| [expm1()](https://www.runoob.com/php/func-math-expm1.html)   | 返回 Ex - 1 的值。                                    |
| [floor()](https://www.runoob.com/php/func-math-floor.html)   | 向下舍入为最接近的整数。                              |
| [fmod()](https://www.runoob.com/php/func-math-fmod.html)     | 返回 x/y 的浮点数余数。                               |
| [getrandmax()](https://www.runoob.com/php/func-math-getrandmax.html) | 返回通过调用 rand() 函数显示的随机数的最大可能值。    |
| [hexdec()](https://www.runoob.com/php/func-math-hexdec.html) | 把十六进制数转换为十进制数。                          |
| [hypot()](https://www.runoob.com/php/func-math-hypot.html)   | 计算直角三角形的斜边长度。                            |
| [is_finite()](https://www.runoob.com/php/func-math-is-finite.html) | 判断是否为有限值。                                    |
| [is_infinite()](https://www.runoob.com/php/func-math-is-infinite.html) | 判断是否为无限值。                                    |
| [is_nan()](https://www.runoob.com/php/func-math-is-nan.html) | 判断是否为非数值。                                    |
| [lcg_value()](https://www.runoob.com/php/func-math-lcg-value.html) | 返回范围为 (0, 1) 的一个伪随机数。                    |
| [log()](https://www.runoob.com/php/func-math-log.html)       | 返回一个数的自然对数（以 E 为底）。                   |
| [log10()](https://www.runoob.com/php/func-math-log10.html)   | 返回一个数的以 10 为底的对数。                        |
| [log1p()](https://www.runoob.com/php/func-math-log1p.html)   | 返回 log(1+number)                                    |
| [max()](https://www.runoob.com/php/func-math-max.html)       | 返回一个数组中的最大值，或者几个指定值中的最大值。    |
| [min()](https://www.runoob.com/php/func-math-min.html)       | 返回一个数组中的最小值，或者几个指定值中的最小值。    |
| [mt_getrandmax()](https://www.runoob.com/php/func-math-mt-getrandmax.html) | 返回通过调用 mt_rand() 函数显示的随机数的最大可能值。 |
| [mt_rand()](https://www.runoob.com/php/func-math-mt-rand.html) | 使用 Mersenne Twister 算法生成随机整数。              |
| [mt_srand()](https://www.runoob.com/php/func-math-mt-srand.html) | 播种 Mersenne Twister 随机数生成器。                  |
| [octdec()](https://www.runoob.com/php/func-math-octdec.html) | 把八进制数转换为十进制数。                            |
| [pi()](https://www.runoob.com/php/func-math-pi.html)         | 返回圆周率 PI 的值。                                  |
| [pow()](https://www.runoob.com/php/func-math-pow.html)       | 返回 x 的 y 次方。                                    |
| [rad2deg()](https://www.runoob.com/php/func-math-rad2deg.html) | 把弧度值转换为角度值。                                |
| [rand()](https://www.runoob.com/php/func-math-rand.html)     | 返回随机整数。                                        |
| [round()](https://www.runoob.com/php/func-math-round.html)   | 对浮点数进行四舍五入。                                |
| [sin()](https://www.runoob.com/php/func-math-sin.html)       | 返回一个数的正弦。                                    |
| [sinh()](https://www.runoob.com/php/func-math-sinh.html)     | 返回一个数的双曲正弦。                                |
| [sqrt()](https://www.runoob.com/php/func-math-sqrt.html)     | 返回一个数的平方根。                                  |
| [srand()](https://www.runoob.com/php/func-math-srand.html)   | 播种随机数生成器。                                    |
| [tan()](https://www.runoob.com/php/func-math-tan.html)       | 返回一个数的正切。                                    |
| [tanh()](https://www.runoob.com/php/func-math-tanh.html)     | 返回一个数的双曲正切。                                |



## PHP 5 预定义的 Math 常量

| 常量                | 值                     | 描述                                  | PHP 版本 |
| :------------------ | :--------------------- | :------------------------------------ | :------- |
| INF                 | INF                    | 无限                                  | PHP 4    |
| M_E                 | 2.7182818284590452354  | 返回 e                                | PHP 4    |
| M_EULER             | 0.57721566490153286061 | 返回 Euler 常量                       | PHP 4    |
| M_LNPI              | 1.14472988584940017414 | 返回圆周率 PI 的自然对数：log_e(pi)   | PHP 5.2  |
| M_LN2               | 0.69314718055994530942 | 返回 2 的自然对数：log_e 2            | PHP 4    |
| M_LN10              | 2.30258509299404568402 | 返回 10 的自然对数：log_e 10          | PHP 4    |
| M_LOG2E             | 1.4426950408889634074  | 返回 E 的以 2 为底的对数：log_2 e     | PHP 4    |
| M_LOG10E            | 0.43429448190325182765 | 返回 E 的以 10 为底的对数：log_10 e   | PHP 4    |
| M_PI                | 3.14159265358979323846 | 返回 Pi                               | PHP 4    |
| M_PI_2              | 1.57079632679489661923 | 返回 Pi/2                             | PHP 4    |
| M_PI_4              | 0.78539816339744830962 | 返回 Pi/4                             | PHP 4    |
| M_1_PI              | 0.31830988618379067154 | 返回 1/Pi                             | PHP 4    |
| M_2_PI              | 0.63661977236758134308 | 返回 2/Pi                             | PHP 4    |
| M_SQRTPI            | 1.77245385090551602729 | 返回圆周率 PI 的平方根：sqrt(pi)      | PHP 5.2  |
| M_2_SQRTPI          | 1.12837916709551257390 | 返回圆周率 PI 的 2/平方根：2/sqrt(pi) | PHP 4    |
| M_SQRT1_2           | 0.70710678118654752440 | 返回 1/2 的平方根：1/sqrt(2)          | PHP 4    |
| M_SQRT2             | 1.41421356237309504880 | 返回 2 的平方根：sqrt(2)              | PHP 4    |
| M_SQRT3             | 1.73205080756887729352 | 返回 3 的平方根：sqrt(3)              | PHP 5.2  |
| NAN                 | NAN                    | 不是一个数字                          | PHP 4    |
| PHP_ROUND_HALF_UP   | 1                      | 遇到 .5 的情况时向上舍入              | PHP 5.3  |
| PHP_ROUND_HALF_DOWN | 2                      | 遇到 .5 的情况时向下舍入              | PHP 5.3  |
| PHP_ROUND_HALF_EVEN | 3                      | 遇到 .5 的情况时取偶数舍入            | PHP 5.3  |
| PHP_ROUND_HALF_ODD  | 4                      | 遇到 .5 的情况时取奇数舍入            | PHP 5.3  |

#### PHP常量：

TRUE  真； FALSE  假； E_ERROR  1错误； E_WARNING  警告； E_PARSE  34解析错误；

E_NOTICE  8非关键错误； M_PI  圆周率； __ FILE __  当前文件地址也是文件名称；

PHP_OS  当前系统； PHP_VERSION  当前PHP版本；

__ LINE __  当前行数； __ CLASS __  当前类名

__ METHOD __  当前的方法名； __ FUNCTION __  当前的函数名称；

NULL  空值；

#### PHP函数：

array_unshift ( ) 函数降新元素添加到数组头部；array_push（）函数将每一个新元素添加到数组的末尾；

array_shift ( ) 删除数组第一个元素；array_pop ( ) 删除并返回数组末尾的第一个元素；

array_rand ( ) 返回数组中的一个或多个键；

explode ( ) 将字符串转换成数组；implode（）将数组转换成字符串；

例如：a=explode（ "分隔符" ,$string）这样就把$string 字符以分隔符的方式转换成了数组

is_array ( ) 判断是否是数组； is_float ( ) 、is_double ( ) 、is_real () 是否是浮点类型；

is_int ( ) 、is_integer ( ) 、is_long ( ) 判断是否是整型； is_string ( ) 判断是否是字符串； is_object ( ) 判断是否是对象；

is_resource ( ) 判断是否是资源对象； is_null ( ) 判断是否是空；

Is_numeric ( ) 判断是否是任何类型的数字或数字字符串；

empty（）用来判断一个变量的值是否为空，如果为空则返回 true 否则false；

#### PHP数组函数：

##### 参考手册：

| 函数                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [array()](https://www.runoob.com/php/func-array.html)        | 创建数组。                                                   |
| [array_change_key_case()](https://www.runoob.com/php/func-array-change-key-case.html) | 返回其键均为大写或小写的数组。                               |
| [array_chunk()](https://www.runoob.com/php/func-array-chunk.html) | 把一个数组分割为新的数组块。                                 |
| [array_column()](https://www.runoob.com/php/func-array-column.html) | 返回输入数组中某个单一列的值。                               |
| [array_combine()](https://www.runoob.com/php/func-array-combine.html) | 通过合并两个数组（一个为键名数组，一个为键值数组）来创建一个新数组。 |
| [array_count_values()](https://www.runoob.com/php/func-array-count-values.html) | 用于统计数组中所有值出现的次数。                             |
| [array_diff()](https://www.runoob.com/php/func-array-diff.html) | 比较数组，返回两个数组的差集（只比较键值）。                 |
| [array_diff_assoc()](https://www.runoob.com/php/func-array-diff-assoc.html) | 比较数组，返回两个数组的差集（比较键名和键值）。             |
| [array_diff_key()](https://www.runoob.com/php/func-array-diff-key.html) | 比较数组，返回两个数组的差集（只比较键名）。                 |
| [array_diff_uassoc()](https://www.runoob.com/php/func-array-diff-uassoc.html) | 比较数组，返回两个数组的差集（比较键名和键值，使用用户自定义的键名比较函数）。 |
| [array_diff_ukey()](https://www.runoob.com/php/func-array-diff-ukey.html) | 比较数组，返回两个数组的差集（只比较键名，使用用户自定义的键名比较函数）。 |
| [array_fill()](https://www.runoob.com/php/func-array-fill.html) | 用给定的键值填充数组。                                       |
| [array_fill_keys()](https://www.runoob.com/php/func-array-fill-keys.html) | 用给定的指定键名的键值填充数组。                             |
| [array_filter()](https://www.runoob.com/php/func-array-filter.html) | 用回调函数过滤数组中的元素。                                 |
| [array_flip()](https://www.runoob.com/php/func-array-flip.html) | 反转/交换数组中的键名和对应关联的键值。                      |
| [array_intersect()](https://www.runoob.com/php/func-array-intersect.html) | 比较数组，返回两个数组的交集（只比较键值）。                 |
| [array_intersect_assoc()](https://www.runoob.com/php/func-array-intersect-assoc.html) | 比较数组，返回两个数组的交集（比较键名和键值）。             |
| [array_intersect_key()](https://www.runoob.com/php/func-array-intersect-key.html) | 比较数组，返回两个数组的交集（只比较键名）。                 |
| [array_intersect_uassoc()](https://www.runoob.com/php/func-array-intersect-uassoc.html) | 比较数组，返回两个数组的交集（比较键名和键值，使用用户自定义的键名比较函数）。 |
| [array_intersect_ukey()](https://www.runoob.com/php/func-array-intersect-ukey.html) | 比较数组，返回两个数组的交集（只比较键名，使用用户自定义的键名比较函数）。 |
| [array_key_exists()](https://www.runoob.com/php/func-array-key-exists.html) | 检查指定的键名是否存在于数组中。                             |
| [array_key_first()](https://www.runoob.com/php/func-array-key-first.html) | 获取指定数组的第一个键值。                                   |
| [array_key_last()](https://www.runoob.com/php/func-array-key-last.html) | 获取指定数组的最后一个键值。                                 |
| [array_keys()](https://www.runoob.com/php/func-array-keys.html) | 返回数组中所有的键名。                                       |
| [array_map()](https://www.runoob.com/php/func-array-map.html) | 将用户自定义函数作用到给定数组的每个值上，返回新的值。       |
| [array_merge()](https://www.runoob.com/php/func-array-merge.html) | 把一个或多个数组合并为一个数组。                             |
| [array_merge_recursive()](https://www.runoob.com/php/func-array-merge-recursive.html) | 递归地把一个或多个数组合并为一个数组。                       |
| [array_multisort()](https://www.runoob.com/php/func-array-multisort.html) | 对多个数组或多维数组进行排序。                               |
| [array_pad()](https://www.runoob.com/php/func-array-pad.html) | 将指定数量的带有指定值的元素插入到数组中。                   |
| [array_pop()](https://www.runoob.com/php/func-array-pop.html) | 删除数组中的最后一个元素（出栈）。                           |
| [array_product()](https://www.runoob.com/php/func-array-product.html) | 计算数组中所有值的乘积。                                     |
| [array_push()](https://www.runoob.com/php/func-array-push.html) | 将一个或多个元素插入数组的末尾（入栈）。                     |
| [array_rand()](https://www.runoob.com/php/func-array-rand.html) | 从数组中随机选出一个或多个元素，返回键名。                   |
| [array_reduce()](https://www.runoob.com/php/func-array-reduce.html) | 通过使用用户自定义函数，迭代地将数组简化为一个字符串，并返回。 |
| [array_replace()](https://www.runoob.com/php/func-array-replace.html) | 使用后面数组的值替换第一个数组的值。                         |
| [array_replace_recursive()](https://www.runoob.com/php/func-array-replace-recursive.html) | 递归地使用后面数组的值替换第一个数组的值。                   |
| [array_reverse()](https://www.runoob.com/php/func-array-reverse.html) | 将原数组中的元素顺序翻转，创建新的数组并返回。               |
| [array_search()](https://www.runoob.com/php/func-array-search.html) | 在数组中搜索给定的值，如果成功则返回相应的键名。             |
| [array_shift()](https://www.runoob.com/php/func-array-shift.html) | 删除数组中的第一个元素，并返回被删除元素的值。               |
| [array_slice()](https://www.runoob.com/php/func-array-slice.html) | 返回数组中的选定部分。                                       |
| [array_splice()](https://www.runoob.com/php/func-array-splice.html) | 把数组中的指定元素去掉并用其它值取代。                       |
| [array_sum()](https://www.runoob.com/php/func-array-sum.html) | 返回数组中所有值的和。                                       |
| [array_udiff()](https://www.runoob.com/php/func-array-udiff.html) | 比较数组，返回两个数组的差集（只比较键值，使用一个用户自定义的键名比较函数）。 |
| [array_udiff_assoc()](https://www.runoob.com/php/func-array-udiff-assoc.html) | 比较数组，返回两个数组的差集（比较键名和键值，使用内建函数比较键名，使用用户自定义函数比较键值）。 |
| [array_udiff_uassoc()](https://www.runoob.com/php/func-array-udiff-uassoc.html) | 比较数组，返回两个数组的差集（比较键名和键值，使用两个用户自定义的键名比较函数）。 |
| [array_uintersect()](https://www.runoob.com/php/func-array-uintersect.html) | 比较数组，返回两个数组的交集（只比较键值，使用一个用户自定义的键名比较函数）。 |
| [array_uintersect_assoc()](https://www.runoob.com/php/func-array-uintersect-assoc.html) | 比较数组，返回两个数组的交集（比较键名和键值，使用内建函数比较键名，使用用户自定义函数比较键值）。 |
| [array_uintersect_uassoc()](https://www.runoob.com/php/func-array-uintersect-uassoc.html) | 比较数组，返回两个数组的交集（比较键名和键值，使用两个用户自定义的键名比较函数）。 |
| [array_unique()](https://www.runoob.com/php/func-array-unique.html) | 删除数组中重复的值。                                         |
| [array_unshift()](https://www.runoob.com/php/func-array-unshift.html) | 在数组开头插入一个或多个元素。                               |
| [array_values()](https://www.runoob.com/php/func-array-values.html) | 返回数组中所有的值。                                         |
| [array_walk()](https://www.runoob.com/php/func-array-walk.html) | 对数组中的每个成员应用用户函数。                             |
| [array_walk_recursive()](https://www.runoob.com/php/func-array-walk-recursive.html) | 对数组中的每个成员递归地应用用户函数。                       |
| [arsort()](https://www.runoob.com/php/func-array-arsort.html) | 对关联数组按照键值进行降序排序。                             |
| [asort()](https://www.runoob.com/php/func-array-asort.html)  | 对关联数组按照键值进行升序排序。                             |
| [compact()](https://www.runoob.com/php/func-array-compact.html) | 创建一个包含变量名和它们的值的数组。                         |
| [count()](https://www.runoob.com/php/func-array-count.html)  | 返回数组中元素的数目。                                       |
| [current()](https://www.runoob.com/php/func-array-current.html) | 返回数组中的当前元素。                                       |
| [each()](https://www.runoob.com/php/func-array-each.html)    | 返回数组中当前的键／值对。                                   |
| [end()](https://www.runoob.com/php/func-array-end.html)      | 将数组的内部指针指向最后一个元素。                           |
| [extract()](https://www.runoob.com/php/func-array-extract.html) | 从数组中将变量导入到当前的符号表。                           |
| [in_array()](https://www.runoob.com/php/func-array-in-array.html) | 检查数组中是否存在指定的值。                                 |
| [key()](https://www.runoob.com/php/func-array-key.html)      | 从关联数组中取得键名。                                       |
| [krsort()](https://www.runoob.com/php/func-array-krsort.html) | 对关联数组按照键名降序排序。                                 |
| [ksort()](https://www.runoob.com/php/func-array-ksort.html)  | 对关联数组按照键名升序排序。                                 |
| [list()](https://www.runoob.com/php/func-array-list.html)    | 把数组中的值赋给一些数组变量。                               |
| [natcasesort()](https://www.runoob.com/php/func-array-natcasesort.html) | 用"自然排序"算法对数组进行不区分大小写字母的排序。           |
| [natsort()](https://www.runoob.com/php/func-array-natsort.html) | 用"自然排序"算法对数组排序。                                 |
| [next()](https://www.runoob.com/php/func-array-next.html)    | 将数组中的内部指针向后移动一位。                             |
| [pos()](https://www.runoob.com/php/func-array-pos.html)      | current() 的别名。                                           |
| [prev()](https://www.runoob.com/php/func-array-prev.html)    | 将数组的内部指针倒回一位。                                   |
| [range()](https://www.runoob.com/php/func-array-range.html)  | 创建一个包含指定范围的元素的数组。                           |
| [reset()](https://www.runoob.com/php/func-array-reset.html)  | 将数组的内部指针指向第一个元素。                             |
| [rsort()](https://www.runoob.com/php/func-array-rsort.html)  | 对数值数组进行降序排序。                                     |
| [shuffle()](https://www.runoob.com/php/func-array-shuffle.html) | 把数组中的元素按随机顺序重新排列。                           |
| [sizeof()](https://www.runoob.com/php/func-array-sizeof.html) | count() 的别名。                                             |
| [sort()](https://www.runoob.com/php/func-array-sort.html)    | 对数值数组进行升序排序。                                     |
| [uasort()](https://www.runoob.com/php/func-array-uasort.html) | 使用用户自定义的比较函数对数组中的键值进行排序。             |
| [uksort()](https://www.runoob.com/php/func-array-uksort.html) | 使用用户自定义的比较函数对数组中的键名进行排序。             |
| [usort()](https://www.runoob.com/php/func-array-usort.html)  | 使用用户自定义的比较函数对数组进行排序。                     |

#### PHP字符串函数：

###### strip_tags（字符串，规定允许的标签）将HTML标签过滤掉；

##### 参考手册：

| 函数                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [addcslashes()](https://www.runoob.com/php/func-string-addcslashes.html) | 返回在指定的字符前添加反斜杠的字符串。                       |
| [addslashes()](https://www.runoob.com/php/func-string-addslashes.html) | 返回在预定义的字符前添加反斜杠的字符串。                     |
| [bin2hex()](https://www.runoob.com/php/func-string-bin2hex.html) | 把 ASCII 字符的字符串转换为十六进制值。                      |
| [chop()](https://www.runoob.com/php/func-string-chop.html)   | 移除字符串右侧的空白字符或其他字符。                         |
| [chr()](https://www.runoob.com/php/func-string-chr.html)     | 从指定 ASCII 值返回字符。                                    |
| [chunk_split()](https://www.runoob.com/php/func-string-chunk-split.html) | 把字符串分割为一连串更小的部分。                             |
| [convert_cyr_string()](https://www.runoob.com/php/func-string-convert-cyr-string.html) | 把字符串由一种 Cyrillic 字符集转换成另一种。                 |
| [convert_uudecode()](https://www.runoob.com/php/func-string-convert-uudecode.html) | 对 uuencode 编码的字符串进行解码。                           |
| [convert_uuencode()](https://www.runoob.com/php/func-string-convert-uuencode.html) | 使用 uuencode 算法对字符串进行编码。                         |
| [count_chars()](https://www.runoob.com/php/func-string-count-chars.html) | 返回字符串所用字符的信息。                                   |
| [crc32()](https://www.runoob.com/php/func-string-crc32.html) | 计算一个字符串的 32 位 CRC（循环冗余校验）。                 |
| [crypt()](https://www.runoob.com/php/func-string-crypt.html) | 单向的字符串加密法（hashing）。                              |
| [echo()](https://www.runoob.com/php/func-string-echo.html)   | 输出一个或多个字符串。                                       |
| [explode()](https://www.runoob.com/php/func-string-explode.html) | 把字符串打散为数组。                                         |
| [fprintf()](https://www.runoob.com/php/func-string-fprintf.html) | 把格式化的字符串写入到指定的输出流。                         |
| [get_html_translation_table()](https://www.runoob.com/php/func-string-get-html-translation-table.html) | 返回 htmlspecialchars() 和 htmlentities() 使用的翻译表。     |
| [hebrev()](https://www.runoob.com/php/func-string-hebrev.html) | 把希伯来（Hebrew）文本转换为可见文本。                       |
| [hebrevc()](https://www.runoob.com/php/func-string-hebrevc.html) | 把希伯来（Hebrew）文本转换为可见文本，并把新行（\n）转换为 <br>。 |
| [hex2bin()](https://www.runoob.com/php/func-string-hex2bin.html) | 把十六进制值的字符串转换为 ASCII 字符。                      |
| [html_entity_decode()](https://www.runoob.com/php/func-string-html-entity-decode.html) | 把 HTML 实体转换为字符。                                     |
| [htmlentities()](https://www.runoob.com/php/func-string-htmlentities.html) | 把字符转换为 HTML 实体。                                     |
| [htmlspecialchars_decode()](https://www.runoob.com/php/func-string-htmlspecialchars-decode.html) | 把一些预定义的 HTML 实体转换为字符。                         |
| [htmlspecialchars()](https://www.runoob.com/php/func-string-htmlspecialchars.html) | 把一些预定义的字符转换为 HTML 实体。                         |
| [implode()](https://www.runoob.com/php/func-string-implode.html) | 返回一个由数组元素组合成的字符串。                           |
| [join()](https://www.runoob.com/php/func-string-join.html)   | implode() 的别名。                                           |
| [lcfirst()](https://www.runoob.com/php/func-string-lcfirst.html) | 把字符串中的首字符转换为小写。                               |
| [levenshtein()](https://www.runoob.com/php/func-string-levenshtein.html) | 返回两个字符串之间的 Levenshtein 距离。                      |
| [localeconv()](https://www.runoob.com/php/func-string-localeconv.html) | 返回本地数字及货币格式信息。                                 |
| [ltrim()](https://www.runoob.com/php/func-string-ltrim.html) | 移除字符串左侧的空白字符或其他字符。                         |
| [md5()](https://www.runoob.com/php/func-string-md5.html)     | 计算字符串的 MD5 散列。                                      |
| [md5_file()](https://www.runoob.com/php/func-string-md5-file.html) | 计算文件的 MD5 散列。                                        |
| [metaphone()](https://www.runoob.com/php/func-string-metaphone.html) | 计算字符串的 metaphone 键。                                  |
| [money_format()](https://www.runoob.com/php/func-string-money-format.html) | 返回格式化为货币字符串的字符串。                             |
| [nl_langinfo()](https://www.runoob.com/php/func-string-nl-langinfo.html) | 返回指定的本地信息。                                         |
| [nl2br()](https://www.runoob.com/php/func-string-nl2br.html) | 在字符串中的每个新行之前插入 HTML 换行符。                   |
| [number_format()](https://www.runoob.com/php/func-string-number-format.html) | 通过千位分组来格式化数字。                                   |
| [ord()](https://www.runoob.com/php/func-string-ord.html)     | 返回字符串中第一个字符的 ASCII 值。                          |
| [parse_str()](https://www.runoob.com/php/func-string-parse-str.html) | 把查询字符串解析到变量中。                                   |
| [print()](https://www.runoob.com/php/func-string-print.html) | 输出一个或多个字符串。                                       |
| [printf()](https://www.runoob.com/php/func-string-printf.html) | 输出格式化的字符串。                                         |
| [quoted_printable_decode()](https://www.runoob.com/php/func-string-quoted-printable-decode.html) | 把 quoted-printable 字符串转换为 8 位字符串。                |
| [quoted_printable_encode()](https://www.runoob.com/php/func-string-quoted-printable-encode.html) | 把 8 位字符串转换为 quoted-printable 字符串。                |
| [quotemeta()](https://www.runoob.com/php/func-string-quotemeta.html) | 引用元字符。                                                 |
| [rtrim()](https://www.runoob.com/php/func-string-rtrim.html) | 移除字符串右侧的空白字符或其他字符。                         |
| [setlocale()](https://www.runoob.com/php/func-string-setlocale.html) | 设置地区信息（地域信息）。                                   |
| [sha1()](https://www.runoob.com/php/func-string-sha1.html)   | 计算字符串的 SHA-1 散列。                                    |
| [sha1_file()](https://www.runoob.com/php/func-string-sha1-file.html) | 计算文件的 SHA-1 散列。                                      |
| [similar_text()](https://www.runoob.com/php/func-string-similar-text.html) | 计算两个字符串的相似度。                                     |
| [soundex()](https://www.runoob.com/php/func-string-soundex.html) | 计算字符串的 soundex 键。                                    |
| [sprintf()](https://www.runoob.com/php/func-string-sprintf.html) | 把格式化的字符串写入一个变量中。                             |
| [sscanf()](https://www.runoob.com/php/func-string-sscanf.html) | 根据指定的格式解析来自一个字符串的输入。                     |
| [str_getcsv()](https://www.runoob.com/php/func-string-str-getcsv.html) | 把 CSV 字符串解析到数组中。                                  |
| [str_ireplace()](https://www.runoob.com/php/func-string-str-ireplace.html) | 替换字符串中的一些字符（大小写不敏感）。                     |
| [str_pad()](https://www.runoob.com/php/func-string-str-pad.html) | 把字符串填充为新的长度。                                     |
| [str_repeat()](https://www.runoob.com/php/func-string-str-repeat.html) | 把字符串重复指定的次数。                                     |
| [str_replace()](https://www.runoob.com/php/func-string-str-replace.html) | 替换字符串中的一些字符（大小写敏感）。                       |
| [str_rot13()](https://www.runoob.com/php/func-string-str-rot13.html) | 对字符串执行 ROT13 编码。                                    |
| [str_shuffle()](https://www.runoob.com/php/func-string-str-shuffle.html) | 随机地打乱字符串中的所有字符。                               |
| [str_split()](https://www.runoob.com/php/func-string-str-split.html) | 把字符串分割到数组中。                                       |
| [str_word_count()](https://www.runoob.com/php/func-string-str-word-count.html) | 计算字符串中的单词数。                                       |
| [strcasecmp()](https://www.runoob.com/php/func-string-strcasecmp.html) | 比较两个字符串（大小写不敏感）。                             |
| [strchr()](https://www.runoob.com/php/func-string-strchr.html) | 查找字符串在另一字符串中的第一次出现。（strstr() 的别名。）  |
| [strcmp()](https://www.runoob.com/php/func-string-strcmp.html) | 比较两个字符串（大小写敏感）。                               |
| [strcoll()](https://www.runoob.com/php/func-string-strcoll.html) | 比较两个字符串（根据本地设置）。                             |
| [strcspn()](https://www.runoob.com/php/func-string-strcspn.html) | 返回在找到任何指定的字符之前，在字符串查找的字符数。         |
| [strip_tags()](https://www.runoob.com/php/func-string-strip-tags.html) | 剥去字符串中的 HTML 和 PHP 标签。                            |
| [stripcslashes()](https://www.runoob.com/php/func-string-stripcslashes.html) | 删除由 addcslashes() 函数添加的反斜杠。                      |
| [stripslashes()](https://www.runoob.com/php/func-string-stripslashes.html) | 删除由 addslashes() 函数添加的反斜杠。                       |
| [stripos()](https://www.runoob.com/php/func-string-stripos.html) | 返回字符串在另一字符串中第一次出现的位置（大小写不敏感）。   |
| [stristr()](https://www.runoob.com/php/func-string-stristr.html) | 查找字符串在另一字符串中第一次出现的位置（大小写不敏感）。   |
| [strlen()](https://www.runoob.com/php/func-string-strlen.html) | 返回字符串的长度。中文字符串的处理使用 [mb_strlen() 函数](https://www.runoob.com/php/func-string-mb_strlen.html)。 |
| [strnatcasecmp()](https://www.runoob.com/php/func-string-strnatcasecmp.html) | 使用一种"自然排序"算法来比较两个字符串（大小写不敏感）。     |
| [strnatcmp()](https://www.runoob.com/php/func-string-strnatcmp.html) | 使用一种"自然排序"算法来比较两个字符串（大小写敏感）。       |
| [strncasecmp()](https://www.runoob.com/php/func-string-strncasecmp.html) | 前 n 个字符的字符串比较（大小写不敏感）。                    |
| [strncmp()](https://www.runoob.com/php/func-string-strncmp.html) | 前 n 个字符的字符串比较（大小写敏感）。                      |
| [strpbrk()](https://www.runoob.com/php/func-string-strpbrk.html) | 在字符串中搜索指定字符中的任意一个。                         |
| [strpos()](https://www.runoob.com/php/func-string-strpos.html) | 返回字符串在另一字符串中第一次出现的位置（大小写敏感）。     |
| [strrchr()](https://www.runoob.com/php/func-string-strrchr.html) | 查找字符串在另一个字符串中最后一次出现。                     |
| [strrev()](https://www.runoob.com/php/func-string-strrev.html) | 反转字符串。                                                 |
| [strripos()](https://www.runoob.com/php/func-string-strripos.html) | 查找字符串在另一字符串中最后一次出现的位置(大小写不敏感)。   |
| [strrpos()](https://www.runoob.com/php/func-string-strrpos.html) | 查找字符串在另一字符串中最后一次出现的位置(大小写敏感)。     |
| [strspn()](https://www.runoob.com/php/func-string-strspn.html) | 返回在字符串中包含的特定字符的数目。                         |
| [strstr()](https://www.runoob.com/php/func-string-strstr.html) | 查找字符串在另一字符串中的第一次出现（大小写敏感）。         |
| [strtok()](https://www.runoob.com/php/func-string-strtok.html) | 把字符串分割为更小的字符串。                                 |
| [strtolower()](https://www.runoob.com/php/func-string-strtolower.html) | 把字符串转换为小写字母。                                     |
| [strtoupper()](https://www.runoob.com/php/func-string-strtoupper.html) | 把字符串转换为大写字母。                                     |
| [strtr()](https://www.runoob.com/php/func-string-strtr.html) | 转换字符串中特定的字符。                                     |
| [substr()](https://www.runoob.com/php/func-string-substr.html) | 返回字符串的一部分。                                         |
|                                                              |                                                              |
| [mb_substr()](https://www.runoob.com/php/func-string-mb_substr.html) | 返回中文字符串的一部分。                                     |
| [substr_compare()](https://www.runoob.com/php/func-string-substr-compare.html) | 从指定的开始位置（二进制安全和选择性区分大小写）比较两个字符串。 |
| [substr_count()](https://www.runoob.com/php/func-string-substr-count.html) | 计算子串在字符串中出现的次数。                               |
| [substr_replace()](https://www.runoob.com/php/func-string-substr-replace.html) | 把字符串的一部分替换为另一个字符串。                         |
| [trim()](https://www.runoob.com/php/func-string-trim.html)   | 移除字符串两侧的空白字符和其他字符。                         |
| [ucfirst()](https://www.runoob.com/php/func-string-ucfirst.html) | 把字符串中的首字符转换为大写。                               |
| [ucwords()](https://www.runoob.com/php/func-string-ucwords.html) | 把字符串中每个单词的首字符转换为大写。                       |
| [vfprintf()](https://www.runoob.com/php/func-string-vfprintf.html) | 把格式化的字符串写到指定的输出流。                           |
| [vprintf()](https://www.runoob.com/php/func-string-vprintf.html) | 输出格式化的字符串。                                         |
| [vsprintf()](https://www.runoob.com/php/func-string-vsprintf.html) | 把格式化字符串写入变量中。                                   |
| [wordwrap()](https://www.runoob.com/php/func-string-wordwrap.html) | 按照指定长度对字符串进行折行处理。                           |

#### PHP正则表达式：
``` php
// 例如：
$val='15093691582';
if(preg_match('/^1[1-9][0-9]{9}$/',$val)){
	echo"ok";
}else{
	echo"no";
}
```

##### 正则表达式的用途：判断邮箱地址 判断特殊字符 判断格式 判断手机号

##### 正则表达式函数：

preg_grep("正则表达式",string、array) 返回正则表达式匹配的内容、

preg_match("正则表达式",字符串、数组) 返回0 1 如果匹配返回1 不匹配则返回0、

preg_match_all("正则表达式",字符串,一个数组) 将正则表达式匹配的内容返回给数组、

preg_auote() 暂时未找到资源这个好像不是、

应该是preg_quote() 需要参数 str 并向其中 每个正则表达式语法中的字符前增加一个反斜线。 这通常用于你有一些运行时字符串 需要作为正则表达式进行匹配的时候。

preg_replace() 、

preg_replace_callback() 、

preg_split()

##### 参考表：

| 特别字符 | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| $        | 匹配输⼊字符串的结尾位置。如果设置了 RegExp 对象的 Multiline 属性 ，则 $ 也匹配 '\n' 或 '\r'。要匹配 $ 字符本身，请使⽤ \$。 |
| ()       | 标记⼀个⼦表达式的开始和结束位置。⼦表达式可以获取供以后使⽤。 要匹配这些字符，请使⽤ \( 和 \)。 |
| *        | 匹配前⾯的⼦表达式零次或多次。要匹配 * 字符，请使⽤ \*。     |
| +        | 匹配前⾯的⼦表达式⼀次或多次。要匹配 + 字符，请使⽤ \+。     |
| .        | 匹配除换⾏符 \n 之外的任何单字符。要匹配 . ，请使⽤ \. 。    |
| [        | 标记⼀个中括号表达式的开始。要匹配 [，请使⽤ \[。            |
| ?        | 匹配前⾯的⼦表达式零次或⼀次，或指明⼀个⾮贪婪限定符。要匹配 ? 字符，请使⽤ \?。 |
| \        | 将下⼀个字符标记为或特殊字符、或原义字符、或向后引⽤、或⼋进制 转义符。例如， 'n' 匹配字符 'n'。'\n' 匹配换⾏符。序列 '\\' 匹配 ""，⽽ ' \(' 则匹配 "("。 |
| ^        | 匹配输⼊字符串的开始位置，除⾮在⽅括号表达式中使⽤，此时它表示不接受该字符集合。要匹配 ^ 字符本身，请使⽤ ^。 |
| {        | 标记限定符表达式的开始。要匹配 {，请使⽤ \{。                |
| \|       | 指明两项之间的⼀个选择。要匹配 \|，请使⽤ \|。               |

#### PHP磁盘、目录和文件夹操作：

``` php
opendir(path,context)打开目录句柄

$file = __FILE__;

echo "<pre>";
echo "<br/>";
echo basename($file);//文件名称
echo "<br/>";
echo dirname($file);//文件路径
echo "<br/>";

print_r(pathinfo($file));//函数以数组的形式返回关于文件路径的信息。

fopen(filename,mode,include_path,context)  //fopen函数打开一个url或一个文件
// 如果 fopen() 失败，它将返回 FALSE 并附带错误信息。您可以通过在函数名前面添加一个'@' 来隐藏错误输出。
```



##### 参考表：

| 参数         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| filename     | 必需。规定要打开的文件或 URL。                               |
| mode         | 必需。规定您请求到该文件/流的访问类型。可能的值："r" （只读方式打开，将文件指针指向文件头）"r+" （读写方式打开，将文件指针指向文件头）"w" （写入方式打开，清除文件内容，如果文件不存在则尝试创建之）"w+" （读写方式打开，清除文件内容，如果文件不存在则尝试创建之）"a" （写入方式打开，将文件指针指向文件末尾进行写入，如果文件不存在则尝试创建之）"a+" （读写方式打开，通过将文件指针指向文件末尾进行写入来保存文件内容）"x" （创建一个新的文件并以写入方式打开，如果文件已存在则返回 FALSE 和一个错误）"x+" （创建一个新的文件并以读写方式打开，如果文件已存在则返回 FALSE 和一个错误） |
| include_path | 可选。如果您还想在 include_path（在 php.ini 中）中搜索文件的话，请设置该参数为 '1'。 |
| context      | 可选。规定文件句柄的环境。context 是一套可以修改流的行为的选项。 |

#### PHP表单提交or数据库连接：
``` php
// 提交方式or内置数组：
 $_SERVER、 $_GET、 $_POST、 $_REQUEST、 $_SESSION、 $_FILES、 $_COOKIE、 $_ENV、 $_GLOBALS、 $_FILES['file']['error']
```
其值为 0，没有错误发生，文件上传成功。

其值为 1，上传的文件超过了 php.ini 中 upload_max_filesize 选项限制的值。

其值为 2，上传文件的大小超过了 HTML 表单中 MAX_FILE_SIZE 选项指定的值。

其值为 3，文件只有部分被上传。

其值为 4，没有文件被上传。

其值为 6，找不到临时文件夹。PHP 4.3.10 和 PHP 5.0.3 引进。

其值为 7，文件写入失败。PHP 5.1.0 引进。

##### MySQL内置函数 参考手册：

| 函数                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [mysqli_affected_rows()](https://www.runoob.com/php/func-mysqli-affected-rows.html) | 返回前一次 MySQL 操作所影响的记录行数。                      |
| [mysqli_autocommit()](https://www.runoob.com/php/func-mysqli-autocommit.html) | 打开或关闭自动提交数据库修改。                               |
| [mysqli_change_user()](https://www.runoob.com/php/func-mysqli-change-user.html) | 更改指定数据库连接的用户。                                   |
| [mysqli_character_set_name()](https://www.runoob.com/php/func-mysqli-character-set-name.html) | 返回数据库连接的默认字符集。                                 |
| [mysqli_close()](https://www.runoob.com/php/func-mysqli-close.html) | 关闭先前打开的数据库连接。                                   |
| [mysqli_commit()](https://www.runoob.com/php/func-mysqli-commit.html) | 提交当前事务。                                               |
| [mysqli_connect_errno()](https://www.runoob.com/php/func-mysqli-connect-errno.html) | 返回上一次连接错误的错误代码。                               |
| [mysqli_connect_error()](https://www.runoob.com/php/func-mysqli-connect-error.html) | 返回上一次连接错误的错误描述。                               |
| [mysqli_connect()](https://www.runoob.com/php/func-mysqli-connect.html) | 打开一个到 MySQL 服务器的新的连接。                          |
| [mysqli_data_seek()](https://www.runoob.com/php/func-mysqli-data-seek.html) | 调整结果指针到结果集中的一个任意行。                         |
| [mysqli_debug()](https://www.runoob.com/php/func-mysqli-debug.html) | 执行调试操作。                                               |
| [mysqli_dump_debug_info()](https://www.runoob.com/php/func-mysqli-dump-debug-info.html) | 转储调试信息到日志中。                                       |
| [mysqli_errno()](https://www.runoob.com/php/func-mysqli-errno.html) | 返回最近调用函数的最后一个错误代码。                         |
| [mysqli_error_list()](https://www.runoob.com/php/func-mysqli-error-list.html) | 返回最近调用函数的错误列表。                                 |
| [mysqli_error()](https://www.runoob.com/php/func-mysqli-error.html) | 返回最近调用函数的最后一个错误描述。                         |
| [mysqli_fetch_all()](https://www.runoob.com/php/func-mysqli-fetch-all.html) | 从结果集中取得所有行作为关联数组，或数字数组，或二者兼有。   |
| [mysqli_fetch_array()](https://www.runoob.com/php/func-mysqli-fetch-array.html) | 从结果集中取得一行作为关联数组，或数字数组，或二者兼有。     |
| [mysqli_fetch_assoc()](https://www.runoob.com/php/func-mysqli-fetch-assoc.html) | 从结果集中取得一行作为关联数组。                             |
| [mysqli_fetch_field_direct()](https://www.runoob.com/php/func-mysqli-fetch-field-direct.html) | 从结果集中取得某个单一字段的 meta-data，并作为对象返回。     |
| [mysqli_fetch_field()](https://www.runoob.com/php/func-mysqli-fetch-field.html) | 从结果集中取得下一字段，并作为对象返回。                     |
| [mysqli_fetch_fields()](https://www.runoob.com/php/func-mysqli-fetch-fields.html) | 返回结果中代表字段的对象的数组。                             |
| [mysqli_fetch_lengths()](https://www.runoob.com/php/func-mysqli-fetch-lengths.html) | 返回结果集中当前行的每个列的长度。                           |
| [mysqli_fetch_object()](https://www.runoob.com/php/func-mysqli-fetch-object.html) | 从结果集中取得当前行，并作为对象返回。                       |
| [mysqli_fetch_row()](https://www.runoob.com/php/func-mysqli-fetch-row.html) | 从结果集中取得一行，并作为枚举数组返回。                     |
| [mysqli_field_count()](https://www.runoob.com/php/func-mysqli-field-count.html) | 返回最近查询的列数。                                         |
| [mysqli_field_seek()](https://www.runoob.com/php/func-mysqli-field-seek.html) | 把结果集中的指针设置为指定字段的偏移量。                     |
| [mysqli_field_tell()](https://www.runoob.com/php/func-mysqli-field-tell.html) | 返回结果集中的指针的位置。                                   |
| [mysqli_free_result()](https://www.runoob.com/php/func-mysqli-free-result.html) | 释放结果内存。                                               |
| [mysqli_get_charset()](https://www.runoob.com/php/func-mysqli-get-charset.html) | 返回字符集对象。                                             |
| [mysqli_get_client_info()](https://www.runoob.com/php/func-mysqli-get-client-info.html) | 返回 MySQL 客户端库版本。                                    |
| [mysqli_get_client_stats()](https://www.runoob.com/php/func-mysqli-get-client-stats.html) | 返回有关客户端每个进程的统计。                               |
| [mysqli_get_client_version()](https://www.runoob.com/php/func-mysqli-get-client-version.html) | 将 MySQL 客户端库版本作为整数返回。                          |
| [mysqli_get_connection_stats()](https://www.runoob.com/php/func-mysqli-get-connection-stats.html) | 返回有关客户端连接的统计。                                   |
| [mysqli_get_host_info()](https://www.runoob.com/php/func-mysqli-get-host-info.html) | 返回 MySQL 服务器主机名和连接类型。                          |
| [mysqli_get_proto_info()](https://www.runoob.com/php/func-mysqli-get-proto-info.html) | 返回 MySQL 协议版本。                                        |
| [mysqli_get_server_info()](https://www.runoob.com/php/func-mysqli-get-server-info.html) | 返回 MySQL 服务器版本。                                      |
| [mysqli_get_server_version()](https://www.runoob.com/php/func-mysqli-get-server-version.html) | 将 MySQL 服务器版本作为整数返回。                            |
| [mysqli_info()](https://www.runoob.com/php/func-mysqli-info.html) | 返回有关最近执行查询的信息。                                 |
| [mysqli_init()](https://www.runoob.com/php/func-mysqli-init.html) | 初始化 MySQLi 并返回 mysqli_real_connect() 使用的资源。      |
| [mysqli_insert_id()](https://www.runoob.com/php/func-mysqli-insert-id.html) | 返回最后一个查询中自动生成的 ID。                            |
| [mysql_kill()](https://www.runoob.com/php/func-mysqli-kill.html) | 请求服务器杀死一个 MySQL 线程。                              |
| [mysqli_more_results()](https://www.runoob.com/php/func-mysqli-more-results.html) | 检查一个多查询是否有更多的结果。                             |
| [mysqli_multi_query()](https://www.runoob.com/php/func-mysqli-multi-query.html) | 执行一个或多个针对数据库的查询。                             |
| [mysqli_next_result()](https://www.runoob.com/php/func-mysqli-next-result.html) | 为 mysqli_multi_query() 准备下一个结果集。                   |
| [mysqli_num_fields()](https://www.runoob.com/php/func-mysqli-num-fields.html) | 返回结果集中字段的数量。                                     |
| [mysqli_num_rows()](https://www.runoob.com/php/func-mysqli-num-rows.html) | 返回结果集中行的数量。                                       |
| [mysqli_options()](https://www.runoob.com/php/func-mysqli-options.html) | 设置额外的连接选项，用于影响连接行为。                       |
| [mysqli_ping()](https://www.runoob.com/php/func-mysqli-ping.html) | 进行一个服务器连接，如果连接已断开则尝试重新连接。           |
| mysqli_prepare()                                             | 准备执行一个 SQL 语句。                                      |
| [mysqli_query()](https://www.runoob.com/php/func-mysqli-query.html) | 执行某个针对数据库的查询。                                   |
| [mysqli_real_connect()](https://www.runoob.com/php/func-mysqli-real-connect.html) | 打开一个到 MySQL 服务器的新的链接。                          |
| [mysqli_real_escape_string()](https://www.runoob.com/php/func-mysqli-real-escape-string.html) | 转义在 SQL 语句中使用的字符串中的特殊字符。                  |
| mysqli_real_query()                                          | 执行 SQL 查询                                                |
| mysqli_reap_async_query()                                    | 返回异步查询的结果。                                         |
| [mysqli_refresh()](https://www.runoob.com/php/func-mysqli-refresh.html) | 刷新表或缓存，或者重置复制服务器信息。                       |
| [mysqli_rollback()](https://www.runoob.com/php/func-mysqli-rollback.html) | 回滚数据库中的当前事务。                                     |
| [mysqli_select_db()](https://www.runoob.com/php/func-mysqli-select-db.html) | 更改连接的默认数据库。                                       |
| [mysqli_set_charset()](https://www.runoob.com/php/func-mysqli-set-charset.html) | 设置默认客户端字符集。                                       |
| mysqli_set_local_infile_default()                            | 撤销用于 load local infile 命令的用户自定义句柄。            |
| mysqli_set_local_infile_handler()                            | 设置用于 LOAD DATA LOCAL INFILE 命令的回滚函数。             |
| [mysqli_sqlstate()](https://www.runoob.com/php/func-mysqli-sqlstate.html) | 返回最后一个 MySQL 操作的 SQLSTATE 错误代码。                |
| [mysqli_ssl_set()](https://www.runoob.com/php/func-mysqli-ssl-set.html) | 用于创建 SSL 安全连接。                                      |
| [mysqli_stat()](https://www.runoob.com/php/func-mysqli-stat.html) | 返回当前系统状态。                                           |
| [mysqli_stmt_init()](https://www.runoob.com/php/func-mysqli-stmt-init.html) | 初始化声明并返回 mysqli_stmt_prepare() 使用的对象。          |
| mysqli_store_result()                                        | 传输最后一个查询的结果集。                                   |
| [mysqli_thread_id()](https://www.runoob.com/php/func-mysqli-thread-id.html) | 返回当前连接的线程 ID。                                      |
| [mysqli_thread_safe()](https://www.runoob.com/php/func-mysqli-thread-safe.html) | 返回是否将客户端库编译成 thread-safe。                       |
| mysqli_use_result()                                          | 从上次使用 mysqli_real_query() 执行的查询中初始化结果集的检索。 |
| mysqli_warning_count()                                       | 返回连接中的最后一个查询的警告数量。                         |

#### PHP图像处理：

创建图像的㇐般流程:

1. 设定标头，告诉浏览器你要生成的 MIME 类型。

2. 创建㇐个图像区域，以后的操作都将基于此图像区域。

3. 在空白图像区域绘制填充背景。

4. 在背景上绘制图形轮廓输入文本。

5. 输出最终图形。

6. 清除所有资源。

### 设定标头指定 MIME 输出类型
``` php
header('Content-Type: image/png');

//创建㇐个空白的图像区域
$im = imagecreatetruecolor( 200 , 200 );

//在空白图像区域绘制填充背景
$blue = imagecolorallocate($im, 0 , 102 , 255 );
imagefill($im, 0 , 0 ,$blue);

//在背景上绘制图形轮廓输入文本
$white = imagecolorallocate($im, 255 , 255 , 255 );
imageline($im, 0 , 0 , 200 , 200 ,$white);
imageline($im, 200 , 0 , 0 , 200 ,$white) ;
imagestring($im,  5 ,  80 ,  20 , "12345", $white);

//输出最终图形
imagepng($im);

//清除所有资源
imagedestroy($im);

//其他⻚面调用创建的图形
<img src="Demo4.php" alt="PHP 创建的图片" />

```

## PHP  session 与 cookie

setcookie(name, value, expire, path, domain);

echo $_COOKIE['name'];

#### Cookie和Session的区别：

session是存储服务器端，cookie是存储在客户端，所以session的安全性比cookie高。

#### PHP与Ajax
``` js

//创建请求对象。XMLHttpRequest对象拥有发起请求的能力
var http = new XMLHttpRequest();

// 设置相应事件或者状态改变监听事件,事件的注册
http.onreadystatechange = stateChange;

// 设置请求的方式和地址
http.open("GET", "/admin/cities.php?pid="+obj.value, true);

//发起请求
http.send();

//监听之后的动作
function stateChange(){
    //如果监听的事件发生了则触发该函数
    http.readyState == 4
    http.status == 200 //HTTP协议中的状态码
    http.statusText == 'OK'//HTTP协议中的状态码的描述
    http.responseText //就是相应的数据内容
}

```
##### PHP中：json_encode ( );将数组转换城 json 数据格式；

##### JavaScript中：JSON.parse ( );将字符串转换成 json 数据格式；

##### //JSON数据结构

{"名1":"值1","名2","值2"}

{"name":"xikun",'age':19,'isboy':true} 表示㇐个单独的对象

[{"name":"xikun",'age':19},{"name":"xikun",'age':19}] 表示json数

#### PHP面向对象

##### php面向对象老师整理的笔记本地地址：[F:\WeChat_temp\WeChat Files\wxid_oldeueiusn0612\FileStorage\File\2021-01](F:\WeChat_temp\WeChat Files\wxid_oldeueiusn0612\FileStorage\File\2021-01)

| 可见性   | private | protected | public |
| -------- | ------- | --------- | ------ |
| 类内部   | 可以    | 可以      | 可以   |
| 子类内部 |         | 可以      | 可以   |
| 类外部   |         |           | 可以   |

``` php

fainl function eat ( ) {
	 // 我不能被子类继承；
}

$_GLOBALS[' ']; 全局变量；

// 举个例子：
// 设置一个父级类
class father
{
    protected $name;
    protected $model;
    protected $color;
    protected $brand;

  public function __construct($model='',$color='',$brand='')
  {
        echo "型号：".$this->model=$model;
        echo "颜色：".$this->color=$color;
        echo "品牌：".$this->brand=$brand;
  }
   public function setName($name){
	    $this->name=$name;
   }
   public function getName(){
	    return $this->name;
   }
}

设置一个类 继承了 父级 father
include "father.php";
class Car extends father
{
    public function __construct($model,$color,$brand){
	    parent::__construct($model,$color,$brand);
    }
    public function action($action){
	    echo "正在：".$this->action=$action;
    }

}
```


## PHP写接口：

```php
//写法：一个PHP文件，写上请求头，从数据库查出数据并返回；
//写上请求头，解决跨域问题；
//也可以写 token；
header("Access‐Control‐Allow‐Origin: *"); //解决跨域问题；
header("Access‐Control‐Allow‐Methods:POST,GET"); //请求方式；
header("Access‐Control‐Allow‐Headers:x‐requested‐with,content‐type"); //
//响应首部
//Headers的三种类型："application/x‐www‐form‐urlencoded"、"multipart/form‐data" 或 "text/plain"
header("Content‐type:text/json;charset=utf‐8"); //请求头 数据格式
```
#### ThinkPHP：

###### Tp文档：http://www.thinkphp.cn/

##### TP使用数据库：

```php
//先使用 数据库类库
use think\facade\Db;

$data = Db::name('table')‐>select(); //查询table表中的值 name也可以写成talbe 也可以加where条件
Db::name('table')‐>insert(['id'=> 1 ,'name'=>'hello']); //添加一条数据 添加成功 返回true 1 添加失败 返回false 0
Db::name('table')‐>delete( 1 ); //根据主键删除 也可以加where条件 添加成功 返回true 1 添加失败 返回false 0
Db::name('table')‐>update(['id'=> 1 ,'name'=>'world']); //修改数据 也可以加where条件

// 设置 Sesion 以及使用
use think\facade\Session; //引用 Session 类
// 设置 session
Session::set('name',value);
// 获取 session
Session::get('name');
// 判断 session 是否存在
Session::has('name');
// 删除 session
Session::delete('name');
//取值 session 并删除
Session::pull('name');
// 获取全部 session
Session::all();
// 清空所有 session
Session::clear();
// 设置session 并且在下一次请求之前有效
Session::flash('name','value');

// 设置 Cookie 以及使用
use think\facade\Cookie; //引用 Cookie 类
// 设置 Cookie
Cookie::set('name','value', 3600 ); //第三个参数是 时间（秒）如果不填默认 3600
// 获取 删除 和 Session 一样
//获取全部 Cookie
Cookie::get();
//永久保存 Cookie
Cookie::forever('name','value');
```



##### TP   Session 配置参数：

| 参数           | 描述                                    |
| -------------- | --------------------------------------- |
| type           | session类型（File或者Cache）            |
| store          | 当type设置为cache类型的时候指定存储标识 |
| expire         | session过期时间（秒）必须大于0          |
| var_session_id | 请求session_id变量名                    |
| name           | session_name                            |
| prefix         | session前缀                             |
| serialize      | 序列化方法                              |