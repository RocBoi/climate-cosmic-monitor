name: Deploy App
on:
  push:
    branches:
      - main
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2

      - name: Set up Python
        uses: actions/setup-python@v2
        with:
          python-version: 3.9

      - name: Install Dependencies
        run: |
          pip install fastapi uvicorn requests
          npm install

      - name: Run Tests
        run: |
          pytest backend/tests
          npm test

      - name: Deploy Backend
        run: |
          echo "Deploying backend..."
          # Add cloud deployment script here

      - name: Deploy Frontend
        run: |
          echo "Deploying frontend..."
          # Add Netlify/Vercel deployment script here

 
