# Vehicle-performance-
Vehicle Performance Evaluation using MATLAB Simulink

This project simulates and evaluates a basic vehicle performance logic using MATLAB and Simulink. The model reads speed and acceleration signals from external data, evaluates driving conditions, and switches between two driving modes based on dynamic thresholds.

---

## 📁 Project Structure

| File                      | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `Simulink_performance.slx`| Simulink model that performs the drive mode evaluation                      |
| `signalData.mat`          | Contains a `Simulink.SimulationData.Dataset` with speed and acceleration signals |
| `signalDataProgram.mlx`   | MATLAB Live Script used to generate synthetic signal data                   |

---

## 🚗 Simulation Logic

The Simulink model uses two input signals:
- **Speed** (in km/h)
- **Acceleration** (in m/s²)

It evaluates the following condition:

If speed ≥ 100 OR (speed ≥ 35 AND abs(acceleration) ≥ 3)
→ Drive Mode 2
Else
→ Drive Mode 1


The output signal indicates the active drive mode at each time step.

---

## ⚙️ How to Run the Project

1. **Open MATLAB**
2. Run `signalDataProgram.mlx` to regenerate `signalData.mat` (optional)
3. Open `Simulink_performance.slx`
4. In the **Signal Editor** block or **From Workspace** block, ensure it loads from `signalData.mat`
5. Click **Run** to simulate
6. Observe the output signal to see drive mode switching

---

## 📌 Requirements

- MATLAB (R2021b or later recommended)
- Simulink
- Simulink Signal Editor / From Workspace block support

---

## 📊 Output

The simulation will output a signal indicating whether **Drive Mode 1** or **Drive Mode 2** is active based on real-time input values.

---

## ✅ Customization

You can modify the conditions or add new sensors/signals by updating the `signalDataProgram.mlx` and regenerating the `signalData.mat` file.

---

## 🔒 License

This project is open for educational and research use. Attribution appreciated.

---

## 📬 Contact

Feel free to reach out if you have questions or suggestions!

