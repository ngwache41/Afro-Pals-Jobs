services:
  - type: web
    name: afro-personala-api
    env: python
    buildCommand: "pip install -r requirements.txt"
    startCommand: "uvicorn app.main:app --host 0.0.0.0 --port $PORT"
    plan: starter
    autoDeploy: true
    envVars:
      - key: MONGO_URI
        sync: false
      - key: JWT_SECRET
        sync: false
      - key: R2_ACCESS_KEY_ID
        sync: false
      - key: R2_SECRET_ACCESS_KEY
        sync: false
      - key: R2_BUCKET_NAME
        sync: false
      - key: R2_ENDPOINT
        sync: false
      - key: SMTP_HOST
        sync: false
      - key: SMTP_PORT
        sync: false
      - key: SMTP_USERNAME
        sync: false
      - key: SMTP_PASSWORD
        sync: false
      - key: DOMAIN
        value: "https://afropalsjobs.ru"
