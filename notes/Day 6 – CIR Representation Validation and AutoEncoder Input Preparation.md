**Error Mitigation for TDoA UWB Indoor Localization Using Unsupervised Machine Learning**

## Objective

The objective of Day 6 was to perform a deeper validation of the raw CIR
representation and prepare the CIR data for the convolutional AutoEncoder
described in the paper.

Following the initial dataset exploration performed on Day 5, this stage
focused on validating the hexadecimal CIR representation, decoding the raw
samples into signed int16 values, verifying the I/Q structure, and determining
the correct input representation for the AutoEncoder.

---

## Dataset Re-validation

The selected dataset remains:

`data/Rack/Processed_full.csv`

The dataset contains:

- Total records: **100557**
- Dataset features: **48**
- Invalid/unusable CIR records: **69**
- Valid CIR records used in the final preprocessing pipeline: **100233**

Each valid CIR contains:

- **2400 hexadecimal characters**
- **1200 bytes**
- **600 signed little-endian int16 values**
- **300 I/Q pairs**

---

## CIR Decoding

The hexadecimal CIR strings were decoded using signed little-endian int16
representation.

The resulting decoded CIR dataset has the following characteristics:

| Item | Value |
|------|------:|
| Valid CIR samples | 100233 |
| Decoded values per sample | 600 |
| I/Q pairs per sample | 300 |
| Data type | int16 |
| Minimum | -16511 |
| Maximum | 16509 |
| Mean | 64.0832 |
| Standard deviation | 938.0722 |

The presence of both positive and negative values confirms that the CIR
samples must be interpreted as signed values rather than unsigned bytes.

---

## I/Q Representation Validation

Each CIR sample contains 600 signed int16 values.

These values can be grouped into 300 I/Q pairs:

```text
[I0, Q0]
[I1, Q1]
[I2, Q2]
...
[I299, Q299]
