# 智能淨灘車計畫
> presented by 週三下午第4組

## 車體
### 車頭支架
**配備:** RPi, PiCamera及HC-SR04超音波模組
**用途:** 垃圾種類辨識、障礙物迴避

### 前方掃把滾輪
**用途:** 將垃圾掃到斜坡上

### 斜坡
**配備:** 壓克力板、滾筒4個(各以2個TT馬達驅動)、橡皮筋
**用途:** 將掃起的垃圾送進垃圾桶

### 垃圾桶
**配備:** 八角形鴛鴦木桶(中間用木板隔成兩區)、轉軸、萬向輪
**用途:** 垃圾分類(可回收/一般垃圾)

## Rpi
### 辨識模型: You Only Look Once
**來源:** [YOLO官網](https://docs.ultralytics.com/)
**版本:** YOLOv8
### dataset 1
![圖片](https://hackmd.io/_uploads/Bkgq5iDHA.png)
**citation:** 
```
@article{taco2020,
    title={TACO: Trash Annotations in Context for Litter Detection},
    author={Pedro F Proença and Pedro Simões},
    journal={arXiv preprint arXiv:2003.06975},
    year={2020}
}
```
**來源:** [TACO (Trash Annotations in Context)](http://tacodataset.org/)

### dataset 2 (from Roboflow)
![圖片](https://hackmd.io/_uploads/ryd4ijPrR.png)

**citation:** 
```
@misc{
    taco-mqclx_dataset,
    title = { TACO Dataset },
    type = { Open Source Dataset },
    author = { Divya },
    howpublished = { \url{ https://universe.roboflow.com/divya-lzcld/taco-mqclx } },
    url = { https://universe.roboflow.com/divya-lzcld/taco-mqclx },
    journal = { Roboflow Universe },
    publisher = { Roboflow },
    year = { 2022 },
    month = { jun },
    note = { visited on 2024-06-13 },
}
```
**來源:** [TACO dataset with YOLO (by Divya)](https://universe.roboflow.com/divya-lzcld/taco-mqclx)
**用途:** 使用其以垃圾為主的資料庫照片作為模型訓練之素材

## Arduino
**配備:** 14顆TT馬達，HC-SR04超音波模組、ST7789螢幕模組，RGB模組，傳輸線(對RPi)

## 參考資料
- 計畫靈感來源: [淨灘車(Youtube)](https://www.youtube.com/watch?v=wqPrcYVvkt0)
- 物體辨識模組: [YOLOv8 by ultralytics](https://docs.ultralytics.com/)
