# Data004: AI導入・デジタル能力・戦略的意思決定品質データのlvsem分析

出典: Navara & Prabowo (2026), Mendeley Data, DOI https://doi.org/10.17632/fs78cfs84v.2

このフォルダには、Mendeley Dataから取得した元データと、ローカルRパッケージ `lvsem` を使った再現可能な分析ファイルを収録しています。他の `PLS-SEM/demo` フォルダと同じ流れで、測定ブロック、潜在変数スコア、構造モデル、ブートストラップ、信頼性・AVE、モデル図を出力します。

- `Excel data respondent.xlsx`: Mendeley Dataから取得した元Excelファイル
- `data004_ai_adoption_clean.csv`: 分析に使用したLikert項目を短い変数名に整理したデータ
- `Data_Dictionary.csv`: 変数名と元質問文の対応表
- `data004_analysis.Rmd`: R/lvsemによる再現用分析ノートブック
- `data004_analysis.html`: HTMLレポート
- `data004_lvsem_ai_adoption_model.png`: 構造モデル図
- `data004_path_coefficients_bootstrap.csv`: 1000回ブートストラップによるパス係数
- `data004_reliability_ave.csv`: Cronbachのalpha、合成信頼性、AVE
- `data004_outer_loadings.csv`: 外部負荷量
- `data004_latent_scores.csv`: 潜在変数スコア
- `data004_r2.csv`: 内生潜在変数のR2

レポートを再生成する場合:

```powershell
$env:RSTUDIO_PANDOC='C:\Users\hyama\AppData\Local\r-pandoc\r-pandoc\3.9.0.2'
& 'C:\Program Files\R\R-4.4.0\bin\Rscript.exe' -e "rmarkdown::render('data004_analysis.Rmd')"
```

注: 末尾の7つの観測変数は、データセットの説明に合わせて `Innovation_Capability` として扱っています。ただし、質問文そのものは戦略的意思決定品質に近い内容を含むため、構成概念の解釈には注意が必要です。
