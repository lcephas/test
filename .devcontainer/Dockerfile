FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

RUN pip install -U "huggingface_hub[cli]" \
    && huggingface-cli download microsoft/Phi-3-mini-4k-instruct-onnx

FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye
COPY --from=0 ~/.cache/huggingface/hub/models--microsoft--Phi-3-mini-4k-instruct-onnx/snapshots/a484edc37e8f7b425a5aefa25e35905769963681/cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4 /app/cpu_and_mobile/cpu-int4-rtn-block-32-acc-level-4
