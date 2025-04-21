# Notebooks Documentation

This folder contains various Jupyter Notebooks from our LSTM-based modeling experiments. The models tested include:

- LSTM
- DIA-LSTM
- STL-ATTLSTM

Each notebook explores different architectures and evaluation metrics to determine the most effective model for our commodity price forecasting task.

---

## 🧠 LSTM

**Long Short-Term Memory (LSTM)** is a type of recurrent neural network (RNN) capable of learning long-term dependencies. It is widely used for time series forecasting due to its ability to handle vanishing gradient issues.

🔗 Reference Paper: [Prediksi Harga Cabai menggunakan Metode Long-Short Term Memory (Case Study : Kota Malang)](https://j-ptiik.ub.ac.id/index.php/j-ptiik/article/view/12406)

**Performance:**
- **MAE**: 14,706.54  
- **RMSE**: 21,840.86  
- **MAPE**: 27.11%  
- **R-squared**: -8.871

📊 _See included visualizations._

![LSTM Plot](https://drive.google.com/uc?export=view&id=1bzpizcAs0NaYx3IKCLMQBkHg9OIDnvk9)

---

## ⚙️ DIA-LSTM

**DIA-LSTM (Data-Interactive Attention LSTM)** introduces attention mechanisms and external data interactions into the LSTM structure, improving its ability to capture temporal dependencies and external factors.

🔗 Reference Paper: [Forecasting Agricultural Commodity Prices Using Dual Input Attention LSTM](https://www.mdpi.com/2077-0472/12/2/256)

**Performance:**
- **MAE**: 4,824.58  
- **RMSE**: 9,301.33  
- **MAPE**: 9.62%  
- **R-squared**: 0.657

📊 _See included visualizations._

![DIA-LSTM Plot](https://drive.google.com/uc?export=view&id=1J4INv50nj_aKCKqbZ-k1tZp-Hx3qB7Wm)

---

## 📈 STL-ATTLSTM

**STL-ATTLSTM (Seasonal-Trend decomposition using Loess with Attention LSTM)** combines STL decomposition with an attention-enhanced LSTM, allowing the model to isolate and better learn trend and seasonal patterns before prediction.

🔗 Reference Paper: [STL-ATTLSTM: Vegetable Price Forecasting Using STL and Attention Mechanism-Based LSTM](https://www.mdpi.com/2077-0472/10/12/612)

**Performance:**

### 🧅 Bawang Merah
- **MAE**: 393.75  
- **RMSE**: 596.64  
- **MAPE**: 1.07%  
- **R²**: 0.995

### 🧄 Bawang Putih
- **MAE**: 200.19  
- **RMSE**: 318.43  
- **MAPE**: 0.56%  
- **R²**: 0.998

### 🌶️ Cabai Rawit
- **MAE**: 1,047.07  
- **RMSE**: 1,375.50  
- **MAPE**: 1.99%  
- **R²**: 0.996

📊 _See included visualizations._

![STL-ATTLSTM Plot](https://drive.google.com/uc?export=view&id=1ceic_rVNBGs2A3KBUnYg2fa_jk4Z3lwU)

---

## ✅ Model Selection

Based on the evaluation metrics, **STL-ATTLSTM** outperformed other models in terms of accuracy and generalization. It was tested in two approaches:

1. One model per commodity  
2. A single multi-output model for all three commodities

Both approaches yielded similar performance, indicating that either setup is viable. We decided to proceed with **STL-ATTLSTM** as the primary model for this project.
