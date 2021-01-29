# PYTHON_NOTE2

# Pandas_dataframe_series 
# updated on 21-01-29
---------------------------------------------------------------------------------------------------------------------
# Pandas 是 python 的一個數據分析 lib，2009 年底開源出來，提供高效能、簡易使用的資料格式(Data Frame)讓使用者可以快速操作及分析資料，
# 主要特色描述如下：在異質數據的讀取、轉換和處理上，都讓分析人員更容易處理，例如：從列欄試算表中找到想要的值。

# Pandas 提供兩種主要的資料結構，Series 與 DataFrame。
  # Series 顧名思義就是用來處理時間序列相關的資料(如感測器資料等)，主要為建立索引的一維陣列。
  # DataFrame 則是用來處理結構化(Table like)的資料，有列索引與欄標籤的二維資料集，例如關聯式資料庫、CSV 等等。

# 透過載入至 Pandas 的資料結構物件後，可以透過結構化物件所提供的方法，來快速地進行資料的前處理，如資料補值，空值去除或取代等。
# 更多的輸入來源及輸出整合性，例如：可以從資料庫讀取資料進入 Dataframe，也可將處理完的資料存回資料庫。
  # 安裝: pip install pandas 

# example_1: 
import pandas as pd
import pandas_profiling

pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/planets.csv').profile_report()

import pandas as pd # 引用套件並縮寫為 pd

groups = ["Modern Web", "DevOps", "Cloud", "Big Data", "Security", "自我挑戰組"]
ironmen = [46, 8, 12, 12, 6, 58]

ironmen_dict = {"groups": groups,
                "ironmen": ironmen
                }

ironmen_df = pd.DataFrame(ironmen_dict)

print(ironmen_df) # 看看資料框的外觀
print(type(ironmen_df)) # pandas.core.frame.DataFrame
