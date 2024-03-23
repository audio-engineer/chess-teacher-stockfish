# ChessTeacher Stockfish

This containerized Python application is a REST API
built using FastAPI that serves [Stockfish](https://stockfishchess.org/) engine responses using
[py-stockfish/stockfish](https://github.com/py-stockfish/stockfish) as a wrapper.

The Stockfish software is licensed under GPL v3.
The full source code for the version of the software used in this project can be found here:
[official-stockfish/Stockfish](https://github.com/official-stockfish/Stockfish/tree/sf_16.1).

To build it, run:

```shell
docker build -t audio-engineer/chess-teacher-stockfish:latest .
```

## Local Development

```shell
docker compose up -d
```

```shell
docker exec -it chess-teacher-stockfish-python-1 /bin/sh
```

To run the linters in the `python` service container:

```shell
pylint app/ && flake8 && ruff check
```

```shell
docker compose down
```
