openCVを使ったカメラから動画を取得し、表示する
import cv2
# VideoCapture オブジェクトを取得します
capture = cv2.VideoCapture(0)
#カメラから連続的に画像を取得するため、ここでは while 文で繰り返し処理
#while 内の最初で、カメラから1コマのデータを取得するため capture.read() を呼び出す
#取得した1コマの画像データは、変数 frame で取得
#qを押すとループを終わる。
while(True):
　　ret, frame = capture.read()
  　cv2.imshow('frame',frame)
　　if cv2.waitKey(1) & 0xFF == ord('q'):
  　　　　break
capture.release()
cv2.destroyAllWindows()
