# Global Survey of Android Dual-use Apps

## Files included
1. `terms.csv`: 
2. `play_store.csv`: Contains all downloaded apps in 2020 and 2020. The file includes `appId`, `title`, `detected_language` (language of metadeta), `crawl_language` (qurey language used to obtain app), `crawl_year`, `ml_score`(classification score), `manual_label`, and `capabilities` (capabilities of flagged dual-use apps).
3. `flagged_apps_2020.csv`: All apps manually flagged in 2020
4. `flagged_apps_2022.csv`: All apps manually flagged in 2022
5. `chinese_stores.csv`: Contains all downloaded apps from the four Chinese app stores *Xiaomi*, *Baidu*, *Tencent*, and *Huawei*. The file includes `appId`, `title`, `manual_label`, and `capabilities` (capabilities of flagged dual-use apps).
6. `script.ipynb`: A script that compiles important results from the main analysis of 2020's crawl.
7. `play_store.db`: Contains `play_store.csv` as a table (The file will get removed after updating script.ipynb to use pandas instead of SQLite).

