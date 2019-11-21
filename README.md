# python_object-oriented

物件（object）或者實體（matters）：在 Python 中，物件是資料與程式碼的組合，可以是指整個應用程式或者是應用程式中的一小部分。以生活中的物品為例，我們可以說電腦是一個物件，而組成電腦的 CPU、硬碟等也都可以做為一個物件。

### Python3.4

class Cat: #{1}
    def __init__(self,name): #{2}
        self.__name = name #{3}

    def shout(self): #{4}
        return "My name is "+self.__name+". meow~" #{5}

def main():
    cat = Cat("May") #{6}
    print(cat.shout()) #{7}

if __name__=="__main__": #{8}
    main()

# output:
# My name is May. meow~
