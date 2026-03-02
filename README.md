# GT3-telemetry
#Python telemetry analysis for Mercury GT3 racecar. Lap time evolution, sector analysis, ML tire prediction
import matplotlib.pyplot as plt

# Mercury GT3 lap times (rubbering-in effect)
laps = list(range(1,16))
times = [95.2,94.8,94.1,93.9,93.7,93.5,93.4,93.6,93.8,94.0,94.2,94.5,94.8,95.1,95.4]

plt.figure(figsize=(10,6))
plt.plot(laps, times, 'o-', linewidth=2, markersize=6)
plt.xlabel('Lap Number')
plt.ylabel('Lap Time (seconds)')
plt.title('Mercury GT3 - Rubbering In Effect')
plt.grid(True, alpha=0.3)
plt.tight_layout()
plt.savefig('_laps.png', dpi=150)
plt.show()
