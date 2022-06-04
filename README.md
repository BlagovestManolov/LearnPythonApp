# LearnPython 🚀
### by Blagovest.Manolov 🇧🇬
A project made for educational purposes. I am a student and decided to make an application through which we can learn Python.

### For this purpose I have used the following libraries:
- :atom: `Tkinter`
- ⚛️ `Random`
### The fonts used are taken from Google Fonts, or as follows:
- [Cinzel](https://fonts.google.com/specimen/Cinzel?query=Cinzel)
- [Lakki Reddy](https://fonts.google.com/specimen/Lakki+Reddy?query=Lakki)
- [Source Code Pro](https://fonts.google.com/specimen/Source+Code+Pro?query=Source+Code+Pro)
### Colors used for the visualization of the program:
-  ![Asset 21](https://user-images.githubusercontent.com/101090286/171855617-2642e54e-0f9b-41bb-98ad-5902c5393b08.png) `#ad6332`
- ![Asset 22](https://user-images.githubusercontent.com/101090286/171855772-8e3f0483-ae9a-48f3-b92b-997f1ccf783c.png) `#2d6063`
- ![Asset 23](https://user-images.githubusercontent.com/101090286/171855923-7d4fbbd7-84f2-4e45-9a98-e052fad576bd.png) `#e7e0c6`


### Application interface: 🖥️
- The foundational element of a Tkinter GUI is the window. Windows are the containers in which all elements live.
  - Import Tkinter :atom:
  ```python
  from tkinter import *
  ```
  - Create a window:
  ```python
  first_window = Tk()
  first_window.title("LEARN PYTHON") # window name
  first_window.geometry("800x640") #window size
  first_window.config(bg="#e7e0c6") #background color 
  first_window.mainloop() #start your window
  ```
![first_window](https://user-images.githubusercontent.com/101090286/171996373-d0cd4881-5c66-4c0d-9b63-134c442b9bd1.png)
   - Create an additional canvas, which we place in an existing window. Place the canvas in the left, upper corner with coordinates 0, 0
  ```python
  r_canvas = Canvas(first_window,
                  width=130,
                  height=640,
                  bg="#ad6332")
  r_canvas.place(x=0, y=0)
  ```
![canvas](https://user-images.githubusercontent.com/101090286/171997741-57a9b725-d14a-4a99-97c4-1146fc37a7c8.png)
   - Creating another canvas with a size of y - 3 times smaller, which will serve to show what stage of the program we are. Place the canvas in the left, 
     upper corner with coordinates 0, 0. After accessing another window other than the initial one, the green canvas will move one position down.
  ```python
  b_canvas = Canvas(first_window,
                  width=130,
                  height=213,
                  bg="#2d6063")
  b_canvas.place(x=0, y=0)
  ```
![new_canvas](https://user-images.githubusercontent.com/101090286/171997912-91c7f849-f142-4f12-b72d-87dd68bfc109.png)
