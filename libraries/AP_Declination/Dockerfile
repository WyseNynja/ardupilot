# Usage:
#   docker build . -t ap_declination
#   docker run --rm -it -v $(pwd):/AP_Declination -w /AP_Declination ap_declination ./generate/generate.py
#   docker run --rm -it -v $(pwd):/AP_Declination -w /AP_Declination ap_declination bash

FROM python:3.6

RUN pip install --no-cache-dir numpy

RUN { set -eux; \
    \
    apt-get update; \
    apt-get install --no-install-recommends -y gfortran; \
    rm -rf /var/lib/apt/lists/*; \
}

RUN pip install --no-cache-dir "pyigrf12>=1.3"
