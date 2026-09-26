# LSM-MediaPipe-SVM

[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![IEEE](https://img.shields.io/badge/Paper-IEEE%20Latin%20America%20Transactions-blue)]()

Reproducible benchmark of classifiers for the static alphabet of Mexican Sign Language (LSM) on GPU-less hardware.

## 📌 Overview

This repository contains the full source code, trained models, and reproducible results for the paper:

> **"Reproducible Benchmark of Classifiers for the Static Alphabet of Mexican Sign Language on GPU-less Hardware"**
> Juan Juárez Fuentes, Hugo Alberto Flores Arguedas, Eduardo Sánchez Soto
> *IEEE Latin America Transactions* (under review)

The system recognizes the static alphabet of Mexican Sign Language (LSM) in real time using:

- **MediaPipe Hands** for 21 hand landmarks extraction (63 normalized features)
- **SVM with RBF kernel** as the final classifier
- **No GPU required** — runs on a standard CPU (Ryzen 5, 16 GB RAM)

## 🎯 Results

| Model | Accuracy | Train time (s) | Inference (ms) |
|-------|----------|----------------|----------------|
| Linear SVM | 97.53% | 230.54 | 0.65 |
| **RBF SVM** | **99.36%** | **174.41** | **1.20** |
| k-NN (k=5) | 99.09% | 0.43 | 2.30 |
| MLP (128, 64) | 99.63% | 327.85 | 1.85 |

- **Real-time performance:** 16.8 FPS with full GUI
- **Hardware:** Dell Ryzen 5, 16 GB RAM, no dedicated GPU
- **Validation:** service-robotics simulation on 11×11 grid

## 📁 Repository structure
