# AI Olympiad Template — Computer Vision (PyTorch)

Готовый шаблон для олимпиад по ИИ / соревнований (ML, CV, NLP).
- 🧱 Структура: `src/`, `configs/`, `notebooks/`, `scripts/`, `tests/`
- ⚙️ Запуск: конфиги в YAML
- 🧪 CI: GitHub Actions (lint + tests)
- 🧹 pre-commit: black, isort, flake8
- 🐳 Docker (по желанию)

## Быстрый старт

```bash
# 1) создать окружение
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -U pip
pip install -r requirements.txt
pip install -e .

# 2) минимальный прогон
python scripts/train.py --config configs/default.yaml
python scripts/evaluate.py --config configs/default.yaml
python scripts/infer.py --config configs/default.yaml --input path/to/sample.csv
```

## Структура
```
.
├── configs/
│   └── default.yaml
├── data/
│   ├── .gitkeep
│   └── README_DATA.md
├── notebooks/
│   └── EDA.ipynb
├── scripts/
│   ├── train.py
│   ├── evaluate.py
│   └── infer.py
├── src/aoi_cv/
│   ├── __init__.py
│   ├── data.py
│   ├── models.py
│   ├── utils.py
│   └── metrics.py
├── tests/
│   └── test_smoke.py
├── .gitignore
├── .pre-commit-config.yaml
├── .github/workflows/ci.yml
├── LICENSE
├── pyproject.toml
├── setup.cfg
├── requirements.txt
└── README.md
```

## Как загрузить в GitHub
```bash
git init
git add .
git commit -m "Init: AI Olympiad Template — Computer Vision (PyTorch)"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```
