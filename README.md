[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

# Machine Learning for Commodity Price Forecasting

This project focuses on forecasting the prices of three essential agricultural commodities in West Java, Indonesia: **shallots (bawang merah)**, **garlic (bawang putih)**, and **bird’s eye chili (cabai rawit)**. The forecasting is based on time series data using advanced LSTM-based deep learning models, including STL decomposition and attention mechanisms.

---

## 📁 Project Structure

### 🔹 `Data/`
Contains the full dataset built from scratch using data scraping and processing from multiple trusted sources:
- Inflation data from BPS
- Weather data from BMKG
- Commodity production data from Open Data Jabar
- Price data from PIHPSN
- Public event (holiday) indicators from an open GitHub API

> See `Data/README.md` for full details.

---

### 🔹 `Notebooks/`
Includes several Jupyter Notebooks for experimentation with different model architectures:
- Vanilla LSTM
- DIA-LSTM (Data-Interactive Attention)
- STL-ATTLSTM (Seasonal-Trend decomposition with Attention LSTM)

Performance metrics and visualizations are provided for each model, and STL-ATTLSTM was selected as the final model for deployment.

> See `Notebooks/README.md` for model results and links to reference papers.

---

### 🔹 `Models/`
Contains pre-trained models saved in both `.h5` and Keras `SavedModel` formats, prepared for application deployment. Includes:
- Individual models per commodity (`bm_model`, `bp_model`, `cr_model`)
- A multi-output model (`multioutput_model`) for all commodities at once

> See `Models/README.md` for loading instructions and structure.

---

## 📌 Key Technologies Used
- TensorFlow / Keras
- STL decomposition
- Attention mechanism
- LSTM, DIA-LSTM, STL-ATTLSTM
- Pandas, NumPy, Matplotlib, Seaborn

---

## 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

[contributors-shield]: https://img.shields.io/github/contributors/LokaFresh-VegeNation/Machine-Learning.svg?style=for-the-badge
[contributors-url]: https://github.com/LokaFresh-VegeNation/Machine-Learning/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/LokaFresh-VegeNation/Machine-Learning.svg?style=for-the-badge
[forks-url]: https://github.com/LokaFresh-VegeNation/Machine-Learning/network/members
[stars-shield]: https://img.shields.io/github/stars/LokaFresh-VegeNation/Machine-Learning.svg?style=for-the-badge
[stars-url]: https://github.com/LokaFresh-VegeNation/Machine-Learning/stargazers
[issues-shield]: https://img.shields.io/github/issues/LokaFresh-VegeNation/Machine-Learning.svg?style=for-the-badge
[issues-url]: https://github.com/LokaFresh-VegeNation/Machine-Learning/issues
[license-shield]: https://img.shields.io/github/license/LokaFresh-VegeNation/Machine-Learning.svg?style=for-the-badge
[license-url]: https://github.com/LokaFresh-VegeNation/Machine-Learning/blob/main/LICENSE
