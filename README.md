# DC-DC-open-loop-Buck-convertor
# 🔋 Closed-Loop Buck Converter

A **Closed-Loop Buck Converter** designed and implemented as part of the **Industrial Electronics & Process Control Lab** at the Department of Electronics & Instrumentation Engineering.

The project demonstrates the conversion of a higher DC voltage into a regulated lower DC voltage using a buck converter with **PWM-based switching and feedback control**.

---

## 📌 Project Overview

A buck converter is a **DC-DC power converter** used to step down a higher input voltage to a lower output voltage efficiently.

In an open-loop buck converter, the output voltage mainly depends on the input voltage and switching duty cycle. Therefore, changes in input voltage or load can cause fluctuations in the output voltage.

To overcome this limitation, this project implements a **closed-loop feedback mechanism**. The output voltage is monitored and compared with a reference voltage, and the control system adjusts the switching signal to maintain a stable output.

The project uses an **NE555 timer** to generate the PWM signal, with a potentiometer used for duty-cycle/reference adjustment.

---

## 🎯 Objectives

* Design and implement a DC-DC buck converter.
* Step down a higher DC input voltage to a lower DC output voltage.
* Generate PWM using an **NE555 timer**.
* Control the switching operation of the converter.
* Implement feedback-based voltage regulation.
* Reduce output voltage fluctuations caused by changes in input or load conditions.
* Understand the practical implementation of switching power converters.

---

## ⚙️ Working Principle

The basic operating sequence of the converter is:

```text
DC Input
   ↓
NE555 Timer
   ↓
PWM Generation
   ↓
MOSFET Switching
   ↓
Inductor Energy Storage
   ↓
Energy Release to Load
   ↓
Output Capacitor Filtering
   ↓
Regulated DC Output
```

The **NE555 timer** generates the PWM signal. The duty cycle can be adjusted using the potentiometer, which controls the switching operation of the MOSFET.

The inductor stores energy during the switching cycle and releases it to the load when the switch is turned off. The capacitor filters the resulting waveform to obtain a smoother DC output.

The feedback mechanism continuously monitors the output and helps maintain the desired voltage.

---

## 🧩 Block Diagram

### Converter Flow

```text
┌──────────────┐
│   DC INPUT   │
└──────┬───────┘
       ↓
┌──────────────┐
│  NE555 TIMER │
└──────┬───────┘
       ↓
┌──────────────┐
│ PWM SIGNAL   │
│ GENERATION   │
└──────┬───────┘
       ↓
┌──────────────┐
│    MOSFET    │
│   SWITCHING  │
└──────┬───────┘
       ↓
┌──────────────┐
│   INDUCTOR   │
│ ENERGY STORE │
└──────┬───────┘
       ↓
┌──────────────┐
│    OUTPUT    │
│   FILTER     │
└──────┬───────┘
       ↓
┌──────────────┐
│  DC OUTPUT   │
└──────────────┘
```

---

## 🔌 Circuit Components

| Component              | Specification | Purpose                         |
| ---------------------- | ------------- | ------------------------------- |
| Inductor               | 100 µH Axial  | Energy storage                  |
| Electrolytic Capacitor | 100 µF        | Output filtering                |
| Electrolytic Capacitor | 10 µF         | Loop compensation/filtering     |
| Ceramic Capacitor      | 0.01 µF       | High-frequency noise filtering  |
| Potentiometer          | 10 kΩ, 3-pin  | Reference/duty-cycle adjustment |
| Resistor               | 33 kΩ, ¼ W    | Feedback network                |
| Resistor               | 51 kΩ, ¼ W    | Feedback divider                |
| Resistor               | [VALUE]       | Biasing                         |
| Resistor               | 470 Ω, ¼ W    | Current limiting                |
| Breadboard             | MB102         | Circuit prototyping             |
| PCB                    | 8 cm × 6 cm   | Final circuit implementation    |
| Timer IC               | NE555         | PWM generation                  |
| Jumper Wires           | 23 AWG        | Circuit interconnections        |

The component list is based on the project document. The value of one biasing resistor is not clearly specified in the source document, so it is intentionally left as **[VALUE]** rather than assumed.

