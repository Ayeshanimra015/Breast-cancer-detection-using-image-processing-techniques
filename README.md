# Breast-cancer-detection-using-image-processing-techniques
In this project, I developed a deep learning model using image processing techniques to accurately detect breast cancer and predict its stage. The workflow included key stages such as image preprocessing, segmentation, feature extraction, classification, and detection.
1. Image Preprocessing
  - Enhanced mammogram images by applying grayscale conversion and Gaussian filtering to reduce noise and improve image clarity, making feature extraction more effective.
2.Segmentation
  - Applied thresholding and region-based segmentation to isolate regions of interest (ROIs) that could potentially represent cancerous tissues, allowing the model to focus on relevant areas of the mammogram.
3.Feature Extraction
  - Used Convolutional Neural Networks (CNN) to automatically extract critical features such as texture, shape, and edge patterns from the segmented regions, differentiating between normal and abnormal tissues.
4. Classification
  - Implemented a CNN-based model to classify the extracted features into cancerous and non-cancerous categories.
5.Detection
  - The model further predicted the stage of the cancer, ranging from stage 0 (early detection) to stage 4 (advanced cancer), based on the features extracted from the mammogram.
  - This detection allowed for precise identification of the cancer’s progression, helping clinicians assess the stage and tailor treatment accordingly.
This model is developed using Deep learning, Machine learning algorithms and Image processing techniques with an accuracy rate of 91%.
from tkinter import *
import sqlite3
import os
import sys
from tkinter import messagebox

from PIL import ImageTk, Image
root = Tk()
root.geometry('1366x768')
root.title("BreastCancer")
root.configure(bg='white')

canv = Canvas(root, width=1366, height=768, bg='white')
canv.grid(row=2, column=3)
img = Image.open('back.png')
photo = ImageTk.PhotoImage(img)
canv.create_image(1,1, anchor=NW, image=photo)
Un = StringVar()
Pw = StringVar()

def back():
    root.destroy()
    os.system('python Main.py')

def login():
    un = Un.get()
    pw = Pw.get()
    if un == "":
        messagebox.showinfo("Cancer","Enter Username")
    else:
        if pw == "":
            messagebox.showinfo("Apple", "Enter Password")
        else:
            if un == "admin" and pw == "admin":
                root.destroy()
                os.system('python menu.py')
            else:
                messagebox.showinfo("Cancer", "Try Again")


label_0 = Label(root, text="Admin Login", bg='black',fg="white", width=20, font=("bold", 20))
label_0.place(x=840, y=300)
label_4 = Label(root, text="Username", bg='black',fg="white", width=10, font=("bold", 10))
label_4.place(x=900, y=350)
entry_5 = Entry(root, textvar=Un)
entry_5.place(x=1000, y=350)
label_5 = Label(root, text="Password", bg='black',fg="white", width=10, font=("bold", 10))
label_5.place(x=900, y=400)
entry_6 = Entry(root, textvar=Pw, show="*")
entry_6.place(x=1000, y=400)
Button(root, text='Login', width=15, bg='brown', fg='white', command=login).place(x=900, y=450)
Button(root, text='Cancel', width=15, bg='brown', fg='white', command=back).place(x=1015, y=450)
label_0 = Label(root, text="                   ", bg='black',fg="white", width=20, font=("bold", 20))
label_0.place(x=840, y=500)
root.mainloop()
