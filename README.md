# Concurrent Airline Reservation Server

A robust, multi-client airline reservation platform designed to demonstrate advanced concepts in Linux system programming, TCP/UDP socket communication, and concurrency control.

## 📌 Overview
This project simulates a real-time airline ticketing backend where Airline Management Servers, Airline Clients, and Customer Clients interact concurrently. The system utilizes TCP sockets for reliable transactions (like booking and registration) and UDP broadcast sockets for real-time announcements (like new flights). It is strictly implemented using Linux system calls.

## 🚀 Key Features
* **TCP/UDP Socket Programming:** Reliable client-server communication using IPv4 sockets (`<sys/socket.h>`).
* **Non-Blocking Concurrency:** Multiplexing I/O operations using the `select()` system call to handle multiple simultaneous user connections without blocking the main thread.
* **Temporary Reservations (Timers):** Implementation of a 30-second hold limit on reservations using `SIGALRM` and the `alarm()` system call, automatically freeing expired seats.
* **Role-Based Workflows:** Distinct operations for Airlines (creating flights, mapping seat rows/columns) and Customers (viewing, reserving, confirming, and canceling seats).
* **Real-time UDP Broadcasting:** Automated notifications sent to all active clients when a new user registers or a new flight is added.

## 🛠️ Tech Stack
* **Language:** C/C++
* **OS APIs:** Linux System Calls (POSIX Sockets, Signals, Select, read/write)
* **Build Tool:** Make
