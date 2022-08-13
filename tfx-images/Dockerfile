ARG TFX_VERSION = "1.9.0"
FROM tensorflow/tfx:${TFX_VERSION}
COPY requirements.txt .
RUN pip install -r requirements.txt --no-install-requirement
RUN rm requirements.txt

WORKDIR /tfx/src