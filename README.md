代码在fork https://github.com/NightNord/ljd 的基础上修改的

主要修正了原版本没有将_read_header函数解析过的header中的flag值带进_read_protoypes。

解决了原代码只能解析带调试信息的luajit字节码，而解析不带调试信息字节码时报错的问题。

此版本可解析luajit2.1.0-beta2的字节码文件。如果要解析其它版本的luajit字节码文件，需要将

luajit源码中的opcode，写进instruction.py 和 code.py


使用说明：python main.py  "path of luajit-bytecode"

解释文档：http://www.freebuf.com/column/177810.html

参考：https://github.com/NightNord/ljd
      https://github.com/feicong/lua_re/blob/master/lua/lua_re3.md
	  https://bbs.pediy.com/thread-216800.htm