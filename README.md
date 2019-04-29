# CVFX_HW4
  # 1.sequence of moving-forward images in campus
  >><img width="250" height="250" src="IMG_20190429_181209.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181214.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181219.jpg"/> |
  >><img width="250" height="250" src="IMG_20190429_181224.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181228.jpg"/>
   |<img width="250" height="250" src="IMG_20190429_181233.jpg"/> 
  >### 以上是我們在梅園拍的六張連續照片。
  
  # 2.feature extraction and matching results
  >## orb
  >><img width="1000" height="500" src="out1.jpg"/> <img width="1000" height="500" src="out2.jpg"/> 
  >><img width="1000" height="500" src="out3.jpg"/> <img width="1000" height="500" src="out4.jpg"/>
  >><img width="1000" height="500" src="out5.jpg"/>
  > 
  最初我們用跟助教相同的code做feature extraction，feature extractor是用orb，分別做出了五張對應圖，但可能是由於照片色調較暗的關係，對應的線條較不明顯。

  
  # 3.image alignment and generate infinite zooming effect
  >>![](bad1.gif)
  # 4.implement different feature extrators
  >## SIFT
  >><img width="1000" height="500" src="sift5-6.jpg"/>
  >### 之後我們做了圖片五到六sift，sift需要跑比較久，但是效果較佳。
  >## SURF
  >><img width="1000" height="500" src="surf1-2.jpg"/>
  >### 最後圖片一到二的surf，  
  
  # 5.add some image processing to enhance effect
  >>![](new_out.gif)
  >### 最後我們有加了一些特效，像是  
  >### 另外有一個解析度較佳的版本存在[雲端](  https://drive.google.com/open?id=1sLpkx2ouSv--P3yEZ7bUzH0dNpYyiIZL)
