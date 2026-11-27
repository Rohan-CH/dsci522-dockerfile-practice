# dsci522-dockerfile-practice

Practice Docker image for UBC MDS **DSCI 522 (Data Science Workflows)**, Individual Assignment 2.

## What's inside
- Ubuntu 24.04 base
- Python 3.14, installed by [uv](https://docs.astral.sh/uv/)
- Two pinned packages: `cowsay==6.1` and `numpy==2.5.5`
- Packages live in `/opt/venv`, installed exactly as recorded in `uv.lock`

## Usage
Pull the image:

    docker pull rohanchakkadath/dsci522-dockerfile-practice:latest

Test that both packages load:

    docker run --rm rohanchakkadath/dsci522-dockerfile-practice:latest \
      uv run python -c "import cowsay, numpy; cowsay.cow(f'numpy says 1 + 2 + 3 = {numpy.sum([1, 2, 3])}')"

## Tags
- `latest`: most recent build
- `sha-<7 chars>`: build from a specific commit

## Source
Built and pushed automatically by GitHub Actions from
[Rohan-CH/dsci522-dockerfile-practice](https://github.com/Rohan-CH/dsci522-dockerfile-practice).
