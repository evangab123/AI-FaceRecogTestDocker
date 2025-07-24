# Face Recognition App with FastAPI + Docker (w600k\_r50.onnx)

A simple facial recognition system using FastAPI and FaceNet. Easily deployable with Docker.

---

## Features

* Upload and store face embeddings
* Real-time face recognition
* Delete face data
* RESTful API using FastAPI
* ONNX runtime with `w600k_r50.onnx`
* Dockerized for easy deployment

---

## Requirements

* Docker
* Docker Desktop

---

## Endpoints

* `GET /api/face`
  Get a list of all faces in the database.

* `POST /api/face/register`
  Register a new face by adding its facial features to the database.

* `POST /api/face/recognize`
  Recognize a face by matching its facial features against the database and returning the matched face if found.

* `DELETE /api/face/{id}`
  Delete a face from the database by its ID.

---

## How to Run (Demo/Testing)

1. Open VS Code or WSL Ubuntu Terminal with Docker installed.
2. Run the Docker container:

   ```bash
   docker-compose up
   ```
3. Open your browser and go to [http://localhost:8000/docs](http://localhost:8000/docs) to access the FastAPI Swagger UI.
4. To register a face:

   * Click on the `/api/face/register` section.
   * Click the "Try it out" button.
   * Upload your image and click "Execute".
5. To recognize a face:

   * Click on the `/api/face/recognize` section.
   * Click the "Try it out" button.
   * Upload your image and click "Execute".
6. To get a list of all registered faces:

   * Click on the `/api/face` section and click "Try it out" > "Execute".
7. To delete a face:

   * Click on the `/api/face/{id}` section.
   * Click the "Try it out" button.
   * Input the face ID from step 7 and click "Execute".


---
## 📦 Source Code

Source code are there [`source-code.zip`](./source-code.zip), you can use and test it without search inside docker image, source code can use docker locally make sure you download docker before or docker dekstop 

---


## Notes

To ensure accurate and reliable face recognition results, please follow these image guidelines:

- ✅ Use a **clear, front-facing image** of the person's face.
- ✅ Ensure the **face is centered** in the image and fully visible.
- ✅ Use **good lighting** (avoid shadows or overexposure).
- ✅ Upload images with **moderate distance** — not too close, not too far.
- ✅ Only **one face per image** is recommended.

Avoid:

- ❌ Blurry or low-resolution images
- ❌ Faces with sunglasses, heavy makeup, or masks
- ❌ Side profiles or extreme angles
- ❌ Group photos with multiple faces

Following these suggestions will help the model generate better embeddings and improve recognition accuracy.

---

Model: w600k_r50.onnx
Source: [Hugging Face - maze/faceX](https://huggingface.co/maze/faceX/resolve/main/w600k_r50.onnx)

Make sure the model is placed in the correct path (app/models/w600k_r50.onnx) before running the app.

