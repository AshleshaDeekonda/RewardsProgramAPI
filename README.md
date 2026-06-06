# RewardsProgramAPI

A Spring Boot REST API built to calculate customer loyalty reward points dynamically across multiple transaction profiles within rolling multi-month intervals.

## Calculation Blueprint
* 2 points for every dollar spent over $100.
* 1 point for every dollar spent between $50 and $100.

## Engineering Architecture & Standards
* **Decoupled Strategy**: Pure separation of operations between domain entities, translation models (DTOs), processing algorithms, and REST gateways.
* **Agile Calendar Calculations**: Leverages Java `java.time.LocalDate` grouping strategies preventing static array monthly locks.
* **Robust Safety Nets**: Implements global structural exception intercepts targeting dirty/negative values gracefully.

## Project Structure Diagram
rewards-program/
├── src/
│   ├── main/java/com/retailer/rewardsprogram/
│   │     ├── controller/       <-- API Interfaces
│   │     ├── dto/              <-- Wire Contract Layer
│   │     ├── exception/        <-- Error Interceptors
│   │     ├── model/            <-- Entities
│   │     └── service/          <-- Calculation Engine
│   └── test/                   <-- Unit & Integration Suites
└── pom.xml
