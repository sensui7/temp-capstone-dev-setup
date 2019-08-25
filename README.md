# temp-capstone-dev-setup

## Installation Links & Account Setup
- Register for the JetBrains Student Pack (use your PSU email)
  - https://www.jetbrains.com/shop/eform/students
- Install the IDE for development environment (click the right one for your platform)
  - https://www.jetbrains.com/pycharm/download

## Python Installation to Work w/ Pycharm
- Download Python 3.7.4 here
  - https://www.python.org/downloads/release/python-374/
  
## Git Integration w/ Pycharm
- Install GIT here required for use w/ IDE (cross-platform)
  - https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
- OPTIONAL - Install Git Toolbox plugin on IDE's plugin list

## Flask & Django Integration
- Already is an option on Pycharm when you click on setting up a new project.
- Django project as a template is also provided as an option.

## Linking IDE to DB (MongoDB)
- Install `Mongo Plugin` in the plugins window on Pycharm
  - This tool allows accessing to Mongo databases and provides CRUD operations on mongo collections.

## Setting up Built-in Python Dev Tools (unit tests and tkinter)
- `unittest` module should be provided already as a part of the language
  - You can just simply create a unit test by creating a new Python file, and then pick the unit test file option
  - See https://docs.python.org/3/library/unittest.html
  - Example program
```
import unittest

class TestStringMethods(unittest.TestCase):

    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')

    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
        self.assertFalse('Foo'.isupper())

    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        # check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)

if __name__ == '__main__':
    unittest.main()
```
- tkinter module needs to be installed
   - Please install tkinter via `sudo apt-get install python3-tk`
   - See https://docs.python.org/3/library/tkinter.html
   - Example program
```
import tkinter as tk

class Application(tk.Frame):
    def __init__(self, master=None):
        super().__init__(master)
        self.master = master
        self.pack()
        self.create_widgets()

    def create_widgets(self):
        self.hi_there = tk.Button(self)
        self.hi_there["text"] = "Hello World\n(click me)"
        self.hi_there["command"] = self.say_hi
        self.hi_there.pack(side="top")

        self.quit = tk.Button(self, text="QUIT", fg="red",
                              command=self.master.destroy)
        self.quit.pack(side="bottom")

    def say_hi(self):
        print("hi there, everyone!")

root = tk.Tk()
app = Application(master=root)
app.mainloop()
```
    
## What is Django, Flask, and Tkinter?
- Django
  - A Python-based free and open-source web framework, which follows the model-template-view architectural pattern.
- Flask
  - A popular, extensible web microframework for building web applications with Python.
- Tkinter
  - The standard Python interface or module for creating GUIs.
