# Organic/Inorganic Classification

"Comparacion de la eficacia de los sensores de humedad, capacitivo y camara con vision artificial para clasificar residuos organicos e inorganicos"

This project compares low-cost sensing approaches for classifying waste as organic or inorganic. The current direction combines Arduino sensor readings with a camera or AI-assisted workflow so the hardware and model outputs can be tested side by side.

## Goals

- Compare humidity, capacitive, and camera-based signals for waste classification.
- Keep Arduino examples easy to test one sensor at a time.
- Document the expected project layout so future code, data, and model files are easier to find.
- Leave room for an integrated system that combines sensors, serial output, and the AI/webcam pipeline.

## Hardware

The project is expected to use:

- Arduino-compatible board
- DHT11 or DHT22 humidity sensor
- Capacitive or inductive sensor modules
- Camera or webcam for visual classification
- Jumper wires, breadboard, and a stable USB power/data connection

Exact pin mappings should live beside each Arduino sketch so wiring can be checked before uploading code.

## Repository Layout

```text
arduino/
  sensors/
    DHT11/
      DHT11_standalone/
        DHT11_standalone.ino
      README.md
ai-model/
database/
```

`arduino/` contains firmware examples and setup notes for the hardware side of the project. The first starter slice currently documents and tests a standalone DHT11 sketch.

`ai-model/` should hold training, inference, preprocessing, configuration, and model documentation once the classification pipeline is added.

`database/` should hold dataset notes, source links, raw/processed data references, labels, and generated outputs. Large datasets or model files should usually be linked instead of committed directly.

## Arduino Setup

1. Install the Arduino IDE or `arduino-cli`.
2. Install the board package for your Arduino-compatible board.
3. Install the required sensor libraries for the sketch you are testing.
4. Open the sketch under `arduino/sensors/<sensor-name>/`.
5. Check the pin map in the sensor README before wiring.
6. Compile and upload the sketch.
7. Open the serial monitor and confirm the output format.

For the DHT11 starter sketch, install:

- `DHT sensor library`
- `Adafruit Unified Sensor`

## Data And Model Notes

Future AI/model work should document:

- dataset source links and licensing
- raw versus processed data format
- preprocessing steps
- training command and expected outputs
- inference command or webcam integration path
- evaluation metrics and sample predictions

## Current Status

The repository is still being organized. The Arduino folder has a starter DHT11 example, while the AI model and database folders still need the structure and documentation described in the open issues.

## Contributing

Small, focused contributions are easiest to review. Good next steps include adding one sensor example at a time, documenting one dataset source at a time, or adding a narrow README section that matches files already present in the repository.
