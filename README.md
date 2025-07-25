# Forecasting-Air-Quality-In-Africa
# 🌍 Air Quality Forecasting in Nairobi 🇰🇪 & Dar es Salaam 🇹🇿

This project was completed as part of the **Applied Data Science Lab by WorldQuant University**. It focuses on **time series forecasting** of PM2.5 pollution levels across two major African cities — **Nairobi** and **Dar es Salaam** — using real-world data from **OpenAfrica**.

We developed, tuned, and validated models to predict hourly air pollution levels, while applying best practices in time series modeling, diagnostics (ACF/PACF), and walk-forward validation.

---

## 🧠 Project Overview

In this end-to-end data science project, we:
- Connected to a **MongoDB database** hosting air sensor data
- Cleaned and resampled the data to hourly PM2.5 readings
- Built and compared several models: **Linear Regression**, **AutoReg**, and **ARIMA**
- Tuned hyperparameters (lags, `p`, and `q`)
- Validated model performance using **walk-forward prediction**
- Evaluated results using plots, residuals, and correlation diagnostics

This project offers insights into modeling **time-dependent data for public health**, and the techniques here apply directly to domains like **finance**, **NLP**, and **environmental monitoring**.

---

## 🗃️ Data Source

The dataset comes from [OpenAfrica.net](https://africaopendata.org/), one of the largest open data platforms in Africa. We used collections for:
- **Nairobi, Kenya**
- **Dar es Salaam, Tanzania**

Data is stored in a **MongoDB database**, accessible and queried using `pymongo`.

---

## 💻 Technologies Used

- **Languages**: Python
- **Libraries**:  
  - Data: `pandas`, `numpy`, `gzip`, `json`, `pickle`
  - Plotting: `matplotlib`, `seaborn`, `plotly.express`
  - Modeling: `statsmodels`, `scikit-learn`
  - Database: `pymongo`
- **Environment**: Jupyter Notebook

---

## 🔧 Project Structure

This project is organized into 4 main lessons and a final assignment:

| Notebook                                            | Description                                                                |
|----------                                           |-------------                                                               |
| `031-data-wrangling-with-mongodb.ipynb`             | Connects to MongoDB and performs initial wrangling                         |
| `032-linear-regression-with-time-series-data.ipynb` | Builds baseline linear regression model                                    |
| `033-autoregressive-models.ipynb`                   | Builds and evaluates AR models                                             |
| `034-arma-models-and-hyperparameter-tuning.ipynb`   | Implements ARMA models with lag tuning                                     |
| `assignment.ipynb`                                  |  Final walk-forward validation and model evaluation for Dar Es Salaam city |

---

## 🔍 Time Series Diagnostics (ACF & PACF)

To tune and evaluate time series models, we used:

- **ACF (Autocorrelation Function)**: Measures how a time series is correlated with its own past values. Useful to determine the number of **MA (q)** lags.
- **PACF (Partial Autocorrelation Function)**: Measures the direct effect of past lags, removing indirect influences. Helps determine the number of **AR (p)** lags.
- After model training, we re-applied **ACF** on residuals to confirm randomness (white noise). This validates model fit.

---

## 📈 Visualizations and Analysis

We used various plots to analyze data and model performance:

- 📊 **Line plots**: Showed PM2.5 trends over time
- 📉 **7-day rolling averages**: Smoothed short-term spikes
- 🔁 **ACF & PACF plots**: Guided model structure
- 📊 **Histogram of residuals**: Evaluated prediction errors
- 🔍 **Walk-forward validation plots**: Compared actual vs. predicted PM2.5 levels

---

## ⚙️ Modeling Pipeline

1. **Data Wrangling**
   - Localized timestamps (Africa/Nairobi and Africa/Dar_es_Salaam)
   - Removed PM2.5 outliers above 100
   - Resampled to hourly mean and forward-filled missing values

2. **Baseline Modeling**
   - Linear regression using time-based features

3. **Advanced Modeling**
   - AutoReg models (AR)
   - ARMA models with tuned p/q values
   - Lag search (1–30) for best performance (based on MAE)

4. **Evaluation**
   - Mean Absolute Error (MAE)
   - Residuals analysis
   - ACF of residuals to confirm model adequacy

5. **Walk-Forward Validation**
   - Simulated real-time forecasting
   - Compared predictions with true values
   - Plotted results using `plotly.express`

---

## 🧰 Skills Gained

✅ Querying and working with **MongoDB** databases  
✅ Handling **time-indexed data** and resampling  
✅ Building and evaluating **autoregressive (AR) and ARMA** models  
✅ Using **ACF/PACF** for diagnostics and model tuning  
✅ Performing **walk-forward validation**  
✅ Communicating results with rich, interpretable visualizations  
✅ Working in a **production-style environment** using serialization and testing

---

## 📂 Repository Contents
- Additional lesson notebooks: Practice and graded tasks
- `assignment.ipynb`: Full modeling, diagnostics, and final plots
- `README.md`: Project summary and context

---

## 🎯 Key Insight

In forecasting tasks — especially in public health and environmental science — going beyond accuracy to include residual checks, correlation diagnostics, and careful model validation is **mission-critical**.

This project bridged theory and real-world application, preparing us for similar challenges in **finance**, **NLP**, or **IoT sensor analytics**.

---

## 📎 Related

This project was built as part of the **WorldQuant University Applied Data Science Lab**.  
For more information: [https://www.wqu.edu](https://www.wqu.edu)  
GitHub Repo: [https://github.com/ashraf635sakr/air-quality-in-nairobi]([https://github.com/ashraf635sakr/air-quality-in-nairobi](https://github.com/Houssam-123-ship-it/Forecasting-Air-Quality-In-Africa)

---

## 🙏 Acknowledgments

Thanks to **WorldQuant University** for designing this practical and hands-on project experience. Special appreciation to the OpenAfrica platform for open environmental data access.

---

## 📬 Contact

If you'd like to discuss this project, forecasting methods, or public health applications in data science — feel free to connect via [LinkedIn](https://www.linkedin.com/in/houssam-kichchou-a184a8271/).

