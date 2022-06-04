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
  ![first_window](https://user-images.githubusercontent.com/101090286/172004471-382ccf4e-76ce-49dd-b926-bd7ce4de09be.png)

   - Create an additional canvas, which we place in an existing window. Place the canvas in the left, upper corner with coordinates 0, 0
  ```python
  r_canvas = Canvas(first_window,
                  width=130,
                  height=640,
                  bg="#ad6332")
  r_canvas.place(x=0, y=0)
  ```
  ![first_canvas](https://user-images.githubusercontent.com/101090286/172004589-281df13c-02e6-43bf-b56e-6beecdf76879.png)

   - Creating another canvas with a size of y - 3 times smaller, which will serve to show what stage of the program we are. Place the canvas in the left, 
     upper corner with coordinates 0, 0. After accessing another window other than the initial one, the green canvas will move one position down.
  ```python
  b_canvas = Canvas(first_window,
                  width=130,
                  height=213,
                  bg="#2d6063")
  b_canvas.place(x=0, y=0)
  ```
  ![second_canvas](https://user-images.githubusercontent.com/101090286/172004669-496ddb32-9cac-4dd3-a54f-5359b6224cc2.png)

  - Place a text label in the middle of your window. In this case we use a Lakki Reddy font, from google (shown above in the project presentation). The text label is the name of our game. Here the font size is larger (58), and the desired effect is easy to read the title.
  ```python
  ame_name_first = Label(
    text="LearnPython",
    font=("Lakki Reddy", 58),
    fg="#2d6063",
    bg="#e7e0c6"
  )
  game_name_first.place(x=230, y=215)
  ```
  ![name_game](https://user-images.githubusercontent.com/101090286/172006020-324d6a10-8934-4131-9c36-deb2b78c09f3.png)

  
