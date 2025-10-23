---
title: "Godot Game Cpp"
date: 2025-06-07
layout: page
categories: [gamedev]
tags: [linux,cpp,godot]
---

# C++26-Powered 2D RPG (Godot Engine)
*A Souls-like / Bullet-Hell*

This project represents an ambitious blend of modern C++ development practices and game design innovation. Built using **Godot Engine** and deeply integrated with **C++26**, it showcases how cutting-edge language features can enhance performance, maintainability, and expressiveness in real-time applications like games.

---

## Development Stack

- **Language**: Modern C++26 (with `-fno-rtti` for binary optimization)
- **Build System**: CMake + Conan2 for dependency management
- **IDE**: CLion
- **Tools**: Valgrind, Profiling tools, Precompiled Headers (via CMake), SQLite

---

## Recent Advancements

### Performance Improvements
We've achieved a **massive boost in runtime efficiency** thanks to:
- Heavy use of `std::ranges` and `std::views` for zero-copy data processing.
- Functional-style composition over imperative loops.
- Removal of RTTI (`-fno-rtti`) to reduce binary size and improve load times.
- Use of precompiled headers via CMake for faster compilation cycles.

### Architectural Enhancements
- **Event Bus System**: Implemented a lightweight event bus using `std::function` and lambdas for decoupled communication between subsystems (e.g., GUI ↔ combat logic).
- **Monads in Practice**: Introduced monadic structures for optional chaining (e.g., safe item usage, stat checks) inspired by functional programming patterns.

### Data Handling & Persistence
- **SQLite Integration**: Used SQLite not only for saving player progression but also for dynamic queries such as tracking "most used weapon" or crafting stats.

---

## Core Technologies in Depth

### C++26 Highlights
- **`std::ranges` / `std::views`**: For efficient, readable filtering and transformations on enemy groups or inventory items.
- **`std::function` & Lambdas**: As the backbone of event-driven systems (GUI events, AI behaviors).
- **Compile-Time Optimization**: With Conan2 and CMake, we’ve streamlined build pipelines and ensured reproducibility.

---

## Development Workflow

- **Code Quality & Debugging**
  - Static analysis via Clang-Tidy
  - Memory profiling with Valgrind
  - Real-time CPU/GPU profiling inside Godot

- **Toolchain**
  - CLion for code navigation and refactoring
  - Git Submodules for engine integration

---

## Game Features Overview

| Feature                   | Description                                           |
| ------------------------- | ----------------------------------------------------- |
| **Souls-like Combat**     | Stamina system, dodge rolls, parry mechanics          |
| **Bullet-Hell Mechanics** | Complex projectile patterns, hitbox/hurtbox precision |
| **Fallout-Inspired RPG**  | Stats, skills, crafting, inventory systems            |
| **Handcrafted Levels**    | Interconnected metroidvania-style maps                |

---

## Looking Ahead

- More advanced AI using behavior trees powered by functional combinators
- Shader-based VFX enhancements

---
