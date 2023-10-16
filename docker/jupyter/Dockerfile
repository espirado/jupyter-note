# Start from jupyter/minimal-notebook
FROM jupyter/minimal-notebook

# Copy requirements and install packages
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

# Create 'espirado' user with UID 1000 (typically the first user's UID on a Linux system)
USER root
RUN useradd -m -s /bin/bash -u 1000 espirado && \
    chown -R espirado:users /home/jovyan

# Switch to 'espirado' user
USER espirado
