# 鐵達尼號生還預測

這是一個使用 **Kaggle Titanic Dataset** 的機器學習專案，目標是預測乘客是否能在鐵達尼號事故中存活。此專案主要用來練習 **資料前處理、特徵工程** 與 **多種分類模型的比較**。

## 專案內容

- **資料分析與視覺化**
  - 使用 seaborn/ matplotlib 分析乘客屬性（性別、艙等、年齡、親屬數等）與生還率的關係  
  - 缺失值檢查與處理  

- **資料前處理**
  - 移除無關欄位（`Name`, `Cabin`, `Ticket`, `PassengerId`）  
  - 類別欄位編碼（`Sex`, `Embarked` → LabelEncoder）  
  - 數值標準化（StandardScaler）  

- **模型訓練與比較**
  - Logistic Regression  
  - K-Nearest Neighbors (KNN)  
  - Support Vector Machine (Linear & RBF)  
  - Gaussian Naive Bayes  
  - Decision Tree  
  - Random Forest  

- **模型評估**
  - 訓練準確率（Training Accuracy）  
  - 測試集準確率（Confusion Matrix & Accuracy Score）  
  - 特徵重要度（Decision Tree Feature Importances）  

## 使用方法

### 1. 環境需求
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
### 2. 資料集

請先下載 Titanic Dataset (train.csv)
，並放到專案資料夾中。

### 3. 執行

若使用 Colab：
直接開啟 Titanic.ipynb，上傳 train.csv 後即可執行。

若使用 本地環境：
```bash
python titanic.py
```

## 實驗結果

* 訓練準確率

    * Logistic Regression: ~80%
    
    * KNN: ~83%
    
    * SVM (Linear): ~79%
    
    * SVM (RBF): ~83%
    
    * Naive Bayes: ~79%
    
    * Decision Tree: ~98%（可能過擬合）
    
    * Random Forest: ~90%

* 測試準確率

    * 約 78% ~ 83% 之間

* 特徵重要度 (Decision Tree)

    * Sex > Pclass > Age > SibSp > Parch > Fare > Embarked

## 備註

本專案主要用於學習機器學習流程，並非最佳解法，未來將持續改進。
