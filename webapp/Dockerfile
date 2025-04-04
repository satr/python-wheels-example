FROM docker.io/python:3.9.21-alpine3.21

# Copy wheel file directly into container
COPY dist/*.whl /tmp/

# Install the wheel
RUN pip install --upgrade pip
RUN pip install /tmp/*.whl

EXPOSE 8000

# Run app
CMD ["uvicorn", "simple_webapp.main:app", "--host", "0.0.0.0", "--port", "8000"]
