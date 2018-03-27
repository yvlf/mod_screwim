PHP螺丝的改进（screwim）扩展

= =

【！【GitHub许可]（https：／／IMG。盾牌。IO /徽章/许可RSD 202条蓝色，SVG）]（https://raw.githubusercontent.com/oops-org-php/mod_screwim/master/license）

【！【GitHub上发布]（https：／／IMG。盾牌。IO / GitHub /释放/ oops-org-php / mod_screwim。SVG）]（https://github.com/oops-org-php/mod_screwim/releases）

【！[问题]（https：GitHub关闭/ IMG。盾牌。IO / GitHub /问题封闭原/ oops-org-php / mod_screwim。SVG）]（https://github.com/oops-org-php/mod_screwim/issues？Q =为3aissue + % 3aclosed）

【！[拉]（HTTPS请求Github封闭：/ / IMG。盾牌。IO / GitHub /问题/ oops-org-php /公关关原mod_screwim。SVG）]（https://github.com/oops-org-php/mod_screwim/pulls？Q =为3apr + % 3aclosed）



# #摘要



* PHP螺杆改进（screwim）***是一个PHP脚本加密工具。当您使用PHP开发一个商业包时，脚本可以以加密方式分发直到执行前。这保留了你的知识产权。



这个扩展是基于PHP螺杆] [（http://www.pm9.com/newpm9/itbiz/php/phpscrew/）谁由【*** Kunimasa田*** ]（地址：kuni@pm9.com）在[公司]（pm9.com，http://www.pm9.com）



与原始PHP螺钉的差异如下：

1。通过在内存中处理而不是在解码期间创建临时文件来提高性能。

1。应用[ Sungwook Shin改进补丁]（https://github.com/edp1096）

2。通过固定重复打开文件的性能改进（问题# 4）

三.固定内存泄漏。

2。在编码或解码大文件时通过改变内存重新分配逻辑来提高性能。

三.只有当“启用”选项是screwim。

*在正常环境下不检查魔法键（常规PHP脚本）提高性能。

*参见[ # 3添加screwim.enable INI选项问题]（https://github.com/oops-org-php/mod_screwim/issues/3）

4。固定内存泄漏。

5。删除全局变量。也许线程安全。

6。预防，可以反编译[ php_unscrew ]问题（https://github.com/dehydr8/php_unscrew）

7。支持运行时加密功能` ` ` screwim_encrypt() ` ` `

8。支持运行时解密功能` ` ` screwim_decrypt()，screwim_seed() ` ` `

9。凡此种种，不一而足。



# #描述



* * * * * *是screwim加密PHP脚本的加密工具。



而且，在一个PHP脚本的执行时间，解密screwim.so是PHP扩展执行，就在PHP脚本交给Zend编译器。



事实上你要做的是只是添加描述php.screw到php.ini。PHP脚本程序员不需要意识到解密过程。而且你将加密脚本文件和未加密的一个可能。



在加密工具加密逻辑（screwim）和解密的解密逻辑（screwim。所以），可以轻松地定制。



包含的普通目的代码和解密逻辑可以通过改变加密种子密钥来定制。虽然很容易cusomize加密，通过加密种子，这并不意味着，这个PHP脚本可以解密，容易被别人。



# #许可



版权所有（C）2016 joungkyun。基姆



[ ]（许可证）了2-clause BSD



需求量



*** PHP 5 ***和之后（也支持*** PHP 7 ***）

* PHP *** zlib ***延伸。

检查PHP zlib编译它与PHP脚本：

“PHP”

<？PHP gzopen()；？>

` ` `

*类UNIX操作系统。



# #安装



# # # 1。自定义加密/解密

* ~ ~更改加密种子密钥（*** screwim_mcryptkey ***）在*** my_screw。h ***的值根据你所喜欢的。~ ~

如果你在加密种子数组中添加更多的值，加密将更加困难。

但是，种子的大小与解密处理的时间无关。

*加密种子密钥现在自动从5到8个数组在配置时生成。不要使用*** my_screw h ***更多。（成就了你这与*** screwim_enc_data ***恒在config. h）

*（***可选***）加密脚本获得一个添加到文件开头的图章。如果你喜欢，你可以改变这枚邮票由*** screwim ***和*** screwim_len *** *** *** php_screwim。H。* * * * * * screwim_len必须小于或等于大小screwim *** ***。



# # # 2。建造和安装

```bash

[主持人] phpize美元mod_screwim根@

[主持人]根@ mod_screwim美元。/配置

[主持人]根@ mod_screwim美元安装

` ` `

在配置、***，使screwim解密***选择加解密功能（*** screwim_decrypt()，screwim_seed() ***）。这意味着***可以对加密的php文件进行解密。



如果你正在建设***分配***，从不添加，使screwim解密选项！




# # # 3。配置

添加一行（PHP配置文件php.ini等等）



“ini”

screwim.so延伸=

screwim.enable = 1

` ` `



默认情况下，解密不起作用，因此常规PHP文件的性能比原始PHP螺钉要好。的screwim.enable选项必须打开解密工作。又见https://github.com/oops-org—