---

## 🖼️ Project Images

### 1. Physical Circuit

> **Add your physical circuit photograph here**

```markdown
![Physical Circuit](# 🔋 Closed-Loop Buck Converter

A **Closed-Loop Buck Converter** designed and implemented as part of the **Industrial Electronics & Process Control Lab** at the Department of Electronics & Instrumentation Engineering.

The project demonstrates the conversion of a higher DC voltage into a regulated lower DC voltage using a buck converter with **PWM-based switching and feedback control**.

---

## 📌 Project Overview

A buck converter is a **DC-DC power converter** used to step down a higher input voltage to a lower output voltage efficiently.

In an open-loop buck converter, the output voltage mainly depends on the input voltage and switching duty cycle. Therefore, changes in input voltage or load can cause fluctuations in the output voltage.

To overcome this limitation, this project implements a **closed-loop feedback mechanism**. The output voltage is monitored and compared with a reference voltage, and the control system adjusts the switching signal to maintain a stable output.

The project uses an **NE555 timer** to generate the PWM signal, with a potentiometer used for duty-cycle/reference adjustment.

---

## 🎯 Objectives

* Design and implement a DC-DC buck converter.
* Step down a higher DC input voltage to a lower DC output voltage.
* Generate PWM using an **NE555 timer**.
* Control the switching operation of the converter.
* Implement feedback-based voltage regulation.
* Reduce output voltage fluctuations caused by changes in input or load conditions.
* Understand the practical implementation of switching power converters.

---

## ⚙️ Working Principle

The basic operating sequence of the converter is:

```text
DC Input
   ↓
NE555 Timer
   ↓
PWM Generation
   ↓
MOSFET Switching
   ↓
Inductor Energy Storage
   ↓
Energy Release to Load
   ↓
Output Capacitor Filtering
   ↓
Regulated DC Output
```

The **NE555 timer** generates the PWM signal. The duty cycle can be adjusted using the potentiometer, which controls the switching operation of the MOSFET.

The inductor stores energy during the switching cycle and releases it to the load when the switch is turned off. The capacitor filters the resulting waveform to obtain a smoother DC output.

The feedback mechanism continuously monitors the output and helps maintain the desired voltage.

---

## 🧩 Block Diagram

### Converter Flow

```text
┌──────────────┐
│   DC INPUT   │
└──────┬───────┘
       ↓
┌──────────────┐
│  NE555 TIMER │
└──────┬───────┘
       ↓
┌──────────────┐
│ PWM SIGNAL   │
│ GENERATION   │
└──────┬───────┘
       ↓
┌──────────────┐
│    MOSFET    │
│   SWITCHING  │
└──────┬───────┘
       ↓
┌──────────────┐
│   INDUCTOR   │
│ ENERGY STORE │
└──────┬───────┘
       ↓
┌──────────────┐
│    OUTPUT    │
│   FILTER     │
└──────┬───────┘
       ↓
┌──────────────┐
│  DC OUTPUT   │
└──────────────┘
```

---

## 🔌 Circuit Components

| Component              | Specification | Purpose                         |
| ---------------------- | ------------- | ------------------------------- |
| Inductor               | 100 µH Axial  | Energy storage                  |
| Electrolytic Capacitor | 100 µF        | Output filtering                |
| Electrolytic Capacitor | 10 µF         | Loop compensation/filtering     |
| Ceramic Capacitor      | 0.01 µF       | High-frequency noise filtering  |
| Potentiometer          | 10 kΩ, 3-pin  | Reference/duty-cycle adjustment |
| Resistor               | 33 kΩ, ¼ W    | Feedback network                |
| Resistor               | 51 kΩ, ¼ W    | Feedback divider                |
| Resistor               | [VALUE]       | Biasing                         |
| Resistor               | 470 Ω, ¼ W    | Current limiting                |
| Breadboard             | MB102         | Circuit prototyping             |
| PCB                    | 8 cm × 6 cm   | Final circuit implementation    |
| Timer IC               | NE555         | PWM generation                  |
| Jumper Wires           | 23 AWG        | Circuit interconnections        |

The component list is based on the project document. The value of one biasing resistor is not clearly specified in the source document, so it is intentionally left as **[VALUE]** rather than assumed.

---

## 🖼️ Project Images

### 1. Physical Circuit

> **Add your physical circuit photograph here**

```markdown
![Physical Circuit](images/physical-circuit.jpg)
```

**Recommended photo:** A clear top-view photograph showing the complete assembled circuit.

---

### 2. Circuit Diagram

> **Add your circuit schematic/diagram here**

```markdown
![Circuit Diagram](images/circuit-diagram.png)
```


## 🔄 Control & Feedback

The closed-loop configuration improves voltage regulation compared with an open-loop converter.

The general feedback process is:

```text
          Reference Voltage
                 │
                 ▼
        ┌─────────────────┐
        │ Error Detection │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Control / PWM   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ MOSFET Switching │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Buck Converter  │
        └────────┬────────┘
                 │
                 ▼
             DC Output
                 │
                 │ Feedback
                 └───────────────►
