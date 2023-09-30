# 30-Day-of-AI
# Introduction to computer vision using openCV with python
import cv2  # imprting library
img = cv2.imread("pro1.jpg")  #read an image 
cv2.imwrite("new logo.png", img)  # save an image

cv2.imshow("python logo", img)

# converting color to gray
grayimg = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)  # color to gray
cv2.imwrite("grayImage.png", grayimg)  #save an image

cv2.imshow("Orig", img)
cv2.imshow("Gray", grayimg)

# altering treshold value
threshImg = cv2.threshold(grayimg, 120, 255, cv2.THRESH_BINARY)[1]
cv2.imshow("threshImg", threshImg)
cv2.imwrite("thresholdImg3.png", threshImg)
cv2.waitKey(0)
cv2.destroyAllWindows()
