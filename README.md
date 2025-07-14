# UART-Communication-in-C-Linux-

This project demonstrates a basic communication setup between **two UART (Universal Asynchronous Receiver-Transmitter) ports** on a Linux system. It uses the `libserialport` library to enable bidirectional serial communication with threading support.

---

## 🛠️ Build Instructions

Follow the steps below to build the project:

### 1. Install Required Dependencies

Ensure the `libserialport` development library is installed:

```bash
sudo apt-get update
sudo apt-get install libserialport-dev
```

### 2. Compile the Code

Use the `gcc` compiler with the following flags:

```bash
gcc -Wall -Wextra -pedantic -std=c11 main.c -o uart_comm_v1
```

---

## 📦 Dependencies

This project requires:

- `libserialport-dev`

Ensure it's installed before compiling the source code.

---

## ▶️ Usage Instructions

1. Connect two UART-capable devices (e.g., USB-to-Serial converters) to available COM ports on your Linux machine.

2. Launch the compiled executable:

```bash
./uart_comm_v1
```

3. The program will prompt for two UART port numbers:
   - **Thread 1** → handles the first COM port (input)
   - **Thread 2** → handles the second COM port (output)

4. The selected ports are configured at a baud rate of **115200 bps**.

5. A system message queue is created to handle packet transfer between threads.

6. Type a message on the terminal → it will be sent from Thread 1 to Thread 2.

7. The received message appears in real time on the output terminal.

---

## 🧪 Example Session

```txt
Enter COM port number for Thread 1: 1
Enter COM port number for Thread 2: 2

Type packet data: Hello UART
[Thread 2] Received: Hello UART
```

You can continue to send and receive messages interactively between the two connected UART devices.

---

## 🧠 Learning Outcomes

- Gained hands-on experience with UART-based communication on Linux.
- Practiced multithreading with POSIX threads.
- Worked with system-level file I/O using `/dev/tty*` ports.
- Utilized `libserialport` for portable and flexible serial communication.

---
