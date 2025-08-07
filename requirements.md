renvisio/
├── renvisio/                    # Основной модуль (src-based layout)
│   ├── __init__.py
│   ├── config/                  # Конфигурации Hydra (.yaml)
│   │   ├── config.yaml
│   │   ├── paths.yaml
│   │   ├── model/
│   │   ├── data/
│   │   └── train/
│   ├── dataio/                  # Загрузка, парсинг, подготовка данных (DICOM, NIfTI)
│   │   ├── dicom_reader.py
│   │   ├── nifti_utils.py
│   │   └── dataset_splitter.py
│   ├── preprocessing/           # Предобработка: фильтры, нормализация, аугментации
│   │   ├── denoise.py
│   │   ├── resize.py
│   │   └── augmentation.py
│   ├── segmentation/            # Архитектуры и обучение сегментаторов (UNETR и др.)
│   │   ├── models/
│   │   │   └── unetr.py
│   │   ├── train.py
│   │   └── infer.py
│   ├── postprocessing/          # Морфология, фильтрация, объединение масок
│   │   └── clean_masks.py
│   ├── visualization/           # Визуализация срезов, 3D, overlay, VTK
│   │   ├── slice_plotter.py
│   │   └── vtk_viewer.py
│   ├── export/                  # Экспорт результатов (STL, JSON, отчёты)
│   │   ├── export_stl.py
│   │   └── report_generator.py
│   ├── evaluation/              # Метрики качества (Dice, IoU, Surface DSC)
│   │   ├── metrics.py
│   │   └── evaluate.py
│   ├── utils/                   # Общие вспомогательные функции и классы
│   │   ├── logger.py
│   │   └── timer.py
│   └── cli/                     # CLI-интерфейсы для запуска (Hydra + argparse)
│       ├── run_train.py
│       ├── run_infer.py
│       └── run_pipeline.py
├── notebooks/                   # Jupyter-ноутбуки для исследований и анализа
│   ├── data_exploration.ipynb
│   └── model_analysis.ipynb
├── tests/                       # Unit и integration тесты (pytest)
│   ├── test_dataio.py
│   ├── test_segmentation.py
│   └── conftest.py
├── scripts/                     # Bash-скрипты, утилиты, быстрые вызовы
│   ├── train_local.sh
│   └── export_model.sh
├── docker/                      # Dockerfile и docker-compose
│   ├── Dockerfile
│   └── docker-compose.yml
├── .env                         # Переменные окружения (не коммитить)
├── .gitignore
├── .pre-commit-config.yaml      # Преформаттеры (black, flake8, isort)
├── pyproject.toml               # Poetry/Build config
├── requirements.txt             # requirements.txt для fallback
├── README.md                    # Документация проекта
├── LICENSE
└── setup.cfg                    # Настройки линтеров (mypy, flake8 и пр.)
