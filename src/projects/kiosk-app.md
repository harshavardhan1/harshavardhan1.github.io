# Self-Ordering Kiosk Web Application


## Core Technical Architecture
* **Frontend Engine:** React JS (Modular Presentation Components)
* **Data Fetching & State:** TanStack Query, React Hook Form (RHF)
* **Native Integration Layer:** Electron JS
* **Design & Motion:** Shadcn UI, Tailwind CSS, Framer Motion (GPU Accelerated)
* **Real-time Pipeline:** Firebase Cloud Messaging, i18next, Storybook

## Feature Deep-Dive & Key Deliverables

### 1. Decoupled Core Architecture (UI Cloning System)
* **Implementation:** Built a highly predictable core React engine that completely isolated core business logic, API routes, and local state engines from visual layout sheets.
* **Impact:** Created a reusable standalone template blueprint allowing the development team to rapidly clone and spin up entirely unique client UI layouts without altering underlying functional stability.

### 2. Reactive Data Layer
* **Implementation:** Integrated Firebase Cloud Messaging to run asynchronous background data updates over active connections.
* **Impact:** Allowed the kiosk hardware to capture instant database state changes and menu updates silently without requiring continuous, resource-heavy client polling cycles.

### 3. GPU-Accelerated UI Rendering Metrics
* **Implementation:** Optimized component render lifecycles utilizing React Pure Components alongside dynamic list/component virtualization. Custom UI micro-interactions and transitions were bound to CSS transform properties using Framer Motion.
* **Impact:** Offloaded layout computations directly to the GPU, entirely eliminating frame-rate drops on resource-constrained physical touchscreen hardware.

### 4. Native Hardware Bridge Engine
* **Implementation:** Configured a native Electron JS wrapper running on top of the web codebase to bypass standard web browser hardware communication security sandboxes.
* **Impact:** Created direct bindings into local Windows OS-level printer drivers, unlocking automated, zero-latency thermal physical receipt printing directly from the checkout stream.