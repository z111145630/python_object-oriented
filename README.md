# python_object-oriented

### 物件（object）或者實體（matters）：

在 Python 中，物件是資料與程式碼的組合，可以是指整個應用程式或者是應用程式中的一小部分。以生活中的物品為例，我們可以說電腦是一個物件，而組成電腦的 CPU、硬碟等也都可以做為一個物件。

屬性（attribute）或成員變數（member variable）：是用來描述物件（object）的特性。以電腦為例，CPU 等級或者製造商等用來描述電腦的特質就是這個物件的屬性。

方法（method）或成員函式（member function）：
定義物件的動作。以電腦為例，開機、關機、執行應用程式等動作就是電腦這個物件的方法。

類別（class）：
是指物件的分類，可以透過類別將物件分門別類，同樣類別的物件有相同的屬性與方法。以電腦這個類別為例，有廠牌、顏色等屬性，以及開機、關機、執行應用程式等方法，那麼 Surface 的筆記型電腦隸屬於電腦這類別，廠牌為 Microsoft，顏色則為銀色，至於 Dell 的筆記型電腦就屬於電腦類別的其他物件。也可以說物件是類別的實體。

物件導向程式設計（Object Oriented Programming, OOP）主要有以下的特徵：
封裝（encapsulation）：將資料與用來處理資料的函式放在一起成為一個類別，稱為「封裝」。

繼承（inheritance）：從原先有的類別定義出新的類別，既有的類別稱為「父類別（parent class）」，而衍伸的新類別叫做「子類別（child class）」。透過 OOP 的繼承特性，可以提高軟體的重複使用性，只要撰寫完成父類別的程式碼，就可以在其他子類別程式碼中重複使用。

多型（polymorphism）：當子類別的不同物件收到相同訊息的時候，可以根據子類別中定義的方法來作執行，而不受父類別的限制。以飛行物為例，設定飛行物為父類別，其下的子類別有熱氣球與直升機，而父類別的方法包括起飛與降落，當子類別的物件收到起飛的訊息時，熱氣球可以用燃燒來起飛，而直升機可以靠旋轉螺旋槳起飛，子類別中的方法可以覆蓋（override）父類別的方法。



### Python3.4

```python
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
```
