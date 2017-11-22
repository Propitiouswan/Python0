


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #请把下面的Student对象的gender字段对外隐藏起来，用get_gender()和set_gender()代替，并检查参数有效性。
    class Student(object):
        def __init__(self, name, gender):
            self.name = name
            self.__gender = gender
        def get_gender(self):
            return self.__gender
        def set_gender(self, gender):
            self.__gender = gender
    instance1 = Student('wanjun', 'F')
    instance2 = Student('zhouwenhui', 'M')
    if instance2.get_gender() != 'M':
        print('测试失败!')
    else:
        instance2.set_gender('F')
        if instance2.get_gender() != 'F':
            print('测试失败!')
        else:
            print('测试成功!')