```

The source document describes the feedback concept as continuously monitoring the output, comparing it with a reference, processing the error, and adjusting the switching signal accordingly.

---

## 🧪 Experimental Setup

The converter was first prototyped using an **MB102 breadboard** and jumper-wire connections. A double-sided universal PCB was specified for the final circuit implementation.

### Setup Photograph

```markdown
![Experimental Setup](images/experimental-setup.jpg)
```

---

## 📊 Results

Add your measured experimental results here.

| Parameter           |         Value |
| ------------------- | ------------: |
| Input Voltage       |        [XX V] |
| Output Voltage      |        [XX V] |
| Switching Frequency |   [XX Hz/kHz] |
| Duty Cycle          |        [XX %] |
| Output Ripple       |       [XX mV] |
| Load                | [XX Ω / XX W] |

### Output Results

```markdown
![Output Results](images/output-results.png)
```

> **Note:** These values should be replaced with your actual experimental measurements. The uploaded project document does not provide numerical experimental results.

---

## 📈 Expected Characteristics

The important characteristics to observe experimentally include:

* Input voltage
* Output voltage
* PWM duty cycle
* Switching waveform
* Output ripple
* Response to load variation
* Voltage regulation

You can add graphs such as:

```markdown
![Input vs Output Voltage](images/input-output-graph.png)
```

and

```markdown
![Output Voltage vs Duty Cycle](images/duty-cycle-graph.png)
```

---

## 💡 Applications

Buck converters are widely used in:

* 🔋 Battery-powered systems
* 💻 Embedded systems
* ⚡ Voltage regulation
* 🔌 Power supply systems
* 🔋 Battery charging systems
* 🤖 Embedded and electronic control systems

The project document specifically identifies applications including battery charging, embedded systems, and voltage regulation.

---

## ✅ Advantages

* Efficient voltage step-down conversion
* Better voltage regulation than an open-loop configuration
* PWM-based control
* Improved response to input/load variations
* Compact implementation
* Useful for understanding practical power electronics

The project document highlights improved regulation, reliability, and performance as benefits of closed-loop operation.

---

## 🚀 Future Improvements

The project can be further improved by:

* Implementing a dedicated PID controller.
* Adding digital voltage/current monitoring.
* Measuring converter efficiency under different loads.
* Adding over-current protection.
* Adding over-voltage protection.
* Studying transient response.
* Comparing open-loop and closed-loop performance.
* Designing a compact custom PCB.
* Adding microcontroller-based monitoring and control.

---

## 🛠️ Technologies & Concepts

**Hardware**

* NE555 Timer
* MOSFET
* Inductor
* Capacitors
* Resistors
* Potentiometer
* Breadboard
* Universal PCB

**Concepts**

* DC-DC Conversion
* Buck Converter
* PWM
* Feedback Control
* Voltage Regulation
* MOSFET Switching
* Energy Storage in Inductor
* Output Filtering
* Power Electronics

---

## 👥 Project Team

**Department of Electronics & Instrumentation Engineering**

| Name                    | Roll Number |
| ----------------------- | ----------- |
| Kuppala Sarath Narendra | 23UEI103    |
| Jigyasu                 | 23UEI104    |
| Prasun Kumar            | 23UEI105    |
| Shubhank                | 23UEI106    |
| Suhana Priyadarshini    | 23UEI107    |
| Aman Kumar              | 23UEI115    |
| Dhirendra Sahani        | 23UEI121    |
| Raj Das                 | 23UEI127    |

The team information is taken directly from the project document.

---

## 🎓 Academic Context

**Course/Lab:** Industrial Electronics & Process Control Lab
**Department:** Electronics & Instrumentation Engineering
**Project:** Closed-Loop Buck Converter

---

## 📁 Repository Structure

```text
Closed-Loop-Buck-Converter/
│
├── README.md
│
├── images/
│   ├── physical-circuit.jpg
│   ├── breadboard-prototype.jpg
│   ├── circuit-diagram.png
│   ├── pcb-implementation.jpg
│   ├── experimental-setup.jpg
│   ├── output-waveform.png
│   ├── output-results.png
│   ├── input-output-graph.png
│   ├── duty-cycle-graph.png
│   └── team-photo.jpg
│
├── documentation/
│   └── project-report.pdf
│
└── simulation/
    └── [simulation files]
