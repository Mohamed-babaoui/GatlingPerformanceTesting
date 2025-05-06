# GatlingPerformanceTesting
This is a repo descibes Gatling Performance testing project 
# CPWeb Performance Test Engine

## 🚀 Project Overview

The **CPWeb Performance Test Engine** is a Java-based test automation framework that combines **Gatling** for performance testing with **Selenium WebDriver** for UI interaction. It is designed to simulate real user behavior on a web reservation system and measure application performance under load.

This engine goes beyond basic simulation by automatically generating performance reports, comparing them to previous runs, visualizing trends with graphs, and sending the results via email.

---

## 🎯 Key Objectives

- ✅ Simulate full user journeys (login, search, reservation, confirmation) on the CPWeb portal.
- ✅ Measure key performance metrics: response times, errors, throughput, standard deviation, etc.
- ✅ Compare current performance results with past executions.
- ✅ Generate summary files (`output.txt`, `compare.txt`) for traceability.
- ✅ Produce a visual graph of response time over time (`graph.png`).
- ✅ Send a detailed email report with all result files attached.

---

## 🧩 Project Structure

```plaintext
.
├── simulations/
│   └── CPWebSimulation.java          # Main Gatling simulation using CPWeb1 and CPWeb2
├── scenarios/
│   ├── CPWeb1Scenario.java           # User scenario 1 (login → reservation → confirmation)
│   └── CPWeb2Scenario.java           # User scenario 2 (alternative journey)
├── engine/
│   └── CPWebEngine.java              # Main launcher with log analysis, graph creation, and email reporting
├── config/
│   └── utils/
│       ├── BrowserManager.java       # Manages Selenium WebDriver instances
│       └── Methods.java              # Utilities (e.g. email sending)
├── resources/
│   ├── config.properties             # User credentials and base URL
│   └── testdata2.properties          # Test-specific input data
├── src/test/oldCP/                   # Previous execution results (used for comparison)
└── target/gatling/                   # Gatling results output

