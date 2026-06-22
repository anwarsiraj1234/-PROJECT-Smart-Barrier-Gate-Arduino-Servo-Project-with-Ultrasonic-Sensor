# 🚧 Smart Barrier Gate System Using Arduino & Ultrasonic Sensor

### 👨‍💻 Made By: Sir Anwar Siraj | DS & AI Robotics

---

## 📖 Project Description

The **Smart Barrier Gate System** is an Arduino-based automation project that uses an **HC-SR04 Ultrasonic Sensor** and an **SG90 Servo Motor** to create an automatic barrier gate.

When a vehicle or object comes within **30 cm** of the sensor, the servo motor automatically raises the barrier gate. After a short delay, the gate closes automatically.

This project is ideal for:

* Smart Parking Systems
* Automatic Toll Gates
* Security Checkpoints
* STEM & Robotics Education
* Arduino Learning Projects

---

# 🛠 Components Required

| Component                 | Quantity    |
| ------------------------- | ----------- |
| Arduino Uno/Nano          | 1           |
| HC-SR04 Ultrasonic Sensor | 1           |
| SG90/MG90 Servo Motor     | 1           |
| Jumper Wires              | As Required |
| USB Cable / Power Supply  | 1           |

---

# 🔌 Circuit Connections

## HC-SR04 Ultrasonic Sensor

| HC-SR04 Pin | Arduino Pin |
| ----------- | ----------- |
| VCC         | 5V          |
| GND         | GND         |
| TRIG        | D6          |
| ECHO        | D7          |

## Servo Motor

| Servo Wire             | Arduino Pin |
| ---------------------- | ----------- |
| Red (VCC)              | 5V          |
| Brown/Black (GND)      | GND         |
| Orange/Yellow (Signal) | D9          |

---

# 📊 Circuit Diagram

```text
                 HC-SR04
             +-------------+
             | VCC -> 5V   |
             | GND -> GND  |
             | TRIG-> D6   |
             | ECHO-> D7   |
             +-------------+
                     |
                     |
        +-------------------------+
        |      Arduino UNO        |
        |                         |
        | D6  <--- TRIG           |
        | D7  ---> ECHO           |
        | D9  ---> Servo Signal   |
        | 5V  ---> VCC            |
        | GND ---> GND            |
        +-------------------------+
                     |
                     |
              +-------------+
              | SG90 Servo  |
              | VCC -> 5V   |
              | GND -> GND  |
              | SIG -> D9   |
              +-------------+
```

---

# ⚙️ Working Principle

### Step 1: Distance Measurement

The HC-SR04 ultrasonic sensor continuously measures the distance between the sensor and an approaching object.

### Step 2: Vehicle Detection

When the measured distance becomes less than **30 cm**, the Arduino detects the presence of a vehicle.

### Step 3: Gate Opening

The servo motor rotates from **0° to 120°**, opening the barrier gate.

### Step 4: Gate Open Delay

The gate remains open for **3 seconds** to allow the vehicle to pass.

### Step 5: Gate Closing

The servo motor rotates back from **120° to 0°**, closing the barrier gate.

### Step 6: Ready for Next Vehicle

The system waits for **5 seconds** before checking for the next vehicle.

---

# 🔄 System Flow

```text
Start
  │
  ▼
Measure Distance
  │
  ▼
Distance < 30 cm ?
  │
 ┌┴───────────┐
 │            │
No           Yes
 │            │
 ▼            ▼
Continue   Open Gate
Scanning      │
              ▼
      Wait 3 Seconds
              │
              ▼
         Close Gate
              │
              ▼
       Wait 5 Seconds
              │
              ▼
      Measure Again
```

---

# 📷 Physical Components

### 1️⃣ Arduino Uno

Main controller that processes sensor data and controls the servo motor.

### 2️⃣ HC-SR04 Ultrasonic Sensor

Measures the distance between the sensor and approaching vehicles.

### 3️⃣ SG90 Servo Motor

Acts as the barrier gate mechanism by rotating to open and close the gate.

### 4️⃣ Jumper Wires

Used for electrical connections between components.

### 5️⃣ Power Supply

Provides 5V power to the Arduino and connected components.

---

# 🎯 Applications

* Smart Parking Management
* Automated Toll Collection Systems
* Vehicle Access Control
* Security Barrier Gates
* School STEM Projects
* Robotics Competitions
* Engineering Demonstrations

---

# ✅ Features

* Automatic Vehicle Detection
* Contactless Operation
* Low Cost
* Easy to Build
* Beginner Friendly
* Arduino Compatible
* Real-Time Distance Monitoring

---

# 📚 Educational Concepts

This project helps students learn:

* Arduino Programming
* Servo Motor Control
* Ultrasonic Sensor Interfacing
* Distance Measurement
* Automation Systems
* Smart Transportation Technology
* Robotics & Embedded Systems

---

## 👨‍🏫 Author

**Sir Anwar Siraj**
**DS & AI Robotics**

🚀 Build • Learn • Innovate
