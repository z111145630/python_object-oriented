# Python物件導向（Object Oriented, OO）

### 物件（object）或者實體（matters）：

在 Python 中，物件是資料與程式碼的組合，可以是指整個應用程式或者是應用程式中的一小部分。以生活中的物品為例，我們可以說電腦是一個物件，而組成電腦的 CPU、硬碟等也都可以做為一個物件。

### 屬性（attribute）或成員變數（member variable）：
是用來描述物件（object）的特性。以電腦為例，CPU 等級或者製造商等用來描述電腦的特質就是這個物件的屬性。

### 方法（method）或成員函式（member function）：
定義物件的動作。以電腦為例，開機、關機、執行應用程式等動作就是電腦這個物件的方法。

### 類別（class）：
是指物件的分類，可以透過類別將物件分門別類，同樣類別的物件有相同的屬性與方法。以電腦這個類別為例，有廠牌、顏色等屬性，以及開機、關機、執行應用程式等方法，那麼 Surface 的筆記型電腦隸屬於電腦這類別，廠牌為 Microsoft，顏色則為銀色，至於 Dell 的筆記型電腦就屬於電腦類別的其他物件。也可以說物件是類別的實體。

<br>
<br>
<br>

### 物件導向程式設計（Object Oriented Programming, OOP）主要有以下的特徵：

#### • 封裝（encapsulation）：
將資料與用來處理資料的函式放在一起成為一個類別，稱為「封裝」。


```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        print("area = ", self.length*self.width)

    def Perimeter(self):
        print("perimeter = ", 2*(self.width+self.length))
```
說明：簡單的說將同一類或者同一物的資料與運算打包起來,就稱之為封裝。
上面建立了一個矩形類別，要求矩形的周長與面積,如果以函式的話,勢必得要有兩次長度與寬度的資料傳入函式,而封裝起來的物件,僅需要直接調用定義的方法(Method)即可。
<br>

#### • 繼承（inheritance）：
從原先有的類別定義出新的類別，既有的類別稱為「父類別（parent class）」，而衍伸的新類別叫做「子類別（child class）」。透過 OOP 的繼承特性，可以提高軟體的重複使用性，只要撰寫完成父類別的程式碼，就可以在其他子類別程式碼中重複使用。

```python
class Pet:
    def __init__(self, name):
        self.name = name

    def jumps(self):
        print("jump")

    def runs(self):
        print("run")


class Dog(Pet):
    def shout(self):
        print("my name is " + self.name + " bow-wow ")


class Cat(Pet):
    def shout(self):
        print("my name is " + self.name + " meow")
```        
說明：將多個類別的相似處設為一個基礎類別,各類別再針對個別特性從基礎類別去做延伸,以貓狗為例子,將定義其跑,跳,叫聲的類別以Python寫出來如上,同樣在定義狗的時候,卻重複了跑與跳,寫兩次雖說不是不可以,但這就是多餘的,更何況若有多個類似物件,重複的步驟可就多了,這時候就可利用繼承方式將不一樣的挑出來。
由於貓與狗只有叫聲不同,將跑與跳定義為Pet類別,在定義貓與狗時,分別繼承Pet類別即可。
<br>

#### • 多型（polymorphism）：
當子類別的不同物件收到相同訊息的時候，可以根據子類別中定義的方法來作執行，而不受父類別的限制。
```python
mycat = Cat("May")
mydog = Dog("Lucky")

mycat.shout()
mydog.shout()
```
說明：多型讓子類別(貓與狗)呼叫同名的方法(Method shout)時，呈現各子類別不同之處(貓叫與狗吠)，例如牛也能有叫聲,它僅需要在類別中定義shout方法即可，也就是說不在乎是哪一種物件呼叫了同名方法,只需要該物件有定義此同名方法就好了。



