# laptop-price-predictor

## 🛠 Tech Stack
- **Languages:** Python
- **ML & Data:** scikit-learn, pandas, NumPy
- **MLOps:** MLflow, DVC, GitHub Actions, Docker, FastAPI
- **Cloud / Storage:** AWS EC2, S3
- **Monitoring:** Prometheus, Grafana (optional)

## 📈 Results
- Model: Random Forest / Gradient Boosting (tuned)
- Example metric: **MAE = ₹X,XXX** (replace with your measured value)
- Inference latency: **~Y ms** (containerized)

## 🔁 How to run (dev)
```bash
# clone
git clone https://github.com/ABHISHEKKHOPADE/DEEP_LEARNING.git
cd DEEP_LEARNING/laptop-price-predictor

# install
pip install -r requirements.txt

# reproduce training (DVC + MLflow)
dvc pull                # fetch data & models
python src/train.py     # trains and logs run to MLflow

# serve model with FastAPI
docker build -t laptop-price-api .
docker run -p 8000:8000 laptop-price-api
# then: curl http://localhost:8000/predict -d '{"ram":8, "cpu":"i5", ...}'
