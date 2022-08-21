from pytube import YouTube                                                                  # I used the python pytube module to get Youtube
import ssl                                                                                  # This installs the  ca-certificates(otherwise you will get an error on how the certificates were not verified)
ssl._create_default_https_context = ssl._create_unverified_context


print("Copy & Paste the video url you would like to download ")                             # This print statement ask the user for input then saves the input in the variable link
link = input()

print(link)                                                                                  # I was having trouble in getting the link so I put this print statement to let me know exactly what was being
                                                                                             #  processed when the yt variable was called, think of it as a self debugger. 

yt = YouTube(link)                                                                           # yt is a variable that runs the Youtube link when called.


print("Title: ", yt.title)                                                                   # this prints out the Title 

print("Views: ", yt.views)                                                                   # this prints out the views of the video        

yd = yt.streams.get_highest_resolution()                                                     # this shows what quality to download it in 

yd.download("/Users/jasonbempong/Desktop/All/resume projects/ytdownloader/downloaded vids")  #this specifies where I want the video to go 



# If you are using a IDE, this code has to be executed in a virtual environment to install pytube
# virtual environment commands for terminal as below 
# virtualenv venv
# source venv/bin/activate   *to activate the environment 
# Then its ready for use (make sure you install pytube)  ...pip install pytube
# Made by Dragstarr :)


