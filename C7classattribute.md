


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #为了统计学生人数，可以给Student类增加一个类属性，每创建一个实例，该属性自动增加。
    class Getcount(object):
        count = 0
    class Student(Getcount):
        def __init__(self, name):
            Getcount.count = Getcount.count + 1
            self.name = name
    instance1 = Student('wanjun')
    instance2 = Student('wanjun')
    print(Student.count)