```

---

## 📸 Recommended GitHub README Layout

For the best visual presentation, place your **main physical circuit photograph near the top** of the README:

```markdown
# 🔋 Closed-Loop Buck Converter

![Project](images/physical-circuit.jpg)

> A PWM-based closed-loop DC-DC buck converter for efficient
> voltage step-down and improved voltage regulation.
```

Then place the **circuit diagram and output waveform** in their respective sections.

---

## 📜 License

This project was developed for academic and educational purposes as part of the Industrial Electronics & Process Control Lab.

Feel free to use this project for **learning and educational reference**, with appropriate credit to the project team.

---

## ⭐ Acknowledgement

We would like to express our gratitude to the faculty and laboratory staff of the **Electronics & Instrumentation Engineering Department** for their guidance and support throughout the development of this project.

---

### 🔖 Keywords

`Buck Converter` · `Closed Loop Control` · `DC-DC Converter` · `PWM` · `NE555` · `MOSFET` · `Power Electronics` · `Voltage Regulation` · `Feedback Control` · `Industrial Electronics`
.jpg)
```

**Recommended photo:** A clear top-view photograph showing the complete assembled circuit.

---

### 2. Circuit Diagram

> **Add your circuit schematic/diagram here**

```markdown
![Circuit Diagram](images/circuit-diagram.png)
```



## 🔄 Control & Feedback

The closed-loop configuration improves voltage regulation compared with an open-loop converter.

The general feedback process is:

```text
          Reference Voltage
                 │
                 ▼
        ┌─────────────────┐
        │ Error Detection │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Control / PWM   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ MOSFET Switching │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Buck Converter  │
        └────────┬────────┘
                 │
                 ▼
             DC Output
                 │
                 │ Feedback
                 └───────────────►
```

The source document describes the feedback concept as continuously monitoring the output, comparing it with a reference, processing the error, and adjusting the switching signal accordingly.

---

## 🧪 Experimental Setup

The converter was first prototyped using an **MB102 breadboard** and jumper-wire connections. A double-sided universal PCB was specified for the final circuit implementation.

### Setup Photograph

```markdown
![Experimental Setup](images/experimental-setup.jpg)
```

---

## 📊 Results

Add your measured experimental results here.

| Parameter           |         Value |
| ------------------- | ------------: |
| Input Voltage       |        [XX V] |
| Output Voltage      |        [XX V] |
| Switching Frequency |   [XX Hz/kHz] |
| Duty Cycle          |        [XX %] |
| Output Ripple       |       [XX mV] |
| Load                | [XX Ω / XX W] |

### Output Results

```markdown
![Output Results](images/output-results.png)
```

> **Note:** These values should be replaced with your actual experimental measurements. The uploaded project document does not provide numerical experimental results.

---

## 📈 Expected Characteristics

The important characteristics to observe experimentally include:

* Input voltage
* Output voltage
* PWM duty cycle
* Switching waveform
* Output ripple
* Response to load variation
* Voltage regulation

You can add graphs such as:

