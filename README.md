# AVR microcontroller lab 10

## Task

1. На базі розробленої у 9-й лабораторній роботі мережі RS-485 (один ATmega2560 та два ATmega328P) + CRC, спроектувати систему для збору даних із кінцевих давачів, що підключені до МК-Slave.
2. Розробити клієнтську програму (С++, C#, JavaScript) та написати для неї програмний код, що реалізовуватиме зв’язок між комп’ютером та МК «master» і відображатиме отримані дані з давачів.

**Параметри:**  
**RS-485**: швидкість передачі 9600 Бод  
**RS-232**: швидкість передачі 7200 Бод  
**Aдреси МК**: Slave1 = 88, Slave2 = 52  
**CRC**: CRC-16/CCIT-ZERO (таблична реалізація) для кожних 4 байтів інформації

![DS18S20 із паразитним живленням](https://i.imgur.com/74rmhVx.png)

### Специфікації алгоритмів CRC

| Name             | Poly   | Init   | RefIn | RefOut | XorOut |
| ---------------- | ------ | ------ | ----- | ------ | ------ |
| CRC-16/CCIT-ZERO | 0x1021 | 0x0000 | false | false  | 0x0000 |

## Getting Started

### Prerequisites

- Install [VS Code](https://code.visualstudio.com/Download)
- Install [PlatformIO](https://platformio.org/install/ide?install=vscode)
- Install [Proteus](https://www.labcenter.com/)
- Install [Python 3.8+](https://www.python.org/downloads/release/python-382/)

### Installing

- Clone repository into your system

```
git clone https://github.com/Ravenen/microcontroller_lab_10.git
```

- Activate Python virtual environment

  - Windows

  ```
  GUI\venv\Scripts\activate
  ```

  - Unix

  ```
  source GUI/venv/Scripts/activate
  ```

- Install requirements from `requirements.txt`

```
pip install -r GUI/requirements.txt
```

### Executing program

- Build a project in `code` folder via PlatformIO builder
- Run the `GUI/app.py` file
- Open Proteus project, configure COMPIM with COM port and speed, and run the simulation

## Authors

[Vitaliy Pavliyk (@ravenen)](https://github.com/Ravenen)
