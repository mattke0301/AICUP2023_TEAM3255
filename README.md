# AICUP2023 多模態病例嗓音分類競賽 TEAM_3255
## 聲音訊號資料處理
covarep-1.4.2為從covarep官網下載的程式碼，本程式碼可以在 **MATLAB R2015b(9.0)** 上運行  
請至cocarep以及MATLAB官網下載對應版本  
下載完後，請在MATLAB開啟對應檔案位置(open folder)  
之後在Command Window分別執行項列兩個程式:  
1. startup
2. test(**其中test.m 中的in_dir請修改成要提取特徵的.wav音檔檔案位置**)  
**請注意: test.m請放到./covarep-1.4.2/feature_extraction/的資料夾下**

執行完上述兩個程式後即可提取出音檔對應的.mat檔案  

## 訓練流程
python版本為3.6，請先創建一個空的環境，其餘的package請執行**pip install -r requirements.txt**  
model訓練過程請執行**model_final_version.ipynb**，請注意其中file_path和read_csv的讀取路徑記得修改成自己對應的路徑!  

另外模型在訓練時會把模型儲存在fold_model的資料夾中，如為創建，請記得創建一個資料夾以存放模型。  
而在**model_final_version.ipynb**中有一些碼起來的程式碼，其為在測試模型時所使用的(沒做K-fold和Ensemble)，如有需要的話可以自行取用

## 預測結果
**submit_ensemble.ipynb**提供了預測Public & Private 測試集的code  
一樣請記得修改對應路徑即可成功執行程式碼，程式執行完後會直接存成csv檔
