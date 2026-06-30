DIR = .
FILE = main.py

all: lint
	uv run $(DIR)/$(FILE)

format:
	uv run black $(DIR)

lint:
	uv run flake8 $(DIR)

clean:
	rm -rf .venv uv.lock
	find . -name "__pycache__" -exec rm -rf {} +

.PHONY: all format lint clean
