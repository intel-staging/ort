# OpenVINO™ integration with PyTorch ONNX Runtime Dockerfiles for Ubuntu* 18.04 and Ubuntu* 20.04


We provide Dockerfiles for Ubuntu* 18.04 and Ubuntu* 20.04 which can be used to build runtime Docker* images for OpenVINO™ integration with PyTorch on CPU.
They contain all required runtime python packages, and shared libraries to support execution of a PyTorch Python app with the OpenVINO™ backend. By default, it hosts an Image Classification and Sequence Classification sample that demonstrate the performance benefits of using OpenVINO™ integration with PyTorch.

Build the docker image

	cd torch_ort_inference\docker\
    docker build -f .\Dockerfile.ort-infer-stable-torch1120-onnxruntime1120-openvino-ubuntu20.04 -t ort_infer_ubuntu20 .

To run on **CPU** backend:

	docker run -it --rm \
		   -v <path to demos directory>:/home/ \
		   ort_infer_ubuntu20

---
\* Other names and brands may be claimed as the property of others.