# 🌍 AtlasID: Local-First Identity Wallet

AtlasID is a decentralized, offline-first identity system designed to facilitate humanitarian aid and secure credentialing in regions with limited connectivity. By moving trust to the "edge," AtlasID allows for the verification of IDs and vouchers without a real-time internet connection.

---

## 🛠️ Project Architecture

The project is structured as a monorepo, divided into three core pillars:

- **`/frontend` (Person 1):** A React Native mobile wallet for storing credentials and generating offline QR codes.
- **`/backend` (Person 2):** A Node.js & PostgreSQL engine that manages the identity registry and aid entitlements.
- **`Security Layer` (Person 3):** Ed25519 cryptographic signing and verification logic integrated across both platforms.

---

## 🚀 Getting Started

### ⚙️ Backend Setup
1. Navigate to the directory: `cd backend`
2. Install dependencies: `npm install`
3. Configure environment: Create a `.env` file (see `.env.example`).
4. Run migrations: `psql -f schema.sql`
5. Start development server: `npm run dev`

### 📱 Frontend Setup
1. Navigate to the directory: `cd frontend`
2. Install dependencies: `npm install`
3. Start the metro bundler: `npx react-native start`
4. Run on device/emulator: `npx react-native run-android` (or `run-ios`)

---

## 🧪 Testing & CI/CD

We use a comprehensive CI/CD pipeline powered by **GitHub Actions** to ensure system stability.

- **Automated Tests:** Run `npm test` inside the `/backend` folder to execute the Jest integration suite.
- **Pipeline:** Every push to `main` or `develop` triggers the **AtlasID Integrated Pipeline**, which validates:
  - Backend API logic (via Jest & PostgreSQL service container).
  - Frontend code quality (via ESLint).
  - Production Docker builds.

---

## 📑 Core Features
- ✅ **Offline Trust Protocol:** Verify credentials via QR codes with zero server pings.
- ✅ **Self-Sovereign Identity:** Users own their keys and data locally on their device.
- ✅ **Aid Entitlements:** NGO-backed vouchers for food, medicine, and services.
- ✅ **W3C Standards (Roadmap):** Aligning with global Verifiable Credentials standards.

---

## 📜 License
This project is developed as part of the AtlasID Digital Public Infrastructure initiative.