```markdown
![Input vs Output Voltage](images/input-output-graph.png)
```

and

```markdown
![Output Voltage vs Duty Cycle](images/duty-cycle-graph.png)
```

---

## 💡 Applications

Buck converters are widely used in:

* 🔋 Battery-powered systems
* 💻 Embedded systems
* ⚡ Voltage regulation
* 🔌 Power supply systems
* 🔋 Battery charging systems
* 🤖 Embedded and electronic control systems

The project document specifically identifies applications including battery charging, embedded systems, and voltage regulation.

---

## ✅ Advantages

* Efficient voltage step-down conversion
* Better voltage regulation than an open-loop configuration
* PWM-based control
* Improved response to input/load variations
* Compact implementation
* Useful for understanding practical power electronics

The project document highlights improved regulation, reliability, and performance as benefits of closed-loop operation.

---

## 🚀 Future Improvements

The project can be further improved by:

* Implementing a dedicated PID controller.
* Adding digital voltage/current monitoring.
* Measuring converter efficiency under different loads.
* Adding over-current protection.
* Adding over-voltage protection.
* Studying transient response.
* Comparing open-loop and closed-loop performance.
* Designing a compact custom PCB.
* Adding microcontroller-based monitoring and control.

---

## 🛠️ Technologies & Concepts

**Hardware**

* NE555 Timer
* MOSFET
* Inductor
* Capacitors
* Resistors
* Potentiometer
* Breadboard
* Universal PCB

**Concepts**

* DC-DC Conversion
* Buck Converter
* PWM
* Feedback Control
* Voltage Regulation
* MOSFET Switching
* Energy Storage in Inductor
* Output Filtering
* Power Electronics

---

## 👥 Project Team

**Department of Electronics & Instrumentation Engineering**

| Name                    | Roll Number |
| ----------------------- | ----------- |
| Kuppala Sarath Narendra | 23UEI103    |
| Jigyasu                 | 23UEI104    |
| Prasun Kumar            | 23UEI105    |
| Shubhank                | 23UEI106    |
| Suhana Priyadarshini    | 23UEI107    |
| Aman Kumar              | 23UEI115    |
| Dhirendra Sahani        | 23UEI121    |
| Raj Das                 | 23UEI127    |

The team information is taken directly from the project document.

---

## 🎓 Academic Context

**Course/Lab:** Industrial Electronics & Process Control Lab
**Department:** Electronics & Instrumentation Engineering
**Project:** Closed-Loop Buck Converter

---

## 📁 Repository Structure

```text
Closed-Loop-Buck-Converter/
│
├── README.md
│
├── images/
│   ├── physical-circuit.jpg
│   ├── breadboard-prototype.jpg
│   ├── circuit-diagram.png
│   ├── pcb-implementation.jpg
│   ├── experimental-setup.jpg
│   ├── output-waveform.png
│   ├── output-results.png
│   ├── input-output-graph.png
│   ├── duty-cycle-graph.png
│   └── team-photo.jpg
│
├── documentation/
│   └── project-report.pdf
│
└── simulation/
    └── [simulation files]
```

---

## 📸 Recommended GitHub README Layout

For the best visual presentation, place your **main physical circuit photograph near the top** of the README:

```markdown
# 🔋 Closed-Loop Buck Converter

![Project](images/physical-circuit.jpg)

> A PWM-based closed-loop DC-DC buck converter for efficient
> voltage step-down and improved voltage regulation.
```

Then place the **circuit diagram and output waveform** in their respective sections.

---

## 📜 License

This project was developed for academic and educational purposes as part of the Industrial Electronics & Process Control Lab.

Feel free to use this project for **learning and educational reference**, with appropriate credit to the project team.

---

## ⭐ Acknowledgement

We would like to express our gratitude to the faculty and laboratory staff of the **Electronics & Instrumentation Engineering Department** for their guidance and support throughout the development of this project.

---

### 🔖 Keywords

`Buck Converter` · `Closed Loop Control` · `DC-DC Converter` · `PWM` · `NE555` · `MOSFET` · `Power Electronics` · `Voltage Regulation` · `Feedback Control` · `Industrial Electronics`
