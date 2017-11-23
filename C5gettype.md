    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #使用type()
    print(type(123))
    print(type('abc'))
    print(type(None))
    print(abs)
    import types
    def fn():
        pass
    if type(fn) == types.FunctionType:
        print('True1')
    if type(abs) == types.BuiltinFunctionType:
        print('True2')
    if type(lambda x: x) == types.LambdaType:
        print('True3')
    if type((x for x in range(10))) == types.GeneratorType:
        print('True4')
    #使用isinstance()
    print(isinstance('a', str))
    print(isinstance(123, str))
    a1 = isinstance([1, 2, 3], (list, tuple))
    print(a1)
    #使用dir()获得所有属性和方法
    print(dir('ABC'))
    a2 = 'ABC'.__len__()
    print(a2)

