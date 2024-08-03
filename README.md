# Anomaly Detection for Aerial Adversaries Dataset

This repository contains a dataset for the purpose of anomaly detection in aerial adversaries. The dataset is structured to include both benign and spoofed signal data, captured in different scenarios and distances. The data is provided in two formats: `.bits` and `.bits.iq`.

## Folder Structure

The repository is organized as follows:

```
.
├── Benign
│ ├── iq
│ │ └── (IQ data files)
│ └── (raw bits data files)
├── LICENSE
└── Spoofed
├── All Scenarios
│ ├── iq
│ │ └── (IQ data files)
│ └── (raw bits data files)
├── Scenario 1 ~ Static
│ ├── iq
│ │ └── (IQ data files)
│ └── (raw bits data files)
├── Scenario 2 ~ Moving TX
│ ├── iq
│ │ └── (IQ data files)
│ └── (raw bits data files)
└── Scenario 3 ~ Moving TX & RX
├── iq
│ └── (IQ data files)
└── (raw bits data files)
```


## Dataset Description

### Benign
The `Benign` folder contains data representing normal, non-spoofed signals. The data is available in both raw bits and IQ (in-phase and quadrature) formats.

### Spoofed
The `Spoofed` folder contains data representing various spoofing scenarios. The data is categorized into three main scenarios and one combined folder:
1. **All Scenarios**: Contains all spoofed data.
2. **Scenario 1 ~ Static**: Data where the transmission is static.
3. **Scenario 2 ~ Moving TX**: Data where the transmitter (TX) is moving.
4. **Scenario 3 ~ Moving TX & RX**: Data where both the transmitter (TX) and receiver (RX) are moving.

Each scenario folder contains data in both raw bits and IQ formats, captured at different distances ranging from 10m to 120m.

## Usage

### Loading Data
To load and process the data, you can use any standard data processing tool compatible with `.bits` and `.bits.iq` formats. For example, you can use Python with libraries like `numpy` and `scipy` to handle IQ data.

### Example
```python
import numpy as np

# Load IQ data
iq_data = np.fromfile('path_to_file.bits.iq', dtype=np.complex64)

# Process the data
# (Add your processing code here)
```

### Custom Data Files
The `.bits` files are outputs from a custom version of [gr-iridium](https://github.com/muccc/gr-iridium), which is a GNU Radio implementation for processing Iridium satellite signals. These files contain the raw captured data for further analysis.

