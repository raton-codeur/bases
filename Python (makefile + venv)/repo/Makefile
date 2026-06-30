DIR = .
FILE = main.py

all : .venv lint
	.venv/bin/python $(DIR)/$(FILE)

format : .venv
	.venv/bin/black $(DIR)

lint : .venv
	.venv/bin/flake8 $(DIR)

.venv : requirements.txt
	python3 -m venv .venv
	.venv/bin/pip install -r requirements.txt

clean :
	rm -rf .venv
	find . -name "__pycache__" -exec rm -rf {} +

.PHONY : all format lint clean
