# Mapty - Workout Tracking Application

Mapty is a web application designed for tracking running and cycling workouts. It allows users to add new workouts, visualize them on a map, and store their workout history locally. This project uses object-oriented programming principles and is built with JavaScript, HTML, and CSS.

## Features

- Add running and cycling workouts with distance, duration, and additional stats.
- View workouts as markers on a map.
- Zoom into workout locations by clicking on the workout list.
- Data persistence with `localStorage`, so workouts remain saved even after refreshing the page.

## Application Overview

Mapty is structured using OOP principles, with key classes and methods to manage workouts and application logic.

### Architecture Diagram

The following diagram showcases the architecture of the Mapty application:

![Mapty Architecture](15-Mapty/Mapty-architecture-part-1.png)

### Workflow Flowchart

The workflow of the application can be visualized in the following flowchart:

![Mapty Flowchart](./Mapty-flowchart.png)

## Classes and Methods

### `Class Workout`
This serves as a base class for all types of workouts and includes:
- `id`, `distance`, `duration`, `coords`, etc.
- Methods such as `_setDescription()` for setting descriptions of workouts and `click()`.

### `Child Class Running` and `Child Class Cycling`
Inherit from `Workout` and contain additional properties and methods specific to their type.

### `Class App`
Handles application state, including:
- `workouts`: An array to store workout instances.
- `_loadMap()`, `_newWorkout()`, `_renderWorkout()`, and other utility methods to manage UI and data.

## Application Workflow

1. **Page Loads**:
   - The user's current location is fetched.
   - The map is rendered at the user's location.
   - Existing workouts are loaded from `localStorage`.

2. **User Interactions**:
   - Clicking on the map prompts the user to add a new workout.
   - After the user submits the form, the workout is stored and rendered both on the map and in the workout list.
   - Clicking on a workout in the list moves the map to the workout's location.

## Getting Started

### Prerequisites
To run this project locally, you need:
- A browser that supports ES6.
- Internet connection to use Leaflet.js for maps.

### Installation
1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/mapty.git
   cd mapty
