# Face Extractor API

This is a simple and lightweight API I built using FastAPI and OpenCV. It takes an image of an ID or passport, detects the face, and gives you either:

- A base64 string of the cropped portrait
- Or the actual image (PNG format)

I made this for a case study project where the goal was to showcase end-to-end deployment, AI logic, and API design in a clean and testable way.

---

## How it works

There are two main endpoints:

### POST `/extract-portrait/`
- Upload a photo of an ID/passport
- You get a base64-encoded portrait in return
- Useful for saving as text or embedding in apps

### POST `/extract-portrait/image`
- Same input as above
- But instead, you get the actual cropped image back (as PNG)

---

## How to run it locally

```bash
uvicorn main:app --reload
```

Make sure you’ve installed the requirements:

```bash
pip install -r requirements.txt
```

---

## Why I made it

I wanted to show I could:
- Build a real-world ML-based API
- Handle image processing with OpenCV
- Deploy it online (I used Render)
- Document everything properly

---

## Swagger UI

You can test everything here:
`/docs`

If you run into any issues, the API returns friendly errors like:
- “No face found”
- “Invalid image file”
