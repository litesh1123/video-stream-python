# video-stream-python
step1: import cv2

in the above command we are importing module cv2 ,which is computer vision ,aftr writing this command we are connecting our cv2 module with our jupyter notebook code.

step2: cap=VideoCapture(0)

in the above command , this function VideoCapture is used to connect to webcam if 0 is used than it would to connect to our internal connected devices .

step3: here we will be using while loop ,with true . while true

it is infinite loop

step 4: status,photo=cap.read()

in the above command we are going to read photo we captured ,we are going to use read() function this function would return two values so we have used two variables status and photo this will store our two values .

status will print true if captured and false if not captured.

step 5: a=photo[100:300,250:450]

here in above command ,inside photo variable we have stored photo .as we need to crop we will use slicing operation feature present in python.now cropped photo is stored in a variable

step 6: b=photo[100:300,250:450]

here in above command , we have cropped using slicing operation and stored in variable b

step 7: photo[0:200,0:200]=a
photo[280:480,440:640]=b

photo[0:200,0:200]=a
photo[280:480,440:640]=b
in the above comands we have stored variables a and b in photo variable at top left and bottom right

step 8:

cv2.imshow("My window",photo)
    if cv2.waitKey(100)==13:
        break
in the above command we are using a function which will show us a pop up window with name “my window” and in it photo variable is displayed

whenever if cv2.waitKey(100)==13: in this command when u click enter 13 number is taken , if someone click enter till then pop up box will wait

and if condition is satisfied than break will be executed and it will be coming out of loop

step 9:

cv2.destroyAllWindows()
after using this function pop up window will be deleted .

step 10:

cap.release()
and it will release , camera that it disconnects connection between camera and jupyter notebook .
