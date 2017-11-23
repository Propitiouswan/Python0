


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #Python内置的@property装饰器负责把一个方法变成属性调用。
    #请利用@property给一个Screen对象加上width和height属性，以及一个只读属性resolution。
    class Screen(object):
        @property
        def width(self):
            return self._width
        @width.setter
        def width(self, value):
            if not isinstance(value, int):
                raise ValueError('应输入整数。')
            elif value < 0 or value > 10000:
                raise ValueError('应输入0~10000之间的数。')
            else:
                self._width = value
        @property
        def height(self):
            return self._height
    
        @height.setter
        def height(self, value):
            if not isinstance(value, int):
                raise ValueError('应输入整数。')
            elif value < 0 or value > 10000:
                raise ValueError('应输入0~10000之间的数。')
            else:
                self._height = value
        @property
        def resolution(self):
            return self._width*self._height
    s = Screen()
    s.width = 1024
    s.height = 768
    print('resolution =', s.resolution)
    if s.resolution == 786432:
        print('测试通过!')