


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #最简单的函数。
    def myfunc():
        print("myfunc() called.")
    myfunc()
    print('='*30)
    #使用装饰函数，在函数执行前和执行后分别附加额外功能。
    def deco(func):
        print("before myfunc() called.")
        func()
        print("after myfunc() called.")
        return func
    def myfunc():
        print("myfunc() called.")
    myfunc = deco(myfunc)
    print('='*30)
    #使用语法糖@来装饰函数.
    def deco(func):
        print("before myfunc() called.")
        func()
        print("after myfunc() called.")
        return func
    @deco
    def myfunc():
        print("myfunc() called.")
    print('='*30)
    #使用内嵌包装函数来确保每次新函数都被调用.
    def deco(func):
        def _deco():
            print("before myfunc() called.")
            t = func()
            print(t)
            print("after myfunc() called.")
            return 'ok1'
    
        return _deco
    @deco
    def myfunc():
        print("myfunc() called.")
        return 'good'
    t = myfunc()
    print(t)
    print('='*30)
    #对带参数的函数进行装饰。
    #内嵌包装函数的形参和返回值与原函数相同，装饰函数返回内嵌包装函数对象。
    def deco(func):
        def _deco(a, b):
            print("before myfunc() called.")
            ret = func(a, b)
            print("after myfunc() called. result: %s" % ret)
            return ret
        return _deco
    @deco
    def myfunc(a, b):
        print("myfunc(%s,%s) called." % (a, b))
        return a + b
    myfunc(1, 2)
    myfunc(3, 4)
    print('='*30)
    #对参数数量不确定的函数进行装饰。
    def deco(func):
        def _deco(*args, **kwargs):
            print("before %s called." % func.__name__)
            ret = func(*args, **kwargs)
            print("after %s called. result: %s" % (func.__name__, ret))
            return ret
        return _deco
    @deco
    def myfunc1(a, b):
        print("myfunc1(%s,%s) called." % (a, b))
        return a + b
    @deco
    def myfunc2(a, b, c):
        print("myfunc2(%s,%s,%s) called." % (a, b, c))
        return a + b + c
    myfunc1(1, 2)
    myfunc1(3, 4)
    myfunc2(1, 2, 3)
    myfunc2(4, 5, 6)
    print('='*30)
    #让装饰器带参数。
    def deco(arg):
        def _deco(func):
            def __deco():
                print("before %s called [%s]." % (func.__name__, arg))
                func()
                print("after %s called [%s]." % (func.__name__, arg))
            return __deco
        return _deco
    @deco("decorator1")
    def myfunc1():
        print("myfunc1() called.")
    @deco("decorator2")
    def myfunc2():
        print("myfunc2() called.")
    myfunc1()
    myfunc2()
    print('='*30)
    #装饰器带类参数。
    class locker:
        def __init__(self):
            print("locker.__init__() should be not called.")
        @staticmethod
        def acquire():
            print("locker.acquire() called.（这是静态方法）")
        @staticmethod
        def release():
            print("locker.release() called.（不需要对象实例）")
    def deco(cls):
        def _deco(func):
            def __deco():
                print("before %s called [%s]." % (func.__name__, cls))
                cls.acquire()
                try:
                    return func()
                finally:
                    cls.release()
            return __deco
        return _deco
    
    @deco(locker)
    def myfunc():
        print("myfunc() called.")
    myfunc()