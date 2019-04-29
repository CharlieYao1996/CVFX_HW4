# CVFX_HW4
  # 1.sequence of moving-forward images in campus
  Input:梅園
  >><img width="250" height="250" src="IMG_20190429_181209.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181214.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181219.jpg"/> |
  >><img width="250" height="250" src="IMG_20190429_181224.jpg"/>        |<img width="250" height="250" src="IMG_20190429_181228.jpg"/>
   |<img width="250" height="250" src="IMG_20190429_181233.jpg"/> 
 
  
  # 2.feature extraction and matching results
  Orb (Oriented Fast and rotated BRIEF)
  >><img width="1000" height="500" src="out1.jpg"/> <img width="1000" height="500" src="out2.jpg"/> 
  >><img width="1000" height="500" src="out3.jpg"/> <img width="1000" height="500" src="out4.jpg"/>
  >><img width="1000" height="500" src="out5.jpg"/>
  > 
  最初我們用跟助教相同的code做feature extraction，feature extractor是用orb，分別做出了五張對應圖，但可能是由於照片色調較暗的關係，對應的線條較不明顯。

  
  # 3.image alignment and generate infinite zooming effect
  >>![](bad1.gif)
  >
  我們根據上面ORB的結果對照片做了zoom effect，使用照片原檔無修圖的結果如上圖所示，可以看到由於梅園的兩側皆為茂密的樹木，所以乍看之下zoom的效果其實還不錯，只是因為照片的邊緣太銳利的關係，會有很明顯的照片間格，此缺陷我們會在稍後介紹改善方法。
  # 4.implement different feature extrators
  1.SIFT (Scale-invariant feature transform)
  >><img width="1000" height="500" src="sift5-6.jpg"/>
我們做了圖片5-6的SIFT，SIFT需要跑比較久，但是也可以明顯的看出SIFT對應到的線條較多且皆為優良的平行線。
>
2. SURF (Speeded Up Robust Features)
  >><img width="1000" height="500" src="surf1-2.jpg"/>
接下來做了圖片1-2的SURF，可以看到跟上面ORB的結果比較下來也是看起來比較良好的，但是缺點就是形成時間較久。  
  
  # 5.add some image processing to enhance effect
  >>![](new_out.gif)
為了改善上述3.的缺點，我們在照片的邊角加上了bluring、feathering等效果，讓圖片的銜接看起來較為自然且平順，但由於圖片原始檔較大，產生的檔案也太大導致於無法直接上傳至Github，所以上圖是我們經過壓縮後的GIF檔，我們另外放了原始大檔案的GIF檔的版本在[這裡](  https://drive.google.com/open?id=1sLpkx2ouSv--P3yEZ7bUzH0dNpYyiIZL) ，但其實在銜接的過程中還是可以看出很多不自然的地方，我們認為這應該是跟拍照時的穩定角度有關，也許之後測試新的檔案可以想辦法利用穩定器等輔助工具來幫助我們更好的完成zoom effect的進行。

  # Conclusion
  
 在進行過這次的image alignment還有zooming effect的製作後可以簡單的歸納出一些方法的優缺點:
 |             | ORB           | SIFT | SURF  |
| :-------------: |:-------------:| :-----:| :-----:|
| Time       | Best      | command |good  |
| Scale        | Best     |  good | command  |
| Illumination      |good      |   Best | good  |

