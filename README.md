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

  - Create another text label that I will use to advertise myself 😄
  ```python
  created_by = Label(
      text="created by Blagovest.Manolov",
      font=("Cinzel Decorative Bold", 9),
      fg="#2d6063",
      bg="#e7e0c6"
  )
  created_by.place(x=230, y=287)
  ```
  ![by_me](https://user-images.githubusercontent.com/101090286/172006500-50d259dd-bbea-4477-8fbb-aff933f67fc9.png)
  - It's time for the buttons. We will use two types of buttons:
    - Button to start the application and go to the next window. Used Cinzel Decorative Black font. When creating a button, it must execute a command. In this case, pressing the button will redirect us to a function named start.
    ```python
    start_button = Button(
          text="Start",
          font=("Cinzel Decorative Black", 16),
          fg="#e7e0c6",
          bg="#ad6332",
          command=start
    )
    start_button.place(x=230, y=309)
    ```
    ![start_button](https://user-images.githubusercontent.com/101090286/172007104-6810e8f8-59c8-43fa-a57e-61b5e8cdd0c8.png)

    - Button that gives us information about the application. Here, in addition to creating the button, we will have to import something else. At the beginning of the project we need to import tkinter.messagebox. This allows us to open a new window that is individual. In addition, we will have to make a command to redirect to a function to open this message box.
    ```python
    import tkinter.messagebox
    ```
    ```python
    information_button = Button(
          text="INFORMATION",
          font=("Cinzel Decorative Black", 8),
          fg="#e7e0c6",
          bg="#2d6063",
          command=information
    )
    information_button.place(x=230, y=364)
    ```
    ![information](https://user-images.githubusercontent.com/101090286/172007938-d74d329c-8b6e-4786-9188-9b592ad239d4.png)
    
    - We will now define the first function (information). Through it we will access information about the project by pressing the information button.
    ```python
    def information():
      tkinter.messagebox.showinfo("INFORMATION", "A project made for educational purposes. \n"
                                                 "I am a student and decided to make an application\n"
                                                 " through which we can learn Python.")
    ```
    ![information_panel](https://user-images.githubusercontent.com/101090286/172008569-c4016cbc-bcb8-4d75-b432-84e551907ebc.png)
