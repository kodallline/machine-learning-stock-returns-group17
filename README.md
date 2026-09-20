# Machine Learning and Stock Return Predictability | Group 17

Research seminar project based on Avramov, Cheng and Metzker (2023), *Machine Learning vs. Economic Restrictions: Evidence from Stock Return Predictability*, *Management Science*. This is an adaptation using our own dataset, not a replication of the authors' original results.

## Group members

- [Chistiakova Maria](https://github.com/mariachistiakova)
- [Meyzler Liya](https://github.com/kodallline)
- [Rudko Sofia](https://github.com/Sophie-Rudko)
- [Samoilova Maria](https://github.com/merysamoylova)

## Project

We use daily Yahoo Finance prices and volumes for 50 large U.S. stocks to build 16 technical features and predict monthly returns with Ridge and a neural network (NN3). We compare monthly rebalanced, equal-weighted, long-only top-five portfolios against an equal-weighted portfolio of all 50 stocks. We evaluate turnover, trading costs (0, 10, 25 and 50 bps), and a retention-buffer strategy. The test period is 2021–2025.

The gross performance differences are not statistically significant. Trading costs remove the small baseline advantage; the buffer lowers turnover, but its improvement in net performance is not statistically clear. The 50-stock sample was selected retrospectively and has survivorship bias. See the notebook for methods, figures, results and additional limitations.

## Files

| File | Purpose |
| --- | --- |
| `Group17_Final_Research_Notebook.ipynb` | Main notebook, including saved outputs |
| `daily_prices.csv.gz` | Input daily price and volume data |
| `group17_support_files.zip` | **Required:** data pipeline, tests, data dictionary and project protocols |
| `person3_person4_predictions.zip` | **Required:** frozen Ridge and NN3 forecasts used in portfolio analysis |
| `.gitignore` | Excludes locally generated files |

**All three input archives/files are required.** Do not rename them: the notebook checks their filenames and SHA-256 hashes. The support ZIP is not optional; without it the data pipeline cannot run.

## Run in Google Colab

1. Download the notebook and the three input files from this repository.
2. Open `Group17_Final_Research_Notebook.ipynb` in [Google Colab](https://colab.research.google.com/).
3. Upload `daily_prices.csv.gz`, `group17_support_files.zip` and `person3_person4_predictions.zip` to the Colab session's `/content` directory (Files sidebar → Upload).
4. Select **Runtime → Run all**. The notebook verifies file hashes and extracts the support files automatically. TensorFlow is required for the NN3 training cells; if Colab's environment changes, additional dependency adjustments may be needed.
5. Review all outputs and save a copy after a successful run. Colab session uploads are temporary, so re-upload the three files in a new session.

The notebook also supports running from a local directory containing these three input files, provided the required Python packages are installed. The prediction ZIP contains frozen forecasts so portfolio results use a consistent NN3 run.

## Reference

Avramov, D., Cheng, S., & Metzker, L. (2023). Machine Learning vs. Economic Restrictions: Evidence from Stock Return Predictability. *Management Science*, 69(5), 2587–2619. https://doi.org/10.1287/mnsc.2022.4449

The paper PDF is not redistributed in this repository.
