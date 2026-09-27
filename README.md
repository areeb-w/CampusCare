# CampusCare 🏫💳

**Smarter, safer, more connected school canteens.**

CampusCare brings together health monitoring, a cashless rewards wallet, and nurse-facing health records into one integrated platform — helping schools catch health risks early, encourage academic performance, and keep allergy-prone students safe at every meal.

---

## ✨ Features

### 🩺 Triage Bot
An AI-driven early-warning system for student health.
- Tracks each student's canteen transaction history
- Cross-references purchases against food metadata (glycemic index, nutritional values)
- Predicts potential health risks based on eating patterns
- Notifies students to log symptoms when a risk is flagged
- Issues checkup vouchers redeemable at the school infirmary for a nurse diagnosis

### 💰 Mock Wallet
A cashless, points-based payment system for the canteen.
- Digital wallet balance funded by parents
- Academic performance converts into micro-scholarships, credited as reward points
- Contactless payments and digital menu at the canteen counter

### 🪪 Student Health Passport + Nurse Dashboard
A shared source of truth for student health data.
- Students and parents input key health info: blood group, allergies, existing medications, etc.
- Nurses access this data in real time through a dedicated dashboard
- Automatically flags allergens at the point of payment, integrated directly into the canteen app

---

## 🧩 How It Fits Together

```
Student/Parent ──> Health Passport ──> Nurse Dashboard
      │                                     ▲
      ▼                                     │
  Mock Wallet ───> Canteen Payment ───> Allergen Check
      │                                     │
      ▼                                     ▼
Transaction History ──> Triage Bot ──> Risk Alert ──> Checkup Voucher
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/areeb-w/campuscare.git
cd campuscare

# Install dependencies
# (update this once your package manager / stack is finalized)

# Run the app
# (add your start command here)
```

> ⚙️ Setup instructions are placeholders — update this section once the tech stack and build process are finalized.

---

## 📌 Roadmap

- [ ] Finalize risk-prediction model for the Triage Bot
- [ ] Parent-facing wallet top-up flow
- [ ] Nurse Dashboard allergen alert integration
- [ ] Academic-performance-to-reward-points pipeline

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open a pull request or start a discussion.

---

## 📄 License

Specify a license (e.g., MIT) here.
