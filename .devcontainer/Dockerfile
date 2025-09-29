# Use the official Python base image
FROM python:3.12

# Create a non-root user
RUN useradd -ms /bin/bash devuser
USER devuser
WORKDIR /uc_quantum

# Install basic dependencies
COPY requirements.txt /uc_quantum/requirements.txt
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

# Expose Jupyter port
EXPOSE 8888
