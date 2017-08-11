import cv2
import numpy as np

# Load our input image
#upper
img1 = cv2.imread('./images/all1.jpg')
#lower
img2 = cv2.imread('./images/all2.jpg')
#vetical flip
img22=cv2.flip(img2,1)

#upper+lower image/merge
img3 = np.vstack((img1,img22))

#add text
cv2.putText(img3, 'Believe Half of What You See',(100,100),cv2.FONT_ITALIC,4,(255,255,255),2)
cv2.putText(img3, 'And None of What You Hear.',(300,200),cv2.FONT_ITALIC,3,(255,255,255),2)
cv2.putText(img3, 'Believe Half of What You See',(900,900),cv2.FONT_ITALIC,4,(255,255,255),3)
cv2.putText(img3, 'And None of What You Hear.',(1200,1000),cv2.FONT_ITALIC,4,(255,255,255),3)
cv2.putText(img3, 'Believe Half of What You See',(2000,1500),cv2.FONT_ITALIC,3.5,(255,255,255),2)
cv2.putText(img3, 'And None of What You Hear.',(2200,1700),cv2.FONT_ITALIC,2,(255,255,255),2)
cv2.putText(img3, 'All War Is Deception.',(2200,1700),cv2.FONT_ITALIC,2,(255,255,255),2)

#export
cv2.imwrite('./output/all12.jpg',img3)
cv2.imshow('Original', img3)
cv2.waitKey()
cv2.destroyAllWindows()

HAVE A NICE DAY B)
