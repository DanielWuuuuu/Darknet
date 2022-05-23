### Darknet 修改紀錄

### 1. 檔案: `src/detector.c`

#### 1.1 修改範圍

1) function: float validate_detector_map( )

#### 1.2 說明

1. function: float validate_detector_map( )
   
   (1) 修改目的        => 導出TP及FP的bbox於`.txt`檔

       (2) [DanielWu]    => 為DanielWu新增的註解

       (3) 重新編譯並執行`darknet.exe`後，會產生`results/calculate_mAP_log.txt`

       (4) TP的bbox可於`++tp_for_thresh = %d`的下一行找到

            如：`# dets[    6].bbox : (0.863384, 0.710473, 0.162466, 0.230406)`

       (5) FP的bbox可於`fp_for_thresh++ = %d`的下一行找到

            如：`# dets[  2].bbox : (0.684666, 0.172405, 0.025626, 0.078889)`

       (6) TP或FP加一後，會記錄TP或FP在各類別的數量

       (7) 目前判斷成FN的bbox未能導出來


