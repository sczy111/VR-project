# Basic Guide

## 🕹 Basic Interactions

- **X Button**:  
  Triggers the **first teleport**.  
  After teleporting, the **Rating UI** will appear. Select your rating to automatically teleport to the next location.

- **B Button**:  
  Toggles the **Quitting menu**.

- **Rating Selection**:
  - Use the **left-hand joystick** to choose a rating (1–5).
  - Press the **left-hand trigger** to confirm your selection.
  - ⚠️ _Note_: In rare cases during testing, the left-hand joystick may freeze. If this happens, move your **right hand** towards the rating menu and there will be a ray allowing you to point at the rating and press the **right-hand trigger** to select it.

## 💻 System Specs & Performance Notes

This project was developed and tested on a low-end laptop with:

- **GPU**: NVIDIA RTX 3050 (Laptop version)
- **CPU**: AMD Ryzen 5000 Series
- **VR App Warning**: The Meta Quest app reports this system as **not meeting the minimum requirements** for VR.

**Headset Settings**:

- **Refresh Rate**: 72 Hz
- **Rendering Resolution**: 3616 × 1856

Despite the hardware limitations, the scene ran **relatively smoothly** during testing. Performance is expected to **significantly improve** on higher-end systems with increased refresh rate and resolution.

## LSL Output

To monitor LSL (Lab Streaming Layer) output, run the following command in Windows Command Prompt or use your own methods:
`python -m pylsl.examples.ReceiveStringMarkers`

### Marker Values:

- **10**: Normal scene (`PostProcessingVolume.Unbound = False`)
- **11**: Weird scene (`PostProcessingVolume.Unbound = True`)
- **1–5**: Rating selected by the user

After going through **200 target points**, a CSV file will be automatically exported to: `C:/Users/Public/`

The file includes:

- Target Point Index
- User Rating (1–5)
- Post Processing Volume State (Unbound or not)
- Sun Angle

---

_Enjoy testing the VR experience!_
