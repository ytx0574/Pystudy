# Py_Study


global 标记全局变量, 可在函数内部修改值.  不同其他语言, global声明必须是已经声明过的变量.(在你需要修改值得地方进行声明)

exec 直接把字符串当做pyton的代码执行

with-as 快速处理异常, 类似try: finally:的操作  with所求值得对象必须有__enter__()和__exit(self, type, value, trace)__函数.  用法上面有点类似swift中的 if let 声明


is 与==同理

lambda 匿名函数. 类似代码块  如 get_sum = lambda x, y, z: x + y + z

pass 空语句, 用于保持程序的完整性, 占位


try: except ExceptionType, ExceptionType: else:
try: except ExceptionType, Argument: else:
try: finally:

with 变量的别名
yield  一个带有yield的函数就是一个generator.  调用的时候看起像个函数调用, 其实是生成一个generator对象, 而普通的函数调用则是返回它的返回值.
当对其使用for循环的时候, 其实内部调用为next(). 当执行到yield时, 就会被中断, 返回迭代值. yield可以让一个函数拥有迭代器的能力, 因为自动保留上一次的值, 所以资源上消耗不大

from  inspect import  isgeneratorfunction
isgeneratorfunction(fab) 通过该函数判断是否为generator

import types
isinstance(fab, Iterable) 判断是否为类的实例

@staticmethod @classmethod instance method.  如果有名称一样的同样的函数, 优先级依次为static class instance. intance默认第一个参数为self, class默认第一个参数为cls. 外部定义的函数为mudule_method.
