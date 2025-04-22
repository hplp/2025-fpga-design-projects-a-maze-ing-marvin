# Phase II Update! 

We’re excited to share that the **DS-CNN model has been trained and integrated** with the maze game code! The game runs using the laptop's onboard microphone and is functional. The only remaining hurdle is deploying the game on the **PYNQ-Z1 board**. While this has come with its fair share of challenges, we’re optimistic that everything will be running smoothly by the delivery date.

---

## DS-CNN Model Update
- ✅ Model implemented and trained on our dataset  
- ✅ Exported to `.tflite` format for efficient inference  
- ✅ Deployed on the FPGA as a lightweight inference model  

> Check out `speechCommand.ipynb` for the full implementation!

---

## Game Development Update
- 🔍 Initially found a public domain maze game  
- ⚠️ Discovered that **`pygame`** doesn't work in Jupyter Notebooks  
- 🛠️ Built a custom maze-style game using graphing tools to simulate maze logic and visuals
> Check out `IMPLEMENTATION.md` for the full story and photos, and 'GameAttempt2.ipynb' for the code!
---

## Integration Progress
- ⚠️ The PYNQ board's default Python version wasn’t compatible with `tflite-runtime`  
  → ✅ Installed **Python 3.7** on the FPGA  
- ✅ Created a new environment and successfully installed `tflite-runtime`  
- ✅ Installed supporting packages: `numpy`, Jupyter Notebook dependencies, etc.  
- ✅ `tflite-runtime` is now **operational in a dedicated kernel** for our project  
- 🔍 Attempted to use `sounddevice` for mic input  
  → ❌ Mic libraries didn’t detect the board’s microphone  
- ⚙️ Currently working on installing **PYNQ**  
  → This involves integrating board-specific hardware files with the new Python environment  

> We’re currently troubleshooting the install of pynq so that we can use the overlay library to get audio data, but we expect that once it works, our game will be entirely deployed on the board!
