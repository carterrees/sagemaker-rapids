FROM rapidsai/rapidsai:cuda10.0-runtime-ubuntu16.04

RUN apt-get update && apt-get install -y --no-install-recommends build-essential 

RUN source activate rapids && pip install sagemaker-containers

# Copies the training code inside the container
COPY rapids-higgs.py /opt/ml/code/rapids-higgs.py

# Defines rapids-higgs.py as script entry point
ENV SAGEMAKER_PROGRAM rapids-higgs.py
