---
title: "Engine ECS"
date: 2025-06-07
layout: page
categories: [gamedev]
tags: [linux,cpp,sdl2]
---

# SDL2 Engine - High-Performance 2D ECS Game Engine

Welcome to the official repository and development journal of **SDL2 Engine**, a high-performance 2D game engine built from scratch using **modern C++26** features. This project is an ongoing effort to explore advanced programming paradigms, performance optimization techniques, and modern build systems while creating a flexible and scalable foundation for 2D games. *Jejeje, yes that was IA :D*

## 🚀 Project Overview

SDL2 Engine is an independent, solo-developed Entity Component System (ECS) engine designed with performance, modularity, and maintainability in mind. **Now** its on Data Oriented Desing, for an excellent performance. It leverages the latest C++ standards and tools to deliver a robust framework for building complex 2D applications.

### 🔧 Technologies & Tools
- **C++26**: Modern language features including ranges, lambdas, monads, reflection, and more.
- **CMake**: Build system.
- **Conan2**: Package management for external dependencies.
- **CLion**: Primary IDE for development and debugging.
- **SDL2**: Graphics, input, and windowing subsystems.
- **Valgrind & Profiling Tools**: Memory leak detection and performance analysis.

---

## 📈 Development Highlights & Progress

This engine has evolved significantly through multiple iterations, each aimed at improving architecture, performance, and usability.

### 🛠️ Architectural Evolution

#### V1 – The Foundation

- Inspired by classic OOP tutorials (e.g., Pikuma)
- Heavy use of inheritance and class hierarchies
- Performance bottlenecks due to inefficient loops and poor memory layout

#### V2 – True ECS Architecture

- Query-based entity filtering system
- Composition over inheritance
- SparseSet-based component storage for fast access
- Event Bus for decoupled communication between systems
- **Result**: Performance increase — handling 10K entities at 60 FPS vs. 12 FPS in V1

#### V3 – Hybrid Experimentation

- Merged V1 and V2 concepts to test hybrid models
- Ultimately reverted to pure ECS model for clarity and long-term maintainability

#### V4 – Current, using Data Oriented Design

- Re-build again, using DOD.
- Query-based entity filtering system
- SparseSet-based component storage for fast access
- Event Bus for decoupled communication between systems
- Almost 100% Composition.
- Cache in Systems.
- In V1, V2, V3 I had to limit the calls to Physics and Collision Systems, in this version I dont.
- **Result**: Performance increase — handling 90K entities at 60 FPS.

---

## ⚙️ Performance Optimizations

I have applied numerous optimizations across systems to ensure the engine remains lightweight and responsive:

- **CollisionSystem**: Added `is_sleeping` flag to skip inactive bodies
- **ScenarioManager**: Finite State Machine for smooth scene transitions
- **Time Management**: Replaced `SDL_Delay` with `std::chrono` + `std::thread` for precise timing control
- **Rendering**: Implemented camera subsystems with zoom, follow, and viewport culling
- **Build Optimization**: Disabled RTTI (`-fno-rtti`) to reduce binary size
- **Precompiled Headers**: Speed up compilation times using CMake support

---

## 💻 Modern C++26 Features Used

The engine makes heavy use of modern C++ features to improve safety, expressiveness, and efficiency:

- **Functional Programming Paradigm**
  - Lambdas for callbacks and inline logic
  - Monads (e.g., optional chaining, error handling via `std::expected`)
  - Functional composition using `std::function`, `std::bind`

- **Ranges & Views**
  - `std::ranges` for declarative querying of entities
  - `std::views` for lazy evaluation and transformations
  - Custom views for filtering and iterating components

- **Language Enhancements**
  - `std::variant`, `std::optional`, `std::reference_wrapper`
  - Early experiments with **C++26 static reflection**
  - RAII principles throughout the codebase
  - `_` naming convention for unused variables

---

## 🧪 Tooling & Integration

A strong focus on tooling ensures seamless integration and extensibility:

- **CMake**: For modular.
- **SDL2**: For rendering, audio, and input handling
- **SQLite**: For save/load state persistence
- **Tiled/JSON**: Level design pipeline with custom parsers
- **Spatial Partitioning**: Benchmarking spatial hashing vs quad-trees for collision resolution

---

## 🧬 Future Roadmap

I actively exploring next-gen patterns and features:

- **Archetypes**: Testing archetype-based storage as an alternative to SparseSets
- **Multithreading**: Job system for PhysicsSystem inspired by `entt::scheduler`
- **C++26 Reflection**: Auto-generating serialization code for components
- **Coroutines**: Exploring `std::generator` for coroutine-based systems
- **Scripting Layer**: Potential integration with Lua or Python bindings

---

## 🖼️ Screenshots

Check out some visual progress of the engine in action:

![Game Screenshot 01](https://github.com/chriztheanvill/SDL2_Engine/raw/v0.0.8-Fusion/Screenshots/Game_show_01.png)  
![Game Screenshot 02](https://github.com/chriztheanvill/SDL2_Engine/raw/v0.0.8-Fusion/Screenshots/Game_show_02.png)  
![Game Screenshot 03](https://github.com/chriztheanvill/SDL2_Engine/raw/v0.0.8-Fusion/Screenshots/Game_show_03.png)  
![Game Screenshot 04](https://github.com/chriztheanvill/SDL2_Engine/raw/v0.0.8-Fusion/Screenshots/Game_show_04.png)  
![Game Screenshot 05](https://github.com/chriztheanvill/SDL2_Engine/raw/v0.0.8-Fusion/Screenshots/Game_show_05.png)

---

## 🌐 Branches

-[`v0.0.2-DOD Current`](https://github.com/chriztheanvill/SDL2_Engine/tree/v0.0.2-DOD)
- [`0.0.8-alt`](https://github.com/chriztheanvill/SDL2_Engine/tree/0.0.8-alt): Experimental branch focusing on architectural flexibility
- [`v0.0.8-Fusion`](https://github.com/chriztheanvill/SDL2_Engine/tree/v0.0.8-Fusion): Main development branch with integrated systems

---

## 📚 Git

- [GitHub Repository](https://github.com/chriztheanvill/SDL2_Engine)

---

## 🧑‍💻 Developed By: Cris

Software Engineer | Game Dev Enthusiast  

