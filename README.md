# Global Survey of Android Dual-use Apps
## Abstract
Intimate partner violence (IPV) is a pervasive societal problem that affects millions of people around the world. IPV perpetrators increasingly weaponize digital technologies like mobile applications (“apps”) to spy on, monitor, and harass victims. Surveillance-capable apps can have legitimate use cases, for example, locating children, and are therefore easily available on various mobile app stores like the Google Play Store. Nevertheless, these applications are easily repurposed by abusers to track their victims. The problem of such dual-use apps in IPV is global. However, current understanding of the ecosystem of such apps is limited to English-language apps, potentially limiting its relevance to non-English speaking IPV survivors across the world. In this paper, we study the prevalence of dual-use applications found in 15 languages and 27 countries. We collected 51,868 unique apps in 2020 from the Google Play Store, using queries such as “track wife’s location.” Through a semi-manual analysis of a subset of these apps, we discovered 854 unique dual-use apps, and estimate that among the apps collected from Google Play, 3,988 are dual-use apps. We found notable differences in app search results, suggested queries, and marketed capabilities of dual-use apps across different languages. For instance, we identified that 18% of dual-use apps do not have an English description, and 28% could not be found using English queries. Google Play (cursorily) blocks certain queries referring explicitly to intimate partner surveillance (IPS) to discourage potential abusers, but the blocking efficacy varies across languages. For example, we found that 80% of explicit IPS queries for English are blocked, but none for Bengali, Chinese, Hindi, Malay, Thai, and Vietnamese. Thus, abusers fluent in those languages can evade such blocking with no effort.

## Paper
Our paper appears in PoPETS/PETS 2022; you may find the paper [here](https://petsymposium.org/popets/2022/popets-2022-0102.pdf). 

## Crawling script
You may find the crawling script [here](https://github.com/rchatterjee/appscrapers)

## Files
1. `play_apps.csv`: Contains all downloaded apps in 2020 and 2020. The file includes `appId`, `title`, `detected_language` (language of metadeta), `crawl_language` (qurey language used to obtain app), `crawl_year`, `ml_score`(classification score), `manual_label`, and `capabilities` (capabilities of flagged dual-use apps).
2. `flagged_apps_2020.csv`: All apps manually flagged in 2020
3. `flagged_apps_2022.csv`: All apps manually flagged in 2022
4. `chinese_stores.csv`: Contains all downloaded apps from the four Chinese app stores *Xiaomi*, *Baidu*, *Tencent*, and *Huawei*. The file includes `appId`, `title`, `manual_label`, and `capabilities` (capabilities of flagged dual-use apps).
5. `script.ipynb`: A script that compiles important results from the main analysis of 2020's crawl.
6. `play_apps.db`: Contains `play_apps.csv` as a table; used by `script.ipynb` (The file will get removed after updating script.ipynb to use pandas instead of SQLite).
7. `terms.csv`: Contains results from query snowballing and apps collected for each term. You may find the [file here](https://drive.google.com/file/d/1VYj54HwIHPqvPjkVIpv7wF6jDyRVWiZO/view?usp=sharing) _(File size: 1.22 GB)_.

## Dependencies
The script needs
* `Python3.5+`
* `sqlite3`
* `pandas` (pandas 1.4+ is recommonded)
* [`jupyter notebook`](https://jupyter.org/install)

## How to run
To use the script, run the following line
```bash
$ jupyter notebook script.ipynb 
```

If you are unfamiliar with jupyter notebook, you may use the following line to output results as an HTML file:
```bash
$ jupyter nbconvert --execute --to html script.ipynb
```

## License

MIT License

Copyright (c) 2022 Majed Almansoori

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
