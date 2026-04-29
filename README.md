import numpy as np
import matplotlib.pyplot as plt

def simulate_breathing(duration=60, rate=12):
    """
        Simulates respiratory cycles over a given duration.
            :param duration: Total time in seconds
                :param rate: Breaths per minute
                    """
                        fs = 100  # Sampling frequency
                            t = np.linspace(0, duration, duration * fs)
                                
                                    # Frequency in Hz (breaths per second)
                                        freq = rate / 60
                                            
                                                # Simulate lung volume (Sine wave: 0 to 1 range)
                                                    volume = 0.5 * (1 + np.sin(2 * np.pi * freq * t))
                                                        
                                                            return t, volume

                                                            if __name__ == "__main__":
                                                                time, vol = simulate_breathing()
                                                                    
                                                                        plt.figure(figsize=(10, 4))
                                                                            plt.plot(time[:1000], vol[:1000]) # Plot first 10 seconds
                                                                                plt.title("Simulated Respiratory Cycle")
                                                                                    plt.xlabel("Time (s)")
                                                                                        plt.ylabel("Lung Volume (Normalized)")
                                                                                            plt.grid(True)
                                                                                                plt.show()

                                                                                                # Respiratory Simulation Tool

                                                                                                A lightweight Python utility to simulate and visualize human respiratory cycles.

                                                                                                ## 🚀 Features
                                                                                                * **Customizable Rates:** Adjust breaths per minute (BPM) and duration.
                                                                                                * **Visualization:** Generates clear plots of lung volume over time.
                                                                                                * **Clean Code:** Modular design for easy integration into larger health-tech projects.

                                                                                                ## 🛠️ Installation
                                                                                                1. Clone this repository:
                                                                                                   ```bash
                                                                                                      git clone https://github.com
                                                                                                         ```
                                                                                                         2. Install dependencies:
                                                                                                            ```bash
                                                                                                               pip install numpy matplotlib
                                                                                                                  ```

                                                                                                                  ## 💻 Usage
                                                                                                                  Run the main script to generate a sample 60-second breathing simulation:
                                                                                                                  ```bash
                                                                                                                  python respiratory_sim.py
                                                                                                                  ```

                                                                                                                  ## 📊 Sample Output
                                                                                                                  The tool produces a normalized sine wave representing the rhythmic expansion and contraction of the lungs.

                                                                                                                  ## 📄 License
                                                                                                                  Distributed under the MIT License.
                                                                                                                  