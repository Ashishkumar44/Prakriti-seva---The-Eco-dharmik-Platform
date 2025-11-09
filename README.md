
  # Prakriti Seva - The Eco Dharmik Platform

  This repository contains the code for "Prakriti Seva - The Eco Dharmik Platform." It was implemented based on a Figma design; the reference file (for attribution) is: https://www.figma.com/design/rZMN081pMcTusgZiRXBQdJ/Prakriti-Seva-Website-Design.

  ## Running the code

  Run `npm i` to install the dependencies.

  Run `npm run dev` to start the development server.

  ## Backend (optional)

  This project includes a small Express backend scaffold in `server/` to add product APIs and a Stripe-ready checkout endpoint.

  Quick start (in a new terminal):

  ```powershell
  cd c:\Users\Ashish Sahay\OneDrive\Desktop\seva\server
  npm install
  cp .env.example .env
  # edit .env to set STRIPE_SECRET_KEY if you want live Stripe
  npm start
  ```

  API endpoints provided by the scaffold:
  - `GET /api/products` - list products
  - `POST /api/products` - add a product (payload: { title, price, image?, description? })
  - `POST /api/checkout` - create an order and (if Stripe key is set) a Stripe Checkout Session

  Notes:
  - The backend uses a simple file-based JSON database (`server/db.json`) to keep demo product and order data. It's not intended for production.
  - To enable real payments, set `STRIPE_SECRET_KEY` in `server/.env` and configure `SUCCESS_URL`/`CANCEL_URL`.
  